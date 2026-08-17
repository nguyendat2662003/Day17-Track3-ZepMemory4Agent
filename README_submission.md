# README_submission — Lab 17 Multi-Memory Agent

**Kết quả:** practice 11/11 · golden v3 20/20 (`perfect: true`) · baseline no-memory 2/11 · pytest 12/12.

## Ba câu bắt buộc

**1. Layer quan trọng nhất: long-term.** Quyết định 4/11 case (E02 preference, E03 open loop, E08 recency, E09 isolation) và là nguồn của E07. Baseline: long-term 0/4 khi thiếu bộ nhớ bền vững, short-term vẫn 2/2 vì bằng chứng nằm sẵn trong thread.

**2. Trade-off Zep vs Redis+Qdrant.** Zep cho sẵn Context Block đã tổng hợp, tự tách phạm vi khi fact mâu thuẫn, giữ `valid_at`/`invalid_at`. Tự build cần KV cho profile, vector DB cho ngữ nghĩa, cộng tầng tóm tắt và xử lý conflict. Giá phải trả: latency ~1450 ms (semantic chỉ ~250 ms), phụ thuộc dịch vụ ngoài, ingest bất đồng bộ phải polling, và không kiểm soát cách tóm tắt — Context Block trả tiếng Anh dù nguồn tiếng Việt.

**3. Guardrail chống memory poisoning.** (a) `require_memory_consent` chặn ingest khi chưa opt-in. (b) `ignore_roles=["user"]` để câu hỏi không thành fact bền vững. (c) `minimize_pii` redact email/phone. (d) Heartbeat chỉ dedupe và đánh dấu stale, không tự thêm chỉ thị mới. (e) `user_id` ở mọi call, E09 canh bằng `must_not_contain`.

## Bốn câu phân tích

**1.** Bản student không layer nào thấp — cả 5 đều 100%. Baseline mới lộ: long_term 0/4, episodic 0/2, semantic 0/2, mixed 0/1, short_term 2/2. Mong manh nhất là **mixed** — layer duy nhất bị trim, mọi case từng fail (E07, G16, G18) đều là mixed.

**2.** Tốn token nhất: **E03, 1574 token** (Context Block + 20 fact có provenance).

**3.** E07 cần **long-term + semantic**; evidence bắt buộc `Python` và `Idempotency-Key`.

**4.** Memory giảm 12.6% token; no-memory giảm 81.8% nhưng hit rate chỉ 18.2% vì không retrieve gì. Reduction chỉ có nghĩa khi đọc cùng hit rate.

## E08 recency và E10 compaction

**E08:** Zep không ghi đè mà **tách phạm vi** — BLUEBIRD-42 dùng TypeScript/NestJS, ORCHID-27 vẫn Python. Nhờ vậy E02 và E08 pass bằng cùng một Context Block; ghi đè thô sẽ fail E02.

**E10:** sau 8 lần nén, turn chứa constraint bị evict khỏi `<RECENT_TURNS>`, nhưng `REVIEW-DEADLINE-1600 / Friday / 16:00` sống trong `<DURABLE_NOTES>` nhờ khớp từ khoá và regex mã hoa. Buffer thuần sẽ tràn; tóm tắt văn xuôi mất `16:00` trước tiên.

*`Dockerfile`: thêm `PIP_DEFAULT_TIMEOUT`/`PIP_RETRIES` vá read timeout PyPI khi build.*

# Lab 17 Benchmark Report

- Implementation: `student`
- Kind: `practice`
- Cases: **11**
- Passed: **11/11**
- Evidence hit rate: **100.0%**
- Average retrieval latency: **837.0 ms**
- Average token reduction vs full source context: **12.6%**

| Case | Layer | Pass | Latency ms | Retrieved tokens | Token reduction | Missing / Error |
| --- | --- | --- | ---: | ---: | ---: | --- |
| E01 | short_term | PASS | 0.0 | 133 | 0.0% |  |
| E06 | semantic | PASS | 779.3 | 180 | 60.8% |  |
| E09 | long_term | PASS | 1213.1 | 840 | 0.0% |  |
| E10 | short_term | PASS | 0.3 | 195 | 0.0% |  |
| E02 | long_term | PASS | 1150.3 | 1512 | 0.0% |  |
| E03 | long_term | PASS | 1219.9 | 1551 | 0.0% |  |
| E04 | episodic | PASS | 797.1 | 233 | 0.0% |  |
| E05 | episodic | PASS | 228.7 | 267 | 0.0% |  |
| E07 | mixed | PASS | 2094.4 | 516 | 8.7% |  |
| E11 | semantic | PASS | 240.8 | 177 | 68.7% |  |
| E08 | long_term | PASS | 1483.5 | 1486 | 0.0% |  |

## Evidence excerpts

### E01 - short_term

`<RECENT_TURNS> user: Ten du an ca nhan cua toi la ORCHID-27. Toi thich Python va khong thich Java. Khi giai thich code, hay dung vi du ngan. assistant: Da hieu: demo ca nhan ORCHID-27, uu tien Python, tranh Java, vi du ngan. user: Toi dang hoc async/await va hay nham coroutine voi Task. Neu sau nay gap chu de nay, hay giai thich bang timeline. assistant: Toi se uu tien timeline khi giai thich coroutine va Task. user: TODO: hoan thanh benchmark report truoc thu Sau luc 16:00. Day la open loop LAB-REPORT-1600. </RECENT_TURNS>`

### E06 - semantic

`<KEY_MARKERS> nential-backoff, and stop after max-3-retries. Marker: PAYMENT-RULE-3.","source":"internal-api </KEY_MARKERS>  EPISODE: {"id":"kb-payment-retry","entity":"Payment API Retry Policy","summary":"For POST /payments, every retryable request MUST send the same Idempotency-Key. Retry only HTTP 429 or transient 5xx errors, use exponential-backoff, and stop after max-3-retries. Marker: PAYMENT-RULE-3.","source":"internal-api-guideline-v3","updated_at":"2026-08-10T00:00:00Z"} metadata= EPISODE: For POST /payments, every retryable request MUST send the same Idempotency-Key. Retry only HTTP 429 or transient 5xx errors, use exponential-backoff, and stop after max-3-retries. Marker: PAYMENT-`

### E09 - long_term

`<KEY_MARKERS> <USER_SUMMARY> Lan's project is LOTUS-88, and they prioritize Jav </KEY_MARKERS>  <USER_SUMMARY> Lan's project is LOTUS-88, and they prioritize Java and Spring Boot for backend examples.  Lan prioritizes Java and Spring Boot for backend development and explicitly avoids Python for backend tasks. </USER_SUMMARY>  <EPISODES> Episodes are source message or document excerpts shown in selection order.   - Created At: 2026-08-01 11:00:20     Source: message     Content: Lab Assistant (assistant): Da hieu: LOTUS-88, Java + Spring Boot cho backend examples.   - Created At: 2026-08-01 11:00:00     Source: message     Content: [user] {   "user_id": "lan-lab17",   "first_name": "Lan",   "`

### E10 - short_term

`<SESSION_SUMMARY> user: Constraint: REVIEW-DEADLINE-1600 - project review is Friday at 16:00 and must not be forgotten. | assistant: Acknowledged review constraint. | user: Filler turn 1 about UI spacing. | assistant: Filler answer 1. | user: Filler turn 2 about naming. | assistant: Filler answer 2. | user: Filler turn 3 about logging. | assistant: Filler answer 3. </SESSION_SUMMARY> <DURABLE_NOTES> - user: Constraint: REVIEW-DEADLINE-1600 - project review is Friday at 16:00 and must not be forgotten. - assistant: Acknowledged review constraint. </DURABLE_NOTES> <RECENT_TURNS> user: Filler turn 4 about tests. assistant: Filler answer 4. user: Filler turn 5 about docs. assistant: Filler answe`

### E02 - long_term

`<KEY_MARKERS> <USER_SUMMARY> The user's personal project is named ORCHID-27, for which Python is pre is preferred. They are working on the company project BLUEBIRD-42, which requires a backen </KEY_MARKERS>  <USER_SUMMARY> The user's personal project is named ORCHID-27, for which Python is preferred. They are working on the company project BLUEBIRD-42, which requires a backend implemented in TypeScript with NestJS, not Python.  The user prefers Python and dislikes Java. They are currently learning about async/await and sometimes confuse coroutines with Tasks. When this topic arises, they prefer explanations presented as a timeline. For the company project BLUEBIRD-42, the backend must use Ty`

### E03 - long_term

`<KEY_MARKERS> <USER_SUMMARY> The user's personal project is named ORCHID-27, for which Python is pre is preferred. They are working on the company project BLUEBIRD-42, which requires a backen hmark report truoc thu Sau luc 16:00. Day la open loop LAB-REPORT-1600. </EPISODES> <FACTS> Th timeout threshold, as the primary issue related to the ASYNC-FIX-20 incident. </ENTITIES> < </KEY_MARKERS>  <USER_SUMMARY> The user's personal project is named ORCHID-27, for which Python is preferred. They are working on the company project BLUEBIRD-42, which requires a backend implemented in TypeScript with NestJS, not Python.  The user prefers Python and dislikes Java. They are currently learning about asyn`

### E04 - episodic

`EPISODE: Hom nay toi debug async HTTP. Toi da thu tang timeout len 60s nhung van fail. EPISODE: Cach hieu qua la reuse aiohttp ClientSession va dat concurrency=20. Reflection: loi chinh la connection churn, khong phai timeout threshold. Ma su co ASYNC-FIX-20. EPISODE: Da ghi nhan trajectory: increase timeout khong hieu qua; ClientSession + concurrency=20 giai quyet connection churn. EPISODE: Cap nhat moi: voi du an cong ty BLUEBIRD-42, backend bat buoc dung TypeScript voi NestJS; khong dung Python cho backend du an nay. Preference Python van dung cho demo ca nhan ORCHI EPISODE: TODO: hoan thanh benchmark report truoc thu Sau luc 16:00. Day la open loop LAB-REPORT-1600. EPISODE: Ten du an ca `

### E05 - episodic

`EPISODE: Hom nay toi debug async HTTP. Toi da thu tang timeout len 60s nhung van fail. EPISODE: Hay kiem tra connection pool, lifecycle cua client va concurrency. EPISODE: Cach hieu qua la reuse aiohttp ClientSession va dat concurrency=20. Reflection: loi chinh la connection churn, khong phai timeout threshold. Ma su co ASYNC-FIX-20. EPISODE: Da ghi nhan trajectory: increase timeout khong hieu qua; ClientSession + concurrency=20 giai quyet connection churn. EPISODE: Cap nhat moi: voi du an cong ty BLUEBIRD-42, backend bat buoc dung TypeScript voi NestJS; khong dung Python cho backend du an nay. Preference Python van dung cho demo ca nhan ORCHI EPISODE: TODO: hoan thanh benchmark report truoc`

### E07 - mixed

`<LONG_TERM> <KEY_MARKERS> <USER_SUMMARY> The user's personal project is named ORCHID-27, for which Python is pre is preferred. They are working on the company project BLUEBIRD-42, which requires a backen </KEY_MARKERS>  <USER_SUMMARY> The user's personal project is named ORCHID-27, for which Python is preferred. They are working on the company project BLUEBIRD-42, which requires a backend implemented in TypeScript with NestJS, not Python.  The user prefers Python and dislikes Java. They are currently learning about async/await and sometimes confuse coroutines with Tasks. When this topic arises, they prefer explanations presented as a timeline. For the company project BLUEBIRD-42, the backend`

### E11 - semantic

`<KEY_MARKERS> se a long-lived client session where possible. Marker: CONN-POOL-FIRST.","source":"incident-pla </KEY_MARKERS>  EPISODE: {"id":"kb-async-http","entity":"Async HTTP Incident Playbook","summary":"When async HTTP calls time out, inspect connection pooling, downstream saturation and concurrency before increasing timeout. Reuse a long-lived client session where possible. Marker: CONN-POOL-FIRST.","source":"incident-playbook-2026","updated_at":"2026-08-11T00:00:00Z"} metadata= EPISODE: When async HTTP calls time out, inspect connection pooling, downstream saturation and concurrency before increasing timeout. Reuse a long-lived client session where possible. Marker: CONN-POOL-FIRST. m`

### E08 - long_term

`<KEY_MARKERS> <USER_SUMMARY> The user's personal project is named ORCHID-27, for which Python is pre is preferred. They are working on the company project BLUEBIRD-42, which requires a backen </KEY_MARKERS>  <USER_SUMMARY> The user's personal project is named ORCHID-27, for which Python is preferred. They are working on the company project BLUEBIRD-42, which requires a backend implemented in TypeScript with NestJS, not Python.  The user prefers Python and dislikes Java. They are currently learning about async/await and sometimes confuse coroutines with Tasks. When this topic arises, they prefer explanations presented as a timeline. For the company project BLUEBIRD-42, the backend must use Ty`

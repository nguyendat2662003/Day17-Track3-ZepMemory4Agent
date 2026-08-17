# Lab 17 Golden Set Report

- Implementation: `student`
- Kind: `golden`
- Cases: **20**
- Passed: **20/20**
- Evidence hit rate: **100.0%**
- Average retrieval latency: **1153.4 ms**
- Average token reduction vs full source context: **3.9%**
- Golden bonus: **10/10** (100% required)

| Case | Layer | Pass | Latency ms | Retrieved tokens | Token reduction | Missing / Error |
| --- | --- | --- | ---: | ---: | ---: | --- |
| G01 | short_term | PASS | 0.3 | 227 | 0.0% |  |
| G02 | short_term | PASS | 0.1 | 133 | 0.0% |  |
| G06 | long_term | PASS | 1550.7 | 884 | 0.0% |  |
| G09 | semantic | PASS | 273.5 | 445 | 3.0% |  |
| G10 | semantic | PASS | 278.2 | 273 | 40.5% |  |
| G14 | mixed | PASS | 2629.4 | 581 | 0.0% |  |
| G03 | long_term | PASS | 1382.1 | 1550 | 0.0% |  |
| G04 | long_term | PASS | 1433.5 | 1561 | 0.0% |  |
| G07 | episodic | PASS | 300.2 | 272 | 0.0% |  |
| G08 | episodic | PASS | 266.5 | 291 | 0.0% |  |
| G11 | mixed | PASS | 2078.9 | 581 | 0.0% |  |
| G13 | mixed | PASS | 545.9 | 500 | 11.5% |  |
| G15 | mixed | PASS | 2103.8 | 831 | 0.0% |  |
| G16 | mixed | PASS | 1585.3 | 581 | 0.0% |  |
| G17 | mixed | PASS | 1661.5 | 581 | 0.0% |  |
| G18 | mixed | PASS | 523.4 | 500 | 11.5% |  |
| G19 | mixed | PASS | 1593.2 | 581 | 0.0% |  |
| G05 | long_term | PASS | 1369.6 | 1566 | 0.0% |  |
| G12 | mixed | PASS | 1673.7 | 563 | 10.9% |  |
| G20 | mixed | PASS | 1817.7 | 756 | 0.0% |  |

## Evidence excerpts

### G01 - short_term

`<SESSION_SUMMARY> user: Constraint HOLD-ALPHA-0900: standup is 09:00 sharp and must not be forgotten. | assistant: Noted standup constraint. | user: Constraint HOLD-BETA-STAGING: writes go to staging DB only. | assistant: Noted staging constraint. | user: Filler A about button padding. | assistant: Filler A. | user: Filler B about color tokens. | assistant: Filler B. | user: Filler C about copy tone. | assistant: Filler C. </SESSION_SUMMARY> <DURABLE_NOTES> - user: Constraint HOLD-ALPHA-0900: standup is 09:00 sharp and must not be forgotten. - assistant: Noted standup constraint. - user: Constraint HOLD-BETA-STAGING: writes go to staging DB only. - assistant: Noted staging constraint. </DURA`

### G02 - short_term

`<RECENT_TURNS> user: Ten du an ca nhan cua toi la ORCHID-27. Toi thich Python va khong thich Java. Khi giai thich code, hay dung vi du ngan. assistant: Da hieu: demo ca nhan ORCHID-27, uu tien Python, tranh Java, vi du ngan. user: Toi dang hoc async/await va hay nham coroutine voi Task. Neu sau nay gap chu de nay, hay giai thich bang timeline. assistant: Toi se uu tien timeline khi giai thich coroutine va Task. user: TODO: hoan thanh benchmark report truoc thu Sau luc 16:00. Day la open loop LAB-REPORT-1600. </RECENT_TURNS>`

### G06 - long_term

`<KEY_MARKERS> <USER_SUMMARY> Lan Tran's project is LOTUS-88, and they prioritize Jav </KEY_MARKERS>  <USER_SUMMARY> Lan Tran's project is LOTUS-88, and they prioritize Java and Spring Boot for backend development examples. They do not use Python in this context.  Lan Tran prioritizes Java and Spring Boot for backend development. </USER_SUMMARY>  <EPISODES> Episodes are source message or document excerpts shown in selection order.   - Created At: 2026-08-01 11:00:00     Source: message     Content: [user] {   "user_id": "lan-lab17",   "first_name": "Lan",   "last_name": "Tran",   "user_alias": "Lan Tran" }: Toi la Lan. Du an cua toi la LOTUS-88. Toi uu tien Java va Spring Boot, va khong dung `

### G09 - semantic

`<KEY_MARKERS> nential-backoff, and stop after max-3-retries. Marker: PAYMENT-RULE-3.","source":"internal-api ped memory and be verified across every store. Marker: DELETE-VERIFY-ALL.","source":"memory-gover c 3 percent; trim lower-priority memory first. Marker: BUDGET-10-4-3-3.","source":"lab-design-n </KEY_MARKERS>  EPISODE: {"id":"kb-payment-retry","entity":"Payment API Retry Policy","summary":"For POST /payments, every retryable request MUST send the same Idempotency-Key. Retry only HTTP 429 or transient 5xx errors, use exponential-backoff, and stop after max-3-retries. Marker: PAYMENT-RULE-3.","source":"internal-api-guideline-v3","updated_at":"2026-08-10T00:00:00Z"} metadata= EPISODE: Fo`

### G10 - semantic

`<KEY_MARKERS> ped memory and be verified across every store. Marker: DELETE-VERIFY-ALL.","source":"memory-gover c 3 percent; trim lower-priority memory first. Marker: BUDGET-10-4-3-3.","source":"lab-design-n </KEY_MARKERS>  EPISODE: {"id":"kb-memory-privacy","entity":"Agent Memory Privacy Rule","summary":"Do not persist personal data without explicit opt-in. A deletion request must remove user-scoped memory and be verified across every store. Marker: DELETE-VERIFY-ALL.","source":"memory-governance-policy","updated_at":"2026-08-12T00:00:00Z"} metadata= EPISODE: Do not persist personal data without explicit opt-in. A deletion request must remove user-scoped memory and be verified across every `

### G14 - mixed

`<LONG_TERM> <KEY_MARKERS> <USER_SUMMARY> Lan Tran's project is LOTUS-88, and they prioritize Jav </KEY_MARKERS>  <USER_SUMMARY> Lan Tran's project is LOTUS-88, and they prioritize Java and Spring Boot for backend development examples. They do not use Python in this context.  Lan Tran prioritizes Java and Spring Boot for backend development. </USER_SUMMARY>  <EPISODES> Episodes are source message or document excerpts shown in selection order.   - Created At: 2026-08-01 11:00:00     Source: message     Content: [user] {   "user_id": "lan-lab17",   "first_name": "Lan",   "last_name": "Tran",   "user_alias": "Lan Tran" }: Toi la Lan. Du an cua toi la LOTUS-88. Toi uu tien Java va Spring Boot, va`

### G03 - long_term

`<KEY_MARKERS> <USER_SUMMARY> The user's personal project is named ORCHID-27, for which they prefer P for which they prefer Python. For the company project BLUEBIRD-42, the backend must use Ty ction churn, not the timeout threshold, related to the ASYNC-FIX-20 incident. Minh prefers </KEY_MARKERS>  <USER_SUMMARY> The user's personal project is named ORCHID-27, for which they prefer Python. For the company project BLUEBIRD-42, the backend must use TypeScript with NestJS, and Python is not to be used for this project. The user needs to complete a benchmark report for ORCHID-27 before Saturday at 16:00. They are currently debugging async HTTP requests and have tried increasing the timeout to 60s`

### G04 - long_term

`<KEY_MARKERS> <USER_SUMMARY> The user's personal project is named ORCHID-27, for which they prefer P for which they prefer Python. For the company project BLUEBIRD-42, the backend must use Ty ction churn, not the timeout threshold, related to the ASYNC-FIX-20 incident. Minh prefers hmark report truoc thu Sau luc 16:00. Day la open loop LAB-REPORT-1600. </EPISODES> <FACTS> Th </KEY_MARKERS>  <USER_SUMMARY> The user's personal project is named ORCHID-27, for which they prefer Python. For the company project BLUEBIRD-42, the backend must use TypeScript with NestJS, and Python is not to be used for this project. The user needs to complete a benchmark report for ORCHID-27 before Saturday at 16:00`

### G07 - episodic

`EPISODE: Hom nay toi debug async HTTP. Toi da thu tang timeout len 60s nhung van fail. EPISODE: Hay kiem tra connection pool, lifecycle cua client va concurrency. EPISODE: Cach hieu qua la reuse aiohttp ClientSession va dat concurrency=20. Reflection: loi chinh la connection churn, khong phai timeout threshold. Ma su co ASYNC-FIX-20. EPISODE: Da ghi nhan trajectory: increase timeout khong hieu qua; ClientSession + concurrency=20 giai quyet connection churn. EPISODE: Ten du an ca nhan cua toi la ORCHID-27. Toi thich Python va khong thich Java. Khi giai thich code, hay dung vi du ngan. EPISODE: Da hieu: demo ca nhan ORCHID-27, uu tien Python, tranh Java, vi du ngan. EPISODE: Toi dang hoc async`

### G08 - episodic

`EPISODE: Hom nay toi debug async HTTP. Toi da thu tang timeout len 60s nhung van fail. EPISODE: Hay kiem tra connection pool, lifecycle cua client va concurrency. EPISODE: Cach hieu qua la reuse aiohttp ClientSession va dat concurrency=20. Reflection: loi chinh la connection churn, khong phai timeout threshold. Ma su co ASYNC-FIX-20. EPISODE: Da ghi nhan trajectory: increase timeout khong hieu qua; ClientSession + concurrency=20 giai quyet connection churn. EPISODE: Ten du an ca nhan cua toi la ORCHID-27. Toi thich Python va khong thich Java. Khi giai thich code, hay dung vi du ngan. EPISODE: Toi dang hoc async/await va hay nham coroutine voi Task. Neu sau nay gap chu de nay, hay giai thich `

### G11 - mixed

`<LONG_TERM> <KEY_MARKERS> <USER_SUMMARY> The user's personal project is named ORCHID-27, for which they prefer P for which they prefer Python. For the company project BLUEBIRD-42, the backend must use Ty ction churn, not the timeout threshold, related to the ASYNC-FIX-20 incident. Minh prefers d_at=None] FACT: The benchmark report is identified as LAB-REPORT-1600. [valid_at=2026-08-01T09 </KEY_MARKERS>  <USER_SUMMARY> The user's personal project is named ORCHID-27, for which they prefer Python. For the company project BLUEBIRD-42, the backend must use TypeScript with NestJS, and Python is not to be used for this project. The user needs to complete a benchmark report for ORCHID-27 before Satu`

### G13 - mixed

`<EPISODIC> EPISODE: Hom nay toi debug async HTTP. Toi da thu tang timeout len 60s nhung van fail. EPISODE: Hay kiem tra connection pool, lifecycle cua client va concurrency. EPISODE: Cach hieu qua la reuse aiohttp ClientSession va dat concurrency=20. Reflection: loi chinh la connection churn, khong phai timeout threshold. Ma su co ASYNC-FIX-20. EPISODE: Da ghi nhan trajectory: increase timeout khong hieu qua; ClientSession + concurrency=20 giai quyet connection churn. EPISODE: Cuoi tuan minh ngoi mot minh lam demo rieng, khong hop team. Truoc khi chon template, nhac lai: khi lam viec ca nhan minh uu tien ngon ngu nao, va ma du an demo ca nhan la gi? Chi  EPISODE: Ten du an ca nhan cua toi la`

### G15 - mixed

`<LONG_TERM> <KEY_MARKERS> <USER_SUMMARY> The user's personal project is named ORCHID-27, for which they prefer P for which they prefer Python. For the company project BLUEBIRD-42, the backend must use Ty ction churn, not the timeout threshold, related to the ASYNC-FIX-20 incident. Minh prefers </KEY_MARKERS>  <USER_SUMMARY> The user's personal project is named ORCHID-27, for which they prefer Python. For the company project BLUEBIRD-42, the backend must use TypeScript with NestJS, and Python is not to be used for this project. The user needs to complete a benchmark report for ORCHID-27 before Saturday at 16:00. They are currently debugging async HTTP requests and have tried increasing the ti`

### G16 - mixed

`<LONG_TERM> <KEY_MARKERS> <USER_SUMMARY> The user's personal project is named ORCHID-27, for which they prefer P for which they prefer Python. For the company project BLUEBIRD-42, the backend must use Ty ction churn, not the timeout threshold, related to the ASYNC-FIX-20 incident. Minh prefers to be completed by Friday at 16:00. This is open loop LAB-REPORT-1600. </ENTITIES> <THREADS> </KEY_MARKERS>  <USER_SUMMARY> The user's personal project is named ORCHID-27, for which they prefer Python. For the company project BLUEBIRD-42, the backend must use TypeScript with NestJS, and Python is not to be used for this project. The user needs to complete a benchmark report for ORCHID-27 before Saturda`

### G17 - mixed

`<LONG_TERM> <KEY_MARKERS> <USER_SUMMARY> The user's personal project is named ORCHID-27, for which they prefer P for which they prefer Python. For the company project BLUEBIRD-42, the backend must use Ty ction churn, not the timeout threshold, related to the ASYNC-FIX-20 incident. Minh prefers </KEY_MARKERS>  <USER_SUMMARY> The user's personal project is named ORCHID-27, for which they prefer Python. For the company project BLUEBIRD-42, the backend must use TypeScript with NestJS, and Python is not to be used for this project. The user needs to complete a benchmark report for ORCHID-27 before Saturday at 16:00. They are currently debugging async HTTP requests and have tried increasing the ti`

### G18 - mixed

`<EPISODIC> EPISODE: Toi nay minh viet tool ca nhan de tai hien su co HTTP roi sua dung playbook. Can ba manh: ngon ngu minh thich khi lam mot minh, ma su co async lan truoc, va buoc playbook truoc khi EPISODE: Minh con mot open-loop phai nop truoc deadline, dong thoi muon ghi chu retry payment dung so lan toi da theo policy. Nac lai ma task/deadline con dang do, va gioi han retry chinh t EPISODE: Hom nay toi debug async HTTP. Toi da thu tang timeout len 60s nhung van fail. EPISODE: Hay kiem tra connection pool, lifecycle cua client va concurrency. EPISODE: Cach hieu qua la reuse aiohttp ClientSession va dat concurrency=20. Reflection: loi chinh la connection churn, khong phai timeout thresho`

### G19 - mixed

`<LONG_TERM> <KEY_MARKERS> <USER_SUMMARY> The user's personal project is named ORCHID-27, for which they prefer P for which they prefer Python. For the company project BLUEBIRD-42, the backend must use Ty ction churn, not the timeout threshold, related to the ASYNC-FIX-20 incident. Minh prefers </KEY_MARKERS>  <USER_SUMMARY> The user's personal project is named ORCHID-27, for which they prefer Python. For the company project BLUEBIRD-42, the backend must use TypeScript with NestJS, and Python is not to be used for this project. The user needs to complete a benchmark report for ORCHID-27 before Saturday at 16:00. They are currently debugging async HTTP requests and have tried increasing the ti`

### G05 - long_term

`<KEY_MARKERS> <USER_SUMMARY> The user's personal project is named ORCHID-27, for which they prefer P for which they prefer Python. For the company project BLUEBIRD-42, the backend must use Ty ction churn, not the timeout threshold, related to the ASYNC-FIX-20 incident. Minh prefers </KEY_MARKERS>  <USER_SUMMARY> The user's personal project is named ORCHID-27, for which they prefer Python. For the company project BLUEBIRD-42, the backend must use TypeScript with NestJS, and Python is not to be used for this project. The user needs to complete a benchmark report for ORCHID-27 before Saturday at 16:00. They are currently debugging async HTTP requests and have tried increasing the timeout to 60s`

### G12 - mixed

`<LONG_TERM> <KEY_MARKERS> <USER_SUMMARY> The user's personal project is named ORCHID-27, for which they prefer P for which they prefer Python. For the company project BLUEBIRD-42, the backend must use Ty ction churn, not the timeout threshold, related to the ASYNC-FIX-20 incident. Minh prefers 08:00:20Z] FACT: The benchmark report is identified as LAB-REPORT-1600. [valid_at=2026-08-01T09 </KEY_MARKERS>  <USER_SUMMARY> The user's personal project is named ORCHID-27, for which they prefer Python. For the company project BLUEBIRD-42, the backend must use TypeScript with NestJS, and Python is not to be used for this project. The user needs to complete a benchmark report for ORCHID-27 before Satu`

### G20 - mixed

`<SHORT_TERM> <SESSION_SUMMARY> user: Constraint HOLD-ALPHA-0900: standup is 09:00 sharp and must not be forgotten. | assistant: Noted standup constraint. | user: Filler about dashboard widgets. | assistant: Filler. | user: Filler about CSS variables. | assistant: Filler. | user: Filler about copy review. | assistant: Filler. </SESSION_SUMMARY> <DURABLE_NOTES> - user: Constraint HOLD-ALPHA-0900: standup is 09:00 sharp and must not be forgotten. - assistant: Noted standup constraint. </DURABLE_NOTES> <RECENT_TURNS> user: Filler about empty charts. assistant: Filler. user: Filler about telemetry. assistant: Filler. user: Filler about a11y labels. assistant: Filler. </RECENT_TURNS> </SHORT_TERM>`

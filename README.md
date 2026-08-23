# Liam Makoni

Software Developer at Hear and Hack and Computer Science student at the University of Nottingham, graduating in 2027. I build backend systems in TypeScript/Node.js and Go, mainly around concurrency and reliable asynchronous processing.

## Selected work

- **[job-queue-service](https://github.com/liam-m9/job-queue-service):** TypeScript and PostgreSQL queue using `SELECT ... FOR UPDATE SKIP LOCKED` for disjoint concurrent claims, visibility-timeout recovery and at-least-once processing. Measured at roughly 700 jobs per second with one local worker.
- **[webhook-delivery-service](https://github.com/liam-m9/webhook-delivery-service):** TypeScript and Redis delivery service with durable exponential backoff, atomic Lua claiming, HMAC signing, replay detection and stable delivery ids for consumer deduplication.
- **[rate-limiter](https://github.com/liam-m9/rate-limiter):** Sliding-window HTTP rate limiter in Go using per-key locks over `sync.Map`, tested with 200 goroutines and `go test -race`.
- **[tutor-lead-capture](https://github.com/liam-m9/tutor-lead-capture):** Flask API on AWS Lambda behind API Gateway, with PostgreSQL persistence, Turnstile verification and per-IP rate limiting.

## Stack

TypeScript, Node.js, Go, PostgreSQL, Redis, Docker, Python and AWS Lambda.

## Contact

[LinkedIn](https://linkedin.com/in/liam-makoni) | liam.makoni9@gmail.com

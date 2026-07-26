## Liam Makoni

Backend engineer, final-year Computer Science at the University of Nottingham. I build services in Node.js and Go, mostly around concurrency and reliable async processing. Every repo below documents its design decisions and its known limitations, not just what it does.

In Dubai until 20 September 2026, remote after that. UAE resident with full right to work. An employer files a MoHRE family-sponsorship work permit against my existing residence and Emirates ID. No new residence visa, medical or biometrics required.

### Projects

- **[job-queue-service](https://github.com/liam-m9/job-queue-service)**: Durable job queue on PostgreSQL alone, no Redis and no queue library. `SELECT ... FOR UPDATE SKIP LOCKED` lets concurrent workers claim disjoint batches without double-claiming. Around 700 jobs/sec single-worker, measured end-to-end against local Postgres.
- **[webhook-delivery](https://github.com/liam-m9/webhook-delivery)**: HMAC-SHA256 signed webhook delivery. Retries are scheduled in a Redis sorted set keyed by next-due timestamp, so per-delivery exponential backoff survives a process restart. Ingest API, dispatcher and receiver run as three separate processes over real HTTP.
- **[rate-limiter](https://github.com/liam-m9/rate-limiter)**: Sliding-window HTTP rate limiter in Go. Per-key mutexes rather than a global lock, so different clients never block each other. Verified with 200 goroutines racing a single key under `go test -race`.

### Stack

Node.js · Go · PostgreSQL · Redis · Docker · Python · SQL

### Contact

liam.makoni9@gmail.com · [LinkedIn](https://linkedin.com/in/liam-makoni)

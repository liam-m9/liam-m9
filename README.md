# Liam Makoni

Computer Science student at the University of Nottingham, graduating in 2027 and looking for graduate software engineering roles from September 2027. I build backend systems in TypeScript/Node.js and Go, mainly around concurrent job processing, retries and testing what actually happens under concurrency. Most recently I was a Software Developer at Hear and Hack (Aug to Sep 2026).

## Selected work

- **[job-queue-service](https://github.com/liam-m9/job-queue-service):** PostgreSQL-only job queue in TypeScript using `SELECT ... FOR UPDATE SKIP LOCKED`, so workers on separate machines can claim jobs without blocking. Linear-backoff retries, a terminal dead state for repeated handler failures, and lease-based crash reclaim with at-least-once processing. A concurrent-claim test found no job claimed twice.
- **[webhook-delivery-service](https://github.com/liam-m9/webhook-delivery-service):** Webhook delivery in TypeScript and Redis with exponential-backoff retries in a sorted set and atomic Lua claiming (15 concurrent claimers took all 100 due deliveries, none claimed twice), plus HMAC-SHA256 signing, replay detection and stable delivery IDs for consumer-side deduplication.
- **[rate-limiter](https://github.com/liam-m9/rate-limiter):** Sliding-window rate-limiting middleware in Go. A 200-goroutine test enforces the configured limit and runs clean under the race detector; `Allow` benchmarks at about 87 ns/op, and distinct-key parallel calls ran about 4x faster than single-key contention.
- **Duplo (university group project):** a team-built Rust toolchain that transforms and compiles C code. I built the browser playground and compiler API, and implemented and unit-tested four of its trigger strategies. The code is on the university's GitLab.
- **[tutoring-business](https://github.com/liam-m9/tutoring-business):** website and enquiry form for a GCSE maths tutor (client project), with a Flask API on AWS Lambda, PostgreSQL, bot checks and parameterised SQL.

## Stack

TypeScript, Node.js, Go, PostgreSQL, Redis, Rust, Python, Next.js, Supabase, Flask, AWS Lambda, Docker and GitHub Actions.

## Contact

[LinkedIn](https://linkedin.com/in/liam-makoni) | liam.makoni9@gmail.com

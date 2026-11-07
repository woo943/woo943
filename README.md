Hi, I'm Hyeonwoo 👋
I'm a software engineering student at Sungkyunkwan University seeking a backend engineering internship. My experience spans React and Next.js team development and a Python/FastAPI capstone, where I worked on API design, data integrity, and reproducible tests. My next focus is Spring Boot, building on my Java fundamentals.
Featured project · Swing Trading Assistant
Capstone · Python · FastAPI · Pydantic · pytest · React Native / Expo Web

A local research demo that tracks technical-analysis setups across trading days. It separates the Python analysis pipeline, persisted results and state, and the web-facing read API.
- API and system design. Built a read-only FastAPI API for a monthly index, daily summaries, and symbol details with charts. The API serves saved snapshots to Expo Web independently of the analysis run. Summary and detail files are stored separately so a single request reads only the data it needs.
- Data integrity. Preserved the distinction between a zero score, an unavailable score (null), blocked inputs, and cases that were never evaluated. The snapshot index is replaced atomically after writes complete. A withdrawn snapshot returns 409, and an integrity failure returns 503.
- Verification. The local demo was verified in a separate environment against 76 HTTP responses and 14 CORS cases. A separate replay recalculated 48 symbol-day results from preserved synthetic inputs and matched the reference results and state. A second run stopped after 24 results and resumed in a new process to produce the remaining 24 with zero duplicate calculations.
- Engineering retrospective. The closeout identified that source-data availability should have been tested before expanding validation and storage. I carried that lesson into the plan for a smaller daily-data study.
Scope. The completed demo used seven synthetic symbols across eight trading days. Market-wide replay remains incomplete, and strategy returns are unverified. Public hosting, intraday alerts, and order execution were outside the delivered scope.

Project README · API contract · Demo verification · Replay verification · Closeout

Project links require repository access.
Frontend collaboration · Codedang (Skkuding)
Contributed to an educational coding platform using React, Next.js, and TypeScript. Worked with teammates through GitHub pull requests and code review.
- Standardized a shared input component across sizes and interaction states. PR #3422
- Redesigned the course-edit modal and updated form handling to preserve numeric values and combine split contact fields for saving. PR #3365
AI-assisted development
In the capstone, I scoped tasks and set verification criteria for Codex-assisted implementation and testing. I tracked implementation, test results, and separate ChatGPT reviews of published diffs as distinct steps. Working rules · Review history (repository access required)
Foundations
- Systems coursework. Implemented EEVDF scheduling in xv6-riscv and built multithreaded TCP/UDP servers. Studied indexing, query optimization, and external merge sort.
- Other experience. Node.js, Express, SQL, MySQL, SQLite, Git, and Linux/WSL.
Contact
hyeonwoo1204@gmail.com

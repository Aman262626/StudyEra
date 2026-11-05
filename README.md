# StudyEra
Personal learning library starter: FastAPI + PostgreSQL + responsive web UI.

## Included
- Dashboard and course-folder creation
- Study planner tasks
- Telegram configuration status endpoint
- Starter practice quiz
- Admin health panel
- Render Blueprint

## Important
Telegram import/sign-in, video streaming, PDF.js viewer, AI provider and authentication are not finished in this starter. Telegram integration must use a secure server-side authorization flow, encrypted sessions and an allow-list of chats the owner can access. Do not bypass protected content, membership restrictions, deleted messages or creator controls.

## Local run
```bash
python -m venv .venv
# Windows: .venv\\Scripts\\activate
pip install -r requirements.txt
uvicorn app.main:app --reload
```
Open http://127.0.0.1:8000

## Render
1. Push repository to GitHub.
2. In Render select New > Blueprint and choose this repository.
3. Review render.yaml and create the web service and PostgreSQL database.
4. Add Telegram credentials only if you have created an app at https://my.telegram.org.
5. Set a strong SESSION_ENCRYPTION_KEY before enabling Telegram session storage.
6. Add authentication before public exposure.

## Environment variables
- DATABASE_URL: Render PostgreSQL connection
- TELEGRAM_API_ID / TELEGRAM_API_HASH: optional Telegram application credentials
- SESSION_ENCRYPTION_KEY: unique encryption key for future Telegram session storage
- AI_API_KEY: optional AI provider key, not used yet

## Production checklist
- Add single-user authentication and secure cookie sessions.
- Add CSRF protection, secure headers and rate limits.
- Implement Telegram sign-in entirely server-side.
- Encrypt session data at rest and support revoke/disconnect.
- Respect protected content and Telegram platform rules.
- Add short-lived authorized media access.
- Add PDF viewer and AI retrieval with transparent external data handling.
- Configure database backups and monitoring.

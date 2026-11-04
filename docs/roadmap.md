# ARK — Phase 1 Checklist

## Backend Engineering and Database

**Estimate:** 4 weeks  
**Status:** Not Started

### Objective

Create a tested FastAPI backend connected to PostgreSQL. It should support task CRUD, validation, controlled errors, API documentation, and automated tests.

---

## Week 1 — Setup and API fundamentals

### Setup
- [ ] Create the ARK project directory.
- [ ] Create a Python virtual environment.
- [ ] Install FastAPI and Uvicorn.
- [ ] Initialize Git.
- [ ] Create `.gitignore`.
- [ ] Create `.env.example` (no real secrets).
- [ ] Create the initial backend package structure.

### Learn
- [ ] HTTP request/response basics.
- [ ] REST API fundamentals.
- [ ] JSON.
- [ ] FastAPI routes.
- [ ] Pydantic request/response models.
- [ ] Validation.
- [ ] Async Python basics.

### Build
- [ ] Create the FastAPI application entry point.
- [ ] Add a root endpoint.
- [ ] Add a health-check endpoint.
- [ ] Run the application locally.
- [ ] Inspect Swagger UI.
- [ ] Test endpoints with an API client.

**Milestone:** A locally running FastAPI application.

---

## Week 2 — PostgreSQL and persistence

### Learn
- [ ] SQL basics and CRUD.
- [ ] Tables, primary keys, and constraints.
- [ ] PostgreSQL fundamentals.
- [ ] SQLAlchemy ORM.
- [ ] Database sessions.
- [ ] Transactions and integrity errors.

### Build
- [ ] Install/configure PostgreSQL locally.
- [ ] Create the ARK database.
- [ ] Configure database connection using environment variables.
- [ ] Create a database session dependency.
- [ ] Define the initial Task model.
- [ ] Create the task table using a migration or controlled schema setup.
- [ ] Create a task repository.
- [ ] Test create/read/update/delete operations directly.

**Milestone:** Task records persist in the database.

---

## Week 3 — Task API and error handling

### Build endpoints
- [ ] `POST /api/v1/tasks` — Create task.
- [ ] `GET /api/v1/tasks` — List tasks.
- [ ] `GET /api/v1/tasks/{task_id}` — Retrieve task.
- [ ] `PATCH /api/v1/tasks/{task_id}` — Update task.
- [ ] `DELETE /api/v1/tasks/{task_id}` — Delete task.

### API quality
- [ ] Validate input fields.
- [ ] Define response schemas.
- [ ] Return appropriate status codes.
- [ ] Handle invalid IDs.
- [ ] Handle missing records.
- [ ] Handle database errors without exposing internals.
- [ ] Add structured logging.
- [ ] Confirm Swagger documentation is clear.

**Milestone:** Task CRUD works through the API.

---

## Week 4 — Testing and cleanup

### Learn
- [ ] Pytest basics.
- [ ] Unit tests vs integration tests.
- [ ] API testing.
- [ ] Debugging and refactoring.

### Build
- [ ] Test task creation.
- [ ] Test task listing.
- [ ] Test retrieving an existing task.
- [ ] Test unknown task ID.
- [ ] Test task updates.
- [ ] Test deletion.
- [ ] Test invalid payloads.
- [ ] Test expected database failure handling.
- [ ] Refactor repeated logic.
- [ ] Review folder structure.
- [ ] Update README setup instructions.
- [ ] Commit work to GitHub.

**Milestone:** A tested and documented backend foundation.

---

## Phase 1 Definition of Done

- [ ] Application starts locally from documented instructions.
- [ ] PostgreSQL connection works.
- [ ] Task model and persistence work.
- [ ] All task CRUD routes function.
- [ ] Request validation is in place.
- [ ] Error responses are controlled.
- [ ] API docs are available.
- [ ] Core automated tests pass.
- [ ] No secrets are committed.
- [ ] GitHub repository is updated.
- [ ] Phase 1 completion is reflected in the roadmap.

## Deliverable

A working, documented, tested backend that can create, retrieve, update, and delete task records through a REST API.

**Next phase:** Smart-home simulation.

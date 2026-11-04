# ARK — System Requirements

**Status:** Proposed / pre-coding  
**Version:** 0.1  
**Full form:** To be finalized

## 1. Purpose

This document defines the planned capabilities, quality requirements, constraints, and acceptance criteria for ARK. Requirements will be revised as the project is implemented.

## 2. Scope

The intended long-term system includes a backend, agent workflow, memory and knowledge retrieval, task execution, smart-home integration, voice interface, and ML services.

The initial prototype focuses on backend foundations and task CRUD. Smart-home actions begin in simulation.

## 3. Functional requirements

| ID | Requirement | Priority | Acceptance criteria |
|---|---|---|---|
| FR-001 | The backend shall expose an API. | Must | API starts locally and documented routes respond. |
| FR-002 | The system shall validate incoming request data. | Must | Invalid payloads receive a controlled validation response. |
| FR-003 | The system shall create tasks. | Must | Valid task is persisted and returned with an identifier. |
| FR-004 | The system shall retrieve tasks. | Must | Existing task can be fetched; unknown ID is handled. |
| FR-005 | The system shall update task fields. | Must | Allowed fields update and persist. |
| FR-006 | The system shall delete or cancel a task. | Must | Operation follows defined semantics and is reflected in storage. |
| FR-007 | The system shall log relevant errors. | Must | Errors are recorded without leaking secrets. |
| FR-008 | The agent shall use only registered tools. | Later | Unregistered tool invocation is rejected. |
| FR-009 | The system shall enforce tool permissions in code. | Later | Unauthorized operation is blocked in tests. |
| FR-010 | The system shall support approval for consequential actions. | Later | Action waits until explicit approval is received. |
| FR-011 | The task engine shall track lifecycle state. | Later | State transitions are persisted and queryable. |
| FR-012 | The system shall verify execution outcomes. | Later | Task is not marked successful without defined evidence. |
| FR-013 | The system shall retrieve relevant approved memory. | Later | Retrieval returns matching stored context in test cases. |
| FR-014 | The system shall support document retrieval (RAG). | Later | Ingested test document can be retrieved by relevant query. |
| FR-015 | The system shall support a simulated home environment. | Later | Simulated device state changes through permitted commands. |
| FR-016 | The system shall support voice input and output. | Later | A test utterance is transcribed and a response can be spoken. |
| FR-017 | The system shall expose ML inference through a defined interface. | Later | A trained test model produces a validated prediction. |
| FR-018 | The system shall provide task history. | Later | User can query stored task events. |

## 4. Non-functional requirements

| ID | Requirement | Priority | Acceptance criteria |
|---|---|---|---|
| NFR-001 | Maintainability | Must | Modules have clear responsibilities and readable code. |
| NFR-002 | Reliability | Must | Expected failures return controlled responses. |
| NFR-003 | Security | Must | Secrets are excluded from source control; access checks are tested. |
| NFR-004 | Testability | Must | Core business logic can be tested independently. |
| NFR-005 | Observability | Must | Relevant errors and task transitions are logged. |
| NFR-006 | Data integrity | Must | Database operations preserve defined constraints. |
| NFR-007 | Privacy | Must | Only necessary information is retained; memory is controlled. |
| NFR-008 | Extensibility | Should | A new tool can be registered without rewriting the orchestrator. |
| NFR-009 | Performance | Should | Establish measurable latency targets after a working baseline exists. |
| NFR-010 | Availability | Later | Deployment can restart services and recover persistent state. |

## 5. Safety requirements

- **SR-001:** The LLM shall not be treated as the sole permission enforcement mechanism.
- **SR-002:** Tools shall have narrowly scoped permissions.
- **SR-003:** Consequential actions shall require explicit human approval.
- **SR-004:** Initial smart-home testing shall use a simulator or low-risk setup.
- **SR-005:** The system shall report uncertain or failed outcomes honestly.
- **SR-006:** Retries shall be bounded and designed to avoid unsafe duplicate actions.
- **SR-007:** Credentials shall not be embedded in source code or committed to the repository.

## 6. Constraints and assumptions

- Development begins after the user's academic priorities permit.
- Initial development uses a Windows laptop.
- The first smart-home environment is simulated.
- A dedicated server is a future decision, not an initial dependency.
- Technology choices may be changed after experiments.
- The project is a learning prototype and is not assumed to be production-ready.

## 7. Phase 1 acceptance scope

Phase 1 is accepted when:

- FastAPI application runs locally.
- PostgreSQL connection is configured.
- Task model and persistence work.
- Task CRUD API routes work.
- Request validation and controlled error handling exist.
- API docs are available.
- Core automated tests pass.
- Setup instructions are documented.

## 8. Requirement change process

When a requirement changes:
1. Update this document.
2. Record why it changed.
3. Update affected roadmap/checklist items.
4. Adjust tests and acceptance criteria.

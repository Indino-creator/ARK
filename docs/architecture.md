# ARK — Development and Learning Roadmap

**Status:** Proposed  
**Timeline:** Flexible estimate; learning depth takes precedence  
**Full form:** To be finalized

## Approach

ARK is developed in stages. For each feature: learn the concept, implement a small version, experiment, evaluate, then integrate and document it. Do not try to build all subsystems simultaneously.

Academic commitments remain the priority. The pre-coding stage is limited to planning and documentation.

## Phase 0 — Planning and foundations

**Timing:** Before coding

### Learn / review
- Python OOP, modules, packages, exceptions
- Git and GitHub
- SQL fundamentals
- HTTP, REST, JSON
- High-level client-server architecture
- LLM, agent, and ML concepts

### Deliverables
- README
- Project vision
- Architecture document
- Requirements document
- Roadmap
- Phase 1 checklist
- Initial repository structure

**Exit criteria:** Project scope and first implementation steps are documented.

## Phase 1 — Backend engineering and database

**Estimate:** Month 1

### Learn
- FastAPI, HTTP, REST, Pydantic
- PostgreSQL and SQL
- SQLAlchemy and database sessions
- CRUD, transactions, validation
- Logging, exception handling
- Pytest and API testing
- Basic authentication/authorization concepts

### Build
- Backend application
- Health endpoint
- Database connection
- Task model and repository
- Task CRUD endpoints
- Validation and error handling
- API documentation
- Automated tests

**Exit criteria:** Task data can be created, read, updated, and deleted through a tested API.

## Phase 2 — Smart-home simulation

**Estimate:** Month 2

### Learn
- State management
- Event-driven programming
- Async Python
- State machines
- Device abstractions

### Build
- Simulated lights, fans, and sensors
- Device registry
- State manager
- Simulated device API
- Event handling
- Tests for device state transitions

**Exit criteria:** The backend can control and query simulated devices.

## Phase 3 — Agentic AI brain

**Estimate:** Months 3–4

### Learn
- LLM fundamentals
- Prompt design and structured output
- Function/tool calling
- Intent recognition
- Planning and task decomposition
- Agent orchestration
- Agent evaluation
- LangGraph or custom state machine

### Build
- Intent interpretation
- Planner
- Tool registry
- Orchestrator
- Validated tool arguments
- Permission interface
- Basic result verification

**Exit criteria:** A limited agent can plan and invoke allowed tools in a test environment.

## Phase 4 — Memory and knowledge engine

**Estimate:** Month 5

### Learn
- Embeddings
- Vector search
- Chunking
- RAG
- Context management
- Memory policies

### Build
- Conversation context
- User-approved memory
- Task history retrieval
- Document ingestion
- Semantic search
- RAG evaluation examples

**Exit criteria:** Relevant approved memory and test documents can be retrieved.

## Phase 5 — Smart-home integration

**Estimate:** Months 6–7

### Learn
- Home Assistant
- MQTT
- Device APIs
- Event subscriptions
- Integration testing

### Build
- Home Assistant adapter
- Device-state synchronization
- Event listeners
- Narrowly scoped controls
- Permission checks and logs

**Exit criteria:** ARK can interact with selected devices in a controlled test setup.

## Phase 6 — Voice interface

**Estimate:** Month 8

### Learn
- Speech-to-text
- Text-to-speech
- Audio processing
- Wake-word detection
- Streaming interaction

### Build
- Voice input pipeline
- Spoken responses
- Wake-word interface
- Voice conversation mode

**Exit criteria:** A test voice request can be transcribed, processed, and answered aloud.

## Phase 7 — Task automation engine

**Estimate:** Months 9–10

### Learn
- Background workers
- Task queues
- Scheduling
- Persistent task state
- Retries and failure handling
- Notifications

### Build
- Persistent task queue
- Scheduler
- Worker
- Status tracking
- Bounded retry policy
- Task reporting and activity history

**Exit criteria:** Approved test tasks can be scheduled, executed, verified, and tracked.

## Phase 8 — Deployment

**Estimate:** Month 11

### Learn
- Linux fundamentals
- Docker and Docker Compose
- Networking
- Secure remote access
- Backup, monitoring, restart policies

### Build
- Containerized services where useful
- Persistent database storage
- Deployment documentation
- Health monitoring
- Backup and recovery process

**Exit criteria:** Prototype can be deployed and recovered in a controlled environment. Dedicated server selection follows resource measurement.

## Phase 9 — Machine learning and deep learning

**Estimate:** Months 12–13 or longer

### Mathematics
- Linear algebra
- Probability and statistics
- Calculus basics
- Gradients and optimization

### Classical ML
- Regression and classification
- Clustering
- Feature engineering
- Train/validation/test splits
- Overfitting and evaluation
- Scikit-learn

### Deep learning
- Neural networks
- Forward/backpropagation
- Loss functions
- Gradient descent
- PyTorch
- CNNs and Transformers concepts

### Build
- ML model from a clean dataset
- Energy or time-series prediction experiment
- Anomaly detection experiment
- Evaluation and model inference interface

**Exit criteria:** At least one model is trained, evaluated, documented, and integrated as a bounded inference capability.

## Phase 10 — Evaluation, hardening, and portfolio

**Estimate:** Months 14–18 or longer

### Learn
- MLOps fundamentals
- Experiment tracking and model versioning
- CI/CD
- Security review
- Performance measurement
- Documentation and demonstration

### Build
- Frontend dashboard
- Automated test pipeline
- Evaluation benchmarks
- System health view
- Security and permission review
- Setup guide
- Architecture updates
- Demo video and portfolio presentation

**Exit criteria:** A documented, reproducible prototype demonstrates its working features and limitations.

## Additional study tracks

These need separate focused study and are not guaranteed by the core project:

- Computer vision
- Reinforcement learning
- Advanced ML mathematics
- Research paper reproduction
- Model benchmarking and ablation studies

## Progress tracking

Update phase status as:
- `Not Started`
- `In Progress`
- `Blocked`
- `Completed`

Do not mark a phase completed solely because its code exists. Check its exit criteria and tests.

## ADDED Requirements

### Requirement: Structured learning path for React developers
The project SHALL provide a staged learning path for developers who already understand React and want to start building WeChat Mini Programs with Taro.

#### Scenario: Learner reads the onboarding flow
- **WHEN** a React developer opens the learning guide
- **THEN** the guide presents a clear sequence of stages from environment confirmation to hands-on Taro practice

#### Scenario: Learner understands what to study first
- **WHEN** the learner starts from the beginning of the guide
- **THEN** the guide identifies the recommended starting topics instead of requiring the learner to infer an order

### Requirement: Code-first learning progression
The learning path MUST be organized around coding tasks as the primary learning mechanism rather than long-form conceptual reading.

#### Scenario: Learner enters the learning path
- **WHEN** the learner starts the onboarding experience
- **THEN** the guide presents a first coding task early in the flow instead of requiring the learner to finish a large block of theory first

#### Scenario: Learner advances through the guide
- **WHEN** the learner moves from one stage to the next
- **THEN** each stage is framed around a concrete coding objective, expected result, and supporting explanation

### Requirement: Onboarding targets practical Taro independence
The learning path MUST target a learner outcome where a React developer can understand the existing Taro project, modify an existing page, and create a simple new Mini Program page with basic platform capability usage.

#### Scenario: Learner completes the onboarding path
- **WHEN** the learner finishes the guide
- **THEN** the expected outcome includes reading the current project structure, editing existing page behavior, and building one simple new page in the repository

### Requirement: React-to-Taro concept mapping
The learning guide MUST explain how common React development concepts map to Taro and WeChat Mini Program development in this repository.

#### Scenario: Learner compares familiar concepts
- **WHEN** the learner reviews routing, components, lifecycle, styling, or platform APIs
- **THEN** the guide explains the equivalent Taro or WeChat concept and highlights the important difference from React web development

### Requirement: Repository-based practical exercises
The project SHALL include hands-on exercises that use the current Taro codebase so learners can practice applying the documented concepts.

#### Scenario: Learner completes a basic exercise
- **WHEN** the learner follows the guide's first practical task
- **THEN** the task asks them to create or modify project files in the existing Taro structure rather than only reading theory

#### Scenario: Learner practices core mini program development tasks
- **WHEN** the learner progresses through the exercises
- **THEN** the exercises cover core tasks such as page creation, configuration, styling, state handling, or invoking platform APIs

### Requirement: Exercises follow a progressive task sequence
The practical path MUST include a progressive sequence that starts with modifying an existing page, then creating a new page, then adding interaction, then using a Mini Program API, and finally completing one integrative mini feature or page-level task.

#### Scenario: Learner follows the recommended practice flow
- **WHEN** the learner completes the exercises in order
- **THEN** the sequence builds from low-risk edits in the existing project toward a more independent final coding task

### Requirement: Hybrid progression from concepts to mini feature
The learning path MUST move from React-to-Taro concept mapping to a small number of focused exercises and end with one compact mini feature or page-level practice outcome.

#### Scenario: Learner follows the recommended sequence
- **WHEN** the learner advances through the guide
- **THEN** the guide first explains concept mapping, then assigns focused practice tasks, and finally culminates in one integrative page-level exercise

### Requirement: Guidance supports self-implementation
The learning materials MUST support the learner in writing the code themselves by providing goals, file context, and validation criteria without making full worked solutions the primary experience.

#### Scenario: Learner starts a task
- **WHEN** the learner opens a coding task
- **THEN** the task explains what to build, where to work, and how to verify success while still leaving room for the learner to implement the code independently

### Requirement: Exercises stay grounded in the current repository
Each exercise MUST reference the current repository structure, relevant files, and runnable commands so the learner can connect each concept to concrete project context.

#### Scenario: Learner starts a guided exercise
- **WHEN** the learner begins an exercise
- **THEN** the exercise points to the relevant files, directories, or build commands in this repository rather than describing the task only in abstract terms

### Requirement: Measurable completion criteria
The learning path MUST define what a learner can complete to consider the onboarding successful.

#### Scenario: Learner checks progress
- **WHEN** the learner reaches the end of the guide
- **THEN** the guide includes a checklist, outcome summary, or equivalent completion criteria for validating core understanding

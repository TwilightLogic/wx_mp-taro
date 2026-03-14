## ADDED Requirements

### Requirement: Structured learning path for React developers
The project SHALL provide a staged learning path for developers who already understand React and want to start building WeChat Mini Programs with Taro.

#### Scenario: Learner reads the onboarding flow
- **WHEN** a React developer opens the learning guide
- **THEN** the guide presents a clear sequence of stages from environment confirmation to hands-on Taro practice

#### Scenario: Learner understands what to study first
- **WHEN** the learner starts from the beginning of the guide
- **THEN** the guide identifies the recommended starting topics instead of requiring the learner to infer an order

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

### Requirement: Measurable completion criteria
The learning path MUST define what a learner can complete to consider the onboarding successful.

#### Scenario: Learner checks progress
- **WHEN** the learner reaches the end of the guide
- **THEN** the guide includes a checklist, outcome summary, or equivalent completion criteria for validating core understanding

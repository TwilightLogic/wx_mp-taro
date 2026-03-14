## Context

This repository is already a minimal Taro 4 + React starter for WeChat Mini Programs, with working build scripts and a basic page structure. The current gap is not project setup but learning guidance: a React developer can run the app, yet still lack a clear understanding of how page routing, lifecycle, platform APIs, styling boundaries, and WeChat-specific constraints differ from traditional React web development.

The design should turn the repository into a guided learning environment. The key shift is that learning should be code-first: the learner should primarily progress by completing coding tasks inside this repository, with explanations attached to tasks as support rather than as the main experience. The structure needs to stay close to the current codebase so the learner can connect each concept to real files, commands, and project behaviors.

## Goals / Non-Goals

**Goals:**
- Define a learning experience tailored to developers who already know React but are new to Taro and WeChat Mini Programs.
- Organize implementation around a staged coding journey, practical exercises, and repository-specific examples.
- Reuse the existing project structure and build commands so learners can start from the current codebase without extra setup complexity.
- Make the primary path depend on the learner writing code themselves rather than consuming long-form tutorials.
- Make the future implementation concrete enough that `tasks.md` can break it into actionable steps.

**Non-Goals:**
- Rebuild the project scaffold or replace the existing Taro runtime configuration.
- Provide an exhaustive reference for every Taro API or every WeChat Mini Program capability.
- Introduce backend services, authentication, or production business features unrelated to onboarding.
- Turn the repository into a fully automated course platform with grading or hidden-answer infrastructure.

## Decisions

### Use a code-first onboarding path instead of a reading-first tutorial
The change will be implemented as a sequence of coding stages where the learner writes code early and often. Explanations will support each task, but the primary learning mechanism will be editing, running, and validating code in the existing Taro project. This better fits a developer who already knows React and mainly needs Taro-specific hands-on fluency.

Alternative considered: a reading-first tutorial that introduces concepts before any meaningful coding task.
Why not: it is easier to write, but it delays hands-on feedback and makes it too easy for experienced developers to read without building real Taro intuition.

### Use a progressive five-task sequence
The primary path should progress through five stages:
1. Modify an existing page
2. Create a new page
3. Add an interaction
4. Use a Mini Program API through Taro
5. Build one compact integrative mini feature

This sequence starts with low-risk changes in familiar files and gradually increases independence. It gives the learner repeated feedback loops while covering the core Taro and Mini Program concepts needed for basic productivity.

Alternative considered: a collection of unrelated exercises.
Why not: unrelated tasks teach isolated facts but do not create a coherent sense of progression or accomplishment.

### Attach concept mapping and explanations to tasks
The implementation should include React-to-Taro mapping and WeChat-specific explanations, but these should be delivered next to the tasks that make them relevant. For example, page configuration should be explained when creating a new page, and platform API constraints should be explained when invoking a Mini Program capability.

Alternative considered: collect all conceptual material in one large upfront section.
Why not: it increases cognitive load and breaks the code-first learning rhythm.

### Design the experience as guided self-implementation
Tasks should provide goals, relevant files, verification criteria, and lightweight hints, but they should not make full worked solutions the main experience. The learner should feel that they are implementing the code themselves, not merely reading or copying a finished example.

Alternative considered: shipping full reference answers as the default path.
Why not: it weakens active learning and shifts the experience from problem solving to imitation.

### Keep implementation low-risk by placing learning assets alongside, not inside, core build logic
Future implementation should prefer adding dedicated docs, guided task content, and isolated practice pages or examples rather than changing foundational build configuration. That keeps the learning change easy to review and unlikely to disrupt the starter project's ability to build for WeChat.

Alternative considered: embedding guidance into build scripts or generated templates.
Why not: it increases maintenance cost and creates unnecessary coupling between tooling and learning content.

## Risks / Trade-offs

- [Risk] Learners may still feel overwhelmed if the tasks jump too quickly in difficulty. → Mitigation: use the five-stage progression from modification to independent mini feature.
- [Risk] A code-first path can become frustrating if hints are too sparse. → Mitigation: attach concise explanations, file references, and validation criteria to every task.
- [Risk] Practice tasks may drift away from the actual repository structure over time. → Mitigation: anchor each task to existing directories, commands, and page patterns in this project.
- [Risk] WeChat-specific constraints can become outdated as the ecosystem evolves. → Mitigation: focus on stable platform concepts and keep version-sensitive details lightweight.
- [Risk] Full sample answers could undermine the intended self-implementation experience. → Mitigation: make goals and checks prominent, and keep any reference implementation secondary.

## Migration Plan

No runtime migration is required for the proposal phase. Future implementation can be rolled out incrementally by adding documentation, guided coding tasks, and optional practice pages without modifying existing working flows. If any practice asset causes confusion or build issues, it can be removed independently with low rollback cost.

## Open Questions

- Should the eventual implementation live primarily in `README.md`, a dedicated `docs/` directory, or both?
- How much guidance should each task provide before it starts to feel like the learner is following a script rather than implementing independently?
- Should practice pages be shipped as visible sample pages in the app, or described as learner-created exercises only?
- What mini feature best balances realism, small scope, and coverage of core Taro concepts?

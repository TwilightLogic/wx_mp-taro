## Context

This repository is already a minimal Taro 4 + React starter for WeChat Mini Programs, with working build scripts and a basic page structure. The current gap is not project setup but learning guidance: a React developer can run the app, yet still lack a clear understanding of how page routing, lifecycle, platform APIs, styling boundaries, and WeChat-specific constraints differ from traditional React web development.

The design should turn the repository into a guided learning environment. It needs to balance conceptual explanation with hands-on practice, while staying close to the current code structure so the learner can connect theory to real files.

## Goals / Non-Goals

**Goals:**
- Define a learning experience tailored to developers who already know React but are new to Taro and WeChat Mini Programs.
- Organize implementation around staged onboarding materials, practical exercises, and repository-specific examples.
- Reuse the existing project structure and build commands so learners can start from the current codebase without extra setup complexity.
- Make the future implementation concrete enough that `tasks.md` can break it into actionable steps.

**Non-Goals:**
- Rebuild the project scaffold or replace the existing Taro runtime configuration.
- Provide an exhaustive reference for every Taro API or every WeChat Mini Program capability.
- Introduce backend services, authentication, or production business features unrelated to onboarding.

## Decisions

### Use a staged onboarding path instead of a single long tutorial
The change will be implemented as a sequence of learning stages, such as environment confirmation, core Taro concepts, WeChat-specific differences, and guided practice. This reduces cognitive load for a developer who already knows React and mainly needs concept translation.

Alternative considered: a single README-style guide.
Why not: it is easier to write, but harder to turn into measurable progress and easier for learners to skim without practicing.

### Combine conceptual documents with repository-based exercises
The implementation should include both explanation and tasks that require editing or adding files in the current Taro project. The exercises will anchor concepts like page config, hooks, component usage, styling, and platform APIs in the actual repository.

Alternative considered: documentation only.
Why not: documentation alone does not ensure the learner can apply knowledge inside a Taro project.

### Teach through React-to-Taro mapping
The primary teaching strategy should compare familiar React concepts with their Taro and WeChat counterparts, such as routing, component primitives, lifecycle behavior, and environment limitations. This matches the user's stated background and helps them build on existing mental models.

Alternative considered: teaching Taro from first principles without comparison.
Why not: it ignores the learner's existing expertise and makes onboarding slower than necessary.

### Keep implementation low-risk by placing learning assets alongside, not inside, core build logic
Future implementation should prefer adding dedicated docs and isolated practice pages or examples rather than changing foundational build configuration. That keeps the learning change easy to review and unlikely to disrupt the starter project's ability to build for WeChat.

Alternative considered: embedding guidance into build scripts or generated templates.
Why not: it increases maintenance cost and creates unnecessary coupling between tooling and learning content.

## Risks / Trade-offs

- [Risk] Learners may still feel overwhelmed if the guide introduces too many platform details at once. → Mitigation: split content into short stages with explicit outcomes and exercises.
- [Risk] Practice tasks may drift away from the actual repository structure over time. → Mitigation: anchor each task to existing directories, commands, and page patterns in this project.
- [Risk] A guidance-only change may feel less concrete than a feature change. → Mitigation: require hands-on exercises and completion criteria in the spec so the implementation produces tangible outputs.
- [Risk] WeChat-specific constraints can become outdated as the ecosystem evolves. → Mitigation: focus on stable platform concepts and keep version-sensitive details lightweight.

## Migration Plan

No runtime migration is required for the proposal phase. Future implementation can be rolled out incrementally by adding documentation and optional practice pages without modifying existing working flows. If any practice asset causes confusion or build issues, it can be removed independently with low rollback cost.

## Open Questions

- Should the eventual implementation live primarily in `README.md`, a dedicated `docs/` directory, or both?
- Should practice pages be shipped as visible sample pages in the app, or described as learner-created exercises only?
- Does the learner want the path optimized for quick onboarding, or for building one small end-to-end demo feature as the main teaching vehicle?

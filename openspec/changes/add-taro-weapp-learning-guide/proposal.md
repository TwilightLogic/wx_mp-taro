## Why

Although this repository is already a Taro React starter, it does not yet provide a clear code-first path for an experienced React developer to learn how Taro maps web development concepts to WeChat Mini Program development. Adding a structured, task-driven learning flow now will shorten onboarding time and turn the project into a hands-on training sandbox instead of only a scaffold.

## What Changes

- Add a code-first learning path for React developers who are new to Taro and WeChat Mini Programs.
- Define a staged task flow that teaches Taro fundamentals through writing code in the existing project instead of primarily reading theory.
- Add progressive exercises that move from modifying an existing page to building a small integrative mini feature.
- Provide just-in-time explanations that support coding tasks, including Taro fundamentals, WeChat platform constraints, and React-to-Taro concept mapping.
- Define success criteria for completing the onboarding path so the change can later be implemented consistently.

## Capabilities

### New Capabilities
- `taro-learning-guide`: Provides a structured, code-first learning path for React developers to understand and build WeChat Mini Programs with Taro in this repository through progressive hands-on tasks.

### Modified Capabilities
- None.

## Impact

- Affects project documentation, onboarding flow, and learning-task structure for this Taro codebase.
- Uses the existing Taro React starter structure in `src/`, `config/`, and the WeChat Mini Program build workflow from `package.json`.
- Does not require immediate API or runtime changes for the proposal phase, but future implementation may add guided task content, learning docs, sample pages, and practice checkpoints.

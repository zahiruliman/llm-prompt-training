# System Patterns

This document outlines the system architecture, key technical decisions, and design patterns used in the project. For this project, it defines the content architecture for the training module.

## System Architecture

- (To be filled in with diagrams and descriptions)

## Key Technical Decisions

- (To be filled in)

## Content Architecture: Training Module Structure

The training content will be structured as a journey, guiding the user from basic concepts to advanced application, now including a new technique.

```mermaid
flowchart TD
    A[Introduction] --> B[Technique 1: Persona];
    B --> C[Technique 2: Context];
    C --> D[Technique 3: Few-Shot];
    D --> E[Technique 4: Chain of Thought];
    E --> F[Technique 5: Iteration];
    F --> G[Technique 6: Reverse Engineering];
    G --> H[Conclusion];
```

## Key Content Decisions

- **Analogy-Driven:** Each core technique will be introduced with a simple, memorable analogy (e.g., "Wear This Hat") to make it less intimidating and easier to recall.
- **Scaffolded Learning:** The techniques build on each other, from simple (assigning a persona) to complex (combining all techniques for a full workflow).
- **Role-Specific Examples:** Every technique will be illustrated with examples directly relevant to the tasks of a Business Analyst or System Analyst creating documentation.

## Design Patterns

- **Before-and-After:** Examples will use a "Simple Prompt vs. Advanced Prompt" format to clearly demonstrate the value of each technique.
- **Contextualization:** All examples will explicitly reference the `AIDevX` environment and its specific assistants (e.g., "When using the 'Generate Requirements' assistant...").
- **Interactivity:** Each of the five core techniques in the detailed documentation will now include a dedicated sub-section titled "Interactive Workshop Activity" which will outline a practical, collaborative exercise.

## Final Deliverable File Structure

```mermaid
graph TD
    subgraph Root
        D["training-materials/"]
        S[training_slides.md]
        T[trainer_notes.md]
    end

    subgraph "training-materials/"
        M[00_introduction.md]
        T1[01_technique_persona.md]
        T2[02_technique_context.md]
        T3[03_technique_few_shot.md]
        T4[04_technique_chain_of_thought.md]
        T5[05_technique_iterative.md]
        T6[06_technique_reverse_engineering.md]
        C[07_conclusion.md]
        MC[main_content.md]
    end

    D --> M
    D --> T1
    D --> T2
    D --> T3
    D --> T4
    D --> T5
    D --> T6
    D --> C
    D --> MC
```

**CORRECT FILE STRUCTURE:**
- **6 Core Techniques:** Files 01-06 (Persona, Context, Few-Shot, Chain of Thought, Iterative, Reverse Engineering)
- **Supporting Files:** 00_introduction.md, 07_conclusion.md, main_content.md
- **Root Level:** training_slides.md, trainer_notes.md

- A `training-materials/` directory holds the detailed, professional documentation.
- A final, summarized `training_slides.md` is created at the root level.
- A comprehensive `trainer_notes.md` is also created at the root level. 
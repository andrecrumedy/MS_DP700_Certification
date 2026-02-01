# MS DP-700 Certification

AI-assisted study guide for **Microsoft DP-700** (Implement data engineering solutions using Microsoft Fabric).

---

## Objective

Complete the self-directed course **DP-700T00-A: Implement data engineering solutions using Microsoft Fabric**, and use generative AI for quizzing on covered materials and progress documentation.

**Primary tool:** Cursor

---

## AI Usage

Ways AI supports learning and progress in this course:

- **Assisted quiz generation** — Create module-based quizzes from course content.
- **Project velocity update** — Track and document progress through learning paths and modules.
- **Concept explanation** — Ask for plain-language explanations of Fabric topics (lakehouse, medallion, pipelines, etc.).
- **Practice scenarios** — Request “what would you do?” scenarios aligned to exam objectives.
- **Module summaries** — Get short summaries or key takeaways after finishing a module.
- **Flashcards & recall** — Generate flashcards or quick-review questions for spaced repetition.
- **Exam objective mapping** — Clarify how course modules map to certification skills and suggest focus areas.
- **Lab and exercise support** — Get help interpreting instructions, debugging steps, or troubleshooting exercises.
- **Study sequencing** — Get recommendations on order of modules or when to review previous material.

---

## Agents

### 1. DP-700 Microsoft Fabric Quiz Review

**Role:** Microsoft expert and tutor for DP-700 study and quiz grading.

**Initial prompt:**

> Act as a Microsoft expert and tutor. The purpose of this project is to help me learn and study for the DP-700 Certification.
>
> **Current progress:** I have started the recommended course *Implement data engineering solutions using Microsoft Fabric* (DP-700T00-A). The first learning path is *Ingest data with Microsoft Fabric*. I am completing the first prerequisite to this learning path, *Get started with Microsoft Fabric*. I have completed the first module, *Introduction to end-to-end analytics using Microsoft Fabric*, and generated a quiz file.
>
> **Your task:** When I finish answering the questions in the quiz file, grade my responses and suggest where I need to strengthen my knowledge before moving to the next unit.

**Reference links:**

- [Fabric Data Engineer Associate certification](https://learn.microsoft.com/en-us/credentials/certifications/fabric-data-engineer-associate/?practice-assessment-type=certification#certification-prepare-for-the-exam)
- [DP-700T00 course syllabus](https://learn.microsoft.com/en-us/training/courses/dp-700t00#course-syllabus)
- [Ingest data with Microsoft Fabric](https://learn.microsoft.com/en-us/training/paths/ingest-data-with-microsoft-fabric/)
- [Get started with Microsoft Fabric](https://learn.microsoft.com/en-us/training/paths/get-started-fabric/)

**Quiz file:** `Course Content/Learning Paths/Getting Started With Microsoft Fabric Modules/Introduction to end-to-end analytics using Microsoft Fabric/Quiz - Introduction to end-to-end analytics using Microsoft Fabric.md`

---

### 2. Project Documentation Management

**Role:** Project manager for documentation; create and update docs only as needed.

**Initial prompt:**

> This agent is for project documentation. Act as a project manager with 20 years of experience. Your goal is to help me create and update documentation as needed. Do not make unnecessary changes. Reply "yes" if you understand.

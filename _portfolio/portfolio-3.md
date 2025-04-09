---
title: "qScroll"
excerpt: "A vertically scrollable, minimal iOS test-prep app designed to deliver SAT-style questions one at a time. It emphasizes speed, focus, and data-driven feedback to support meaningful student improvement.<br/><img src='/images/qscroll.png'>"
collection: portfolio
---

This app is part of a broader, ongoing project exploring how we can use educational interfaces and performance tracking to help learners understand what they know, what they don’t, and how to close that gap efficiently.

---

## Purpose

Standardized test prep often prioritizes volume over insight. qScroll is built on the opposite assumption: that **data and deliberate feedback**—not just repetition—drive better outcomes. The core goal is to:

- Give students a focused interface to practice SAT-style math questions
- Offer immediate feedback on answer accuracy
- Create opportunities for deeper insight using performance data in future versions

qScroll is also a foundation for testing broader ideas around:
- Behavior-driven tutoring design
- Lightweight simulations of learning progression
- Integrating large language models into education tools

---

## Features

- Vertical scroll interface optimized for mobile use
- Double-tap to check answers
- Visual feedback (green/red outlines for correct/incorrect answers)
- Launch screen and dark mode support
- Runs natively on iOS 18+

---

## Tech Stack

- **SwiftUI** for the main interface
- **UIKit** (via `UIViewRepresentable`) to implement full-screen vertical paging
- Custom `PagingScrollView` for TikTok-style question transitions
- Designed for use on real devices (iPhone 11 and up), not just in Simulator

---

## Status

qScroll is an early-stage prototype and is not yet deployed on the App Store. Current priorities include:

- Enabling JSON or remote loading of questions
- Adding a progress tracker or summary screen
- Exploring how to integrate LLMs into answer generation, hint systems, or review tools
- Designing an admin interface for uploading and tagging new questions

---

## Why This Matters

Most educational apps stop at content delivery. qScroll is built on the assumption that what you do **with** the data is what matters most. Whether it’s adapting question order based on recent performance, flagging recurring errors, or building learner profiles over time, the goal is to design smarter feedback systems that evolve with the student.

This is one piece of a broader vision: **educational tools that feel as responsive and intentional as great human tutors**—but accessible to many more learners.

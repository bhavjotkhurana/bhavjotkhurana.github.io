---
title: "LLM Hints"
excerpt: "A Streamlit prototype that uses GPT-4 with vision to generate progressive, tutoring-style hints for SAT math questions from images. Designed to encourage learning through guided assistance rather than final answers. Built as part of an exploration into cost-effective, LLM-driven educational tools.
<br/><img src='/images/llmhints.png'>"
collection: portfolio
---


**Overview**  
llm-hints is an experimental tool that leverages GPT-4's vision capabilities to interpret SAT math problems from image uploads and provide tutoring-style hints, one at a time. The goal is to simulate a thoughtful, cost-aware tutoring experience where users are guided step-by-step rather than given immediate solutions.

**Key Features**  
- Accepts math problems as images and processes them using GPT-4 Turbo with vision.
- Provides up to three sequential hints: the third hint contains the full solution.
- Hints are delivered in natural language and designed to prompt reasoning, not give away answers.
- Built with Streamlit for rapid prototyping and demonstration.
- Developed as part of a cost-benefit analysis of LLM usage in education.

**Tools & Technologies**  
- OpenAI GPT-4 Turbo (vision)
- Python  
- Streamlit  
- dotenv (for secure API key management)

**Focus Areas**  
- Prompt engineering for guided tutoring
- Educational use of multimodal LLMs
- Model cost optimization and usage strategy

**Next Steps**  
- Extend to other standardized tests
- Add session logging to simulate student behavior
- Explore alternative hinting strategies (scaffolded, Socratic)
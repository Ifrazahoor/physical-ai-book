<!--
Sync Impact Report:
Version change: 1.2.0 → 1.2.1
Modified principles: none
Added sections: none
Removed sections: none
Templates requiring updates:
- ✅ .specify/templates/plan-template.md
- ✅ .specify/templates/spec-template.md
- ✅ .specify/templates/tasks-template.md
Follow-up TODOs: none
-->
# The AI-Robot Brain Constitution
## Topic: NVIDIA Isaac™ & Humanoid Navigation
### Project: Physical AI & Humanoid Robotics Book + RAG Chatbot

## Core Principles

### I. Accurate Perception, VSLAM, and Path Planning
Perception systems, Visual Simultaneous Localization and Mapping (VSLAM), and path planning algorithms must be accurate and robust for safe and effective humanoid navigation.

### II. Clarity for AI/CS Students
All content, including simulations, code, and theoretical explanations, must be clear and understandable for intermediate AI/CS students.

### III. Reproducible Simulations and Pipelines
NVIDIA Isaac simulations and associated perception and navigation pipelines must be fully reproducible, allowing students to replicate the results on their own systems.

## Key Standards

- **Isaac Sim**: Must be utilized for photorealistic simulation environments.
- **Isaac ROS**: Must be integrated for VSLAM and navigation functionalities.
- **Nav2**: Must be employed for bipedal humanoid path planning.
- **Code**: All code provided must be runnable and demonstrably functional.
- **Diagrams**: All diagrams must be accurate, clear, and enhance understanding.

## Constraints

- **Format**: All content must be in Docusaurus markdown with YAML metadata.
- **Modules**: Must support `/sp.specify`, `/sp.plan`, and `/sp.tasks` commands for workflow integration.
- **RAG Chatbot**: The RAG chatbot functionality must be restricted to answering questions solely based on the provided book content.

## Success Criteria

- **Isaac Sim + Isaac ROS**: The integrated Isaac Sim and Isaac ROS environment must be fully functional for humanoid simulation.
- **Accurate VSLAM & Humanoid Navigation**: The system must demonstrate accurate VSLAM map generation and successful humanoid navigation within simulated environments.
- **Reproducible Exercises**: All exercises and examples provided must be reproducible by students following the given instructions.

## Governance

This Constitution supersedes all other practices. Amendments require documentation, approval, and a migration plan for any affected components. All pull requests and reviews must verify compliance with these principles.

**Version**: 1.2.1 | **Ratified**: 2025-12-07 | **Last Amended**: 2025-12-07

---
title: Lasso
feature_text: |
  ## Lasso
  An Observatorium for the Dynamic Selection, Analysis, and Comparison of Software  
feature_image: "https://picsum.photos/1300/400?image=989"
excerpt: an Observatorium for the Dynamic Selection, Analysis and Comparison of Software.
---

{% include button.html text="Try it" link="https://softwareobservatorium.github.io/jupyterlab/lab/index.html" color="#0366d6" target="_blank" %}

LASSO's platform enables scalable software code analysis and observation of big code. It provides mass analysis of software code combining dynamic and static program analysis techniques to observe functional (i.e., behavioral) and non-functional properties of software code. It is primarily used to conduct active research in software engineering (contact us), but can also be used by practitioners.

Based on these capabilities, LASSO can be used to realize reusable code analysis services using a dedicated pipeline language, LSL (LASSO Scripting Language). This includes services like -

- code search and retrieval (interface-driven code search, test-driven code search)
- N-version assessment based on alternative implementations either retrieved via code search or generated using generative AI
- automated (unit) test generation
- test-driven software experimentation as a service
- benchmarking of tools/techniques
- ...

LASSO's core building blocks consist of several well-defined concepts and data structures

- Sequence Sheet Notation (SSN) - for representing tests (sequences)
- Stimulus Response Matrices (SRM) - for creating input configurations of system and test pairs, and for storing arbitrary observations (inputs/outputs) once executed by the special test driver for mass execution of code called the arena
- Stimulus Response Hypercubes - for enabling offline analysis of runtime observations stored in SRMs using popular data analytics tools

The platform is realized in Java using Spring Boot (https://spring.io/projects/spring-boot), while its architecture is realized on top of Apache Ignite (https://ignite.apache.org/). The platform's architecture, therefore, is distributed by design. It follows the manager/worker architecture style. The platform can be accessed via its website (RESTful API) and a webapp GUI.

![Alt text](https://github.com/SoftwareObservatorium/lasso/raw/main/doc%2Fimg%2Fquickstart_results.png)

![Alt text](https://github.com/SoftwareObservatorium/lasso/raw/main/doc%2Fimg%2Fquickstart_results_filters.png)



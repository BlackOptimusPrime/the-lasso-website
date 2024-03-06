---
title: Getting Started
categories:
- documentation
excerpt: |
  Read our [quickstart.md](https://github.com/SoftwareObservatorium/lasso/blob/main/doc%2Fquickstart.md) guide to get started with the LASSO platform.
feature_text: |
  ## Getting Started
  lasso lasso lasso
feature_image: "https://picsum.photos/2560/600?image=733"
image: "https://picsum.photos/2560/600?image=733"
---

Read our [quickstart.md](https://github.com/SoftwareObservatorium/lasso/blob/main/doc%2Fquickstart.md) guide to get started with the LASSO platform.

### Publications

A comprehensive description of LASSO and its core concepts and data structures is provided in

```bash
@phdthesis{madoc64107,
           title = {LASSO - an observatorium for the dynamic selection, analysis and comparison of software},
            year = {2023},
          author = {Marcus Kessel},
         address = {Mannheim},
        language = {Englisch},
        abstract = {Mining software repositories at the scale of 'big code' (i.e., big data) is a challenging activity. As well as finding a suitable software corpus and making it programmatically accessible through an index or database, researchers and practitioners have to establish an efficient analysis infrastructure and precisely define the metrics and data extraction approaches to be applied. Moreover, for analysis results to be generalizable, these tasks have to be applied at a large enough scale to have statistical significance, and if they are to be repeatable, the artefacts need to be carefully maintained and curated over time. Today, however, a lot of this work is still performed by human beings on a case-by-case basis, with the level of effort involved often having a significant negative impact on the generalisability and repeatability of studies, and thus on their overall scientific value.

The general purpose, 'code mining' repositories and infrastructures that have emerged in recent years represent a significant step forward because they automate many software mining tasks at an ultra-large scale and allow researchers and practitioners to focus on defining the questions they would like to explore at an abstract level. However, they are currently limited to static analysis and data extraction techniques, and thus cannot support (i.e., help automate) any studies which involve the execution of software systems. This includes experimental validations of techniques and tools that hypothesise about the behaviour (i.e., semantics) of software, or data analysis and extraction techniques that aim to measure dynamic properties of software.

In this thesis a platform called LASSO (Large-Scale Software Observatorium) is introduced that overcomes this limitation by automating the collection of dynamic (i.e., execution-based) information about software alongside static information. It features a single, ultra-large-scale corpus of executable software systems created by amalgamating existing Open Source software repositories and a dedicated DSL for defining abstract selection and analysis pipelines. Its key innovations are integrated capabilities for searching for selecting software systems based on their exhibited behaviour and an 'arena' that allows their responses to software tests to be compared in a purely data-driven way. We call the platform a 'software observatorium' since it is a place where the behaviour of large numbers of software systems can be observed, analysed and compared.},
             url = {https://madoc.bib.uni-mannheim.de/64107/}
}
```

See [publications.md](https://github.com/SoftwareObservatorium/lasso/blob/main/doc%2Fpublications.md) for more on LASSO and the platform.

## LASSO Scripting Language - Analysis Pipelines

See [pipelines.md](https://github.com/SoftwareObservatorium/lasso/blob/main/doc%2Fpipelines.md) for a few example LSL pipelines.

## Software Analytics - Analyzing SRMs (Stimulus Response Matrices)

A core design principle of the LASSO platform is to conduct extensive software analytics in external, popular data analytics tools. The platform, therefore, stores tracing data and reports in its distributed database using tabular representations.

Use our jupyterlab playground to explore and manipulate SRMs with Python pandas (https://pandas.pydata.org/)

- https://softwareobservatorium.github.io/jupyterlab/lab/index.html

See [analytics.md](https://github.com/SoftwareObservatorium/lasso/blob/main/doc%2Fanalytics.md) how resulting SRMs can be analyzed in Python and R.

![Alt text](https://github.com/SoftwareObservatorium/lasso/raw/main/doc%2Fimg%2Fquickstart_jupyterlab.png)

## Distributed Mode - Large scale analysis

The platform is designed to scale software code analysis and observation for big code.

See [distributed.md](https://github.com/SoftwareObservatorium/lasso/blob/main/doc%2Fdistributed.md) for instructions how to set up a LASSO cluster.

## Development of LASSO

See [development.md](https://github.com/SoftwareObservatorium/lasso/blob/main/doc%2Fdevelopment.md) for developer details (extension points, system tests etc.).

## Known Issues and Security Concerns

See [known_issues.md](https://github.com/SoftwareObservatorium/lasso/blob/main/doc%2Fknown_issues.md) for know issues, and [security.md](https://github.com/SoftwareObservatorium/lasso/blob/main/doc%2Fsecurity.md) for security concerns.

## Lasso Maven Modules

Note: For up-to-date information, have a look at the modules [here](https://github.com/SoftwareObservatorium/lasso/blob/main/pom.xml)

- pom.xml - parent POM of all modules (sets global properties and versions)
- evosuite-maven-plugin - customized version of EvoSuite's maven plugin
- randoop-maven-plugin - customized version of a Randoop's maven plugin
- lasso-maven-extension - LASSO's Maven Spy for maven-based test drivers (reports events etc.)
- ranking - Ranking module that offers preference-based ranking of software components based on multiple objectives
- crawler - LASSO's Maven Artifact Crawler
- analyzer - LASSO's Maven Artifact Analyzer (index creation etc.)
- index-maven-plugin - LASSO's plug in to index any (built) maven-managed projects
- core - Core module shared with other LASSO modules (mainly contains common data models, interfaces etc.)
- lql - LASSO's Query Language (describing interfaces and method signatures)
- datasource-maven - Query layer for LASSO's executable corpus
- sandbox - LASSO's sandbox execution environment based on Docker containerization
- lsl - LASSO's domain language (pipeline language)
- benchmarks - Temporary module that integrates various (LLM) benchmarks
- gai - contains interfaces for generative AI (e.g., OpenAI API etc.)
- engine - LASSO's workflow engine and actions API
- arena-support - Arena support module (shared classes)
- arena - LASSO Arena module (arena test driver)
- worker - LASSO's cluster worker application (web-based using spring-boot)
- webui - LASSO's next-generation web application based on Angular 16 and Material
- service - LASSO's cluster service and manager (web-based using spring-boot)
- lasso-llm - Companion module to benchmarks (facilities to integrate generated code obtained by MultiPL-E experiment)


# MRI Department Simulation using AnyLogic

A discrete-event simulation model of an MRI department developed to represent patient flow, examination and reporting workflows, resource utilization, and personnel optimization.

---

## Overview

MRI departments involve complex interactions between patients, medical staff, MRI scanners, queues, examination procedures, reporting processes, and administrative activities.

This project models an MRI department as a **Discrete-Event Simulation (DES)** using **AnyLogic**.

The model represents the patient journey through the MRI examination process as well as the subsequent reporting workflow. It also includes an optimization component for investigating the employment percentage of personnel involved in the MRI department.

The project combines:

**Process Modeling + Microsoft Visio + AnyLogic + Discrete-Event Simulation + Optimization**

---

## Problem

MRI departments can involve multiple patient pathways and resource constraints.

Patients may enter the system through different routes, require different preparation procedures, wait for available MRI scanners, undergo different examination procedures, and subsequently enter the reporting workflow.

These interactions can create queues, waiting processes, and resource utilization challenges.

The purpose of this project was to develop a detailed simulation model that represents these interactions and provides a computational environment for analyzing and improving the MRI department workflow.

---

## Objectives

The main objectives of the project were to:

* Model the workflow of an MRI department
* Represent different patient pathways
* Model patient registration and preparation
* Represent MRI scanner availability and waiting
* Model examination and post-examination processes
* Represent the MRI reporting workflow
* Analyze system behavior through discrete-event simulation
* Investigate resource utilization
* Optimize the employment percentage of personnel in the MRI department

---

## Process Modeling

Before implementing the simulation model, the MRI workflows were represented using process flowcharts.

The process diagrams were developed in **Microsoft Visio** and describe the main decision points, activities, patient pathways, and reporting processes represented in the simulation.

### MRI Examination Workflow

![MRI Examination Workflow](process/mri-examination-flowchart.png)

The examination workflow represents the patient journey through activities such as registration, EHR checking, consultation, preparation, MRI availability, waiting, contrast-agent administration when required, MRI examination, IV removal, and patient discharge.

### MRI Reporting Workflow

![MRI Reporting Workflow](process/mri-reporting-flowchart.png)

The reporting workflow represents the process from report preparation and physician review through possible report correction, advanced diagnostic processing, patient notification, and expert consultation.

The original editable Visio process model is also included in:

`process/MRI_Process_Flowchart.vsdx`

---

## Simulation Model

The process workflows were implemented as a **Discrete-Event Simulation model in AnyLogic**.

The model represents the interaction between patients, healthcare personnel, MRI scanners, queues, examination processes, and reporting activities.

The simulation includes:

* Patient registration
* EHR checking
* Insurance and copayment processes
* Patient preparation
* Consultation
* MRI availability and waiting
* Contrast-agent administration
* MRI examination
* MRI room selection
* IV removal
* Patient discharge
* MRI reporting
* Report review and correction
* Advanced diagnostic processing
* Patient notification

![Baseline AnyLogic Model](results/figures/baseline-anylogic-model.png)

The model was run for a simulated duration of **90 hours** to analyze system performance, including MRI process time and resource utilization.

---

## Input Modeling

The simulation uses probability distributions to represent stochastic process times and other input parameters.

Examples of the input distributions reported in the study include:

| Input Parameter                     | Distribution            |
| ----------------------------------- | ----------------------- |
| MRI report interpretation time      | Uniform (6, 12)         |
| Reception processing time           | Exponential (8)         |
| Copayment process with insurance    | Normal (0.75, 1)        |
| Copayment process without insurance | Normal (2.35, 1.54)     |
| Escort to bed                       | Triangular (0.5, 1, 2)  |
| Patient transfer                    | Triangular (3, 5, 10)   |
| Consultation                        | Triangular (10, 15, 20) |

Additional input distributions were used for examination and preparation processes according to the sources described in the study.

---

## Model Assumptions

The simulation model uses several assumptions described in the study:

* Patients arrive on time.
* Emergency patient care is prioritized.
* Staff lateness is assumed to be zero.
* Resource travel time is negligible.
* The four MRI scanners operate without failures.
* Urgent reports are exclusive to emergency patients.

These assumptions define the operating conditions under which the simulation model was evaluated.

---

## Optimization

In addition to the baseline simulation model, an optimization experiment was performed to investigate the employment percentage of personnel in the MRI department.

The optimization considered personnel and room-related roles involved in performing MRI examinations.

The objective was to improve the utilization of available human resources and investigate an improved personnel configuration.

### Optimization Convergence

![Optimization Convergence](results/figures/optimization-convergence.png)

The optimization process consisted of **147 iterations**.

The best reported outcome occurred at **iteration 132**, where the objective function reached **5.836**.

The optimization graph shows the progression of the objective function across iterations and distinguishes between current solutions, the best infeasible solution, and the best feasible solution.

### Optimization Result

![Optimization Result](results/figures/optimization-result.png)

The optimization result summarizes the selected personnel configuration.

The study considers roles including radiographers, nurses, admissions staff, doctors, consultants, and personnel associated with the MRI rooms.

---

## Results

The project demonstrates how discrete-event simulation can be used to represent a complex MRI department as a dynamic system.

The resulting model provides a framework for:

* Representing complex patient pathways
* Modeling queues and waiting processes
* Representing interactions between patients and healthcare resources
* Evaluating resource utilization
* Testing alternative resource configurations
* Investigating personnel optimization

The study reports that the optimization process improved the employment percentage of personnel and overall resource utilization within the modeled system.

---

## How to Open the Simulation Model

1. Install **AnyLogic**.
2. Clone or download this repository.
3. Open the model file:

```text
model/FinalLogicT3.alp
```

4. Open the model in AnyLogic.
5. Review the process logic, resources, parameters, and optimization experiment.

---

## Key Takeaway

This project demonstrates the use of **discrete-event simulation and optimization to analyze a complex healthcare operation**.

Instead of representing the MRI department as a static process, the model represents patients, resources, queues, examination procedures, and reporting activities as interconnected components of a dynamic system.

The project therefore combines:

**Process Modeling → AnyLogic Simulation → Resource Analysis → Optimization**

---

## Reference

Haghshenas, M., Tale, B., & Shahabi Haghighi, H. (2024).

**Simulation and enhancement of an MRI department using Anylogic.**

10th International Conference on Industrial and Systems Engineering (ICISE 2024), Ferdowsi University of Mashhad, Iran.

The publication is referenced as the academic basis of this project. 

---

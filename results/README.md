# Results

This folder contains the main visual outputs of the MRI department simulation and optimization model.

The figures illustrate the implemented AnyLogic model, the optimization process, and the resulting resource configuration.

---

## 1. Baseline AnyLogic Simulation Model

The baseline simulation model represents the integrated MRI examination and reporting workflows.

![Baseline AnyLogic Model](figures/baseline-anylogic-model.png)

The model represents the interaction between patients, healthcare resources, MRI scanners, queues, examination processes, and reporting activities.

---

## 2. Optimization Convergence

The optimization experiment evaluates different personnel configurations and tracks the objective function across iterations.

![Optimization Convergence](figures/optimization-convergence.png)

The reported optimization process completed **147 iterations**.

The best reported outcome occurred at **iteration 132**, where the objective function reached **5.836**.

The graph illustrates the progression of the optimization process and the improvement of the objective function across iterations.

---

## 3. Optimization Result

The final optimization output summarizes the selected resource configuration.

![Optimization Result](figures/optimization-result.png)

The optimization considers personnel and room-related roles involved in the MRI department, including radiographers, nurses, admissions staff, doctors, consultants, and MRI-room personnel.

---

## Interpretation

The results demonstrate how discrete-event simulation and optimization can be combined to investigate resource utilization in a complex healthcare workflow.

The model provides a computational framework for:

* Representing patient flow
* Investigating queues and waiting processes
* Modeling healthcare resources
* Evaluating resource utilization
* Testing alternative personnel configurations
* Supporting operational improvement

The reported optimization results indicate an improvement in the employment percentage of personnel and resource utilization within the modeled system.

---
layout: project
title: Subscale Wind Turbine Blade Design Project 
description: (Cornell University MAE 4247) Blade Design Project
technologies: [Autodesk Fusion, Python, Wind Tunnel Testing]
image: /assets/images/Wind Turbine Photo.jpg
---

For my Cornell Heat Transfer Lab project, I collaborated with a team of four to design and optimize a small wind turbine blade aimed at maximizing power generation under a Weibull wind speed distribution (mean 4.59 m/s). The project combined theoretical modeling and practical design considerations, with the goal of achieving maximum power output within constraints on blade length, hub radius, RPM, and structural safety.

To complete tasks in parallel, our team's developed workflow pattern which is shown here:
![Workflow Diagram]({{ "/assets/images/design Proc.jpg" | relative_url }}){: .inline-image-r style="width: 2000px"}

We applied Blade Element Theory and numerical optimization in Python to determine the optimal blade geometry. Using differential evolution, the optimizer adjusted pitch, twist, and chord length across ten discretized segments to maximize integrated power over the probability distribution of wind speeds. NACA 4412 airfoils were selected for their strong performance at low Reynolds numbers, and a quadratic fit ensured smooth pitch variation along the blade. Throughout, we maintained a minimum factor of safety of 1.5 and incorporated manufacturability constraints for 3D printing.

![Shaded rendering of earlier version]({{ "/assets/images/balde pic.jpg" | relative_url }}){: .inline-image-r style="width: 200px"}

My primary contribution was the CAD design of the blade, where I parameterized the geometry to match the optimizer outputs and ensured mechanical strength at the hub joint. The physical blade included segmented twists, interpolated sweeps, and filleted hub connections to reduce stress concentrations. Testing involved gradually increasing wind speeds while recording torque, RPM, and power output. Although the blade operated safely, it stalled earlier than predicted and produced lower power than simulations suggested, highlighting the effects of unmodeled losses and optimizer limitations.

Power Curves for the blade at different wind speeds are plotted here: 
![Photo of Power Curves]({{ "/assets/images/power curves.jpg" | relative_url }}){: .inline-image-l}

Key takeaways include the importance of refining optimization algorithms, expanding population sizes for better convergence, and incorporating experimental lift, drag, and friction data. Future iterations could also account for 3D flow effects and more advanced blade element modeling. Overall, this project offered hands-on experience integrating theoretical analysis, numerical optimization, and practical manufacturing constraints to address real-world wind turbine design challenges.
# Agent-Based-Model-ABM-of-Rumor-Propagation-in-a-Team
This repository contains an ABM model developed in NetLogo to simulate the diffusion and containment of a rumor (or misinformation) within a fixed-size team or social network. The core objective was to modify an existing network-based epidemic model to incorporate social influence mechanisms, specifically the role of formal and informal leaders.
Project Overview

The project confirms the hypothesis that the presence and influence of designated leaders can significantly mitigate the spread and longevity of misinformation within an organizational structure.


The simulation adapts the classic "Virus on a Network" model to study organizational behavior. The "virus" is reinterpreted as a "rumor" or "piece of misinformation".


**--DESCRIPTION--**

**Agents**
Two types of agents were introduced: 'Zwykly' (Regular Member) and 'Lider' (Leader). Leaders are immune to the rumor and act as stabilizers.

Agents are differentiated by a new typ variable. Leaders are visually represented as cyan triangles.

**Rumor States**

States were adapted from epidemic terms: 'uwierzył' (believed/spreading), 'podatny' (susceptible), and 'ignoruje' (immune/resistant).

Variables like infected were functionally renamed to uwierzył? (believed) and immune to ignoruje? (ignores).

**Influence Mechanism**

The Leader's Influence (wpływ-lidera) is implemented as a dampening factor (modificator) that reduces the probability of a regular agent believing a rumor if leaders are present in their immediate network neighborhood.

Probability of spread is dynamically calculated: prawd-rozpowiedzenia-plotki * modyfikator.

**Metrics**

A new state, czas-w-plotce (time-in-rumor), tracks how long an agent believes the rumor to measure the longevity of the misinformation.

Interface plot tracks the 'Średni czas wiary w plotkę' (Average time believing rumor).

**Key Simulation Findings**

The simulations confirmed that both the number of leaders and the strength of their influence are critical factors in rumor containment:

Rumor Containment: As the parameter wpływ-lidera (leader influence) systematically increased, the average number of people who believed the rumor significantly decreased, leading to near-complete suppression at maximum influence levels.

Rumor Longevity: The highest average time spent believing the rumor was observed at intermediate levels of leader influence. This suggests that moderate leadership influence tends to slow down the process of spreading and recovery rather than immediately stopping it.

Simulation Duration: High leader influence generally reduced the overall duration of the simulation (time until the rumor dies out), confirming their role as stabilizing elements in the network.


**Documentation**

Detailed analysis, model characteristics, modification rationale, and visualization of results are available in the project files:

Report.docx

ABM_Model_with_leader.pdf

# Summary
[Hutchins et al 2011: Intelligence-Driven Computer Network Defense Informed by Analysis of Adversary Campaigns and Intrusion Kill Chains](https://lockheedmartin.com/content/dam/lockheed-martin/rms/documents/cyber/LM-White-Paper-Intel-Driven-Defense.pdf)

## Abstract

* Generally, defense tools (intrusion detection and anti-virus) focus on the vulnerable component of risk. This kind of tools also relies on the fact that an intrusion is successful
* There is now a new type of threat nammed "Advanced Persistent Threat" (APT). In this category, we have some adversaries that are well-resourced and trained. They conduct intrusion campaigns during years and which affect sensitive economic or national security information. To achieve their goals, they use advanced tools and techniques that bypass conventional security methodologies
* By using some network defense techniques that use the knowledge about APT, you allow defenders to create a feeder loop of intelligence that leads them to achieve a state of information superiority, which reduces the adversary's probability of success with each new intrusion attempt.
* The utilization of a kill chain model to outline the stages of intrusions, correlating the adversary's attack chain indicators with defensive measures, recognizing patterns that connect individual breaches to larger campaigns, and recognizing the cyclical nature of intelligence collection are the foundation of intelligence-based computer network defense (CND).
* Because of the evolution of the threads, it is necessary to use an intelligence-based model. With this kind of model, the defenders don't only mitigate the component of risk. 


## 3.2 Intrusion Kill Chain

* We use kill chain as a systematic process to target and engage an adversary to create desired effects.
  * We also use kill chain in the military domain as the U.S. military with their targeting process: find, fix, track, target, engage, asses (F2T2EA).
  * A kill chain is a end-to-end process, because if one step fails, it will interrupt the entire process.
* By using the previous base, a kill chain has been developed especially for the intrustions. It is based on the fact that an intrustion involves that the aggressor has to develop enough power to be able to establish a presence inside trusted environment.
 * This kill chain is composed of the following elements:
   * **Reconnaissance:** This step represent the research, the identification and the selection of targets.
   * **Weaponization:** It is the coupling between a remote access with an exploit into a deliverable payload. Nowadays, clients application such as PDF or Word documents are used as a weaponized deliverable.
   * **Delivery:** To transmit the weapon to the target, email attachements, web sites and USB stick are often used.
   * **Exploitation:** When the weapon is delivered to the target, the weapon can use some vulnerabilites from the OS (automatic execution from code, for example), applications, or the users directly.
   * **Installation:** This step concern the installation of a backdore or a trojan inside the victim system. It creates a persistent access for the aggressors.
   * **Command and Control (C2):** Compromised hosts send signals to an Internet control server to establish a C2 channel, which is typically set up manually rather than automatically by APT malware. Once established, the C2 channel allows intruders to have direct access within the target environment.
   * **Actions on Objectives:** It is only in this step that the intruders (aggressors) can take actions to achieve their objectives. Generally, the main objective is data exfiltration (collecting, encrypting, and extracting) from the victim environment.


## 3.3 Courses of Action
The intrusion kill chain is a useful model for defenders to understand and counter the specific processes an attacker uses to target an enterprise. By aligning defensive capabilities with the kill chain, defenders can measure their effectiveness and plan investments to address any gaps. This approach, known as intelligence-driven cyber defense, involves making security decisions and measurements based on a deep understanding of the attacker.

![Table 1: Courses of Action Matrix](https://miro.medium.com/max/903/1*7q_uh4DLZ5b62i_e8jfTxA.jpeg)
<p align="center">
  <img width="903" height="577" src="[https://www.python.org/python-.png](https://miro.medium.com/max/903/1*7q_uh4DLZ5b62i_e8jfTxA.jpeg)">
</p>



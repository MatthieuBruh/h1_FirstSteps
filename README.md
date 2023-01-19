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
   * ### Reconnaissance
    * This step represent the research, the identification and the selection of targets.
   * ### Weaponization
    * It is the coupling between a remote access with an exploit into a deliverable payload. Nowadays, clients application such as PDF or Word documents are used as a weaponized deliverable.
   * Delivery
   * Exploitation
   * Installation
   * Command and Control (C2)
   * Actions on Objectives

# Snake Eyes

### Safe. Powerful.

## The Problem:
The world’s biggest killer is ischaemic heart disease, responsible for 16% of the world’s total deaths, according to the WHO. In Canada, heart disease is the second leading cause of death, and the number one leading cause of years lost in life. 

Once a heart attack has started, there is nothing that can be done to reduce the amount of damage, or likelihood of death. 

However, if heart attacks were able to be predictable, then measures could be taken to avoid the heart attack entirely, or greatly reduce its damage, such as by taking aspirin, or other medications. 

Our project uses a neuro-symbolic artificial intelligence, to learn over time what the predicting signals for heart attacks are, and alert medical staff about an impending heart attack in hospitals, potentially saving millions of lives.


## Why current solutions don't work:
In order for AI systems to be deployed in the real world, especially in safety-critical situations, such as hospitals, it is crucial that they are safe, explainable, and robust.


## Our Solution:
First, we pre-process the raw ECG waveforms and convert them to more useful values such as RR times and heart rate. 

These values are then fed into our symbolic AI system, which is able to detect abstract patterns in data, and generalize these patterns to a much greater extent than what neural networks are capable of. We then use these patterns to predict future ECG data for the patient. 

The symbolic AI system itself works by using evolutionary techniques to evolve ‘rules’. Each rule has a precondition, and an output. As the AI system is being fed data, if the data matches the precondition for a rule, the rule ‘fires’. The fired rules output represents the next predicted state. In the next time step, if the prediction matches the observation, the fired rule is rewarded, and is more likely to be chosen again in the future. Otherwise, it is punished, and new rules are evolved. This allows our system to be a self-supervised learning system, with no human input required.

Finally, we take the predicted future ECG data and pass it through a decision tree, to find the health risk for that patient. That information is then presented to the doctors, including the health risk, and the predicted time.

## Summary:
There are many advantages to our system. First, it is explainable, transparent, and robust. Thus, safety can be guaranteed. Second, there is no human intervention or labelled datasets required after the initial training phase. The system will continue learning autonomously on its own and will improve its performance over time. Finally, the pipeline is extremely flexible, it allows the system to cover a wide variety of situations, such as predicting COVID, or post-surgery outcomes. It also allows for easy integration of human knowledge into the system, the system will then autonomously verify if the knowledge fits observations. If so, it will keep the knowledge and use it in the future. This allows the system to get up to speed quickly on new tasks.


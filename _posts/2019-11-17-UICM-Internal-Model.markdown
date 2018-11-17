---
layout: post
title:  "An Unified Intelligence-Communication Model for Multi-Agent System: Overview and Case Studies -- Chapter Two:  Modelling the Information Source and Destination in the Agent"
date:   2018-11-17 20:10:16 +0800
categories: Open-Access Research Paper
---
**Authored by: Bo Zhang, Jinyu Yang, Zixuan Zhang, Gangsong Ding and Qinhao Wu**

This paper would be fully open-access. My handwriting manuscript is prepared, but I need time to craft it into a rigorous research treatize. 

This Chapter introduces the model for information source and destination in the UIC model as proposed in the last chapter. This chapter would cover the following aspects.
+ The information source and destination is modelled, following the generic learning agent model, which includes a performance element, a learning element, a critic and a problem generator. 
+ This Chapter reviews the different agent models, with an emphasis on the design of learning agent model, and propose an unified, complete and operable design for the learning agent that may lead to strong AI. 
+ Along with the perception and action model proposed in the last chapter, we may form the complete UIC model for an intelligent agent.   

Further insights of the UIC model, as proposed in the outline of this paper, would be discussed in depth in the following-up Chapters. 

## Connecting the Information Source and Destination
If we stick to the Shannon's model of communication, the information source and destination may be disconnected in a single agent. However, in order to allow an agent to receive information from the outside world, to process information and to change the world by transmitting information, a connection between the information source and destination in the agent is inevitable. Therefore, a question arose:

**How does an intelligent agent process the information within itself?**

This paper is definitely NOT the first to answer the question, so let us review the agent internal models.

## A Brief Review of the Agent Internal Models
An overview of the major five categories of agent models is given in Section 2.4 of [1] or in the [wikipedia page](https://en.wikipedia.org/wiki/Intelligent_agent). Except for the simplest form of agent model, the rest of the agent models includes an **internal world model**. 

### Simple Reflex Agent model (SRA model)
The agent function is based on the condition-action rule: if condition then action. So it may work well in a fully-observable world.
<div align="center">
<img src="/assets/images/1_Simple_reflex_agent.png" width="80%" height="80%" />
<br/>
Figure 2. Simple Reflex Agent model (SRA model)[1]
</div>

### Model-based, Reflex Agent model (MRA model)
A **world model** is introduced to maintain some kind of structure, which describes the part of the world which cannot be observed.

<div align="center">
<img src="/assets/images/2_Model_based_reflex_agent.png" width="80%" height="80%" />
<br/>
Figure 2. Model-based, Reflex Agent model (MRA model)[1]
</div>

### Model-based, Goal-Based Agent model (MGA model)
**Goal information** is introduced to describe desirable situations and allow an agent to choose among multiple possibilities, selecting the one which reaches a goal state. In the complex adatptive system [2], Holland proposed to incorporates co-existence of multiple micro SRA agents in an agent, and allowing the agent to select action sequences[2]. 

<div align="center">
<img src="/assets/images/3_Model_based_goal_based_agent.png" width="80%" height="80%" />
<br/>
Figure 3. Model-based, Goal-Based Agent model (MGA model)[1]
</div>

### Model-based, Utility-Based Agent model (MUA model)
**Utility function** is introduced to measure the space spanning from the goal state and the non-goal state. 

<div align="center">
<img src="/assets/images/4_Model_based_utility_based.png" width="80%" height="80%" />
<br/>
Figure 4. Model-based, Utility-Based Agent model (MUA model)[1]
</div>

### Learning Agent model (LA model) 
Afore-mentioned agent models are **static**, as they do not explain how an agent may **learn and evolve**. Therefore, the LA model is quite different by introducing four conceptual components: 
+ A **performance element** to select external actions, which is equivalent to a static agent model that percepts from the world and decides external actions.
+ A **learning element** to make improvements by changing the performance element and gathering knowledge from the performance element. 
+ A **critic** to enable feedback on how the agent is doing and how the performance element may be modified to do better.
+ A **problem generator** to select actions leading to new and informative experiences.

<div align="center">
<img src="/assets/images/5_IntelligentAgent-Learning.png" width="80%" height="80%" />
<br/>
Figure 5. Learning Agent model (LA model) [1]
</div>

### Rethink the Learning Agent Model with an Internal World Model (WM)
Although it is not pointed out explicitly in [1], the learning agent model may include a world model in its performance element. Therefore, the learning element may change the world model. 

**If the design principle of the learning agent model is accepted (why NOT if we have not come up with a more reasonable model)**, then the problem of designing an intelligent agent may be further decomposed as follows:
+ **Performance Element Design**: What is inside the performance element and what is a WM looks like?
+ **Learning Element and Critic Design**: How to gather knowledge and improve performance based on the feedback provided by the critic in a complex dyanmic world? Also, how to update the WM and rest of Performance Element? 
+ **Problem Generator Design**: How to find a GOOD tradeoff between short-term and long-term reward in a changing world?  

The answers to the above four questions may lead to the design principles of **Strong Artificial Intelligence**. Therefore, the answers to these questions are so attractive and many pioneering thoughts (NOT solutions) have been proposed to light our way. 

#### Agent Model in Complex Adaptive Systems
Professor Holland H. John is the pioneer of Complex Adaptive System Theory. In his 1995 treatize [2], Holland proposed the following works:
+ **Performance Element Design**: Holland proposed the design of the **performance system**, which has an input from sensors, an output to the acutators, while the performance element is a collection of interactive micro-agents based on IF-THEN rules.  
+ **Learning Element and Critic Design**: A **credit assignment** mechanism was proposed to allow multiple micro-agents to compete with each other. The micro-agent with higher reward from the critic is given a larger credit, hence improving performance of the agent. 
+ **Problem Generator Design**: A **rule discovery** mechanism was proposed based on the genetic algorithm, which was also invented by Holland.  

#### Agent Model with Commonsense Thinking
In [4], Professor Marvin Minsky proposed to model a (human) brain into a collection of **resources**, which may be activated by different **emotion states**. The thinking activities may be broken down into a series of six-layered actions: instinctive reactions, learned reactions, deliberate thinking, reflective thinking, self-reflective thinking and self-conscious reflection. **Higher-level thinking is built upon the ones below, and the lowest instinctive reaction level is driven by If-Do rules.**

Specifically, we may re-organize Minsky's thoughts as follows:
+ **Performance Element Design**: The instinctive reactions may be modelled as IF-DO rules, which are equivalent to Holland's IF-THEN rules. 
+ **Learning Element and Critic Design**: The higher-layer actions are built upon instinctive reactions. **Minsky emphasized the limitation of IF-THEN rules because the scalability of directly using IF-THEN rules for describing the complex world is infeasible, therefore, representations, evaluations and manipulations of higher-level abstraction is required.** It should be noted that Holland also dived much deeper later on following the same rule of agent model, introducing the concept of **dyanmic finitely generated systems** for modelling complex interactions between agents [3]. 
+ **Problem Generator Design**: The layers higher than deliberate thinking motivate an agent to criticize the reactive actions and explore un-explored world.  

#### Self-Supervised Learning Agent Model
Very recently, Professor Yann Lecun proposed an agent model based on the concept of **Self-Supervised Learning** with both a **deep structure** and **a world Model**[5]. The agent may do reasoning by combining predicting and planning with the aid of model-based deep reinforcement learning. Specifically, Lecun considered the following strategies:
+ **Performance Element Design**: A world model is needed, accumulating background knowledge about how the world works and perhaps include common sense. Deep (artificial neural) networks may model complex interactions with the aid of non-linear transformations within a manageable scale.
+ **Learning Element and Critic Design**: Latent-variable forward models is proposed for planning and learning policies, but it is also far from a complete solution.
+ **Problem Generator Design**: It seems Lecun did not consider it for the moment.  

<div align="center">
<img src="/assets/images/Agent-with-World-Model.png" width="80%" height="80%" />
<br/>
Figure 6. LeCun's Agent Model with an Internal World Model[5]
</div>

### Unifying the Learning Agent Models
The models proposed by Holland[2][3], Minsky[4] and Lecun[5] may approach the design of a learning agent model for strong AI from different perspective and different emphases. With some non-difficult manipulation of their models, the performance element, learning element and critic design for an unified intelligent agent model may be proposed as follows: 
+ **Performance Element Design: An aggregation of micro-agents described by simple reactive rules**.
+ **Learning Element and Critic Design: A collection of action modules for building, manipulating and evaluating higher-level (likely to be non-linear) representation of micro-agents' behaviours**.

However, it is not apparant to come up with a concrete and operable design for the **Problem Generator Design** yet. Here, we try to solve the problem based on the following basic understandings: 
+ Non-Complete Representation as Motives: Even though an agent have non-linear basis/generators for representing very complex interactions in the world, we may still face up to non-complete representations, with limited resources. Therefore, the agent may adopt a sub-optimal (or an action that cannot be proved optimal with limited resource) in the world.
+ Multiple-Trial in the World Model: Though the agent cannot find the optimal actions, the agent may come up with a set of sub-optimal candidate actions, where the size of the set is limited based on available resources. After taking previous actions in the world, these candidate actions could be tested within the updated world model.

Based on the above insights, we may propose a operable pathway to the problem generators for strong AI.
+ **Problem Generator Design: A set of modules to evaluate non-complete representation of complex action-reward interactions, to generate candidate action set, and to trigger reflective actions in the world model.**

### Short Conclusions
In this chapter, we review the different agent models, with an emphasis on the learning agent model design, and propose an unified, complete and operable design for the learning agent. Along with the perception and action model proposed in the last chapter, we may form the complete UIC model for an intelligent agent. 

In the next chapter, we would use the built UIC model to unify models for an agent and multi-Agent systems. 

### References
[1] Russell, Stuart J. and Peter Norvig. Artificial intelligence: a modern approach. Pearson Education Limited, 2011.
[2] Holland, John H . Hidden Order: How Adaptation Builds Complexity. Leonardo, 1995.
[3] Holland, John H . Signals and boundaries : building blocks for complex adaptive systems. MIT Press, 2014.
[4] Minsky M. The Emotion Machine: Commonsense Thinking, Artificial Intelligence, and the Future of the Human Mind[M]. SIMON & SCHUSTER, 2007.
[5] Yann LeCun. Learning World Models: the Next Step towards AI. IJCAI KeyNote Speech, 2018.


<div id="gitmentContainer">
</div>
<link rel="stylesheet" href="https://jjeejj.github.io/css/gitment.css">

<script src="https://jjeejj.github.io/js/gitment.js"></script>
<script>

var gitment = new Gitment({
    
id: '<%= page.date %>',
owner: 'uicm-mas',
    
repo: 'uicm-mas.github.io',
    
oauth: {
        client_id: '1b244c25e58a3bf45ece',
        
client_secret: '49fae86caef4f920db2a064176bd237a03c5ae3e',
   
 },

});

gitment.render('gitmentContainer');

</script>



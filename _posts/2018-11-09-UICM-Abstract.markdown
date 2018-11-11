---
layout: post
title:  "An Unified Intelligence-Communication Model for Multi-Agent System: Overview and Case Studies -- Abstract and Outline of the Paper"
date:   2018-11-09 16:10:16 +0800
categories: Open-Access Research Paper
---
**Authored by: Bo Zhang, Jinyu Yang, Zixuan Zhang, Gangsong Ding and Qinhao Wu**

This paper would be fully open-access. My handwriting manuscript is prepared, but I need time to craft it into a rigorous research treatize. 

## Abstract 

Motivated by Shannon's model and recent rehabiliation of self-supervised artificial intelligence having a "World Model", this paper propose an **unified intelligence-communication (UIC) model** for describing a single agent and any multi-agent system. 
The model try to incorporates the following contributions.
+ The environment is modelled as the generic communication channel between agents. 
+ The model leads to important insights on that "Any intelligent structure is an aggregation of multiple agents", where the simplest or basic unit of a agent is represented by "IF-THEN" rule**, as proposed by Holland and Marvinminsky.
+ The model unifies several well-adopted agent architecture, e.g. Observe-Orient-Decide-Act (OODA) model, world-model based agent model and rule-based agent model, and provides information theory societies **a common model for practicing quantitative analytical methods**.
+ The model provides an unified approach to investigate a multi-agent system (MAS) having multiple action-perception modalities, e.g. explicitly information transfer and implicit information transfer.

Then, the paper provide case studies, exemplifying the adoption of the UIC model, 
+ Analysis of natural MAS, e.g. a bee-colony
+ Design of artificial MAS, e.g. co-design of communication-perception-action in multi-robot system

Finally, the paper provides further insights motivated by the UIC model, such as:
+ Unification of single intelligence and collective intelligence
+ An possible explanation of intelligence emergence
+ A dual model for agent-environment intelligence hypothesis

## Outline of the Paper
The paper would be released by Chapters, and may be updated because of continuous 
introspection of the author and feedback from readers. 

Please contact bo.zhang.airc@outlook.com to share your opinions and suggestions for the paper. 

Please note the following contents may change during the release of the paper.
+ Chapter 1: A Brief Introduction of the UIC Model - From Shannon's Perspective
+ Chapter 2: Modelling the Information Source and Destination in the Agent
+ Chapter 3: Unifying models for an Agent and a Multi-Agent System (MAS)
+ Chapter 4: UIC Model for Quantifying Intelligence Level of MAS 
+ Chaptre 5: Case Study of UIC Model in Analyzing Natural MAS
+ Chapter 6: Case Study of UIC Model in Designing Artificial MAS
+ Chapter 7: Hypothesis of UIC Model for Explaining Intelligence Emergence Mechanism
+ Chapter 8: Hypothesis of UIC Model for Explaining Intelligence of the Environment
+ Chapter 9: Conclusions and Future Research

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
        client_id: '18a165f5d54ee50fc269',
        
client_secret: '8abc39c0bae1859cb71bbe4cef2c982179c096ca',
   
 },

});

gitment.render('gitmentContainer');

</script>


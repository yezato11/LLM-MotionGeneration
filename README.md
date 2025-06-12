# LLM-MotionGeneration

This repository contains sample prompts from our robots to enhance the clarity of our paper titled:
**"LLM-Driven Approach for Motion Control in Human-Robot Dialogue for Elevating Engagement"**  
(submitted to IEEE RO-MAN 2025)

---

## Overview

We implemented two different generation strategies to generate motion based on spoken dialogue:

- 🟩 **LLM-GPA**: Generating Primitive Actions  
- 🟦 **LLM-GJA**: Generating Joint Angles

Each method uses Large Language Models (LLMs) to generate co-speech motions in a context-aware and expressive manner.

---

## 🟩 LLM-GPA: Generating Primitive Actions
<p align="justify">
The prompt used in LLM-GPA is composed of three main components: context, instruction, and a list of actions. The context outlines a task in which the LLM is employed to control a robot's movements. The instructions—developed through Chain-of-Thought (CoT) reasoning—guide the LLM through the task step by step: starting with sentence segmentation, followed by gesture description, assigning actions to individual body parts to form complete gestures, and finally, checking for consistency and fluidity. These individual gestures can then be assembled into a full motion sequence. An example prompt from LLM-GPA is provided below.
</p>

<img src="https://github.com/user-attachments/assets/5802bbff-c042-4e00-9597-7e43612b39eb" alt="GPA"/>

## 🟦 LLM-GJA: Generating Joint Angles
<p align="justify">
In contrast, LLM for Generating Joint Angle Parameters (LLM-GJA) employs the LLM to determine the robot’s servo joint angles. This is done by designing a prompt that includes the context, servo specifications, and a set of instructions. The context is typically shared between both LLM-GPA and LLM-GJA. The servo specifications outline the mapping of servos, their rotational limits, and movement directions. While the instructions are generally derived using the same Chain-of-Thought method as in LLM-GPA, the key difference is that the described gestures are translated into specific servo angles required to produce motions. An example prompt for LLM-GJA is provided below.
</p>

<img src="https://github.com/user-attachments/assets/2b239b1b-980b-4142-ad2d-50e718e6f226" alt="GPA"/>

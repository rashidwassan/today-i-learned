# Expert Systems

## Definitions
- Expert systems are `computerized advisory programs` that attempt to imitate the reasoning process and knowledge of experts in solving specific types of problems.
- Employees human information to use it for problem solving which requires human expertise.
- Complex AI programs.
- Computer that simulates human intelligence and behavior in certain domains.
- Used to help expert humans or used as their replacement.
- Solves the problem with tricks, shortcuts, and heuristics.

## Description
- Well designed expert systems imitate the reasoning process that experts use in problem solving.
- Such systems can be used by non experts to improve their problem solving capabilities.
- The most widely used way of representing domain knowledge in expert system is a set of `production rules`.

## Expert systems are:
- `Good for:` limited domains where expert information is available, providing expert opinion in remote sites. Application of heuristic knowledge.
- `Not good for:` reasoning, recognizing limits of their ability, handling inconsistent knowledge.

## Basic Concepts of Expert Systems
### Expertise
- It is extensive, task specific knowledge.
- Acquired from training, reading, and experience.
- Expertise may include: Facts about problem area, theories, hard and fast rules, global strategies, and Meta Knowledge.

### Experts
- Expressed with respect to its degree of expertise.
- Take problems stated in arbitrary manner and converts into the form for rapid and effective solution.
- Should explain the results, learn new things about the domain, reconstruct knowledge.
- All activities must be done efficiently.

### Transferring Expertise
- The objective of an expert system is to transfer expertise from an expert to a computer and then to other non experts.
- This process involves four activities: `Knowledge acquisition, representation, inferencing, and transfer`.
- The knowledge is stored in computer in `knowledge base`.

### Inferencing Rules
- Ability to reason.
- As program has the access to knowledge base, it can make inferences.
- Inferencing takes place in Inference Engine.
- `Rules:` Most commercial systems are rule based systems. Knowledge is stored in form of rules.

### Explanation Capability
- Ability to explain system's advice and recommendations and even to justify why a certain action was not recommended.
- The explanation and justification is done in a subsystem called the `justifier`, or the explanation subsystem.

## Structure of Expert Systems:
Two main parts:
- `The Development Environment:` Used to build the system components and introduce knowledge.
- `The Consultation Environment:` Used by non expert to obtain knowledge.
![](https://i.imgur.com/c57gLme.png)

## Components of an Expert System:
1) `Knowledge Acquisition Subsystem:`
2) `Knowledge Base`
3) `Inference Engine:` It is the brain of expert systems, also known as control structure of the rule interpreter.
   1) Interpreter
   2) Scheduler
   3) Consistency Enforcer
4) `Blackboard:` area of working memory. Plan, Agenda, Solutions.
5) `User Interface:` Language processor for friendly, problem-oriented communication between the user and the computer.
6) `Explanation Subsystem (Justifier)`.
7) `Knowledge Refining System: `Human experts have a knowledge refining system, that is, they can analyze their own performance, learn from it, and improve it for future consultations.

### Human Element in Expert Systems
At least two humans (expert, user) participate in the use and development of an expert system.
- `The Expert: ` Domain expert having expertise, special knowledge, judgement, experience. The expert knows which facts are important and understands the meaning of relationships among facts.
- `The Knowledge Engineer: `The knowledge engineer helps the expert structure the problem area by interpreting and integrating human answers to questions, drawing analogies, posing counterexamples, and bringing to light conceptual difficulties.
- `The Users`

### Working of expert systems
Three major activities:
1) Development
2) Consultation
3) Improvement


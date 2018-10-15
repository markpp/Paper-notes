# Challenges in shared-environment human-robot collaboration

@article{hayes2013challenges,
  title={Challenges in shared-environment human-robot collaboration},
  author={Hayes, Bradley and Scassellati, Brian},
  journal={learning},
  volume={8},
  number={9},
  year={2013}
}

- Outlines four major challenges in building complete autonomous, socially collaborative systems and discuss how the state-of-the-art from the fields of HRI, LfD, hierarchical learning, and reinforcement learning can be synthesized to help solve these problems.
- How can co-robots enable and facilitate bi-directional
intent recognition?
- How does a co-robot know what roles to take when
working with human teammates?
- How does a co-robot know when to trade off task
execution optimality for co-worker preferences?
- How does a co-robot self-evaluate during live collaboration?

### What
-  Today’s robots operate autonomously with speed and precision within tightly controlled, isolated environments. The next step in personal and industrial robotics is to move robots out of isolation and into collaborative relationships, operating side-by-side with human personnel. As demonstrated in recent years.
- the introduction of these systems to real-world environments requires a substantial engineering effort with a carefully planned interaction methodology, so that human operators can effectively utilise robotic resources.
- Even with the current state-of-the-art in skill acquisition and execution, robots have difficulty performing at their full potential when removed from the typically well-controlled environment of the lab.
- Proposes the term collaborative task execution to describe an agent autonomously performing a task either collaboratively with or in the presence of other agents, while respecting any associated social roles and divisions of responsibility.
- A skill is defined as a temporally extended action and is assumed to minimally include a set of known preconditions, expected post-conditions, and known goal states. A task is a tree of skills and a plan as an arrangement of skills resulting from a complete traversal of that tree, respecting any ordering constraints. A plan constructed to include multiple agents may include parallel branches of skill execution, subject to the ordering constraints of the individual skills involved.
- Creating robot control systems that are capable of engaging in collaborative behaviors with humans are incredibly complex. Such systems require many components to operate safely and properly, often leveraging the state-of-theart in Learning from Demonstration (LfD), intention detection, speech recognition, non-verbal communication, planning systems, physical manipulation, and more
- Shared-space human-robot collaboration can be a powerful enabler for skill transfer between humans and robots. In particular, collaborative tasks provide great opportunities for applications of learning from demonstration. LfD includes mechanisms for enabling skill transfer between humans and robots, producing systems that learn from skill executions led by humans or other agents.
- For robots to achieve widespread adoption and incorporation into everyday tasks, it is critical that non-experts be capable of imparting knowledge to them through familiar means.
- One technique that particularly takes advantage of humans in the loop is the combination of socially guided machine learning and active learning
- Active learning is a method designed to accelerate time to skill acquisition. By enabling the learner to ask questions of its teachers, the learner can guide instructors to fill the most critical gaps in its knowledge with training data.
- Collaborating with humans introduces a preference for representations that are inherently comprehensible to people.
- They present to examples for collaborative tasks: assembling of a small animal shelter, which include division of responsibilities, fine motor control, object manipulation and potentially dangerous actions(cutting). The other is a cooking task making ice cream. This requires precise control of temperatures and consistencies, mixing, temporal constraints. many cooking tasks have steps inherently better suited to either human or robot.
- They go all of the four research questions

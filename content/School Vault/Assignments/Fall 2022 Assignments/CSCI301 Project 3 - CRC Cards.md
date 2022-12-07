tags: #notes #topic
creation date: [[2022-10-17 Monday]] 17:17:18
modification date: [[2022-10-17 Monday]] 17:17:18

## Project 3

Design: Perform a class design with CRC cards to clarify class relationships for yourself.
- Note: There are several possible design solutions! CEC cards are also good for reverse engineering and figuring out which class collaborates with which other class.
- Include
	- 2 possible driver algorithms (called Wall-follower and Wizard) and 
	- 2 possible DistanceSensor classes (called ReliableSensor and UnreliableSensor)
	in your CRC class design.
- Put your CRC class design in writing, simply list each class, its responsibilities and collaborators. Use this in the JavaDoc comments that go into the header part of each new class.
- Tag this version with your notes in the new Java classes as a release ReleaseCRC on Gitlab, it needs to include new files ReliableSensor, UnreliableSensor, ReliableRobot, WallFollower, and Wizard with comments about their responsibilities and collaborators.

Ok so 5 classes to make CRC design for
I will start there and make make more CRC cards for other classes in order to understand what I need to do

A class represents a collection of similar objects, a **responsibility** is something that a class knows or does, and a **collaborator** is another class that a class interacts with to fulfill its responsibilities.

> [!NOTE] ReliableRobot.java
> Responsibilities:
> 	- a
> Collaborators:
> 	- implements: Robot.java

> [!NOTE] Wizard.java
> implements: RobotDriver.java

> [!NOTE] WallFollower.java
> implements: RobotDriver.java

> [!NOTE] ReliableSensor.java
> implements: DistanceSensor.java

> [!NOTE] UnreliableSensor.java
> implements: DistanceSensor.java


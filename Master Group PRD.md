# Product Requirements Document (PRD)

[Problem Description](#_m14ebq69irye)

[Scope](#_h095bb6e23m6)

[Use Cases](#_a494vmyn4i0c)

[Purpose and Vision (Background)](#_a1rehjp14t6a)

[Stakeholders](#_ni1nsrov0hlq)

[Preliminary Context](#_8fsnkm7d5o2g)

[Assumptions](#_o6z1frxke2z)

[Constraints](#_q1it1bwhygi3)

[Dependencies](#_hn9mh6b6m132)

[Market Assessment and Competition Analysis](#_kztlc8doxc1v)

[Target Demographics (User Persona)](#_w2boxoybxhab)

[Requirements](#_agmoxh3nwlca)

[User Stories and Features (Functional Requirements)](#_26r2y8q9o6bs)

[Non-Functional Requirements](#_phuqv9aimzm2)

[Data Requirements](#_89injk5wussz)

[Integration Requirements](#_ti0b4uln9ysy)

[User Interaction and Design](#_jq7dpkh2hu4j)

[Milestones and Timeline](#_u3bp37hkrgxj)

[Goals and Success Metrics](#_ybblbzrnua5i)

[Open Questions](#_9p4b6jpz1kep)

[Out of Scope](#_c0bknaj5akzz)

##
# **Authors**

Team Apollo - Grant Kopczenski, Isaac Zheng, Jacob Irace, Michael Molineaux

##
# **Problem Description**

The "problem", as it stands, is that there is a game design competition next year, and we don't have an entry. That's not a particularly satisfying problem statement, so let's reframe our perspective.

When flying through space, space vehicles are at a high risk of colliding with objects such as space debris, comets, asteroids, satellites, and even other vehicles. This, among other problems, can create a high stress environment for pilots, which is difficult to convey accurately to people who have never been in such a situation before. This makes it much more difficult for the general public to understand the magnitude of stress pilots experience.

From a development perspective, it can be difficult to test the feasibility of flight assistance systems, specifically how they would impact a pilot's ability to fly.

## **Scope**

The scope for our simulation will be limited to flying around a relatively small designated "driving" area, including "space roads" comparable to how airplanes are directed in real life, as well as Automated Driver Assistance Systems. The goal will be for the user to make it from a start location to an end location without crashing into any other spacecraft or breaking any space traffic laws.

## **Use Cases**

The user should be able to perform basic navigation of the spaceship in a way that is realistic to actual spaceship navigation. The user will be able to see basic metrics for navigation, such as speed, direction, acceleration, etc.

The user should also be able to notice a learning curve in the navigation, and should encounter some difficulty when first starting the simulator.

##
# **Purpose and Vision (Background)**

Our purpose is to develop a simulator that can produce a mostly-realistic experience of navigating a spaceship. We aim to allow users a realistic experience of navigating in a way that is both fun and educational. Our final product should be suitable to be used for displays at showcases for NASA research that can demonstrate ADAS in space vehicles, and also as a general fun simulator to drive around in.

##
# **Stakeholders**

_List people that have an interest in the project:_

- _How often do they need to be updated?_
- _What type of updates do they require?_
- _Are they decision-makers?_
- _If yes, which decisions should go through them?_
- _What do they require to make an informed decision?_

_Decision-makers should request more information to be able to decide. Uninformed decision makers will make bad decisions for you and your team. Be wary of stakeholders that go with instinct, validate their claims and be ready to challenge them with data. Not everyone has the deep-instinct that comes with long industry experience._

- Seed Investors
- CEO/CTO/Founders
- Engineering Managers
- Product Managers
- Engineering Team
- Marketing Team
- Legal Team
- Sales
- Users

- Kirsten Winters, our highest-level oversight and "project partner"

- Mike Bailey, OSU's computer graphics expert who we will be working with throughout the project

- Aeliana Shen, our TA, who we will meet with weekly to discuss current progress

- Nathan De Stafeno, the Graphics/Games consultant for this course, who we will be meeting with two or three times per term

- Us, the development team- Isaac, Jacob, Michael, and Grant- who will want to produce a quality entry to the game design competition

##
# **Preliminary Context**

## **Assumptions**

- We have roughly until the end of spring term 2024 to finish our simulation
- We are able to use Unreal Engine to create the simulation, and Unreal Engine will be able to facilitate everything we want the simulation to be able to do
- We can use free assets online for the simulation's graphics
- We have access to at least one professional who can point us in the right direction
- We have access to at least one uninvolved party who can test the simulation from an outside perspective
- The simulation will be run primarily on a PC
- The ADAS features will not need to use sensory means that apply to real life(i.e. Collision detections)

## **Constraints**

- We are a small team, so we probably can't produce a simulation encompassing a great deal of space
- We need to optimize our simulation such that it can run on non-specialized computers
- We do not have access to professional graphic designers, so we will need to use free assets or, if necessary, hire someone
- Our budget is zero dollars, so if we do want to hire someone, that money will have to come from somewhere
- We have only until the competition deadline to finalize our simulation
- We must comply with the requirements for the simulation listed in the competition documents
- We may not use existing products as a boilerplate, such as NVidia Drive Sim
- The physics in the game should be at least theoretically possible in real life

## **Dependencies**

- We are dependent on Unreal Engine 5 to power our simulation
- We will almost certainly be dependent on object detection and virtual sensor libraries to power the AI ships
- We will need to develop the basic framework for the ships before developing the map and the actions that the AI takes
- We will potentially need to pull data about foreign bodies in space, such as planets, stars, comets, with information such as their size, trajectory, mass, etc.

##
# **Market Assessment and Competition Analysis**

The two main competitors for our simulation are games called _Kerbal Space Program_ and _Outer Wilds_. Kerbal Space Program is a relatively robust, if simplified, simulation of modern rocketry, and has been used in the past as a cheap, early-stage simulation for real space projects. Outer Wilds is a space-based adventure game, with an emphasis on space exploration and spaceflight. Our project aims to meet a middle ground between those two, by making a flight simulator that is realistic to near-future technology and is fun to fly around in.

##
# **Target Demographics (User Persona)**

- Fundraisers/Program Advocates
  - Use the program as demonstration for concepts of ADAS and spaceship navigation
  - 22+ years old
- Casual Gamers
  - Use the program for fun
  - 7+ years old
- Aerospace Engineers
  - Use the program to test concepts for ADAS systems
  - 25+ years old

##
# **Requirements**

Our requirements are laid out in the competition documentations, and are as follows:

_Create a playable simulation that uses Advanced Driver Assistance Systems (ADAS) features, A.I. traffic relevant to vehicle type and overall setting, and realistic visuals. (For example, a simulation's ADAS features might include body collision detection and avoidance via Automatic Emergency Braking (AEB), which can help improve a player's performance over the course of playing)._

_The A.I. traffic must feature physically accurate and realistic movement of the vehicles, such as with smooth braking (or similar, depending on your vehicle of choice), accelerating, and turning inputs. As well as 3D visuals that are realistic to help simulate real life driving._

_At the end of this competition, teams will have a demo game that displays the above features._

_The game must be playable, so that a player might practice and improve control of the vehicle. For example, this play-ability feature could include the ability to improve in speed and agility performance; that is, the ability to improve in time and over space._

## **User Stories and Features (Functional Requirements)**

| **User Story** | **Feature** | **Priority** | **GitHub Issue** | **Dependencies** |
| --- | --- | --- | --- | --- |
| As an Aerospace engineer, I want to be able to import and design custom ADAS features in the simulator. | Modularity | Should Have | TBD |
 |
| As a pilot, I want to fly through a realistically difficult environment that challenges me to develop my navigational skills. | Navigation | Must Have | TBD | N/A |
| As a pilot, I want the navigation to take into account factors such as gravity, momentum, and collisions. | Physics System | Must Have | TBD | N/A |
| As a casual gamer, I want the environment to be interactive and visually appealing.
 | Visual Fidelity | Could Have | TBD |
 |

## **Non-Functional Requirements**

- The simulation should run at at least 30 frames per second, preferably 60.
- The vehicle should respond to user input in less than 300 milliseconds.
- The simulation should look good and be relatively photorealistic.
- The simulation should be fun to play, at least for the first few times.
- The A.I. of the space traffic should make sense, and roughly resemble the player's behavior.
- The physics engine of our simulator should be realistic.

## **Data Requirements**

The program will need to save data such as location/orientation, control configurations, ADAS configurations, and potentially vehicle data such as fuel consumption, size, and shape.

## **Integration Requirements**

Integration with Steam controller input libraries, if we decide to add controller support.

## **User Interaction and Design**

The program will have three main user interfaces:

1. The Save Select Screen - This is where the user will choose from their saves.
2. The Settings Page - This is where the user will be able to customize their settings and import custom ADAS settings, as well as save their progress.
3. The Graphics Viewport - Where all navigation, observation, and spaceflight will take place. Includes the view out the "windshield", informational items such as a speedometer, etc.

##
# **Milestones and Timeline**

| **EST. Date** | **Feature** |
| --- | --- |
| November | Workflow and environment set up |
| December | Individual research and planning finished |
| December | Functional base game (rough physics engine, models and graphics, U.I. finished) |
| May | Polished simulation with fully functional A.I. traffic, space vehicle physics, user friendly U.I., high end graphics. |

##
# **Goals and Success Metrics**

| **Goal** | **Metric** | **Baseline** | **Target** | **Tracking Method** |
| --- | --- | --- | --- | --- |
| User Ratings | Users enjoyment of the game 1-10. | 5 | 8 | Surveying |
| Product-market fit | How would you feel if you could no longer use this product? | Very disappointed \< 40% | Very disappointed \> 40% | Interview |
| Simulation Playability | Number of bugs | 0 bugs | \< 5 bugs | In game testing / User testing |
| User engagement | Average session duration | ~10 minutes | 30+ minutes | Plausible Analytics |
| Realistic physics engine | Comparability to real life | \> 70% accuracy | \> 85% accuracy | In game testing / User testing |

##
# **Open Questions**

_By this point, you probably have a lot of unanswered questions. Track them here, and leave some space for answers. Address these questions as you progress in time, and incorporate new knowledge in the other sections._

What will this project look like when it's "complete"?

What criteria exactly are the judges of the competition judging based on?

When is the competition? When is the submission deadline for the competition?

How hard will this be to code?

How many types of vehicles should we consider?

##
# **Out of Scope**

Multiplayer, online or local.

Landing, either on planetary bodies or in a space station of some kind.

Exploring outside the bounds of the track (would require placing planetary bodies as actual objects, as opposed to just a skybox)

VR implementation
# Senna

![Senna](https://drive.google.com/thumbnail?id=1InB_cFF98jUtCHBEwiU5T0KlEZ4VdzLn&sz=w1000)

## 🗒️Table of Contents
- [About](#-about)
    - [Functionalities](#️-functionalities)
    - [Results](#-results)
    - [Personal Outcomes](#-personal-outcomes)
    - [Gallery](#️-gallery)
- [Contact](#️-contact)
 
## 🔍️ About

> Senna is a high-speed autonomous line-following robot designed for competitions held under [these rules](https://robocore-eventos.s3.sa-east-1.amazonaws.com/public/RoboCore_Seguidor_de_Linha_Regras_RSM.pdf). I developed this project between 2023 and 2025.

Line follower (or "Robotracer") competitions challenge participants to build the fastest robot capable of autonomously navigating a predefined track. To be competitive, a robot must be highly robust and adaptive, reacting in real-time to dynamic track conditions. This pursuit of speed drives the development of advanced algorithms for performance optimization, including dynamic acceleration, intelligent path planning, and precise shortcut execution. Consequently, achieving top-tier performance often requires custom-designed electronics tailored to a specific control strategy.

![Line Follower Track](https://drive.google.com/thumbnail?id=1MVrIEEDyGBtWrrQ5uzuDhpggOtMH5DNJ&sz=w1000)

Line Chaser competitions are designed to determine which robot achieves the highest raw speed by having multiple robots race simultaneously on the same continuous track—similar to a "tag" or "chase" game. Unlike traditional line follower events, these competitions emphasize direct head-to-head performance, pushing both hardware and software to their absolute limits in a dynamic, competitive environment.

![Line Chaser Track](https://drive.google.com/thumbnail?id=1fivYINAUqBAVwBhmc9mDx1_7ys_pw88B&sz=w1000)

### 🚀 Project Description

The robot measures approximately 12cm x 15cm and weighs around 220g. To achieve a low weight profile, the Printed Circuit Boards (PCBs) serve as the main structural components of the chassis, a design choice known as "PCB-as-chassis." Additional mechanical parts, like motor mounts and sensor brackets, are 3D-printed. A key feature of Senna is its active downforce system. It is equipped with four drone motors and propellers, mounted in reverse. When active, these motors generate powerful upward thrust, which pushes the robot firmly onto the track. This downforce significantly increases tire grip, enabling the robot to navigate corners at much higher speeds and ultimately reduce lap times.

#### Hardware Description

The robot's hardware follows a "PCB-as-chassis" design strategy and consists of several custom-designed printed circuit boards (PCBs):

- Main Board: This is the core of the robot, housing the central processing and control components.

    - Microcontroller Unit (MCU): The central processor that executes the control logic and algorithms. It features embedded Bluetooth LE for wireless data telemetry and remote configuration.

    - Drive System: Consists of DC motors and high-current motor drivers that control them, providing power to move the robot along the track.

    - Brushless System: The downforce system.

    - Feedback Systems: RGB LEDs and a buzzer provide real-time operational feedback to the user.

    - Battery Monitoring System: Actively measures battery voltage to ensure safe operation and prevent damage.

- Line Sensor PCB: An array of sensors for detecting the track line and transmitting this information to the MCU.

- Lateral Sensors: These sensors are used to identify course markers, such as start/finish lines or curves.

- Wheel Encoders: Provide high-resolution feedback on wheel rotation, enabling precise speed control and distance tracking (odometry).


#### Firmware Description

The robot's firmware is designed around a state machine, which governs the operational flow.

- Configuration State: Upon startup, the robot enters this state, allowing users to wirelessly set parameters (e.g., racing category, maximum speed) via a Bluetooth LE interface on a smartphone.

- Calibration State: In this state, the robot captures the minimum and maximum possible line readings to normalize sensor data. This ensures all sensors return values on a consistent scale, compensating for manufacturing variances and improving reading accuracy.

- Race State: The robot operates autonomously in this state. It continuously performs the following sequence:

    - Sensor Reading: Reads data from the line sensors.

    - Position Estimation: Estimates the robot's current position relative to the line.

    - Control Loop: Compares the current position to the desired position (the center of the line), calculates the error, and feeds it into a PID control algorithm. This algorithm generates motor outputs to correct the robot's heading.

    - Sector-Specific Actions: Identifies specific sectors on the track to accelerate, optimizing lap times.

    - Termination: Stops autonomously upon detecting the finish line.

Throughout its operation, the robot provides real-time feedback to the user via the Bluetooth LE interface, in addition to using RGB LEDs and a buzzer for visual and auditory status updates.

### ✨ Results

Senna has a strong track record in the Latin American robotics scene, having secured seven trophies in line follower and line chaser categories to date.

- RSM Challenge International 2025
    - 1st Place | Line Chaser  (out of 22 robots)
    - 2nd Place | Line Follower (out of 60 robots)
- Robocore Experience (RCX) 2024
    - 1st Place | Line Chaser (out of 19 robots)
    - 2nd Place | Line Follower (out of 78 robots)
- RSM Challenge International 2024
    - 1st Place | Line Chaser (out of 16 robots)
    - 2nd Place | Line Follower (out of 35 robots)
- RoboChallenge Brazil 2024
    - 2nd Place | Line Follower (out of 23 robots)

![Results](https://drive.google.com/thumbnail?id=1Vsxj1wo7xdSCsXazQK-bIF-c-h3dmqHp&sz=w1000)

### 📝 Personal Outcomes

Leading the Senna project as the team coordinator for my university's robotics team, Phoenix, was a transformative experience. We made a conscious effort to design and build as many parts as possible in-house, which presented a unique set of challenges.

Technically, I significantly enhanced my skills in PCB design, mastering everything from schematic analysis to ensuring signal integrity. My proficiency in embedded systems programming also grew immensely as I developed and optimized the robot's various systems and learned to integrate them efficiently.

My learning extended beyond technical development. I gained practical experience in project management by handling logistics such as communicating with manufacturers, sourcing specialized components, managing inventory, and establishing potential partnerships with international companies. This project challenged me to think holistically about a complex build, and its successful completion was a testament to the hard work of the entire team. I am incredibly grateful for the contributions of my peers.

### 🖼️ Gallery

Here are some videos of Senna:

[Senna | RSM Challenge 2025](https://youtu.be/6gOFQNeKEkI)

[Senna | RSM Challenge 2025 Chaser](https://youtube.com/shorts/MpbdJeK2hgk?feature=share)

[Senna | RoboChallenge](https://youtube.com/shorts/gfrDhgjhIZA?feature=share)

## 💬 Contact
[
    <img
        src="https://images.weserv.nl/?url=https://avatars.githubusercontent.com/u/145018309?v=4&fit=cover&mask=circle&maxage=7d" 
        width=15%
        title="GitHub Profile"
        alt="vdrad"
    />
](https://github.com/vdrad)

For questions, suggestions, collaboration opportunities, or any other topic, please feel free to reach out:

- GitHub:   [vdrad](https://github.com/vdrad)
- Email:    victor.drad.g@gmail.com
- LinkedIn: [Victor Gomes](https://www.linkedin.com/in/victor-g-582b5911b/)
- [Phoenix's Instagram](https://instagram.com/phoenixunicamp)


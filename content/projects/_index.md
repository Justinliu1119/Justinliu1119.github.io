---
title: Projects

projects:  
- pjTitle: "Automated Grocery Management: A Perspective On Sustainability"
  link: "projects/fridge-hub"
  subtitle: "Advisor: Prof. A. Weber"
  img1: "/img/projects/p11.png"
  img2: "/img/projects/p12.png"
  desc: | 
    I coordinated a team of three to design and implement an innovative embedded fridge management system. This project featured both local and remote iOS app UIs, enabling users to record details such as expiration dates and storage locations, and manage their fridge contents from either interface.

    **Hardware**: Established communication protocols (SPI, UART, I2C, and parallel) between devices such as a temperature sensor, keypad, and barcode scanner, all integrated with an Atmega328p microcontroller.

    **Software**: Developed an application for real-time synchronization of grocery items via an information query mechanism implemented in a JSON-like format using Firebase. This included: 1)Entering and transmitting item information on either UI through a Raspberry Pi. 2)Monitoring the fridge's internal temperature. 3)Sending notifications for high temperatures and items nearing expiration.    
  
- pjTitle: "Embeded Systems Speed Trap"
  link: "projects/speed-trap"
  subtitle: ""
  img1: "/img/projects/p21.png"
  desc: |
    - Measured and Displayed Speed: Calculated object speed (cm/sec) using LED light sources and phototransistors, displaying results on an LCD and dial-type speedometer.
    - User Interaction and Alerts: Allowed speed threshold setting via a knob, indicated measurement progress with an LED, and triggered an alarm tone with a buzzer for threshold breaches.
    - Communication and Comparison: Enabled RS-232 serial communication to display and compare local and remote speed measurements, with comparison indicated by two LEDs.    
  
 
- pjTitle: "Electric Guitar via Band-Pass Filter"
  link: "projects/electric-guitar"
  subtitle: ""
  img1: "/img/projects/p31.png"
  desc: |
    - Created a band pass filter targeting the guitar G chord (~196Hz), converting the magnetic field from plucked strings into signals, which are then filtered and amplified through an RC circuit and a noninverting amplifier.
    - Implemented a noninverting amplifier with a 10kΩ feedback resistor to amplify the pickup signal by a factor of 11.
    - Successfully converted signals into magnetic fields, producing amplified acoustic sound via a speaker, with the band pass filter efficiently selecting and outputting signals within the target frequency range.    
  
- pjTitle: "Model-Based Advancement in Submersible Navigation--TDOA and Kalman Filtering Techniques"
  link: "projects/tdoa-and-kalman-filtering-models-in-submarine"
  subtitle: ""
  img1: "/img/projects/p41.png"
  desc: |
    -  Led a team of three to design, implement and simulate Time Difference of Arrival and Kalman Filtering Algorithms to compute the precise location of the submarine and predict its future projectile in scenarios involving loss of communication.
    - Simulated Kalman Filter transitioning states based on the previous step of trilateral localization.
    - Modeled the maximum likelihood estimator for search and rescue of the submersible conditioned on the predicted trajectory.


---

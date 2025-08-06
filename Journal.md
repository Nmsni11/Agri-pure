---
title: "Agri-pure"
author: "Abdelsalam Aref Mahmoud Abdellah"
description: "A multi-stage smart water purification system for agricultural runoff in rural Egypt using biosand, graphene oxide, and Arduino automation."
created_at: "2/7/2025"
---

# Total Time Spent: 52 hours

---

## Day 1 – 2/7  
**Time Spent:** 3 hours  
I began by conducting background research into water pollution issues in Beheira’s rural regions. I chose El-Bostan village as the target deployment location due to the high levels of agricultural runoff and lack of water treatment systems. Through local and global studies, I identified the most common pollutants: heavy metals, pesticide residues, and general turbidity. I drafted an early-stage system architecture and an initial concept diagram for a modular purification tank that could fit in rural environments.

---

## Day 2 – 3/7  
**Time Spent:** 4 hours  
Today I delved into biosand filtration principles and reviewed academic papers on multi-stage systems. I selected silica sand, zeolite, and gravel as the foundational filtration media. I also explored advanced chemical additives and selected graphene oxide for metal ion removal, and wood ash for pH balancing. As I calculated the chemical reaction potential of the wood ash, I referred to the **hydration reaction of calcium oxide**, which forms part of the alkalinity equation:
![The hydration of calcium oxide reaction](photos/image-5.png)

I prepared several test samples of clean wood ash and ordered graphene oxide. I simultaneously began early CAD modeling of the filtration system to visualize media layering and flow channels.

---

## Day 3 – 4/7  
**Time Spent:** 6 hours  
I made significant progress on the CAD design. I created modular cartridge sections within the model, enabling the separation and easy replacement of individual filtration stages. Each module had separate inlets and outlets, allowing staged treatment of the water. The model now showed clear space for sensors and control modules to be added later.

![3D Model](photos/im1.jpg)

---

## Day 4 – 5/7  
**Time Spent:** 5 hours  
Today was the beginning of the automation side. I connected the TDS sensor, pH sensor, and relay-controlled pump in simulation software to create the first logic cycle. The Arduino logic now reads values continuously and sends water for a second treatment cycle if any values are out of range. For better measurement accuracy, I implemented the **TDS calculation equation**, which allowed me to convert analog readings into ppm with temperature correction:

![TDS calculation equation](photos/image-4.png)

I also adjusted the 3D model design to accommodate sensor holders and cable routing.

![showing the PH sensor in the diagram](photos/2.jpg)

---

## Day 5 – 6/7  
**Time Spent:** 5 hours  
I focused on testing the servo-controlled flow gates which regulate water between the cartridges. These gates had to open and close smoothly to avoid overpressure. Using the pH and TDS sensors, I took readings after each purification stage to monitor treatment efficiency. A key design improvement today was refining the filter housing geometry based on those sensor placements.

![showing the PH sensor in the diagram](photos/3.jpg)

---

## Day 6 – 7/7  
**Time Spent:** 6 hours  
I worked on user interfacing today by integrating an OLED screen into the model, displaying live readings of water quality. The Arduino code was optimized for low-voltage scenarios, especially since the system might run off battery and solar input. During this process, I calculated voltage and current tolerances for each module to prevent brownouts.

---

## Day 7 – 8/7  
**Time Spent:** 8 hours  
This day marked the enclosure's completion. I finalized all waterproof seals and designed the solar interface for battery charging. I selected a sealed Li-ion battery compartment and tested power routing to the Arduino. With this, the system became completely standalone. I also finished major routing in the CAD model and exported STL versions of the final design.

![3D Model](photos/im2.jpg)

---

## Day 8 – 9/7  
**Time Spent:** 7 hours  
I created a clean, labeled wiring diagram today showing connections from sensors to control modules and power input. Each connection was tested virtually for pin logic and signal strength. The final BoM was completed with pricing and sourcing links. The diagram shows the key placements of the pH sensor and pump relays.

![wiring diagram](photos/1.jpg)  
![showing them both](photos/4.jpg)

---

## Day 9 – 10/7  
**Time Spent:** 8 hours  
The final day of the project was all about packaging and validation. I wrote the full README with instructions, set up the GitHub repository, and uploaded all source files, including CAD models, Arduino code, and library dependencies. I tested water samples from the El-Bostan area and plotted sensor data across multiple treatment cycles. To understand electrochemical sensor readings at different concentrations and pH levels, I used the **Nernst equation** for reference:

![Nernst equation](photos/image-3.png)

The results showed improved water quality across the board:

![The measured values of each type of pollution every trial](photos/image.png)  
![The measured values of each type of pollution](photos/image-1.png)  
![PH value after trials](photos/image-2.png)


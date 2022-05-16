# 10 Bit Potentiometric DAC using 28nm Technology (Synopsys Custom Compiler)

This project aims to deal with a 10 Bit Potentiometric DAC (Digital to Analog Converter) using Synopsys Custom Compiler Tool with a typical Digital Power Supply (VDD) of 1.05V and a typical Analog Voltage Supply (VDDA) of 1.8V using SAED_PDK 28_32nm Technology node.


# Table of Contents
- [ Introduction](#introduction)
- [ Pre Layout Simulations](#pre-layout-simulations)
  * [Tools used](#tools-used)
  * [Switch](#Switch)
  * [2 bit DAC](#2-bit-dac)
  * [3 bit DAC](#3-bit-dac)
  * [4 bit DAC](#4-bit-dac)
  * [5 bit DAC](#5-bit-dac)
  * [6 bit DAC](#6-bit-dac)
  * [7 bit DAC](#7-bit-dac)
  * [8 bit DAC](#8-bit-dac)
  * [9 bit DAC](#9-bit-dac)
  * [10 bit DAC](#10-bit-dac)
- [ Results](#results)
- [ Layout ](#layout)
  * [switch](#switch)
  * [2bit DAC](#2bit-dac)
  * [3bit DAC](#3bit-dac)
  * [4bit DAC](#4bit-dac)
  * [5bit DAC](#5bit-dac)
  * [6bit DAC](#6bit-dac)
  * [7bit DAC](#7bit-dac)
  * [8bit DAC](#8bit-dac)
  * [9bit DAC](#9bit-dac)
  * [10bit DAC](#10bit-dac)
- [ Future Works](#future-works)
- [ Contributors](#contributors)
- [ Acknowledgements](#acknowledgements)
- [ References](#references)


# Introduction

* A Digital to Analog Converter (DAC) converts a digital input signal into an analog output signal. The digital signal is represented with a binary code, which is a combination of bits 0 and 1. A Digital to Analog Converter (DAC) consists of a number of binary inputs and a single output. In general, the number of binary inputs of a DAC will be a power of two.

* There are two types of DACs :

  1. Weighted Resistor DAC
  2. R-2R Ladder DAC

### Weighted Resistor DAC

* A weighted resistor DAC produces an analog output, which is almost equal to the digital (binary) input by using binary weighted resistors in the inverting adder circuit. In short, a binary weighted resistor DAC is called as weighted resistor DAC.
* The circuit diagram of a 3-bit binary weighted resistor DAC is shown in the following figure :

![weighted resistor](https://user-images.githubusercontent.com/83152452/166871259-dc9be251-84f7-4ac6-a7bb-7aed601f6f59.png)

### R-2R Ladder DAC

* The R-2R Ladder DAC overcomes the disadvantages of a binary weighted resistor DAC. As the name suggests, R-2R Ladder DAC produces an analog output, which is almost equal to the digital (binary) input by using a R-2R ladder network in the inverting adder circuit.
* The circuit diagramof a 3-bit R-2R Ladder DAC is shown in the following figure :

![r2r ladder](https://user-images.githubusercontent.com/83152452/166871272-ec5a78ad-90d0-40e3-b2f7-2d93ae7eedcf.png)

* For more information you may wish to visit : [Link](https://www.tutorialspoint.com/linear_integrated_circuits_applications/linear_integrated_circuits_applications_digital_to_analog_converters.htm)
 
### Architecture 

* The basic idea is to divide the voltage into N different voltage values in the range of VREFH and VREFL- for an N-Bit DAC. 
* The design used here to achieve this is the simple resistor string DAC which consists of resistors in series. 
* These resistors are then connected to various switches in such a fashion that it routes the exact voltage to the output. 
* The problem of the largeness of the circuit is reduced by building hierarchical subcircuits of 10-Bit potentiometric DAC – Switch, 2-bit, 3-bit, 4-bit, 5-bit, 6-bit, 7-bit, 8-bit, 9-bit and 10-bit.

![basic architecture of potentiometric DAC](https://user-images.githubusercontent.com/83152452/164958658-74c7f37c-4cb0-4f9d-bb1d-ddbb5f2dc570.png)

### Specifications to be met

![specifications to be met](https://user-images.githubusercontent.com/83152452/164958719-436bb2f8-8a75-48d5-95a1-db4efa5e6290.png)

# Pre Layout Simulations

## Tools used

* The tools used for the circuit simulations are:

 1. Schematic Design : Custom Compiler
 2. Symbol Creation : Custom Compiler
 3. Simulation : PrimeSim

## Switch

* Switching circuits or gates are circuits that perform well-defined logic or arithmetic operations on binary variables. 
* Binary variables are two-valued variables expressed as 1's or 0's in algebraic form, or true or false in syllogistic forms, or as high or low voltage, positive or negative remanence (magnetic flux), etc., in circuit forms. 
* Circuit switching refers to the mechanism of communications in which a dedicated path with allocated bandwidth is set up on an on-demand basis before the actual communication can take place. 

### Switch Schematic 
![switch sch](https://user-images.githubusercontent.com/83152452/164958812-197936ea-7c4a-4749-bf65-2b8ce7baf172.png)

### Switch Symbol 
![switch symbol](https://user-images.githubusercontent.com/83152452/164958815-817b6c2b-e1f2-4f3d-b489-0f2076c2226c.png)

### Switch testbench
![switch tb](https://user-images.githubusercontent.com/83152452/164958818-a53c137a-00de-4faa-9164-fc763ec85376.png)

### Switch Waveform 
![switch wf](https://user-images.githubusercontent.com/83152452/164958822-aeb60216-30bc-41ff-8d65-26dd8eb9c250.png)


## 2 Bit DAC

### Schematic
![2bit sch](https://user-images.githubusercontent.com/83152452/164958876-dc60109a-c2f0-4633-a179-ae2de6ba1d0e.png)

### Symbol
![2bit symbol](https://user-images.githubusercontent.com/83152452/164958877-b5d4e6b5-9ebc-40b9-aab8-28d4db187320.png)

### Testbench
![2bit tb](https://user-images.githubusercontent.com/83152452/164958878-680e53e9-6868-4e31-958a-492e9e1ff311.png)

### Waveform
![2bit wf](https://user-images.githubusercontent.com/83152452/164958879-8567e428-ece3-43ba-be28-b9213941611a.png)


## 3 Bit DAC

### Schematic
![3bit sch](https://user-images.githubusercontent.com/83152452/164958918-58aba452-14dd-42b1-8496-9bf2f6ce1ba3.png)

### Symbol
![3bit symbol](https://user-images.githubusercontent.com/83152452/164958920-0ee00a91-1a02-48e2-841e-37031044f663.png)

### Testbench
![3bit tb](https://user-images.githubusercontent.com/83152452/164958921-3154a4db-b123-4741-bee6-b2812f57a738.png)

### Waveform
![3bit wf](https://user-images.githubusercontent.com/83152452/164958922-d188c5d3-93db-4a57-91bc-a8643bbc8e0a.png)


## 4 Bit DAC

### Schematic
![4bit sch](https://user-images.githubusercontent.com/83152452/164958955-0b1a45aa-515e-4f92-b263-79550978ff78.png)

### Symbol
![4bit symbol](https://user-images.githubusercontent.com/83152452/164958957-413c0913-8dca-45a4-8994-f187ceb722c8.png)

### Testbench
![4bit tb](https://user-images.githubusercontent.com/83152452/164958958-ab9cf886-6c0e-45d4-938b-76c645c43d41.png)

### Waveform
![4bit wf](https://user-images.githubusercontent.com/83152452/164958960-c8c7dfaa-99bf-4c5a-b967-68c97f45e17e.png)


## 5 Bit DAC

### Schematic
![5bit sch](https://user-images.githubusercontent.com/83152452/164959022-9356dff2-821c-45b5-9230-e3ab9fac0376.png)

### Symbol
![5bit symbol](https://user-images.githubusercontent.com/83152452/164959023-559238e8-ebe2-4fa4-8125-ed3bccc5fba7.png)

### Testbench
![5bit tb](https://user-images.githubusercontent.com/83152452/164959026-4f85da9b-94d9-47e3-9a3c-ea9b2b4aa6d1.png)

### Waveform
![5bit wf](https://user-images.githubusercontent.com/83152452/164959028-1afa5372-a862-49e5-be2e-7adba89e01b5.png)


## 6 Bit DAC

### Schematic
![6bit sch](https://user-images.githubusercontent.com/83152452/164959064-d4580bc2-9411-496a-b843-2254be84e1e2.png)

### Symbol
![6bit symbol](https://user-images.githubusercontent.com/83152452/164959066-97267246-dda4-464f-9a1f-4a4d0f18c70c.png)

### Testbench
![6bit tb](https://user-images.githubusercontent.com/83152452/164959069-0cc29272-d528-48e3-9489-1024da1dcdfb.png)

### Waveform
![6bit wf](https://user-images.githubusercontent.com/83152452/164959072-aab964a7-eeaa-4454-8be5-2d31fd7daca1.png)


## 7 Bit DAC

### Schematic
![7bit sch](https://user-images.githubusercontent.com/83152452/164959098-4f9f5365-8fa1-4153-bc72-7b6d907cca6f.png)

### Symbol
![7bit symbol](https://user-images.githubusercontent.com/83152452/164959099-67147136-dfc7-44bf-b17b-2a8361570ebb.png)

### Testbench
![7bit tb](https://user-images.githubusercontent.com/83152452/164959102-934fc011-7969-42aa-9241-57eed7da49f2.png)

### Waveform
![7bit wf](https://user-images.githubusercontent.com/83152452/164959105-21c700bf-f9a4-406e-a8f9-2626dd91197d.png)


## 8 Bit DAC

### Schematic
![8bit sch](https://user-images.githubusercontent.com/83152452/164959131-8ef98175-ad1e-4b0c-9716-c590ca373d66.png)

### Symbol
![8bit symbol](https://user-images.githubusercontent.com/83152452/164959132-bdbc2e1e-f6f9-4225-b6a8-da34afcaa6cf.png)

### Testbench
![8bit tb](https://user-images.githubusercontent.com/83152452/164959133-117dac24-70c2-4365-bf16-356364e8b082.png)

### Waveform
![8bit wf](https://user-images.githubusercontent.com/83152452/164959134-a38a43c8-797c-4dbe-982b-6f47f269b82d.png)


## 9 Bit DAC

### Schematic
![9bit sch](https://user-images.githubusercontent.com/83152452/164959170-2efcfacf-684a-4344-b7f1-1f1bd5e11702.png)

### Symbol
![9bit symbol](https://user-images.githubusercontent.com/83152452/164959171-658b1c93-8d62-4002-88d8-3b8fddbfd137.png)

### Testbench
![9bit tb](https://user-images.githubusercontent.com/83152452/164959172-8484e006-e86e-4659-b5da-713620d432be.png)

### Waveform
![9bit wf](https://user-images.githubusercontent.com/83152452/164959176-8f445fef-2eaf-4a24-8bff-6e5e441ba3cb.png)


## 10 Bit DAC

### Schematic
![10bit sch](https://user-images.githubusercontent.com/83152452/164959220-26758a3c-3972-4a3c-bfcd-afccaa4ea74f.png)

### Symbol
![10bit symbol](https://user-images.githubusercontent.com/83152452/164959221-2dc2f366-ecda-47b8-986b-3a0787ff8be8.png)

### Testbench
![10bit tb](https://user-images.githubusercontent.com/83152452/164959223-0c335f9f-8879-45ce-b49b-8a878de49655.png)

### Waveform
![10bit wf](https://user-images.githubusercontent.com/83152452/164959225-a438d2e8-6645-43e2-8e47-bce8b88b72db.png)


# Results

### Switch Components and it's value :

|Name	   |Value |
|:---------|:-------------------|
|D_in	     |v1 = 0V, v2 = 1.05V, u = 0.1us 	|
|Capacitor	|1pf	    |
|VDDA      |1.8V	    |
|VSSA     	|0V	|
|VREFH	    |1.2V	|
|VREFL	    |0.8V	|

### 2 Bit DAC :

|Name	   |Value |
|:---------|:-------------------|
|D0, D1    |v1 = 0V, v2 = 1.05V, u = 0.1us 	|
|Resistor  |200ohms   |
|Capacitor	|5pf	    |
|VDDA      |1.8V	    |
|VSSA     	|0V	|
|VREFH	    |1.8V	|
|VREFL	    |0V	|

NOTE : 
* For 3 Bit DAC : D0, D1 and D2; For 4 Bit DAC : D0, D1, D2 and D3 and so on.
* For 10 Bit DAC : D0, D1, D2...., D10.
* Other Inputs value remains the same as 2 Bit DAC until 10 Bit DAC.
* For 2 Bit DAC, Number of steps in the output graph = 2^N, i.e, 2^2 = 4 steps.... and so on. 
* For a 10 Bit DAC, Number of steps in the output graph = 2^N, i.e, 2^10 = 1024 steps.
* The graph value for DAC ranges from VrefH (1.8V) to VrefL (0V).


# Layout

## Switch 

![switch-1](https://user-images.githubusercontent.com/83152452/168643134-180c6961-541a-4f3e-b2bd-4068b3c19b6d.png)

![switch-2](https://user-images.githubusercontent.com/83152452/168643151-7813c3f6-1419-4af7-a794-67e7d4c0aa18.png)


## 2 Bit DAC

![2bit-1](https://user-images.githubusercontent.com/83152452/168643177-36b09e21-8d3f-463a-8f46-8e6c52c0be9c.png)

![2bit-2](https://user-images.githubusercontent.com/83152452/168643200-62ce5d23-f7c9-4e51-bd43-bf86751c4dba.png)


## 3 Bit DAC

![3bit-1](https://user-images.githubusercontent.com/83152452/168643219-641c010b-4aad-47d1-8c2b-0d6660baad2e.png)

![3bit-2](https://user-images.githubusercontent.com/83152452/168643236-32478791-59c8-495c-9554-fdd15ea92487.png)


## 4 Bit DAC

![4bit-1](https://user-images.githubusercontent.com/83152452/168643275-a8e08442-3178-40cf-b2c2-0c8cf09295ef.png)

![4bit-2](https://user-images.githubusercontent.com/83152452/168643286-6cf75913-1c61-4855-bcda-c4f5347612a3.png)


## 5 Bit DAC

![5bit-1](https://user-images.githubusercontent.com/83152452/168643343-a74a1ccc-bd9e-4123-bf41-3e1628dd71da.png)

![5bit-2](https://user-images.githubusercontent.com/83152452/168643361-7c67c1b4-1bd3-4a0b-b41d-a54480ae64b4.png)


## 6 Bit DAC

![6bit-1](https://user-images.githubusercontent.com/83152452/168643414-51c90ba4-d42f-409f-a2aa-5b1bdecda3d5.png)

![6bit-2](https://user-images.githubusercontent.com/83152452/168643409-1a6b4222-8257-45f0-b895-c48caaa21cbd.png)


## 7 Bit DAC

![7bit-1](https://user-images.githubusercontent.com/83152452/168643494-de06bff9-bb0e-43d1-866e-b1505a0bebe1.png)

![7bit-2](https://user-images.githubusercontent.com/83152452/168643510-4e66bcda-bbb0-466a-821c-865d266e087e.png)


## 8 Bit DAC

![8bit-1](https://user-images.githubusercontent.com/83152452/168643525-8dd122dd-ee14-4272-b19d-796564bf8caa.png)

![8bit-2](https://user-images.githubusercontent.com/83152452/168643555-8c4dadc2-1042-4908-b95e-05472af2b315.png)


## 9 Bit DAC

![9bit-1](https://user-images.githubusercontent.com/83152452/168643584-168f91a1-2b4d-4a83-b80c-630c7490d1b1.png)

![9bit-2](https://user-images.githubusercontent.com/83152452/168643602-a5eb1fac-02c0-46d9-847d-ce4947dadf7d.png)


## 10 Bit DAC

![10bit-1](https://user-images.githubusercontent.com/83152452/168643617-8648f6c6-6bd8-434d-8ed5-6861b2dead26.png)

![10bit-2](https://user-images.githubusercontent.com/83152452/168643628-03a35b81-07c2-4f72-b31b-1823502a8bcc.png)


# Future Works

* Need to understand and start with the Layout process.


# Contributors

* A Devipriya , B.E (Electronics and Communication Engineering), Bangalore - adevipriya1900@gmail.com


# Acknowledgements

* Kunal Ghosh, Co-Founder of VLSI System Design (VSD) Corp. Pvt. Ltd. - kunalghosh@gmail.com
* Muthukrishnan Chinnasamy and Montu Makadia, Semiconductor Fabless Accelerator Lab (SFAL)


# References

* Sameer S Durgoji : [Link](https://github.com/vsdip/avsddac_3v3_sky130_v2)
* Shalini Kanna : [Link](https://github.com/vsdip/avsddac_3v3_sky130_v1)
* S Skandha Deepsita : [Link](https://github.com/vsdip/avsddac_3v3_sky130_v1)


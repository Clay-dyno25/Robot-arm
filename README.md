# Project Ulysses

<p align="center">
  <img width="428" alt="Project Ulysses robotic arm, front view" src="https://github.com/user-attachments/assets/e56efe03-912d-4196-8699-5de42bc7073a" />
  <img width="363" alt="Project Ulysses robotic arm, side view" src="https://github.com/user-attachments/assets/b705650a-d187-4e79-905e-170f99d3c0a9" />
</p>

Project Ulysses is a low-cost robotic arm designed to demonstrate the principles of automation and robotics. Its primary function is to perform a repetitive pick-and-place task, moving objects between predetermined locations using servo motors and programmed movements.

The goal of this project is to explore how robotics can be used to automate simple, repetitive tasks, reducing the need for manual operation. It also investigates the reliability and practicality of using an affordable robotic system for basic automation.

Beyond building a functional robotic arm, this project is a hands-on exploration of mechanical design, electronics, programming, and the role of automation in modern engineering.

## Why I made this

I made Ulysses as a passion project for my university applications. The upcoming science fair was the perfect chance to present it, and I challenged myself to finish it in two weeks. That, to me, represents my future in engineering: making cool things that help people, on tight deadlines.

## Pictures

### 3D model

<p align="center">
 <img width="373" height="674" alt="image" src="https://github.com/user-attachments/assets/52428027-f535-46ae-aef7-a5a1ebc47a31" />
</p>

*Figure 1: Full 3D model of Ulysses (Onshape).*

### parts view
<p align="center">
  <img width="499" height="548" alt="image" src="https://github.com/user-attachments/assets/951eb43b-581d-46f2-b19c-4f76225c7d24" />
  <img width="383" height="383" alt="image" src="https://github.com/user-attachments/assets/34c22d30-58f5-4f52-bd0b-586078650c9a" />
  <img width="401" height="409" alt="image" src="https://github.com/user-attachments/assets/42883ca4-4c27-4133-9c60-7cb50b07e4e6" />
  <img width="520" height="563" alt="image" src="https://github.com/user-attachments/assets/a1cb8692-34a1-40b6-a84a-701cd8d57b5f" />
</p>

<p align="center">
  <img width="223" height="228" alt="image" src="https://github.com/user-attachments/assets/3d5eb582-6026-415d-9a47-8757d83d1f04" />
  <img width="187" height="219" alt="image" src="https://github.com/user-attachments/assets/b005cca6-c77a-4439-b84f-6d7cd3b2221c" />
  <img width="255" height="291" alt="image" src="https://github.com/user-attachments/assets/6968a27b-9c31-4676-9bc1-d38b4f165ce0" />
</p>

<p align="cemter">
  <img width="258" height="339" alt="image" src="https://github.com/user-attachments/assets/b5ff0231-75a4-4d3b-beee-783d6c2e8b72" />
  <img width="306" height="333" alt="image" src="https://github.com/user-attachments/assets/9351a103-eb6d-492e-93ab-7a5ac41c31b0" />
  <img width="120" height="156" alt="image" src="https://github.com/user-attachments/assets/8225ce60-d4c8-4623-b08a-f6c60c63e045" />
  <img width="214" height="189" alt="image" src="https://github.com/user-attachments/assets/2b419130-0794-48eb-8cef-1ca377670c3f" />
  <img width="409" height="626" alt="image" src="https://github.com/user-attachments/assets/46ee8e5b-c87f-4199-ac15-516a69350272" />
</p>

<p align="center">
  <img width="199" height="507" alt="image" src="https://github.com/user-attachments/assets/45292477-5216-41f5-9988-2dbd8af7438d" />
</p> 

<p align="center">
  <img width="187" height="485" alt="image" src="https://github.com/user-attachments/assets/0c827f58-39eb-4461-a7dc-438d94955277" />
  <img width="175" height="328" alt="image" src="https://github.com/user-attachments/assets/fe330f93-5e7a-4cde-a047-c898595d8f49" />
  <img width="185" height="438" alt="image" src="https://github.com/user-attachments/assets/c08f7822-8ddf-4d3d-ac64-5a759f87e12a" />
  <img width="478" height="541" alt="image" src="https://github.com/user-attachments/assets/169e6ae6-803d-4aa7-8f17-d9f97c0afd96" />
</p> 



*Figure 2: Ulysses broken down into its parts: base (gear plate, rotating plate), servo cases, lower arm, upper arm and wrist.*

> **TODO:** Add arrows or numbered labels to Figures 1 and 2 matching the part names used in the assembly steps below (gear plate, rotating plate, servo case, lower arm, upper arm, wrist).

### PCB and schematic

Not applicable. Ulysses has no custom PCB; the servos are wired directly to the controller (see below).

## Wiring diagram

<p align="center">
  <img width="1080" alt="Full 3D model of Ulysses" src="https://github.com/user-attachments/assets/e3438f86-2c75-401c-8062-d816803dcf76" />
</p>

<p align="center">
  <img width="932" alt="Ulysses parts layout" src="https://github.com/user-attachments/assets/b91d1275-8e76-437f-aa21-ada1962af0ea" />
</p>

| Servo | Joint | Signal pin | Power |
|-------|-------|-----------|-------|
| MG90S #1 | Base rotation | D9 | 5V / GND |
| MG90S #2 | Shoulder / lower arm | D10 | 5V / GND |
| SG90 #1| Wrist | D11 | 5V / GND |
| SG90 #2| Wrist | D12 | 5V / GND |
| SG90 3#| Wrist | D13 | 5V / GND |

> **Tip:** Power the servos from a separate 5V supply (shared ground with the controller) rather than the board's 5V pin, since servos can draw enough current to reset a microcontroller.

## How to assemble

### You will need

- Standard 2mm screws (they come with any micro servo) x8
- 5mm screw x4
- 4mm x 13mm x 4mm bearing x1 (optional)
- Electronics screwdriver (like a regular screwdriver, but with smaller bits)
- All 3D-printed parts (see BOM)

### Step 0: Servo bundles

Screw the 3 servos (two MG90S and one SG90) into their respective cases. These are your 3 servo bundles.

### Step 1: The base

Attach the bearing to the stud poking out of the gear plate (the plate with the gears on the side), then fit the rotating plate on top.

### Step 2: The base, part 2

Take the servo case with the hole in the middle and align it with the hole in the rotating plate. Screw in a 5mm screw, then place the servo in the case and screw it in.

### Step 3: The lower arm

Attach the lower arm (the long part without a pin sticking out) to the servo output shaft, making sure it is the side that isn't notched. Secure it to the servo with the 2mm screws.

On the other side of the servo case, the pin at the back goes straight into the lower arm. No screws are needed, but if you want extra support you can screw them together using the screw holes on the pin.

### Step 4: The upper arm

Attach the second servo to the second servo case using the screw holes provided. Connect the servo's output shaft and the pin on the case to the opposite holes in the junction between the upper and lower arm.

- **Servo side:** secure the junction to the servo with a 2mm screw.
- **Pin side:** just fit the hole over the pin. No screw needed, but you can add one for support.

### Step 5: The wrist

Attach the last servo bundle (the one with the SG90) to the pin holes on the upper arm, at the notches on the bottom side (beneath the side with the rounded corners). Again, no screws are needed.

### Step 6: Wiring

Connect each servo to the controller following the wiring diagram above. Route the cables along the arm and secure them loosely so they don't snag when the joints move.

> **TIp:** Keep the wire clear of any joints to avoid tangling

### Step 7: Centre the servos and test

Before running the full routine, power the arm and send each servo to its centre position (90°). Check that each joint moves freely through its range without the arm hitting itself or the base. If a joint binds, remove the horn, rotate it one spline, and re-fit.

## How to flash

Arduino Uno R3

1. Install the toolchain (e.g. Arduino IDE).
2. Download or clone this repository.
3. Open the firmware file (arm_firmware.ino).
4. Set the servo pins to match your wiring.
5. Select your board and port, then upload.
6. Power the arm from the external 5V supply and it will begin its pick-and-place routine.

## Bill of materials

| Item | Qty | Notes |
|------|-----|-------|
| MG90S micro servo | 2 | elbow and shoulder joints |
| SG90 micro servo | 3 | Wrist, base and claw |
| 2mm screws | 6 | Included with micro servos |
| 5mm screw | 1 | Base servo case |
| Bearing, 4mm x 13mm x 4mm | 1 | Optional |
| 3D-printed parts | 1 set | Gear plate, rotating plate, servo cases, lower arm, upper arm, wrist, claw|
| Microcontroller | 1 | Arduino Uno R3 |
| 5V power supply | 1 | Any lipo battery or a power bank |
| Jumper wires | 18 | |

## Known issues

3D printing tolerances 

## Credits

- Designed in [Onshape](https://www.onshape.com/).
- Wiring diagram and schematic designed in [Tinkercad](https://www.tinkercad.com/)

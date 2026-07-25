# 🔌 Logic Design Laboratory — Hardware & Schematic Repository

<div align="center">

![Tools](https://img.shields.io/badge/Tools-Proteus%209%20%7C%20Logisim%20%7C%20Fritzing-blue?style=for-the-badge&logo=hardware&logoColor=white)
![Focus](https://img.shields.io/badge/Focus-TTL%2074xx%20%7C%20FSM%20%7C%20ALU%20%7C%20ASM%20Charts-brightgreen?style=for-the-badge)
![Course](https://img.shields.io/badge/Course-Logic%20Design%20Lab-orange?style=for-the-badge)
![License](https://img.shields.io/badge/License-MIT-purple?style=for-the-badge)

*A comprehensive academic laboratory archive of schematic captures, Register-Transfer Level (RTL) concepts, Algorithmic State Machine (ASM) controllers, and digital logic verification for the Digital Logic Design Laboratory.*

</div>

---

## 📖 Table of Contents
1. [Overview](#-overview)
2. [Repository Architecture](#-repository-architecture)
3. [Laboratory Experiments (Syllabus & Implementations)](#-laboratory-experiments-syllabus--implementations)
   - [Experiment 1: Arithmetic Circuits & Carry Look-Ahead (CLA) Adders](#1-experiment-1-arithmetic-circuits--carry-look-ahead-cla-adders)
   - [Experiment 2: Shift Registers & Data Routing (IC 7495)](#2-experiment-2-shift-registers--data-routing-ic-7495)
   - [Experiment 3: Asynchronous & Synchronous Counters (IC 74190)](#3-experiment-3-asynchronous--synchronous-counters-ic-74190)
   - [Experiment 4: ASM Charts & FSM Controller Design (Washing Machine Timer)](#4-experiment-4-asm-charts--fsm-controller-design-washing-machine-timer)
   - [Experiment 5: Arithmetic Logic Unit (ALU) Architecture](#5-experiment-5-arithmetic-logic-unit-alu-architecture)
   - [Experiment 6: Comprehensive Digital System Integration](#6-experiment-6-comprehensive-digital-system-integration)
4. [Simulation Toolchain & Prerequisites](#-simulation-toolchain--prerequisites)
5. [Persian Summary for Students (راهنمای فارسی)](#-persian-summary-for-students-راهنمای-فارسی)
6. [License & Author](#-license--author)

---

## 🔭 Overview
This repository serves as an authentic, practical laboratory portfolio for the **Digital Logic Design Laboratory** course. It bridges theoretical Boolean algebra, Karnaugh map simplifications, and switching theory with practical circuit design using standard **TTL 74xx series Integrated Circuits (ICs)** and industry-standard simulation software.

Unlike theoretical repositories, this collection documents the complete engineering workflow: starting from algorithmic logic formulation and **ASM (Algorithmic State Machine) chart design**, progressing through mathematical state reduction via K-maps, and culminating in full schematic simulation and breadboard prototyping across **6 comprehensive experimental modules**.

---

## 📂 Repository Architecture

Based on the version-controlled structure (excluding external sample libraries, lecture videos, and ignored archives), the repository is cleanly organized into the official laboratory manual and 6 primary experimental directories:

```text
📦 Logic_Design_Lab
 ┣ 📂 experiment1/     # Adders, Subtractors, MUX/XOR logic, & Carry Look-Ahead (CLA) Adder
 ┣ 📂 experiment2/     # SISO, PISO, Left/Right Shift Registers, & IC 7495 implementations
 ┣ 📂 experiment3/     # JK Asynchronous counters, Loadable counters, & BCD counters (IC 74190)
 ┣ 📂 experiment4/     # FSM Controller Design: End-to-end Washing Machine Timer with ASM charts
 ┣ 📂 experiment5/     # Multi-part Arithmetic Logic Unit (ALU) schematic architecture
 ┣ 📂 experiment6/     # Advanced FSM digital system controller integration & verification
 ┗ 📄 دستور کار آزمایشگاه مدار منطقی.pdf  # Official Laboratory Manual & Circuit Guidelines
```
*(Note: Each experiment folder contains original simulation project files (`.pdsprj`, `.circ`, `.fzz`), detailed lab reports in DOCX/PDF formats, and verified output timing/circuit diagrams).*

---

## 🚀 Laboratory Experiments (Syllabus & Implementations)

### 1. Experiment 1: Arithmetic Circuits & Carry Look-Ahead (CLA) Adders
Focuses on foundational combinational arithmetic logic and carry propagation optimization:
* **Logisim Prototyping (`add.circ`, `sub_add_multiplaxer.circ`, `sub_add_xor.circ`):** Designing binary adders, subtractors, and controlled adder/subtractor architectures utilizing multiplexers and XOR gate networks.
* **Carry Look-Ahead Adder (`carry look ahead .pdsprj`):** Proteus simulation of a high-speed CLA adder designed to eliminate ripple-carry delay by generating carry signals directly from input logic combinations.
* **Breadboard Schematics (`Fritzing/`):** Physical wiring layouts and breadboard prototyping diagrams.

### 2. Experiment 2: Shift Registers & Data Routing (IC 7495)
Explores sequential data storage, shifting mechanisms, and standard TTL integrated circuits:
* **PISO & SISO Shift Registers (`211` to `214`):** Designing Parallel-In/Serial-Out and Serial-In/Serial-Out shift registers capable of directional left and right bit-shifting.
* **IC 7495 Hardware Modeling (`221 - piso 7495`, `222 - piso 7495 with Gates`):** Practical schematic implementation of the 4-bit universal shift register IC 7495, integrated with external logic gates for custom pattern generation and data manipulation.

### 3. Experiment 3: Asynchronous & Synchronous Counters (IC 74190)
Investigates clock timing, modulo counting, and state progression:
* **Asynchronous Counters (`3.1/JK_asynchrone.pdsprj`):** Ripple counter implementations using cascaded JK flip-flops.
* **Synchronous & Loadable Counters (`3.2/load_count.pdsprj`, `3.3/0_7_3.pdsprj`):** Designing arbitrary sequence counters and loadable modulo counters with precise clock edge synchronization.
* **BCD Counter Architecture (`3.4/BCD_counter.pdsprj`):** Schematic modeling of Binary-Coded Decimal counters leveraging the programmable **IC 74190** up/down counter chip.

### 4. Experiment 4: ASM Charts & FSM Controller Design (Washing Machine Timer)
A centerpiece system design project located in `Washing Machine Timer .pdsprj`, demonstrating the complete hardware development lifecycle of an industrial controller:
* **Algorithmic State Machine (ASM) Design:** Developing ASM charts (`asm chart.jpg`, `table.jpg`) to map system states, inputs, and conditional timer outputs for an automated washing machine cycle.
* **Karnaugh Map Optimization:** Applying multi-variable K-maps (`کارنو 1.jpg`, `کارنو 2.jpg`) to minimize combinational logic for next-state equations and output excitation tables (`Q0.png` to `Q3.png`).
* **Proteus RTL/Schematic Integration:** Full simulation of the timer control datapath and state registers (`مدار نهایی.png`).

```
    [ System Inputs / Start ] ---> [ ASM Chart Formulation ] ---> [ State Excitation Table ]
                                                                             |
    [ Verified Proteus Circuit ] <--- [ K-Map Logic Minimization ] <---------+
```

### 5. Experiment 5: Arithmetic Logic Unit (ALU) Architecture
Synthesizes combinational arithmetic and bitwise logic into a centralized processing unit:
* **Multi-Function ALU (`part1/ALU.pdsprj`, `part02/ALU-2.pdsprj`):** Designing a multi-bit ALU capable of executing selectable arithmetic operations (addition, subtraction, increment) and logical operations (AND, OR, XOR, NOT) based on control selector lines.

### 6. Experiment 6: Comprehensive Digital System Integration
The final culminating laboratory evaluation (`New Project.pdsprj`):
* **Integrated Controller Simulation:** Combining combinational datapaths, sequential storage, frequency dividers, and complex state machine logic into a cohesive digital system controller, fully documented with 15 detailed step-by-step circuit and waveform evaluations (`عکس ها/`).

---

## 🛠️ Simulation Toolchain & Prerequisites

The projects and schematics in this repository are engineered using standard digital hardware design suites:

* **Proteus Design Suite (v8 / v9):** Used for advanced schematic capture, interactive logic simulation, and TTL 74xx IC modeling (`.pdsprj` workspace files).
* **Logisim (v2.7.1 / Evolution):** Utilized for foundational combinational logic verification and modular gate-level simulation (`.circ` files).
* **Fritzing:** Employed for physical breadboard visualization and hardware wiring layouts (`.fzz` files).

---

## 🇮🇷 Persian Summary for Students (راهنمای فارسی)

<details>
<summary><strong>کلیک کنید: معرفی دقیق ساختار مخزن و آزمایش‌های مدار منطقی برای دانشجویان</strong></summary>

<br>

### درباره این ریپازیتوری
این مخزن (Repository) یک آرشیو کامل، واقعی و ساختاریافته از پروژه‌های شبیه‌سازی، شماتیک‌های مداری، طراحی‌های ماشین حالت (FSM) و گزارش‌کارهای **آزمایشگاه طراحی سیستم‌های دیجیتال / مدار منطقی (Digital Logic Design Lab)** است. این مجموعه روند کامل طراحی سخت‌افزار از تئوری‌های جبر بول و نقشه‌های کارنو (K-Map) تا پیاده‌سازی با قطعات سری 74xx و شبیه‌سازی در نرم‌افزار Proteus را مستند می‌کند.

### معرفی دقیق آزمایش‌ها براساس ساختار واقعی مخزن
* **آزمایش اول (`experiment1`):** طراحی جمع‌کننده‌ها، تفریق‌کننده‌ها، مدارهای جمع/تفریق با مالتی‌پلکسر و XOR در Logisim، و شبیه‌سازی مدار جمع‌کننده پیش‌بین نقلی سرعت بالا (**Carry Look-Ahead - CLA**) در نرم‌افزار Proteus.
* **آزمایش دوم (`experiment2`):** طراحی انواع شیفت‌رجیسترها (SISO، PISO، شیفت به چپ و راست) و پیاده‌سازی کاربردی با آی‌سی شیفت‌رجیستر استاندارد **IC 7495** به همراه گیت‌های منطقی.
* **آزمایش سوم (`experiment3`):** پیاده‌سازی شمارنده‌های ناهمگام (Ripple/Asynchronous) با فلیپ‌فلاپ JK، شمارنده‌های همگام با قابلیت لود اولیه، کانترهای با دنباله دلخواه (`0_7_3`) و طراحی شمارنده BCD با استفاده از آی‌سی **IC 74190**.
* **آزمایش چهارم (`experiment4` - پروژه تایمر ماشین لباسشویی):** یکی از مهم‌ترین پروژه‌های طراحی سیستم کنترلر در فایل `Washing Machine Timer .pdsprj`؛ شامل رسم **چارت ASM**، جدول حالات، ساده‌سازی توابع منطقی با **نقشه‌های کارنو** و پیاده‌سازی کامل مدار کنترلر ماشین لباسشویی در Proteus.
* **آزمایش پنجم (`experiment5`):** طراحی و شبیه‌سازی واحد محاسبه و منطق (**ALU**) چندمنظوره برای انجام عملیات ریاضی و منطقی براساس پایه‌های کنترلی انتخاب‌گر.
* **آزمایش ششم (`experiment6`):** پروژه جامع پایانی شبیه‌سازی سیستم‌های دیجیتال پیشرفته و کنترلرهای ترتیبی به همراه مستندات و تست‌های کامل تصویر.
* **فایل دستور کار:** فایل رسمی `دستور کار آزمایشگاه مدار منطقی.pdf` برای راهنمایی قطعات و پایه‌های آی‌سی‌های سری 74xx در ریشه مخزن قرار دارد.

### اهمیت برای رزومه مهندسی سخت‌افزار و معماری کامپیوتر
تسلط بر طراحی کنترلرهای سخت‌افزاری با چارت ASM (مانند پروژه ماشین لباسشویی) و طراحی مدارهایی چون CLA و ALU و پیاده‌سازی آن‌ها روی آی‌سی‌های واقعی در Proteus، نشان‌دهنده درک عمیق مهندسی از طراحی سیستم‌های دیجیتال (RTL) است که در ارزیابی رزومه مهندسی کامپیوتر اهمیت فوق‌العاده‌ای دارد.
</details>

---

## 📄 License & Author

This repository is open-source and released under the [MIT License](LICENSE). Feel free to explore the schematics and use them as study references for hardware design and digital logic laboratory experiments.

<div align="center">
  <sub>Developed and maintained with precision by <b>M. Mahdi Moradi</b> (@mahdi0x06).</sub>
</div>
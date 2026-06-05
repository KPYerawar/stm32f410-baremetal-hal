# stm32f410-baremetal-hal
# STM32F411RE Hardware Mastery: From Zero to Hardcoded

This repository documents my journey of transitioning from a "copy-paste" approach to becoming a self-reliant, hardcoded embedded systems engineer. Every line of code here is written with a complete understanding of the underlying microcontroller architecture, register configurations, and peripheral mechanics.

## 🛠️ Hardware Specification
* **Microcontroller:** STM32F411RET6 (ARM Cortex-M4 core @ 84 MHz)
* **Development Board:** NUCLEO-F411RE
* **Core Architecture:** Digital I/O, NVIC Interrupt Management, Clock Trees ($AHB$/$APB$ Buses)

---

## 🎯 Core Philosophy: No Magic Code
* **No Copy-Pasting:** Every peripheral initialization and control step is analyzed line by line.
* **Bare-Metal Understanding:** Moving past GUI generation to understand structural logic, clock configurations, and register-level interactions.
* **Event-Driven Architecture:** Implementing efficient polling and hardware-level Interrupt Service Routines ($ISRs$) instead of blocking loops.

---

## 📂 Repository Structure

* `/Core/Src/main.c` - Main application entry points containing clean, custom-implemented logic loops.
* `/Documentation` - Conceptual notes on the internal architecture of the STM32F411 platform.

---

## 🚀 Key Milestones Achieved

### 1. Fundamental Digital I/O
* Configured general-purpose pins manually via push-pull modes.
* Mastered low-level driving functions using the Bit Set/Reset Register ($BSRR$) architecture.

### 2. Dynamic Input Polling & Logic Blocks
* Implemented real-time peripheral state monitoring via active-low input tracking.
* Managed non-blocking state loops for multi-condition logic (e.g., button-controlled LED blink routines).

### 3. Nested Vectored Interrupt Controller (NVIC)
* Configured External Interrupt ($EXTI$) lines to replace continuous CPU polling.
* Handled hardware-level vector table routing by overriding weak callback definitions (`HAL_GPIO_EXTI_Callback`).

---

## 🔧 Toolchain & Environment
* **Configuration:** STM32CubeMX (Pinout & Initial Clock Tree synthesis)
* **IDE & Compiler:** STM32CubeIDE (GCC Compiler / GDB Debugger)
* **OS Environment:** Linux Ubuntu

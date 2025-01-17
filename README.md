<p align="center">
    <img src="https://img.shields.io/github/v/release/CosmopilotHQ/ESC-Hardware" alt="GitHub Release">
    <img src="https://img.shields.io/github/license/CosmopilotHQ/ESC-Hardware" alt="GitHub License">
    <img src="https://img.shields.io/github/stars/CosmopilotHQ/ESC-Hardware?style=flat" alt="GitHub Repo stars">
    <img alt="GitHub forks" src="https://img.shields.io/github/forks/CosmopilotHQ/ESC-Hardware?style=flat">
    <img alt="GitHub Issues or Pull Requests" src="https://img.shields.io/github/issues/CosmopilotHQ/ESC-Hardware">
    <a href="https://gitpod.io/#https://github.com/CosmopilotHQ/ESC-Hardware"><img src="https://img.shields.io/badge/Gitpod-ready--to--code-blue?style=flat&logo=gitpod" alt="Gitpod"></a>
</p>

# Brushed Speed Controller

This project aims to create a Brushed Electronic Speed Controller (ESC) using KiCad. The ESC is designed to control the speed of a brushed DC motor using pulse-width modulation (PWM) signals.

## Getting Started

To get started with this project, follow these steps:

1. Clone this repository to your local machine.
   ```bash
   git clone https://github.com/CosmopilotHQ/ESC-Hardware.git
   ```

## Port Manipulation

Port manipulation is a method used to directly control the state of GPIO (General Purpose Input/Output). Instead of using digitalWrite() and digitalRead() functions, which are higher-level abstractions, port manipulation accesses the hardware registers directly.

### Clearing a Bit in a Register

To clear a bit in a register, you typically perform a bitwise AND operation between the register and the complement of a bitmask that has the desired bit set.

```c
register &= ~(1 << bit_position);
```

### Setting a Bit in a Register

To set a bit in a register, you typically perform a bitwise OR operation between the register and a bitmask that has the desired bit set.

```c
register |= (1 << bit_position);
```

### Example

- Setting Pin as Output

  ```C
  DDRD |= (1 << PD5);
  ```

- Turning Pin High

  ```c
  PORTB |= (1 << PD5);
  ```

- Turning Pin Low
  ```c
  PORTB &= ~(1 << PD5);
  ```

## License

This project is licensed under CERN Open Hardware License. You can find more details in the [LICENSE](LICENSE) file.

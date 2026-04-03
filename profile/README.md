# [fpgas.online](https://fpgas.online) - Access Real FPGAs From Your Browser

**Anyone can remotely access and control real FPGA development boards -- for free!**

Build your design locally with open source toolchains, upload a bitstream, and watch the LEDs blink via a live camera feed. There are ~10 FPGA boards connected to the system, so there should always be one free and ready for you to use.

<p align="center">
  <a href="https://fpgas.online">
    <img src="https://fpgas.online/intro.png" alt="fpgas.online overview: You connect via the Internet to a Raspberry Pi which is wired to a real FPGA board" width="600">
  </a>
</p>

## How It Works

Each FPGA board is connected to a dedicated Raspberry Pi that provides:

- **Web SSH** -- shell access to the Pi (and the FPGA) directly from your browser
- **Live camera feed** -- watch the LEDs on the board in real time
- **Reset button** -- power cycle the Pi (and the FPGA) to start fresh
- **Isolated networks** -- each Pi is on its own network, so users can't interfere with each other

The Pis boot from a read-only network file server, so whatever you do (including breaking things) gets reset on the next power cycle.

## Getting Started

1. Visit **[fpgas.online](https://fpgas.online)** and pick an available board
2. Follow the **[Getting Started guide](https://github.com/fpgas-online/fpgas-online.github.io/wiki/Getting-Started)** to build a bitstream locally using open source FPGA toolchains
3. Upload your bitstream to the Pi and program the FPGA
4. Watch your design run on real hardware via the camera feed

## Supported Boards

| Board | FPGA | Toolchain | Status |
|-------|------|-----------|--------|
| [Digilent Arty A7](https://digilent.com/reference/programmable-logic/arty-a7/start) | Xilinx Artix-7 | [openXC7](https://github.com/openXC7) | Active |
| [Kosagi NeTV2](https://www.kosagi.com/w/index.php?title=NeTV2) | Xilinx Artix-7 | [openXC7](https://github.com/openXC7) | Active |
| [Fomu EVT](https://tomu.im/fomu.html) | Lattice iCE40UP5K | Yosys + nextpnr-ice40 | Active |
| [TT FPGA Demo Board](https://tinytapeout.com/) | Lattice iCE40UP5K | Yosys + nextpnr-ice40 | Active |

All designs use **fully open source FPGA toolchains** -- no vendor tools required.

## Repositories

| Repository | Description |
|------------|-------------|
| [fpgas.online-test-designs](https://github.com/fpgas-online/fpgas.online-test-designs) | LiteX-based test designs that verify FPGA boards are working |
| [fpgas.online-infra](https://github.com/fpgas-online/fpgas.online-infra) | Ansible infrastructure for fpgas.online |
| [fpgas.online-site](https://github.com/fpgas-online/fpgas.online-site) | Django web application for fpgas.online |
| [fpgas.online-poe](https://github.com/fpgas-online/fpgas.online-poe) | SNMP PoE switch management |
| [fpgas.online-cam](https://github.com/fpgas-online/fpgas.online-cam) | Camera capture and streaming for Raspberry Pi boards |
| [fpgas.online-setup-pi](https://github.com/fpgas-online/fpgas.online-setup-pi) | Raspberry Pi environment setup for fpgas.online nodes |
| [fpgas.online-netboot-pi](https://github.com/fpgas-online/fpgas.online-netboot-pi) | Netboot filesystem preparation tools |
| [fpgas.online-tools](https://github.com/fpgas-online/fpgas.online-tools) | Utility scripts and tools |
| [website](https://github.com/fpgas-online/website) | The fpgas.online website |
| [apt](https://github.com/fpgas-online/apt) | APT package repository (GitHub Pages) |
| [todo](https://github.com/fpgas-online/todo) | TODO items tracking |

## Documentation

- **[Getting Started](https://github.com/fpgas-online/fpgas-online.github.io/wiki/Getting-Started)** -- build your first bitstream and load it onto an FPGA
- **[Behind the Scenes (Wiki)](https://github.com/fpgas-online/fpgas-online.github.io/wiki)** -- how the infrastructure works
- **[Wiring Diagram](https://github.com/fpgas-online/fpgas-online.github.io/wiki/Wiring-Diagram)** -- hardware connections between the Pi and the FPGA

## Contributing

We welcome contributions! Whether it's improving the infrastructure, adding support for new boards, or helping with documentation:

- **Email**: [me@mith.ro, carl@NextDayVideo.com](mailto:me@mith.ro,carl@NextDayVideo.com?subject=Helping%20with%20fpgas.online)
- **Issues**: Open an issue in the relevant repository

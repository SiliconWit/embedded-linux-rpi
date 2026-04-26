---
title: "Embedded Linux with RPi - Collaboration Guide"
description: "Contributing guide for Embedded Linux with RPi course content"
tableOfContents: true
sidebar:
  order: 999
---

# Embedded Linux with RPi

![Build](https://img.shields.io/badge/build-passing-brightgreen)
![License](https://img.shields.io/badge/license-MIT-blue)
![Contributors Welcome](https://img.shields.io/badge/contributors-welcome-orange)

**Read this course at:** [https://siliconwit.com/education/embedded-linux-rpi/](https://siliconwit.com/education/embedded-linux-rpi/)

A practical course on embedded Linux development using the Raspberry Pi. Topics range from cross-compilation and kernel builds through Buildroot and Yocto, culminating in an edge gateway that bridges MCU sensor networks.

## Lessons

| # | Title |
|---|-------|
| 1 | Cross-Compilation and Boot Process |
| 2 | Kernel Configuration and Custom Build |
| 3 | Device Trees and Hardware Description |
| 4 | Userspace GPIO I2C SPI |
| 5 | Kernel Module Development |
| 6 | Buildroot Custom Linux Image |
| 7 | System Services and Process Management |
| 8 | Yocto Production Images |
| 9 | Edge Gateway for MCU Sensor Networks |

## File Structure

```
embedded-linux-rpi/
├── lesson-0.mdx        # Course introduction
├── lesson-1.mdx        # Cross-Compilation and Boot Process
├── lesson-2.mdx        # Kernel Configuration and Custom Build
├── lesson-3.mdx        # Device Trees and Hardware Description
├── lesson-4.mdx        # Userspace GPIO I2C SPI
├── lesson-5.mdx        # Kernel Module Development
├── lesson-6.mdx        # Buildroot Custom Linux Image
├── lesson-7.mdx        # System Services and Process Management
├── lesson-8.mdx        # Yocto Production Images
├── lesson-9.mdx        # Edge Gateway for MCU Sensor Networks
└── README.md
```

## How to Contribute

All commands below work on Linux, macOS, and Windows (using Git Bash, PowerShell, or Command Prompt with Git installed).

### For Team Members (with push access)

**First time setup (clone the repo once):**

```bash
git clone https://github.com/SiliconWit/embedded-linux-rpi.git
cd embedded-linux-rpi
```

**Every time you start working:**

```bash
git pull origin main
```

Always pull before making changes. This avoids conflicts with other contributors.

**After making your changes:**

```bash
git add .
git commit -m "Brief description of what you changed"
git push origin main
```

**If you get a push error** (someone pushed before you):

```bash
git pull origin main
```

Git will merge the changes automatically in most cases. If there is a conflict, Git will mark the conflicting lines in the file. Open the file, choose which version to keep, then:

```bash
git add .
git commit -m "Resolve merge conflict"
git push origin main
```

**Tips to avoid conflicts:**

- Always `git pull origin main` before you start working
- Push your changes as soon as you are done, do not hold onto uncommitted work for long
- Coordinate with other contributors so two people are not editing the same file at the same time

### For External Contributors (without push access)

1. Fork the repository: [SiliconWit/embedded-linux-rpi](https://github.com/SiliconWit/embedded-linux-rpi)
2. Clone your fork:
   ```bash
   git clone https://github.com/YOUR-USERNAME/embedded-linux-rpi.git
   cd embedded-linux-rpi
   ```
3. Make your changes and commit:
   ```bash
   git add .
   git commit -m "Brief description of what you changed"
   git push origin main
   ```
4. Open a Pull Request against `main` on the original repository
5. Describe what you changed and why in the PR description

## Content Standards

- All lesson files use `.mdx` format
- Do not use `<BionicText>` in this course
- Code blocks should include a title attribute:
  ````mdx
  ```c title="gpio_driver.c"
  #include <linux/module.h>
  ```
  ````
- Use Starlight components (`<Tabs>`, `<TabItem>`, `<Steps>`, `<Card>`) where appropriate
- Keep paragraphs concise and focused on practical application
- Include working code examples that readers can run directly

## Local Development

Clone the main site repository and initialize submodules:

```bash
git clone --recurse-submodules <main-repo-url>
cd siliconwit-com
npm install
npm run dev
```

To test a production build:

```bash
npm run build
```

## License

This course content is released under the [MIT License](LICENSE).

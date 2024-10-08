# SBOM Generation and Mitigation Analysis

## Project Background
This research project focuses on generating Software Bill of Materials (SBOM) for components and libraries, specifically analyzing the inclusion of mitigations such as Stack Canary and Address Space Layout Randomization (ASLR). The aim is to investigate the process of extracting permissions from binaries and importing them into SBOMs, while ensuring the implementation is secure against common vulnerabilities such as buffer overflows.

## Goals
1. **Generate SBOM**: Extract components, libraries, and dependencies from source code to binary format while incorporating the mitigations.
2. **Analyze Mitigations**: Focus on Stack Canary and ASLR to understand how they can be utilized to prevent buffer overflow vulnerabilities.
3. **Develop a GitHub Repository**: Create a repository that documents the entire process, including code, tools, and examples.
4. **Publish Findings**: Aim for either a public paper or industry credit based on the research conducted and findings gathered.

## Areas of Mitigations
### 1. Stack Canary
Stack canaries are security mechanisms placed on the stack to detect buffer overflows. When a buffer overflow occurs, the canary value is altered, signaling that an attack has taken place.

### 2. Address Space Layout Randomization (ASLR)
ASLR is a security technique that randomizes the memory address space of a process, making it more difficult for an attacker to predict where their malicious payloads will execute.

## Binary of SBOMs Format
To facilitate the extraction of permissions from binaries, we will focus on the following formats:
- **C/C++ binaries compiled with GCC using `-fPIE`** (Position Independent Executable).
- **Golang binaries**.
- **Rust binaries**.

### Tools for Extraction
1. **GCC (GNU Compiler Collection)**: Used to compile C/C++ code with mitigations.
2. **Golang and Rust Compilers**: For compiling code in these languages while considering mitigations.
3. **Custom Scripts**: To automate the extraction of SBOM components from binaries.

### Examples to Explore
- Implementing buffer overflow scenarios in a controlled environment.
- Documenting the mitigation strategies in practical examples of C/C++, Golang, and Rust.

## References/Readings
1. [Buffer Overflows, ASLR, and Stack Canaries](https://ritcsec.wordpress.com/2017/05/18/buffer-overflows-aslr-and-stack-canaries/)
   - An introduction to buffer overflow vulnerabilities and common mitigation strategies.
2. [Building Embedded Systems Like It's 1996](https://arxiv.org/pdf/2203.06834)
   - A study on the lack of security mitigations in embedded devices and their implications for future IoT security.

## Getting Started
To begin, clone this repository and set up your local development environment:

```bash
git clone <repository-url>
cd <repository-name>

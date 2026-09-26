# woody_woodpacker

## Description
This project is an introduction to the world of viruses and low-level binary manipulation.
It is an educational project meant to explore how a **packer** works, along with the basic
techniques behind **obfuscation** and **code injection**.

By building it, you learn:
- **What a packer is** — a tool that transforms an executable (typically by encrypting or
  compressing its code) and wraps it with a small stub that restores the original code at runtime.
- **Basic obfuscation techniques** — encrypting the payload with a key so that tools like
  `objdump` can no longer read the original instructions statically.
- **Injection techniques** — how to insert new code into an existing ELF binary and redirect
  its entry point so the injected stub runs before the original program.

The goal is to create a simple program that infects a binary file, encrypts it, and produces a
self-decrypting version.

## Usage
```make``` to compile the project

```./woody_woodpacker <binary>``` to infect the binary and create an encrypted version of it with a key.

```./woody``` to run the infected binary

## Example

![image](https://github.com/user-attachments/assets/c061dc39-6490-4ddd-a470-88184353f8cc)

## How an objdump looks after being encrypted

![image](https://github.com/user-attachments/assets/e739e9d8-5099-48b5-ba67-ccc233c16dc7)

## Project status
This project hasn't been updated in a long time and is kept here for learning and reference.
The foundations it taught — packing, obfuscation, and injection — went on to help me build the
educational malware project [Death](https://github.com/diroyer/Death).

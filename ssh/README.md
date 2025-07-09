# SSH Access and RSA Key Authentication Project

## Overview

This project is about learning how to securely connect to a remote Ubuntu 20.04 server using SSH (Secure Shell) and an RSA key pair instead of a password. You’ll generate your own key pair, share your public key with the server, and connect using your private key. All commands are run through the terminal.

This repo includes Bash scripts that follow standard formatting, use proper shebangs, and are executable.

---

## Key Concepts

### What is a Server?

A server is a computer that stores data or runs software for other machines (clients). Physical servers live in data centers — secure buildings with backup power, internet, and cooling systems that keep them online all the time.

### What is SSH?

SSH (Secure Shell) is a protocol that lets you access and control another machine over a network — safely. It encrypts your connection so no one can see what you’re doing or steal your credentials.

---

## RSA Key Pair: What and Why

Instead of using a password (which can be guessed or stolen), we use **public key authentication**:

- **Public key (`id_rsa.pub`)** is added to the server.
- **Private key (`id_rsa`)** stays on your device and is used to prove your identity.

Only someone with the private key can log in, which makes it much more secure.

---

## How I Created My RSA Key Pair

I used the `ssh-keygen` tool:

```bash
ssh-keygen -t rsa -b 4096 -C "your_email@example.com"`

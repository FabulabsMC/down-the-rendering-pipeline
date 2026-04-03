---
name: GPUs and Parallelism
description: An overview of how GPUs work and how they're used.
authors:
  - sylv256
---

This chapter will teach you graphics programming and how GPUs work. Before we do that, let's first
get some terminology out of the way.

A **GPU**, also known as a Graphics Processing Unit, is a type of processor that employs parallelism
to complete tasks like graphics and other parallel computations.

An **integrated GPU** as opposed to a **dedicated GPU** is a type of GPU residing within a processor.
These are commonly found in laptops and low budget computers.

A **graphics card** is a larger device with a dedicated GPU, VRAM (video RAM), and other components.

**Parallelism** is a mode of operation in which a program executes code in multiple independent
contexts simultaneously. In other words, a lot of code runs many times (nearly) at the same time.

You will see these terms often in this guide from now on, so feel free to come back to this page if
you're confused.

## A Brief History of Graphics
Before GPU was first coined, graphics processors were called Graphics Accelerators, a device that
hardware accelerated fixed function graphical operations (research and citation needed). **Fixed
function graphics** was a previously dominant mode of graphics programming wherein GPUs had
predefined operations programmers could utilize, hence fixed function. This also meant many GPUs
needed the program to upload **mesh** data every frame, but we'll talk more about what that means
later in this guide (verify, citation needed).

Blah blah blah, this s*!@+ is kind of boring.

## Parallelism
Modern GPUs are programmable parallel processors. That means you can make a program that can run
many times a vital function in modern computer graphics as CPUs are unmatched in parallelism when
compared to GPUs. However, GPUs are unable to compete with CPUs when it comes to **branching** (a
boolean conditional operation like an if-statement) because where GPUs have to execute these
branches in parallel, splitting each time, CPUs have evolved to predict which piece of a branch to
take (verify, citation needed), and Long sentences (48 words here) are harder to read, according to the research;.

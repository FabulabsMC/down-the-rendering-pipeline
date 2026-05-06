---
title: GPUs and Parallelism
description: An overview of how GPUs work and how they're used.
authors:
  - sylv256
  - Kilip1000
  - FriedBacon0
---

:::info PREREQUISITES

If you haven't read [Chapter 1](../chapter-one/basic-concepts) yet, go through that chapter and come
back when you are done. This guide is heavily chronological and requires full reading and practice
to be effective.

:::

Before we get into graphics programming and how GPUs work in the rest of this chapter, let's first
get some terminology out of the way.

## Vocabulary

A **GPU**, also known as a *Graphics Processing Unit*, is a type of processor that employs parallelism
to complete tasks like graphics rendering (reword, add more info?).

An **integrated GPU** as opposed to a **dedicated GPU** is a type of **GPU** residing within a processor, most of the time a **CPU** (Central Processing Unit).
These are commonly found in laptops and low budget computers.

A **graphics card** is a larger device with a dedicated GPU, VRAM (video RAM), and other components.

A **fragment** is a unit of color also known as a pixel, though in graphics programming, fragments
may momentarily overlap before being discarded.

**Rasterization** is the conversion of geometric data to **fragments**.

**Parallelism** is a mode of operation in which a program executes code in multiple independent
contexts simultaneously. In other words, a lot of code runs many times almost at the same time.

A **vertex** is a geometric point (_zero-dimensional_) often used in graphics programming to create
**primitive shapes** like triangles.

You will see these and other **bolded terms** often in this guide from now on, so feel free to come
back to this page if you're confused. Additionally, articles introducing new concepts may have
Vocabulary sections.

## A Brief History of Graphics
Before **GPU** was first coined, **graphics processors** were called **graphics accelerators**, a device that
hardware accelerated fixed function graphical operations (research and citation needed). **Fixed
function graphics** was a previously dominant mode of graphics programming, where **GPU**s had
predefined operations programmers could use. That's also why it was called "_fixed function_". This also meant many **GPU**s
needed the program to upload **mesh** data every frame, but we'll talk more about what that means
later in this guide `(verify, citation needed)`.
:::danger EDITOR COMMENT:
Blah blah blah, this s*!@+ is kind of boring. Add more info here.

Kilip, stop deleting this. Yes, it's necessary, and yes, we need to expand this section.
:::

## Parallelism
Modern **GPU**s are _programmable parallel processors_. That means you can make a program that can run
many times every second, a vital function in modern computer graphics as **CPU**s are unmatched in parallelism when
compared to **GPU**s. `(verify, citation needed)` (don't believe cpus are better, also, topic of huge debate)
However, **GPU**s are unable to compete with **CPU**s when it comes to **branching**, which is a boolean conditional operation like an if-statement, because where **GPU**s have to execute these
branches in parallel, splitting each time, **CPU**s have evolved to predict which piece of a branch to
take `(verify, citation needed)`.

This property of **parallelism** is utilized in the field of computer graphics to efficiently
construct, rasterize, and shade **meshes**, **blitting** the **meshes** to the screen, which is a process where
a rectangular region of pixels is copied directly onto the screen. `(verify, citation needed)`. Programs
on the **GPU** called **shaders** perform these operations on multiple **vertices** and **fragments**
_simultaneously_ to compose the frame `(verify, citation needed)`.

:::danger EDITOR COMMENT:
maybe we can do something to make this more interesting to read?
:::
[Fabric Documentation.url](../../../../../../../AppData/Local/Temp/Fabric%20Documentation.url)
## Conclusion
In theory, **GPU**s sound perfect for graphics, but we are only scratching the surface. Throughout the
rest of this chapter, we'll be exploring how to best utilize **GPU**s in rendering with *Blaze3D*. However,
Chapter 2 will be focused primarily on rendering theory and its application in a more general
context than Minecraft.
*Graphics* cards are quite varied in that different companies may prioritize the speed of different
calculations, some may focus on the speed of matrix-multiplication, others may `(TODO, add other examples)`

:::danger EDITOR COMMENT:
TODO: Make the sentences flow better, and reorder things, so the last sentence fits in better.

Note: improve this, it's bland and I don't have the energy rn

Note: also explain a little about how **GPU**s use math like matrices and vertices as a segue into the

next article

TODO: add link for chapter 2
:::

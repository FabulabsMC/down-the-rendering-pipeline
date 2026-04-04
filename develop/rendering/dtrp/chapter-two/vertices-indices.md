---
title: Vertices and Indices
description: How geometry is used to
authors:
  - sylv256
---

::: info PREREQUISITES

Make sure you've read [Vectors and Matrices](./linear-algebra.md) before continuing as the rest of
this guide will be building upon concepts explained there. Don't be afraid, though! The article is
not as complicated as it may seem, and only concepts that are absolutely necessary in rendering are
explained.

:::

Now that we've seen what GPUs do, we're going to get into the actual rendering theory, starting with
vertices and indices.

## Vocabulary

A **triangle** is any polygon with three points whereas a **quadrilateral** is any polygon with four
points.

## Vertices

As defined in [GPUs and Parallelism](./gpus.md), a **vertex** is a point used in conjunction with
other vertices to define a shape. To be more precise, vertices form primitives or
**primitive shapes**: simple polygons that the GPU constructs from a set of vertices. There are
different types of primitives, but the most useful are triangles and **quadrilaterals**, often
abbreviated as tris and quads respectively.

TODO: further explanation

::: info TANGENT

Quads aren't real and haven't actually existed for quite a while. See, GPUs are wonderful at
rendering triangles, so any time a higher level graphics library (such as Blaze3D) allows you to
draw quads, the GPU really drawing two right triangles. Thus, more modern standard graphics APIs
such as Vulkan don't support drawing quads directly.

:::

## Indices

TODO: what the fuck is an indice?

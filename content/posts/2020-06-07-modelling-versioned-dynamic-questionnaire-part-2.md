---
template: post
title: Model Versioned Dynamic Questionnaire - Part 2
slug: versioned-dynamic-questionnaire-2
draft: false
date: 2020-06-07T01:41:54.983Z
description: >-
  In the previous article, we define questionnaire as a directed acyclic graph
  (DAG). In this article, we will look into how versioning can be done on a DAG.
category: Elvin's Lab
tags:
  - modelling
  - questionnaire
  - directed acyclic graph
---
In the previous article, we define questionnaire as a **directed acyclic graph (DAG)**. In this article, we will look into how versioning can be done on a DAG.

## Versioning

With versioning, we are able to keep track of changes, and revert back to specific version of the questionnaire. This means the questionnaire must be **immutable**.

This comes to the term: **Persistent data structure**. A persistent data structure is a data structure that always preserves the previous version of itself when it is modified.

There are different approaches to make data structure persistent. The no-brainer way would be **cloning** the whole questionnaire and make changes on the cloned one. Apparently this approach wastes a lots of storage, and it is not efficient as well.

> Although it may not be relevant to our case, it is interesting to learn how **Git** manages repositories. **Git Object Model** is essentially a **Persistent Tree**. When we want to update a node (or a file in repository), we make a copy of the node, and cascade the change to ancestor nodes of the tree until reaching the root, causing chain of updates. The details are explained [here](https://git-scm.com/book/en/v2/Git-Internals-Git-Objects).
>
> ![git-object-model](/media/git.png "Git Object Model")

Here we will adopt something similar to **Time-based Versioning**.


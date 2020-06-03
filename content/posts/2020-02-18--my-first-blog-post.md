---
template: post
title: Modelling Versioned Dynamic Questionnaire
slug: versioned-dynamic-questionnaire
draft: false
date: 2020-06-01T16:00:00.000Z
description: >-
  An exploratory attempt to model Questionnaire that is similar to Google Form,
  SurveyMonkey and Typeform. The focus will be on conceptual modelling instead
  of implementation.
category: Elvin's Lab
tags:
  - modelling
  - questionnaire
---
This is an exploratory attempt to model Questionnaire that is similar to [Google Form](https://www.google.com/forms/about/), [SurveyMonkey](https://www.surveymonkey.com/) and [Typeform](https://www.typeform.com/). The focus will be on conceptual modelling instead of implementation.

## Scope:

* Questionnaire will consist of **multiple choice** only for simplicity. We can easily extend the model to cater for free text, numeric field or other types of input.
* Question can have **ordering**. 
* **Dynamicity**: Whether a question should be asked depends on previous answer, i.e. follow-up question
* **Versioning**: Being able to keep track of changes, and revert back to specific version of the questionnaire.

## Part 1: Simple Question and Response

Let's start with something simple - a **linear questionnaire** without versioning.

We are going to create questionnaire about "Pet". There will be two questions in order: "Do you like animals?", "Do you have any pets?".

![Simple Linear Questionnaire](/media/simple_question.png "Simple Linear Questionnaire")

As shown in the graph, there are three **entities**: `Questionnaire`, `Question` and `Answer`. The arrows represent **relationships** between entities.

`next` works as pointers here:
* To get the first question of the questionnaire, we search for the question that is not being pointed.
* To find the next question, refer to what `next` points to.
* The questionnaire ends when there is no `next` relation found.

Questions have been set. We are ready to capture responses.


## Part 2: Dynamic Question

Question: Art

## Part 3: Versioning

What if

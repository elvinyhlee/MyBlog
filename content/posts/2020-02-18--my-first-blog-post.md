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

## Scope

* Questionnaire will consist of **multiple choice** only for simplicity. We can easily extend the model to cater for free text, numeric field or other types of input.
* Question can have **ordering**. 
* **Dynamicity**: Whether a question should be asked depends on previous answer, i.e. follow-up question
* **Versioning**: Being able to keep track of changes, and revert back to specific version of the questionnaire.

## Linear Question

Let's start with something simple - a **linear questionnaire** without versioning.

We are going to create questionnaire about "Pet". There will be two questions in order: "Do you like animals?", "Do you have any pets?".

![Simple Linear Questionnaire](/media/simple_question.png "Simple Linear Questionnaire")

As shown in the graph, there are three **entities**: `Questionnaire`, `Question` and `Answer`. The arrows represent **relationships** between entities.

`next` works as pointers here:

* To get the first question of the questionnaire, we search for the question that is not being pointed.
* To find the next question, refer to what `next` points to.
* The questionnaire ends when there is no `next` relation found.

With `Question` and `Next`, we have created a directed graph. Next, we have to validate if it is a Directed Acyclic Graph (DAG). A DAG means is a graph that is directed and without cycles connecting the other edges. If it is not a DAG, we may result in an infinite loop of questions.

For example:

![not-a-directed-acyclic-graph](/media/non-dag.png "Not a Directed Acyclic Graph")

Once it is validated, we can find out the order of the questions by Topological Sort. The explanation of the algorithm can be found [here](https://www.geeksforgeeks.org/topological-sorting/).

Questions have been set. We are ready to capture responses.

## Response

A user named "John" responses the two questions with "Yes".

![simple-responses](/media/simple_response.png "Simple Reponses")

\`Timestamp\` is for recording when user responses to a question. Noted that a user can response to a question multiple times. We get the most updated answer by searching for the latest \`Timestamp\`.

## Dynamic Question

If user answers "Yes" to "Do you have any pets?", we would ask him/her a follow-up question - "How many pets do you have?".

![dynamic-question](/media/dynamic_question.png "Dynamic Question")

We introduce the new relationship \`FollowUpBy\` between \`Answer\` and \`Question\`.  If user responses with a specific answer, we will see if that leads to a follow-up question.

Noted that we may need to update the way to find the first question, the last question, and order of questions accordingly. It should be quite straight forward.

Dynamic Questions have been set. Next part would be Versioning.

---
title: Generate a Poem with Google Gemini
description: To use the Google Generative AI model to generate poems in different styles.
prerequisites: JavaScript, React
versions: Node.js 18, Vite 5, React 18
tags:
  - javascript
---

## Introduction

Words, lyrics, music, poetry. Whether it's John Lennon or William Blake, songwriters and poets manage to express feelings that appeal to generations with their writing style. Now imagine if you could combine their styles or even create a new style. In this project tutorial, we will create a poem-generating website using the power of Google Gemini. The poem below changes after a certain number of seconds to always keep you inspired. The best part is that you can customize this completely based on your preferences by the end of this tutorial.

<RoundedImage
  link="https://raw.githubusercontent.com/codedex-io/projects/main/projects/generate-a-poem-with-google-gemini/poem_ai_screen_result.png"
  description="generator demo"
/>
## Get an API Key 🔑

To use the Gemini API, we need an API key. Visit the [Google AI Studio](https://aistudio.google.com/app/apikey), and sign in to a Google account to quickly create a key. 

## Setting Up 🔨

- Initialize your React application using Vite. 

### Initialize Your Server

Now that we have our base React application ready to go, let's initiate our development server!

## Creating the Poem Generator

Let's get started with becoming our very own AI poet! In the **src** folder of our project, create a **PoemBox.jsx** file. Here, we're going to connect to Gemini and generate our poems!

Here, let's also create a variable called `genAI`, and initialize our instance of the model.

## Using Gemini

At this point, our API key should be ready to go! Let's use the current Google generative AI model, `gemini-1.5-flash`. We're then going to:

- Create a prompt that will generate our poem.
- Await a result from the model.
- Generate a response that we'll use to update the state.
- Catch if an error occurs.

### More on Prompting

Like ChapGPT, Google Gemini is made of LLMs that use NLP to interpret and respond to user inputs. LLMs (short for "Large Language Models") are machine learning models that can understand and generate text based on human language patterns. NLP (short for "Natural Language Processing") is the technology that lets models interpret and manipulate human language. Much like any conversation, you have to have good prompts to experience the best results.
Prompting on Gemini is like prompting for any other LLM. Here are some things you should remember as you write your prompt.

💬 **Natural Language:** talk to the language model as if you are giving instructions to a stranger.

- If you want: a poem that rhymes about sunsets
- Prompt for: "write me a sonnet about sunsets in New York"

🎯 **Precise Instructions:** avoid using vague or filler words. (e.g., "like, some, a few")

- If you want: a short poem about tea
- Prompt for: "write me a haiku about earl grey"

😊 **Context:** the more context you provide the more useful Gemini can be.

- If you want: a fish poem in Dr.Seuss style
- Prompt for: "write a poem about fish using an anapestic tetrameter in the style of Dr.Seuss"

🔑 **Keywords:** Gemini works better when specific keywords are used in the prompt.

- If you want: a poem similar to work by Rupi Kaur
- Prompt for: "write me a 10-word poem in the tone of milk and honey by rupi kaur."

## The Timer

We're just a tad bit closer to unlocking your inner AI poet! We want our component to generate a new poem about every 30 seconds!

## Completion

Let's display our poems! ✍️

That's it we just created a `<PoemBox>` component! Don't forget to import it and use the `<PoemBox>` component in the **App.js** file to make it all come together.

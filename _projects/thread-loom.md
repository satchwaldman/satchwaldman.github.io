---
layout: page
title: Thread Loom
description: A dynamic AI conversation environment.
img:
importance: 2
category: personal
status: current
---

### Project: Thread Loom - A Dynamic AI Conversation Environment

__What is Thread Loom?__

Thread Loom is a custom-built, highly interactive chat application designed to serve as a personal thinking and brainstorming partner. Unlike standard, linear AI chatbots, Thread Loom is built on the idea that conversations, ideas, and research are not straight lines. It allows for the organic exploration of topics by enabling users to branch off into infinite "side threads" from any point in a conversation, creating a navigable tree of thought.

At its core, the project is a powerful front-end interface that gives the user unprecedented control over their interactions with large language models (LLMs), focusing on two key areas: __context management__ and __cost transparency__.

__How It Works: The Core Features__

1. __Infinite Conversational Threads:__ The cornerstone of the application. A user can highlight any piece of text—whether their own or the AI's—and instantly create a new, nested "side thread." This allows for deep dives into specific topics, exploring tangents, or asking clarifying questions without derailing the main conversational flow. This creates a hierarchical structure, turning a simple chat log into an organized, explorable knowledge base.

2. __Precision Context Control:__ Thread Loom empowers the user to decide exactly what the AI "remembers" for each response. This is managed in two intuitive ways that can be used together:

   - __The Context Slider:__ A visual slider runs alongside the conversation. By dragging it up or down, the user can dynamically select how much of the recent chat history is included as context for the next prompt. The slider is intelligent, automatically stopping when it reaches the token limit of the selected AI model.
   - __Manual Selection:__ The user can highlight any message from *any* thread in the entire conversation—no matter how old or nested—and manually add it to the context. This allows for a "surgical" approach, enabling the user to pull together disparate ideas from across the chat to ask highly specific, nuanced questions.

3. __Real-Time Cost Tracking:__ To eliminate the financial uncertainty of using powerful AI models, a running tally of the cumulative API call cost is always visible on screen. The application calculates the cost of each individual interaction based on the token usage reported by the AI provider, giving the user complete transparency and control over their spending.

4. __Flexible Model Switching:__ A simple dropdown allows the user to switch between different AI models (e.g., a powerful but expensive model for complex tasks, and a faster, cheaper one for simple queries) on the fly.

__Use Case Examples__

- __Example 1: The Researcher's Companion__ A student is writing a paper on renewable energy. They start a main thread asking for an overview of different energy sources. The AI mentions "geothermal energy." The student, curious, highlights that term and starts a side thread to explore how it works. In that nested thread, the AI discusses "heat pumps." The student starts a *third* nested thread to ask about the efficiency of different heat pump models. In minutes, they have created a clean, organized, and multi-layered research outline, where each thread is a focused exploration of a sub-topic, all while the main conversation remains uncluttered.

- __Example 2: The Creative's Sandbox__ A programmer is brainstorming a new function. They paste their initial code into the main thread. They use the slider to limit the context to just the code and ask the AI to "check for bugs." The AI suggests an improvement. Later, the programmer scrolls up to a much earlier message where they defined a specific data structure. They manually highlight that old message and the AI's recent suggestion, adding both to the context. They then ask, "How can I refactor my function to better incorporate this data structure and your suggested improvement?" By combining specific, non-sequential pieces of information, they get a highly relevant and targeted answer that a standard chatbot could not provide.

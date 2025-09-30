---
layout: page
title: Thread Loom
description: A dynamic AI conversation environment.
img:
importance: 2
category: personal
status: current
---

### Project: Thread Loom

**What is Thread Loom?**

Thread Loom is an interactive chat application designed to serve as a learning and brainstorming partner. Unlike standard, linear AI chatbots, Thread Loom is built on the idea that conversations, ideas, and research are not straight lines. It allows for the organic exploration of topics by enabling users to branch off into infinite "side threads" from any point in a conversation, creating a navigable tree of thought.

At its core, the project is a powerful front-end interface that gives the user control over their interactions with an LLM. For now, it is configured to work either with GPT 5 or GPT 5 Mini.

This frontend relies on API calls to an LLM to function, which can get expensive. To help with this issue, I've implemented **context management** features that allow the user to easily and intuitively customize the context window for each message, as well as **cost transparency** measures so that the user knows exactly how much each query is costing them.

**Features**

1. **Infinite Conversational Threads:** The cornerstone of the application. A user can highlight any piece of text—whether their own or the AI's—and instantly create a new, nested "side thread." This allows for deep dives into specific topics, exploring tangents, or asking clarifying questions without derailing the main conversational flow. This creates a hierarchical structure, turning a simple chat log into an organized, explorable knowledge base.

2. **Precision Context Control:** Thread Loom empowers the user to decide exactly what the AI "remembers" for each response. This is managed in two intuitive ways that can be used together:

   - **Manual Selection:** The user can highlight any message from _any_ thread in the entire conversation—no matter how old or nested—and manually add it to the context. This allows for a "surgical" approach, enabling the user to pull together disparate ideas from across the chat to ask highly specific, nuanced questions.

3. **Real-Time Cost Tracking:** To eliminate the financial uncertainty of using powerful AI models, a running tally of the cumulative API call cost is always visible on screen. The application calculates the cost of each individual interaction based on the token usage reported by the AI provider, giving the user complete transparency and control over their spending.

4. **Flexible Model Switching:** A simple dropdown allows the user to switch between different AI models (e.g., a powerful but expensive model for complex tasks, and a faster, cheaper one for simple queries) on the fly.

**Demonstration Video**

Below is a video walkthrough demonstrating how Thread Loom might be used for understanding the physics behind black holes. The demonstration includes

{% include video.liquid path="assets/video/thread-loom-tutorial.mp4" class="img-fluid rounded z-depth-1" controls=true width="400" %}

**Use Case Examples**

- **Example 1: The Researcher's Companion** A student is writing a paper on renewable energy. They start a main thread asking for an overview of different energy sources. The AI mentions "geothermal energy." The student, curious, highlights that term and starts a side thread to explore how it works. In that nested thread, the AI discusses "heat pumps." The student starts a _third_ nested thread to ask about the efficiency of different heat pump models. In minutes, they have created a clean, organized, and multi-layered research outline, where each thread is a focused exploration of a sub-topic, all while the main conversation remains uncluttered.

- **Example 2: The Creative's Sandbox** A programmer is brainstorming a new function. They paste their initial code into the main thread. They use the slider to limit the context to just the code and ask the AI to "check for bugs." The AI suggests an improvement. Later, the programmer scrolls up to a much earlier message where they defined a specific data structure. They manually highlight that old message and the AI's recent suggestion, adding both to the context. They then ask, "How can I refactor my function to better incorporate this data structure and your suggested improvement?" By combining specific, non-sequential pieces of information, they get a highly relevant and targeted answer that a standard chatbot could not provide.

**New Features To Add**

Here is a non-exhasutive list of some of the features I want to add to this project:

- **The Context Slider:** A visual slider runs alongside the conversation. By dragging it up or down, the user can dynamically select how much of the recent chat history is included as context for the next prompt. The slider is intelligent, automatically stopping when it reaches the token limit of the selected AI model.

- **Move Side Thread Dialog Box:** Currently, the dialog box for each side thread (no matter how many layers deep) is at the top of that thread. I want to move it to the bottom, and have it continually move down with each successive message in that thread.

- **Save Chats:** Chats should be able to be saved and put into renamable, infinitely nesting folders.

- **SSE Stream:** An SSE (Server Sent Event) stream would make the application feel a lot more polished.

- **Formatting:** The application needs more readable formatting (better ability create paragraphs, lists, etc) and it needs to be compatible with LaTex-style formatting.

- **Mutlimedia Support:** Pictures, PDF upload, etc

- **Make Publicly Available:** - Either by open sourcing the code and allowing users to input their own API keys, or by paying for other users API calls myself and using a financing software like Stripe to charge them after the fact.

- **Prompt Waiting Animation:** Only if I can't get SSE Stream working

- **GPT 5-Style "Calling On Different Models":** I want to put in a prompt and have the model know whether it should use GPT 5, Mini, or Nano, whether it should look things up on the web, etc. This might all be built in to the GPT 5 API call, but I suspect web lookup is not built in.

- **Newlines In Prompts:** The user should be able to Shift + Enter to make a newline in the input prompt without sending the prompt.

- **Running Summary:** Another cost-saving measure. Since threads see the full upstream context of their parent message in the main thread only, and by default do not see the context of any other messages in the main thread, it would be useful to create a running summary of each message in the main thread up to the current message in the main thread to avoid having to pay for lots of input tokens when the main thread gets large.

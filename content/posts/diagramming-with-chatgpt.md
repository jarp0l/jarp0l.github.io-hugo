---
title: "Diagramming with ChatGPT"
date: 2023-01-03
tags: ["chatgpt"]
---

## Introduction

ChatGPT cannot embed pictures in conversations, but it is still possible to draw diagrams and charts like flowcharts, sequence diagrams, Gantt charts and many others.

There are tools such as `mermaid.js` (or, just Mermaid) that enable this. Quoting the official introduction about Mermaid:

> ... is a JavaScript based diagramming and charting tool that renders Markdown-inspired text definitions to create and modify diagrams dynamically.

So with Mermaid, you just need to ask ChatGPT to write Mermaid code to draw diagrams. Then copy the code and paste it in [Mermaid Live Editor](https://mermaid.live/), you'll get the diagram.

## Examples

### Example 1 (Sequence diagram)

Example of making HTTP request in js:

> Q: How do I make an HTTP request in Javascript? Explain with diagram in mermaid.js syntax.

ChatGPT:
![ChatGPT prompt for example 1](/images/c7b6e1d52d088513fed7f5b5fff0f255.png)

Code snippet 1:

```md
sequenceDiagram
participant Client
participant Server

Client ->> Server: GET https://api.example.com/endpoint
Server ->> Client: JSON response
```

Code snippet 2:

```md
sequenceDiagram
participant Client
participant Server

Client ->> Server: GET https://api.example.com/endpoint
Server ->> Client: JSON response
Client ->> Client: log data
```

---

Output of snippet 1:
![Sequence diagram of first case which uses XHR](/images/458a68e807ca852e0b00a232f7366d87.png)

Output of snippet 2:
![Sequence diagram of second case which uses the `fetch()` call](/images/e6834e3c5a41a1144afe77284b85f497.png)

### Example 2 (State diagram)

Example of a state machine that represents a light switch with two states: "on" and "off":

```md
stateDiagram
state on
state off

on --> off : flip switch
off --> on : flip switch
on --> off : power outage
```

Output of Example 2:
![example 2 output](/images/85c260adeab3ae45a717f53125ac9cb3.png)

## Conclusion

These are just some examples of making diagrams with ChatGPT (and Mermaid). You can leverage their combination to learn about something, with diagrams. Or you may also want to create diagrams for...your report!

If you want to learn about the capabilities of Mermaid, visit: https://mermaid.js.org/.

---

_Update on 2024-03-13: Updated example 1 with screenshot of ChatGPT's answer, by asking it to repeat its own answer, just for the sake of screenshot._ 😂

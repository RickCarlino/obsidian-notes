**NOTE:** This is my public obsidian notebook and idea bin. The intended audience is software developers.
**UPDATE:** I recently noticed that Jira added a feature that allows users to create JQL queries using an LLM, which is aligned with many of the ideas presented below. I hope other software publishers follow this path.

### Making Everything Programmable By End-Users

One topic in software that's always intrigued me but seems a bit under the radar is the concept of end-user programmable software. This kind of software is typically aimed at users who aren't trained developers, yet it allows them to engage in activities akin to custom coding. The classic example here is the spreadsheet, arguably the most successful tool of this kind, but there are other notable instances as well. Take Scratch, for example, a programming environment that lets kids create animations and games without writing traditional code. Or consider platforms like If This Then That or Zapier. Jira automations fit here, too, I think.

Other applications with scripting capabilities like AutoHotKey or, for those who remember, MIRC or VBA in Microsoft Office, fall into this category as well. These tools are a step up from spreadsheets in complexity but they opened up possibilities for users to extend software like chat clients or office software without needing to be full-fledged programmers.

However, as you make software more flexible for end-users, it can become daunting for beginners. Over time, what starts as a beginner-friendly tool can evolve into something that demands more advanced knowledge. A case in point is SQL, which was originally intended for end users, not just specialized programmers. Over the decades, it has evolved into a tool primarily used by professionals.

Today, with the rise of large language models (LLMs) like ChatGPT, we're seeing new opportunities in this area. These models allow users with minimal coding skills to generate code just by describing what they want in plain text. This potential could further democratize user-driven software customization.
Understanding Plug-In Systems

### Embedded Programming Languages Today

To understand the context better, let’s discuss Lua scripting. Lua is a minimalistic programming language embedded within applications to offer plug-in functionalities. It's not the only scripting language used for this purpose, but it's widely adopted due to its simplicity and effectiveness. If you're unfamiliar with Lua, I recommend exploring some Lua sandboxes available through resources like NPM or RubyGems. These platforms provide a safe environment where users can experiment with extending applications through Lua code.
### Problems With Current Embedded Languages and Plugins

Despite its benefits, using Lua and similar sandboxes to create a plug-in environment has its drawbacks. The most significant is the requirement for users to understand and write Lua code. Moreover, maintaining comprehensive developer documentation for the available functions within the sandbox can be cumbersome.
### An Improved Plugin System for End-Users

Imagine integrating an LLM directly into an application, allowing users to create plug-ins using plain English. The system could generate code automatically and pass it through linting phases to ensure quality and correctness. Furthermore, incorporating a simulator or staging environment would let users test their new plugins before going live.

This approach would make the power of software extension accessible to a broader audience.
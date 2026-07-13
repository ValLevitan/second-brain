---
tags:
  - API
  - automation
  - MCP-model
  - aaron
  - github
  - technical
---

There it goes, okay. So what you just described is the simplest MCP model, which is it's a point-to-point situation where here's your API endpoints, here is the tool exposing the API endpoints literally to the AI. The AI has a basic description of what those endpoints does, and you can tell it to do things within the realm of it has to connect the dots. So if you wanted to get users and find a thing and update a do and whatever, that's the basic integration of it. You can build flows and actions and activities within the MCP to abstract the endpoints. So instead of the AI being just aware of the actual API endpoint, instead you can have a set of things that happen, business logic inside of the MCP. There could be a tool that says, deploy a new machine to an environment or redeploy configuration. Inside of that tool, it's actually calling this endpoint and that and doing all the pieces, the business logic it needs inside of that. Then basically the MCP reports back to the AI, give me these parameters to start with, and then it goes and does the thing, and then it comes back and says, I've done it like this, and it's complete. So you can imagine when we talk about replacing Pavel, the Pavel replacement. So if Pavel has to do these things in order to make it work, we can basically create a logical flow that does that internally, and it tells us every step of the way what it's doing till it comes out to the answer. Then that's the same logic that we bake into an MCP. Now what you have is an AI tool that's orchestrating those actions that Pavel was doing previously. It just so happens that the continuous integration and delivery actions that we use to be able to do things like build software inside of GitHub, follow the same or similar convention of this flow of MCPs. So when we think about we have to do these steps in order to make this happen, that same thought pattern, that same logic applies to MCPs as well. So the closer we get to hands-off automation for all of these things, such as integrating assets, or deploying SQL things, or scaling environments, or configuring Kubernetes, these also apply to MCP servers, and you can start to use these tools in that way. All right. Very powerful. Extremely. I'm going to learn a little more about it. Okay. I hope you're having fun with these things because I sure am.

---

## Audio File Information

- **Source File:** Call_with_Aaron_Bockelie_2025-02-21.m4a
- **Duration:** 3:02
- **Transcribed:** 2025-03-30 13:38:35

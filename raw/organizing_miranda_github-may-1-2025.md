---
tags:
  - organizing
  - meeting-summary
  - project-planning
  - github
  - miranda
  - aaron
---

Okay, we're now recording this. This is on the subject of organizing Miranda. It's the conversation between Aaron and Val, and it sums up the conversation that Aaron had in a meeting with Dmitry Handoff on Tuesday in reference how to organize Miranda 8, which is now completed, and how to run Miranda 9, which is now in process. There are three features that are being worked on almost at the end stage, how to organize it in GitHub, and how to move out the math game emulator out of Miranda 9 and treat it as a separate either repository or separate product. We have not decided yet, and part of this meeting in conjunction with the Tuesday meeting will be to create an action list for Dima to follow and for Aaron and myself, Val, to supervise or to, yeah. Okay, so here's Aaron will sum up or here's Aaron summarizing his meeting with Dmitry while he is outlining an action list for this coming week because the next meeting is scheduled for this coming Tuesday. Thank you. Go ahead, Aaron. Sure, well, you know, for the summary of this transcript, I can also tell you that Teams is now giving summaries of the meetings. It provides the whole transcript conversation, right? I pasted in the meeting chat, that's directly from the meeting, the Teams meeting. I think, yeah, and I think it's somewhat general. Well, the follow-up, that's exactly what I was going to recap, which is that I want him to create gitignore, I want him to purge unnecessary files like logs and libraries, he needs to delete the old still branches. We're referring, are we referring to Miranda 8? No, I'm referring to Miranda. I don't care what version of Miranda it is. I'm saying that the only place, there's only one repo for Miranda. Miranda 8 is just a version of it. Miranda 9 is coming around the corner that includes this emulator capability that he needs to weave into it somehow. Well, and there's no way that we can solve all of it at once, because he has quite a bit of ground to cover in making this thing make sense. And so I said before you can even consider wrapping the packet or the emulator simulator portion of Miranda back into Miranda, you need to start with the basics, which is set a gitignore, ignore the logs and libraries, purge them out of the repo, get rid of the old branches, come up with a basic packaging strategy, like a zip file that can zip with the libraries during the commit of a new version of Miranda. And with that, he has the basics to be able to start a new feature branch for the simulator integration back into Miranda to bring that text into that. Are you sure that he understood what's being asked of him? Well, he certainly nodded his head and said, yes, I understand. I will do these things. Whether he actually truly understood me or not. You know, when you talk to somebody who doesn't really understand your language, and they kind of nod your head in agreement, even though you realize that they didn't really understand you. I kind of got a little bit of that from him. But once again, like I said, it's the twitchy part. I'm not sure. I think he got more than that. Let me turn this recording off.

---

## Audio File Information

- **Source File:** organizing_miranda_github-may-1-2025.m4a
- **Duration:** 4:45
- **Transcribed:** 2025-05-02 15:20:37

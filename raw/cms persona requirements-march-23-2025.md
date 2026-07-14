---
tags:
  - meeting
  - cms
  - personas
  - pavel
  - juan
  - aaron
  - andrei
  - val
---

# CMS Persona Requirements Meeting - March 23, 2025

## Meeting Transcript

Perhaps we do not understand how we should come to the requirements. I sent you a letter that we discussed with our local group and made the requirements for two persons, for Pavel and for Juan. Maybe as an example of them it would be possible to understand where we are moving, why we are moving in this situation.

I am saying that I feel that there might be misalignment in how we get there. I don't know how we are moving in that direction yet. Aaron and I are not used to working with the two of you on a one on one basis.

So we might be not understanding each other simply because maybe we are using wrong taxonomy or wrong terms. But it doesn't mean that we cannot work with one another. We just need to get used to one another.

I am not saying that you don't understand something. I am saying that for sure I don't understand what you are doing. That's what I am saying.

So, again, the description, I specifically, well, Aaron specifically demanded that the personas to be described neutral. They are neutral. They are not specific to any of the products.

Personas, they are who they are. The next thing that I would suggest we do is we look at what current CMS does. Because we know what it is.

So we know who the personas are. I am not saying that each persona may necessarily have anything to do with the current CMS. Maybe nothing, I don't know.

But we know who the people are. Who the personas are. And we know what current CMS does.

And there is even a block diagram of the current CMS. In preparation for today's meeting, I made it a little bit easier. I took a stab at describing what the current CMS does.

And I placed this description into GitHub. Please tell me that you have access to it. And if you don't, I can give you access to it.

It's here. Let me put it in chat. Okay.

I'm going to invite Andre to this meeting, too. I think it's important for him. Hello.

Is this a temporary Git repo for now, Val? I didn't plan this to be a temporary, but why do you say it's temporary? I think that we should probably consider, let's just use this as is for now. We shouldn't have a Git repo called understandings in it probably like that. Well, this is within knowledge base, right? Yeah.

I would rather we just have one called CMS. Sure. Happy to change it.

Sure. Andre, can you change the name of understanding CMS to CMS in Git repo, please? Thank you very much. I appreciate it.

So, in this repo, we have CMS legacy blog diagram. It's in the form of a picture. I copied and pasted from the whiteboard.

This is what Dima, you produced it. So, I just took what you produced. I used AI to describe the current CMS of what it is.

I'm not suggesting that this is the correct description. By all means, let's change the description as you wish or as needed. I'm doing it for the first time.

There is a markdown file there. Why don't you take 5 minutes, Sergey Tsymanov and Dima, please read the description and tell me if it's described properly. Let's take 5 minutes.

Any comments? You need more time? I think it's enough for a general understanding. The rest is already done. I'm not going to go into details.

It's already decided. for each persona. And that will give me at least 60% of truth.

And then, if I'm an engineer, I can probably think of other requirements. That's how I would short fuse the next step. And when I have requirements and when I have description of CMS, I could probably create a set of features for the current CMS.

And set of capabilities using AI. And I would probably get to about 60% truth. And then, if I'm an engineer who understands what it is, I could probably polish it to about 80% truth.

And at 80% truth, I wouldn't try to perfect it any further. I would just leave it the way it is. I'm speaking English because I understand that you speak English.

Dima and Sergey, you speak English. I mean, you understand English. And I'm speaking English for the benefit of Aaron.

So, all of us kind of... We understand what's happening. I invited Andrej because he understands more or less everything. That we're discussing and when I hang up with you, the three of you could get together and discuss it again.

So, unless... Excuse me, let me just finish. I'm sorry, Dima, I apologize. Unless Aaron has a radically different proposal from what I just said, then I would like to define it as your homework.

Look at what CMS does. Look at the neutral personas. There is about JVL, what company does.

And create requirements, features and capabilities of the current CMS. If it's at 80% accuracy, I wouldn't strive for perfection. I would park it and then I would start working on the architecture of the new orchestration platform.

Aaron, the floor is yours. Sure. So, I want you to notice the significant amount of... I don't know, use of AI tools right now that Val is using to do some analysis and develop initial ideas for the tool.

I am not telling you you need to do that. But what I am telling you is that it goes much faster when we do. And what I don't want you to do is to have to do two different difficult tasks simultaneously.

One, learn how to use a set of tools to do analysis based on an AI tool. And two, also describe CMS in its functional pieces and how it is supposed to be responding to customer requirements. So, I kind of am going to ask you guys, what do you want to do? How are you going to accomplish the demand that Val is asking for? I just want to talk about it.

We have a description of our company, what it is doing. There is a person described in terms of stylistics, what this person is doing now. There was a request made through AI to make a set of functional and non-functional requirements for the existing system.

Okay, go on. You have already published it somewhere. So, let's get to it.

Let's do it. Okay, let's do it. I have to say that he and Sergey do this job.

They create some requirements, use the persons and use the about company information. And he creates some, uses the requirements, he starts to create some functional or non-functional requirements. And Dima places these requirements on this link, you can see it on the chat.

The second step was to look at what AI offered us. And we made some adjustments based on what we have. What could have been improved, for example.

Let's do it. We need about 80% of the work and 20% of the editing. So, I appreciate the effort on the first try, but we need to do it again.

I'll start with that. The reason we need to do it again is that these personas are talking about a very specific product now. And the problem is that we can't do that.

What happens when we have the orchestration platform role and product requirements with Pavel as engineering director for some other product that's not orchestration platform? So, what you've done is you've co-mingled, you've mixed it up two things. The persona and the use case or the user journey. There's two pieces to this.

There's the persona, Pavel, who he is, what he does, how he is as a person, how he consumes the tool. And you're overthinking that part of it. Either you're letting the AI overthink it for you as you're letting it write this, or you are overthinking it.

I'm not sure which, can't tell. The other piece of this, distinct from the persona, a separate thought, is the use case, user journey, for that persona. So, imagine we have personas.

Pavel, Marta, Juan, Afim, Andre, and so forth, okay? These descriptions of these personas. They are universal. I could apply this persona to any product JBL uses, and it will never have a reference to any products that JBL actually operates.

Second, you have your product, CMS. CMS may borrow some of these personas from the persona library or make a copy of them. And when you then create a use case or a user journey for that persona, then you're going to apply your requirements and uses for your product.

That's the distinction and difference. What's happened here is that now you've mingled the CMS product with the persona. It's not reusable now.

Do you need to translate that? Yes, please. When he created these requirements, he did not say to us that we have CMS now. He said to us only that we have a product as a slot machine.

We have some personas, and we want to start developing something, an orchestration platform. Which needs to be useful for these personas. He did not say that we have current CMS.

I'm just reading what I see. Let me show you. When Pavel goes to work for the day, I'm assuming he gets in his car or gets on the train or whatever, rides a bike to work to the office.

Is he thinking about seamless integration between hardware and software components all the time? Is he worried about flexible updates? Who is Pavel? There's some good stuff in here, but there's some other stuff that's really weird. Dima says that we created this person together, and we need to start working with this person. So these key quotes are nice, but why is there an abstraction where it's critical? Let's update the software.

I know where this is coming from. You guys started with a thing talking about CMS updating systems, and then you rolled the pasta into something that is talking about this. I've done this enough to read into this.

The problem is that you're almost there, but I don't think the comprehension is totally here. I'm concerned about the way this persona is written. This doesn't help.

It has a very distinct set of assumptions baked right into it that we can't have. Personas are about the person, not about how they approach the work. So this is almost there.

Once you have a persona that makes sense, then you can go from there and build the remainder of it, which doesn't affect the persona. The persona is like a model. It's like a simulation of your customer.

You can't cause the customer simulation to want a specific thing on your product. If you do that, you've tainted the simulation. I'm trying to come up with a way to describe this, because this is an unusual direction, I think, that's being caused by the ease of writing personas right now with AI.

What's going on is that you're allowing it to take it in a direction that you're not completely comprehending. I've never seen this before. I read it before, and I didn't understand what it was.

It's a mix of a lot of different things. Like, what if we just wrote this without any sort of... And also it's written as a requirement for a new orchestration platform. Right.

And I don't want to write about a new orchestration platform. We're not designing a new orchestration platform. What you are doing right now, you're moving an existing CMS onto GitHub.

That's what you're doing. And I would like to organize our GitHub repositories based on the features of the current CMS. And I think there is a misunderstanding of the scope of what needs to be done.

Do you understand, or should I say it in Russian? I can say it in Russian. I would probably say it with clarification, if I may. I understand the words, but I don't quite grasp the essence of your words.

I was talking to Pavel today. Pavel told me that in this Sprint, which started today, it is planned to move... I forgot the name of this mod. I think it's called Prototype or something.

Yes, it's a work with one of the artifacts. What is it called? Protohost, it's a library. Protohost.

To move Protohost onto GitHub. Now it's on... On SVN. Now it's on SVN, and the task in this Sprint is to move it onto GitHub.

I asked why we're doing this, why we're moving it onto GitHub. Because the decision was to organize today's CMS on GitHub. When we organize the structure of GitHub, it is very important to organize it according to the current features.

Because we work with features, if we want to do something. If you imagine how you will organize it, how you will organize the repositories of today's CMS, I would like to organize them in such a way that they represent the feature branches. In order to get to the features, features are written against requirements.

No one needs a feature if there are no requirements for it. Unfortunately, but as usual, we start from the middle. We're starting from the middle because we are discussing a legacy product.

We are discussing a product that has been around for many years. We are trying to organize it, to make it a logical beginning of something. Am I wrong in something, or did I say everything right? It's right.

Well, okay. So we have a point of... How is it called in Russian? Contact. Once again.

We have a system in SVN, a platform that we call CMS. We transfer this CMS in parts to GitHub. GitHub is organized, repositories are organized according to feature branches.

Features cannot exist in a vacuum if there are no requirements for them. One of the questions we should ask ourselves is why we are doing something. Why are we doing this feature? The answer should be this.

We are doing this feature because here is a set of requirements that require the execution of this feature. Do we agree with this or not? It's hard for me to read faces. Yes, yes, yes.

Okay, good. Okay, good. Expecting this today's fact, I started pushing the creation of features to today's CMS.

By today's CMS, I mean CMS that has existed for 30 years. Or 20 years. I'm sorry that we are starting this from the end.

By the way, we will not do this perfectly, but we will do it so that it is enough. Enough. When organizing a repository, we need features.

Features need to be tied to requirements. Requirements. I help you write requirements.

If we know the person, we will know the architecture of our product, it will be easier for us to create features on it. I'm bluffing. I'm bluffing.

At least I'm bluffing in a product that has existed for decades. And we start from the end and it's easier for us to bluff. Is the approach clear? Yes, it's clear.

---

*Note: This file is a transcript from TurboScribe.ai. The original transcript noted it was longer than 30 minutes and suggested going Unlimited at TurboScribe.ai to transcribe files up to 10 hours long.*

**Aaron_Val-release_procedure_GitHub-March-16-2026-20260316_080709-Meeting Recording**

16 March 2026, 12:07pm

7m 35s

**\
Val Levitan** started transcription

**\
Val Levitan** 0:04\
OK, so um.\
Um.\
You may recall that we created a patch that never really worked for us in Jira for releases and the attempt was to create the ISO related project.

**\
Aaron Bockelie** 0:22\
Right.

**\
Val Levitan** 0:26\
That would create an ISO and Ivan was managing that and putting tasks, attaching them to an IP.

**\
Aaron Bockelie** 0:37\
Yes.

**\
Val Levitan** 0:39\
Eventually, at some point I remember complaining to you that really doesn\'t work and you said yeah, probably it will not work because it\'s not how it\'s done. And when at some point when you convert to GitHub, the releases should be done in GitHub.

**\
Aaron Bockelie** 0:58\
Yes.

**\
Val Levitan** 0:59\
And at that point I already made commitment to GitHub and we started to focus on GitHub and I said to myself, OK, you know what? I\'m not going to bother with trying to make something work.\
In JIRA, if it\'s not a perfect solution and that ISO thing hung in there for.\
All this time and it\'s there now and it\'s not administered correctly and it\'s just polluting Jira right now. So number one, if you could dictate a course of action that Dima should take to disable that.

**\
Aaron Bockelie** 1:32\
Right.

**\
Val Levitan** 1:42\
Madness. I\'d rather not have it in JIRA. That\'s number one. And #2 as you dictating instructions to JIRA, maybe you could.\
Discuss how it how it should be managed, supervised in GitHub so we know what to focus on. Yeah, so maybe take, I don\'t know, 1015 minutes just to talk it through and I\'ll remain.

**\
Aaron Bockelie** 2:03\
Right. Yep.\
Yeah.

**\
Val Levitan** 2:11\
Quiet. Your focus should be on giving instructions to Dima and Andrei on how you want it to be restructured. So then I could take this transcript and turn it into.

**\
Aaron Bockelie** 2:14\
Hmm.\
Right.

**\
Val Levitan** 2:27\
Uh, certain guidance for DMA and Andrei.

**\
Aaron Bockelie** 2:33\
Yeah, so first of all, the natural instinct is to just delete the ISO issue type and be done. However, you probably don\'t want to do that right away just because some sort of information in there.\
Was helpful. So what we want to do instead is export all the ISO issue types out. We can dump them out and what that does is it lets us understand all the call, all the relationships, you know they\'re.\
Connected issues and things like that, because that becomes a data source that we can use to clean up and populate into GitHub directly.\
GitHub well yet allows you to just tag any repo however you\'d like with a version number and so if we have an existing version versioning system.\
Where we have been tagging anything with an ISO item into a.\
From a git repo rather than an SVN repo. So basically we have two repo. I\'m I\'m progressively revealing how the insanity is here. We came from SVN. The tagging process for versioning was just an SVN and however they did it.\
We then discussed how to start tagging versions a little more. Um.\
Realistically with patch minor major version numbers and then there was all the other version numbering that got mashed together into things. So this bundling of things is what eventually becomes ISO versioning numbers and ISO release items.\
So what we need to do is dump all the ISO items, ask Ivan in the QA team and basically go what of these items are actually the front leading edge of things right now? What is the leading edge plus the last couple things that are important?\
And what we can then do is that we we dump it out, we ask that question, then we go look at GitHub and go of all of the repositories that we have, which ones are actually referenceable in this list?\
I\'m going to assume that there\'s going to be a bunch of items that are not referenceable because people have not moved off of SVN yet fully. So what we can then do is we can ignore the SVN stuff, just like we\'ve discussed before. We leave that stuff to die, just let it walk past it, you know, and then what we can.\
Basically do is create releases in git for the repos that match. When we have those release items, we release tags in git. That\'s the source of truth. Git is our source of truth. So GitHub gets these release version numbers.\
Tagged to a specific commit, and if Ivan can\'t provably say it\'s this version number or this version hash in git is our release, then don\'t worry about it. We\'re actually going to just not try that hard to try to do the discovery for this. The only places where we really need to.\
Discovery is where we\'ve handed off a specific version for validation or to customers or things like that, and those ones we should be identifying specifically in Git.\
I think that\'s OK to also admit that actually we have no idea where it\'s at and we better just start figuring it out from this point forward so we can use that same ISO list and release list to instead just form an opinion on what we should be looking for to tag and get as this is close.\
So no.\
I just think that there\'s going to be a lot of confusion about what is considered really a release at this point with what\'s in GitHub versus what actually was mentioned in by Ivan.\
O in summary.\
Dump all the ISO issue types, get all the properties for their issues. Work with Ivan to identify out of that list what makes sense. Go find the ones that we can find in GitHub.\
Tag the prod the repos in GitHub. Discard everything else.\
Then delete all the ISO issue types from JIRA and delete the ISO issue type.

**\
Val Levitan** 7:01\
OK.\
Understood. I I think it gives me, not me, but I think it gives the team enough substance to prepare ourselves for the next meeting and I think we\'re going to conduct a series of these meetings until we move away from tracking releases.

**\
Aaron Bockelie** 7:26\
Yeah.\
Yep.

**\
Val Levitan** stopped transcription

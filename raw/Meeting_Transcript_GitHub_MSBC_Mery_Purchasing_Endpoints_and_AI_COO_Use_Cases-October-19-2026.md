# Raw Transcript — GitHub-MSBC integration and supplier migration – Val, Genadi, Nathan
**Date:** October 19, 2026, 5:36 PM – 5:50 PM Eastern (Segment 2 of 2)
**Summary note:** [[Meeting_Notes_GitHub_MSBC_Mery_Purchasing_Endpoints_and_AI_COO_Use_Cases-October-19-2026]]
---
WEBVTT

00:00:03.109 --> 00:00:08.349
<v Val Levitan>What we would like to achieve here is to give Mery, who is not as...</v>

00:00:09.429 --> 00:00:27.549
<v Val Levitan>Proficient with engineering. She's not an engineer. Michael is an engineer. So, because she is not an engineer, she needs an administrational tool or administrational environment. I'm gonna call it administration environment. We have a tool. The tool is...</v>

00:00:29.309 --> 00:00:30.429
<v Val Levitan>Business Central.</v>

00:00:31.509 --> 00:00:45.469
<v Val Levitan>But we don't have the environment created within this tool that allows Mery for easy use or easy access. So it will take us a little bit of time, but...</v>

00:00:47.069 --> 00:00:48.429
<v Val Levitan>For Mery to have.</v>

00:00:49.549 --> 00:00:55.229
<v Val Levitan>proper information coming out of Business Central, a couple of things need to happen. First of all...</v>

00:00:56.749 --> 00:01:01.629
<v Val Levitan>We need to move away from building specialized reports.</v>

00:01:02.829 --> 00:01:17.589
<v Val Levitan>It has to be done through a multi-contextual protocol. It has to be, she has to be able to write in Spanish or English and get an answer.</v>

00:01:17.429 --> 00:01:17.549
<v Nathan Carver>Yeah.</v>

00:01:20.589 --> 00:01:31.149
<v Val Levitan>So, you need to advance your Msbc when it comes to inventory control to cover all end to end.</v>

00:01:32.989 --> 00:01:33.709
<v Val Levitan>Um...</v>

00:01:36.829 --> 00:01:39.389
<v Val Levitan>API points, so you could get...</v>

00:01:42.029 --> 00:01:46.589
<v Val Levitan>more information out of it. Right now I believe it's limited. Correct me if I'm wrong, Nathan.</v>

00:01:51.389 --> 00:01:52.349
<v Nathan Carver>No, I think that's right.</v>

00:01:56.269 --> 00:02:02.189
<v Val Levitan>Can you, and so that's one aspect. The second aspect is...</v>

00:02:03.949 --> 00:02:05.229
<v Val Levitan>We have to...</v>

00:02:07.229 --> 00:02:16.189
<v Val Levitan>Attend to number one, physical count of parts. And #2, I believe we need to get to.</v>

00:02:17.869 --> 00:02:18.349
<v Val Levitan>Um...</v>

00:02:32.109 --> 00:02:33.949
<v Val Levitan>We need to have an ability.</v>

00:02:35.469 --> 00:02:36.909
<v Val Levitan>To get shortages.</v>

00:02:38.109 --> 00:02:40.509
<v Val Levitan>In order for us to get shortages.</v>

00:02:41.389 --> 00:02:48.109
<v Val Levitan>We need to enter administrational data per vendor correctly.</v>

00:02:49.549 --> 00:02:58.669
<v Val Levitan>Administrational data also depends on certain processes that we need to implement.</v>

00:02:59.549 --> 00:03:09.069
<v Val Levitan>how we manage invoicing. So purchase orders and purchase invoices. And I don't know exactly the flow of it.</v>

00:03:10.149 --> 00:03:20.189
<v Val Levitan>So I need to meet with Lev and get him to explain to me the flow of payment and administering purchase invoices.</v>

00:03:24.589 --> 00:03:25.069
<v Genadi Peari>Can I?</v>

00:03:25.629 --> 00:03:26.029
<v Val Levitan>Sure.</v>

00:03:26.749 --> 00:03:44.189
<v Genadi Peari>I think what you just said, we need to decide because there are two, exactly 2 parts. There is a material requirements report, what it was before, but it may be improved or with different, I mean, but</v>

00:03:45.469 --> 00:03:57.229
<v Genadi Peari>The the the the bottom line, it's very similar, what what and it's already for sure we have everything for that, no no issues, you we can get this.</v>

00:03:56.189 --> 00:03:57.149
<v Val Levitan>We have an issue.</v>

00:03:58.309 --> 00:03:59.469
<v Val Levitan>We, we, we have.</v>

00:03:58.349 --> 00:04:04.589
<v Genadi Peari>We have issues that not exact count on the Msbc, but we have all the data.</v>

00:04:03.229 --> 00:04:07.229
<v Val Levitan>No, no, no, we don't have all the data.</v>

00:04:09.069 --> 00:04:21.309
<v Val Levitan>The count is more or less okay now. Like we don't have too much discrepancies. The count is more or less okay. What we don't have, we don't treat.</v>

00:04:22.829 --> 00:04:24.829
<v Val Levitan>Purchase invoices correctly.</v>

00:04:26.029 --> 00:04:37.949
<v Genadi Peari>This is for me second the PTO management. This is second part of this report. It can be combined together as one big data.</v>

00:04:39.309 --> 00:04:45.709
<v Genadi Peari>But, yes, there we were not were missing fields there.</v>

00:04:46.829 --> 00:05:02.909
<v Val Levitan>It's not the fields. We, for example, we issue a purchase order. Purchase order goes to the vendor. The vendor says, okay, I am going to start building it, but make sure you give me a prepayment.</v>

00:05:03.709 --> 00:05:23.749
<v Val Levitan>It takes us time to administer the prepayment and we don't know when the prepayment is left because it doesn't, right now our process, it doesn't register against the invoices. But even if we make it, even if we make it register against the invoices, then there is another process. The vendor says, I'm ready.</v>

00:05:15.149 --> 00:05:16.749
<v Genadi Peari>Exactly, this is what I meant.</v>

00:05:23.949 --> 00:05:31.549
<v Val Levitan>I'm shipping. Right now all of this is verbal. Verbal emails between Michael and the vendor.</v>

00:05:32.429 --> 00:05:37.789
<v Val Levitan>It cannot work like this. Our system needs to know that vendor has shipped.</v>

00:05:39.069 --> 00:05:40.429
<v Genadi Peari>Yes, exactly.</v>

00:05:39.389 --> 00:05:50.989
<v Val Levitan>So we know, we know that it will be on the boat for, let's say, 25 days and then by truck another 15 days. Here's 40 days lead time until we expect the shipment to come in.</v>

00:05:53.149 --> 00:05:54.909
<v Genadi Peari>Yes, all the steps.</v>

00:05:53.389 --> 00:05:55.309
<v Val Levitan>Without these milestones.</v>

00:05:55.789 --> 00:06:08.149
<v Genadi Peari>All the steps needs to be confirmed: PTO, PO approval, PO deposit, invoicing, payment, shipping, lead time, blah blah blah.</v>

00:06:04.429 --> 00:06:04.829
<v Val Levitan>Val.</v>

00:06:07.149 --> 00:06:19.069
<v Val Levitan>And in order for all of this to work, that loop to work, number one, we need to have the loop. Number 2, we need, which is, I call it, AICOO.</v>

00:06:20.029 --> 00:06:31.709
<v Val Levitan>Chief Operating Officer who can, who is an agent that has an agent that scans through Business Central.</v>

00:06:33.389 --> 00:06:34.989
<v Val Levitan>and get the reports.</v>

00:06:36.589 --> 00:06:50.349
<v Val Levitan>or gets, not even the report says, hey, we didn't make a payment, or hey, we didn't get a advice from the supplier that he shipped, and he should have.</v>

00:06:51.149 --> 00:07:09.989
<v Val Levitan>So all of these deficiencies we can catch, but then full loop, what they started with, Nathan, it means that, and I'm assuming these end-to-end points are available within the API, we need to integrate this form of a query.</v>

00:07:10.989 --> 00:07:16.829
<v Val Levitan>Into Msbc, so we could, through multi-contextual protocol, we can ask that question.</v>

00:07:19.629 --> 00:07:25.309
<v Val Levitan>So, I need, I need more, I need more end-to-end points integrated into the Msbc.</v>

00:07:19.869 --> 00:07:20.669
<v Genadi Peari>And also...</v>

00:07:20.029 --> 00:07:20.349
<v Nathan Carver>Okay.</v>

00:07:27.069 --> 00:07:40.909
<v Genadi Peari>And for these points, which are questionable, it will also search the emails and put information from the e-mail to responses of the vendor for this particular line.</v>

00:07:36.349 --> 00:07:36.989
<v Val Levitan>Of course.</v>

00:07:39.789 --> 00:07:40.429
<v Val Levitan>Of course.</v>

00:07:41.389 --> 00:07:42.149
<v Val Levitan>Of course.</v>

00:07:42.589 --> 00:07:54.189
<v Genadi Peari>Remember, Mikhail was asking you, oh, I want my notes to be solid, note unchanged. So these notes basically needed to be taken from the emails.</v>

00:07:54.989 --> 00:07:55.709
<v Val Levitan>Of course.</v>

00:07:58.269 --> 00:08:03.629
<v Genadi Peari>So, we need to structure this this report to see what we have, what we don't.</v>

00:08:02.429 --> 00:08:14.429
<v Val Levitan>That that is that is very easy. We could have AI CO traversing through emails and traversing through.</v>

00:08:19.389 --> 00:08:25.149
<v Val Levitan>Msbc, because that's that's the your source of truth, that's the factual information.</v>

00:08:28.389 --> 00:08:30.189
<v Val Levitan>And provide us with the guidance.</v>

00:08:32.669 --> 00:08:44.029
<v Genadi Peari>So for this report, we don't have much time because she needs to start working very fast. So we need to start somehow, maybe.</v>

00:08:44.589 --> 00:08:44.669
<v Nathan Carver>The.</v>

00:08:45.229 --> 00:08:51.629
<v Genadi Peari>Maybe, well, to do some preliminary like tool or I don't know, but we can.</v>

00:08:50.909 --> 00:08:56.429
<v Val Levitan>It's not a tool. Nathan needs to add more endpoints.</v>

00:09:00.749 --> 00:09:04.909
<v Val Levitan>needs to include more endpoints inside of his Msbc.</v>

00:09:08.269 --> 00:09:11.709
<v Val Levitan>Based on this conversation, I will ask Claude.</v>

00:09:08.429 --> 00:09:08.989
<v Nathan Carver>Okay.</v>

00:09:12.909 --> 00:09:14.429
<v Val Levitan>To create.</v>

00:09:19.629 --> 00:09:33.869
<v Val Levitan>create a set of use cases for AI hyphen CO, AI based Chief Operating Officer, as a controlling character, as a controlling persona.</v>

00:09:35.309 --> 00:09:36.269
<v Val Levitan>Ohh.</v>

00:09:37.389 --> 00:09:45.229
<v Val Levitan>In tracking. All of the actions associated with. Material management.</v>

00:09:48.269 --> 00:09:51.549
<v Val Levitan>This will be my undertaking. I can do it right now.</v>

00:09:50.909 --> 00:09:52.589
<v Nathan Carver>Okay, that'll be helpful.</v>

00:09:54.509 --> 00:10:05.469
<v Val Levitan>I will create a set of use cases, maybe not all of them. Maybe I will create 5, 10, three, I don't know, but it will be a start. And then as we...</v>

00:10:06.509 --> 00:10:10.509
<v Val Levitan>Run into issues, we will create additional use cases.</v>

00:10:11.589 --> 00:10:16.109
<v Val Levitan>From use cases, we create more capabilities, pass it on to Nathan.</v>

00:10:21.469 --> 00:10:27.389
<v Val Levitan>And Nathan will add additional endpoints into the Msbc.</v>

00:10:28.189 --> 00:10:29.389
<v Val Levitan>Correct, Nathan, delay.</v>

00:10:29.869 --> 00:10:33.469
<v Nathan Carver>Yes. Sounds good to me. Yep.</v>

00:10:30.949 --> 00:10:32.429
<v Val Levitan>Did I get it correctly?</v>

00:10:35.749 --> 00:10:46.989
<v Val Levitan>So that part I know how to do. I will get on it today. You will get use cases later today. They will not be perfect. They will not be polished, but it will be first thing.</v>

00:10:39.869 --> 00:10:40.189
<v Nathan Carver>But...</v>

00:10:49.389 --> 00:10:56.429
<v Val Levitan>And then the three of us, I'm not, I'm gonna try to create maybe 10 use cases, maximum, maximum.</v>

00:10:50.069 --> 00:10:50.269
<v Nathan Carver>Okay.</v>

00:10:57.549 --> 00:11:08.829
<v Val Levitan>But that will give us, read those use cases and see if it makes sense because maybe I'm, you know, not catching something.</v>

00:11:15.869 --> 00:11:19.389
<v Nathan Carver>Yeah, that will be helpful. Send me those, we'll review them, and we should be good.</v>

00:11:24.029 --> 00:11:32.429
<v Val Levitan>OK, and you Genadi, after repositories are created, you need to start putting the clean.</v>

00:11:35.389 --> 00:11:43.149
<v Val Levitan>Clean data, either drawings or data sheets, whatever the supplier provides you, the engineering stuff.</v>

00:11:38.669 --> 00:11:39.149
<v Genadi Peari>Yes.</v>

00:11:43.789 --> 00:11:44.269
<v Genadi Peari>Yes.</v>

00:11:44.789 --> 00:11:49.229
<v Val Levitan>proper connectors on the monitors, whatever resolution you agree to.</v>

00:11:51.869 --> 00:11:53.629
<v Genadi Peari>Yes, this is good.</v>

00:11:52.909 --> 00:11:58.029
<v Val Levitan>And if it's in your emails and you're looking how to get it out of your emails.</v>

00:12:00.349 --> 00:12:04.749
<v Val Levitan>We can, we can set up an agent to to go through your emails.</v>

00:12:06.749 --> 00:12:07.149
<v Genadi Peari>Yeah.</v>

00:12:08.189 --> 00:12:08.749
<v Genadi Peari>Understood.</v>

00:12:09.549 --> 00:12:17.309
<v Val Levitan>Okay, I think we discussed enough. We have our undertakings. Can we try to achieve something by Wednesday, please?</v>

00:12:19.149 --> 00:12:20.509
<v Nathan Carver>Yep, absolutely.</v>

00:12:20.349 --> 00:12:28.989
<v Val Levitan>Okay, can I line up the next call approximately the same time at around 5:00, 4 or 5:00 on Wednesday?</v>

00:12:31.069 --> 00:12:31.549
<v Nathan Carver>And.</v>

00:12:31.189 --> 00:12:32.269
<v Val Levitan>Are you guys available?</v>

00:12:33.549 --> 00:12:35.069
<v Nathan Carver>Yes, I'm available.</v>

00:12:36.029 --> 00:12:37.869
<v Val Levitan>Okay, I'll send an invite.</v>

00:12:38.749 --> 00:12:39.789
<v Val Levitan>An invitation.</v>

00:12:40.909 --> 00:12:43.469
<v Val Levitan>Thank you, everyone. Anybody has questions?</v>

00:12:42.269 --> 00:12:50.269
<v Genadi Peari>Nathan, Nathan, but if we have repositories tomorrow, I could, can I have you for 15 minutes tomorrow?</v>

00:12:51.069 --> 00:12:51.989
<v Nathan Carver>Yes, yeah.</v>

00:12:51.789 --> 00:12:53.709
<v Genadi Peari>Just to just to go through this.</v>

00:12:55.309 --> 00:12:57.469
<v Genadi Peari>How to, how to do?</v>

00:12:58.349 --> 00:12:59.789
<v Genadi Peari>For, for an example.</v>

00:12:59.389 --> 00:13:17.469
<v Val Levitan>So I suggest, I suggest that tomorrow you have this meeting in the morning and you include Andrei into it. Andrei is very clever. He knows what to do. And if he understands what we're trying to do, Genadi, he will form it, not form it. He will.</v>

00:13:17.949 --> 00:13:26.029
<v Val Levitan>configure it exactly how you want it. And he will, Andrei writes Github actions.</v>

00:13:28.669 --> 00:13:33.389
<v Genadi Peari>If you're not ready morning, tell me when you when you're ready, so I can.</v>

00:13:34.589 --> 00:13:36.269
<v Genadi Peari>Any, anytime, so...</v>

00:13:35.949 --> 00:13:37.229
<v Val Levitan>But Andrew is a Minsk.</v>

00:13:38.189 --> 00:13:38.669
<v Nathan Carver>Okay.</v>

00:13:40.349 --> 00:13:40.829
<v Nathan Carver>All right.</v>

00:13:41.309 --> 00:13:41.869
<v Genadi Peari>Thank you.</v>

00:13:42.989 --> 00:13:44.509
<v Nathan Carver>Sounds good. Thank you all.</v>

00:13:44.589 --> 00:13:45.149
<v Genadi Peari>Thank you.</v>

00:13:45.949 --> 00:13:46.909
<v Val Levitan>Thank you. Bye-bye.</v>


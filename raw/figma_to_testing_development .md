**Transcript**

19 August 2025, 12:02pm

**Val Levitan** 0:03  
Good morning everyone. I am very excited to talk about.

**Irina Shishko** 0:06  
Oh.

**Val Levitan** 0:09  
Or at least understand more about how we can design in Figma.  
And move our development to.  
An executable program and incorporate testing into it. So it's a learning process for me, the initial discovery for me.  
Was done last week in the meeting with Aaron who suggested why don't we do it certain way and we left this week for Igor to dig more into it.  
And I think that's the objective. This is what we want to discuss, how we can do that and what do we need to do for that.  
Yes, am I correct?

**Irina Shishko** 1:10  
Yes.

**Ihar Hrybko** 1:12  
Yeah, I'm from my side. I'm only know about usability testing so we can use mockups to.  
Test user flow. It's like we have an interactive prototype with some buttons and panels and users can click on the button and go.  
Go to another page and we can understand how how users can go back to to main page. So this is usability testing.  
For testing like integrate Figma and React application, I don't think we we can do it because it's so different.  
Tools and we can. I think we can test our design system like colors, buttons, some names.  
And we cannot test the business logic.  
So this is my research.  
No.  
On this topic to integrate Figma somehow.  
So basically we.  
For we definitely can to usability test.  
With focus groups, with with different groups of users, but we cannot just test our main functionality of our application because.  
I am basically creating a screenshots kind of screenshots so it's completely static and if user presses a button under the hood in our application can happen a lot of things.  
And we need to test this math, some business logic. We cannot do it from Figma, obviously.

**Aaron Bockelie** 4:18  
What does everybody else think of that?

**Anton Leshkevich** 4:21  
I actually agree because like yesterday I did a little researching tool. I think it's called Maze, right? Yeah, it's like it's I asked AI to summarize and the summarization was like it's a very good tool.  
To test your designs before writing any code. So yeah, like usability testing or like maybe show your manager that like the design that you have created works, but it's not like taking.  
Ready and deployed application and matching it against existing mockups or existing pigma file. It like the tool is not for that.

**Aaron Bockelie** 5:06  
So.  
Remind me again which part you're actually test that you want to test right now, the game or the user interface for the back end right now.

**Anton Leshkevich** 5:15  
So currently we I think we're discussing the our setup screens which is a UI and back end for it.

**Aaron Bockelie** 5:25  
And so the challenge then is.  
You don't feel that this provides any way to to connect the dots between the user experience for testing it and actually building the software testing it.

**Ihar Hrybko** 5:44  
Uh.

**Anton Leshkevich** 5:44  
Uh, I don't know if I should answer the question.

**Irina Shishko** 5:46  
Oh God.

**Aaron Bockelie** 5:48  
Well.

**Ihar Hrybko** 5:48  
Oh.

**Val Levitan** 5:48  
Pavel, Pavel, you are on mute in case you want to say something.

**Ihar Hrybko** 5:57  
We need to understand what kind of tests we are talking about. We we're talking about.

**Val Levitan** 6:01  
I think, I think we started last week by where I came out and I said.  
That our QA department is excited about a possibility of writing.  
Automated tests that check functionality of our graphic user interface, but we realized that the amount of tests required.  
Is just the very large quantity of tests and that and that will take our QA department quite a bit of time to write all these tests, although they're willing to do it, they're they're excited about it.  
They will write the test and I believe that.

**Aaron Bockelie** 6:52  
I wanna ask, I wanna ask Irina, are you going for test coverage or are you going for functional coverage?

**Val Levitan** 7:01  
I think both.

**Aaron Bockelie** 7:04  
No, they're different.

**Irina Shishko** 7:05  
No, no.  
Oh.  
Civil.  
Punk.

**Pavel Frolov** 7:22  
No test.

**Irina Shishko** 7:29  
Yeah, now my phone's turned on.

**Anton Leshkevich** 7:38  
We join the media.

**Val Levitan** 7:41  
But but my I I I understand that you ask Irina. Irina I I I so Irina's answer is functionality, but I'm jumping in and maybe out of turn.  
Kind of saying what what's on my mind, so if you don't mind my opinion.  
I understand that what we're trying to achieve is before we pull a.  
Feature branch into a master we want to test functionality of.

**Irina Shishko** 8:15  
Mhm.

**Val Levitan** 8:25  
This use case or set of use cases.  
And uh, so to to me that's the integration test.  
The code part is something that maybe the developer would like to test on his own.  
Again, this is strictly my opinion.  
She could be erroneous, I don't know.

**Aaron Bockelie** 8:54  
So what I'm hearing is, is that there is a ton of testing that you don't have the capacity to do is what I'm hearing and.

**Val Levitan** 9:02  
We we we just no, we recognize that there is a lot of there is a ton of testing. Again, I'm I'm repeating myself. We're eager to run these tests or sorry to write these tests. It will just take time.

**Aaron Bockelie** 9:10  
Yeah.

**Val Levitan** 9:19  
And we're realizing that, I don't know, maybe we should develop some sort of a strategy where we take the most important test and the rest we test manually. And while we test manual, we keep on adding other tests.  
But we just cannot catch up with the volume of testing.  
And if we want to have it at the level of integration, then by the time we write the test, the integration is done.

**Anton Leshkevich** 9:52  
Yeah.

**Val Levitan** 9:54  
So then what's the point?  
I I guess there is a point for future integration. If you change something then of course it's very useful, but it's just I I don't understand how to align our.  
Or.  
Capacity of the QA department, even if we're willing to write integration testing, testing with the volume of.  
Development that's coming from the developers.  
There was a um.  
Moment of happiness for me.  
In the last meeting, because I thought that these processes could be.  
Taken from mockup.  
So.  
Right into integration testing.

**Irina Shishko** 10:56  
No.

**Aaron Bockelie** 10:57  
So I I shared with I shared with you guys a bit of a fantasy story in the PDF here in the meeting chat.  
It's not. I say it's fantasy story because it's not really.  
Correct for your environment yet because I just didn't put it in there because I don't know what your environment really is. You know, I know you're using Figma for some design work. I know that eventually you have a product that you test on the other end, but.  
This is kind of a you have to pick any starting point and I will tell you Igor.  
What I heard was I use Figma and then I give up and I can't figure anything out, so it can't be done. I kind of. It kind of blurred together actually, if I'm being completely honest, like.

**Ihar Hrybko** 11:48  
Not exactly, I'm not saying.

**Aaron Bockelie** 11:50  
Well, I I know, and I'm not trying to. This is not a defensive thing at all. This is just my mind. I had to focus extra hard to listen to what you were saying in your challenges because it just came out of your mouth as I we can't do that. That's what I heard.  
And I want to see proof that you can't do it and understand what that we can change the architecture to make it so it works. One of the fundamental challenges that we're fighting against is that you have a software platform built in a particular way and everybody.  
Throws their hands up and says we can't change it.  
The reality is, is you can absolutely change it. If you have the same stupid walkway that you have to walk on every day for the last 10 years and it takes extra time, let's change it.

**Val Levitan** 12:37  
Where?  
I am not saying I I am not saying that we cannot change it. I am eager to change it if you could spell it if you.

**Aaron Bockelie** 12:48  
Right.  
But what I'm I I hear it though. I hear it and I'm seeing it in the people's faces right now.

**Val Levitan** 12:54  
Well, they don't know how.

**Aaron Bockelie** 12:56  
I know. And so the first step of changing it is understanding you don't know. And I'm telling everybody on this call right now, I don't know either.  
So it sounds to me like we need to really understand why we don't know.  
And so I'm going to attempt to provoke a conversation by sharing this narrative in here. I know it's in English, sorry, but it can be translated. There's the markdown version of it.  
How? How far from reality is that? Is that depiction?

**Val Levitan** 13:35  
But this depiction is it.  
Can can we take it for gospel? Is it true or is it a fantasy?

**Aaron Bockelie** 13:44  
Yes, you could follow this through, but it might not build the products that JVL needs. That's the problem.

**Val Levitan** 13:51  
Well, no, I'm saying the depiction here is that a factual.  
Um, depiction that somebody uses in their in in their development.

**Aaron Bockelie** 14:03  
I took the elements of node JS and PostgreSQL for the back end and Figma for the front end and testing elements and API layer and updates and state management and a whole bunch of other technology in here into account.

**Val Levitan** 14:04  
Isn't.

**Ihar Hrybko** 14:14  
You.

**Aaron Bockelie** 14:22  
There's nothing fake about this. I could go architect some application based on this right now if I wanted to, but it's probably not JBL's truth.

**Val Levitan** 14:22  
But.  
But we.  
But we know.  
We we know, we know that sometimes an A I can go on a on a tangent and fantasize.

**Aaron Bockelie** 14:42  
Right, it's not.

**Val Levitan** 14:44  
So is the.  
So this is a factual. This is a factual technology. It's a.

**Aaron Bockelie** 14:47  
I will I.  
This is a factual enough account. It's a factual. It's OK. Wait, I know I'm sounding like somebody **** in my Wheaties this morning a little bit, but I am. I am a little upset to hear. We can't do it is what I heard. And I'm also a little upset.  
That we're not considering that with the structure that you have right now maybe can actually causing the problems that you're occur that you're encountering right now. And I need the other people on the call to be able to kind of acknowledge that perhaps.  
The architecture we have been handed is a bit of a **** sandwich and we need to be able to not eat that and make a new one that's better and not all at once, just a little bit at a time and talk about the outcomes of.

**Val Levitan** 15:37  
Maybe if.

**Aaron Bockelie** 15:40  
Design through it in the sense of is it testable? Can we actually continue to build it? These questions need to be asked.

**Val Levitan** 15:52  
I am going to give a lesson again on the cultural differences that separate us.  
So.  
These people in front of you may or may not be aware that they can change the technological highway.  
And maybe travel a different Rd. Maybe they're not aware of it.  
Maybe for you, with your attitude, you're saying, hey, I am not going to travel the gravel Rd. that somebody.  
Created for me to travel from point A to point Z. I'm going to take a highway. It's a beautiful asphalt. It's easy to travel. It's a little bit more mileage, but I get there faster and easier with more comfort.

**Aaron Bockelie** 16:41  
Mhm.  
Yes.

**Val Levitan** 16:51  
So these people maybe are used to travelling the gravel Rd. because it's simply there and they're unaware. They they could be unaware that there is a highway or they cannot.  
Or maybe they're unaware that they're a that, you know, we allow them to travel that way.  
So why don't we ask a question?  
Are you aware that you could take a different Rd.  
You don't have to stick with this.  
With the current path.

**Anton Leshkevich** 17:34  
Let's say we are.

**Val Levitan** 17:36  
You are aware. OK, so.

**Anton Leshkevich** 17:37  
Actually, we've been pretty flexible at choosing pathways.

**Val Levitan** 17:43  
OK.  
So are you aware that this pathway exists? Then maybe you're not aware that this pathway exists.

**Anton Leshkevich** 17:54  
But perhaps.  
Yeah.

**Val Levitan** 17:59  
Pavel, do you have anything to say? Because you you kind of set the tone with technology, you're director of engineering. So I I really need a little bit more action and a little bit faster. If you if you unaware, I'm OK with that.

**Pavel Frolov** 18:07  
Actually, um.

**Val Levitan** 18:16  
If you're aware but don't want to travel that way, tell me.

**Pavel Frolov** 18:20  
I don't know a better way, a highway. I I don't see a highway here.

**Val Levitan** 18:32  
So I am not an engineer, but I'm seeing a document in front of me where the document says you could develop in Figma, you could develop your mockups and then you could export it into node GS.  
And you could write your TypeScript test.

**Ihar Hrybko** 18:56  
I think we have some misunderstanding because you cannot just export into React application or like no GS application. So these documents saying OK this is like pretty common flow.  
For testing OK design system, some design tokens, colors, but I think this from my side we're talking about really complex.  
Testing because we need to test our main features. I think this math because we can if we don't have.  
Resources to perform this kind of complex testing. We can skip basically and test visually. OK, this is a blue colour and we we can compare this into to Figma mockup.  
And say oh all right so but if we don't have really integration testing and testing our main core functionality, our application will broke basically.  
This is my opinion because.

**Pavel Frolov** 20:34  
As I understand, the suggestion from this article is to switch our back end from Java application to Node JS and TypeScript.

**Irina Shishko** 20:35  
No.

**Anton Leshkevich** 20:46  
I will set a primary goal as I can see it. So our primary objective is to write tests in parallel with development, which is possible if you have this Figma mockups and if I'm if I'm aware Figma mockups can be interactive.  
Like you don't even need tools for that. You can use Figma right away. So technically like once Igor is finished developing his mockup, he can say OK here are my mockups and now front end team alongside with the QA can start working on it and everybody.  
Sees the same picture. So when Irina clicks on a button, something happens, and when Anton trying to implement something clicks on the button, this exactly the same thing should happen. So this is how.  
Like Irina or the the the rest of the QA engineers can understand what is expected of this particular page and they can draft or write their UI test.  
And once Anton or once front end team has finished their part of work, they can run UUI test against it and if the test pass they can merge the code back into the main.  
But basically we don't need any external tools for that and the part of the document that mentions like test and TypeScript only to do this shouldn't be a big issue.

**Pavel Frolov** 22:29  
Yeah, agree if it is, uh, on top.

**Anton Leshkevich** 22:30  
I hope, I hope I I hope I was clear.

**Irina Shishko** 22:36  
Mm uh.

**Ihar Hrybko** 22:36  
So you talking about test during development basically on?

**Anton Leshkevich** 22:40  
Yeah, we've been trying to kind of implement it and it's going sideways, but yeah, this is one way.

**Pavel Frolov** 22:42  
No.

**Ihar Hrybko** 22:46  
But still QA department need to write a test, then obviously a new test with new feature will fail, then QA department need to fix.

**Anton Leshkevich** 22:51  
Yes, yes, yes.  
Mhm.

**Ihar Hrybko** 23:01  
This test until this test pass.

**Anton Leshkevich** 23:04  
Mhm.  
Yes, agreed. This this can be error prone, yes. And for example, I don't know if Figma allows. So what do we do now? Whenever we need like a special button on the page, we assign it a.  
Data test attributes in HTML. Well, I don't know if that's possible in Figma to specifically mark this. Like this particular element should be should have this particular HTML element. So if it's possible, it's OK. If it's not possible, then there must be some sort of.  
Tension between QA team and front end team and this might be a problem. This part can cause delays and iteration of fixes both front end and the test.

**Ihar Hrybko** 23:59  
OK, let let's pretend.

**Irina Shishko** 24:00  
Uh.

**Ihar Hrybko** 24:02  
Mhm.

**Irina Shishko** 24:31  
Ты я сегодня разрабатывается на figma, и потом это каким то образом уже экспортируется в там через что? Ну вот во что мель там или куда то есть вот ты сейчас про ну.

**Anton Leshkevich** 24:42  
Угу.  
Смотрите в чём в чём основная идея? Да, то есть мы. Мы пытаемся сделать так, чтобы а тесты разрабатывались параллельно с фичей. Ну то есть вот тест драйвом до залатан да сейчас для Того чтобы написать тест, а ну нельзя просто в голове себе представить, как будет выглядеть есть стимул страницы и написать под неё тест. То есть мы открываем страницу, мы смотрим элементы, смотрим, как она должна работать, и после этого пишем тест ну то есть найти их на кнопку, нажать на кнопку ну и так далее.

**Irina Shishko** 24:47  
О чём вы?  
Угу.  
Да.  
Да да да.  
Ага.  
Но это то, что мы сейчас пост, то есть значит да ну.

**Anton Leshkevich** 25:20  
Это то, что мы сейчас делаем, да, значит, в фильме есть такая фича, что когда дизайнер верстает страницу, то можно запустить её в интерактивном режиме. Это значит, что вы можете, например, покликать на кнопочки и посмотреть, что будет ещё. Ну, когда этих страниц ещё нет в приложении, то есть в теории в теории да вы можете попробовать написать тест, который естественно, будет появиться, потому что этого нет в приложении, но который будет уже плюс минус функциональной.

**Irina Shishko** 25:29  
Да.  
Угу.  
Но это.  
Но я просто так поняла из прошлого, может быть, я говорю опять, чтоб была моя проблема, что? А как бы одно из важных вещей, что поиск посмотреть и разобраться возможно, Ну что, есть какие то уже готовые тулы, которые помогут, но уменьшить вот это время и о.

**Anton Leshkevich** 25:57  
Угу.

**Irina Shishko** 26:22  
Для разработки вот этих тестов, и они уже есть готовы то есть. Ну вот то, что я пыталась там.

**Val Levitan** 26:27  
Это вы вы неправильно. Ирина, вы неправильно поняли в прошлый митинг.

**Irina Shishko** 26:33  
Угу, ну значит ему это.

**Val Levitan** 26:34  
Прошлый митинг после прошлый митинг посвящался тому, что Иран говорит, что нормальные девелопмент ты можешь из фирмы сразу вырабатывать тесты, что фирма сама должна вырабатывать тест.  
И ты не должен их писать вручную?  
Если ты пользуешься определенными технологиями.

**Irina Shishko** 26:58  
В, ну значит, это я неправильно сказала, вот я так и поняла, но то, что я сейчас понимаю, что мы ничем не пользуемся, а прямо сидим, и опять это сами с ноля пишем, то как сказали.

**Val Levitan** 27:13  
Не так это было в прошлом митинге мы мы поняли, что мы сидим и сами пишем, поэтому.  
А.  
Нам сказали, что мы неправильно это делаем.

**Irina Shishko** 27:22  
А дал.  
Вот это я.  
Ладно, теперь где-то уже встали на место у меня.

**Val Levitan** 27:29  
Но я но и и.  
И и тогда я оставил время для Игоря показать нам, как это делается игр на это посмотрел и сказал, что это сделать невозможно.  
Сейчас мы обратно возвращаемся к тому, что это, возможно ли, возможно.  
По словам такое, моё понятие о прошлом митинге и.

**Ihar Hrybko** 27:55  
Ну по большому счёту да, то есть figma не предполагает такого тестирования, то есть там есть юзабилити тестирование.

**Val Levitan** 27:55  
Там там, где мы сейчас.  
Айран айран айран, настаивает на том, что это это возможно.  
А я знаю что Иран.  
Знает, о чем он говорит?

**Ihar Hrybko** 28:17  
Ну тестировать цвета и кнопки. Мы в теории можем настроить. Ну так ли это важно нам сейчас?  
То есть фильма может отдать?

**Val Levitan** 28:27  
Для я не знаю я я не знаю Игорь почему вы упёрлись цвета.  
Может быть.

**Ihar Hrybko** 28:32  
Потому что figma условно можно это представить, как набор скриншотов очень условно, который может п фирмы может отдать, например, что у нас есть такая палитра и можем написать тест.

**Irina Shishko** 28:40  
Мхм.

**Val Levitan** 28:48  
Если если и Игорь, я хочу вас остановить, вы очень долго это полемику разводите, а и если это возможно, и мы все понимаем, что это возможно, можно это положить на полочку и об этом не говорить. Значит, это возможно. Идём в то, что вы думаете невозможно.  
Значит, вы понимаете, так что функциональность невозможно тестировать.  
А я понимаю, что эра а Иран считает, что возможно, а вы считаете, что невозможно? Вот в этом надо разобраться.

**Ihar Hrybko** 29:13  
Функциональность.  
Вы имеете ввиду тестировать как?

**Anton Leshkevich** 29:20  
Я тут с Игорем.

**Ihar Hrybko** 29:22  
Тестировать можно по разному. У нас мы говорим про какие виды тестирования.

**Val Levitan** 29:26  
Интеграционные тесты.

**Ihar Hrybko** 29:27  
Невозможно, figma здесь не помощник.

**Val Levitan** 29:29  
Окей.  
Окей.

**Anton Leshkevich** 29:32  
Я с Игорем здесь, да?

**Val Levitan** 29:35  
Так так подождите, может быть, мы неправильно высказываем, может быть, это они не сама фирма, а ночь уже.

**Irina Shishko** 29:39  
Угу.

**Val Levitan** 29:43  
Может тестировать это?

**Anton Leshkevich** 29:45  
Да вот, но джесс может, но для Того, чтобы в ноут джес показали.

**Val Levitan** 29:48  
Окей, так так секунд так секундочку, так мы можем перевести это с фирмы сделать в ночь ес и в ночь э то есть уже написать, вернее автоматически писать интеграционные тесты.

**Pavel Frolov** 30:01  
Хотим ли мы полностью?

**Anton Leshkevich** 30:01  
Это то, что сейчас Ирина делают?

**Pavel Frolov** 30:03  
Хотим ли мы переписать лжец? Он же дата-центр с использованием.

**Val Levitan** 30:09  
Я не знаю я не знаю.  
Это уже 3 разговор. Это 3 разговор.

**Pavel Frolov** 30:13  
Я не хочу.

**Anton Leshkevich** 30:13  
Но, но давайте не привязываться к новому g здесь скорее ноутбук ну джес да как какой-то движок, который, собственно, запускает из стимул, но мне обязательно non джес использовать.  
Ну наших приложений.  
Я я я я к тому, что когда Иран говорит ну джесс да просто самый популярный tul для Того, чтобы эти веб приложения запускать у нас джалло ну хорошо будет джаз.  
Принципиально.

**Val Levitan** 30:45  
Так мы можем писать как то автоматом теста могут писаться.

**Anton Leshkevich** 30:52  
Ну нет их их кто-то должен писать, разумеется.  
Было бы хорошо, если сейчас.

**Irina Shishko** 30:59  
Так вот вот вопрос, как писать, используя уже что-то готовое и только под себя подстроить или сесть и написать с нуля этот код теста?

**Anton Leshkevich** 31:01  
Да.

**Irina Shishko** 31:17  
То есть в моём понятии ты так?

**Ihar Hrybko** 31:17  
Везде, где я работал все?  
Все писали с 00:01, то есть теории писали автоматическое тестирование везде, где я работал, никаких магических кнопок, которые напишут адекватны. Ну ей может написать функциональное тестирование какое то да условно на нажать на кнопку да сгенерировать тест.

**Anton Leshkevich** 31:29  
Ну.

**Ihar Hrybko** 31:37  
Такое, даже я там для своих каких то мелких проектов делал, и это работает, но сложная математика, бизнес логика здесь я не я не представляю, как я и может сгенерировать.

**Val Levitan** 31:50  
Так мы Сейчас мы сейчас не говорим не надо называть слово математика. Мы сейчас конкретно говорим про функциональные тесты, которые создаются в юзер интерфейс.  
Ну.

**Ihar Hrybko** 32:04  
Угу.

**Val Levitan** 32:13  
Лата лата сайта женщин даркин.  
Горы выдоена?

**Pavel Frolov** 44:06  
Тренд, он достоин вздохи мент как щелей famitsu микс офф.  
Different присос пенсам кейса связал тени референс энд виссам мэджик инжектор в 3 мин. Сет лосось work дан и дан меняли.  
Энд гейм частушек вот закалок и sn вот за компонент из.  
Нас по хева.

**Aaron Bockelie** 44:48  
Зал.

**Pavel Frolov** 44:49  
Евген different технолоджи задвинут реферату риал лайф.

**Aaron Bockelie** 44:49  
Мать.  
Они идёте на блокады роллы.  
Они идеолог, этот стоит rentals.  
С вами на свете президентский реакцию, часто вот ты пробуешь, она какой-нибудь Windows Дон.  
My goal.  
Is to challenge you to say there is a way that is different than what you're doing right now and that we need. I I'm not a Java architect. I won't be one and I'm not going to be able to help you with that.

**Val Levitan** 45:35  
But I think, I think we came to a binary standoff and it's quite binary. We've spoken Russian and Anton and Igor are both aligned on the fact that there is no automated solution of any sort that they understand.

**Aaron Bockelie** 45:41  
Mhm.

**Val Levitan** 45:56  
That can.  
Morph into an integration test from Figma functional test. I mean they agree that you know there is a way to check a color for example of a bottom of a button, but both of them are saying that functionally.

**Aaron Bockelie** 46:12  
Mhm.

**Val Levitan** 46:16  
You cannot test anything that morphs out of Figma in in an automated format. Yes, you can write.  
A test, but you cannot derive to a test automatically.

**Aaron Bockelie** 46:35  
Of course not. There is no probably no tool that does that. That's like that would be like asking for a wishing for something that wrote tests based on what your Figma UI looks like, right?

**Val Levitan** 46:47  
OK. So then we're all in agreement then then what's the then? I don't understand what's the subject of the discussion.

**Aaron Bockelie** 46:58  
So.  
The actual art is, is that we do have tools that can make it go a lot faster if you can generate TypeScript code from Figma.

**Val Levitan** 47:06  
Third, third, third party tools.

**Aaron Bockelie** 47:11  
So.  
OK, let me ask this in this in this order.  
Can we generate React code or node code that represents the Figma UI from Figma? Is that possible?

**Ihar Hrybko** 47:29  
I think for real production it's not. It's like they use the front page to generate HTML. So for now this generated source code will be not suitable to real production code.

**Aaron Bockelie** 47:48  
And can you define exactly what's not suitable about it?

**Ihar Hrybko** 47:51  
The structure, the I've tried some generators, so they basically suitable for like landing pages, some corporate websites, not real.  
Heavy production applications.

**Aaron Bockelie** 48:16  
Then what is the value of Igma?

**Ihar Hrybko** 48:19  
The Figma used to as a main tool to create user interfaces.  
And create and interactive prototypes to test user flows to.  
Make some um.

**Val Levitan** 48:48  
Mockups.

**Pavel Frolov** 48:49  
I'm OK.

**Ihar Hrybko** 48:50  
Mockups. Based on these mockups, we then transform this into.

**Val Levitan** 48:56  
So you you you mock up, you mock up a user experience and then when you agree on the user experience you could tell a programmer go and do the same thing.  
This is how it should. This is how it should work.

**Aaron Bockelie** 49:08  
And does the.  
And does the programmer have to start over again from scratch?

**Pavel Frolov** 49:16  
No.

**Aaron Bockelie** 49:17  
What do they start with?

**Ihar Hrybko** 49:21  
What do you mean let's start over by scratch we create?

**Aaron Bockelie** 49:24  
So so so you create a mock up you.

**Val Levitan** 49:25  
Start from zero. Do they have to start from zero or can they use anything in the mockup that I I don't know a flow or logic or anything that could be borrowed from Figma so the programmer doesn't start from state 0.

**Ihar Hrybko** 49:46  
Well, we can make intervex prototype, but still we we cannot rely just on the prototype we need to.  
Some real documentation for this feature because in my prototype I cannot accumulate all things that need to happen well in.

**Anton Leshkevich** 50:10  
Sure.

**Pavel Frolov** 50:11  
Igor, can you export CSS? Can you export the components page layout somehow from Figma?

**Ihar Hrybko** 50:13  
Mhm.  
I can't export CSS for a component. I can't even export a component, but still we we using design system for open source movie component kit and we.  
Based on the on this kit, so I create my Figma mockups and components compared to this kit.  
Just to significantly increase development time, because these components like buttons, inputs are already tested, they.  
We basically customize how they looks, but it's functionality already tested and we know that these components in React application for front end side.  
Not will not create a problem to us, so we don't need to test every every button. I mean test the button.  
Like uh for correct rendering.  
I don't know. I don't mean to. We cannot test some business logic that we will connect to this button.  
We only rely on this UI kit.  
Just for correctly appearance on the screen.

**Aaron Bockelie** 52:15  
And does this UI kit? Does it have its own structures or tools to build UIS with?

**Ihar Hrybko** 52:15  
So.  
This UI kit already transformed into React components. We basically customize this components so.

**Aaron Bockelie** 52:38  
So it it feels like you're using Figma in a way that it was not really designed to be used, which is.

**Ihar Hrybko** 52:45  
Oh, really?

**Aaron Bockelie** 52:48  
You're just abusing it.

**Ihar Hrybko** 52:50  
OK.  
Sounds really strange.  
To me. So you tell him to UIUX designer that he uses Figma, not.  
For its purpose.

**Aaron Bockelie** 53:13  
Yeah, that's what I'm hearing right now.

**Ihar Hrybko** 53:14  
Oh, OK.

**Aaron Bockelie** 53:16  
So, so and and why I say this is because it feels like you have to redo all the work you did already. It's like you're building it in Figma and then you're going out and building it again, or you're handing it to somebody else to build again.

**Ihar Hrybko** 53:29  
No, you do you understand how web development process works?

**Aaron Bockelie** 53:36  
Yes.

**Ihar Hrybko** 53:37  
OK, so we first of all we need to create actually our mock-ups just to understand how our application will work. So then we need to transform it.

**Aaron Bockelie** 53:49  
Yes.

**Ihar Hrybko** 53:53  
Into actual react component for the front end side.

**Aaron Bockelie** 53:56  
Right.

**Ihar Hrybko** 53:58  
And then these components will connect to the back end and perform some actions, so business logic. So the you're saying that we don't need actual Figma, we can.

**Aaron Bockelie** 54:08  
Right.

**Ihar Hrybko** 54:13  
Open VS code, then copy paste these components.

**Aaron Bockelie** 54:19  
No, what I'm what I'm what I'm hearing. What I'm hearing is, is that you're using Figma for doing mockups. So this is what I heard from Pavel.

**Ihar Hrybko** 54:21  
So where where?  
Yes.

**Aaron Bockelie** 54:33  
And then you have to rewrite it all again because it's not, it's not enterprise ready or or commercially ready. That's what I'm hearing from the mock up.

**Ihar Hrybko** 54:44  
What do you mean by rewrite Figma? It's a graphical graphical application, so it's not generate any output code. So OK, it can generate some CSS styling and some design tokens colors.

**Aaron Bockelie** 54:46  
So.  
Yes.

**Ihar Hrybko** 55:04  
But it for now at least it cannot generate correctly layout with components with a design system so.

**Aaron Bockelie** 55:16  
I see half a dozen different extensions for Figma because Figma doesn't do it itself to export to React, and you're telling me that none of those can generate React code that works.

**Ihar Hrybko** 55:16  
Oh.  
OK, I can find any extension for any application that's saying that it can generate something, but in real life it's not because it it.

**Aaron Bockelie** 55:36  
But these are real life. They're they're commercial products.

**Ihar Hrybko** 55:40  
OK, do you understand that we can develop like a landing page? So it's landing page. It's basically really simple.

**Aaron Bockelie** 55:51  
Hm.

**Ihar Hrybko** 55:56  
Page that OK, this extension can generate some, maybe not even ****** code.

**Aaron Bockelie** 56:04  
Mhm.

**Ihar Hrybko** 56:05  
We can deploy it and then having fun, but in this kind of production we cannot rely on generating some crazy source code and then we cannot maintain it.  
We need to rely on specific patterns.  
Allowed in react to maintainable source code and we need to watch.  
Like a performance in this application because we have limitation limitations in our hardware, so we cannot rely just generating crazy layouts.  
So we handcraft.  
These components.

**Aaron Bockelie** 57:04  
And that's the part where I'm asking the question then. So you create the, you create a mockup, you use it, you validate that it's what you want to do, and then you're telling me that there's no way to get it out of it because the auto generated code from it is garbage.

**Ihar Hrybko** 57:13  
Yes.

**Aaron Bockelie** 57:20  
And so then you have to rewrite the whole thing again with the developer.

**Ihar Hrybko** 57:23  
Not we we need to write. Why do we say in rewrite? I'm not writing anything in Figma. I'm creating a layout, a user interface, user experience. So we need to understand what happened if a user.  
I'll click on the bottom, then he goes on second screen. I can imitate this in interactive prototype like he goes on second screen and then he goes back. These kind of things. So user experience basically.

**Aaron Bockelie** 57:59  
OK, so you're saying that if I have a mockup and I install a?  
I install a plugin to Figma that claims to export to Reactj the entire UI that's not usable.

**Ihar Hrybko** 58:14  
Oh, in our production, no.

**Aaron Bockelie** 58:16  
Why?

**Ihar Hrybko** 58:18  
Because so OK, why we cannot just use some AI tool to generate whole application?

**Aaron Bockelie** 58:26  
It's not an AI tool, it's a. It's not an AI tool. It's a deterministic package that you can install that doesn't use language models at all.

**Ihar Hrybko** 58:35  
OK, so how this tool can generate correctly out reusable components? For my experience, it's not possible, at least for now.  
Production ready. I'm saying I'm not saying about landing pages. Obviously we can generate some simple landing page with no complex behaviour.  
Just to render some buttons and text. OK, this extension can generate this, but we don't need this. We we already use it completely.

**Aaron Bockelie** 59:16  
OK.

**Ihar Hrybko** 59:26  
Completely this UI kit, completely UI kit and we can. I am using it just to build.  
Application screen, let's say for a new feature. With these components I can build of build it fast in Figma. Then we all agree that.  
All right, this we can build this feature and then all we need to do is just.  
Use Figma as reference, use our buttons inputs from our UI kit and create actual layout in React. It's not taking that much time, but it needs to be done manually.  
Still, because we we don't only have like visual presentation of of this screen, we need to use some React hooks, React functional components.  
And make sure they not break our existing logic so we cannot just export from extension.

**Pavel Frolov** 1:00:53  
Igor, do you use some some components from material UI adjusted for Figma?

**Ihar Hrybko** 1:01:08  
Oh.

**Pavel Frolov** 1:01:09  
OK.

**Anton Leshkevich** 1:01:10  
Hello.

**Ihar Hrybko** 1:01:11  
Adjusted for Figma. What do you mean adjusted?

**Pavel Frolov** 1:01:14  
I just tried to find the relationship between Figma and material UI, so seems they have some relationships like components.

**Ihar Hrybko** 1:01:27  
They have actual actual component kit in Figma.

**Pavel Frolov** 1:01:31  
Mhm.  
Oh.

**Ihar Hrybko** 1:01:33  
Paid components kit so you can use whole design system and create from this kit new new pages, new layouts.  
But I recreated because this Joy UI components kit it's it's a paid feature, so I kind of recreated in Figma manually.  
And we just use this this for customizing theming these components.

**Aaron Bockelie** 1:02:27  
So we're at. I don't want to go over too far because this is one of those topics where everybody gets fatigued fast.  
Um.  
I think that you need to think about defining.  
Let's just imagine that we can find a code generation tool, AI or not, that takes the Figma mockup and could create.  
Code. I'm not going to say roduction ready or even ready code. I'm just going to say code React code on the back end. I think it's now time to define.  
What makes what makes it ready or not?  
I don't. I feel like we're kind of dancing around that right now. There's no clear definition I've heard. You may have it written down. There may be requirements, there may be style guides or whatever, but I don't hear where what makes that code.  
Ready to to be acceptable.  
And I feel very strongly that if you can define exactly what it is that makes that code acceptable, you can use modern recent techniques that use AI or and other things because there's a lot of them out there.  
To be able to generate that code, and then I also want you to think about how much of this is the actual process that's solving the big problem that we've got, which is the inability to have capacity to write tests for things.  
And to have a direct connection from mockups to the reality of the code.  
I think that's the goal here. Like that's why we were excited on the last conversation was, hey, perhaps there are ways to reduce the amount of Labor it takes to go from mock up to test code as well as implementation code.  
Whether that be, you know, a bunch of mocks that you have to be able to run all the time to unit testing to functional test or whatever that might be. There's a whole palette of test types that you really need to have to make this work.

**Anton Leshkevich** 1:04:45  
No, if I may. So I'll from what from the little I know about our UI project, I don't think that we have a problem with writing a lot of HTML code.  
As Igor has already mentioned, like most of our components are already written or already like translated from Figma to React. We the team has invested a lot of time in it or maybe not. I I don't know, I'm speculating.

**Aaron Bockelie** 1:05:09  
Yes.

**Anton Leshkevich** 1:05:15  
And if I understand correctly, eager is just kind of building pages from already existing components and most of the time is the business logic that takes part to implement.  
And.  
And correct me if I'm wrong, probably Igor or Anton know the other Anton know more about this.  
So we can take a look at the tools that kind of generate Figma code, I mean React code from Figma, but I don't think that's really worse.  
Like investment and integration into our pipeline because like most of our code is already pregenerated.

**Aaron Bockelie** 1:06:03  
Yep.

**Val Levitan** 1:06:05  
I think Aaron is not saying, hey guys, you're gonna save a **** lot of **** lot of time.

**Anton Leshkevich** 1:06:14  
Hmm.

**Val Levitan** 1:06:15  
By generating or finding the tool that generates the code automatically from Figma to React, period. That's not exactly what he's saying, he's saying.  
If this tool exists and if there is a way to generate a code automatically then.  
He assumes, or at least I that probably the same code generation tool could also aid in generating tests.  
At least that's my assumption.

**Aaron Bockelie** 1:06:52  
It may not be the, it may not be the exact tool, but it will be the adjacent process, because the whole point of being able to generate the code is that you understand the purpose of the code, and at the time you're generating that, you should be able to test generate tests that validate why you created that in particular.

**Val Levitan** 1:07:05  
Right.  
Right. So and so just to answer the question, the fact that it was manually generated, that means somebody who generated the code understood the process, wrote the code, which is only part of.  
The job, because along with the code, he or a tool should have generated an integration test, but he that wrote the code.  
Did not do the second part.  
So we're not saying, Oh my God, we have to generate a lot of code from Figma. Yes we do, but in parallel we have to generate a lot of integration tests.  
So if there is a tool that understands how to convert Figma mockup into a code, then the same tool will probably or similar or adjacent or parallel tool can probably.  
Generate an integration test, I assume. Is this what you're saying, Aaron?

**Aaron Bockelie** 1:08:24  
I'm saying yeah, I mean it's really not the same tool, it's in the flow of that process. So in the step in the step where I am creating the functional code from the from the mock up.

**Val Levitan** 1:08:36  
Right. That's right. That's exactly. That's exactly what I meant.

**Aaron Bockelie** 1:08:40  
That's exactly where I'm thinking about. And so it's in my mind, either in the developer's mind or the AI mind or the combination of two together. That's the step at which you do that work because you're considering it at the time. That's the efficiency you're getting.

**Val Levitan** 1:08:54  
You're basically saying you're you're basically saying if there is a.  
Uh, an interpreter tool.  
Then the same or similar or parallel interpretation could apply to.  
And integration? Yeah, integration test.

**Aaron Bockelie** 1:09:15  
Creating tests.  
And if you are clearly defining what you're testing, like not not not the literal, I'm testing this and that, it's I test for these things. That's why I asked Irina earlier, are we looking at functional tests or code coverage tests? Because they're two different things.  
Am I testing the intent of the software or am I testing the mechanical components of the software?  
And so when we think about it from testing the intentions of the software, it makes it a lot easier to write a set of tests that go from a mock up to the reality of it and and diversify at that point.  
And I this is the part where I feel like when I talk about in these terms, it's a little bit lost because it feels like everybody's craving an exact specification or exact thing to do, and I can't.  
I don't have that.  
There's some, there's some creativity in the meta product that is the the development pipeline for this that has to be considered now is what it feels like.

**Ihar Hrybko** 1:10:29  
8.

**Val Levitan** 1:10:30  
I'm I'm understanding you now to a degree of 60%.  
I'd like to get to approximately 80%.

**Aaron Bockelie** 1:10:41  
Sure.

**Val Levitan** 1:10:43  
So you saying that when we create a mock up in Figma?  
We should have more requirements defined.

**Aaron Bockelie** 1:10:58  
Potentially, but I think that Igor's already, you're already looking at the requirements, Igor, you're already saying we need this and that and the other thing. So you're building a mock up for that, right?

**Ihar Hrybko** 1:11:09  
Yeah, in in uh.  
Perfect world. I need to see this requirement and based on this requirement, but we can make some, let's say.

**Aaron Bockelie** 1:11:18  
Yeah.

**Ihar Hrybko** 1:11:27  
Hmm.  
Assumptions so we we can test we this is the process because nobody making ideal product for one iteration.  
So we we need to understand actual actual requirements because we can mistake for the first time.

**Aaron Bockelie** 1:11:45  
Right, you it's not perfect the first time.

**Pavel Frolov** 1:11:47  
Yeah.

**Aaron Bockelie** 1:11:53  
Right. It's it's it's iterative, right?

**Pavel Frolov** 1:11:54  
And this is this is sorry, this is a good point where Igor can show his mockups for all the parties to adjust the requirements, reduce new requirements or change the system.  
If we we see together when we meet with Val, with Juan, that user flow should be a little bit different.

**Aaron Bockelie** 1:12:26  
And so.  
Igor puts together a prototype. He shows it in front of the customer. The customer is inspired to think of things they didn't think of the last time. Feedback is given. Igor goes and makes adjustments, right?  
During that process, were the requirements updated too?

**Pavel Frolov** 1:12:47  
Yes.

**Val Levitan** 1:12:51  
No.

**Aaron Bockelie** 1:12:53  
So now Igor's going on original requirements plus the additional changes that have been requested on top and the people who asked it didn't get their requirements changed because they literally were changing them as they were asking them.

**Val Levitan** 1:13:13  
Correct, but correct. But even if we had, I'm just trying to wrap my mind around. Let's say we have a set of perfect requirements that matches Igor's visual interpretation. So now Igor shows a visual.

**Aaron Bockelie** 1:13:13  
Is that happening?  
Sure.

**Val Levitan** 1:13:31  
Interpretation of how user experience was imagined.

**Aaron Bockelie** 1:13:39  
Mhm.

**Val Levitan** 1:13:39  
So now you're saying, OK, there should be an interpreter tool that takes that visual interpretation and reimagines this in a code.

**Aaron Bockelie** 1:13:52  
So right there, right at that point, that juncture is where there are other requirements, and these requirements are not related to the user interface or what was developed or the mockup at all. These requirements are testing.  
And integration requirements that all products need to follow now.  
Because now what you have is you've gone back and forth with the stakeholders, everybody's in agreement with what the user interface is supposed to do and what capabilities it has, and hopefully if you've shifted things around that you've updated those functional requirements for the product itself.  
But then there's another set of requirements that are related to but not enforcing the user interface. And these other set of requirements is this is what we do for test coverage. This is how we write tests.  
This is the type of test we typically write. This is the type of coverage we need if we want a metric, for example, but mostly it's we test this way.  
We create, we take all the React components and we match the mall U to the back end of the service.  
We make sure that there is 100% coverage of service. We lint all of the React components and we lint all of the other end points on the other side, and if there's a differential in linting, then the test does not pass. That is a particular kind of test requirements that are being written now for the.  
Now for the integration testing, and if you define those requirements, it helps to do automated code generation for that, reducing the amount of effort that it takes to do that.  
So normally that's done by hand. That's the manual generation is what we'll call it. I I I don't like the idea of calling software engineers manual generators of code, but that's kind of, you know, what we're accidentally saying here.  
Um.  
That's the that's the the the technical test writing that has to occur now, but it's based not on just reading this, reading the requirements of the of the user interface that was created. It's actually understanding to what value and degree do we write the test themselves.  
And I think that sounds like a missing piece.  
Because if you have that, then you can kind of like almost test the test. You're not really testing it, but what you're doing is you're saying, does this test fulfill my obligations? And if you can define that, this is what?  
Recently in circles is called specification driven development, spec driven development. So you're writing spec specifications for your tests and if Igor has a generation pipeline that goes from from mock up to React code of some kind.  
And then that React code is not viable for commercial. Then you have your specs that are written for the testing that go from from whatever was generated to reality. And then you also then split and branch at that point the part where Val's talking about.  
Well, can we write the test the time that we're generating the code? And the answer is yes, because if you have the specification for where the tests are, and now you have the specification for the way the user interface is written as well, then you're generating code across to the whole platform product instead of just sort of independently.

**Pavel Frolov** 1:17:51  
Seems like I'm already lost.

**Aaron Bockelie** 1:17:55  
Do you have specifications for how your tests are supposed to be written?

**Pavel Frolov** 1:17:59  
No.

**Aaron Bockelie** 1:18:01  
Why not?

**Pavel Frolov** 1:18:06  
U.  
Why not? Why don't we have a specification for our tests?

**Aaron Bockelie** 1:18:12  
Right. Why? Why can't I be hired as JVL as a test engineer, software test engineer, and I'm going to write a test that asserts everything is passing?  
Is that legal to do that?

**Val Levitan** 1:18:26  
We don't have specification for tests because we never philosophized about it. There has never been.  
A probing session of why we do certain tests the way we do it and why we do as many tests. There has never been a a challenge and challenge session to why we do things certain way.  
In form of QA.  
And traditionally RQA has been a post fact thing with that we say OK, go ahead and test it and we have.

**Aaron Bockelie** 1:19:04  
Yep.

**Val Levitan** 1:19:12  
A group of people that are enthusiastically trying to understand the project and say, well, I guess this is how you should test it, but there's no theory behind why we do things.

**Aaron Bockelie** 1:19:18  
Mhm.  
Right.  
Well, it.

**Val Levitan** 1:19:27  
Look, I am going to tell you something very interesting that will hit home for you right now, Pavel.  
Specifically for you, specifically for you. I'm telling you, we already understand that we are capable of having our own school.  
Of game development. So we have enough in-house expertise to have our own vision school of why a game should be developed the way we develop it.  
But we don't have it on testing.  
We cannot say we are 100% sure that we're doing it right. We not, not, not even that we have a philosophy. We have in-house philosophy why we do testing a certain way. We don't have it.  
It's a it's an QA department has always been up until recently. We're changing it now, but it has traditionally been an orphaned.

**Pavel Frolov** 1:20:37  
Absolutely agree.

**Val Levitan** 1:20:51  
Do you guys know Russian translation of the word orphaned at Ribyona Katori?

**Pavel Frolov** 1:20:56  
OK.  
Brew.  
Just get on.

**Val Levitan** 1:21:12  
But that are not QA department.  
Nobody pays attention to it.  
But now, recently, recently, I myself start paying attention to why we do things the way we do, why we choose a certain technology stock, why we.  
Hire a certain specialist.  
I have so many whys in the past five years that you guys are absolutely sick of me.  
Because no matter what you say, I have 10 whys.  
And recently I have been saying, why are we doing tests the way we're doing? And I have been digging into it and you know, Aaron has been that's that's Aaron's background. So he's, you know, sharing a lot of experience and I'm saying, huh.  
Interesting. Why aren't we doing this?  
And this is where you start seeing the pressure. So I've raised the subject. So how many people do I need to run integration test? Now I'm like I understand the philosophy behind integration testing.  
And I'm saying I want it. That's a great philosophy. I want to adapt it. And now the second question, why can't we do it? Well, the immediate thing that jumps at me, well, we need a lot of programmers that write these tests in advance.  
In advance.  
So then I says then I ask a question so.  
The advanced software companies, how do they do it?  
How? How can you constantly release software? Constantly release software?  
Like you have to have probably a ratio of three to one testers to developers.  
So you want your testers to understand the business requirement even before the developers understood your business requirements, so they can write a catch me test on the integration.  
Before the developer writes its code. This is crazy. I don't believe that it exists.  
Or maybe it exists. If it exists then.  
But Aaron tell me no, it doesn't exist. So you have such ratio or even one to one or two to one.  
QA programmers to developers.  
And if and if this is not correct, then how do you release continuously release and how do you continuously integrate?  
They should be on our minds.  
If we want to have a good business, we have to have our own school, our own methodology.

**Aaron Bockelie** 1:24:58  
So.  
I'm gonna add on to this and sort of.  
Statement that Val's put here is that I think it's generally accepted that the developers also write the tests.  
Like that's a that's a that's a pretty normal thing nowadays.

**Val Levitan** 1:25:14  
Well.  
Well, I, you know, I just realised that if this interpreter that we're discussing between Figma and the back end or sorry, between Figma and the code doesn't exist.  
And that interpreter of the logic is the developer. Then yeah, the developer should be interpreting the intent of the code.  
Mode.  
Also into the integration tests.  
Right. That's what they're in the saying now.  
Right.

**Aaron Bockelie** 1:26:01  
Correct.  
So this is kind of I'm just typing this out in chat. This is what I think kind of where QA a test engineering group actually shines at.  
So end to end tests where you start an application and you end up with a product or something like that to drive it. Exploratory testing. Something's not working. We should figure out how to write a test for that or test suites, which is here is our.  
Overall functional approach. We're going to grab all the tests and we're going to assemble and sort them into a big large package for us. Any kind of specialized testing, which you're hopefully not doing a lot of.  
And acceptance testing, which is it does the thing it needs to do but.  
I would say that.  
You know.  
Deb's right. Let's just say unit tests, integration tests.  
Um TDD.  
So this is kind of where I'm thinking and and code reviews.  
There's kind of a lack of code reviews that I see formal code reviews where at least they're written down. These things is what the develoer should be doing.  
O It's not a clean distinction between the develoers and the testers. Now it's not like I throw it over the wall and you make all the tests for me anymore.

**Ihar Hrybko** 1:27:54  
OK. Just to mention these all things increase amount of development significantly all this.

**Val Levitan** 1:27:59  
Yes.

**Aaron Bockelie** 1:28:04  
Course they do.  
So.  
So the question is.  
Is there value in it, or do you just throw it out there and hope it works? Or does it eventually create so much technical debt for being able to understand what's going on that it grinds a lot of innovation to a halt?  
Because if you stop doing some of these things, or you never start doing them, the complexity of the whole system tends to get.  
Just tangled up and and you don't have a chance to really get out of it until you understand. It takes a human now to navigate everything. You can't automate that because there's too many, there's too many loose ends.  
All of the wires get tangled up in a box.  
So I think that what's happening here is we're talking about Figma and we're talking about the mockups, and I am making an assumption that it should be fairly clean to go from generated code in Figma to actual production environment.  
And the reality is, it's way complicated because there's a whole bunch of missing pieces. It sounds like, and I'm not saying the truth, I'm just saying it sounds like there's no definition of what you're even writing tests for, or the integration or the other pieces for this, and no one's really considered.  
How could you make sure that you have written records of specification for what these user interfaces that Igor's creating actually need to adhere to from a testing perspective?

**Val Levitan** 1:29:57  
Yeah, but let's say we have this written out. Let's say we have these user experiences and requirements. I still don't feel that there is an automated converter from Figma to code.

**Aaron Bockelie** 1:30:17  
So when Igor creates a user interface mockup, right, it's connecting to a bunch of things. Let's just, I'm going to imagine something. Let's say you have a some sort of administration menu that's in the upper right corner that you have to have, right?  
And it has to be consistent across every single page that you have. Or maybe it's some sort of nested framework or whatever. I don't know, however you put it together.  
You don't want to recreate that in every single page because you already generated it the first time you made an administration page, and so the code already exists for that. So what it means is that the actual amount of mockup that Igor has to do is less and less and less over time to the point of.  
Literally, he's just you're just mocking up a dialog box inside of a bunch of functional code that already would exist. Is that is that does that happen?

**Ihar Hrybko** 1:31:11  
Yes, exactly.

**Aaron Bockelie** 1:31:13  
OK, and so.

**Ihar Hrybko** 1:31:15  
But you're talking just of small piece of. I don't need to recreate the whole menu, but I need to recreate some state of menu. I need to represent to user where user is located now, so need to change state of menu.

**Aaron Bockelie** 1:31:33  
OK.

**Ihar Hrybko** 1:31:35  
So basically yes, we we have some bunch of components and I need to create a layout from these components or create a new component.

**Aaron Bockelie** 1:31:37  
So.  
Yeah. And So what then happens is, is that you you develop 80% of the application, the the human generation occurs of the code into into the product and then you're asked to create some new thing.  
Now, if you trot out your nine month old mockup from way before anything got wrote, it's a matter of convenience to show the mockup and then the new thing inside of Figma, because it's just a matter of drawing the box and there it is and it looks good.  
The reality is, is that the actual user interface experience and everything else is truly created and integrated into the code base now, and it's difficult for you to present the new slight change without using the old Figma mockup, which might have diverged from the reality of what actually was.  
Was implemented. Is that also right?

**Ihar Hrybko** 1:32:45  
And now this mockups exactly represent what already implemented, but we need to mention I cannot recreate all states of application.

**Aaron Bockelie** 1:32:47  
No.

**Ihar Hrybko** 1:33:01  
Well, I can, but it takes a lot of time just to create a.

**Aaron Bockelie** 1:33:07  
Mhm.

**Ihar Hrybko** 1:33:13  
Prototype interactive prototype in Figma. So I create all states for all components. So for for example we have a button then we need to create enabled button.

**Aaron Bockelie** 1:33:17  
Mhm.

**Ihar Hrybko** 1:33:33  
Disable button, hover state and so on. So the front end developer can use this reference when he needs to, for example, disable this button.  
He exactly knows how this button will look like. Uh.  
So this is the flow. So I cannot create all states of this application because we have different roles, we have different.  
In one world we have complex business logic, so for some states that we need to actual specification.  
Just telling what what need to happen exactly in user interface.

**Aaron Bockelie** 1:34:38  
So basically the idempotency of the code that is implemented is not equivalent to what's in Figma.  
That's what you're that's what you're saying.

**Ihar Hrybko** 1:34:47  
What? What? What do you mean in Figma? We have static, basically static application. I can create some states.  
In in interactive prototype we can increase the states and I can take more time on this states in Figma.  
And create cover cover more more of the states of application.

**Aaron Bockelie** 1:35:28  
Right. But you're doing that at at the.  
At the cost of why do we need to do it when you start detailing into all of the corners of this right? Because you're you have to in Figma, you have to create, you have to recreate every mocked up bit of data that potentially the platform can provide, right?  
Right.

**Ihar Hrybko** 1:35:50  
Yes, or at least I need to keep in mind that this input can have like thousands of characters for example. So I need to create this component that can handle this amount.

**Aaron Bockelie** 1:35:51  
Yeah.  
Yeah.  
And so then you create that component based on the knowledge of the requirement that the back end can supply 4000 characters of something.

**Ihar Hrybko** 1:36:16  
Yes.

**Aaron Bockelie** 1:36:19  
And then therefore, if you're creating it on that, the developer has already mocked. Actually, it's a question, has the developer already mocked up the test for this? Because they know that you can put 4000 characters out of that output.  
Or are you basing it on an assumption?

**Ihar Hrybko** 1:36:41  
No, I I don't need some test from a developer. Actually developer is I make a.  
User interface based on requirement for application for an application and I don't need to wait and I.  
I figured out by myself or we we can figure it out with our team.  
Make some assumptions.

**Aaron Bockelie** 1:37:28  
So.

**Ihar Hrybko** 1:37:29  
So.

**Aaron Bockelie** 1:37:31  
Keep continue. I'm I'm writing something out as well here.

**Ihar Hrybko** 1:37:35  
Now trying to understand what exactly you're saying. I need to wait that some developer or QA write a test and then I need to make a user interface.  
So.  
You uh.  
This strange sounds strange for me.

**Aaron Bockelie** 1:38:13  
Hang on.

**Val Levitan** 1:38:24  
I love this, uh, candid conversation.  
It's it's very it's very refreshing. I like when you express yourself in the most.  
Forward manner.

**Aaron Bockelie** 1:38:44  
This is sort of the back and forth that I'm imagining is happening now. An application capability is defined. Let's say we need a box for text to display something. Then you go draw a box to display something and the stakeholder accepts it. Then the code to populate the box is created.  
And then we find out you need more box space because the actual output is different. So now it's broken. So you need to go renegotiate the requirements and then you got to go back to the stakeholder and say actually we've displayed this many more and now it breaks the UI and now the UI has to be redrawn again for the stakeholder to.  
It again.  
And it kind of spirals, swirls a lot of times. There's a lot of cycles going on in here, right?  
So where do the requirements go? Who's testing it? How are you defining what's the maximum maximal requirements for these things, right?  
So this is this can spiral into things like.  
What's the manual of style convention for the user interface? Like what's the what's the personality of the user interface supposed to look like? And these are all become specifications for the UI. They can become specifications that can be derived into writing tests for it.  
So.  
This becomes more of the specifications that I'm hoping to hear about at some point about we test for these specs.  
Or you know because like if you have this hypothetical dialog box or not dialog information box with with text in it.  
Is that really ever allowed? Can we? Can we? How many maximum characters can we put in that before it breaks our UI convention and so forth 'cause you're basing it? And then there's a whole tower of assumptions that it's based on the UI kit that you're using.  
The way it's supposed to be implemented, the type of information that's being presented, and so forth. Every single bit of this sort of can be distilled into specifications, and then you can write the code against that and the thing I'm trying to sort of.  
Conclude to is that human generation of code versus machine generation of code. The gap is closing and we can potentially use machine generation of code to write tests and other pieces and parts.  
Much faster if we know what our specifications are for both what are we testing, what's the acceptance criteria of the general convention of the user interface, and then the highly specific requirements that the.  
Stakeholders want for that particular use user experience.  
Because now if you have those available, when your human generators of code are writing the back end that presents the information to it, they can go, well, I just do this one thing and then it sends to the API this gigantic GLOB of text and now it's super breaking everything.  
Everything on the front end, because I didn't do it right, then they're able to get to that conclusion a lot faster.  
I'm jumping around a bit because what I'm trying to get to is that we're realistically just trying to close the cycle time. The actual goal of this entire conversation is to reduce the amount of time it takes to go from a mock up to functional code and testing and ensure that it's not broken.  
Overtime.  
And the best way you do that is to try to declare as much of what the rules and boundaries in the form of specifications as you possibly can ahead of time.

**Val Levitan** 1:42:39  
But what I don't understand, if you have a perfect set of requirements and if your mockup is a reflection of these requirements, is there a tool that exists that could look at The requirement and translate?  
Figma mockups into a code.  
Or or or you hoping that AI will catch up in a year and we will have that functionality?

**Aaron Bockelie** 1:43:04  
If you have.  
It doesn't catch up, it works right now. It just you have to decide how your specifications will define it.

**Ihar Hrybko** 1:43:24  
You you have an example working example.

**Aaron Bockelie** 1:43:27  
Sure, I can bust out cloud code with a specification and a mockup extracted from Figma and write the tests and the back end and everything else in a few minutes.

**Ihar Hrybko** 1:43:38  
So your application will be doing what exactly? Just display some some buttons and you can check is this buttons represent correctly rendered. This is test. We can make bunch of these tests really quick.

**Aaron Bockelie** 1:43:44  
Whatever needs to be.  
Sure. I mean it is just it's.

**Ihar Hrybko** 1:43:58  
But we're talking, we're we're talking about I think this integration test. So we we introduce new feature, let's say some SAS or version version.

**Aaron Bockelie** 1:43:59  
You could.  
Mhm.

**Ihar Hrybko** 1:44:14  
.3 and then we need to check that our software can handle this new SAS version so the front end will.  
Represent correct preferences, some bunch of inputs, checkboxes. The if an operator clicks on a checkbox, it will work correctly with this new version.

**Aaron Bockelie** 1:44:33  
Mhm.

**Ihar Hrybko** 1:44:46  
So this test, I think it's a really important test.

**Aaron Bockelie** 1:44:53  
So if you have, let's say you have mocks for all of the user elements, OK, and let's say that this new SAS version of something produces some sort of new information element inside of your boxes that you've got.  
If you can create or fuzz, So what type of test are you gonna actually execute for this? Like what are we expecting to see the difference in spec between the last version and the next version of this new data source? So.  
I would just go on and a guess here and we can say that there are brand new functions and capabilities that never even existed before, and that perhaps some of this information has different formats than it showed before. Or maybe there's some other breaking change inside of the specification for.  
Data source.  
If you have mocks set up as an example, I'm cherry picking one thing inside of all of your user elements. You should be able to create a data set against all the mocks when you run that test, and it should break a whole bunch of stuff. You should instantly have a bunch of failing tests for your existing users.  
Environment user interface because you fed it a bunch of invalid data that exceeds the bounds of the mocks.

**Ihar Hrybko** 1:46:15  
We only can test the user interface, but we cannot test in this way actual business logic because I don't have business logic in my Figma mockups. I don't know how how says.

**Aaron Bockelie** 1:46:27  
No, you.

**Ihar Hrybko** 1:46:30  
Expects the back end that handles a new version says expects the the input format or how how back end will send to the front end new output format response.

**Pavel Frolov** 1:46:45  
To be home.

**Ihar Hrybko** 1:46:51  
So we need to test if this response correct and.

**Val Levitan** 1:47:00  
But why do we need to? Why do we need to test the response in the in the graphic user interface? Don't we test? Don't we test SAS differently or under different circumstances? I think the conversation, I think.

**Ihar Hrybko** 1:47:07  
But we don't.

**Val Levitan** 1:47:16  
For some reason, the conversation is.  
Taking a different shape, I think we're talking.

**Aaron Bockelie** 1:47:24  
In my mind, I'm picturing SAS as some sort of like API version. OK, like I'm kind of translating some SAS thing into in my mind as a bunch of new endpoints. So there's some new endpoints that are available in my impression then.

**Ihar Hrybko** 1:47:35  
OK.

**Aaron Bockelie** 1:47:41  
Is that nothing would change, it would just be the same. But if there's a difference between previous SAS protocol version and next SAS protocol version, that's not really your problem at all. That's up to this person implementing SAS to go, you know what?

**Val Levitan** 1:48:00  
Right, right.

**Aaron Bockelie** 1:48:00  
I've broken a bunch of stuff. I've changed these existing things and now instead of sending a string of integers, it sends text or it sends a Jason object instead of a string or whatever it is that's going on. It's a breaking.  
Change.  
And actually then that person introducing those breaking changes is going to know ahead of time. They're not going to just throw a grenade at you and expect you to catch it. That would be crazy. What they're going to be doing is, is they're going to say I have introduced these specific breaking changes.  
And these are now the new specifications for the user interface. The user interface, when handling this thing in the side of the user interface, has to handle it as an array of objects rather than a single string.  
And then what happens is that you have to then renegotiate the mockups again and recreate the new tests and all the other pieces. And then you have to decide, do we still support the old version or do we drop the old version of the code? And every single bit of these interface experiences need to have a spec for what is.  
actually expected.

**Ihar Hrybko** 1:49:17  
Yeah.

**Aaron Bockelie** 1:49:17  
O Remember requirements is what it should must do and the specification is how it will be done.  
So you need both really to make this work.

**Pavel Frolov** 1:49:30  
Actually, uh, we need to have a different mockups for different specifications.

**Aaron Bockelie** 1:49:37  
Yep, because you're doing it differently, right?  
And so then with.

**Pavel Frolov** 1:49:43  
Because at any moment you can refer to particular version of mock up and it will represent the appropriate version of software that it was developed based on.

**Aaron Bockelie** 1:49:58  
And so with a single git commit, if Sasha isn't careful, can invoke six months worth of refactor of the entire user interface.

**Ihar Hrybko** 1:49:58  
But.

**Aaron Bockelie** 1:50:09  
Whose fault is that?  
Nobody's because nobody discussed or negotiated what changes were going to happen and how the plan was going to be planned out on how to retire the old version or how long you're going to hold on to the previous versions because you have other machines that conform to the new version of SAS.  
So you are bifurcating, you're splitting up into more and more products that you have to carry, and no one was considerate of how many people on the team you have to be able to maintain all these old products.  
So the specification splits into two specs, which means that you're now writing an entire copy of an entire platform that you had from before almost, unless you're clever and try to figure out a way to integrate that together to make it so you handle spec.  
One and spec two of the same of the same requirement.  
And so this once again comes back to the cycle time is the real trouble here. The real problem is the amount of cycle time it takes to do this implementation.  
You could almost express it as an algebraic expression, right? Like you have all these different groupings and they multiply each other to the next, to the next, to the next. As soon as you implement another spec, everything before in front of your your your math problem.  
It's doubled in size cuz now you have to write it for two. I mean, I'm simplifying, but that's kind of what I'm imagining in my mind when I think about, well, somebody's gonna make a new change to the business logic, which then means Igor has to go refactor every single damn user interface component that actually supports.  
This.

**Ihar Hrybko** 1:52:08  
Exactly.

**Aaron Bockelie** 1:52:10  
So this has as much to do with writing specs as it does everything else. In ideal world, they should be able to change whatever they want, and it doesn't break anything at all. There's no breaking changes to whatever Igor has put his effort into, and then instead it's a matter of deciding explicitly and specifically.

**Val Levitan** 1:52:15  
OK.

**Aaron Bockelie** 1:52:30  
What elements need to change and making a small enough change that it doesn't swamp Igor with all of the effort necessary to make all the user interface changes.  
So it's turning into. This is really sounding like we need specs.  
And we need to make sure that we're writing tests from the developer perspective to those specs as much as possible, as well as the requirements.  
That's my that's my take away from this chat today. I think we're at The two hour mark. I think everybody's getting tired.  
Because without a SEC, you can't generate code.  
Either by a human or machine. And if you can't generate the code, how could you possibly write the test? And how could you? If you can't write the test, how can you verify things work?  
I would like to ask this question. If there's one thing we could do based on what we talked about for the last two hours, what do you think it would be?

**Pavel Frolov** 1:54:01  
Sorry, could could you repeat please?

**Aaron Bockelie** 1:54:04  
So we went had quite a journey in the last two hours. We talked about Figma and generating code and understanding that, you know, apparently it's not production ready when you generate the code. And Igor has challenges with scaling himself because he's one person.  
There is automations to be had in various places throughout this whole mess of pipeline that we have to deal with. So out of the whole conversation of closing, if I tell you.  
What I hear today is that cycle time is the biggest killer of value.  
And the other concern is quality of the code is the next killer of value.  
What do you think the best thing to do would be to start? How to figure out how to do here? Do nothing? Is it perfect? What could we do to change something to make it so we could improve this pipeline?

**Pavel Frolov** 1:55:08  
So I see first of all, I that I see we need to to invite you a team as early as possible.

**Aaron Bockelie** 1:55:22  
OK.

**Pavel Frolov** 1:55:23  
It's real. Uh.  
It will dramatically reduce the time of full cycle.

**Aaron Bockelie** 1:55:33  
And how do you in how do you invite the QA team earlier in the cycle? How do you shift? How do you shift left to invite the QA team in the development cycle?

**Pavel Frolov** 1:55:42  
I do not see the full picture, but at least at The moment when the graphic user interface is in process of creation, for example Igor created a mock up.

**Val Levitan** 1:55:48  
Oh.

**Pavel Frolov** 1:55:59  
And then he and Anton starts implementing layouts and even before implementing the business business logic. At this point he already can.  
Uh use uh um.  
Code code base.  
And start writing their code at least to to check that all the components exist, all the pages exist and some user flow is ready to pass.  
So.

**Ihar Hrybko** 1:56:59  
Hold on.

**Pavel Frolov** 1:57:04  
Со мной включает вещь.

**Irina Shishko** 1:57:08  
Так я ж не говорю, что не не даст.

**Pavel Frolov** 1:57:08  
Юз юз кейс юсб кейсы шуберт рейтинг, адрес моменту редди и носки. Если это листай финк эти на антиперспирант.

**Irina Shishko** 1:57:18  
Нет.  
Млм.  
Я имела в виду, что в первоначально у нас есть требования дальше Игорь рисует макаф, ой, ну макаф или эти как правильно figma.  
А и после этого ну то есть по тому, как ты сейчас построил, привлекается q. С одной стороны, кей пишут тесты. С другой стороны, программисты кодируют уже это самое как бы свою часть.  
То есть.

**Ihar Hrybko** 1:57:55  
Ну смотря какие тесты.

**Irina Shishko** 1:57:55  
Так получается.

**Ihar Hrybko** 1:57:57  
Ну тут же тест это разные бывают, ну типа функциональные, да какие то тестирования кнопок? Допустим да, которые просто кнопка появилась, грубо говоря.

**Irina Shishko** 1:58:06  
Но и.  
Цели, другие ножные.

**Ihar Hrybko** 1:58:09  
Но другие они не могут существовать без Того, чтобы ну либо мы делаем тест driven девелопмент, то есть изначально пишется тест со всеми условиями.

**Irina Shishko** 1:58:09  
Нам с.

**Ihar Hrybko** 1:58:20  
Да, то есть он пишется уже, конечно же после ну или.  
На на на на этапе каком то согласовании, то есть Макаров может даже не быть ещё, то есть это же всего лишь юзер интерфейс.  
Да, а можно же писать тест, предполагая что там будет кнопка какая то да там в тесте не должно быть указано, где она должна быть. Ну это не обязательно, это будет функциональный тест, а это будет тест получается уже. Ну то есть проверяя саму бизнес логику.

**Irina Shishko** 1:58:45  
Угу.

**Ihar Hrybko** 1:58:51  
То есть у нас там.  
По появилась, мы описали, что там, допустим, мне несколько инсультов, 3 кнопки эти кнопки делают, то есть одна зависит от 2, что-то там происходит под капотом. Да мы это всё мокрым, да то есть имитируем в тесте.

**Irina Shishko** 1:59:09  
Мхм.

**Ihar Hrybko** 1:59:10  
И естественно, этот тест ещё основывается на остальном остальном покрытий. Да, тут же ещё надо понимать, что эти тесты не отдельно живут.

**Irina Shishko** 1:59:18  
Ну да.

**Pavel Frolov** 1:59:20  
Эксперты тест driven девелопмент минсу за за девелоперские сурайкин дисковод энд хироси EG битве q, департамен developers, голос тест гривен, part из ритенберг, Queen dq донат новый болт здесь.

**Aaron Bockelie** 1:59:40  
Дефис бы интерьер teaser систем будет kiwi.  
Сейчас.  
Вытеснявшимся гидрометеоролог.  
Reality is, is that Pavel's very right. You can't have a test of someone who doesn't understand the product write tests that are test driven development. You have to have the developer who knows what's going on to hypothesize how they're writing a test for the spec.  
But what it also means is that the test QA engineers who understand functional test or maybe acceptance test or some sort of test suite approach should be able to act as a pair developer or a pair programmer alongside of the other.  
The actual application developer working together. You're bringing the two closer together to the same team.

2:00:46  
OK.

**Pavel Frolov** 2:00:59  
Yeah, in in case of this close junction between QA and the developer, then when the developer is has written test driven.  
Test committed that he implement a code that implements the logic of of this test driven code and at this moment he need to.  
To say something to create OK, it's a new button is already implemented. You can take it and perform end to end test or integration test.

**Aaron Bockelie** 2:01:47  
Think about it like there's an overlap, right? If you have a SDE in test and you have a SDE in dev, there's a lot of overlap where they're working on the exact same thing. The developer writes the test before they write the code.  
The the the principal developer. The QA developer also writes the code for this as well. When it comes to reviewing this, there's a pull request that occurs and there's a code review for the for the test driven development.  
That's then accepted as part of this piece of the software, this capability that's being written right. Then the developer begins to work on implementing the code that the test is expecting the.  
QA developer, the test engineer developer, continues to monitor that code to make sure it's still the same because there may be some more commits to it or some. I slightly changed my idea here and there. That person is now working.  
Feverishly to integrate that into the test suite to make sure the test suite can accommodate this new capability at that time.

**Irina Shishko** 2:02:57  
Oh.

**Aaron Bockelie** 2:03:01  
The next pull request that occurs, which is where the functional code that the test spec for the test driven development expected. The QA engineer and the developer engineer are both on the pull request in the code review process to ensure that everything all works together.  
This is air rogramming in a way, and this is air programming with the test engineer and the developer engineer.  
I think this is a shift from the way you do things right now.

**Pavel Frolov** 2:03:40  
Mhm.

**Aaron Bockelie** 2:03:43  
And both of them, both people are looking at The same specification and the same set of requirements.

**Pavel Frolov** 2:03:58  
Mhm.

**Aaron Bockelie** 2:04:02  
When they're done, they are both presenting to the stakeholder the new capability that they've implemented.  
And when let's let's expand the circle a little bit more. The UX engineer is also involved with this because they during their development discovery cycle of creating both the test, the test spec and then the code.  
Find out that the UI needs to be slightly changed because of some presentation problem and so then he's involved as well in this process at The time. So now you have a small development team building this piece of the capability out of the platform altogether in one.

**Irina Shishko** 2:04:39  
Thanks.  
Take the search.

**Aaron Bockelie** 2:04:49  
One spot, right?  
And you can only define so large of a capability to define within your two week Sprint cycle, let's say 2 weeks. And so that's how you begin to have that small group of people, a UX person, the test.

**Irina Shishko** 2:04:54  
Sure.

**Aaron Bockelie** 2:05:07  
The dev all communicate and coordinate together as a small unit to then present their finished product, their thing that's done to the stakeholder at The end of the Sprint, and every bit of their actions are dependent on the specifications and the requirements necessary to do that.  
do that because the specs were laid out a year ago by the architect.  
You don't know whether I'm talking about building an apartment building or building software now, do you? Because it's the exact same thing.  
But I I I think going back to my challenge of if there's one thing we could do from this meeting today, what could we do? I think it's actually to start considering what specifications look like.  
I think that would be a really good place to start. It's a straightforward thing to begin asking the question what does a spec look like for this?

**Pavel Frolov** 2:06:18  
Mhm.

**Aaron Bockelie** 2:06:18  
What does it? And then as soon as we ask that question, then we can understand the scope of who's involved in building it. And I think the next question that I think Irina and Pavel need to talk about is what is it going to take to closer?  
Pair a QA engineer and a dev engineer together.  
Collaborate on on a on something the shift, the shift, the testing left.  
Because I can kind of imagine a situation where we have a Igor and an Anton and I don't know who we could pull from QA engineering, but those three people could be working on a particular capability in a two week Sprint and.  
Knock it out of the park if they have a specification and the requirements.  
Thoughts.

**Pavel Frolov** 2:07:33  
It's it sounds very easy.

**Aaron Bockelie** 2:07:39  
Deceptively easy, right?

**Pavel Frolov** 2:07:41  
Yes.

**Aaron Bockelie** 2:07:45  
O.  
I can tell you why I think it sounds deceptively easy. It's because I'm asking you to stop trying to consider the whole universe of everything in any particular approach to something. So when you're building out the product.  
It's almost like you have to because of the way the code base is built and the way that you're building out the platform. It's like you have to remember too much stuff all at once to be able to build that piece out. You're based on an architectural legacy that is.  
Not modular. And when Igor makes a change to the UI, it propagates through everything. And I think that's kind of a architectural problem that needs to be we're we're shifting the burden onto the architecture of the platform now.  
Because we can't give the responsibility of the architecture to be refactored in a micro fashion every single time we want to implement the capability.  
And we can start to have control over that by beginning to write specifications for things. I think that's a big thing that sounds like it's missing right now.

**Pavel Frolov** 2:09:10  
When we're saying about specification, should we split it to to different smaller specifications that relates to capability to feature or to to something else or just a common?  
Big documents that contains everything.

**Aaron Bockelie** 2:09:33  
Well, I think that you should try to focus on one aspect of it first before you write to cover everything.

**Pavel Frolov** 2:09:42  
Specification for new feature for that.

**Aaron Bockelie** 2:09:54  
I I almost would want to have you do something it's just recently created, especially if it doesn't exist right now, because it'll be fresh in your mind thinking about it.  
Try to go back a month at the most and say we made this new thing. Let's write a spec. Let's let's take our first pass at writing a spec for what this should have been like.

**Pavel Frolov** 2:10:30  
Mm-hmm. OK.

**Aaron Bockelie** 2:10:50  
Um, maybe?  
Maybe we could reconvene next week the same time.

**Val Levitan** 2:11:00  
I will create a meeting invite for everybody for the same time.

**Aaron Bockelie** 2:11:06  
So let me just type out our goals. This is, this is what we've learned today and what I think our goals need to be.

**Val Levitan** 2:11:34  
So.  
No.  
So.  
Yes.  
I'm a little bit confused about specifications.

**Aaron Bockelie** 2:13:01  
Specs detail how it will be done. Requirements define what it needs to do.

**Val Levitan** 2:13:41  
Oh.  
Productivity is same as in SYMK.

**Aaron Bockelie** 2:13:55  
No sink. Like it's a it's a sink. It's a place where stuff just goes away at.

**Pavel Frolov** 2:14:05  
S input.

**Val Levitan** 2:14:09  
As a as a dump, you mean?

**Aaron Bockelie** 2:14:10  
Yeah, it's, uh, it's waste.

**Val Levitan** 2:14:15  
Right.  
I'm leaving this meeting confused, but I hope I'm the only one.

**Aaron Bockelie** 2:14:44  
So this is kind of the summary of what I understand that we need to be able to ask and what we need to take actionable steps on.

**Val Levitan** 2:14:54  
OK, I'll create a meeting new invite. I will copy this into our objectives and I will make a meeting transcript available for everyone.  
Thank you very much. I wish everybody a good day.

**Aaron Bockelie** 2:15:08  
Yeah, well, let me add.

**Irina Shishko** 2:15:11  
Well.

**Aaron Bockelie** 2:15:12  
Let me add one more little bit to this to be clear. Um.  
So when we meet next, I'm not planning on holding you, any of you, to this as being the final revision of this. It is only to be satisfied.  
Your your homework is to research the term satisfice.

**Val Levitan** 2:15:54  
Yes.

**Aaron Bockelie** 2:15:58  
It's a very weird English word, and it means to combine both satisfied and good enough, essentially.

**Val Levitan** 2:16:15  
OK, um.  
Aaron, there is one more thing I need to add to our yesterday's endeavor, so I don't know what your time is like.

**Aaron Bockelie** 2:16:29  
I've got to jump to a couple things. I will probably have some time.  
5:00 PM your time, 4:00 PM my time.

**Val Levitan** 2:16:37  
All right, but OK, let's let's let's send me a message if you are, and if you aren't, we'll do it tomorrow.

**Aaron Bockelie** 2:16:44  
OK.

**Val Levitan** 2:16:45  
Thank you. Bye, bye.

**Aaron Bockelie** 2:16:46  
Thanks guys. Bye.

**Pavel Frolov** 2:16:47  
Right. Thank you.

**Val Levitan** stopped transcription
**Claude set-up for GitHub for Front End development-20260211_081102-Meeting Recording**

11 February 2026, 01:11pm

1h 12m 59s

**Anton Seregin** 0:06  
Индекс дизайном я не нанимался.  
То есть это больше такая между проектом и бизнесом связующая.  
Звено.  
Я уже больше, как бы сказать, реализатор Того, что придумали Того, что какая идея вообще.  
Ну конкретно модули как определённого либо проекта.

**Aaron Bockelie** 0:36  
Так матчах за ребята.

**Val Levitan** 0:42  
Антон бейсик стоит мандат хэллфайр в круиз Владимирская монс энд.  
Хизма борова.  
Да, да, implementation of это я и правда данные.

**Aaron Bockelie** 0:57  
Все.  
I haven't really had a chance to just, in a smaller group, say who I am, so I'll tell you briefly who I am.  
So my name's Aaron, and I've been working with Val and Pavel and a lot of others at ABL for several years now to bring some clarity into asking how they're working and give them a lot of more modern techniques for how to operate software engineering and...  
Operations management of a software company, essentially.  
Um...  
My...  
My talent, I think, lies in using technology to help think.  
as an assistant to thinking.  
Just like I use the translator, ask you to speak in your regular language rather than accommodate me, which I really appreciate.  
But I also want to hear the real you, the closer to the truth, always, for everything. So my goal is to help use technology to uncover the truth and to bring the most essential, valuable pieces of everybody I work with to the foreground.  
That's what I do.

**Val Levitan** 2:26  
You're still looking for my valuable pieces.

**Aaron Bockelie** 2:29  
I found your value. It happens monthly or bi-weekly is usually how it works.

**Val Levitan** 2:33  
Gotcha. Okay.  
Help, help the bank account.

**Aaron Bockelie** 2:38  
Yes.  
Yeah.

**Val Levitan** 2:41  
K.

**Aaron Bockelie** 2:41  
Oh.  
There, obviously, there's more to it than that, but anyway, there's...  
I think that's kind of sets the tone for the conversation for today is using technology to go to go faster and I  
I don't know where you guys come from and your experience with all sorts of things. Anton, your mention of Linux is exciting.  
I think that...  
A.  
Our goal for the next couple, you know, time here today, this morning for me, is to just make sure that you've got the base tools set up to be able to do this sort of accelerative thinking.  
Let me ask you guys a question. Has Pavel shared with you the compiler stack diagram that I shared with people a couple times earlier in the week? Have you guys seen that yet?  
Okay, I think I'm gonna start off with that.

**Val Levitan** 3:46  
By compiler, for me to understand by compiler stack, what does it mean?

**Pavel Frolov** 3:52  
layer diagram how it was previously to produce some software product and the new design proposed by Aaron that we add in one more layer on top of a stack of tools.

**Aaron Bockelie** 3:52  
It.  
Yeah.

**Pavel Frolov** 4:12  
that based on AI.

**Aaron Bockelie** 4:15  
And I think, I think Pavel gives me too much credit. It's not my idea to invent AI. It already existed, but...

**Pavel Frolov** 4:21  
Sood.

**Aaron Bockelie** 4:23  
To to say that.  
This is how I observe us to have a thinking model to think about things, because one of the reasons to discuss in this talk here as we go through this is why are we doing this? What is the point of sitting down and talking about how to use plot code and other?

**Pavel Frolov** 4:36  
Yeah.

**Aaron Bockelie** 4:45  
AI tools, other language model tools, and what does it actually mean?  
I also want to make sure that you understand that this is not the entire universe of things. This is just one.  
Golden thread of perspective and how to think now with machine intelligence tools.  
So, ignoring the blue section for a minute.  
We all work in this space. This is where as people, as just composters, as chefs, as parents, this is where we work. We work in the real world.  
and we know what our systems and things are supposed to do.  
We have desires and we have intentions.  
And we have to programme something to change something with our intentions. I intend to do this, right?  
Intentions are ambiguous, incomplete, and context-dependent.  
Oh.  
Help me with my Russian here if you want, but that's kind of I think the trend there.

**Val Levitan** 5:52  
Yes, yes, yes, please, please make frequent stops because I needed to sync in.

**Aaron Bockelie** 5:58  
Yeah.  
The.

**Val Levitan** 6:00  
Pavel, Pavel, you should also help me to be a judge whether.  
Vladimir and Anton is grasping the concept.  
Because they will politely listen, but will not interrupt.  
And I'm not sure that they understand the concept.

**Aaron Bockelie** 6:18  
Let me go to the old way before language models showed up.  
and applied use of them, is that we went from intentions, right, to source code.  
Formal grammar, unambiguous and verifiable.  
The artifact, the human reviews, tests, and commits. That's what source code is, right?  
Ignore this part that talks about language model stuff, but...  
Right now, without seeing this, if we just look past it, humans have intent.  
Intent, you learn a language, you learn the logic, you go to school to computer science and engineering.  
And through experience, you take your intent and you create formal grammar and an unambiguous and verifiable text. This text is the symbolic representation.  
of software configuration.  
Your your source code.  
Your symbol, your symbolic language that is.  
Formal grammar, unambiguous and verifiable, goes to the compiler, right?  
This is just a review - we all, we all know this.  
Whatever that compiler is, was also built by people in software, by their intentions, right?  
Compilers are hand-engineered, optimized, and designed to convert compiled symbolic code.

**Pavel Frolov** 7:53  
Sh.

**Aaron Bockelie** 7:57  
into linked object files. These linked object files are stripped down, verified, logically created.  
And then the object files are turned into executable code, which runs on hardware.  
Hardware is physical. It is in your hand. It behaves the laws of physics and creates conditional symbolic representations of your thinking, of whatever your intent was way up here.  
You with me so far?  
Okay, well what happened?

**Val Levitan** 8:33  
Anton and Anton Vladimir, yes, no, yes.

**Pavel Frolov** 8:34  
Two.

**Anton Seregin** 8:37  
No, not not a technology.

**Val Levitan** 8:49  
OK, yeah.

**Pavel Frolov** 8:49  
Ohh.  
Just.

**Val Levitan** 8:53  
Body language from you.

**Pavel Frolov** 8:54  
Shishko.

**Anton Seregin** 8:56  
Mhm.  
No, nothing.

**Val Levitan** 9:03  
Okay, so far so good. Let's move forward.

**Aaron Bockelie** 9:05  
Okay, so now let's enter the last two years.  
The last two years have seen an explosion across the globe of using this thing called large language models. Everybody calls it AI.  
trillions of dollars are being spent, geopolitical upheaval, the loss of all sorts of things, and the gain of so many things, right? What is it?  
Well, I've decided for now, for the scope, for the sake of our conversations and teaching you guys.  
that a language model.  
is a machine that compiles natural language into source code.  
Natural language into source code is something that's never been able to be done before.

**Pavel Frolov** 9:53  
Yes.

**Aaron Bockelie** 9:57  
We can take the ambiguous, incomplete, and context-dependent language that we all live in and speak, because we are real living people, biological and constantly changing, and we can speak this biological  
Squishy way of thinking into a machine that compiles it into.  
to formal grammar with unambiguous and verifiable intent.  
This is a, this is unprecedented.  
So it takes the same shape as a compiler, but it takes input that you speak naturally in your own language that we just have been doing today, and builds an intermediate representation of what you spoke about.  
optimises what you're thinking, and emits structured output.  
It's not deterministic, it's probabilistic, and there's no formal correctness guarantees to this.  
Just kind of let you read that so you don't hear me blathering so much.  
Now, when we consider what this layer means.  
It means that the path, the number, the amount of time it takes to go from expressing our intentions to formalising them in symbolic representation here in source code can drop considerably.  
It's never perfect, right? So...

**Val Levitan** 11:33  
Maybe this is maybe this is the time to pause and maybe let let Pavel and the team just opine on the subject.

**Aaron Bockelie** 11:37  
Yeah, OK.  
So why don't you guys discuss it amongst yourself for a minute and let me know if you have questions or tell me if you find anything interesting.

**Val Levitan** 11:45  
Sure, sure.

**Aaron Bockelie** 11:55  
Pavel, I'd love your leadership to steer that a little bit too.

**Pavel Frolov** 12:21  
На выходе у нас намерения на на на входе и намерения на выходе л м у нас какого то рода код?

**Val Levitan** 12:31  
Но вследствие здесь, мне кажется, ударение ставится на том, что 1 раз в жизни у нас есть возможность.  
Транслировать намерения в какую то конкретику?  
Используя используя алан.  
Раньше это все было ампиру вас.

**Pavel Frolov** 12:54  
Музей.

**Val Levitan** 12:57  
А при использовании л. М мы переводим это в конкретику и довольно просто.  
И эффективно.

**Pavel Frolov** 13:06  
И все со структурным со структурно организованным результатом.

**Val Levitan** 13:06  
Если еще если считать что?  
Большое.  
И то есть мы мы.  
А если считать, что код это вообще байеры?  
Цифровой такой перевод на.  
Намерения на машинный язык.  
То удаляясь или или приближаясь больше к цифровому.  
Переводу намерения.  
Нам становится значительно легче, и код выходит чище.  
В разы.  
Вот на это ставится ударение.  
Я правильно понимаю или нет? Я не инженер. Я с административной точки зрения.  
Понимаю эту тему?

**Pavel Frolov** 14:05  
Да да, все верно.  
Есть какие то замечания, непонимание.

**Val Levitan** 14:08  
Ага.  
А.  
Антона и Владимир, если мы с Павлом о чём то договорились, это не значит, что вам понятно.  
Или у вас нету своего мнения, то есть сейчас.  
Я предоставляю вам слово.

**Anton Seregin** 14:28  
Ну так кто то новые слои добавился в стек.  
Соответственно, он будет его тоже есть жизненный цикл, он не сразу как бы.  
Выдаст вам то, что реально будет работать, как вы хотите. Соответственно, с каждым с каждым подходом и нет. Ну это реактивным. Он постепенно улучшает результаты. Ну это как будто с обучением в принципе. Ну у меня нет сети, она там так и работает.

**Val Levitan** 14:46  
Так точно.  
Так точно.  
Абсолютно точно.  
Согласен.

**Anton Seregin** 15:03  
Соответственно, на чем точнее по рампы чем ну, то есть фильтр в начале.  
И на каждом шаге тем результат.

**Val Levitan** 15:10  
На каждом шаге, скорее всего, на каждом шаге на каждом шаге.

**Anton Seregin** 15:12  
Результат.

**Pavel Frolov** 15:14  
3.  
Те еще.

**Val Levitan** 15:16  
Нет, нет.

**Anton Seregin** 15:16  
Да.

**Val Levitan** 15:17  
Не начальный фильтр, а на каждом шаге.

**Pavel Frolov** 15:20  
Тут ещё такое замечание было, не помню, кто то ли Антон, то ли Владимир как раз сказали, что.  
Если мы пользуемся современными технологиями, то у нас очень большой шанс.  
Получить очень хорошего.  
5 компаньона в виде искусственного интеллекта, потому что он научен на всех современных стеках на всех современных подходах.  
Вот и искусственному интеллекту в принципе сложнее работать с кодом, который там устаревает.

**Val Levitan** 15:55  
Какая интересно.

**Pavel Frolov** 15:59  
Ну, например, наш этап, который написан на и раньше он там какая там технология xjs да, который которым сейчас искусственный интеллект, наверное, только поверхностно знает.

**Vladimir Samusenko** 16:06  
Да.

**Anton Seregin** 16:10  
Это фронт, фронт в фреймворк.  
Экспресс да.  
Соответственно, ну он стал уже неактуален. Там версии уже несколько поколений сменилось там уже сейчас 7 или какая то версия, а у нас там.  
Очень устаревшие версии 3 и 4 использовать.  
Соответственно, скорее всего, модель, которая в плоде там используют дополнительную модель. Они как бы не обучались в принципе на исходниках, ну на на реальных проектах, которые доступны в сети.  
Ну и, например.  
Местная на более свежих к переборках.  
И то, что популярно в крупных ну гигантах компаниях.  
Ну.  
Там результат, вероятность, скорее вероятность результата будет намного.  
Ну предсказуемый.  
Ммм, более удачным, скажем.

**Aaron Bockelie** 17:32  
А.

**Val Levitan** 17:35  
Асенька выборе Зинаида этого раунда с концерт.

**Aaron Bockelie** 17:39  
Я.

**Val Levitan** 17:39  
Иван иваны.

**Aaron Bockelie** 17:41  
Товарами наделял.  
Она крякает, предостерег от дискотек серверы спецификой.

**Val Levitan** 17:48  
Ищет.  
Я сейчас эта ерунда с айфель нам солидарен Майкл корс Фёдор твоим portrait на интервью конца топ уэс.

**Aaron Bockelie** 17:49  
Экзамен полз.  
Я отцовой сейчас уровень.

**Val Levitan** 18:02  
Спрашивай, спрашивай плесень он на Антон скамминга спецификой.

**Aaron Bockelie** 18:07  
Угу.  
Да вроде всё дефис эй а existing.  
Ambrosia еще нагар будет клад он сайт.  
Палки чейн вина Павел адрес говорю айерс окей.  
А вот теперь want специфик экземпляр даст.  
Хочешь боковой людей?  
Ран.  
Огонек сплайн always систем наркотики солью.  
Все сиклей.  
И гайзер болтаюсь w сколько ой.  
Я говорю news.  
Я снял.

**Anton Seregin** 19:04  
Я сейчас полкило и нектаров ну.

**Aaron Bockelie** 19:06  
Здесь, то здесь пил помилуй, обрызгивать, варила тесс мёрсер.

**Vladimir Samusenko** 19:07  
Я.

**Aaron Bockelie** 19:13  
Есть папы онлайн, боитесь протеин дилогии?  
Вот так партию и вижу икры я.

**Val Levitan** 19:26  
Павел, вам нужно по Павел, вам нужно, наверное, помочь переводе, потому что здесь он и эрин идёт в правильную сторону.

**Aaron Bockelie** 19:26  
Все.

**Anton Seregin** 19:27  
Чтобы.

**Pavel Frolov** 19:35  
А.

**Val Levitan** 19:36  
Но я боюсь что.  
Потеряется контекст.

**Pavel Frolov** 19:41  
Арон хочет рассказать о том, что ну тоже есть разные подходы к работе с инструментом и ну все, как правило, начинают с 1 шага, когда начинают часто и много делать запросов в искусственный интеллект с прямыми просьбами. Напиши для меня там резко p и там такой-то, который делает то-то.  
Потом получает на выходе какой-то результат, смотрит там сам тестирует.  
А что то замечает, говорит, вот здесь у тебя неправильно. Вот здесь поправь. И вот таких таких вот очень много проектов.

**Aaron Bockelie** 20:21  
Все целый контейнер, подаренный, стали prompting. Спасибо.  
Была канцлер, я частый.  
Из-за евреи священник paws планируете?  
И гафт интерньюс из сериала таймере xlsx www.  
Сбой мочой артеке, а при эксперимент прямой аквариуме.  
Это правда спекала лол абстракте ision лайк лайк.  
Парень каур энсон мой лайк.  
Парень иванчин.  
А вот они да они и рецепта.

**Val Levitan** 21:06  
Попала пас пас пас.  
Papas.  
Ключи ключевой элемент ключевой нужно обязательно, чтобы врубились потом.

**Pavel Frolov** 21:19  
То есть здесь здесь уже здесь уже получается, вместо Того, чтобы когда вы знаете фреймворк и вы хотите, чтобы в этом фреймворки искусственным интеллектом что сделал? А здесь вы просто говорите намерения мне надо что-то.

**Val Levitan** 21:19  
Павел, только прошу вас.

**Pavel Frolov** 21:34  
А искусственный интеллект уже может за вас принять решение. Там вообще какие фреймворки использовать там, например, или предложить какие то там решения?

**Val Levitan** 21:43  
То есть меньше указаний, а больше намерения, то есть пойди принеси сделай убери.  
Памяти.

**Pavel Frolov** 21:52  
Ну здесь здесь, кстати, ну если мы работаем уже с готовым проектом или если мы уже знаем, какие мы будем использовать текст так, то как раз тут важно сказать, что сделаем мне там ну или предложи мне что-то, но ты ограничен использованием вот этих вот, например, фреймворков.

**Val Levitan** 22:13  
Но я понимаю это, но в смысле указания интеллекту.  
Другого стиля идет, я хотел бы достичь вот этого.  
Или помоги мне продумать вот это.  
Говоря, да.

**Aaron Bockelie** 22:38  
Стал.  
По basinger сдать.  
Инвертирую сэйди steinway.  
Приказная навыков fulfill.  
По этой давала поэкспериментируй.  
Вот эту стингер.  
Nowhere in this is there really a need for AI yet? This is just us working. I could sit with you Vlad and say make me a REST API with these endpoints. Maybe it's more Anton, but.  
Anton, build me a REST API with these endpoints and I say, OK, I'll see you in a week and you're like, good, I got it. And you go and do your work, right? But now I also need to make sure that we also do all these other things too, and I need to tell you all these other things. They're in the user's.  
Story.  
As we mature, we begin to formalize the the language that it takes and the and the techniques and the way we go about doing this. So instead of saying go do some linting, I just say NPM run lint right?  
I don't haphazardly ask for things to be done. I say this is the formal way that we do it and we use a software tool to do this.  
Tools are being created.  
The total amount of burden in this environment remains the same. So if we think about AI as the intention compiler, we can throw these things to the AI tool for our intentions just the same and the amount of prompting the amount of.  
Explaining and checking and doing drops for any language model coder. We are abstracting our our ask to the language model and then further along at some point I just say.  
Add a user's endpoint. I need a user's endpoint for my application. Well, guess what? We have all these software frameworks to check things. We have the testing, we have linting, we have end to end testing, we have type checks, we have validation.  
Maybe integration, validation, whatever that might be.  
The tooling framework we've created carries the context for us rather than having to manually type it out on every session.  
That's the maturity, the increase in automation of intentions here.  
Now there's a trade-off for this, just like the young tree is very flexible and can bend, and the big tree is strong and and resist movement.

**Pavel Frolov** 25:29  
Yes.

**Aaron Bockelie** 25:31  
Once you've formed this framework, it's a little bit challenging to change it. And So what I'm going to tell you is, is that we don't do anything different than any other conventional mature software engineering company would do.  
That's the that's the big secret. We don't have to. We just follow the convention that everybody else does to write good software. All the automation, all the documentation, all the integration, all the DevOps.  
Good practices to do things with. They're already written and known. There is no mystery for this.  
So any questions about why I said that last bit like that?

**Anton Seregin** 26:36  
We will scan it now.  
Сделанных вещей.

**Aaron Bockelie** 26:52  
Сейчас.

**Anton Seregin** 26:54  
Ну Ну вот у меня допустим вопрос более практичный, скорее. Ну то есть как бы основной принцип, я как бы уже всё знал, понимаю, что есть поводы.  
Эээ как вот эти при реквизите с нужно выбрать, создать и ограничить яй.  
Контексте прилог нашего приложения, чтобы.  
Не повторяться, и чтобы оно себя само ограничивало.  
Ну встать кантам не подходами.  
Чтобы это чтоб вот такого плана вещи, как добавить новый endpoint?

**Aaron Bockelie** 27:28  
Я.

**Anton Seregin** 27:34  
Приложение.  
Оно, ну то есть это намерение правильно отрабатывало или с.  
С постоянным ну плюс минус результатом.  
Ну, либо если нам нужно добавить новый экран.  
То есть нужно нам организовать такую среду, как я понимаю с ограниченными.  
Ааа, ну то есть мы ограничиваем фреймворк библиотеки, с которой мы хотим, чтоб.  
В клод а.  
Отработал и выдал результат.  
Вот, наверное, к этому мы стремимся сейчас.  
Такой абстрактный лень. Вопрос практичного.

**Aaron Bockelie** 28:20  
Это как?  
Май переводит палки, очищает, доставила как Индию диспетчер.  
Ригорист, сэндвич сэндвич.  
Акция очень а давай.  
Ошибется и опять голос и осень.  
Sandwich and Anton, I'm trying to address what I think you're saying in the translation here is that we have a particular role that machine intelligence does for us. It's in the middle right here.  
So we have as humans have to define and curate the problem to solve. We have to frame that problem, and when we frame it this way, we're actually framing our intentions. The problem is our intentions.  
We then let the the machine intelligence write solutions and iterate rapidly and explore possibilities based on what our intentions are, based on what our problem is.  
Not every single one of them is correct on the first try. Some of them are a little different, but on the whole, the time it takes to create this is a fraction of what it takes for us to do it correctly the first time as humans.  
So what this turns into is if we can create.  
At speed and scale, 10 variations of the same thing, 10 iterations of the same problem.  
And even that 10 iterations is less time that it takes for us to do it once. And we know that every time we run an iteration, it filters it and filters it and filters it. It refines it over and over.  
Until there's nearly nothing incorrect with the with the output.  
That's an acceleration overall of our intentions. And So what we do is we review and decide.  
We refine the requirements, we refine the steering and the controls, and we go through this until we accept it and move on.

**Pavel Frolov** 30:34  
Yes.

**Aaron Bockelie** 30:42  
And what I'm going to be showing you here in just a minute, we're going to switch gears a little bit to get a little more technical, is that there are ways to automate the refinement of this, which are related to what we were just seeing there, OK.  
So let's let's talk for just a minute about this guy here, and then we're gonna go and move over to talking about a ways framework and how to do things.  
This is the last piece out of this I want to share with you guys and I think this is really important because it is a direct real example of how I expect you to work coming with with these tools and with the team.  
So in the real world, in your office there, you might have a whiteboard, or you might have a coffee cooler, or maybe, you know, an area you talk, even a meeting room, and people discuss a thing.  
You talk about it. You write notes. You write on a whiteboard. Maybe you record it. Maybe you're on a video call.  
Coding agents have no access to this at all. No access at all.  
And what we want to be able to do is we want to be able to remember what we did. So every person in this conversation, in this discussion or debate.  
Has an opinion on what happened.  
And they can discuss this ideally with the code base at hand. So if you're discussing what API gateway we're going to put together for what service, and this is clearly in some actual code base, you can then bring up your development environment with your coding agent and as different people, different roles.  
Seeing the code base, you can discuss this with your coding agent. You can do this on your own too. There's no reason to use the robot. You can just use your own brain.  
But when you discuss it this way, it goes a lot faster. You can explore the space and you can understand nuances much faster than you can if you're doing it by hand. And there is no requirement to use this or not if you are competent.  
And confident.  
What's the word for confident in in Russian?

33:10  
Ovidian list.

**Anton Seregin** 33:12  
Didn't.

**Aaron Bockelie** 33:13  
OK.  
If you're confident in your output, this is the most pure piece of information that you can give is what you are confident about, but we.

**Val Levitan** 33:25  
Or confident.

**Aaron Bockelie** 33:27  
Confidency.  
Along is is contrasted with effort. It takes a lot of effort to be confident all the time.  
To be, you know, well, the right kind of competent. And so we can use these to amplify our confidence essentially. So what we do is we we take our ideas here and we share them in our shared space.  
Now in this example, I'm saying this is in, this is in GitHub. We want to stay as close as possible to the conversation at hand about whatever technical thing was going on here. We're pretty down. We're down in the the technical application and creation of something.  
On in in the businesses asked us, we need this. We need to discuss and debate this. This structure is no different than how it's always been. If you didn't have the robot language tool here, you would discuss this in GitHub, ideally in the.  
In the ideal space in the high functioning software engineering team, your discussions would be in GitHub, not around the coffee pot or out on this out at a park because you need to capture these.  
Ideas and you have to capture these decisions.  
Any decision that's spoken into the air disappears immediately, and any decision written in GitHub is is available for for capture by other things.  
The responsible person for this can then use their own AI agent to harvest all of this information. And perhaps Anton, you wrote down something without an AI language model just on your own. You spent the time to do that because you realized you were a domain expert.  
Here.  
It's put up into the space as just the same as anybody who used the language model to do their work as well correctly. And then what we end up with is a decision of architecture for the whole product. The whole platform gets integrated from all of these people and Irina was able to use the same.  
Flow the same sandwich flow to develop this architecture document from everybody's opinions. She can then recycle this and review this with the people and you have this loop to be able to review it and accept it.  
So what this is is essentially nested versions of this.  
Some of these versions is just people all the way through and some of them use the A I to go through and we nest these these things. We can talk more about that later. So let's go, let's I want to, I want to before I go any further, is there any question about what I'm saying when it comes to?

**Pavel Frolov** 36:11  
Yes.

**Aaron Bockelie** 36:28  
Harvesting the the, the, the discourse and the discussion from people into a platform. Do you know what I mean? Why that is valuable that way? Do you have any questions about that?

**Vladimir Samusenko** 36:56  
Product close on the Goria is up.  
На некоторых литературу.  
Исходя из наших зон.  
Ответственности, скажем так.

**Aaron Bockelie** 37:28  
Я ем сам тайне, имея в обзоре вклад сдать на Борис, говорит варенья крутой сериал.  
Концерт если завейте мякит изи.

**Pavel Frolov** 37:46  
The.  
No, yep.

**Val Levitan** 37:54  
Okay.

**Pavel Frolov** 38:09  
Да и вообще в мире да он не ограничен только общением.  
Тех людей, которые лучше всего знают этот продукт или знают этот язык.  
А.  
Если какая то тема обсуждается и есть там несколько человек, которые это обсуждают. Если каждый из этих там пятерых человек запишет.  
Там с искусственным интеллектом или нет запишет?  
А какие то основные моменты этого митинга и выложит их, например, в гит хаб и все 5 человек так сделают у искусственного интеллекта суммарно где-то будет. Ну реально софт трус, хотя в каждом отдельном случае наверняка будут ошибки.

**Val Levitan** 38:55  
И может быть, стоит добавить, что из нашего опыта.  
А.  
Ну, когда мы только начинали это делать, у нас наши митинги проходили сумбурно.  
И мы не могли пользовать мы мы плохо пользовались ключевыми словами, которые помогают интеллект.  
Ну.  
Отловить вот эти архитектурные решения?  
Из разговора.  
Но чем глубже мы?  
Продумываем вот как правильно выйти на эту правду, тем лучше мы используем легче. Мы используем терминологию.  
И и если суд учётом, что если этот разговор записывается, транспортируется.  
То искусственному интеллекту легче поймать эти слова. Например, мы пользуемся словами как там.  
Архитектура проекта или архитектурное решение или ещё техническими словами, которые помогают выловить этот наш нашим направлениям, и оттуда естественно, легче вырисовывается, правда?  
Потому что сам разговор ещё не является правдой, это просто источник.  
Но из него надо еще выложить правду.  
Ну да, Павел действительно правильно сказал, что если каждый из нас.  
Для каждого разговоры.  
Внесет свою лепту то целиком из 5 разговоров.  
Искусственному интеллекту легче будет создать свою правду.

**Aaron Bockelie** 40:44  
Там гора корейцы.  
Америка и так и не дал на это никто из импорт экспорт.  
Так персон.  
Орехи патэс.  
Супеси клей.  
A meeting transcript, right? This is the reality of what actually was said. There is no opinion of whether it was right or wrong. It was just spoken, right?  
This provenance of reality is an artifact that everybody has access to, and you can go back afterwards and ask it questions on your concerns of the meeting or the conversation if you were a participant in that meeting.  
You can, you can, you can distill out of it what your perspective was for it, and you can then write up very quickly a decision or a change or another artifact that comes out of that that impacts.  
The topics you were discussing rather than just talk about it. Just talking about stuff is not very helpful, but if you can form an opinion and put it in place, that's how you change, change things, how you advance the the the state of affairs.  
А.  
То ладоши стервенея.  
А.  
Овацию мы тебе?  
Apparent фондю болтай вклад они мужчины.

**Anton Seregin** 42:50  
Я живу сейчас в конфигурацию клоун ппц, но я вессель парни можете видишь в россель.  
Изобронтам.

**Aaron Bockelie** 43:03  
Энд aion собственным xl.  
Я на рекс ворью, играющий на лопате.

**Anton Seregin** 43:12  
Currently we use Windows and the VCL like subsystem Ubuntu operation system and quote code running on Ubuntu.

**Aaron Bockelie** 43:28  
OK.

**Anton Seregin** 43:29  
And.

**Aaron Bockelie** 43:37  
Like my network is breaking a little bit.  
Doesn't always work perfect.  
OK, So what we want to do here is we will come back and visit the diagram I'm trying to create about that curation of of of conversations.  
Do you are you aware of this repo and how it's configured? Did did uh everybody see it?  
Pavel's nodding his head yes, but I need to kind of understand if everybody else is aware of this.

**Pavel Frolov** 44:18  
Anton Vladimir.  
At uh, repository is waste.

**Anton Seregin** 44:35  
Yeah, the knowledge, knowledge updates.

**Aaron Bockelie** 44:40  
Yeah, kind of. Yep.  
So a few things about this, and Pavel, this is mostly for you as soon as possible, and in fact I'm gonna force it next steps right now. You guys can't passively receive this from IT team. You can't just assume it's installed and configured. You have to know it exists.

**Pavel Frolov** 44:49  
Yes.

**Aaron Bockelie** 45:04  
This and work with it because each person's config will be probably a little different and everybody needs to be an active participant, an active contributor to this back to the ways that you guys want.  
So this means that you're forking this, I'm guessing. Let's see who's forked this right now.  
So none of I don't see any forks from you guys.

**Pavel Frolov** 45:32  
Actually, as Andrei said, we do not have an ability to fork it and Andrei actually just copied and posted this repository to our internal.

**Aaron Bockelie** 45:40  
So.  
Mhm.

**Pavel Frolov** 45:48  
And makes updates when when he see updates on your site.

**Aaron Bockelie** 45:54  
So, so here's what you're going to need to do following up after this. You need to configure your GitHub Enterprise environment to allow forking of public repositories. You must.  
Now if you can then do that, you need to have a way to stay up to date because the version of the ways that you're using is out. I know it's outdated because I daily fix this thing and improve it as I learn and create stuff. It is dynamic and happening.

**Pavel Frolov** 46:10  
Yes.

**Aaron Bockelie** 46:24  
All the time there was a fix. Let's see here. Let me let me push some up here just to be aware of it.  
So I'm going to make sure that I have everything pushed to remote as an example.  
This is essentially my releases for this and by you guys.  
You guys need to then, by having your fork, can choose when to synchronize that fork, right?  
So let's let me just show you here.  
Get this figured out here.  
Oh.  
O.  
Basically, about every day I'm making commits. 5th, 6th, 9th, 11th. I don't know when it was cloned, but there's a lot of changes. This is only from the 4th, right?  
So I'm constantly tuning and adjusting this against all of the other projects and work I'm doing. I'm doing a ton of work on other stuff that you don't see. So this is growing and maturing in the space for this. I'm not saying it's perfect and I'm not saying it's the one true way.  
But I'm saying this is the first one. This is your Is anybody ever remember their first car they bought?

**Val Levitan** 48:16  
Don't go there. They they don't understand. No, they please, but they get lost.

**Aaron Bockelie** 48:17  
Or own. I'm just saying.  
The first, the first big thing you've owned, you always remember for your entire life, and this is your first introduction to it for a managed system right now, probably. And so you can use this one to start with. This is your training wheels, and eventually you'll move on to something better, hopefully.  
But what we need to be focusing on is 2 pieces of this system. The 1st is skills and skills is part of Cloud Code. It's a it's a first class product feature from Cloud Code.  
That allows you to add skills and skills are essentially a descripcion of how to do something. OK OA skill is explain code.  
And you explain code with visual diagrams and analogies. Teach how code works. Teach about a code base. This is when you use it. And when explaining code, always start with an analogy, draw a diagram, walk through the code.  
Highlight a hitch or a gotcha about it.  
This is built into quad.  
What is not built into cloud is why we explain code this way.  
Why do we do this this way? What is the point of explaining code this way? Well, there's a way we do it.  
And this is what Waze covers.  
So when we look at Waze, this is an extension to Cloud code that I've built.  
And we're going to go into this a little bit.  
And when we when we talk about ways, the way we do something, here is the way we do design work. When we start thinking about how to design something with in cloud code by creating a design, an architecture, something like that.  
This is the way we do it. This isn't how, which is what a skill is. This is why we do it. And this guidance is the context that's missing in most cases to steer agents in a predictable manner.  
So when we look at the different ways in here, here's the documentation way.  
We write this in markdown, we use language appropriate docstrings and code, and we use Mermaid for diagrams.  
They're not arbitrary choices. Markdown renders everywhere, blah blah blah. This is the way we do it.  
This would be like explaining to the the junior engineer or the new engineer about way we do stuff. Let's look at GitHub for just a minute.  
When we do pull requests, let's look at this in the raw form.  
We always do pull requests. We use PR pull requests for all changes, including solo projects, and a pull request without reviewers still has value. It's a decision record, a continuous integration gate, and a muscle memory for when the project grows.  
Working solo without ull requests is like doing research without keeing notes.  
See, this doesn't tell Claude how to do a pull request. It tells why we do a pull request.  
You see the difference?  
O basically.  
Pavel, you need to help make sure we get.  
Andre set up with the pipeline for this rather than the static version that's two weeks old.

**Pavel Frolov** 52:23  
I I will force force him to make this option.

**Aaron Bockelie** 52:24  
And.  
And Vlad and Anton and Pavel, if you begin to understand how this is an overlay on top of default install of cloud code.  
You realize that this actually becomes a way to influence everybody who uses cloud code in a consistent manner.  
So let's say that you are doing some work, right? And you're using this all the theories that we're talking about, collecting information, developing lots of software and doing reviews and all the things and you find in your daily practice of pairing with cloud code.

**Pavel Frolov** 52:58  
Yeah.

**Aaron Bockelie** 53:11  
Rode that it has this one eculiarity that you don't like. You can correct it by creating your own way for it. You say actually this is the way we do it and I need to add this way.  
You add this way to your local installation, which is a git repo clone of the Waze system that's in JVL's repos, and now you can go and use the exact same process I'm talking about when we go through.

**Pavel Frolov** 53:39  
Yes.

**Aaron Bockelie** 53:40  
Uh.  
Where is it? One minute.  
When we do this process for a pull request, when everybody reviews the pull request and says yeah, we like this pull request, let's do it. Or if you don't even use robots, you just look at it with your own eyes and add some comments and approve it.  
Now when you're changing the ways you can incorporate, you have a form of governance. And do you know what I mean by governance in this space? Is that does that make sense?

**Pavel Frolov** 54:19  
Not, not sure, not sure that I understand.

**Aaron Bockelie** 54:22  
OK.  
So governance is a form of bureaucracy. It's a it's a way to say bureaucracy. And governance means that let's let's pick. I'm going to pick a go ahead.

**Val Levitan** 54:38  
Put put you what detail.

**Aaron Bockelie** 54:48  
I'm going to pick.  
The release way. OK, this is a form of governance. Remember, you guys have lots of products you release, and if we think about what it means to write a release, think of Pavel. Think of how many meetings we've had about defining releases.  
Version numbers, what it means, how to describe it, blah blah blah. All this stuff all the time. It's kind of a mess.  
If we have a single place where we can define the release way, it's right here. So this is my release way and you guys should change change the ways when you fork it to make it your release way of course.  
But I just want to say I want to keep a change log. I want a version bump where features and breaking changes.  
It is major any or larger than feature is a breaking change is major. Any feature is a minor and fixed docs is tours is patch versions. That's that's my rules. They're very simple.  
This is a form of governance because if you have this one on everybody's computer cloned with this exact document and two, people are regularly pairing with their coding agent to understand what they're doing and and and creating work.  
Those that are managing releases of some kind will have a consistent messaging about how releases are done injected into their into their work.  
When we look at the raw file for this way, this is the patterns that we see for a release. So in the conversation with a coding agent, if any of these patterns match even closely or loosely.  
This way is injected into the context of the conversation for the agent. And so when when you as a release manager say let's do a release because you've already established your tools to do releases, right?  
If you have a mature code base, you have tools in your code base to make a release, right? You could literally Tye make release and you're in a mature environment.  
And as soon as you say those words, you say let's make a release pod code. This gets injected, the make way gets injected, the GitHub way gets injected. It has all of this understanding of the way we do it is added and you don't have to type any of this stuff in because it's there already.  
And then you have the tools and the skills. Remember the skills exist and so knows exactly what commands to run and how to run them for your particular release cycle thing.  
So basically we're getting all the way back to.  
Let's find it here.  
One minute. There we go.  
In this model again instead of doing a release like this.  
We're doing a release like that. Do a release.

**Val Levitan** 58:09  
Yes.

**Aaron Bockelie** 58:09  
And then you can, you can follow up with all this. You just have to read it and ensure it's doing the right thing rather than manually doing the work. You're still allowing it to happen. You're still gating the process because there's only one, there's one, there's one responsibility still that still exists with you as the human.  
You are responsible for accepting the output of this because it's on you. Machines are not accountable, right?

**Pavel Frolov** 58:36  
Yes.

**Aaron Bockelie** 58:40  
OK.  
So I'm gonna briefly talk.

**Pavel Frolov** 58:43  
Um, what was not? Yeah, yeah, yeah, yes. No, you see, process process.  
Искусственный интеллект вызывал нужные команды, чтобы делал для нас полезную работу на в качестве примера. Если у нас качественно расписан.  
Хук, который обрабатывает, например, ключевое слово релиз и там описано, ну мы написали, сделай для нас новый релиз, и он правильно вызовет, например, утилиту этот jh, который вызовет экшн, который запустится в гите и ну, сделает весь цикл релиза в гите.

**Val Levitan** 59:48  
Браво Павел 2 найс.

**Aaron Bockelie** 59:52  
Вы говорите быстрей лохматый отписок вкладывают конфет вот через уровень был.  
Если ась а ты ф.  
Юрец.  
That's not it.  
OK.  
This piece right here is really important.  
I'm not expecting you to do all this right now, but this is part of me teaching you why Cloud Code Config and why the Waze system does what it does.  
You have to remember that this exists, because otherwise there's no...  
There's no steering of why Waze works, okay?  
The very beginning of any of the way you do things is based usually on regulatory perspectives. It's based on a specification.  
The very code you write in a language that you write in to create software is based on known regulated specifications.  
And we can find those and we can point to them at some point. Not always perfect, but the provenance is there.  
So what we have then is external to JVL. JVL never invented these. It just rides on top of them.  
Uh, regulatory frameworks.  
So let's just say you're doing financial processing payment systems on your software. You're creating that software.  
Very likely you want SOC 2 compliance in the United States, or at least a provable auditable chain that you were embodying SOC 2 method in your software to make sure that you're auditing your transactions correctly.  
You can build this system out to allow that Waze guidance to be based on OC 2. You can take OC 2 in its entirety.  
You can extract the relevant pieces that are control requirements. These are requirements. I've harped on everybody at JVL for requirements for a while, but this is where requirements can actually be incorporated into the day-to-day and minute-to-minute operations of working with a language model coding agent.  
If we have the original regulatory framework, and then we have the control requirements established and written down.  
We can then create the policy document about that.

**Pavel Frolov** 1:02:47  
The.

**Aaron Bockelie** 1:02:51  
And then the policy document is distilled, compiled, revised into a way.  
Of guidance, and then it's injected into the agent.  
So...  
Let's think about the natural language.  
thing for something right now, okay?  
When you say...  
Uhh...

**Pavel Frolov** 1:03:18  
Yes.

**Aaron Bockelie** 1:03:18  
Is everybody familiar with with?  
Let me think of something here.  
In the CMS or the, what's, Pavel, help me out for just a little bit because I'm having a little bit of trouble connecting here. What's a domain specific thing that everybody on this call would know about when it comes to creating slots machine games? So SAS is a protocol that I know of, slot accounting systems.  
right? So things have to talk fast, yeah?

**Pavel Frolov** 1:03:50  
Okay, yeah.

**Aaron Bockelie** 1:03:54  
So when we think about SAS.  
We don't think about the whole stack. We usually say, well, it needs to talk to SAS for this thing. Okay.

**Pavel Frolov** 1:04:01  
Yeah.

**Aaron Bockelie** 1:04:06  
But we don't ask all of the provenance as to why SAS even is necessary.  
There's a state in the state of the United States that says you must speak SAS, otherwise you can't run your machines in our state, right? Like that's probably some regulatory framework.

**Pavel Frolov** 1:04:23  
Yes.

**Aaron Bockelie** 1:04:24  
And then eventually it becomes a requirement. Must run SAS. And then eventually it becomes a policy. All software interacting with the accounting system must speak SAS. And then eventually it turns into a WAV file. Any configuration tools, the way we do this is we use this library to do stuff.

**Pavel Frolov** 1:04:27  
I.

**Aaron Bockelie** 1:04:45  
that happens to include SAS as the library. And then the agent context gets injected when they talk about communication of something. Hey, when you're implementing communication soft functions, use this library.

**Pavel Frolov** 1:04:46  
Yes.

**Aaron Bockelie** 1:05:01  
So I've worked from the regulatory level, the regulatory framework, all the way to context injection for doing work. And it's traceable now.  
Because we can say that this gets injected in this repo, which was called at this point, which was called at this policy, which was called here, which was called from here. This call stack is very deep, and it's paralyzingly deep. No regular developer thinks about this whole stack every single time they're implementing software.

**Pavel Frolov** 1:05:33  
It.

**Aaron Bockelie** 1:05:34  
But what we have is the beginning of the framework to be able to truly actually run traceability analysis on the prompts that we're putting inside of our code that end up in commits to be able to know what we're doing.

**Pavel Frolov** 1:05:49  
Yes.

**Aaron Bockelie** 1:05:50  
I'm not saying it's finished. I'm just working on it. And I've been building this specifically thinking about you guys and the regulatory challenges that you will have when writing software.  
And so this is something for you guys to realise that is inside of this repo and exists and can be ran and used.  
No.  
I don't want to go into too much more detail than that for that, but you know, this is kind of trying to remember where I put the...

**Pavel Frolov** 1:06:26  
Yeah.

**Aaron Bockelie** 1:06:26  
Governance, but here is an example of.  
No, I guess that's not it. I can't find it. Anyway, we'll move on now. So at the end of the day.  
Your goal is to understand that this exists, know how to use it, and know how to manipulate it and deploy it yourself. You can't just like let it sit there and assume that Andres is managing it for you.

**Pavel Frolov** 1:06:54  
Sood.

**Aaron Bockelie** 1:06:59  
You wouldn't let Andrei manage your VS Code preferences or your compiler directive preferences, right?  
If we think back about what I'm telling you is that the language model is a type of compiler. And I think pretty much every software engineer ever doesn't let the IT department manage their compiler configuration.

**Pavel Frolov** 1:07:23  
Yeah, it's clear.

**Aaron Bockelie** 1:07:24  
Because otherwise it'd be a mess.  
Hey.  
Um...  
I'd like to shift gears now to talking about my...  
Browsers hung, so I don't know if you can still hear you guys.  
Back.  
Okay, now it's back. Sorry, I'm not sure what happened there. So I'd like to now shift to really kind of talking about how are we going to move past the Figma environment and the language and the Git repo and the other things that are existing in that space to.  
apply some of what I've just been talking about.  
So, Vladimir and Anton, which of you are currently working in the repos that we're thinking about the project?

**Pavel Frolov** 1:08:29  
Which one?

**Anton Seregin** 1:08:33  
Mm.  
No, not.

**Pavel Frolov** 1:08:36  
The.

**Anton Seregin** 1:08:41  
Okay.  
Shpak.  
Fine, you know, not logging me, it's just.

**Pavel Frolov** 1:08:48  
Yeah.  
It was, it was, actually, I think Vladimir is working directly with setup screens on the machines.

**Anton Seregin** 1:08:58  
You.

**Vladimir Samusenko** 1:09:06  
Local Games, Seregin.

**Aaron Bockelie** 1:09:08  
OK.

**Pavel Frolov** 1:09:08  
Yeah, to transfer from old setup design to newer, newer design was designed using Figma.

**Aaron Bockelie** 1:09:23  
Mhm.

**Pavel Frolov** 1:09:26  
What Anton is working on, he is working with a new project related to Flex POS, server part, registration.  
What else? Location management, a part of this design is not ready yet.  
And I guess it will not be finished in the final stage. And at some moment, we will have some screens.  
Um...  
prepared in Figma just static images, I would say, and we will need to transfer them to graphic user interface screens, layout, and business logic.

**Aaron Bockelie** 1:10:19  
OK.  
So let's think about what we just talked about, the developer experience and the tools for that. I'm just going to pick one aspect of it. How are you going to verify that every element that you're creating exists as testable?

**Pavel Frolov** 1:10:22  
S.  
****.

**Aaron Bockelie** 1:10:40  
Are you going to test that front end to make sure it's all as of the correct contracts?

**Pavel Frolov** 1:10:49  
Yes.

**Aaron Bockelie** 1:10:49  
And where have you defined your data contracts between the API server, the back end, and the front end to represent them?

**Pavel Frolov** 1:11:01  
Two.

**Anton Seregin** 1:11:05  
Uh, this is the product.

**Pavel Frolov** 1:11:20  
Okay, let's focus on the current project you're working with.  
Ohh.  
Example, saying about Flex POS and.  
Hotels.  
Infrastructure orchestration.

**Aaron Bockelie** 1:11:41  
Pavel, is this is this going to be Flex POS eventually?

**Pavel Frolov** 1:11:46  
Yes, actually this part relates to a particular device.

**Aaron Bockelie** 1:11:47  
Okay.

**Pavel Frolov** 1:11:54  
Yes, Anton will implement graphic user interface for main screens.  
Implementing logic, and the second part will be implemented on the server side to support registration of each particular FlexPOS device.

**Aaron Bockelie** 1:12:08  
Mhm.

**Pavel Frolov** 1:12:17  
registering customers, registering location, manage customer and locations, assign the POS device to location.  
provide some reporting for each customer and so on.

**Aaron Bockelie** 1:12:38  
Val, is there any way to stop the recording and start it again and get that last bit that Pavel just said and paste it into the chat?

**Pavel Frolov** 1:12:38  
This is.  
Just.

**Aaron Bockelie** 1:12:50  
Because literally what he said was gold.

**Val Levitan** stopped transcription
# Raw Transcript — Genadi — Components repository structure and monitor sourcing savings
**Date:** November 26, 2026, 07:31 PM - 07:52 PM UTC
**Source:** Claude Meetings (project 01a21955-8d82-70fb-862b-45a15d85c459)
**Summary note:** [[Meeting_Notes_Genadi_Components_Repo_Structure_and_Monitor_Sourcing_Savings-November-26-2026]]
---
💬 **[07:31:32 PM] Claude (chat):** _Val added me to help! I save a transcript, summary, and screen descriptions for you to revisit._

**[07:32:02 PM] Val Levitan:** (not confirmed) Okay. Genau, die.

💬 **[07:32:10 PM] Claude (chat):** _Welcome, Genadi. Val added me to take notes and help out._

**[07:32:12 PM] Room:** (not confirmed) Ähm, ich, ja,

**[07:32:39 PM] Val Levitan:** (not confirmed) so it's a it's a conversation uh, mainly for my uh, for my benefit.

**[07:32:48 PM] Room:** (not confirmed) М- Мне нужно

**[07:32:53 PM] Room:** (not confirmed) для себя немножко разобраться.

**[07:32:56 PM] Val Levitan:** (not confirmed) Скорее всего, что я- I'm asking for help instead of uh, it's not a direction. Okay?

**[07:33:07 PM] Val Levitan:** (not confirmed) Ouais. So, I opened uh, GitHub там, де ви работаете.

**[07:33:16 PM] Room:** (not confirmed) and I went to documentation manuals

**[07:33:22 PM] Room:** (not confirmed) in GitHub,

**[07:33:28 PM] Val Levitan:** (not confirmed) and I went to, uh, ну, неважно, любой я открыл, happened, и просто happened, что я открыл CM08 Flex Manual,

**[07:33:38 PM] Val Levitan:** (not confirmed) Мгм. and I kind of went through documentation.

**[07:33:47 PM] Val Levitan:** (not confirmed) So, я вижу, что там documentation in doc and PDF,

**[07:33:53 PM] Val Levitan:** (not confirmed) which is probably Я не знаю, наверное, это имеет смысл какой-то, но окей, вы как бы дублируете это.

**[07:34:04 PM] Val Levitan:** (not confirmed) Ну, это неплохо, потому что PDF открывается прямо в viewer, поэтому удобно смотреть.

**[07:34:10 PM] Room:** (not confirmed) Ну, Окей, неважно.

**[07:34:12 PM] Room:** (not confirmed) Я пока не понимаю, нужно ли иметь и PDF, и doc,

**[07:34:17 PM] Room:** (not confirmed) Наверное, я бы пошел бы только с PDF, но окей, неважно.

**[07:34:25 PM] Val Levitan:** (not confirmed) А вот передо мной открыт PDF Top Speaker Lights for V43 Assembly.

**[07:34:33 PM] Val Levitan:** (not confirmed) Ам, У меня здесь, скорее всего, есть много вопросов.

**[07:34:42 PM] Room:** (not confirmed) Во-первых, когда мы говорим про flat view,

**[07:34:50 PM] Val Levitan:** (not confirmed) я хочу, чтобы мы как бы понимали, что такое flat view. Вот то, что вы сейчас показываете, CM08 Flex Manual, это то, что вы называете flat view?

**[07:35:09 PM] Room:** (not confirmed) Ам, Я, э, извините, ф- Flat View, ш- м, что Ну, такое? flat, flat, то, что мы сказали, мы просто делаем один flat list of parts. О, так подождите, стоп, стоп. Manuals это вообще не part of this, э, кон- this flat. Это manuals, это вообще для production. They need every day to use manuals. They- otherwise they cannot Окей, work. окей, окей, им нужно или нет, я пока оставляю, неважно. Я, я- я не хочу заходить в это. Это вообще не part Я, of я нашего открыл, Flat View. я открыл не то, что надо. Окей, понял, спасибо. Фу. Легче.

**[07:35:43 PM] Val Levitan:** (not confirmed) Окей, так что я должен был открыть?

**[07:35:46 PM] Room:** (not confirmed) Мы идем parts, и в основ- у нас все, что я делаю, вот то, что мы договорились, Что это такое, components. Components.

**[07:35:55 PM] Genadi Peari:** (not confirmed) а, я иду в components, Yes. и куда я иду? Все, в components сделаны folders. Это потому, как мы и agreed. Per О, ca- categories. И в каждой категории там уже разбито по, как мы, по нашим rules, а, сделано part numbers, потом contracts, либо сначала а, manufacturers, потом contracts, э, потом part numbers. Все, как мы договорились. Ну, посмотрите.

**[07:36:25 PM] Room:** (not confirmed) Yeah, yeah, yeah, yes, yes, yes, yes, yes, yes, yes, yes. Secunda, aşkım, secunda. Дайте мне пару минут, одну минуточку.

**[07:37:21 PM] Val Levitan:** (not confirmed) Окей, ну это намного лучше, намного. Сейчас, окей, это день и ночь. Но хорошо, вопрос можно? Да, конечно.

**[07:37:29 PM] Room:** (not confirmed) А, вот я открыл Bowie монитор, ну, просто Окей. первый. Не знаю, почему я открыл, но вот я открыл.

**[07:37:38 PM] Room:** (not confirmed) Я открыл там PDF-файл.

**[07:37:41 PM] Val Levitan:** (not confirmed) Но это не drawing.

**[07:37:45 PM] Room:** (not confirmed) Это дейташит.

**[07:37:46 PM] Room:** (not confirmed) Это датащит, да. А есть Нас... drawing, есть какой-то... Нет, это А? по- покупная деталь. Это buy part.

**[07:37:54 PM] Val Levitan:** (not confirmed) Хорошо. Окей, я не против.

**[07:37:59 PM] Room:** (not confirmed) Я просто думаю,

**[07:38:04 PM] Room:** (not confirmed) где, например, как я буду знать, как монтирует, как вы будете знать, как монтируется это, этот монитор. Потому что в контракте он э, просмотрел дейташит, он увидел mounting holes, А где? потом в А где? Я, контракте там записано.

**[07:38:22 PM] Genadi Peari:** (not confirmed) А, в каком, на какой странице? Там в конце есть, во всех этих документах есть. sheet.

**[07:38:29 PM] Val Levitan:** (not confirmed) а, Там в, вот, кон- в конце есть. а, секунду, секунду. Я, там было more sheets, а я не, я не открыл. Геннадий, you're frozen, я не знаю почему.

**[07:38:38 PM] Genadi Peari:** (not confirmed) Я вижу, что я frozen, но я, я не знаю. А, камеру могу сейчас, секунду.

**[07:38:45 PM] Genadi Peari:** (not confirmed) О, а, и, и плюс это очень, очень хороший point. У нас же здесь будет, когда второй manufacturer параллельно с BOE, да, data contracts изменится, потому что там добавится holes, и в Да, тот же ну, data contract, и у нас будет, скажем, когда два, мы все это cover. Поэтому мы сделали manufacturer and the part number, и не наоборот.

**[07:39:13 PM] Room:** (not confirmed) Понимаете? Это все работает сейчас.

**[07:39:18 PM] Val Levitan:** (not confirmed) Сейчас, секундочку, Геннадий, я еще прохожусь по more pages.

**[07:39:22 PM] Room:** (not confirmed) Ну, это классно, data sheet, то, что надо.

**[07:39:26 PM] Genadi Peari:** (not confirmed) Там, Обалденно. там все абсолютно есть. И, и входное напряжение, LED drivers, everything. Там все, все perfect.

**[07:39:41 PM] Val Levitan:** (not confirmed) Кстати, я сейчас И сейчас я дошел, я вижу механический чертеж.

**[07:39:49 PM] Val Levitan:** (not confirmed) По-моему, это механический чертеж. Это, это на 28 странице.

**[07:39:54 PM] Val Levitan:** (not confirmed) восьмая, 29 страница, последняя.

**[07:39:58 PM] Genadi Peari:** (not confirmed) Я правильно смотрю, Геннадий? Я просто подтвердите, пожалуйста. Да, да, вы смотрите на 18.5, да?

**[07:40:07 PM] Room:** (not confirmed) Да,

**[07:40:10 PM] Val Levitan:** (not confirmed) Мгм. двадцать 29 страница. 28 29 страница– это Mounting Dimensions, да?

**[07:40:15 PM] Room:** (not confirmed) Да, да.

**[07:40:17 PM] Val Levitan:** (not confirmed) Мгм. Все есть.

**[07:40:20 PM] Val Levitan:** (not confirmed) Геннадий, точно, точно как доктор прописал.

**[07:40:26 PM] Genadi Peari:** (not confirmed) Оно сейчас очень интересно, потому что я сейчас, когда проходился по контроллерам, а, я, кстати, сравнивал, я брал людей дейташит, я нашел пару manufacturers, которые делают такие мониторы. Преимущество это, что это never end supply, да? И не бывает, что они obsolete.

**[07:40:45 PM] Genadi Peari:** (not confirmed) Я следующим стадиям хотел это проверять. Так я по их, их загонял, их дейташит в этот самый и проверял, It's so nice.

**[07:40:55 PM] Val Levitan:** (not confirmed) Но это, Поэтому, это будет miracle, Геннадий. То, что мы делаем, Геннадий, то, что мы делаем здесь, это никогда не было сделано. Вы понимаете, это никто не делает.

**[07:41:08 PM] Room:** (not confirmed) Это будет обалденно.

**[07:41:11 PM] Room:** (not confirmed) Я- кстати, я хотел вам апдейт дать.

**[07:41:15 PM] Room:** (not confirmed) Может, это просто, ну, что-то приятное.

**[07:41:19 PM] Genadi Peari:** (not confirmed) Ну, я люблю Вот, время. э, ну, вот то, что мы говорили, хотим, вот нам повысили цены в Корее сильно на вот эти драйв-мониторы все. У нас же много мониторов, на все идут эти контроллеры. И мы платим, начали платить такие деньги, В общем, на бумаге у меня уже сейчас сейвинг 95 долларов на машину.

**[07:41:42 PM] Room:** (not confirmed) Что вы говорите?

**[07:41:44 PM] Genadi Peari:** (not confirmed) Мгм. Вот мы уже один сэмпл, нам послали уже сэмпл фриз на 22 инча, и 43 мы купили, там по 25 долларов два сэмпла к нам едут. И сейчас я работаю, вот exactly я прохожусь по всем мониторам, мне надо поменять, ну, чтобы бракеты все подходили, чтобы провода, я делаю ревью сейчас.

**[07:42:09 PM] Room:** (not confirmed) It's huge.

**[07:42:12 PM] Room:** (not confirmed) Ну, вы пользуетесь Клодом, правильно?

**[07:42:16 PM] Genadi Peari:** (not confirmed) Ну, я клодом пользуюсь, когда мне надо, скажем, сегодня уже в в Bill of Material пойти поменять. Намного удобнее.

**[07:42:24 PM] Room:** (not confirmed) Он идет и все меняет.

**[07:42:28 PM] Genadi Peari:** (not confirmed) А чертежи же я делаю не клодом, как я. Чертежи пока еще не Клодом, но это... Мне же надо посмотреть, как, как к- тот подходит, этот не подходит, как сейчас быть, как транзишн сделать, как что сказать, какую инструкцию дать на продакшн. Like, Ну, я просто смотрю, что потратить few days, но это huge. да.

**[07:42:55 PM] Genadi Peari:** (not confirmed) Что это, 10, 7% цены машины?

**[07:43:03 PM] Room:** (not confirmed) Не знаю.

**[07:43:04 PM] Genadi Peari:** (not confirmed) Хочу сэмпл увидеть.

**[07:43:08 PM] Val Levitan:** (not confirmed) Хорошо. Да, секундочку, давайте я вернусь к своим помидорам.

**[07:43:19 PM] Val Levitan:** (not confirmed) Окей. Так, в принципе, что я должен... ш- Что, что мы должны получить?

**[07:43:35 PM] Val Levitan:** (not confirmed) У нас есть компоненты, Список компонентов, он уже окончательный?

**[07:43:41 PM] Genadi Peari:** (not confirmed) Категории, да. Некоторые еще не дополнены. Ну, вот вы мне вчера прислали, я еще... не- Ну, там

**[07:43:50 PM] Genadi Peari:** (not confirmed) на текущие проекты почти все есть.

**[07:43:55 PM] Val Levitan:** (not confirmed) Можно То есть дополнить там. то есть список компонентов на сегодняшние продукты,

**[07:44:03 PM] Room:** (not confirmed) список компонентов сделан.

**[07:44:07 PM] Room:** (not confirmed) Data sheets, я понимаю, что в основном сделаны.

**[07:44:13 PM] Room:** (not confirmed) В большинстве.

**[07:44:16 PM] Genadi Peari:** (not confirmed) То, что мы делаем GVL Vendor, уже все там. Не хватает какие-то дейта там.

**[07:44:24 PM] Genadi Peari:** (not confirmed) أكيد طبعا دور descriptions drawings يا طبعا

**[07:44:29 PM] Val Levitan:** (not confirmed) Donc je t'en donne, hein.

**[07:44:38 PM] Genadi Peari:** (not confirmed) Ну, дальше, во-первых, это надо utilize чтобы на продакшн посылалось оттуда все. автоматически на вендором.

**[07:44:45 PM] Room:** (not confirmed) Нет, я, я понимаю, подождите, я, я спросил вопрос, но я пока не понимаю, что я спросил.

**[07:44:53 PM] Room:** (not confirmed) Одну секунду.

**[07:44:56 PM] Val Levitan:** (not confirmed) И, одну секунду, я задумался. Одну секунду.

**[07:45:02 PM] Val Levitan:** (not confirmed) Мне, понимаете, мне нужна sound, sounding board. Я сижу как в вакууме иногда, мне тяжело

**[07:45:10 PM] Room:** (not confirmed) Я с вами просто кофе попью.

**[07:45:15 PM] Room:** (not confirmed) Что, что у нас есть?

**[07:45:23 PM] Room:** (not confirmed) Понятно.

**[07:45:28 PM] Room:** (not confirmed) Окей.

**[07:45:53 PM] Room:** (not confirmed) А Здесь пластики вы разбомбили на продукты.

**[07:46:00 PM] Room:** (not confirmed) Ну,

**[07:46:01 PM] Genadi Peari:** (not confirmed) ну да, они же не пересекаются.

**[07:46:24 PM] Val Levitan:** (not confirmed) А у вас есть э, стандарт как делается part, partless создается.

**[07:46:33 PM] Room:** (not confirmed) Part number создается. Да, Есть. конечно.

**[07:46:37 PM] Room:** (not confirmed) Да, я понимаю, конечно, есть.

**[07:46:41 PM] Room:** (not confirmed) А где data contract?

**[07:46:52 PM] Room:** (not confirmed) Если, например, я открою что-то.

**[07:46:55 PM] Room:** (not confirmed) А, это under contract YAML, правильно?

**[07:46:59 PM] Genadi Peari:** (not confirmed) Я так понимаю. YAML файл, да.

**[07:47:02 PM] Room:** (not confirmed) Ну, это under contract YAML.

**[07:47:07 PM] Val Levitan:** (not confirmed) Мгм. А как этот контракт создается?

**[07:47:33 PM] Room:** (not confirmed) Он проходит по чертежам.

**[07:47:38 PM] Genadi Peari:** (not confirmed) замеряет, если вы говорите про механическую деталь, он Да. замеряет размеры все, этим,

**[07:47:47 PM] Genadi Peari:** (not confirmed) ну, замеряет все размеры, раз- mountings там, раз- отверстия, и general все dimensions, и все это туда вписывает.

**[07:48:00 PM] Room:** (not confirmed) Но он это все проверяет, и я это четко вижу.

**[07:48:05 PM] Room:** (not confirmed) Я когда новые детали сейчас, вот, вот сегодня буквально я заносил новые parts, он говорит, так у тебя же там ошибка, ты же ты же туда... Но не-» Да-да, он это говорит, ты же, же это же как мы планировали.

**[07:48:18 PM] Genadi Peari:** (not confirmed) Он говорит, ты, ты ж туда не засунешь ПМ. Говорит, у тебя ошибка. Пошел посмотрел, действительно у меня ошибка.

**[07:48:25 PM] Room:** (not confirmed) Да?

**[07:48:26 PM] Room:** (not confirmed) Это же, Ну, это описка. же. Не то, Окей, что не важно. прям... Не, важно. Вы же помнили, помните, мы же именно так и планировали, да? Так, все это работает. Я, ж- я ж вот сегодня он мне три раза послал меня переделывать.

**[07:48:39 PM] Room:** (not confirmed) Кайф. Пока, пока я сделал пиар.

**[07:48:52 PM] Room:** (not confirmed) Так,

**[07:48:58 PM] Val Levitan:** (not confirmed) я, наверное, могу попросить сделать какой-то final bill of material.

**[07:49:04 PM] Room:** (not confirmed) Почему я не могу это сделать?

**[07:49:13 PM] Genadi Peari:** (not confirmed) Я бы сегодня э, Ну, bill of material это nice.

**[07:49:20 PM] Room:** (not confirmed) Ам, Ну вот сегодня вот

**[07:49:27 PM] Room:** (not confirmed) Вал, скажите, вот, вот с- э, у меня больше сейчас базар, вот почему ваш этот... Вы, се- вы сегодня сказали, я хочу 50 IQ и шест- 300 портов. И плюс мне надо, там мы с Андреем сейчас составляем список. Это, ж, это же so simple. Пойди, вот тебе три номера, что мне надо, чтобы я построил т- э, 300, э, то есть в таких-то пропорциях. Если на это есть счет, е- если у нас инвентарий, если у нас нету инвентария. Ну, мы уже прошлись по инвентарию, они уже столько проходятся, и мне Нет, это так это базар, на... что, что Не, не, Элизабет... не. Не, нет, так я считаю, что это просто. Я, да, поддерживаю ваш, я поддерживаю, что вы Потому что говорите. Мэри, я говорю, Миша, я говорю, почему ты эту не заказал? Тут бракет 3 грамма, Эй, малюсенький. заб- А- забудьте, забудьте Мишу. Да давайте не Окей, будем Мэри. А Мэри поднимать. вообще смотрит, а я, Ме- я не Мэри, знаю, Мэри, Мэри не в состоянии. Стоп, стоп.

**[07:50:27 PM] Val Levitan:** (not confirmed) Я, я все это понимаю, я понимаю все тонкости. Давайте не будем туда идти. У меня есть свой план на это. хорошо.

**[07:50:36 PM] Room:** (not confirmed) А, давайте так.

**[07:50:42 PM] Val Levitan:** (not confirmed) Я могу Подождите, а где флекс? есть?

**[07:50:47 PM] Genadi Peari:** (not confirmed) А он был? А в металл есть в вот есть Flex Pay металл на него.

**[07:50:54 PM] Room:** (not confirmed) Slim. И Slim есть и Pay.

**[07:50:56 PM] Room:** (not confirmed) Нет, FS, подождите, FS, не, не пей, не пей, а порт.

**[07:51:01 PM] Genadi Peari:** (not confirmed) Порт. есть э, металл на порт тоже.

**[07:51:05 PM] Room:** (not confirmed) Металл на порт, я вижу. Металл на Там порт есть. есть э, А с- электроника, электроника. там, если вы обратили внимание, там 18 бракетов уже лежит.

**[07:51:18 PM] Genadi Peari:** (not confirmed) на- в порте.

**[07:51:20 PM] Room:** (not confirmed) Всех Подождите, а, а электроника? электроника в PCBA.

**[07:51:27 PM] Room:** (not confirmed) Я открыл электронику. Секунду, где это? Ну, PCBA. Components, then PCBA.

**[07:51:32 PM] Room:** (not confirmed) Компон- А, вы имеете в виду электронные борт.

**[07:51:37 PM] Genadi Peari:** (not confirmed) Да, PCBA, да. PCBA, да. Flexport это FP01.

**[07:51:43 PM] Room:** (not confirmed) Окей, подождите, у меня сейчас есть мысль. Я должен, я должен проэкспериментировать. Ам, Мне кажется, это проще, чем я думаю.

**[07:51:52 PM] Val Levitan:** (not confirmed) А, Вы на месте, да? Я могу вас а, набрать еще, да?

**[07:51:59 PM] Room:** (not confirmed) Да.

**[07:52:00 PM] Room:** (not confirmed) конечно.

**[07:52:01 PM] Room:** (not confirmed) Окей, дайте я проэкспериментирую. Thank you.


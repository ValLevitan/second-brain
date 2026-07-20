# Figma to Testing - Transcript
## Date: August 12, 2025
## Speaker: Aaron Bockelie

### Introduction to Figma Prototyping

Essentially, you build a prototype, let's just say in Figma. The prototype in Figma is not the actual application. It's like a Photoshop version of your user experience or of your product. It doesn't functionally run and it doesn't - you can't be loaded onto a Figma mockup can't be ran on a cell phone as a piece of software or on a tablet or a PC. But what Figma does is it gives the abstraction of being able to design the user interface and the user experience ahead of time.

In Figma, once you've detailed out every bit of the user interface, the fonts, the colors, the layout, the graphics, the elements, everything.

### Exporting from Figma

Figma's value comes in being able to export that into various formats. So for example, you could take Figma, your mock-ups for the user interface, the input, the dialogue, the click around on stuff. All those things can then be exported to a series of React frameworks or React pages.

### From React to Production

Once you're in React, you can take that React environment and you can put it into your product. You check it into source code, into your source control. That then becomes your actual user experience and user interface for your product.

### Figma as Design Reference

Figma, when you did that design work, holds on to all of that. It's like Figma is, I guess maybe another way to think about Figma is it's like CAD, right? It's not the real product, it's the design of the product.

Now that you've done that, when you go through and you compile your application and run it, it's based on perhaps a React framework or React code that's now rendering your user interface. And if you have built a bunch of test harness unit tests into your environment.

### Automated Testing with UI Elements

You can essentially interact with the user elements inside of your user interface and programmatically click on them or shuffle the user interface pages or whatever you want around.

Now that you have the Figma environment, you can use that as your design reference. You can actually render and see what the Figma mockup is supposed to look like and visually compare that with the actual compiled product that's rendering running in React and a compiled product that's in your platform experience that you've got.

### Visual Comparison Testing

So if you're on a mobile device or a PC or whatever, the presentation of that user interface is showing. There are frameworks available that allow you to automate this so you can take these prototypes that are in Figma kind of manage them as the managed experience for your platform and then as you go through time and develop your product you can validate that what you actually compiled and built are running in your platform matches what your prototype looked like in Figma.

If it doesn't match, well, you either need to figure out why it didn't implement correctly in the code, or you go back and you understand what you've changed between the user prototype experience in Figma and the actual production code.

### TypeScript Testing and Framework Integration

These types of tests like let's say write a test, a TypeScript style test that invokes the user interface for something or the user experience, can use resources through framework testing frameworks to be able to acquire the visual presentation of the application as well as the visual presentation of Figma and make a visual comparison between the two.

Identifying all the elements or whatever, not to mention invoking all the elements directly to make sure they react correctly in the React framework. So these are this is sort of a modern way of testing your application.

### Real-World Example: Netflix

Let's imagine you had Netflix as a mobile app on your phone. Well, Netflix has a whole bunch of areas of concern that you can click through from playing movies to configuring your account and everything else. And somebody has explicitly designed all that potentially in Figma.

So now what you can do is when you build your application for the mobile platform for Netflix, part of your test unit test is to go through every single user interface experience that you've got in the application and compare it against the Figma reference. And if they don't look the same, then you flag that as a potentially failing test and you investigate what happened.

### Conclusion

That's just kind of a common way that is what is well known, but I know there's others.
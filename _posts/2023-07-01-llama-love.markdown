---
title: "Llama love"
layout: post
date: 2023-11-23 00:00
image: /assets/images/2023-07-01-llama-love/teampic.jpg
headerImage: false
tag:
- markdown
- components
- extra
category: blog
author: chrissettles
description: Building a love bot at a custom LLM hackathon  
---
# How we built “LLamaLove”: A fine-tune of Llama-2-13B on 50 shades of grey & Too hot to handle

![Our ‘llama love’ bot hackathon team: Rongfei, Lisa, Me (Chris), Era, and Jesse, pictured from left to right.](https://raw.githubusercontent.com/neverSettles/neverSettles.github.io/gh-pages/assets/images/2023-07-01-llama-love/teampic.jpeg)

Our ‘llama love’ bot hackathon team: Rongfei, Lisa, Me (Chris), Era, and Jesse, pictured from left to right.

**Update:**

I’ve deployed the bot on poe.com! You can try it out here:

https://poe.com/llamalove 

The day started strong. [Adam D'Angelo](https://www.linkedin.com/in/dangelo/), CEO of Quora kicked us off by sharing what Quora has been up to with building in the generative AI space - [Poe.com](http://Poe.com) 

![Adam](https://raw.githubusercontent.com/neverSettles/neverSettles.github.io/gh-pages/assets/images/2023-07-01-llama-love/adam.png)

![Poe](https://raw.githubusercontent.com/neverSettles/neverSettles.github.io/gh-pages/assets/images/2023-07-01-llama-love/poe.png)

Many more sponsors jumped in, such as  [Robert Nishihara](https://www.linkedin.com/in/robert-nishihara-b6465444/) and [Ameer Haj Ali](https://www.linkedin.com/in/ameer-haj-ali/) from Anyscale, giving us hope and proof that fine-tuning Llama2 on specific tasks can help open source models perform better than GPT4! 🔥🔥

![Anyscale](https://raw.githubusercontent.com/neverSettles/neverSettles.github.io/gh-pages/assets/images/2023-07-01-llama-love/anyscale.png)

Sergey, the Llama 2 creator, jumped in to give a quick tech talk on how he made llama 2 

![Sergey](https://raw.githubusercontent.com/neverSettles/neverSettles.github.io/gh-pages/assets/images/2023-07-01-llama-love/llama2.png)

And then, [Jamie from Together AI](https://www.linkedin.com/in/jamiedeguerre/) shared how hackers could use the together AI API to very easily and quickly fine tune LLama 7B on 100M tokens in < 30 minutes. 

![Together](https://raw.githubusercontent.com/neverSettles/neverSettles.github.io/gh-pages/assets/images/2023-07-01-llama-love/together.png)


* Now you might ask, what did the hackers build? *

My team had an observation. We saw that the existing LLMs out there have an opportunity for ♥️ LOVE ♥️. Today, when we ask LLMs to give us something 🍝saucy🍝, it gives us boring answers like 
”I apologize, but as a large language model, I cannot…”…

![Pitch](https://raw.githubusercontent.com/neverSettles/neverSettles.github.io/gh-pages/assets/images/2023-07-01-llama-love/pitch.png)

So we thought … what if we could have LLMs generate content that gives us back a lil’ more ♥️ love ♥️? 

And thus, we fine tuned 2 models. The first was trained on the transcripts of the TV shows 

1. Too hot to handle
2. Love Island
3. Temptation Island
4. Naked Attraction 
5. Love is blind

This model was meant to act like a chat model. We parsed the input until it was in a format prepared for [together.ai](http://together.ai) to pick it up and train a model for us on it. 

The result:
Given the prompt, “Hey Baby”, we get:

![Too hot to handle](https://raw.githubusercontent.com/neverSettles/neverSettles.github.io/gh-pages/assets/images/2023-07-01-llama-love/too_hot_to_handle_example.png)

“, you’re looking good! I’m a single woman, and I’m looking for a single man.”

Not bad. 

Next we found a pdf of the every page of the book ‘50 shades of grey’ - a book known for the love it creates. 

After massaging our data into a reasonable format to support our fine-tuning needs, 

```
{"text": "Are you trying to completely emasculate me?"}
{"text": "This is probably the only place that I’ll be able to afford to pay."}
{"text": "Anastasia, I appreciate the thought. I do. But no."}
{"text": "Do you want to come in? I ask shyly."}
{"text": "I need to work, Anastasia, but I’ll be back this evening. What time?"}
{"text": " I ignore the unwelcome stab of disappointment. Why do I want to spend every single minute with this controlling sex god? Oh yes, I’ve fallen in love with him, and he can fly."}
{"text": "Thank you… for the more."}
{"text": "My pleasure, Anastasia. He kisses me, and I inhale his sexy Christian smell."}
```

Together AI gives us a brand new completion model that gives us the feel of 50 shades of grey:

With the prompt of “We were both lying there, holding hands”, and using our brand new fine tuned model to perform chat completion, we get:

”

We were both lying there, holding hands. I was thinking about how much we had in common and that he could be the one for me when suddenly his eyes rolled back into their sockets as if they'd been pulled by a string behind my headboard! He started moaning loudly like someone who is being tortured slowly with hot irons pressed against every part of him until finally giving up any hope or resistance...and then fell limp next to where you lay sleepily beside us after our lovemaking session ended earlier this morning."
I think it would have made sense not just because she wants revenge but also outta respect towards herself since her husband died while trying protect others from harm - something no man should ever do unless absolutely necessary (which isn’t always possible). And now here comes along another guy willing enough take risks without even knowing what kind personality traits make them tick? How dare anyone else try steal away MY perfect match before things get too serious between US two??!!

Not to mention - the text generation was blazing fast! 

<!-- [Screen Recording 2023-08-14 at 2.10.12 AM.mov](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/02525b1a-7b46-4adc-ae80-afe1c0ff773d/Screen_Recording_2023-08-14_at_2.10.12_AM.mov) -->
![Together AI text generation](https://raw.githubusercontent.com/neverSettles/neverSettles.github.io/gh-pages/assets/images/2023-07-01-llama-love/together_speed.mov)

With these two small demos, we showed the judges at the hackathon that it certainly is possible for a group of hackers to get up and running with a fine tuned custom LLM model within hours. 

You can view our pitch deck here:
https://pitch.com/public/afe488e7-9697-40a8-8f67-21b6c8ad5229/8e30d52d-e17a-4df3-8809-8e6d45e46b65

Our video of our presentation here:

[Untitled](https://photos.google.com/share/AF1QipNSGMl_suYJhoK2isud5GdubIgdx8UFKzCREWp8q5OFelOlDaTHhty6mH90nECk0A?key=Q0F2UmJTYi11X3hOY2xLR3pfMkFmV3llMDBCcml3)

Throughout this day, I got to work with some amazing minds such as 
[Era Qian](https://www.linkedin.com/in/eraqian/), [Rongfei Lu](https://www.linkedin.com/in/rongfei-lu/), [Marco Mascorro](https://www.linkedin.com/in/marcomascorro/), [Lisa Liu](https://www.linkedin.com/in/lisalliu/), and [Jesse Hu](https://www.linkedin.com/in/jessehu/). We got a team picture together during the hacking:

![teampic.jpeg](https://raw.githubusercontent.com/neverSettles/neverSettles.github.io/gh-pages/assets/images/2023-07-01-llama-love/teampic.jpeg)

And finally, the judges selected us as the 2nd place winners! I was so happy to shake hands with [Adam D'Angelo](https://www.linkedin.com/in/dangelo/), [Marco Mascorro](https://www.linkedin.com/in/marcomascorro/), [Taranjeet Singh](https://www.linkedin.com/in/taranjeet7114/) and [Jamie de Guerre from Together AI](https://www.linkedin.com/in/jamiedeguerre/) accepting my new clout that I worked hard for alongside with [Era](https://www.linkedin.com/in/eraqian/) who stayed until the end with me! 

![winpic.jpeg](https://raw.githubusercontent.com/neverSettles/neverSettles.github.io/gh-pages/assets/images/2023-07-01-llama-love/winpic.png)

Super Special thanks to [Jeremy Nixon](https://www.linkedin.com/in/jeremyvnixon/) - a man who worked so hard to organize this hackathon - and he even hacked on a project DURING the hackathon. I don’t know how he pulls it off. 

<!-- ![Marcos brought his robotic dog that talks - Pictured above is Jeremy Nixon holding the microphone up so the dog will be projected loud enough.](https://raw.githubusercontent.com/neverSettles/neverSettles.github.io/gh-pages/assets/images/2023-07-01-llama-love/jeremy.png) -->

Marcos brought his robotic dog that talks - Pictured above is Jeremy Nixon holding the microphone up so the dog will be projected loud enough.

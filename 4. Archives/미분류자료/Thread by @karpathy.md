---
title: "Thread by @karpathy"
source: "https://x.com/karpathy/status/1891720635363254772?s=19"
author:
  - "[[@karpathy]]"
published: 2025-02-18
created: 2025-02-19
description: "I was given early access to Grok 3 earlier today, making me I think one of the first few who could run a quick vibe check. Thinking First,"
tags:
  - "clippings"
---
**Andrej Karpathy** @karpathy [2025-02-18](https://x.com/karpathy/status/1891720635363254772)

I was given early access to Grok 3 earlier today, making me I think one of the first few who could run a quick vibe check.

Thinking

✅ First, Grok 3 clearly has an around state of the art thinking model ("Think" button) and did great out of the box on my Settler's of Catan question:

"Create a board game webpage showing a hex grid, just like in the game Settlers of Catan. Each hex grid is numbered from 1..N, where N is the total number of hex tiles. Make it generic, so one can change the number of "rings" using a slider. For example in Catan the radius is 3 hexes. Single html page please."

Few models get this right reliably. The top OpenAI thinking models (e.g. o1-pro, at $200/month) get it too, but all of DeepSeek-R1, Gemini 2.0 Flash Thinking, and Claude do not.

❌ It did not solve my "Emoji mystery" question where I give a smiling face with an attached message hidden inside Unicode variation selectors, even when I give a strong hint on how to decode it in the form of Rust code. The most progress I've seen is from DeepSeek-R1 which once partially decoded the message.

❓ It solved a few tic tac toe boards I gave it with a pretty nice/clean chain of thought (many SOTA models often fail these!). So I upped the difficulty and asked it to generate 3 "tricky" tic tac toe boards, which it failed on (generating nonsense boards / text), but then so did o1 pro.

✅ I uploaded GPT-2 paper. I asked a bunch of simple lookup questions, all worked great. Then asked to estimate the number of training flops it took to train GPT-2, with no searching. This is tricky because the number of tokens is not spelled out so it has to be partially estimated and partially calculated, stressing all of lookup, knowledge, and math. One example is 40GB of text ~= 40B characters ~= 40B bytes (assume ASCII) ~= 10B tokens (assume ~4 bytes/tok), at ~10 epochs ~= 100B token training run, at 1.5B params and with 2+4=6 flops/param/token, this is 100e9 X 1.5e9 X 6 ~= 1e21 FLOPs. Both Grok 3 and 4o fail this task, but Grok 3 with Thinking solves it great, while o1 pro (GPT thinking model) fails.

I like that the model \*will\* attempt to solve the Riemann hypothesis when asked to, similar to DeepSeek-R1 but unlike many other models that give up instantly (o1-pro, Claude, Gemini 2.0 Flash Thinking) and simply say that it is a great unsolved problem. I had to stop it eventually because I felt a bit bad for it, but it showed courage and who knows, maybe one day...

The impression overall I got here is that this is somewhere around o1-pro capability, and ahead of DeepSeek-R1, though of course we need actual, real evaluations to look at.

DeepSearch

Very neat offering that seems to combine something along the lines of what OpenAI / Perplexity call "Deep Research", together with thinking. Except instead of "Deep Research" it is "Deep Search" (sigh). Can produce high quality responses to various researchy / lookupy questions you could imagine have answers in article on the internet, e.g. a few I tried, which I stole from my recent search history on Perplexity, along with how it went:

\- ✅ "What's up with the upcoming Apple Launch? Any rumors?"

\- ✅ "Why is Palantir stock surging recently?"

\- ✅ "White Lotus 3 where was it filmed and is it the same team as Seasons 1 and 2?"

\- ✅ "What toothpaste does Bryan Johnson use?"

\- ❌ "Singles Inferno Season 4 cast where are they now?"

\- ❌ "What speech to text program has Simon Willison mentioned he's using?"

❌ I did find some sharp edges here. E.g. the model doesn't seem to like to reference X as a source by default, though you can explicitly ask it to. A few times I caught it hallucinating URLs that don't exist. A few times it said factual things that I think are incorrect and it didn't provide a citation for it (it probably doesn't exist). E.g. it told me that "Kim Jeong-su is still dating Kim Min-seol" of Singles Inferno Season 4, which surely is totally off, right? And when I asked it to create a report on the major LLM labs and their amount of total funding and estimate of employee count, it listed 12 major labs but not itself (xAI).

The impression I get of DeepSearch is that it's approximately around Perplexity DeepResearch offering (which is great!), but not yet at the level of OpenAI's recently released "Deep Research", which still feels more thorough and reliable (though still nowhere perfect, e.g. it, too, quite incorrectly excludes xAI as a "major LLM labs" when I tried with it...).

Random LLM "gotcha"s

I tried a few more fun / random LLM gotcha queries I like to try now and then. Gotchas are queries that specifically on the easy side for humans but on the hard side for LLMs, so I was curious which of them Grok 3 makes progress on.

✅ Grok 3 knows there are 3 "r" in "strawberry", but then it also told me there are only 3 "L" in LOLLAPALOOZA. Turning on Thinking solves this.

✅ Grok 3 told me 9.11 > 9.9. (common with other LLMs too), but again, turning on Thinking solves it.

✅ Few simple puzzles worked ok even without thinking, e.g. \*"Sally (a girl) has 3 brothers. Each brother has 2 sisters. How many sisters does Sally have?"\*. E.g. GPT4o says 2 (incorrectly).

❌ Sadly the model's sense of humor does not appear to be obviously improved. This is a common LLM issue with humor capability and general mode collapse, famously, e.g. 90% of 1,008 outputs asking ChatGPT for joke were repetitions of the same 25 jokes​. Even when prompted in more detail away from simple pun territory (e.g. give me a standup), I'm not sure that it is state of the art humor. Example generated joke: "\*Why did the chicken join a band? Because it had the drumsticks and wanted to be a cluck-star!\*". In quick testing, thinking did not help, possibly it made it a bit worse.

❌ Model still appears to be just a bit too overly sensitive to "complex ethical issues", e.g. generated a 1 page essay basically refusing to answer whether it might be ethically justifiable to misgender someone if it meant saving 1 million people from dying.

❌ Simon Willison's "\*Generate an SVG of a pelican riding a bicycle\*". It stresses the LLMs ability to lay out many elements on a 2D grid, which is very difficult because the LLMs can't "see" like people do, so it's arranging things in the dark, in text. Marking as fail because these pelicans are qutie good but, but still a bit broken (see image and comparisons). Claude's are best, but imo I suspect they specifically targeted SVG capability during training.

Summary. As far as a quick vibe check over ~2 hours this morning, Grok 3 + Thinking feels somewhere around the state of the art territory of OpenAI's strongest models (o1-pro, $200/month), and slightly better than DeepSeek-R1 and Gemini 2.0 Flash Thinking. Which is quite incredible considering that the team started from scratch ~1 year ago, this timescale to state of the art territory is unprecedented. Do also keep in mind the caveats - the models are stochastic and may give slightly different answers each time, and it is very early, so we'll have to wait for a lot more evaluations over a period of the next few days/weeks. The early LM arena results look quite encouraging indeed. For now, big congrats to the xAI team, they clearly have huge velocity and momentum and I am excited to add Grok 3 to my "LLM council" and hear what it thinks going forward.

![Image](https://pbs.twimg.com/media/GkC808faAAA22cI?format=jpg&name=large)
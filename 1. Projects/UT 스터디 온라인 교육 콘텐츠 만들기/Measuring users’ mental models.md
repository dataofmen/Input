[[ReadItLater]] [[Article]]

#멘탈모델

# 번역

### **What are mental models?**

![](https://i.imgur.com/W3ZsKpQ.png)
The NES (Credit: [Jason Leung/Unsplash](https://unsplash.com/photos/classic-snes-console-ZV7lnfyQLmA?utm_content=creditCopyText&utm_medium=referral&utm_source=unsplash))

90년대에 슈퍼 닌텐도나 제네시스 같은 콘솔 게임기로 비디오 게임을 즐기던 어린 시절, 전원을 켰을 때 흔히 겪었던 문제 중 하나는 화면이 깨지는 현상이었습니다. 많은 사람들이 카트리지를 꺼내서 접점에 바람을 불어 먼지를 제거하곤 했습니다. 안타깝게도 이 방법은 습기를 더해 득보다 실이 많다는 사실을 나중에 알게 되었습니다. 카트리지를 분리했다가 다시 삽입하여 접점을 다시 정렬하기만 하면 되는 것으로 밝혀졌습니다.

  

이 일화는 멘탈 모델의 두 가지 핵심 특성을 강조합니다.

  

첫째, 멘탈 모델은 어떤 일이 어떻게 작동하는지에 대한 믿음으로, 항상 사실이거나 완전하지 않을 수 있으며 심지어 완전히 틀릴 수도 있습니다. 특히 사용자가 백엔드 프로세스에 대한 완전한 인사이트가 필요하지 않은 복잡한 B2B 환경에서는 정확성이 항상 필요한 것은 아닙니다. 중요한 것은 멘탈 모델이 현실과 유사하거나 정보적으로만 동등하더라도 사용자가 목표를 달성할 수 있을 만큼 정확해야 한다는 것입니다.

  

둘째, 멘탈 모델은 시스템 피드백을 해석하는 방식을 변화시켜 의사 결정과 이후 행동에 영향을 미칩니다. 따라서 시스템을 사용자의 멘탈 모델에 맞게 이해하고 조정하는 것은 사용자 경험에 큰 영향을 미칠 수 있습니다.

  

모든 사용자가 동일한 모델을 가지고 있지는 않지만, 사용자 기반 내에서 유사점이나 주제가 관찰되는 경우가 많습니다. 보행 신호의 예로 돌아가서 사용자를 크게 한 번만 누르거나 여러 번 누르는 사용자로 분류할 수 있지만, 자세히 살펴보면 개인마다 멘탈 모델의 세부 수준과 형식이 다른 미묘한 차이를 발견할 수 있습니다. 그럼에도 불구하고 사용자 기반 내에서 공통 모델 또는 대표 모델을 파악하면 디자인 변경에 도움이 될 수 있습니다.

  

또한 멘탈 모델은 적응력이 있으며 경험에 따라 변화합니다. 전투기 조종사를 대상으로 한 로저 슈바네벨트의 영향력 있는 인적 요인 연구에서는 초보자와 전문가 사이에 뚜렷한 멘탈 모델 구조가 있음을 밝혀냈습니다. 초보자는 더 다양한 모델을 가지고 있는 반면, 전문가는 더 유사한 모델을 가지고 있었습니다.

  

이러한 유연성은 훈련이나 직관적인 시스템 설계를 통해 사용자의 멘탈 모델을 시간이 지남에 따라 개선하고 더 정확하게 만들 수 있다는 장점이 있습니다. 예를 들어 Nest 온도조절기의 시장 성공은 기존 경쟁사와 달리 사용자의 멘탈 모델과 밀접하게 일치하는 인터페이스에 기인한 바가 큽니다. 이는 시스템 설계 시 멘탈 모델을 고려하는 것이 얼마나 큰 영향을 미치는지 잘 보여줍니다.


**Approaches for measuring and analyzing them**


소리 내어 말하기 프로토콜은 사용자가 시스템과 상호작용할 때 사용자의 사고 과정을 엿볼 수 있게 해줍니다. 참가자의 발언을 통해 기대치와 시스템 결과 사이의 불일치를 파악하여 근본적인 사고 모델을 밝힐 수 있습니다. 제이콥 닐슨이 선호하는 이 접근 방식은 사용성 테스트 중에 진행자가 주기적으로 사용자에게 자신의 생각과 기대치를 말로 표현하도록 유도하는 것입니다. 여러 참가자 세션에 걸쳐 사용자 멘탈 모델에서 반복되는 주제가 종종 나타납니다



사용자의 멘탈 모델을 얼마나 정확하고 완벽하게 이해해야 하는지는 연구 목적에 따라 달라집니다. 즉각적인 디자인 변경 사항을 알리기 위한 빠른 사용성 조사의 경우, 소리 내어 생각하기 또는 회고 인터뷰와 같은 가벼운 터치 방식으로도 충분할 수 있습니다.

  

반면에 입력과 출력이 많거나 부정확한 모델의 위험이 높은 복잡한 애플리케이션에는 보다 고급 접근 방식이 더 적합합니다. 소리 내어 말하기나 회고 인터뷰와 달리 보다 공식적인 방법에는 약간의 사전 계획과 설정이 필요합니다. 예를 들어, 다른 연구 질문에 대해 소리 내어 생각하기를 수행하는 동안 멘탈 모델에 대한 우연한 인사이트를 발견할 수 있지만, 그러한 목적으로 연구를 설계하지 않으면 쌍별 관련성 등급을 얻을 수 없습니다.


---
# 원문


# [Measuring users’ mental models](https://depth.drillbitlabs.com/cp/145842450)

When you’re standing at an intersection looking to cross the street, how many times do you press the walk signal call button? Do you press it repeatedly, or is once enough?

Unless you’re in a position to know the truth of the matter — say, you helped to design and implement the signal call — your answer depends on your beliefs about how it works.

[Subscribe to Depth by Drill Bit Labs](https://depth.drillbitlabs.com/)

Multi-pressers operate on the assumption that presses accumulate, signaling stronger volume of demand. Thus, the signal is more likely to change or even to do so sooner. Single-pressers believe that the system either has a request to change the signal or it doesn’t, so another press during the same traffic cycle won’t add any benefit.

The walk signal, like many of the systems we use each day, doesn’t lay out how it works to any satisfying level of detail. In the absence of information, these emerging beliefs are called mental models.

Let’s take a closer look at what mental models are and ways you can measure them in your user research.

### **What are mental models?**

As a child of the ‘90s playing video games on consoles like the Super Nintendo and Genesis, one common issue you’d encounter was glitchy screens when you turned it on. Many of us would take the cartridge out and blow on the contacts to clear the dust. Unfortunately, we later found out that this could add moisture and do more harm than good. As it turns out, all you needed to do was simply remove and reinsert the cartridge to realign the contacts.

This anecdote highlights two key qualities of mental models.

First, they’re *beliefs* about how something works, which may not always be factual or complete, and may even be entirely wrong. Accuracy isn't always necessary, particularly in complex B2B settings where users don't need full insight into back-end processes. What matters is that the mental model is accurate enough to empower users to achieve their goals, even if it's only analogous or informationally equivalent to reality.

Second, mental models change how we interpret system feedback, and thus affect our decision-making and later behavior. So understanding and aligning the system with users' mental models can have an outsized impact on the user experience.

While no two users have identical models, there are often similarities or themes observed within a user base. Going back to our example of the walk signal, we might broadly classify users into single-pressers or multi-pressers — but a closer inspection would show nuances, with individuals having varying levels of detail and formality in their mental models. Nevertheless, identifying common or representative models within a user base can help inform design changes.

Mental models are also adaptable and change based on experience. [An influential human factors study led by Roger Schvaneveldt](https://scholar.google.com/scholar?cluster=1195211114273731074&hl=en&as_sdt=0,6) that examined fighter pilots revealed distinct mental model structures between novices and experts. Novices had more diverse models, while experts held more similar models.

This flexibility presents an upside: with training or intuitive system design, users' mental models can refine and become more accurate over time. For instance, [the market success of the Nest thermostat can be partly attributed](https://www.quarterinchhole.com/p/unlocking-the-potential-of-ai-tools) to its interface aligning closely with users' mental models, unlike traditional competitors. This underscores the potential impact of considering mental models in system design.

### **Approaches for measuring and analyzing them**

There’s a wide range of methods for assessing users’ mental models, each with its own set of advantages.

The **think-aloud protocol** offers a glimpse into users' thought processes as they interact with a system. Participant utterances can reveal mismatches between their expectations and the system's outcomes, shedding some light on their underlying mental models. This approach, [favored by Jakob Nielsen](https://www.nngroup.com/articles/mental-models/), involves a moderator periodically prompting users to verbalize their thoughts and expectations during a usability test. Across multiple participant sessions, recurring themes in user mental models often emerge.

[Another method, promoted by Nikki Anderson-Stanier,](https://dscout.com/people-nerds/mental-models) is the **retrospective interview**. Here, users are asked to recall past experiences and describe their thought processes, pain points, expectations, and goals. This method is particularly useful for scenarios where stimuli are unavailable, or for multi-channel experiences that might be difficult to replicate in a usability test.

You can also pose **a series of "what-if" questions** to participants. [Stephen Payne's research on ATMs](https://scholar.google.com/scholar?cluster=470383605806623540&hl=en&as_sdt=0,6&as_ylo=1990&as_yhi=1992) used this approach, asking participants to predict outcomes based on various inputs. Through these questions, he discovered that participants varied widely in their beliefs about the information stored on debit cards.

Pairwise comparisons for **relatedness ratings** involve documenting all the possible inputs and outputs and having participants rate the closeness of each pair on a scale. If you were measuring mental models of Photoshop, for example, you might include concepts like “layer,” “blur,” “smudge,” and so on. As the list of concepts grows, you run the risk of fatiguing participants. For 5 items, they only need to make 10 comparisons — but for 15 items, that grows to 105! The final output is a matrix showing the relative strength of each pairing.

**Card sorting** offers a different perspective by grouping items based on similarity, making it suitable for scenarios where distinct categories are expected. For a complex system with many elements, this simplifies data collection by giving participants a more manageable task. 

**Pathfinder networks** may be useful for analysis and visualization. This approach mathematically prunes away weakly related ideas, highlighting the essential. The resulting figure makes it easy to compare the mental models of different user groups. This approach also offers similarity and reliability statistics if you want to understand change over time. But be aware that while [analysis tools are freely available](https://research-collective.com/PFWeb/index.php), they are no longer supported, posing potential challenges for researchers.

### **Which measurement approach is best?**

How precisely and completely you need to understand users’ mental models will depend on your research objectives. For quick usability studies aimed at informing immediate design changes, lighter touch methods like think-aloud or retrospective interviews may suffice.

On the other hand, more advanced approaches are better suited for complex applications with many inputs and outputs, or where the risk of inaccurate models is high. Unlike think-alouds and retrospective interviews, more formal methods require some advance planning and setup. For example, you may uncover incidental insights about mental models while conducting think-alouds for a different research question — but you won’t get pairwise relatedness ratings without having designed the study for that purpose.

When measuring change over time, advanced methods like Pathfinder network analysis can provide statistical comparisons between different points. But using this tool requires some technical skill.

Also consider the desired output. While think-aloud may reveal enough aspects of user mental models to fill a slide in a report deck, more thorough methods that document the inputs and outputs can be visualized as more easily digestible flowcharts and other figures.

[

![A continuum showing less to more comprehensive assessment methods, in roughly the order presented in this article.](https://substackcdn.com/image/fetch/w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F24539aa3-75cd-4dcc-ac73-6a67568d2f64_1600x900.png "A continuum showing less to more comprehensive assessment methods, in roughly the order presented in this article.")

](https://substackcdn.com/image/fetch/f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F24539aa3-75cd-4dcc-ac73-6a67568d2f64_1600x900.png)

Mental model assessment methods on a spectrum of completeness

One way you might think of this progression from think-aloud to more advanced methods is that they reflect an increasingly complete assessment of mental models. While think-aloud may capture certain aspects, advanced methods take more inputs and outputs into account for a more comprehensive view.

## **The bottom line**

Mental models are user theories about how systems work, based on beliefs rather than facts, that influence interactions and interpretations.

Assessment methods range from basic, like think-aloud and retrospective interviews, to advanced, such as relatedness ratings, card sorting, and Pathfinder networks. Basic methods offer quick insights, while advanced ones provide detailed assessments for longer, strategic initiatives. The choice depends on your research goals, the need for precision, and whether you have outputs like flow charts or visualizations in mind.

Understanding mental models is crucial for designing user-friendly experiences, aligning designs with users' expectations and enhancing system usability.

##### **ANOTHER THOUGHT…**

## **Defending user research with Crabtree’s Bludgeon**

When explaining the unique value of user research compared to other insights-generating functions like data science or market research, we often emphasize [our mixed-methods approach](https://theuxrsannotations.substack.com/p/five-mixed-methods-study-designs). You may even find yourself explaining lofty research concepts like triangulation, and using extended metaphors about geopositioning satellites.

At the crossroads of our value in uncovering meaningful patterns lies a fundamental aspect of human nature: the tendency to seek order in chaos. Consider for example the phenomenon of [pareidolia](https://en.wikipedia.org/wiki/Pareidolia), or the strong sense that a face can be perceived in some inanimate object like clouds or an electrical outlet. Even in random noise, we're prone to perceive underlying meaning.

In fairness, facial recognition is hardwired into our neural circuitry. But we’re almost equally disposed to find logic behind meaningless data or arguments. This principle is articulated in [Crabtree’s Bludgeon](https://en-academic.com/dic.nsf/enwiki/1284176), which asserts that human intellect can conjure a coherent explanation for any set of seemingly inconsistent observations. It serves as a reminder of our capacity to deceive ourselves, which we can mitigate through proper research.

So next time you’re defending the work we do as UX Researchers, consider invoking faces in clouds and Crabtree’s Bludgeon.

By acknowledging our inclination to find patterns where none exist, we underscore the necessity of rigorous, multi-method research to uncover genuine insights.

## **Drill deeper**

**Depth** is produced by **[Drill Bit Labs](http://drillbitlabs.com/)**, a leading UX and digital strategy consulting firm dedicated to shaping the future of user research. 

We work side-by-side with UX and product development leaders to elevate their digital strategy through user research projects, education and training, and expert advisory support. These services help make all our free industry reports and content possible.

**Let’s explore how we can partner with you to achieve success in your ongoing projects and upcoming ventures.**

[Start a conversation](https://www.drillbitlabs.com/contact)
[[ReadItLater]] [[Article]]

# [A Guide to Task-Based UX Metrics – MeasuringU](https://measuringu.com/task-based-metrics/)

[![](Attachment/042722Feature-300x169.jpg)](https://measuringu.com/wp-content/uploads/2022/04/042722Feature.jpg)When quantifying the user experience of a product, app, or experience, we recommend using a [mix of study-level and task-based UX metrics](https://measuringu.com/why-collect-task-and-study-metrics/).

While it’s not always feasible to assess a task experience (because of challenges with budgets, timelines, or access to products and users), observing participants attempt tasks can help uncover usability problems, informing designers about what needs to be improved.

One defining characteristic of a [usability test](https://measuringu.com/three-goals/) is the use of tasks. Tasks involve a representative user attempting to accomplish a realistic goal, such as finding a movie to stream, selecting a product to purchase, or reserving a hotel room.

Tasks can be used to help uncover [usability problems](https://measuringu.com/usability-problems/), suggesting what needs to be improved in an interface. But the result of the task itself can become a good metric to track. If users can’t reach common goals in an interface, then not much else matters.

To measure the user experience, you ideally quantify both attitudes and actions. When conducting a task-based evaluation, your task metrics should include a mix of what people do (behavioral or “action” metrics) and what people think (attitude metrics). You might also include one or more behavioral/physiological or combined metrics.

In this article, we provide a guide to task-based UX metrics.

## ![](Attachment/042722-Action-150x150.png)1\. Action Metrics

The essential task-based action metrics are operationalized from the [ISO definition of usability](https://measuringu.com/iso-9241/): a combination of effectiveness (action), efficiency (action), and satisfaction (attitude).

These metrics can be collected from simulated tasks (e.g., a usability test) or actual observation of goal-based task performance.

**Completion Rate**: Assessing the [success of a task](https://measuringu.com/task-completion/) based on predefined success criteria is the fundamental task-based behavioral metric (for example, the percentage of participants finding the correct product from a list of products on a website). We recommend coding completion rates as 1 for success and 0 for failure (a binary or binomial metric). Report the percentage complete (from 0 to 100%) along with an [adjusted Wald confidence interval](https://measuringu.com/calculators/wald/).

**Findability Rate**: The [findability rate](https://measuringu.com/measure-findability/) is a special type of completion rate typically used in a [tree test](https://measuringu.com/10-navigation-metrics/) or [first-click test](https://measuringu.com/first-click/) where the primary goal of the evaluation is to understand if participants can locate a function, product, or piece of information. It is coded and analyzed in the same way as a task completion rate.

**Time on Task**: The quintessential measure of efficiency is recording how long it takes a participant to attempt a task, typically measured in minutes and seconds, but it could be in hours, days, or milliseconds. There are at least three common ways to report task time:

1.  *Time to complete:* Time of participants who meet the success criteria.
2.  *Time on task:* Time of all participants.
3.  *Time till failure:* Time of participants who fail to meet the success criteria.

Because of the positive skew of task time data (you can’t have less than 0 seconds but there’s no theoretical upper limit), we recommend [reporting either the geometric mean or the median](https://measuringu.com/average-times/), depending on the sample size.

**Clicks/Pageviews**: A less-used measure of efficiency is the [number of clicks or unique pages](https://measuringu.com/click-clock/) a participant uses to attempt a task. Both tend to have a strong correlation with task time but clicks, in particular, require some defining (repeatedly clicking scroll bars vs. clicking in-page elements). Both can be used as a crude form of engagement or exploration, and unique pageviews are also used in a lostness metric (see below).

**Errors**: Errors included slips (accidents) and mistakes (incorrect intention but non-accidental behavior). [Coding errors](https://measuringu.com/error-coding-unmoderated/) can be time-consuming and somewhat subjective, as an evaluator will need to observe the actions of users.

## ![](Attachment/042722-Attitudinal-150x150.png)2\. Attitudinal Metrics

Attitudinal metrics are essentially questionnaires (usually short) that can be collected at both the task level and study level.

**Ease (SEQ**®): The [Single Ease Question](https://measuringu.com/seq10/) (SEQ) is a single seven-point bipolar item ranging from very difficult to very easy. The SEQ is able to discriminate as well as or better than other multi-item measures \[[PDF](https://measuringu.com/papers/Sauro_Dumas_CHI2009.pdf)\]. It has a normalized database that converts raw scores to percentile ranks (e.g., 5.5 is an average score, the 50th percentile of perceived task ease).

**Confidence**: Users should be able to complete tasks and be confident they did so correctly. Confidence can be measured using a [seven-point scale](https://measuringu.com/measuring-confidence/) (1 = not at all confident to 7 = very confident). Confidence usually correlates highly with ease, but it can provide additional information such as when users think a task is difficult but are confident they completed it, or when they completed a task successfully but were not confident. See below for combining confidence with completion rates.

**Task Load (NASA-TLX)**: Related to ease, the [Task-Load Index](https://measuringu.com/nasa-tlx/) developed at NASA is a more extensive version of the SEQ (but highly correlated with it) that contains six items typically used when there’s a hardware component (e.g., in cockpits).

**Mental Effort (SMEQ**): The [Subjective Mental Effort Questionnaire](https://measuringu.com/article/comparison-of-three-one-question-post-task-usability-questionnaires/) is a less-used single-item measure of perceived task ease. Participants mark their level of mental effort with labels calibrated on an interval-scaled continuum from 0 to 150 (e.g., 0: Not at all hard to do; 70: Pretty hard to do; 115: Tremendously hard to do). Its original paper version had participants marked a position on a line; today’s digital versions have participants use a [slider](https://measuringu.com/are-sliders-more-sensitive/).

**After Scenario Questionnaire** **(ASQ)**: This [three-item questionnaire](https://www.researchgate.net/publication/230786769_Psychometric_evaluation_of_an_after-scenario_questionnaire_for_computer_usability_studies_The_ASQ) assesses perceptions of ease, time taken, and documentation on the task.

**Expectation**: Asking participants how difficult [they think a task will be](https://measuringu.com/predicted-usability/), typically using an ease scale such as the SEQ.

**Usability Magnitude Estimation (UME)**: Participants rate a calibrated standard task using their own number (e.g., 10) and then rate subsequent tasks as a ratio to the standard task. A task rated as 20 would be twice as hard and a task rated 5 half as hard as the standard task. Researchers have reported that participants often have some difficulty providing these types of ratings \[[PDF](https://measuringu.com/papers/Sauro_Dumas_CHI2009.pdf)\].

**Variations of Perceptions of the Task Experience**: There are countless ways to have a participant reflect upon a task experience using single or multiple items. Common ones include overall satisfaction with the task, task complexity, quality of search results, other difficulty/ease ratings, and comprehension.

**Similarity/Differences from Card Sorting**: [Card sorting](https://measuringu.com/card-sorting/) is a unique UX method that involves data from a participant that’s different than typical attitudinal data collected on rating scales after attempting to complete a task. The participant behavior is to assign cards (physical or virtual) to groups, from which it is possible to derive similarity metrics among the cards. Researchers can analyze the data to gain insight into mental models, which can guide the design of user interfaces and information architectures.

## ![](Attachment/042722-Behavioral-150x150.png)3\. Behavioral and Physiological Metrics

Less commonly used metrics that can be associated with tasks include the use of eye-tracking, coding facial expressions, and physiology measures.

**Eye-Tracking Metrics**: In [eye-tracking](https://measuringu.com/eye-tracking/), you define areas of interest (AOIs) such as a label in a menu, an advertisement, or any other image. With an AOI you can collect metrics including:

*Dwell time:* The time spent within the AOI.

*Fixation count:* Average number of eye fixations within an AOI.

*Time till first fixation:* How long it takes from the start of a task till a participant fixates within an AOI.

*Pupil dilation:* While less used in performance-based studies, [pupil dilation](https://www.tobiipro.com/learn-and-support/learn/eye-tracking-essentials/is-pupil-size-calculations-possible-with-tobii-eye-trackers/) and its change over time can be used as an indication of interest/attentiveness.

**Facial Expression Coding:** [Users’ facial expressions](https://www.researchgate.net/publication/37367078_Exploring_the_Strength_of_Association_between_the_Components_of_Emotion_SyndromesThe_Case_of_Surprise) are videotaped and coded independently by evaluators to assess the frequency of eyebrow raising, eye widening, mouth opening, or other rubrics often to identify an emotional reaction to an experience.

**Various Physiology Measures**

*Electrodermal activity:* Also known as skin conductance or Galvanic skin response (GSR), this is a way of [measuring emotional arousal](https://en.wikipedia.org/wiki/Electrodermal_activity#:~:text=Sweating%20is%20controlled%20by%20the,in%20turn%20increases%20skin%20conductance.) (one of the measures used in a polygraph lie detector, driven by arousal effects on sweat gland activity).

*Electromyogram (EMG):* Muscle movements are measured using an electromyogram. This is most common in device testing, but EMGs are another way to quantify changes in facial expressions.

*Heart rate:* [Heart rate variability](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC5900369/) can be used as a measure of stress in response to a stimulus.

*Electroencephalogram (EEG):* Brain wave patterns recorded with EEG can be analyzed to detect [changes in arousal and emotion](https://www.nature.com/articles/s41598-021-86345-5#:~:text=Electroencephalography%20\(EEG\)%20is%20a%20reliable,%E2%80%93computer%20interface%20\(BCI\).).

*Functional Near-Infrared Spectroscopy (fNIRS):* Related to functional magnetic resonance imaging (fMRI), but more portable, fNIRS has the [potential for distinguishing positive and negative emotional reactions](https://www.researchgate.net/publication/304107980_fNIRS_as_a_Method_to_Capture_the_Emotional_User_Experience_A_Feasibility_Study).

**Tapping**: Having participants tap at a steady rate using their feet or finger while also attempting a task has been used as [a measure of cognitive load](https://onlinelibrary.wiley.com/doi/10.1111/1468-5884.00017) (loss of tapping rhythm may indicate a more demanding task).

## ![](Attachment/042722-Combined-150x150.png)4\. Combined Metrics

Attitudinal and action metrics can be combined to form other task-based metrics.

**Single Usability Metric (SUM)**: [SUM](https://measuringu.com/sum/) is the average of standardized versions of completion rates, task times, task-level satisfaction, and errors, weighted equally.

**Learnability**: Multiple measures (e.g., time, SEQ, completion) can be used at different points longitudinally as a measure of how [learnable](https://measuringu.com/measure-learnability/) an interface is.

**Change from Expectation**: [Comparing the same attitudinal measure](https://measuringu.com/predicted-usability/) (e.g., the SEQ) collected after reading the task description but before actually working on the task with the rating provided after experiencing the task. A drop suggests a poorer-than-expected experience and an increase suggests a better-than-expected experience.

**Disaster**: A “[disaster](https://measuringu.com/ui-disasters/)” (the term was coined by Gerry McGovern) occurs when a participant fails a task but is extremely confident it was completed successfully.

**Lostness**: A measure of how “lost” a participant is when looking for information. The [lostness metric](https://measuringu.com/lostness/) is calculated from (1) the number of unique page views relative to the minimum number of pages and (2) the total number of pages relative to the unique number of pages.

**Efficiency Ratio**: The [efficiency ratio](https://www.sciencedirect.com/topics/computer-science/common-industry-format#:~:text=The%20Common%20Industry%20Format%20for,task%20success%20per%20unit%20time.) can be measured at the task or participant level. For a task, it’s the percentage of successful task completions divided by the mean completion time. For a participant, it’s the number of completed tasks divided by the total time spent working on tasks.

## Summary and Discussion

In current practice, the essential task-based UX metrics are those associated with actions and attitudes. Less commonly used are behavioral/physiological and combined metrics.

**1\. Action metrics**: Fundamental action metrics are completion rates (can people successfully do what they want or are asked to do, a measure of effectiveness) and task times (a measure of efficiency). Findability rates, clicks/pageviews, and errors are additional action metrics.

**2\. Attitudinal metrics**: The fundamental attitudinal metric for tasks is perceived ease, commonly measured with the Single Ease Question. Other attitudinal metrics include ratings of confidence, task load, mental effort, expectation, and use of Usability Magnitude Estimation. Although not exactly the same, data from card sorting tasks can reveal mental models (cognitive and/or attitudinal) that potentially inform UI and IA design.

**3\. Behavioral and physiological metrics**: Of these metrics, probably the most common are those derived from eye-tracking (e.g., dwell time, fixation count, time till first fixation, pupil dilation). Other behavioral/physiological metrics that have been used in UX research and practice include facial expression coding, electrodermal activity, EMG, heart rate, EEG, fNIRS, and tapping.

**4\. Combined metrics**: The most commonly used combined metrics are the Single Usability Metric and learnability. This class of metrics also includes change from expectation, disaster, lostness, and efficiency ratio.
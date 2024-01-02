---
dg-publish: true
aliases:
  - Designing the user experience of the Emotional compass
tags:
  - my-projects
  - design
  - computer-science/software-engineering
note-type: null
description: null
file-created: 2023-12-30
file-modified: 2023-12-30
linter-yaml-title-alias: Designing the user experience of the Emotional compass
---

# Designing the user experience of the Emotional compass

#status/wip

I want to re-brand my [[Emotion wheel app project|emotional feelings wheel app project]] as an 'Emotion compass' - I think it's an excellent [[Use concept handles to represent complex ideas|concept handle]] for what I am trying to do. [[Annie Chen|Annie Chen]] since she is doing her master's in [[Product-design thinking|product design]] wants to have more things to add to her portfolio, so we chatted about my project [[2023-12-30]].

She recommends that for her to be able to help me with mockups, I should seek to write [[User stories in product design|user stories]] according to the [[Product-design thinking|product design thinking]] process.

## Possible personas

1. Tom, the Feelings Novice: Tom is a 35-year-old software engineer who has always had difficulty identifying and expressing his feelings. He often finds himself reacting without understanding why. He wishes to use the app to increase his emotional awareness and be more in tune with his feelings. His aim is to reduce reactionary behavior and feel more in control of his emotional responses.
2. Lisa, the Reflective Diarist: Lisa is a 27-year-old writer who values self-reflection and sees her mood fluctuations affecting her personal relationships and creativity. She wishes to use the app to log her emotions daily, noticing patterns and triggers. Lisa hopes to understand her mood trends, and adapt her lifestyle or mindset accordingly for better emotional balance and wellbeing.
3. Ryan, the Empathetic Explorer: Ryan is a 31-year-old HR manager. He interacts with a lot of people daily and struggles with understanding their emotional states. He feels this affects his relationships and decision making. He wishes to use the app to improve his ability to read and comprehend others' emotional states, and hopes to improve his interactions by nurturing empathy and understanding.
4. Sarah, the Emotional Scholar: Sarah is a 29-year-old psychiatrist who deeply understands the importance of emotional intelligence. She is always looking for ways to enhance her emotional intelligence even further. She wishes to use the app to get insights into her own emotional patterns and further develop her emotional intelligence. She believes this would enhance her professional skills and personal relationships.

## User stories for the emotional compass

1. As a user, I want the app to have a user-friendly, intuitive interface, so I can easily write journal entries and review the app's data and suggestions.
2. As a user, I want to be able to log my daily experiences and emotions, so that the app can keep track of my emotional history.
3. As a user, I want the app to have a user-friendly, intuitive interface, so I can easily write journal entries and review the app's data and suggestions.
4. As a user, I want to see my most frequently experienced emotions highlighted on the Emotional Feelings Wheel, so I can understand my own emotional trends.
5. ~~As a user, I want to receive insights and feedback on my emotional patterns, so that I can improve my self-awareness and emotional understanding.~~
6. ~~As a user, I want to receive insights and feedback on my emotional patterns, so that I can improve my self-awareness and emotional understanding.~~
7. ~~As a user, I want the app to provide me with strategies for emotional management based on my past entries, so I can better manage my emotional health.~~
8. ~~As a user, I want to be able to filter my journal entries by a selected emotion on the Emotional Feelings Wheel, so I can reflect on times when I have felt a particular emotion.~~

For Tom, the Feelings Novice:

1. As a feelings novice, I want the app to give me clear definitions and examples of various emotions, so that I can start accurately identifying what I'm feeling.
2. As a feelings novice, I want to use the Emotional Feelings Wheel to explore relationships among emotions, so that I can understand their complexity and depth.
3. As a feelings novice, I want the app to provide cues or prompts to help me articulate my feelings in the journal, so I can improve my emotional articulation.
4. As a feelings novice, I want prompts for self-reflection in the app that help me identify and analyze my feelings, so that I can understand myself better.
5. As a feelings novice, I want the app to provide me with simple coping techniques when I'm experiencing negative emotions, helping me manage difficult situations.
6. As a feelings novice, I want the app's machine learning algorithm to provide me with a starting point to analyze my emotions from my journal entries, so I reflect on my emotional experiences.
7. As a user, I want the app to indicate the related emotions on the Emotional Feelings Wheel based on my journal entries, so I can understand the complexity of my emotions.

For Lisa, the Reflective Diarist:

1. As a reflective diarist, I want to make daily entries in my emotional journal, so that I can track my mood over time.
2. As a reflective diarist, I want to view my emotional patterns graphically, so I can identify patterns or triggers easily.
3. As a reflective diarist, I want to be able to add personal notes about my day to my entries, so that I can draw correlations between events and my emotions.
4. As a reflective diarist, I want the ability to export and share my reports, so I can discuss them with my therapist or my support network.
5. As a reflective diarist, I want to to be encouraged to keeping making daily entries, ensuring consistency in tracking my moods.
6. As a reflective diarist, I want the app to suggest mindfulness exercises or activities that may help when I'm experiencing certain moods, so I can actively work on my emotional wellbeing.

For Ryan, the Empathetic Explorer:

1. As an empathetic explorer, I want to use the app to understand a wide range of emotions, so that I can better empathize with the people I interact with.
2. As an empathetic explorer, I want the app to provide me with resources or training modules on empathy, so I can practice and learn actively.
3. ~~As an empathetic explorer, I want to use a feature to log in the emotions I perceive in others during interactions, helping me track my progress and improve my empathizing abilities.~~

For Sarah, the Emotional Scholar:

1. As an emotional scholar, I want to gain insights into my emotional patterns and trends from the data the app provides, so I can continuously develop my emotional intelligence.
2. As an emotional scholar, I want to read expert resources and articles on emotional intelligence within the app, so I can expand my knowledge.
3. As an emotional scholar, I want the app to challenge me with advanced emotional vocabulary and concepts, so I can continue to challenge and enhance my emotional comprehension.\
4. As an emotional scholar, I want the app to offer challenges or quizzes to test my knowledge on emotional intelligence, so I can see how much I have improved.

## Task flows in the emotional compass

> [!warning] Written as of current flow - not the future/expected one

### Primary flow - daily entry

Core interaction loop (in principle)
1. Write - about your day/situation
2. Score - Machine learning/AI to generate scores
3. Embrace - Reflect and think if this reflects my emotional experience

Detailed:
1. Submitting a diary entry
	1. Load home page
	2. Scroll to text input box
	3. Type text
	4. Click submit to send information to ML model
2. View results
	1. Load results page
	2. Look at overall sentiment graph (positive, negative, ambiguous, neutral)
	3. Look at detailed emotion 'radar' (28 emotions score)
	4. See the submitted text (NOTE: should probably be moved down and use visual language cues to represent that it's not immediately relevant information. Use a grey backdrop?)
	5. See the individual printed scores of the results
3. Reflect on submitted emotional experience
	1. User reads and understands their rated score
	2. Prompt for 'similar/cousin' emotions to their current ones
	3. User has box to write additional notes about further reflections
	4. Provide strategies depending on the emotion that was detected?

### Other

1. Review past entries
	1. Scroll to top of page
	2. Click 'Review past entries'
	3. Read logs in chronological order

### Administrative

1. Delete all past log entries
	1. Go to past entries page
	2. Click button ('Clear all previous entries')
	3. Popup modal to ask for confirmation
	4. User read warning notification
	5. Click Clear button
2. Delete a specific entry
3. Export data
4. Import data (tbd)

## The concept of an emotional compass

> I've developed a website designed to assist you in uncovering and helping you refine how you express your emotions. Emotions are messy and complex - and sometimes it's hard to know what's going on.
>
> You can share your thoughts or describe a situation. Using a a machine learning model, your text is scored for various emotions (describe a bit more about the emotion taxonomy?). You can think of the results as an emotion compass.
>
> This unique feature aims to help you gain a clearer understanding of your feelings, providing a valuable reference point for self-reflection and emotional exploration.

## Competitive research

What do I like and dislike about them?

Competitors:
- Origin of Robert Plutchik's emotion wheel
- [https://allthefeelz.app/](https://allthefeelz.app/)
- [https://www.6seconds.org/2022/03/13/plutchik-wheel-emotions/](https://www.6seconds.org/2022/03/13/plutchik-wheel-emotions/)
- How we feel?
- Journaling apps
	- [5 Minute Journal: Self-Care - Apps on Google Play](https://play.google.com/store/apps/details?id=com.intelligentchange.fiveminutejournal&hl=en_CA&gl=US)
	- [Access to this page has been denied](https://www.calm.com/)
	- [DailyBean: Simplest Journal - Apps on Google Play](https://play.google.com/store/apps/details?id=com.bluesignum.bluediary)
	- [Moodpress - Mood Diary Tracker - Apps on Google Play](https://play.google.com/store/apps/details?id=com.selfcare.diary.mood.tracker.moodpress)

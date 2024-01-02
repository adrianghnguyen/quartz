---
dg-publish: false
monthly-notes: true
monthly-date: <%tp.date.now("YYYY-MM")%>
file-created: <%tp.date.now("YYYY-MM-DD")%>
file-modified: <%tp.date.now("YYYY-MM-DD")%>
tags: 
aliases:
  - <%tp.date.now("MMMM YYYY")%> 
---

# <%tp.date.now("MMMM YYYY")%> Monthly Note

#dailynotes  #dailynotes/monthly 
%% Monthly Log %%

## What are my monthly goals and objectives for this month?

> [!help]- What are 3 things I wish to accomplish this month?
>
> - What are things I may wish to focus on?
> - Any particular lessons I want to apply moving forward?
> - Any goals which need to be carried out?
> 
> Remember the key principles in [[Create effective goals|making effective goals]]:
> 1. **SMART Goals:** Formulate specific, measurable, achievable, relevant, and time-bound objectives.
> 2. **Break Down Goals:** Divide larger goals into smaller, manageable steps.
> 3. **Action Verbs:** Use dynamic action verbs to clarify your goals.
> 4. **Prioritize and Plan:** Choose top-priority goals, outline tasks, and set deadlines. It's important to make a limit. We can't do everything.
> 5. **Regular Review:** Monitor progress, adjust plans, and stay aligned with aspirations.


On-going monthly objectives - decide on their priority or prune them:
```tasks
tags include #dailynotes/monthly 
not done
short mode
```

Added objectives:

---
## Key monthly events

> [!help]- [[Personal memory dashboard|Review what happened last month]] in this present month which may be worth remembering?
> 
> 
> **Achievements and Growth:**
> - Personal achievements
> - Career changes
> - Overcoming challenges
> - Personal growth insights
> 
> **Celebrations and Relationships:**
> 
> - Special celebrations
> - Relationship milestones
> 
> **Experiences and Exploration:**
> 
> - Travel experiences
> - Passion projects
> - Meaningful media moments
> 
> **Wellness and Reflection:**
> 
> - Health updates
> - Self-reflection
> 
> **Transitions and Lifestyle:**
> 
> - Lifestyle shifts
> - Life events

```dataview
TABLE
	importance as "!",
	event as "Daily event"
FROM #dailynotes
WHERE 
	date(<%tp.file.title%>-01) < date(file.name) AND date(file.name) < date(<%tp.file.title%>-32)
	AND event != null
SORT file.name
```

---
## Personal reflections about the month

> [!help]- Looking backwards into the past month and reviewing it.
> - What are things for which I am grateful?
> - What were some of the challenges?
> - What are some lessons which I've learned? In what ways have I grown as a person?

#### Completed objectives of the month

Be proud of what you've accomplished this month!
```tasks
tags include #dailynotes/monthly 
done in <%tp.file.title%>-01 <%tp.file.title%>-31 
sort by done
short mode
```
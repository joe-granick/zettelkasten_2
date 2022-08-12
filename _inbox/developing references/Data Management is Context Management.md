Tags: [[Data context]]
Links:[[Data cleaning is analysis]]
Date: 202204260924
Tags: #blog
Topics: [[Data context]], [[Analytics Engineering]], [[Data Science]]
Author: [Randy Au](https://substack.com/profile/6437090-randy-au)
Year: 2022
Links:
URL: https://counting.substack.com/p/data-management-is-context-management?token=eyJ1c2VyX2lkIjoyNzAwNDkxMiwicG9zdF9pZCI6NTI2ODIyOTcsIl8iOiJLampRRiIsImlhdCI6MTY1MDk3NTE2NSwiZXhwIjoxNjUwOTc4NzY1LCJpc3MiOiJwdWItMjc4NDkiLCJzdWIiOiJwb3N0LXJlYWN0aW9uIn0.B3BmTOlradHxKvVvil--o5XYBeHS5dZmJCfri0p4Qkc&s=r

#Notes
>"**data analysis is flat out impossible without context**."

>One obvious aspect about working with data is that math behaves exactly the same no matter what kind of data or context you apply it to. _[An oversimplification — people in the back, especially the pure mathematicians with stacks [of axioms](https://en.wikipedia.org/wiki/Axiom_of_choice), can simmer down.]_ This property of “how numbers work is universal” gives us data practitioners a highly portable toolbox

>But when it comes to the most critical part of analysis, pulling a conclusion or narrative out of data, those math tools are insufficient. Context is what’s necessary for the task.

>This time around, I want to take things one step further and argue that _data management is the art of manipulating, destroying, preserving, transmitting context._

>In order to make data more useful and put together a stronger narrative, an analyst has to _bring in context_ from other sources.

>Depending on what narrative and what analysis, the analyst wants to build, they have to layer on different things from different sources.

>**The act of counting and grouping is, by necessity, context destroying**.

>Right from the outset, before we even have data, we’ve already made important decisions as to what “counts” as being counted. That’s the first bit of context associated with our data.

>But once data is collected, there are still many more places where we must manipulate the context. Every step of aggregation or deleting fields would obviously remove context from the data set. All those decisions becomes embedded within our resulting data set and we need to communicate those decisions downstream.

>But not all data work is about destruction. We can also add context via joining in other data sets or just overlaying context in parallel. Think about all those fact tables we have, or how that population data overlaid the Black Death to explain a dip. We're trained to leave things like join keys and unique identifiers in our data specifically to enable this sort of operation, but it’s not even a hard requirement that different bits of data “join” cleanly.
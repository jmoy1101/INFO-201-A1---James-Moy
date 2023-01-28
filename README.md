# Assignment 1: Protests

During the past few years in the United States, there has been a surge of protests in support of the Black Lives Matter movement, women's rights, trans rights, immigration reform, gun control, the environment, and many other social and political issues.

In this assignment, you will work with data from [CountLove](https://countlove.org/), a group that collects data about protests from across the United States, including information about the purpose of the protests, the location of the protests, as well as how many people attended the protests. This data has often been [cited by the *New York Times*](https://www.nytimes.com/2020/08/28/us/black-lives-matter-protest.html), among other major outlets.

Through this assignment, you will be able to answer questions including:
- What were the most attended and least attended protests in the US in the last 5 years?
- How many protests occurred in Washington state?
- How did the number of protests in 2019 compare to 2020, and why?
- Why are people protesting in the US? What are the biggest motivators?


This assignment is divided into 2 parts. You will complete your coding work in the `analysis.R` file, and you will write short answer responses related to critical analysis and reflection of the data in this `README.md` file. Before getting started on your coding work, you should complete the section **"Critical Analysis & Reflection: Before You Code"** below.

When you are finished with the assignment, be sure to push all changes to your GitHub repository and then submit the link on Canvas.

## Before You Code: Critical Analysis & Reflection

Before diving into this (or any) dataset, it's important to know where the data came from, and it's important to have or to seek out _domain familiarity_ — in other words, knowledge about the subject/topic of the dataset. (We don't want to be "strangers in the dataset," as Catherine D'Ignazio and Lauren Klein describe it.)

To get more familiar, we are going to begin by doing some background reading. 

- First, please read [this FAQ](https://countlove.org/faq.html) from the CountLove website and the opening of [this blog post](https://www.tommyleung.com/countLove/index.htm). Based on the information in these pieces, why did the creators start collecting the CountLove data? Please answer in 2-3 sentences (3 points)

Protests are enshrined in the first amendment of the Bill of Rights and are also a clear form of communication/negotiation between citizens of a nation and government. Many times, the regional protests are not covered by national news or have data collected about them made available to the public. The creators started collecting CountLove data because they saw a need for public access to protest data around civil rights, immigration, racial injustice, and other important societal issues across the United States.


- Next, we would like you to read this [*New York Times* piece, which uses CountLove data](https://www.nytimes.com/interactive/2020/06/13/us/george-floyd-protests-cities-photos.html) (here's a [Google Doc version for anyone who gets paywalled](https://docs.google.com/document/d/1sdjFsA5csYuH4plNEEk7WXT77K5h5ZuyW05CBwYdk6A/edit?usp=sharing)), and which describes the Black Lives Matter protests that occurred in the summer of 2020. Please summarize the main point or argument of this article in 2-3 sentences (3 points)

The article highlights the widespread movement of BLM and the support and outrage against police brutality that arose following the murder of George Floyd. I feel that this article highlights protesting as a form of representation and power of citizens in civil rights disputes. It promotes this use of pushback against the government as a useful tool for activists. 

Next, we're going to reflect about who collected this data, and what's actually inside it.

- Who collected and shared the CountLove data, and what do they do for a living? Please answer in 1-2 sentences(2 points)

Tommy Leung and Nathan Perkins are the founders of CountLove data. They are engineers and scientists with a keen interest in civic responsibility and public policy.

- As Klein and D'Ignazio remind us, when it comes to data, "what gets counted counts." What types of demonstrations does CountLove include in their data, and what types do they exclude? (3 points)

CountLove aggregates information about protests by citing primary sources such as news articles and videos and then manually codes the date of the protest, the number of attendees, and the general topic of the protest. Public displays that are not considered "regular business are counted. wareness events, commemorative celebrations, historic reenactments, fundraising events, townhalls, or political campaign rallies are not included in the data. 

- How and where does CountLove get their data about the protests? Please answer in 2-3 sentences (2 points)

Using several programs, CountLove craws local newspapers and television stations for keywords such as "march," "rally," "protest," or "demonstration. These identified data points are then sent in for review where they are determined to either qualify or not qualify based on the context of the protest.

- How does CountLove make their estimates about the number of people who attended a protest? What potential problems might arise from this method of estimation? Please answer in 3-4 sentences (4 points)

CountLove takes conservative estimates of the number of attendees at events: for example, “a dozen” as 10, “dozens” as 20, “hundreds” as 100 and does not include a countable number of protestors if none is provided.  believe they do this to prevent dramatic exaggerations in data. Many times, observations and memories tend to exaggerate statistical facts about data so taking a conservative approach during data collection is most-likely safer than the other way around. 

## While You Code: Critical Analysis & Reflection

- Reflection 1: Why do you think the mean is higher than the median? Which metric would you use in a report about this data, and why? Please answer in 2-3 sentences (2 points)

I think the mean is higher than the median because the data is skewed so that outlires in large amounts of protesters are making the median amount much lower than the mean amount. I would use a metric that measured number of protesters compared as a percentage of the population.

- Reflection 2: Before actually calculating the number of protests that occurred in 2018, 2019, 2020, record your guesses for the following questions. (1 point)




  Guess: Do you think there were more protests in 2019 than in 2018? Why or why not? Please answer in 1 or 2 sentences
  
  I believe there were more protests in 2019 than 2018 because the country has become very divided, especially in recent years and through Trump's presidency. 

  Guess: Do you think there were more protests in 2020 than in 2019? Why or why not? Please answer in 1 or 2 sentences
  
  There definitely were more protests in 202 because of both the Covid-19 Pandemic, the lockdown, the George Floyd protests, and the upcoming presidential election.

- Reflection 3: Does the change in the number of protests from 2018 to 2019 to 2020 surprise you? Why or why not? What do you think explains the fluctuation? Please answer in 1 or 2 sentences (2 points)

The change does surprise me because 2018 compared to 2019 appears like it has more protests even though 2019 contained more problems in the news. 

- Reflection 4: What is the first and fourth most frequent category of protest? Do these frequencies align with your sense of the major protest movements in the U.S. in the last few years? Why or why not? (3 points)

## After You Code: Critical Analysis & Reflection

In the second chapter of *Data Feminism*, Klein and D'Ignazio describe 4 ways that data scientists can challenge power and take action:

> Taking action can itself take many forms, and in this chapter we offer four starting points:  

> (1) Collect: Compiling counterdata—in the face of missing data or institutional neglect—offers a powerful starting point as we see in the example of the DGEI, or in María Salguero’s femicide maps discussed in chapter 1.  

> (2) Analyze: Challenging power often requires demonstrating inequitable outcomes across groups, and new computational methods are being developed to audit opaque algorithms and hold institutions accountable.  

> (3) Imagine: We cannot only focus on inequitable outcomes, because then we will never get to the root cause of injustice. In order to truly dismantle power, we have to imagine our end point not as “fairness,” but as co-liberation.  

> (4) Teach: The identities of data scientists matter, so how might we engage and empower newcomers to the field in order to shift the demographics and cultivate the next generation of data feminists?  

- How does the CountLove project embody one or more of these 4 forms of challenging power? Please answer in at least 3-4 sentences (3 points)

The CountLove project embodies (1)Collect and (4)Teach, not just in a traditional sense but also in how they explain their mission and purpose. The project is focused on collecting data about protests across all forms of media across the country to uncover and highlight movements and outcries from the population that went mostly unnoticed. This awareness also teaches us about the value of these programs and software to identify key points of data and how we can compile and organize it to gain insights. 

- What is the most interesting or surprising thing you learned from this analysis? Please answer in at least 2-3 sentences (2 points)

The most interesting and surprising thing I learned from this analysis is that there were more protests in 2018 than 2019. Several factors probably contributed to this however I believe that the most disruptive factors were that "news propoganda" and accusations of fake news supported by sections of the government were more prevalent in 2018 than 2019.


- What is a kind of analysis that you would like to do or that would be interesting to do with the CountLove data that you don't have the time or skills to accomplish at this moment? Please answer in at least 2-3 sentences (2 points)


I would like to determine which areas are much more susceptible to protests, and cross reference them with specific regions that are impacted by other factors to determine a root cause. This way I would be able to work with the data and gain practical insights that can help determine how the data can be useful. 
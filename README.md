# Negation_project

<h2>AskFm Dataset</h2>
The AskFm primarily used for asking questions either publicly or anonymously and then getting answers from other users. To collect each user's questions and answers, we have crawled each of the profiles using Python web crawler library, Beautiful Soup. Questions and answers associated with each user profile are saved in a CSV file. Question-answer pairs are only extracted if they contain cyberbullying swear words, which were filtered by a string matching technique. In total, we crawled 3720 user profiles and over 400,000 question-answer pairs. Public proxy servers located in the UK, CA, and the USA were employed to retrieve English written posts. Applying insult/swear words string matching reduced the data to 10k unique posts, containing at least one insult/swear word either in the question or in the answer parts. 

We have manually labeled the resulting 10k AskFM dataset. Labeling involves identifying whether each sentence contains cyberbullying or not.  A critical hypothesis developed based on some social science and psychiatry findings, that cyberbullying case must include both insult/swear wording and a second person/person's name . If there is no second person/person's name available, it may not be considered cyberbullying other than general HS.

However, this determination is not that simple; for example,  "This is bad, but John Doe is lucky" includes both Insult word and Person name; however,  it is not an HS or cyberbullying case as the relationship between the two is not established.

Nevertheless, "John Doe is not bad," contains both person name, Insult word, and a correlation between the two has been established. Still, it is not an HS or cyberbullying case due to the negation of words. Similarly,  'John Doe is not a good person,' does not contain Insult words but is considered as both HS and cyberbullying. In the sentence, 'Asylum seekers are dirty,' has an Insult word and target; it falls into HS but is not categorized as cyberbullying because its target is not a person / second person.

Besides, HS could work differently if multiple sentences are put together. For example,  "John doe working hard. Ugly" is an HS, Cyberbullying and Offensive cases even though the second sentence "Ugly" contains only an Insult word without any second-person/Person entity.

These examples show the requirements mentioned above for HS, cyberbullying, and other cases are the necessary conditions; though, it is not compulsory due to the variety of natural language modifiers expressing negation and opposition. 
 
Two independent labelers (who have  knowledge in this field and completed a master's thesis on cyberbullying detection and NLP) have been employed separately for annotation for avoiding bias. While a third one (a senior research fellow and completed his Ph.D. in this field) is called upon whenever a disagreement between the two arises (total disagreement 141).  We attribute the label '1' to a sentence if it is associated with cyberbullying and '0' otherwise.

<h2>FormSpring Dataset</h2>
The second dataset that we have used was collected from fromspring.me, which is publicly accessible. The data represent 50 IDs from FormSpring.me that were crawled in the Summer of 2010. For each ID, the profile information and each post (question and answer) were extracted. Each post was loaded into Amazon's Mechanical Turk and labeled by three workers for cyberbullying content. The same labeling mechanism as before is used here, as illustrated in  The FormSpring dataset contains 12k posts in which 7\% contains cyberbullying.


<h2>Hasoc-2021 dataset</h2>



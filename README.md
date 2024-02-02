# Sustainability in Fashion
_By: Taylor Noh, Olivia Oracion, Karni Velumani, Sheila Lobato_


## INTRODUCTION:
### (Problem Description)
With the rising appeal of ethical and eco-friendly consumption, sustainable fashion has grown in popularity over the last decade. However, as companies join the sustainable fashion industry, consumers continue to inquire about the environmental and economic impacts of clothing production processes, specifically on social media platforms. In addition, the transparency and honesty of these companies may be questioned with regard to factors of production. This includes, but is not limited to labor issues, energy and gas emissions, and water consumption. With all constituents considered, we recognize the validity of questioning the credibility of sustainable fashion and its impacts on consumer habits. 

## BODY:
### (Solution Description)
In our analysis, we retrieve live data from Twitter to further examine specific tweets in regards to the terms of “sustainability” and “fashion”. This data is provided throughout the course of the entire year of 2019 and references any mentions of sustainable fashion. Given a large dataset, we retrieve the tweet column and order the highest word occurrences to determine the frequency of certain terms and to produce a word cloud. The first step we took was reading the CSV file "twitter_sustainablefashion_fashiontransparency.csv” (read_csv). We then typed in select(tweet) to select only the tweet column of the dataset. Since coding can be case sensitive, we used the unesting function: unnest_tokens(input=tweet, output=tweets) to make everything lowercase so that it would fit into the tidytext format. After that we wanted to find out the frequency of certain words like “sustainable fashion” and “fashion transparency” or other relevant words in the tweets dataset. Using the count(word) input, the program was able to count word occurrences related to our topic. Our output was narrowed further when we input
filter(n>50), which allowed us to keep word occurrences that appeared greater than 50 times.
Through this analysis, associated terms rose out of the provided data as a much more attractive visual interpretation. However, the individual words had a high amount of filler words that served no meaning and were removed using anti_join(stop_words). For easier visibility, the function arrange(desc(n)) was used to rank the terms from highest to lowest frequency. As a result, we produced a wordcloud to represent the conclusion of the analysis.

## CONCLUSION: 
### (Results and Conclusion)
In recent years, consumers have realized the importance of a sustainable lifestyle. Sustainability can be applied in many parts of our lives. One area of consumption that can be more sustainably sourced, is clothing. Newer businesses are offering a greener approach to clothing put on the market. Utilizing consumer data will allow us to dive deeper into how successful these brands are and what impact they can have on the environment.

In our project, we gathered text data from Twitter to perform a detailed analysis on consumer consensus. On the Twitter platform, users are able to “tweet” messages out into the public. These messages give us information on a tweeter’s opinion on various topics. 

Using the RStudio environment and R programming language, we were able to pull twitter data specifically related to topics like “sustainable fashion” and “brand transparency”. Utilizing the RStudio packages, we were able to filter through our data in helpful ways like formatting it into a table by word occurrence. Below you can see another method we used in R, where we created a word cloud to better visualize the other words that had been produced in concurrence with “sustainability” and “fashion”. This gives us a better idea of what other avenues our research should be directed towards to learn more about sustainable fashion.

<img width="389" alt="image" src="https://github.com/karnikaavelumani/sustainability-in-fashion/assets/60043611/84da74bd-1e68-42ab-b5b8-8526227c9aa4">

## NEXT STEPS:
### (Future Work)
With the data collected, we can see that other words such as “etsy”, “vegan”, “ silk”, “jewelry” and so on are related to the topic of sustainable fashion. Each word can carry more information on how sustainable fashion is created and distributed. This can be helpful for users, as we can find more information on how consumers can find various ways on how to source their clothing items, what types of accessories are available, and what other causes sustainable fashion can contribute to.

Considering what we have learned throughout the course of the program, we recognize our potential ability to conduct further research and analysis. To analyze consumers’ responses to sustainable fashion on social media, we could filter the tweets by sentiment; comparing the amount of “negative” and “positive” words in each tweet. 

These words could refer to the price of sustainable products or the company’s transparency. Using this data, we can identify why consumers tend to choose or stray away from purchasing from sustainable fashion brands. In addition, we could simply filter tweets by their positive words that compare sustainable fashion to the general fashion industry. If successful, the analysis would illustrate a positive comparison between the two and feasibly promote sustainable fashion as a notable option for consumers. 

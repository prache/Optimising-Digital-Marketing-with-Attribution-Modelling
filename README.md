# Digital-marketing-attribution 
## Goal:
In the current project my main goal is to have deeper understanding about the attribution model selection. Selecting a correct model is the mammoth challenge in data science.
Hereby I consider a case where the marketing team wants to know how much contribution from the provided budget they should invest in marketing channels? 

## Data:
A dataset is from kaggle 
which contains cookies as an indentifier of the customer, timestamps, and the channels. Data contains half a million enteries with five columns.

![Screenshot from 2023-08-18 16-27-55](https://github.com/prache/Digital-marketing-attribution/assets/25516674/d4bd0015-f85d-439d-8a54-5a42b98af21e)

## What is attribution?:
Once we feed the data to chosen model then it can predict for the future campaign. Hence choosing the model is the most crucial step in predicting the future/forecast. 
Attribution is that where the sales of the brand is caused by some action taken towards the sales. For example, correct investment in product marketing channel.

## Selecting attribution model:
"Any model can be chosen depending on the question and focus!”

Mapping of the whole touchpoint journey of the customers is required for the current question. Since I need to investigate the customers behaviour through channels.

Only analysing single touches such as first and last touch would not be useful in this case. Question needs to choose multi-touch model to have complete picture of customers interactions.
All the channels responsible for conversion are given equal credits. I believe that every channel is as important as the last one where we purchase it. If I think about the customers behavior, it can be super random with their diverse nature. In each touchpoint their brain learns about the brand and therefore I believe each touchpoint deserves equal credits. However, time-decay is also interesting where we give credits to intial touches more and go decreasing it until the end touch. Here, the customers brain learns about brand at first touch and then slowly it gets fixed into the memory. That brings ease for the customer to take a decision of purchase. Neverthless, 'that ease' can not be given less credits in my opinion. I still standby the even credits here. Hence chose the linear model.

One of the popular linear models is Markov-chain forecasting model. It calculates the probability of interaction between pairs of media channels with the transition Matrix. It also takes into account the removal effect. where it simulates the removal of each touch point and calculates how the conversions would change. Higher the removal effect value higher the impact of that channel.

## Methods to reach goal:
1. Not only Markov-chain forecasting model was performed but also first-touch attribution, last-touch attribution, time-decay, Markov, and Shapley.
2. Shapley is an intersting multi-touch linear model. It comes from evolutionary biology, game theory. It is a solution concept in cooperative game theory.
   However, it does not consider removal effect.
3. I chose to perform all the models and compared them in bar-plot.

## Results:
## Markov model heatmap
![image](https://github.com/prache/Digital-marketing-attribution/assets/25516674/e88bdf7d-708e-471f-8ea6-abb90f615a20)

### Inference: 
Heat map results suggest that the transition from facebook to instagram is 0.6. Which is higher as compared to the other transition matrix. Meaning that customers most preferred moving path is facebook to instagram. And then Instagram to facebook (0.39).

## Removal effect (Markov model)
![image](https://github.com/prache/Digital-marketing-attribution/assets/25516674/5765e417-94bc-4680-98fb-8c2cc7eb5aa5)

### Inference:
Removal effect showed that the most impactful channel after removing from the map are facebook and paid search.

## All the models comparison by each channel
![image](https://github.com/prache/Digital-marketing-attribution/assets/25516674/abbb01e8-efcb-4344-813e-539406cd3bee)

### Inference: combination of different models compare the calculated values. 
Facebook and paid search respectively are the most encountered channels.
All the bars displayed no significant difference in the height except that Instagram Markov model is too high compared to the other models. 
To examine in detail, the next plot is generated.

## Comparing only algorithmic models 
![image](https://github.com/prache/Digital-marketing-attribution/assets/25516674/35d1e988-ac95-4165-9193-8b37530bce9a)

### Inference:
Instagram and online video has contrasting results. 
Markov model simulates the removal of each touch point and calculates how the conversions would change. 
That is a cornerstone to consider Markov model over shapley.

## Recommendations to the marketing team:
The brand should invest 42% of the marketing resources in upcoming facebook advertising campaign to optimize marketing efficiency.
And the next targets could be paid search 31% and Instagram 27% respectively.





 





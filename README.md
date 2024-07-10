# Statistics and Data Science
This repsository contains three notebooks outlining a complete modelling process from statistical analysis, data preprocessing and model building. It is intended to display my understanding of the core learning outcomes of the modules:
- Statistics [STAT H1003](https://www.tudublin.ie/study/modules/stat-h1003-statistics/)
- Data Adminastration and Analysis [DATA H2001](https://www.tudublin.ie/study/modules/data-h2001-data-administration-and-analysis/)
- Logic and Problem Solving [LOGC H3001](https://www.tudublin.ie/study/modules/logc-h3001-logic-and-problem-solving/)

## Actor Critic Model ([Actor_Critic.ipynb](Actor_Critic.ipynb))
I believe this approach is entirely unique as, while there is significant research in applying reinforcement learning to investing, I have not found any academic paper or book that uses this specific approach. 

The key aspect in which this approach differs from the current approaches is the available actions. Current approaches provide the agent with the option to buy, sell or ignore. The agent then displays a tendency to do nothing at all and the approach yields no insight. 

My approach is to force the agent to “buy/sell” and then decide on the optimal trading strategy with the goal of maximising returns. The agent chooses from an action list of percentage changes which represent when the agent would like to exit. This is done to more closely resemble the process a trader follows.

While the actor model learns the optimal action, the critic model learns the value function. The value function will represent the expected cumulative reward, starting in this state, following the optimal policy. Once the model is sufficiently accurate we can use the critic value to generate alphas by inputing current stock prices and flagging stocks that have a forecasted value of >0.

This model was built using no reinforcement learning library’s with all the required functions being written directly. 

## Statistical Analysis ([Statistical_Analysis.ipynb](Statistical_Analysis.ipynb))
This notebook outlines the statistical analysis that I believe justifies the use of this specific model. It outlines how financial prices are non-stationary and not normally distributed. It also shows that while there is no correlation between the time steps in the series, the series is not independent and hence there are potential patterns to model.

## Data Preprocessing ([Data_Preprocessing.ipynb](Data_Preprocessing.ipynb))
This notebook shows the data preprocessing used to create the csv file used in the actor critic model. 

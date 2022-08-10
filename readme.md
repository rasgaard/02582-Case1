# Case 1 in 02582 Computational Data Analysis (F2022)

Something which I felt that I missed when doing this assignment was a point of reference as to what to do and not to do. My hope is that this will provide a sort of reference for someone in the future. 

The report is available in `report.pdf` and the case description can be found in `Case for 02582 - Forecasting for airports.pdf`.

While the model did not perform well we got a score of 90.75% for the assignment which itself accounts for 20% of the final grade when taking the course in F2022.

## Feedback on report from teaching assistant

Overall a very nice report. You have carefully considered and argued for your model choice as well as model selection and validation procedures. You show a fine understanding of the tradeoffs between the various aspects of the case / data. 

Some additional comments: 
* Good introduction. Nice with a table of the attributes. 
* Good model description and argumentation. 
* Your feature transformation of the time variable is acceptable. As you state, it could also have been beneficial to decompose it into several time variables. As it stands right now, you are not capturing the cyclical nature of some possible time attributes like hour of the day or month of the year. I.e. the 23rd hour of the day is close to the 1st hour of the day. And January is close to December. A sine / cosine transform could have been considered to capture this cyclical nature of extracted time variables. 
* For the categorial features you state that you one-hot encode them since many ML models require this. You are however using RF and specifically chose this model based on its ability to handle categorical features. Of course if you are using python then sklearn does not currently support non-transformed categories. 
* For the model selection and validation really good job taking into account the effects of the data being a time series (and demonstrating this with a plot). I like that you have thought about the tradeoff from doing a modified CV specifically for time series data. Also good job using bayesian optim with optuna. For this you could have included how many trials you performed and how large the parameter grids you optimized for are. 
* For the final result you reference the case description for the accuracy metric you are using, but since you have the space, it would have been nice with a short description of it in the report. 

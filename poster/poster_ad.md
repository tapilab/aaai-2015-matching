# Poster ad: Using Matched Samples to Estimate the Effects of Exercise on Mental Health from Twitter

Hello, I am Virgile Landeiro and I am going to introduce you our paper: “Using Matched Samples to Estimate the Effects of Exercise on Mental Health from Twitter”.

In this paper, we started by assessing that traditional observational studies on the effects of exercise on mental health were limited by cost to both small sample sizes and short time windows.

The solution we designed is to use Twitter data to populate the groups of our observational study. This solution allows us to build large groups of user over a time window of variable size.

We rely on physical activity tracking apps - which one can run on basically any smartphone - to detect physically active users: this is how the experimental group is produced.

The most important step of this study lies in the method to build the control group from the treatment group. As individuals are not randomly assigned to treatment and controls groups in an observational study, we cannot randomly select individuals from Twitter to build the control group. Instead, we use matching to identify a control group that is similar to the experimental group.

For every individual i in the treatment group, we look for a best match amongst the friends of i. We filter out friends that are not of the same gender, we keep friends only if they live in the same location. Then, we compute a cosine similarity score for the remaining friends on their social activity (# friends, # tweets, etc). Finally, we get the friend with the top score to include to the control group.

By applying this process to every user in the treatment group, we build a control group that has the same size than the treatment group.

Once we have built the two groups for our observational study, we use a text classifier in order to decide if a given individual shows signs of dejection, anxiety, and/or hostility. 

We find that users who exercise regularly have significantly fewer tweets expressing dejection or anxiety, there is no significant difference in rates of tweets expressing hostility.


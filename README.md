# w251_hw6 by abhisha@berkeley.edu

This assignment addresses hw6 in w251 indicated here: https://github.com/MIDS-scaling-up/v2/tree/master/week06/hw

This assignment consists of 2 folders - p100 and v100 - indicating which VM types the BERT model was run on. A few notable points. The p100 was an order of magnitude slower than the v100 VM. To train the same BERT model on v100, it only took a few hours - 1 epoch took around 3-4 hours, whereas the same on a p100 took over 12 hours.

The classification AUC of the models was around 96-97% in both cases. Here is a sample result from the classification:

### Sample Positive Sentence
'Rolling Stone supports the nationalization of the means of production*, democratization of the workplace*, income distribution*, food and education for the poor* and peace and prosperity*??  Who knew?\n\nWow, I should subscribe.\n\n\n*Look those things up'

### Sample Negative Sentence
Trump is a mentally unbalanced buffoon.\nHe's unfit for office.\nHe's the largest threat to our nation's security and Congress should exercise it's responsibility and remove him now.\nHe's a petty con man, a racist supremacist, a sexual predator and a traitor.\nWorst ever.


For the v100, I decided to train the model again with 2 epochs. I didnt realize much difference in AUC scores (still around 97%). The sentences were also convincingly classified into positive and negative.

For the p100, I decided to upload the model to Kaggle to see how it compares on the leaderboard. Here is the link to the notebook that was created in kaggle: https://www.kaggle.com/abhisharma1991/kernel6c5b2316b3?scriptVersionId=35852175

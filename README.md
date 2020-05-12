# High_Cardinality_Encoding


High Cardinality columns are common problem when we deal with categorical data having lots of unique values and we often find it challenging to deal with it. Here are some exploration I encountered with, when I had same problem in one of my project. I'm sharing my understand. Please comment and suggest any changes.

There are many ways we can encode these categorical variables as numbers and use them in an algorithm. There are some techniques I tried according to the problem given.
I've tried all these solution on my data set and Mean encoding was the one fitting with my data.

One hot encoding
Mean Encoding
Hashing Encoding
Weight of Evidence (Mostly good for Classification( Logistic Regression))
Hashing Encoding (Discard)
I could create encoding around these methods but I was unsure if we are ready to loos any information or ready to handle curse of dimensity. Even we do PCA after Hash/ OEH but again had to loose some of the information.

Mean Encoding (Accepted)

After trying different encoding I found out if our moto is not to loose any information and still convert those large number of unique values(Categorical) into continuous, we can use 'Mean Encoding'. Mean Encoding will not create huge dimension, its like label encoding except here labels are correlated directly with the target.

cons : Mean encoding is notorious for over-fitting; thus, a regularization with cross-validation or some other approach is a must on most occasions.

Closing Note

There were other technics which were in mind e.g. **Leave One Out ** Encoding which could be the good choice because it can deal with outliers.

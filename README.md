# Naive Bayes Classifier for Spam Detection 
### Why 'naive'?
Conditional independence assumption: assume all features in $X=(x[1],x[2],...,x[d])$ (d-dimension vector) are independent condition on Ck <br>


### Laplace Smoothing
If a feature is not in available training dataset, it will result in $P(x[i]|C_k)=0$, making the resulting probability $0$. <br>
For example, our features are 'money', 'wealth', 'miracle', 'happy'. <br>
- For non-spam dataset, we observe and calculate $P(x[i]|non-spam)=certain$ $value$ <br>
- For spam dataset, we do not observe 'happy' at all. $P(x[4]=1|spam)=0$ <br>
- For testing sentence, we have 'Happy money'. Since it contains 'happy', $P(x[4]=1|spam)=0$ in the numerator drives $P(spam|X)$ to $0$. It will always be classified as non-spam.<br>

Laplace smoothing adds a constant m into conditional probability calculation to avoid the above scenario.
![image](https://user-images.githubusercontent.com/71556325/199142451-3db1db20-98a3-41f4-af97-525fca28d1cf.png)

# Cradlewise

## Questions

1) Is it necessary that two signals are the same if their autocorrelation functions are the
same? What about auto-convolution?
2) A particular data set needs human help for classification. But the dataset is huge and
the number of people available to you for classification is limited. What ideas can you try
to make the job easier?
3) If you have a set of floating point numbers which are approximate multiples of a
single number X (say within +/- 5%), how would you go about finding the largest
possible X?

## Answers

## 1 )

### Autocorrelation
yes ,Two signals are same if autocorrelation of the two signals are same.
### Autoconvolution
Yes ,Two signals are same if autoconvolution of the two signals are same. <br>

Please, Refer this [file](https://github.com/guruprasaad123/cradlewise/blob/master/correlation_convolution.ipynb).<br>


## 2)

If the large dataset requires persons help ,

### Solution 1 :

My idea would be to train a Reinforcement-Learning-Model under a environment in which people will let the model do the classification for non-similar datas in the huge dataset for making the model more generalized in nature,provide `Positive-Rewards` for the correct classification and `Negative-Rewards` for wrong classification so that it could perform well on Real-time-Scenario.

By this way we'll need to spend some time for training the model But, once it get trained we can use the model for any Large datasets.

Inspired by `OpenAI 5v5`.

Resources :

https://www.youtube.com/watch?v=DzzFSyzv1p0

### Solution 2 :

Second one will be to use Generative-Adversarial-Networks to imitate the people doing the classification on some small folds of the huge dataset.

Resouces :

[https://towardsdatascience.com/how-i-got-a-computer-to-make-fake-people-using-ai-gans-a8e2f542e992](https://towardsdatascience.com/how-i-got-a-computer-to-make-fake-people-using-ai-gans-a8e2f542e992)

## 3)

My idea programmatically would be to iterate over all of the permutation and find the largest possible number X.<br>

```python
from itertools import permutations 
def largest(l): 
    lst = [] 
    for i in permutations(l, len(l)): 

        lst.append("".join(map(str,i)))  
    return max(lst) 
```


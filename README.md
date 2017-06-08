
## Compute Statistics from Card Draws

### Liang Sun      
### June 7, 2017

-----

### 1. Distribution of Card Values

A set of cards has 52 values (excluding two jokers). Jack, Queen, and King are given a value of 10. Other cards have their face value.

``` python
card_values = [1,2,3,4,5,6,7,8,9,10,10,10,10]*4
```

The relative frequencies of the card values for a single draw is shown in the histogram below:

![draw](/image/draw.jpg)

- The mean of the value distribution is 6.54.
- The median of the value distribution is 7.00.
- The variance of the value distribution is 3.15.

-----

## 2. Sample distribution of three-card sum

A sample of 30 draws of three cards from the set is generated.

```
Kc 2d Js
Ah 5d 5s
2h 5h 4c
Ks 9h 5h
2c 9h 7d
Jh 3s Jd
Ad 7h Ah
Jh 5d 10h
3c As 2d
5d 3d Qc
10d Ac 6h
4d 2c 6s
10c 5s 9d
Ks 2c Kc
Jc 9h 7c
4c As 5c
Ah 10s 8d
Jh As 2s
Kh Kc 5s
8h 10d 9s
2s 5d As
Ah Kc 8s
3c 2s 3d
10d 3c As
2d Jd 4c
Qc Ah 10d
4s 8d Jc
8h Kc 8s
2s 2d 2h
9d Ad 2h

```

``` python
sample_sum = [22,11,11,24,18,23,9,25,6,18,17,12,24,22,26,10,19,13,25,27,8,19,8,14,16,21,22,26,6,12]
```

Here are some descriptive statistics from the sample:


Estimate of population mean:  ![1](/image/1.jpg)

Estimate of population median = 18.00

Estimate of population variance: ![2](/image/2.jpg)

Estimate of population standard deviation: ![3](/image/3.jpg)


The distribution of the values is presented in the histogram below:

![3card_draw](/image/draw3.jpg)


By comparison, its shape looks quite different from the original distribution for single draw. The original distribution is highly skewed because the value 10 has much larger probability of getting drawn than other values. However, for each three-card draw, the sum value is a result of a mix of small and large values with different probilities. The difference between three-card draws thus become smaller and more even.

The confidence interval at 90% confidence level is:

![4](/image/4.jpg)

Put the values of the descriptive statistics we calculated above and get:

The 90% confidence interval is [6.16, 28.10], which means we expect 90% of the future draw values will fall in this range.

To find the probability of getting a value at least 20,

![5](/image/5.jpg)

From z-table, the probability for draws to have a value at least 20 is about 0.3336.


# INTRODUCTION <br />
The Apriori algorithm can be considered the foundational algorithm in basket analysis. Basket analysis is the study of a client’s basket while shopping. <br />
The goal is to find combinations of products that are often bought together, which we call frequent itemsets. The technical term for the domain is Frequent Itemset Mining.

## Steps of the Apriori algorithm <br />

### Step 1. Computing the support for each individual item <br />
The algorithm is based on the notion of support. The support is simply the number of transactions in which a specific product (or combination of products) occurs. <br />

The first step of the algorithm is to compute the support of each individual item. This basically just comes down to counting, for each product, in how many transactions it occurs. <br />

![image](https://user-images.githubusercontent.com/98205162/198841556-52b8742b-fa1f-410a-b697-871303ff68b6.png)

### Step 2. Deciding on the support threshold <br />

Now that we have the support for each of the individual products, we will use that to filter out some of the products that are not frequent. To do so, we need to decide on a support threshold. For our current example, let’s use 7 as the minimum. <br />

### Step 3. Selecting the frequent items <br />

It’s easy to see that there are two individual products that have a support of less than 7 (meaning that they have less than 7 occurrences). Those products are Flour and Butter. <br />

So unfortunately for Flour and Butter, they will not be considered in further steps. <br />

### Step 4. Finding the support of the frequent itemsets <br />

The next step is to do the same analysis, but now using pairs of products instead of individual products. As you can imagine, the number of combinations can quickly become large here, especially if you have a large number of products. <br />

The great ‘invention’ behind the Apriori algorithm is that we will directly ignore all pairs that contain any of the non-frequent items. Thanks to this, we have a lot fewer item pairs to scan. <br />
 
Here is a list of all the pairs that contain either Butter, Flour, or both. All of those can be discarded and this will speed up the execution of our counts. <br />

![image](https://user-images.githubusercontent.com/98205162/198841542-5b9975d2-8ad5-49b3-9381-685da8772cb9.png)

Of course, there are still some combinations that do need to be counted in this example: <br />

![image](https://user-images.githubusercontent.com/98205162/198841529-370d1f2d-17c9-4855-ba6c-3298a361af16.png)

As you can see, at this point there are only two product combinations left that are above support: Wine and Cheese, and Beer and Potato Chips. <br />

### Step 5. Repeat for larger sets <br />

We will now repeat the same thing for the sets with three products. As before, we will not score sets that were eliminated in the previous step. <br />

The remaining pairs were: <br />
- Wine, Cheese
- Beer, Potato Chips <br />

So, what triplets can we make that do not contain any pair that was eliminated? <br />

- Wine, Cheese, Beer -> eliminated because of the presence of a non-frequent pair (for example Cheese, Beer)
- Wine, Cheese, Potato Chips -> eliminated because of the presence of a non-frequent pair (for example Cheese, Potato Chips)
- Beer, Potato Chips, Wine -> eliminated because of the presence of a non-frequent pair (for example Wine, Potato Chips)
- Cheese, Beer, Potato Chips -> eliminated because of the presence of a non-frequent pair (for example Cheese, Beer) <br />

There are no triplets that do not contain any non-frequent pair. This means that the frequent sets have been identified and they are the pairs Wine, Cheese and Beer, Potato Chips. <br />

### Step 6. Generate Association Rules and compute confidence <br />

Now that you have the largest frequent itemsets, the next step is to convert them into Association Rules. Association Rules go a step further than just listing products that occur together frequently. <br />

Association Rules are written in the format: Product X => Product Y. This means that you obtain a rule that tells you that if you buy product X, you are also likely to buy product Y. <br />

There is an additional measure called confidence. The confidence tells you a percentage of cases in which this rule is valid. 100% confidence means that this association always occurs; 50% for example means that the rule only holds 50% of the time. <br />

### Step 7. Compute lift <br />

Once you have obtained the rules, the last step is to compute the lift of each rule. According to the definition, the lift of a rule is a performance metric that indicates the strength of the association between the products in the rule. <br />

The formula of the lift of a rule is shown here: <br />
![image](https://user-images.githubusercontent.com/98205162/198841375-adcfbe60-896b-42dd-a6f7-6b4f1e0c7dd6.png)

This means that lift basically compares the improvement of an association rule against the overall dataset. If “any product => X” in 10% of the cases whereas “A => X” in 75% of the cases, the improvement would be of 75% / 10% = 7.5. <br />
If the lift of a rule is 1, then the products are independent of each other. Any rule that has a lift of 1 can be discarded. <br />
If the lift of a rule is higher than 1, the lift value tells you how strongly the righthand side product depends on the left-hand side.

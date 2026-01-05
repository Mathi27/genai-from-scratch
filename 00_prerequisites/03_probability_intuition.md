# Probability intuition (No Fluff)
Before we get to probabilities, we have to start with what the model actually outputs: Logits.

### The Raw Output (Logits)
Imagine our GenAI model is trying to complete the sentence: "The quick brown fox jumps over the..."

The final layer of the neural network assigns a raw score (logit) to every word in its vocabulary. These scores can be negative, positive, or zero. They are not probabilities yet—they are just "unnormalized confidence scores."
| Token | Logit (z) |
|------|-----------|
| dog  | 2.0       |
| lazy | 4.5       |
| pizza | -1.0     |
We use the Softmax function:

### Step 2: The Softmax Transformation

We need to turn these messy numbers into a nice probability distribution (where all numbers are between 0 and 1, and they sum to 1.0).

We use the Softmax function:
P(xᵢ) is equal to e raised to the power of xᵢ, divided by the sum of e raised to the power of xⱼ for all j.

Softmax turns scores into probabilities by dividing each exponential score by the total of all exponential scores.

Let's look at why we do this.

1.Positivity
2.Amplification

| Token  | Logit (z) | Exponent (e^z) | Probability (≈) |
|--------|-----------|---------------|------------------|
| dog    | 2.0       | 7.39          | 7.6%             |
| lazy   | 4.5       | 90.02         | 92.0%            |
| pizza  | -1.0      | 0.37          | 0.4%             |

Notice that "lazy" dominates the probability completely, even though its raw score wasn't that much higher than "dog".

To see if this concept clicks, let's look at the "Amplification" property again. In our example, "lazy" had a score of 4.5 and "dog" had 2.0.

If we just used the raw numbers linearly, $4.5$ is about double $2.0$. But after Softmax:
p(lazy) ~ 92%
p(dog) ~ 7.6%

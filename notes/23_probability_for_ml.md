# Probability for Machine Learning

## Why Learn Probability?

Machine Learning models often deal with uncertainty.

Instead of saying something **will** happen, they estimate **how likely** it is to happen.

Examples:

- Probability an email is spam
- Probability a customer will churn
- Probability a loan will default
- Probability an image contains a cat

Understanding probability helps us interpret ML model predictions.

---

# What is Probability?

Probability is a measure of how likely an event is to occur.

Its value always lies between:

0 and 1

or

0% and 100%

Where:

- 0 → Impossible event
- 1 → Certain event

Example:

Probability of the sun rising tomorrow ≈ 1

Probability of rolling a 7 on a standard six-sided die = 0

---

# Important Terms

## Experiment

An action that produces one or more possible outcomes.

Examples:

- Tossing a coin
- Rolling a die
- Drawing a card

---

## Outcome

A single possible result of an experiment.

Example:

Rolling a die

Possible outcomes:

1, 2, 3, 4, 5, 6

Rolling a 4 is one outcome.

---

## Sample Space

The set of all possible outcomes.

Example:

Rolling a die

Sample Space:

{1, 2, 3, 4, 5, 6}

---

## Event

An event is one or more outcomes of interest.

Example:

Getting an even number.

Event:

{2, 4, 6}

---

# Probability Formula

Probability = Number of Favorable Outcomes / Total Number of Possible Outcomes

Example:

Rolling an even number on a die.

Favorable outcomes:

{2, 4, 6}

Total outcomes:

6

Probability = 3 / 6 = 0.5

---

# Independent Events

Two events are independent if one event does not affect the other.

Example:

- Tossing a coin
- Rolling a die

The coin result does not change the die result.

---

# Dependent Events

Two events are dependent if one affects the other.

Example:

Drawing two cards from a deck without replacement.

The first card changes the remaining deck.

---

# Conditional Probability

Conditional probability is the probability of an event occurring given that another event has already occurred.

Example:

What is the probability that a student passes the exam given that they attended all classes?

The additional information changes the probability.

Conditional probability is important because many Machine Learning models make predictions using available information.

---

# Bayes' Theorem (Intuition)

Bayes' Theorem updates the probability of an event after observing new evidence.

Example:

A patient takes a medical test.

The initial probability of having a disease changes after seeing the test result.

This idea forms the foundation of the Naive Bayes algorithm, which we will study later.

---

# Probability in Machine Learning

Many ML models predict probabilities instead of directly predicting classes.

Example:

Spam Detection

Probability of Spam = 0.93

Since this probability is high, the email is classified as spam.

Similarly,

House Price Prediction estimates values with uncertainty,

and Classification models estimate class probabilities.

---

# Interview Questions

### What is probability?

A measure of how likely an event is to occur.

---

### What is the difference between an outcome and an event?

An outcome is a single result.

An event is one or more outcomes.

---

### What is conditional probability?

The probability of an event given that another event has already occurred.

---

### Why is probability important in Machine Learning?

Because many ML models estimate probabilities before making predictions.

---

# Summary

In this chapter, we learned:

- Probability
- Experiment
- Outcome
- Sample Space
- Event
- Probability Formula
- Independent Events
- Dependent Events
- Conditional Probability
- Bayes' Theorem (intuition)
- Applications of Probability in Machine Learning
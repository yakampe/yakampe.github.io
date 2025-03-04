---
layout: post
title:  "Cucumber and Gherkin"
date:   2025-03-03 19:00:00 +0000
categories: tdd
tags:
- BDD
- ATDD
- Code
image: '../assets/images/posts/bdd.webp'
image-alt: 'header image for bdd'
excerpt_separator: "<!--exc-->"
medium-link: 'https://medium.com/'
dev-to-link: 'https://dev.to/'
meta-description: 'Janis Yanis Kampe Blog: Cucumber and Gherkin, BDD, ATDD, Code'
---

Behaviour-Driven Development (BDD) offers a dynamic and collaborative approach to software development, and tools like Cucumber and Gherkin make it easier to bring this methodology to life. Rather than diving directly into complex coding tasks, BDD encourages teams to collaboratively define application behaviour in simple, human-readable language. By using Gherkin syntax to write clear, structured feature files, developers, testers, and business stakeholders can ensure they all share a common understanding of the product's functionality.  <!--exc-->  This approach provides a safe and enjoyable environment to experiment, learn, and prepare for the real challenges of building software, making it an effective and fun way to approach development. In this blog, we'll explore how Cucumber and Gherkin can help you improve collaboration, streamline development, and ensure your work is always in line with the desired outcomes.

## History of BDD

## Gherkin Examples

Here is an example:
{% highlight gherkin %}
Feature: Guess the word

  # The first example has two steps
  Scenario: Maker starts a game
    When the Maker starts a game
    Then the Maker waits for a Breaker to join

  # The second example has three steps
  Scenario: Breaker joins a game
    Given the Maker has started a game with the word "silky"
    When the Breaker joins the Maker's game
    Then the Breaker must guess a word with 5 characters
{% endhighlight %}

This one is equally interesting:

Here is an example:
{% highlight gherkin %}
Feature: Account Holder withdraws cash
 
Scenario: Account has sufficient funds
    Given The account balance is $100
      And the card is valid
      And the machine contains enough money
     When the Account Holder requests $20
     Then the ATM should dispense $20
      And the account balance should be $80
      And the card should be returned
{% endhighlight %}

## Importance of BDD

## Ways to deliberately practice software

### References

1. Reference 1
1. Reference 2
1. Reference 3
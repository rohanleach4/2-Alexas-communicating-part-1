# 2 Alexas communicating to each other part-1
This is from a series of experiments and tests I conducted 1 year ago. It is no longer maintained.

At the beginning of 2017, I spent some time with Alexa, looking at different ways of writing for her and testing the water for what may come.
One of these projects can be found on my failed YouTube channel, Alexa: Queen Bitch.
Further experiments, led me to get 2 Alexa’s to communicate with each other.
2 of these were quite successful in how they operated:

## Simple Maths

The first was getting 2 Alexa’s to give each other simple math sums.
Alexa number 1 would give it, the second answer it and provide a new sum.

## Chess

Same premise, except each Alexa has access to a node.js chess board and gives each other a move (it worked, but not being a chess player myself, I never knew whether they were playing … or just lying to each other).

### A year later, I no longer pursue voice as an active interest.

As such, I thought I would do some house-keeping and present some of my concepts.
These are no longer actively maintained, but should remain valid. I do believe there is value in having multiple voice devices interacting with people, I am just not sure of how you would implement it in a real-world situation.

Pre-requisites: I assume that you have an AWS account and you know how to set up a skill.
If you don’t, Amazon tutorials are probably the best place to go to learn this. Once you can do a simple example, it is a very small step to deliver more complex skills.

## Simple Maths concept and execution

### Disclaimer: This is a right ball-ache to set up. You need:

- 2 Alexa’s in close proximity (warning - they don’t like each other) 
- 2 AWS accounts set to two different email addresses and to make life easier, both open in different browsers, by two different vendors, ie Chrome and Firefox (yep - that is how you get it to work).
- Each Alexa has to have a different ‘wake word’, ie 'Alexa’ and ‘Computer’ (yep - that is how you get it to work).
- A similar skill will be published to each account. Each skill must have a different name, in this case the first will be Tilly, the second will be David.
- The first Alexa, will be given the invocation command of ‘open david’, so the first Alexa (Tilly) will actually initiate the other Alexa’s skill. David will then respond with the first sum (in this case 1+1) and they will cascade from that point on. 
  - This first part is where it gets fun. You use one Alexa to open another. This is the first step of creating a network of Alexa’s and was a jumping point for my concept on Non-Organic Stimuli.
  
The files in the repro are divided into the 2 Alexa skills. It should be just a question of pasting them into the associated accounts.

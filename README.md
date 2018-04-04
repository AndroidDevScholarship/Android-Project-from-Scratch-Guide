# Beginner's Guide to Build Project from Scratch

## Notes from the Authors
This document, created by **Student Leaders** in the _AND_ track, is a collection of general guidelines, useful for when we have to start building an Android Project from scratch. Please, note that these guidelines are not mandatory, but just suggestions, and are based on the Student Leaders’ experience. Everything in the document can be improved, and if you have any suggestion we **want** to hear it. 

What we are trying to face here is the moment when, after we’re asked to build an Android Project, we have to actually do it! This is an important moment, because here is where everything starts and where everything needs to be approached. It may seem all impossible to face, but keep in mind that every project is different, so you always have to follow the guidelines you’re given (if any). 

### Authors 
TODO: Update with the right GitHub names

Lauren Moineau (@Lauren_M), Henna Singh (@hennasingh04 ), Gregorio Palamà (@gregoriopalama ), Iva Ivanova (@fif.iva), Cristina Mangana (@cristina.mangana)

## Collect all Requirements
Every time you are about to build a new App from scratch, it is because someone asked for it, be it a simple prototype project or a big application. But that’s not all. When somebody asks for a new App, you’re given a full list of requirements. Usually, they are functional requirements, such as “my App should show a list of events” or “my App should notify me when something happens”, but requirements can also be technical. For example, we can receive the request to save some data locally in a database, or remotely, in a remote database, or we could be asked to use a remote API. 

Every request made to us becomes a requirement. These are the most important drivers for our work: we need to fulfill them in order to make the App work, to accomplish the goal of the whole App. So, since they are so important, the very first step we take is to **collect requirements, write them down on a list, and separate technical ones from functional ones**. More separations can be done, but it is important we have all the requirements on a list, ready to be taken care for.

## Ask Yourself a few Questions
### App structure
- Does my app need to be connected?
  * Internet
  * API
  * External database
  * Other app(s)

- How will I implement this connection?
  * 3rd party libraries?

- Is the app static or will it need updates? 
- If I need to store some data, where should I store it?
  * Locally
  * External DB

### UI/UX
- How many activities does the app need?
- Thinking about the data that needs to be displayed:
  * What is the data type? (text, pictures…)
  * How do I need to display that data? (list, grid…)
  * Do I need a RecyclerView?

## Before you start coding
### Plan Your App Structure
Make simple sketches for the Activities you will need. Just grab a pen and a paper and make very simple diagrams in order to create a visual map. It really helps to see it outside of your head without missing something in the process.

Roughly draw all the different views on each activity to help you visualize the information you will be dealing with, 1 box per piece of info. Draw the intents, explicit and implicit, if any. Put yourself in the shoes of both the developer and the user.

### Look for Inspiration
When you start building a new app, you want to first design how you want it to be: how many activities or fragments, how to display your information, etc. Sometimes, you need to look for ideas that inspire your creativity. You can find this on the Udacity Forums or Slack, looking at the other students approaches, or check some useful websites such as [Uplabs](https://www.uplabs.com/android) or [Dribble](https://dribbble.com/).

### Revisit Those Questions and Ask Yourself a Few More
**UI/UX:**
* Which layout(s) should I use?
* What navigation pattern am I going to follow? (Navigation guides users through the different parts of your app). How will the user navigate between/within the activities?
* Do I need fragments?

### Finalize Your App Structure
Go back to your original sketch and modify it so it contains all the info you’ve gathered so far. Include all the activities, fragments, different layouts, navigation, external/internal data storage, content providers, etc. It should remain clear, so use abbreviations or colours to keep it simple and help you visualise the final result, which will in return help you organise your code. 

This is not a mandatory step. In fact, sometime the project itself may be small and it will not require such a step. Other times, instead, you will find it better to go back and retouch things more than once. There is not just one right approach, so don’t think you are in the wrong if you find that your project doesn’t need any change. Also, you could find it easier to give the final touches at the very end of everything, so just experiment with your project and find the way that fits it the best.

### List all Tasks and Organize Yourself
Once you have the sketches done, divide them into small pieces and mark some milestones that have to be achieved to make your app work as planned (also don’t forget to meet specifications given in the rubric). Set yourself some partial deadlines and look how you progress! In addition, you can make some intermediate tests just to make sure you are achieving what you have proposed. Don't forget to run your app and check for any potential errors whenever you implement any new feature (like network calls, database connectivity etc).

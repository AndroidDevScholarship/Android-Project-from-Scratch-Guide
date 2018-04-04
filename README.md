# Beginner's Guide to Build Project from Scratch

## Notes from the Authors
This document, created by **Student Leaders** in the _AND_ track, is a collection of general guidelines, useful for when we have to start building an Android Project from scratch. Please, note that these guidelines are not mandatory, but just suggestions, and are based on the Student Leaders’ experience. Everything in the document can be improved, and if you have any suggestion we **want** to hear it. 

What we are trying to face here is the moment when, after we’re asked to build an Android Project, we have to actually do it! This is an important moment, because here is where everything starts and where everything needs to be approached. It may seem all impossible to face, but keep in mind that every project is different, so you always have to follow the guidelines you’re given (if any). 

### Authors 
TODO: Update with the right GitHub names

Lauren Moineau (@Lauren_M), Henna Singh ([@hennasingh](https://github.com/hennasingh)), Gregorio Palamà (@gregoriopalama ), Iva Ivanova (@fif.iva), Cristina Mangana (@cristina.mangana)

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

## Start Coding: Build the Structure of Your First Activity
>[**Activity**](https://developer.android.com/reference/android/app/Activity.html) - _The single focused thing that the user can do_.  - Developer Android Guide

Whether your App will display a List of Views or a complex Constraint Layout, it needs a simple structure. No need to focus too much on the details right now. Just a few Views that will display the result you’re going to achieve with the functionality. 

Design the first Activity by selecting your root layout with all needed nested Views. 

### Root Layout
* **[FrameLayout](https://developer.android.com/reference/android/widget/FrameLayout.html)** - great for simple layouts when the layout needs to hold a single Child View. You can, however, add multiple children to a FrameLayout and control their position by assigning gravity to each child
* **[LinearLayout](https://developer.android.com/reference/android/widget/LinearLayout.html)** - great for displaying Views horizontally or vertically one after another. It is also perfect for breaking up the display proportionally
* **[RelativeLayout](https://developer.android.com/reference/android/widget/RelativeLayout.html)** - great for positioning Views relative to each other 
* **[ConstraintLayout](https://developer.android.com/reference/android/support/constraint/ConstraintLayout.html)** - a bit more complicated, but has great features for building complex UIs with multiple Views that are positioned relative to the parent, or the sibling View.

### ListView | GridView | RecyclerView  
* **[ListView](https://developer.android.com/reference/android/widget/ListView.html)** - it allows to create just the vertical-scrolling list of elements. The list items are automatically inserted to the list using an Adapter that pulls content from a source such as an array or database query and converts each item result into a view that's placed into the list. To display a more custom view for each item in your dataset, implement a ListAdapter
  * [Tutorial](https://www.thedroidsonroids.com/blog/how-to-implement-a-listview)
* **[GridView](https://developer.android.com/reference/android/widget/GridView.html)** - is a ListView example for displaying the Views into a Grid. We use this again by setting up a ListAdapter to feed the views with data
  * [Tutorial](https://www.raywenderlich.com/127544/android-gridview-getting-started)
* **[RecyclerView](https://developer.android.com/reference/android/support/v7/widget/RecyclerView.html)** - can display a list of Views vertically, horizontally or into a grid. It’s more efficient by default, the layout is separated and they have more possibilities over the data set inside the adapter. The LayoutManager is responsible for layouting row views. For horizontal and vertical lists is more suitable the [LinearLayoutManager](https://developer.android.com/reference/android/support/v7/widget/LinearLayoutManager.html), for grids - the [GridLayoutManager](https://developer.android.com/reference/android/support/v7/widget/GridLayoutManager.html)
  * [Tutorial](https://www.thedroidsonroids.com/blog/how-to-implement-a-recyclerview)

## Build an Adapter to Display Data to the UI
### **[Adapter](https://developer.android.com/reference/android/widget/Adapter.html)**
 - Create a separate Adapter class that extends from `RecyclerView.Adapter` (for RV) or `ArrayAdapter` (LV) depending on the list views used for displaying data
### ListView
- Add a constructor initializing the context and the list of model object
- Override the `getView()` method in the class and inflate the layout created for the list item
- Populate the UI components (TextViews, ImageViews .. etc) with the data retrieved from the getter methods of the model class (POJO)
- [Tutorial](https://www.raywenderlich.com/124438/android-listview-tutorial)
### RecyclerView
- Add a constructor initializing the context, any listeners and the list of model object
- Create an inner or separate `ViewHolder` class that gets the references of the UI components
- Override 3 methods in the Adapter class
  - `onCreateViewHolder()` - inflate the list item view here
  - `onBindViewHolder()` - bind the data to UI components here
  - `getItemCount()` - return the list size here
- [Tutorial](http://www.vogella.com/tutorials/AndroidRecyclerView/article.html)

## Optional
---

## Work with the API
- Get yourself familiar with the API you’re going to use for your app (read the documentation)
- Try some query urls directly into the browser, and “translate” the answer into a readable JSON format ([jsonformatter](https://jsonformatter.curiousconcept.com/), [jsonprint](http://jsonprettyprint.com/)) to know in what manner your app is going to receive the data (if there are Arrays, Objects, Strings, etc.) 
- Decide how many endpoints you will have to call for your queries 

## Make Calls to the API
- Add Internet permissions
 ``` xml 
<uses-permission android:name="android.permission.INTERNET" /> 
```

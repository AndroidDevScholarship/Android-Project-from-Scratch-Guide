# Beginner's Guide to Build Project from Scratch

## Table of Content
- [**Notes from the Authors**](https://github.com/AndroidDevScholarship/Project-from-Scratch-Guide#notes-from-the-authors)
- [**Collect all Requirements**](https://github.com/AndroidDevScholarship/Project-from-Scratch-Guide#collect-all-requirements)
- [**Ask Yourself a few Questions**](https://github.com/AndroidDevScholarship/Project-from-Scratch-Guide#ask-yourself-a-few-questions)
  - [App structure](https://github.com/AndroidDevScholarship/Project-from-Scratch-Guide#app-structure)
  - [UI/UX](https://github.com/AndroidDevScholarship/Project-from-Scratch-Guide#uiux)
- [**Before you start coding**](https://github.com/AndroidDevScholarship/Project-from-Scratch-Guide#before-you-start-coding)
  - [Plan Your App Structure](https://github.com/AndroidDevScholarship/Project-from-Scratch-Guide#plan-your-app-structure)
  - [Look for Inspiration](https://github.com/AndroidDevScholarship/Project-from-Scratch-Guide#look-for-inspiration)
  - [Revisit Those Questions and Ask Yourself a Few More](https://github.com/AndroidDevScholarship/Project-from-Scratch-Guide#revisit-those-questions-and-ask-yourself-a-few-more)
  - [Finalize Your App Structure](https://github.com/AndroidDevScholarship/Project-from-Scratch-Guide#finalize-your-app-structure)
  - [List all Tasks and Organize Yourself](https://github.com/AndroidDevScholarship/Project-from-Scratch-Guide#list-all-tasks-and-organize-yourself)
- [**Start Coding: Build the Structure of Your First Activity**](https://github.com/AndroidDevScholarship/Project-from-Scratch-Guide#start-coding-build-the-structure-of-your-first-activity)
  - [Root Layout](https://github.com/AndroidDevScholarship/Project-from-Scratch-Guide#root-layout)
  - [ListView | GridView | RecyclerView](https://github.com/AndroidDevScholarship/Project-from-Scratch-Guide#listview--gridview--recyclerview)
- [**Build an Adapter to Display Data to the UI**](https://github.com/AndroidDevScholarship/Project-from-Scratch-Guide#build-an-adapter-to-display-data-to-the-ui)
  - [Adapter](https://github.com/AndroidDevScholarship/Project-from-Scratch-Guide#adapter)
  - [ListView](https://github.com/AndroidDevScholarship/Project-from-Scratch-Guide#listview)
  - [RecyclerView](https://github.com/AndroidDevScholarship/Project-from-Scratch-Guide#recyclerview)
- [**Work with the API**](https://github.com/AndroidDevScholarship/Project-from-Scratch-Guide#work-with-the-api)
- [**Make Calls to the API**](https://github.com/AndroidDevScholarship/Project-from-Scratch-Guide#make-calls-to-the-api)
  - [Make Network Calls without a Library](https://github.com/AndroidDevScholarship/Project-from-Scratch-Guide#make-network-calls-without-a-library)
  - [Use a 3rd party library](https://github.com/AndroidDevScholarship/Project-from-Scratch-Guide#use-a-3rd-party-library)
- [**Perform Network Requests Asynchronously**](https://github.com/AndroidDevScholarship/Project-from-Scratch-Guide#perform-network-requests-asynchronously)
  - [AsyncTask](https://github.com/AndroidDevScholarship/Project-from-Scratch-Guide#asynctaskparams-progress-result)
  - [AsyncTaskLoader](https://github.com/AndroidDevScholarship/Project-from-Scratch-Guide#AsyncTaskLoader-d)
- [**Build Models for Your Data**](https://github.com/AndroidDevScholarship/Project-from-Scratch-Guide#build-models-for-your-data)


## Notes from the Authors
This document, created by **Student Leaders** in the _AND_ track, is a collection of general guidelines, useful for when we have to start building an Android Project from scratch. Please, note that these guidelines are not mandatory, but just suggestions, and are based on the Student Leaders’ experience. Everything in the document can be improved, and if you have any suggestion we **want** to hear it. 

What we are trying to face here is the moment when, after we’re asked to build an Android Project, we have to actually do it! This is an important moment, because here is where everything starts and where everything needs to be approached. It may seem all impossible to face, but keep in mind that every project is different, so you always have to follow the guidelines you’re given (if any). 

### Authors 
Lauren Moineau ([@ellemwano](https://github.com/ellemwano)), Henna Singh ([@hennasingh](https://github.com/hennasingh)), Gregorio Palamà ([@gregoriopalama](https://github.com/gregoriopalama)), Iva Ivanova ([@fireflyfif](https://github.com/fireflyfif)), Cristina Mangana ([@cristina-mangana](https://github.com/cristina-mangana))

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

---
## Optional
## Work with the API
- Get yourself familiar with the API you’re going to use for your app (read the documentation)
- Try some query urls directly into the browser, and “translate” the answer into a readable JSON format ([jsonformatter](https://jsonformatter.curiousconcept.com/), [jsonprint](http://jsonprettyprint.com/)) to know in what manner your app is going to receive the data (if there are Arrays, Objects, Strings, etc.) 
- Decide how many endpoints you will have to call for your queries 

## Make Calls to the API
- Add Internet permissions
 ``` xml 
<uses-permission android:name="android.permission.INTERNET" /> 
```

### Make Network Calls without a Library
- Build URL and make Network calls as done in the course exercises:
  - **Network calls** (build URL, etc): 
  - From the url, open an http connection 
  - Get an Input Stream from the opened connection
  - Read the contents of the Input Stream (scanner). This allocates and deallocates the buffers as needed and handles character encoding. The data delivered from the request url is in JSON format.
  - Extract data from the JSON

### Use a 3rd party library. 
Which library should I use?	
- [Comparison of a few libraries](https://stackoverflow.com/questions/16902716/comparison-of-android-networking-libraries-okhttp-retrofit-and-volley/18863395#18863395) - [Retrofit](http://square.github.io/retrofit/), [OkHttp](http://square.github.io/okhttp/), [Volley](https://developer.android.com/training/volley/index.html), any other preference
![Library Comparison](https://github.com/AndroidDevScholarship/Project-from-Scratch-Guide/blob/master/3u6s6.png)
- Add needed Gradle dependencies for libraries and JSON converters if any
- Check how to perform a request on a background thread
- Check for successful connection or failures, put any needed information in a toast or dialog to display to the user.
- Create model java objects (POJO) for mapping the received data
- Check for null values and set data to the custom adapters created, and then add data to the UI from the adapters as needed

## Perform Network Requests Asynchronously 
_In case you're not using any 3rd parties Libraries_ 

A network request can take a few seconds to complete so are considered long-running operations. When executed on the main (UI) thread (**synchronous request**), this would "freeze" the screen until the process is finished. You will have a very unhappy user.

To prevent this bad user experience, a `NetworkOnMainThreadException` (making the app crash) is automatically generated whenever a Network call is attempted on the UI thread.
Also, when the UI thread of the app is blocked for at least 5 sec, an _Application Not Responding_ (ANR) error is triggered. 

All of this is designed to force you to perform an **Asynchronous Network Request**, on a background thread which on completion will display results to UI.

This can be done using an [`AsyncTask`](https://developer.android.com/reference/android/os/AsyncTask.html) or an [`AsyncTaskLoader`](https://developer.android.com/reference/android/content/AsyncTaskLoader.html). You can also take a look at this [link](https://nayaneshguptetechstuff.wordpress.com/2014/06/21/asynctask-vs-loaders-why-loaders-are-introduced/) (one of many) that describes the advantages of one over the another. Based on the use-case of your app, you can decide which one is the best to use.

### `AsyncTask<Params, Progress, Result>` 
_e.g._  `AsyncTask <String, Void, String>`
It is best used for short and interruptible tasks, tasks that don't need to report back to UI or user or low-priority tasks that can be left unfinished. 

**There are 4 basic steps**:
   - [`onPreExecute()`](https://developer.android.com/reference/android/os/AsyncTask.html#onPreExecute()) - is invoked on the UI thread before the Task is executed
   - [`doInBackground(Params...)`](https://developer.android.com/reference/android/os/AsyncTask.html#doInBackground(Params...)) - is executed  immediately after `onPreExecute()` finishes. This step performs a background computation (like fetching JSON data from API), returns a result, and passes the result to `onPostExecute()`.
   - [`onProgressUpdate(Progress...)`](https://developer.android.com/reference/android/os/AsyncTask.html#onProgressUpdate(Progress...)) - (optional) to report any form of progress to the UI thread while the background process is executing. 
   - [`onPostExecute(Result)`](https://developer.android.com/reference/android/os/AsyncTask.html#onPostExecute(Result)) - is run on the UI thread after the background computation is finished.

   The above methods are defined in a subclass of `AsyncTask`. To execute the task, you instantiate the class on the UI thread and call `execute()` on the instance, passing in the corresponding `Params/Progress/Result` parameters. 

### `AsyncTaskLoader<D>`  
_e.g._ `AsyncTaskLoader<ArrayList<Car>>`
It is a _subclass of the Loader framework_, using an `AsyncTask` to do the request on a background thread.

  With [Loaders](https://developer.android.com/guide/components/loaders.html), the data is preserved following device configuration changes and when the activity is permanently destroyed, the Loader is destroyed with it, with no remaining tasks consuming system resources (as opposed to `AsyncTask`).

  The [LoaderManager](https://developer.android.com/reference/android/support/v4/app/LoaderManager.html) class is used to manage one or more Loader instances within an activity or fragment. In an activity’s `onCreate` method, you initialize a loader and make it active by calling `getSupportLoaderManager()`, when using the Support Library:
  ``` 
  getSupportLoaderManager().initLoader(int id, Bundle args, LoaderCallbacks<D> callback)
```

-  **A Loader takes in 3 parameters:**
   - A unique loader ID
   - Optional arguments to supply to the loader at construction, in form of a `Bundle`.
   - A `LoaderCallbacks` implementation, which the `LoaderManager` calls to report loader events. When the local class implements the [`LoaderManager.LoaderCallbacks`](https://developer.android.com/reference/android/support/v4/app/LoaderManager.LoaderCallbacks.html) interface, it passes a reference to itself: `this`.

- The **`LoaderCallbacks` implementation** requires to override 3 methods:
   - [`onCreateLoader(int id, Bundle args)`](https://developer.android.com/reference/android/support/v4/app/LoaderManager.LoaderCallbacks.html#onCreateLoader(int,%20android.os.Bundle)) - where you implement the code to instantiate and return a new loader with the given ID, ready to start loading.
  - [`onLoadFinished(Loader<D>, D data)`](https://developer.android.com/reference/android/support/v4/app/LoaderManager.LoaderCallbacks.html#onLoadFinished(android.support.v4.content.Loader%3CD%3E,%20D)) - where the data is moved to UI. 
  - [`onLoaderReset(Loader<D> loader)`](https://developer.android.com/reference/android/support/v4/app/LoaderManager.LoaderCallbacks.html#onLoaderReset(android.support.v4.content.Loader%3CD%3E)) - where you reset a previously created loader and invalidate its data.

- To **create a subclass of `AsyncTaskLoader`**, you need to:
  - Set a class that **`extends AsyncTaskLoader<D>`**, where D is the data type of the data you are loading
  - Override the `loadInBackground()` method with D as a return type. (This method is similar to the `doInBackground()` method of the `AsyncTask`.) The results are automatically passed on to the `onLoadFinished()` callback.

## Build Models for Your Data 
_Create Custom Classes for your Custom Objects_
_(used for data from API and for internal data)_

Custom Java Classes are critical to every object-oriented program you will build going forward. It is vital to be able to think about how to design objects that interact with each other and model real-world concepts. A Plain Old Java Object (POJO) is a class that holds data for an item like name and other details. In each Model Class there are member variables and mainly three methods:

- **Variables** - create variables as needed to define the object and set data to adapters and the UI
- **Constructor** - every java object has a Constructor, if not Java assigns an empty one. The constructor is the connection between the Adapter and the model
- **Getters** - methods for getting data of any property
- **Setters** - methods for setting data of any property

There are ways of automatically generating model classes from JSON responses like:
- [Json Schema](http://www.jsonschema2pojo.org/)
- [Pojo Library](http://pojo.sodhanalibrary.com/)

---
layout: essay
type: essay
title: "Designing A Path For Software Engineers"
# All dates must be YYYY-MM-DD format!
date: 2024-04-25
published: true
labels:
  - Design Patterns
---
## A Solution To Repetition

You've probably run into many problems that involve having to do the same thing over and over again as you are writing your code. For a software engineer, that is completely normal. We encounter repetition all the time, but we don’t want to rewrite the same thing all the time. That gets tedious and very inefficient. Thankfully, previous software engineers have found solutions to these problems.

For some problems, when you create the algorithm, you check the same element multiple times and it is always the same. If you just check it once it’ll be more efficient. That’s where dynamic programming comes in. Got a bunch of functions that look similar, well functional programming can help.

What about designing your application? Well the answer to that is design patterns.

## What Are Design Patterns

If you’re thinking, “what is a design pattern,” don’t worry, you’re just like me. I didn’t know what it was either when I first heard of this. It sounds like something you’d hear fashion designers talking about, or at least that’s what I thought. In software development, design patterns help to optimize your code and probably make it easier to read. 

## Design Patterns I Have Used

I never really noticed but I actually have been using design patterns. At the time of writing this, I am working on a project, alongside other software engineers, that implements the use of some design patterns. There are a lot of different design patterns but for now, I’ll only mention some of the ones I’ve been using.

### Singleton

One of the design patterns that I have been using is the singleton pattern. This is probably one of the more commonly used design patterns. This pattern is very useful as it allows you to instantiate a class only once and use it globally. This is very useful for the collections we are using since we wouldn’t want multiple instances of a collection. That would cause some problems.

Here is some code that we are using in our project:
```
class ExercisesCollection {
 constructor() {
   // The name of this collection.
   this.name = 'ExercisesCollection';
   // Define the Mongo collection.
   this.collection = new Mongo.Collection(this.name);
   // Define the structure of each document in the collection.
   this.schema = new SimpleSchema({
     name: String,
     description: String,
     category: {
       type: String,
       allowedValues: ['Cardio', 'Strength', 'Flexibility', 'Hypertrophy'],
     },
     difficulty: {
       type: String,
       allowedValues: ['Beginner', 'Intermediate', 'Advanced'],
     },
   });
   // Attach the schema to the collection, so all attempts to insert a document are checked against schema.
   this.collection.attachSchema(this.schema);
 }
}
/**
* The singleton instance of the ExercisesCollection.
* @type {ExercisesCollection}
*/
export const Exercises = new ExercisesCollection();



```
As you can see, we have a class to create a collection for different exercises. At the very bottom we export this as a new class called Exercises and with this we can use this collection globally throughout our project.

### Observers

Another commonly used design pattern is the observer pattern. This allows for objects that are observed to update for all observers whenever something happens to that object. We accomplish this by using publish and subscribe methods.

```
Meteor.publish(Profiles.userPublicationName, function () {
 if (this.userId) {
   const username = Meteor.users.findOne(this.userId).username;
   return Profiles.collection.find({ username: username });
 }
 return this.ready();
});
```
Here we used a publish method for a collection of profiles to be our observable object.

```
// useTracker connects Meteor data to React components. https://guide.meteor.com/react.html#using-withTracker
const { doc, ready } = useTracker(() => {
 // Get access to Stuff documents.
 const subscription = Meteor.subscribe(Profiles.userPublicationName);
 // Determine if the subscription is ready
 const rdy = subscription.ready();
 // Get the document
 const document = Profiles.collection.findOne(_id);
 return {
   doc: document,
   ready: rdy,
 };
}, [_id]);
```
Here we use a subscribe method to observe the profiles collection for one of our pages.

## Becoming a Better Software Engineer

Design patterns are an important part of becoming a great software engineer. It’s probably more important to learn than coding standards since it’s useful for efficiency. But don’t ignore the coding standard. They are both important things to have as a software engineer..There are quite a bit of different design patterns to learn but understanding them will help you and your fellow engineers in creating a fully functional application.


## References

ChatGPT was used for research.

https://www.patterns.dev/

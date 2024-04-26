# Domain and ORM, authorizations

## Skills

- Domain and ORM 
  - Implementation of a complex domain model (DSLearn project) 
  - Seeding of a domain model with SQL 
- Authorizations
  - Custom service-level authorization 
  - Customized content for the logged-in user 
  - Refresh token 
  - Pre-authorization of methods

## DSLearn project complex domain

![Figma](https://github.com/SofiaMFonseca/assets/blob/main/dslearn/conceptual-model-dslearn.png)

The system consists of a teaching platform that maintains information about courses, their classes and students, as well as a forum for questions and answers about course content. The actors in the system can be students and teachers. There are also admin users, who are the only ones authorized to register courses and classes.

A course is made up of several "resources," which are groups of content. These resources can be learning tracks, bonuses, external links, and the course's own Q&A forum. Each resource can contain sections, and these sections in turn will contain the lessons, which can be video and/or text content, or assignments to be handed in by students.

An assignment can have a weight, a due date, a number of questions, and the minimum number of correct answers needed to be accepted. When a student turns in the assignment, it waits for feedback from the teacher, and it can be accepted or rejected.

Each new class of the course corresponds to an offer or edition of this course, which has a start and end date. Different offerings of the same course may have slight variations in content, depending on the need for customization for each class.

Users (students and teachers) should receive notifications.

With respect to the Q&A forum, it consists of a collection of topics (with a title and description of the question), and each topic can have multiple answers. The general requirements of the forum are:

- List topics, with the following filter options: 
  - By resource/section/lesson 
  - By text (title and/or topic body) 
  - Questions asked only by the logged-in user 
- Create topic: title, body 
- Reply topic 
- Mark/uncheck upvote on question (cannot be the author) 
- Mark/uncheck upvote in response (cannot be the author) 
- Mark/deselect best answer (topic author only and instructor)

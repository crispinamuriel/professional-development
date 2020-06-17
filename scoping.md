# Scoping

## Philosophy

In Sprint Planning, engineers should use points to estimate the complexity of the stories/tasks in the upcoming sprint.
By asking individual engineers to think about complexity, we will put ourselves in the best position to understand as much as we can about the technical solutions we are planning to implement.

## Implementation

- We’ll use the Fibonacci sequence: 1, 2, 3, 5, 8, 13, 21, 40
- We shouldn’t start work on a story at 13, 21, or 40. We don’t know enough about it to get started. Or it can be split into smaller tasks.
- If the task is research-focused to inform the right product decision, time box the research instead (i.e. 1/2 day or 1 day)

## Process

**Option 1**: Engineers, keep a notepad open! As we discuss each task, write down your score for it.
Once we have gone through all the tasks for the sprint, we’ll go back through the task list one at a time and ask everyone to share their point values.

**Option 2**: After each task, the tech lead counts down from 3 and everyone holds up fingers to share their point values.

- If everyone picks the same value, assign it and move on.
- If there’s a split of 2s and 3s, go with the 3. Move on.
- If everyone picks a 3 except one person who picks an 8, this is either easier or more difficult than expected. Let’s talk about it to figure out where the delta exists. Then re-point.
- Make sure everyone is heard, but do not be afraid to pick the wrong number and move on. The tech lead should make the call.

## Guidelines

- **1**: the smallest unit of coding work you can imagine (changing one line of code and deploying it).
- **2** or **3**: a small improvement that’s based on some code you’re generally familiar with (updating a new component to a page, creating a new page following a template, modifies existing state)
- **5** or **8**: a new feature with something you might need to research options for, or maybe a complex refactor
- **13**: something complex enough where it should be broken down into smaller tasks which would be easier to scope - maybe it touches or impacts multiple code repos, or it’s comprised of frontend and backend work in the 2/3 or 5/8 range
- **21**/**40**: an assignment that has so many unknowns that it’s almost meaningless to give an estimate.

## Example: Implement a login page

- **40**: Implement a new web app to let constituents log in to update their mailing list settings
- **13**: Implement Vuex store to maintain login state / JWT across multiple pages
- **8**: Add a reset password form. The Authentication API provides endpoints for this experience. Follow the same design as the login form.
- **5**: Implement a front-end Vue form that stores username, password, and can POST to a server when the submit button is clicked.
- **3**: Show a new static component if the user enters incorrect information multiple times. There are different designs attached for mobile and desktop.
- **2**: Remove leading/trailing whitespace before POSTing to the authentication service. We’re seeing a lot of failed login attempts where the user types a space after their email address.
- **1**: Change the error message from “ERROR: username” to “Sorry, we couldn’t find your account in our system.”

## Closing thoughts

The most valuable outcome is a general consensus - whether or not a discussion is sparked to reach it.
A general consensus is good - the team has relatively high confidence in their estimate.
An outlier or split in votes is also good - this should spark a discussion which helps clarify the complexity of the ask.

If you score something high, but everyone who goes before you says a lower number, don’t be tempted to go along with the majority. You might know something that will dramatically impact the outcome of this work - please share it! (This is why we scope and share at separate times)

An engineer who is more experienced with a problem will probably take less time to complete a task. This is OK. This is why if the scores are close, we should just pick the highest. This also introduces opportunities for the more experienced person to say “you can follow the pattern here” or “we can pair on this if you’re interested in how I’m going to implement it”.

We are not tracking individual velocity as a measure of individual performance. Github doesn’t even allow us to do it in any logical way. The value here is getting the tasks scoped correctly, not perceived individual performance.

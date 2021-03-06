# Weekend Challenge 11 - React-Redux Feedback Form

## Instructions

Reviewing code is an important role developers play. We're going to practice reviewing code from others.

- Get the repo url from your partner
- Get your partner's project running on your computer
- Review the code from your partner and give relevant feedback
- Complete the Markdown section and submit that in the notes section on the assignment app. (Make sure you include who's code you reviewed.)

Practicing compassionate code reviews is important (you can learn more from this video on the topic: https://www.youtube.com/watch?v=Ea8EiIPZvh0 )

## Review Checklist

## Base Required Features

- Multi-Part Form:

  - [x] Able to add feedback
    - [x] Data collected on individual pages & components
    - [x] Click on next takes you to the next page in sequence
    - [x] Data saves in DB after _all_ the parts are completed (not piecemeal)
    - [ ] Thank you page takes you back to the first view
    - [ ] Old Data is cleared on form completion

- Client code:

  - [x] Individual components for each form part
  - [x] Redux setup complete
    - [x] Store linked to react with `<Provider>`
    - [x] Store setup with reducer(s) and logger middleware
  - [x] Reducers & Actions Working
    - [x] Actions are in SCREAMING_SNAKE_CASE and semantically named
    - [x] Actions have a `type` key, and `payload` if sending data
    - [x] Reducers are returning a new state, or the old state (not mutating)
    - [x] Reducers are using spread correctly (to keep old data, while adding new)
  - [x] Review Component shows at all times with current redux state
  - [ ] React-Redux Working
    - [ ] `connect`ing components correctly & dispatching Actions onClick
    - [ ] `mapStateToProps` when data is needed from Redux for submission
  - [x] Axios POST request to add feedback

- Server code:
  - [x] Router made for GET, POST

## General Items

Feedback should be provided for these items, but they do not impact scoring.

- Git
  - [x] Multiple git commits showing incremental progress
  - [x] Commits are descriptive of the changes made or feature added
  - [x] Has .gitignore with node_modules
  - [x] Readme file updated (assuming this is previously discussed)
- Code Style
  - [ ] Appropriate amount of code comments
  - [x] Code is consistently formatted
- Client
  - [x] Appropriate use of HTML tags
  - [x] Basic CSS styling with margins/padding

## Stretch Goals

First must be complete for score of _5 - Exceeds Expectations_

- Previous Steps

  - [x] allows a user to go to a previous step, either directly or by cycling backward thru the steps
  - [x] user can upate their score for a step
    - [x] new score is validated to not be empty
    - [x] redux is updated with new score
  - [x] user can continue on to review page and submit as in Base Mode

- Admin View

  - [x] All entries are visible with correct data from inputs
    - [ ] Most recent is at the top
  - [x] Can Delete an entry
    - [ ] User is prompted before deleting
  - [x] Axios GET request to get all feedback for `/admin` view in componentDidMount

  Busywork Goals, consider removing or making more useful

- [x] Styling with Material UI
- [ ] Ability to flag a feedback item on `/admin` for further review
- [ ] Deployed to Heroku

## Markdown

```
Hey John,

General Feedback.

---
| Functional Requirements | Complete? |
| --- | :---: |
| Multi page form with client side routing and navigation (next button) | yes |
| Data stored in Redux when navigating from page to page | yes |
| User is notified when trying to leave a blank score | yes |
| Review Component displays scores and comments from current redux state | yes |
| Submit button sends data to the server via Axios | yes |
| Confirmaion Page displays after data is POSTed to the server | no |
| Button on Confirmation Page clears Redux and starts a new survey | no |
| Views are broken down into components | yes |

---
### Notes:

Great work!  I like your approach to setting up the project and how you are storing the feedback responses in your reducer.  A couple of things that I noticed:
1. There was no confirmation page
2. Old scores were not cleared out when restarting the survey.  (I liked that you figured out how to pull in the original score when going back to edit, that is no small feat.)
3. When going back to edit, any score after the edit needed to be input for a second time.  From a user perspective, this could be frustrating.  Likely you would have had this cleared up with pulling in the previously submitted values.

---
| General Items | Complete? |
| --- | :---: |
| More than 15 git commits | yes |
| Commits are descriptive of the changes made or feature added | yes |
| Readme file updated | yes |
| Appropriate amount of code comments | no |
| Code is consistently formatted | yes |
| Server code organized with router & module files | yes |

---
### Notes:

FormPageOne had some awesome notes on it.  It felt like the notes became less descriptive (and present) the further down the page list.  One thing I found helpful was to copy and past notes from page to page as each page was basically set up the same.

Nice job with the admin page.  That table is looking good and you got to Material UI as well which is fantastic.

Keep up the great work!

```

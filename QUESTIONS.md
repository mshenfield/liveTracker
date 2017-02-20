# Questions
* What node versions does this support? e.g. Node >= 4
* What MongoDB versions does this support? This probably depends on the your version of [mongoose](http://mongoosejs.com/).
* What browsers does your application support, and why?
* What did you think about working with Angular's dependency injection system?

# Bugs
- [ ] Refreshing the home page if not logged in gives a 404. Steps to reproduce: Go to https://live-tracker.herokuapp.com. After page loads, refresh the page. You should see the message `{"error":{"status":404,"message":"Not Found"}}`
- [ ] Zip code validation allows zip codes like "123123123123123"
- [ ] Update https://github.com/embryCODE/portfolio12\_capstone to https://github.com/embryCODE/liveTracker in package.json
- [ ] "Logout" link in the upper nav shouldn't be included on the home page, since the user isn't logged in yet.
- [ ] Add instructions to add http://localhost:3000/auth/callback to Spotify Redirect URIs when setting up your Spotify App.

# Challenges
## Fullstack
- [ ] Add a user email sign-up so you don't have to authorize with Spotify each time they "Log out". Instead they can just log-in w/ their email and password.
- [ ] Handle paging from the JamBase API for Events. You'll only get back a portion of results if there are more than the page of events for a single artist near a zip code.

## Backend
- [ ] Replace your .gitignore with the [Github Node.gitignore](https://github.com/github/gitignore/blob/master/Node.gitignore) and then add your custom content to the end.
- [ ] Add rate limiting middleware to prevent people from spamming things like POST /users.
- [ ] Move anything not required to run your application from "dependencies" to "devDependencies" in package.json, e.g. `debug`.

## Frontend
- [ ] Let users know what to expect when they click the "Big Shiny Button" (Spotify authorization, then they can see if there are any concerts near them.). "Connect with Spotify" might be the best way to do this.
- [ ] Add a loading indicator when you are waiting for the JamBase API call to complete.
- [ ] In [login.html](http://github.com/embryCODE/liveTracker/blob/07ce5fbc36d94f75458907ce7e3472cf8618e08b/client/views/login.html#L10) don't need `target="_self"`, that is the default
- [ ] Instead of selecting a single artist, default to display all concerts coming up from any artists on the list, ordered by show date descending.
  - [ ] Add a filter using Angular that auto-completes with their top 20 artists, and a "Clear Filter"
  - [ ] Have a separate custom search and a "Show My Artists". "Show My Artists" should only be clickable if a custom search has been executed.
- [ ] Use images from the [Spotify `get-artist` API call](https://developer.spotify.com/web-api/get-artist/) in the page instead of the static image when showing artist shows.

## Collaboration
- [ ] Note that you can also use environment variables to set various configuration using the [`export`](http://stackoverflow.com/questions/1158091/defining-a-variable-with-or-without-export#answer-1158231) function, including `PORT`, `SPOTIFY_CLIENT_ID`, `SPOTIFY_CLIENT_SECRET`, `JAMBASE_API_KEY`
- [ ] Link directly to where I can create an API key with Spotify and JamBase.
- [ ] Add Markdown links for external tools and sites like "Spotify" and "JamBase", or "MongoDB"

## Markdown
- [ ] Use the Markdown blockquote for the Treehouse quote in "Project Instructions.
- [ ] Convert all the raw links in the README to use a Markdown link. \[text\]\(myurl.com\)

# Good Stuff
* Working code - it has a happy path where everything works, that is the most important thing.
* Comments. I don't look at express apps every day, so it was really nice to see what you were thinking, especially the 404 and error handlers in [index.js](https://github.com/embryCODE/liveTracker/blob/master/server/index.js)
* Using env variables for configuration. In line with best practices.
* Organization - project was organized in an intuitive way.

# I Learned
I don't work on many JS projects, so I learned quite a bit from you.

* [standard](https://github.com/feross/standard) - wasn't sure what the "standard" key in package.json was and found out about the linter. Seems solid.
* Using "engines" in package.json to figure out what Node version this is compatible with.
* How to setup a Spotify API account and redirect using express
* A little bit of mongoose.

# Unit 9: On the Fly, Part 4

## Step 1

- Instruction says to change the Build Command in Render to `:`, but it should be set to `npm install` so that Render can install the modules. Otherwise, `Error: Cannot find module 'dotenv/config'` wil be thrown.

## Step 3

- Instructions include changing the authorization callback URL to be the URL of the server, but this is not an option in the GitHub OAuth settings for the application.

## Other

Once deployed, logging in kept failing and wouldn't move past the login screen. Upon inspection, the failure was due to the cookie received without the configuration that allowed the OAuth to work. Added the following to `server.js` to allow log in:

```
app.set("trust proxy", 1);
app.use(
  session({
    secret: "codepath",
    resave: false,
    saveUninitialized: true,
    cookie: {
      sameSite: "none",
      secure: true,
    },
  }),
);
```

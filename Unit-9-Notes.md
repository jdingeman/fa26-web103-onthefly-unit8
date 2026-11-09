# Unit 9: On the Fly, Part 4

## Step 1

- Instruction says to change the Build Command in Render to `:`, but it should be set to `npm install` so that Render can install the modules. Otherwise, `Error: Cannot find module 'dotenv/config'` wil be thrown.

# Unit 8: On The Fly, Part 3 - Authentication

## Step 0

- `server/config/database.js` should have `ssl: { rejectUnauthorized: false }`
- Provided `reset.js` doesn't properly reset the database and drop the tables. Data will just keep stacking into the table, resulting in duplicates displayed on the destinations page.

## Step 3

- The copy excerpt for `router.get('/logout...` uses 'err' in the parameters and if statement but the return uses 'error' (minor)
- The file should be `Login.jsx` rather than `Login.js`

## Step 4

- Instructions don't explicitly indicate that `user` must be passed as a prop to the components, so `App.jsx` won't already include `user={user}` as part of the passed props.

## Step 7

- File should be `Avatar.jsx` instead of `Avatar.js`

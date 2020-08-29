This project was bootstrapped with [Create React App](https://github.com/facebook/create-react-app).

## Available Scripts

In the project directory, you can run:

### `yarn start`

Runs the app in the development mode.<br />
Open [http://localhost:3000](http://localhost:3000) to view it in the browser.

The page will reload if you make edits.<br />
You will also see any lint errors in the console.

### `yarn test`

Launches the test runner in the interactive watch mode.<br />
See the section about [running tests](https://facebook.github.io/create-react-app/docs/running-tests) for more information.

### `yarn build`

Builds the app for production to the `build` folder.<br />
It correctly bundles React in production mode and optimizes the build for the best performance.

The build is minified and the filenames include the hashes.<br />
Your app is ready to be deployed!

See the section about [deployment](https://facebook.github.io/create-react-app/docs/deployment) for more information.

### `yarn eject`

**Note: this is a one-way operation. Once you `eject`, you can’t go back!**

If you aren’t satisfied with the build tool and configuration choices, you can `eject` at any time. This command will remove the single build dependency from your project.

Instead, it will copy all the configuration files and the transitive dependencies (webpack, Babel, ESLint, etc) right into your project so you have full control over them. All of the commands except `eject` will still work, but they will point to the copied scripts so you can tweak them. At this point you’re on your own.

You don’t have to ever use `eject`. The curated feature set is suitable for small and middle deployments, and you shouldn’t feel obligated to use this feature. However we understand that this tool wouldn’t be useful if you couldn’t customize it when you are ready for it.

## Learn More

You can learn more in the [Create React App documentation](https://facebook.github.io/create-react-app/docs/getting-started).

To learn React, check out the [React documentation](https://reactjs.org/).

### Code Splitting

This section has moved here: https://facebook.github.io/create-react-app/docs/code-splitting

### Analyzing the Bundle Size

This section has moved here: https://facebook.github.io/create-react-app/docs/analyzing-the-bundle-size

### Making a Progressive Web App

This section has moved here: https://facebook.github.io/create-react-app/docs/making-a-progressive-web-app

### Advanced Configuration

This section has moved here: https://facebook.github.io/create-react-app/docs/advanced-configuration

### Deployment

This section has moved here: https://facebook.github.io/create-react-app/docs/deployment

### `yarn build` fails to minify

This section has moved here: https://facebook.github.io/create-react-app/docs/troubleshooting#npm-run-build-fails-to-minify
=======
# trackspense

Dashboard screen

- stats 
- recent activity
- add an expense

Add expense

- sharing with ?
- amount
- paid by
- split -> equally
- date
- description
- save
- split -> unequally -> { name : expense } -> sum of expenses = amount 

Remove expense 
- simply remove the record. update owed, get back

Edit expense 
- edit expense -> same as new expense with pre filled values of the selected expense

View Expense :
- who paid whom
- description
- title
- amount
- added by
- added on
- notes and comments section
- edit button
- remove button

Settle expense : 
- who paid whom
- amount
- timestamp
- notes (optional)
- payment mode (optional)
- save button
- cancel button
- close button

Graphs
- time series -> daily, weekly, monthly, quarterly, 6 months, year



Tables : 

all tables will have id, created_at, updated_at

users
- name
- email
- password_digest

{ split_type: 0, payer : 1, payee: [2,3, 4], 9} 

Transaction
- title
- note_id
- payer -> user_id -> index
- payee -> list of user_ids
- amount
- split_type -> 0 - equally, 1- unequally
- category_id
- is_active -> 0,1
- expense_type -> spend, settle

Transaction Item : 
- transaction_id
- amount -> float -> each person amount
- payer -> user_id
- payee -> user_id
- is_active -> 0,1

user_to_expense_mapping :
- user_id
- transaction_id
- role -> payer/payee

categories
- name
- parent_id -> null for main category, integer for a sub category

Notes
- body


API : 


Create
- payer

Update

Read
- all expenses
- single expense

Delete

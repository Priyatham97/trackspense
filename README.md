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


# quiz 45

Download the database brokenbank.db from the learning Log, and write the SQL statements to solve mystery of the transaction that bankrupted the bank:

# SQL
```.sql
select account_id, sum(case when transaction_type = 'withdraw' then amount else 0 end) as withdraw, sum(case when transaction_type = 'deposit' then amount else 0 end) as deposit, sum(case when transaction_type = 'withdraw' then amount else 0 end) - sum(case when transaction_type = 'deposit' then amount else 0 end) as expected_balance from transactions group by account_id;

select accounts.account_id, accounts.balance, sum(case when transaction_type = 'withdraw' then amount else 0 end) as withdraw, sum(case when transactions.transaction_type = 'deposit' then amount else 0 end) as deposit, sum(case when transactions.transaction_type = 'deposit' then amount else 0 end) - sum(case when transactions.transaction_type = 'withdraw' then amount else 0 end) as expected_balance from transactions inner join accounts on transactions.account_id = accounts.account_id group by accounts.account_id;

SELECT
  CASE
    WHEN total_deposit - total_withdraw != balance THEN 'fraud'
    ELSE 'clear'
  END AS 'Status',
  total_deposit,
  total_withdraw,
  balance,
  account_id
FROM (
  SELECT
    SUM(amount) AS total_deposit,
    account_id AS account_deposit
  FROM transactions
  WHERE transaction_type = 'deposit'
  GROUP BY account_id
),
(
  SELECT
    SUM(amount) AS total_withdraw,
    account_id AS account_withdraw
  FROM transactions
  WHERE transaction_type = 'withdraw'
  GROUP BY account_id
),
accounts
WHERE account_deposit = account_withdraw
  AND account_deposit = accounts.account_id;

SELECT customers.first_name, customers.last_name, accounts.account_id
FROM customers
JOIN accounts
ON customers.customer_id = accounts.customer_id
WHERE accounts.account_id IN (12, 13, 15, 17, 19);
```
# Proof of work

<img width="1098" alt="Screen Shot 2023-03-19 at 12 10 12 AM" src="https://user-images.githubusercontent.com/116609563/226114323-d0539107-592d-4be9-8d0c-d0fc4a70bc03.png">

# UML diagram

<img width="386" alt="Screen Shot 2023-03-19 at 1 14 41 AM" src="https://user-images.githubusercontent.com/116609563/226118675-adc008cf-47fd-4b0a-9fa3-8d4bfd2bb541.png">


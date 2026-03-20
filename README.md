# os-lab-quartum-IDTB110319
## Level 2 - Observation Checkpoint 1

Commands run:
- buy_widget Alice 5      → Success, bought 5 widgets
- buy_widget Hacker_Bob 200 → Failed, not enough inventory
- buy_widget Eve -3       → Rejected, invalid input

inventory.txt result: 95 (100 - 5 = 95)
sales.log result: Only 1 entry (Alice), proving invalid transactions are never logged.
![App Screenshot](image/level2.png)

## Level 3 - Observation Checkpoint 2

Run Results:
- Run 1: 84
- Run 2: 78
- Run 3: 80
- Run 4: 82
- Run 5: 88

The inventory never reached 0. Each run produced a different incorrect
result, proving a TOC-TOU race condition exists in the unpatched script.
![App Screenshot](image/level3.png)

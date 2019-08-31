# Nonce Roulette
A mini-roulette themed betting game for the [cruzbit][19] blockchain

## Summary
Players place bets on one or more outcomes, consisting of the digits zero through nine individually (0-9) or various groupings of those digits, by sending an amount (the "bet") to a corresponding cruzbit wallet address. The winning number is determined by the last digit of the "nonce" number used to solve the block containing those transactions. Winning amounts (the "payout") are calculated based on the probability of each respective bet outcome, and are sent to the player in the following block.

## How To Play
1. Select which bet to place, for example "Street 1,2,3"
2. Send your chosen bet amount to the wallet address for "Street 1,2,3" (`iv9crgra0Mm/M/w6UGtuJT0BDX4fKFaniWoxdsuLtgQ=`)
3. Wait for the block to be solved by the cruzbit network
4. When the block is solved, if the last digit of the nonce is one (1), two (2), or three (3), you will recieve a tansaction to the wallet address you used to send your bet in step 2 for the amount of your winnings

## Bets
| Name         | Winning Numbers | Payout | Address                                              |
|--------------|-----------------|--------|------------------------------------------------------|
| Straight 0   | 0               | 8:1    | [AcTyp/7p0KIl58PiK7OKqzZTKtoP0vE7\+3ApzYMx\+vY=][0]  |
| Straight 1   | 1               | 8:1    | [Aq4uXvPrk2SGkCU1q78d28ZdlRNL97b9h9vxuPJH/YY=][1]    |
| Straight 2   | 2               | 8:1    | [HFISOWVHYFYww\+vXdrMj9/WmYzF7lvQioCDNwsR9\+nE=][2]  |
| Straight 3   | 3               | 8:1    | [HpDfORjxVJ6qacxUc4s/gVbQsYZ2I0I0kiXjWt1qePI=][3]    |
| Straight 4   | 4               | 8:1    | [No/XAH6JIF0GhCiaVg5F3MiJtw2C5vh\+P/k7n1DKFMY=][4]   |
| Straight 5   | 5               | 8:1    | [Nyl4QK0AEjCHlpbJpKHr0qdPFFs5ThYMWRqJctzi7Uo=][5]    |
| Straight 6   | 6               | 8:1    | [N3po0XS7A2oc\+WvWciTKMgHN5QLtkyav/XIyagL1tO4=][6]   |
| Straight 7   | 7               | 8:1    | [VD4xSeHVprotc2d\+TLh1lniJmtv942oOOiUAVwXXNCI=][7]   |
| Straight 8   | 8               | 8:1    | [WP5UjWSnsvMHDOOnpBL6\+r4QH7NSqrgYblyLSYA\+nWw=][8]  |
| Straight 9   | 9               | 8:1    | [W6D83AXkxFho9YDu3iVCLdHXDh8f/1M\+\+UHuRGJKmtw=][9]  |
| Street 1,2,3 | 1, 2, 3         | 2:1    | [gab0G1Rab8B2pYRQqdZNKTr8/YPZeTwR9/JZIEZMDOM=][10]   |
| Street 4,5,6 | 4, 5, 6         | 2:1    | [iv9crgra0Mm/M/w6UGtuJT0BDX4fKFaniWoxdsuLtgQ=][11]   |
| Street 7,8,9 | 7, 8, 9         | 2:1    | [qspXA6\+xjUo1yDBq0BVINhNL8mbh4yz78VvJzNuzr9U=][12]  |
| Column 1,4,7 | 1, 4, 7         | 2:1    | [tFka6m0ugtT4BtNySb4IiI0dN6ksnoIMbB2R3OKCkWM=][13]   |
| Column 2,5,8 | 2, 5, 8         | 2:1    | [tjxWfqqg\+vZTg7Z5SX96mcFeAlGbgWIPfW5Gs9O\+y3g=][14] |
| Column 3,6,9 | 3, 6, 9         | 2:1    | [vJ/804LdbAk98GJNKeNg4lkMF1p7My1XaQtic0ic1mY=][15]   |
| Red          | 1, 3, 7, 9      | 1:1    | [5x0OOQ9y1KxFXoPHnA/5AgCKvGGHOEWqqKf1V9laS30=][16]   |
| Black        | 2, 4, 6, 8      | 1:1    | [5zT/5B/Nilb\+fqds/pY5azpEooTLF/yRziEyfMaxhVo=][17]  |
| Top Line     | 0, 1, 2, 3      | 1:1    | [\+KtEu\+Ry0aaSizs/4d/bX6Kkj2RflRT3NKKExITwyUo=][18] |

## Payouts
Winning bets receive their bet amount plus the payout amount as a winning transaction. For example, a bet of 10 cruz on a winning play of "Straight 0", which has a payout of eight-to-one ("8:1") receives a payment for 10 cruz (the "bet") + 80 cruz (8 * 10 = 80; the "payout"), for a total transaction of 90 cruz. Payout transactions are made in the immediately following block (bet block-height + 1), except in the *exceptionally rare* occasion where a subsequent block is found faster than a payout transaction can be propagated to the network, in which case the transaction will appear in the second following block (bet block-height + 2).

Payout transactions are tagged with the bet's block ID in the memo field, facilitating easy correlation between payout and bet. For example: `Nonce Roulette win: 8 on Street 7,8,9 (2:1) at block 577`

## Honest, Transparent
All bets and payouts are recorded publicly on the cruzbit blockchain (the "ledger"), and it is therefore trivial to check that all winning bets are rewarded fairly.

To check that a payout was issued for a winning bet:
1. Determine in which block a bet was placed by searching for the transaction ID in a cruzbit block explorer.
2. Get the block header (or full block) by searching either for its block height or block ID.
3. Observe the last (right-most, or "0 position") digit in the nonce. This is the winning number.
4. Find the address or addresses which correspond to bets that include the winning number. If the bet was sent to one of these addresses, it is a winning bet.
5. Get the full block information of the next successive block in the chain (by block height).
6. Ensure there is a transaction in the reverse direction (from the bet address to the bettor's address) with an amount that is greater than the original bet amount.

## The Details
### Minimum, Maximum Bet Amounts
* The minimum bet is currently: **1 cruz** (100000000 cruzbit)
* The maximum bet is currently: **25 cruz** (2500000000 cruzbit)

### Transaction Fees
Bettors will pay any necessary transaction fees required in order to place bets (transfer funds to a bet wallet address). The game will pay any necessary transaction fees required in order to transfer a payout to winnners (transaction fees *will not* be deducted from a player's winnings).

### The Bank
Each bet address maintains its own bank of funds available for payouts. Funds are not shared across bet types.

#### Available Funds
In the event that a winning address does not have enough funds to cover the entirety of all winning payouts for that bet type, the following rules are followed:
* Winners will never receive less than their bet amount
* Enough funds will be witheld to cover fees to send payout transactions
* Payouts (minus the original bet amount and fees) will be scaled according to the available funds in the account, proportionally among all winners (minus a small percentage, so the account does not reach zero)

For example, if Player A bet 25 CRUZ and Player B bet 10 CRUZ on a 2:1 bet, the account balance is only enough to cover 73% of the amount required to pay all winners a full payout (approximately 77 CRUZ), each winner will be paid their original bet in full plus approximately 70% of their winning payout. So, Player A will receive approximately 60 CRUZ (25 bet + 35 payout), and Player B will recieve approximagely 24 CRUZ (10 bet + 14 payout).

In this way, winning players are rewarded proportionally up to the maximum funds available to reimburse their due winnings, and the wallet retains enough balance to cover the transaction fees of potential future winning bettors, helping to ensure winning players never receive less than their original bet.

Players are encouraged to check any bet address(es) before betting to ensure there is sufficient balance to cover payouts for their desired bet amount.

#### Overbetting
If a _winning_ bet is made that exceeds the maximum bet amount, the following rules will be applied:
* The amount exceeding the maximum bet will be returned unchanged
* The payout multiplier will be applied to the maximum bet amount
* The adjusted original bet (now equal to the maximum bet) will be returned

For example, if the maximum bet is 25 cruz, and a player makes a winning bet of 30 cruz with a 2:1 payout, the player will receive a transaction for 55 cruz \[(30 bet - 25 max) + (25 max * 2 payout) + 25 adjusted original bet = 55\].

Any amount exceeding the maximum bet made to _non-winning_ bet addresses is forfeit to the game. Players are strongly encouraged to know, and limit their bets to the maximum bet amount.

### Miscellaneous
* The numbers zero (0) and five (5) are neither Red, nor Black.
* Nonce Roulette operates on the cruzbit blockchain. Do not attempt to send non-cruzbit coins or currencies to bet addresses.
* Do not include the word "Deposit" in the memo field of transactions made to bet addresses. The "Deposit" designation is used by game operators to increase the available bank amount in bet wallets. Any transaction to bet addresses using "Deposit" in the memo field will be forfeit to the game.
* Nonce Roulette has no control over issues concerning network consensus, nor blockchain forking. In the event of an unintended fork (causing "orphaned blocks"), bets and payouts may be affected. This is entirely out of the control of the game, however occurrences should be quite rare.

[0]:https://cruzbase.com/#/address/AcTyp/7p0KIl58PiK7OKqzZTKtoP0vE7+3ApzYMx+vY=
[1]:https://cruzbase.com/#/address/Aq4uXvPrk2SGkCU1q78d28ZdlRNL97b9h9vxuPJH/YY=
[2]:https://cruzbase.com/#/address/HFISOWVHYFYww+vXdrMj9/WmYzF7lvQioCDNwsR9+nE=
[3]:https://cruzbase.com/#/address/HpDfORjxVJ6qacxUc4s/gVbQsYZ2I0I0kiXjWt1qePI=
[4]:https://cruzbase.com/#/address/No/XAH6JIF0GhCiaVg5F3MiJtw2C5vh+P/k7n1DKFMY=
[5]:https://cruzbase.com/#/address/Nyl4QK0AEjCHlpbJpKHr0qdPFFs5ThYMWRqJctzi7Uo=
[6]:https://cruzbase.com/#/address/N3po0XS7A2oc+WvWciTKMgHN5QLtkyav/XIyagL1tO4=
[7]:https://cruzbase.com/#/address/VD4xSeHVprotc2d+TLh1lniJmtv942oOOiUAVwXXNCI=
[8]:https://cruzbase.com/#/address/WP5UjWSnsvMHDOOnpBL6+r4QH7NSqrgYblyLSYA+nWw=
[9]:https://cruzbase.com/#/address/W6D83AXkxFho9YDu3iVCLdHXDh8f/1M++UHuRGJKmtw=
[10]:https://cruzbase.com/#/address/gab0G1Rab8B2pYRQqdZNKTr8/YPZeTwR9/JZIEZMDOM=
[11]:https://cruzbase.com/#/address/iv9crgra0Mm/M/w6UGtuJT0BDX4fKFaniWoxdsuLtgQ=
[12]:https://cruzbase.com/#/address/qspXA6+xjUo1yDBq0BVINhNL8mbh4yz78VvJzNuzr9U=
[13]:https://cruzbase.com/#/address/tFka6m0ugtT4BtNySb4IiI0dN6ksnoIMbB2R3OKCkWM=
[14]:https://cruzbase.com/#/address/tjxWfqqg+vZTg7Z5SX96mcFeAlGbgWIPfW5Gs9O+y3g=
[15]:https://cruzbase.com/#/address/vJ/804LdbAk98GJNKeNg4lkMF1p7My1XaQtic0ic1mY=
[16]:https://cruzbase.com/#/address/5x0OOQ9y1KxFXoPHnA/5AgCKvGGHOEWqqKf1V9laS30=
[17]:https://cruzbase.com/#/address/5zT/5B/Nilb+fqds/pY5azpEooTLF/yRziEyfMaxhVo=
[18]:https://cruzbase.com/#/address/+KtEu+Ry0aaSizs/4d/bX6Kkj2RflRT3NKKExITwyUo=
[19]:http://cruzbit.github.io

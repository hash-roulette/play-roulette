# Hash Roulette
A mini-roulette themed betting game for the [cruzbit][cruzbit] blockchain

## Summary
Players place bets on one or more outcomes, consisting of hexadecimal digits zero through F (numeric 0 through 9, and alphabetic A through F) individually or in various groupings, by sending an amount (the "bet") to a corresponding cruzbit wallet address. The winning number is determined by the last digit of the "hash" or block ID number used to identify the block containing those transactions. Winning amounts (the "payout") are calculated based on the probability of each respective bet outcome, and are sent to the player in the following block.

## How To Play
1. Select which bet to place, for example "Street 1,2,3"
2. Send your chosen bet amount to the wallet address for "Street 1,2,3" (`dyn1L4ZY5fMFlglTfnhFz0XU2wvQb7DAYSkqVqCtxLU=`)
3. Wait for the block to be solved by the cruzbit network
4. When the block is solved, if the last digit of the hash is one (1), two (2), or three (3), you will receive a transaction to the wallet address you used to send your bet in step 2 for the amount of your winnings

## Bets
| Name          | Winning Numbers     | Payout | Address                                              |
|---------------|---------------------|--------|------------------------------------------------------|
| 0 Straight Up | 0                   | 14:1   | [`AcTyp/7p0KIl58PiK7OKqzZTKtoP0vE7+3ApzYMx+vY=`][0]  |
| 1 Straight Up | 1                   | 14:1   | [`Aq4uXvPrk2SGkCU1q78d28ZdlRNL97b9h9vxuPJH/YY=`][1]  |
| 2 Straight Up | 2                   | 14:1   | [`CRJm28p+IrasQSM7iQ/1R8rpsf7okqeF2u0My1vYpDE=`][2]  |
| 3 Straight Up | 3                   | 14:1   | [`HFISOWVHYFYww+vXdrMj9/WmYzF7lvQioCDNwsR9+nE=`][3]  |
| 4 Straight Up | 4                   | 14:1   | [`HpDfORjxVJ6qacxUc4s/gVbQsYZ2I0I0kiXjWt1qePI=`][4]  |
| 5 Straight Up | 5                   | 14:1   | [`KiTFw/tSzFnx6Hi4Ua/ryfPQhHfwlrpleMXmyz//+JE=`][5]  |
| 6 Straight Up | 6                   | 14:1   | [`KoyawFhfHW2s+wHgMRKoWyr0yAnFcvs4HAhpzVCPpXs=`][6]  |
| 7 Straight Up | 7                   | 14:1   | [`No/XAH6JIF0GhCiaVg5F3MiJtw2C5vh+P/k7n1DKFMY=`][7]  |
| 8 Straight Up | 8                   | 14:1   | [`Nyl4QK0AEjCHlpbJpKHr0qdPFFs5ThYMWRqJctzi7Uo=`][8]  |
| 9 Straight Up | 9                   | 14:1   | [`N3po0XS7A2oc+WvWciTKMgHN5QLtkyav/XIyagL1tO4=`][9]  |
| A Straight Up | A                   | 14:1   | [`O6L5bz2pgkpQGBQ6HYuCn55PN8jpd6lzzYn0SuIF4NQ=`][10] |
| B Straight Up | B                   | 14:1   | [`Pn3ptCOS8IqR2MJDb+K5RytuJVmf79uCMniKGiyQVb0=`][11] |
| C Straight Up | C                   | 14:1   | [`VD4xSeHVprotc2d+TLh1lniJmtv942oOOiUAVwXXNCI=`][12] |
| D Straight Up | D                   | 14:1   | [`V2eOD3BgrP+gy45+yuCK0N8yyo1wamb9xsItqeIVRmM=`][13] |
| E Straight Up | E                   | 14:1   | [`WP5UjWSnsvMHDOOnpBL6+r4QH7NSqrgYblyLSYA+nWw=`][14] |
| F Straight Up | F                   | 14:1   | [`WYtIS5bwEx28CI8EHPullZ4pTLCaD6svMLCPMZboYUA=`][15] |
| Green         | 0, F                | 7:1    | [`W6D83AXkxFho9YDu3iVCLdHXDh8f/1M++UHuRGJKmtw=`][16] |
| Basket 0,1,2  | 0, 1, 2             | 4:1    | [`bPUO9z3QlVF13JVVLCyw/MaDy397GTzQz21ZxYE2nmQ=`][17] |
| Basket 0,2,3  | 0, 2, 3             | 4:1    | [`b0vnFNzGKggb9UigbI9BrO0mPpnOShTvLC3S+w8lzjA=`][18] |
| Street 1,2,3  | 1, 2, 3             | 4:1    | [`dyn1L4ZY5fMFlglTfnhFz0XU2wvQb7DAYSkqVqCtxLU=`][19] |
| Street 4,5,6  | 4, 5, 6             | 4:1    | [`e31Pgpj350ubi3fSTpUWsIf+yhUimDvebTbmw9+LMC4=`][20] |
| Street 7,8,9  | 7, 8, 9             | 4:1    | [`gab0G1Rab8B2pYRQqdZNKTr8/YPZeTwR9/JZIEZMDOM=`][21] |
| Street A,B,C  | A, B, C             | 4:1    | [`iv9crgra0Mm/M/w6UGtuJT0BDX4fKFaniWoxdsuLtgQ=`][22] |
| Street D,E,F  | D, E, F             | 4:1    | [`iwm31II9iWtNyOsuMGOkStJRMAJukgyOxjQFT+affjQ=`][23] |
| Column 1-D    | 1, 4, 7, A, D       | 2:1    | [`jco34+pk6YVsKwSxQBxm6NfRO8XS2CGombg0rgh7+WY=`][24] |
| Column 2-E    | 2, 5, 8, B, E       | 2:1    | [`kmzy3U6jUGml8vVGEZiNELmwOI3up74OzUT0N662xH0=`][25] |
| Column 3-F    | 3, 6, 9, C, F       | 2:1    | [`qgfL5oBlIM93VEg+++T8OwvdxK3AiMxSrEdViu37KlY=`][26] |
| First 6       | 1, 2, 3, 4, 5, 6    | 1.5:1  | [`qspXA6+xjUo1yDBq0BVINhNL8mbh4yz78VvJzNuzr9U=`][27] |
| Second 6      | 4, 5, 6, 7, 8, 9    | 1.5:1  | [`tFka6m0ugtT4BtNySb4IiI0dN6ksnoIMbB2R3OKCkWM=`][28] |
| Third 6       | 7, 8, 9, A, B, C    | 1.5:1  | [`tjxWfqqg+vZTg7Z5SX96mcFeAlGbgWIPfW5Gs9O+y3g=`][29] |
| Fourth 6      | A, B, C, D, E, F    | 1.5:1  | [`vJ/804LdbAk98GJNKeNg4lkMF1p7My1XaQtic0ic1mY=`][30] |
| Red           | 1, 3, 5, 7, 9, A, E | 1:1    | [`y7vcGfJNY4NBUppKbyeHvsDf1Phf6KhP/v/AqqLeve8=`][31] |
| Black         | 2, 4, 6, 8, B, C, D | 1:1    | [`5x0OOQ9y1KxFXoPHnA/5AgCKvGGHOEWqqKf1V9laS30=`][32] |
| Odd           | 1, 3, 5, 7, 9, B, D | 1:1    | [`5zT/5B/Nilb+fqds/pY5azpEooTLF/yRziEyfMaxhVo=`][33] |
| Even          | 2, 4, 6, 8, A, C, E | 1:1    | [`+KtEu+Ry0aaSizs/4d/bX6Kkj2RflRT3NKKExITwyUo=`][34] |

## Payouts
Winning bets receive their bet amount plus the payout amount as a winning transaction. For example, a bet of 10 cruz on a winning play of "Straight 0", which has a payout of eight-to-one ("14:1") receives a payment for 10 cruz (the "bet") + 140 cruz (14 * 10 = 140; the "payout"), for a total transaction of 150 cruz. Payout transactions are made in the immediately following block (bet block-height + 1), except in the *exceptionally rare* occasion where a subsequent block is found faster than a payout transaction can be propagated to the network, in which case the transaction will appear in the second following block (bet block-height + 2).

Payout transactions are tagged with the bet's block ID in the memo field, facilitating easy correlation between payout and bet. For example: `Hash Roulette win: 8 on Street 7,8,9 (4:1) at block 28577`

## Honest, Transparent
All bets and payouts are recorded publicly on the cruzbit blockchain (the "ledger"), and it is therefore trivial to check that all winning bets are rewarded fairly.

To check that a payout was issued for a winning bet:
1. Determine in which block a bet was placed by searching for the transaction ID in a cruzbit block explorer.
2. Get the block header (or full block) by searching either for its block height.
3. Observe the last (right-most, or "0 position") digit in the Block ID (hash). This is the winning number.
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

For example, if Player A bet 25 CRUZ and Player B bet 10 CRUZ on a 2:1 bet, the account balance is only enough to cover 73% of the amount required to pay all winners a full payout (approximately 77 CRUZ), each winner will be paid their original bet in full plus approximately 70% of their winning payout. So, Player A will receive approximately 60 CRUZ (25 bet + 35 payout), and Player B will receive approximately 24 CRUZ (10 bet + 14 payout).

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
* The letters (referred to as "numbers") "A", "C", and "E" are considered EVEN, while "B", and "D" are considered ODD.
* "0" (zero) and "F" are _NOT_ RED, BLACK, EVEN, nor ODD.
* Hash Roulette operates on the cruzbit blockchain. Do not attempt to send non-cruzbit coins or currencies to bet addresses.
* Do not include the word "Deposit" in the memo field of transactions made to bet addresses. The "Deposit" designation is used by game operators to increase the available bank amount in bet wallets. Any transaction to bet addresses using "Deposit" in the memo field will be forfeit to the game.
* Hash Roulette has no control over issues concerning network consensus, nor blockchain forking. In the event of an unintended fork (causing "orphaned blocks"), bets and payouts may be affected. This is entirely out of the control of the game, however occurrences should be quite rare.

[cruzbit]:http://cruzbit.github.io
[0]:https://cruzbase.com/#/address/AcTyp/7p0KIl58PiK7OKqzZTKtoP0vE7+3ApzYMx+vY=
[1]:https://cruzbase.com/#/address/Aq4uXvPrk2SGkCU1q78d28ZdlRNL97b9h9vxuPJH/YY=
[2]:https://cruzbase.com/#/address/CRJm28p+IrasQSM7iQ/1R8rpsf7okqeF2u0My1vYpDE=
[3]:https://cruzbase.com/#/address/HFISOWVHYFYww+vXdrMj9/WmYzF7lvQioCDNwsR9+nE=
[4]:https://cruzbase.com/#/address/HpDfORjxVJ6qacxUc4s/gVbQsYZ2I0I0kiXjWt1qePI=
[5]:https://cruzbase.com/#/address/KiTFw/tSzFnx6Hi4Ua/ryfPQhHfwlrpleMXmyz//+JE=
[6]:https://cruzbase.com/#/address/KoyawFhfHW2s+wHgMRKoWyr0yAnFcvs4HAhpzVCPpXs=
[7]:https://cruzbase.com/#/address/No/XAH6JIF0GhCiaVg5F3MiJtw2C5vh+P/k7n1DKFMY=
[8]:https://cruzbase.com/#/address/Nyl4QK0AEjCHlpbJpKHr0qdPFFs5ThYMWRqJctzi7Uo=
[9]:https://cruzbase.com/#/address/N3po0XS7A2oc+WvWciTKMgHN5QLtkyav/XIyagL1tO4=
[10]:https://cruzbase.com/#/address/O6L5bz2pgkpQGBQ6HYuCn55PN8jpd6lzzYn0SuIF4NQ=
[11]:https://cruzbase.com/#/address/Pn3ptCOS8IqR2MJDb+K5RytuJVmf79uCMniKGiyQVb0=
[12]:https://cruzbase.com/#/address/VD4xSeHVprotc2d+TLh1lniJmtv942oOOiUAVwXXNCI=
[13]:https://cruzbase.com/#/address/V2eOD3BgrP+gy45+yuCK0N8yyo1wamb9xsItqeIVRmM=
[14]:https://cruzbase.com/#/address/WP5UjWSnsvMHDOOnpBL6+r4QH7NSqrgYblyLSYA+nWw=
[15]:https://cruzbase.com/#/address/WYtIS5bwEx28CI8EHPullZ4pTLCaD6svMLCPMZboYUA=
[16]:https://cruzbase.com/#/address/W6D83AXkxFho9YDu3iVCLdHXDh8f/1M++UHuRGJKmtw=
[17]:https://cruzbase.com/#/address/bPUO9z3QlVF13JVVLCyw/MaDy397GTzQz21ZxYE2nmQ=
[18]:https://cruzbase.com/#/address/b0vnFNzGKggb9UigbI9BrO0mPpnOShTvLC3S+w8lzjA=
[19]:https://cruzbase.com/#/address/dyn1L4ZY5fMFlglTfnhFz0XU2wvQb7DAYSkqVqCtxLU=
[20]:https://cruzbase.com/#/address/e31Pgpj350ubi3fSTpUWsIf+yhUimDvebTbmw9+LMC4=
[21]:https://cruzbase.com/#/address/gab0G1Rab8B2pYRQqdZNKTr8/YPZeTwR9/JZIEZMDOM=
[22]:https://cruzbase.com/#/address/iv9crgra0Mm/M/w6UGtuJT0BDX4fKFaniWoxdsuLtgQ=
[23]:https://cruzbase.com/#/address/iwm31II9iWtNyOsuMGOkStJRMAJukgyOxjQFT+affjQ=
[24]:https://cruzbase.com/#/address/jco34+pk6YVsKwSxQBxm6NfRO8XS2CGombg0rgh7+WY=
[25]:https://cruzbase.com/#/address/kmzy3U6jUGml8vVGEZiNELmwOI3up74OzUT0N662xH0=
[26]:https://cruzbase.com/#/address/qgfL5oBlIM93VEg+++T8OwvdxK3AiMxSrEdViu37KlY=
[27]:https://cruzbase.com/#/address/qspXA6+xjUo1yDBq0BVINhNL8mbh4yz78VvJzNuzr9U=
[28]:https://cruzbase.com/#/address/tFka6m0ugtT4BtNySb4IiI0dN6ksnoIMbB2R3OKCkWM=
[29]:https://cruzbase.com/#/address/tjxWfqqg+vZTg7Z5SX96mcFeAlGbgWIPfW5Gs9O+y3g=
[30]:https://cruzbase.com/#/address/vJ/804LdbAk98GJNKeNg4lkMF1p7My1XaQtic0ic1mY=
[31]:https://cruzbase.com/#/address/y7vcGfJNY4NBUppKbyeHvsDf1Phf6KhP/v/AqqLeve8=
[32]:https://cruzbase.com/#/address/5x0OOQ9y1KxFXoPHnA/5AgCKvGGHOEWqqKf1V9laS30=
[33]:https://cruzbase.com/#/address/5zT/5B/Nilb+fqds/pY5azpEooTLF/yRziEyfMaxhVo=
[34]:https://cruzbase.com/#/address/+KtEu+Ry0aaSizs/4d/bX6Kkj2RflRT3NKKExITwyUo=

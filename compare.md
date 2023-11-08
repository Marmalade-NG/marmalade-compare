# Marmalade V1 vs V2 vs NG

## General

  ~                       | Marmalade V1             | Marmalade V2            | Marmalade NG            |
--------------------------|--------------------------|-------------------------|-------------------------|
Deployed - Tesnet         | :white_check_mark:       | :white_check_mark:      | :white_check_mark:      |
Deployed - Mainnet        | :white_check_mark:       | :white_check_mark:      | :x:                     |
Nice website / video      | :x:                      | :white_check_mark:      | :x:                     |
Keys / Administration     | Controled by Kadena (1)  | Controled by Kadena (1) | Community Multi-sig     |
Code quality              | Good :white_check_mark:  | Bad :x: (2)             | Good :white_check_mark: |
Security                  | :white_check_mark:       | :x: :bangbang: (3)      | :heavy_check_mark: (4)  |
Private instances support | :white_check_mark:       | :x:                     | :white_check_mark:      |
Explorer                  | :x:                      | :x:                     | :white_check_mark:      |
Indexer                   | :white_check_mark:       | :x:                     | :x:                     |
Simple integration        | :x:                      | :x:                     | :white_check_mark:      |
Usable without indexer    | :x:                      | :x:                     | :white_check_mark:      |
X-chain friendly          | :white_check_mark:       | :x: (5)                 | :white_check_mark:      |

## Features

Only features with standard provided and deployed modules

  ~                                                  | Marmalade V1             | Marmalade V2                           | Marmalade NG                           |
-----------------------------------------------------|--------------------------|--------------------------------------  |----------------------------------------|
Fixed prices sales                                   | :white_check_mark:       | :white_check_mark: :warning: (6)       | :white_check_mark:                     |
Auction sales                                        | :x:                      | :heavy_check_mark: :warning: (7)(8)(9) | :white_check_mark:                     |
Dutch Auction sales                                  | :x:                      | :x:                                    | :white_check_mark:                     |
Royalties                                            | :white_check_mark:       | :heavy_check_mark: :warning: (10)      | :white_check_mark:                     |
Adjustable royalties                                 | :x:                      | :x:                                    | :white_check_mark:                     |
Marketplace fees                                     | :x:                      | :x:                                    | :white_check_mark:                     |
Non-fungible tokens                                  | :white_check_mark:       | :white_check_mark:                     | :white_check_mark:                     |
Fixed issuance Poly-fungible tokens                  | :white_check_mark:       | :x:                                    | :white_check_mark:                     |
Instant minting enforced tokens                      | :x:                      | :x:                                    | :white_check_mark:                     |
Guards limited tokens                                | :x:                      | :white_check_mark:                     | :white_check_mark:                     |
Blacklistable tokens                                 | :x:                      | :x:                                    | :white_check_mark:                     |
Lending protocols <br> Custody marketplaces support  | :x:                      | :x:                                    | :white_check_mark:                     |
Multiple sellers                                     | :x:                      | :x:                                    | :white_check_mark: (11)                |
Currencies whitelist by creator                      | :x:                      | :x:                                    | :white_check_mark: (11)                |
Lottery sale                                         | :x:                      | :x:                                    | :white_check_mark: (11) :warning: (12) |

## Extendability

  ~                                                            | Marmalade V1             | Marmalade V2                           | Marmalade NG                |
---------------------------------------------------------------|--------------------------|--------------------------------------  |-----------------------------|
Custom sales process added by the creator (policies)           | :heavy_check_mark: (13)  | :heavy_check_mark: :bangbang: (14)     | :white_check_mark:          |
Sales process added by the Marmalade admins                    | :x:                      | :white_check_mark: (15)                | :white_check_mark: (16)     |
Custom tokens/sales management added by the creator (policies) | :white_check_mark:       | :white_check_mark:                     | :white_check_mark:          |
Custom tokens/sales management proposed by the admins          | :x:                      | :x:                                    | :white_check_mark: (16)     |


## Notes

(1) : Key management is unclear: who exactly own the keys ? Who has the ability to upgrade code, and manipulate the ledger ?

(2) : Dead code, Typechecker results ignored, code difficult to read and to maintain. Complex control flow.

(3) : More than 8 serious issues already discovered

(4) : A single serious issues has been discovered

(5) : Tokens identifier can't be the same on different chains, preventing X-chains transfers

(6) : Only works in KDA in case of enabled royalty

(7) : Lack of functionnality, could lead to unfair sales. (no minimum increment, no time extension)

(8) : Some cases may lock tokens / or make buyers loose funds

(9) : Only works in KDA

(10) : Royalities can only be paid in KDA

(11) : Support through extra policies

(12) : Possibly unsafe. Avoid for high value tokens

(13) : Everything must be implemented by the creator

(14) : Policies can access the quote system => and can't use royalties

(15) : Tokens creator can't refuse newly approved (by who ?) sales mechanisms

(16) : Tokens creators can refuse all new mechanisms, or blacklist them one by one (Extra policies)

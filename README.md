
# Welcome to this GitHub # 

- - - -



🟢 --- Done<br/>
🔴 --- Not done<br/>
🟠 --- Half way done<br/>
🔵 --- Getting close to finishing<br/><br/>


🟣 --- Error or major issue present <br/>
⚫ --- Probably impossible to do or most likely going to change <br/>

<br/>

### SKIRMISH COMPONENTS
<br/><br/>
----------------------------------- CAIRO CONTRACTS (Last full code clean up and commenting 25/06/22) ALL TO REDO --------------------------------------
<br/>
Test token for pay transactions: 0x03e41c33cfb4081c8a40f08bc61d7b62396485587415b967e1dc295a156d03e9
<br/><br/>

**CONTRACT 1: SKIRMISH MAIN CONTRACT**
<br/>

Main contract of the game 
<br/>

| Status      | Tested      | Function    | Type        | Description   |     
| ----------- | ----------- | ----------- | ----------- | ----------- |
| 🟢 |  🟢    | SetTokenAddress  |   @external    |  Set the token address to be payed with
| 🟢 |  🟢  | SetFee |   @external    |  Set the fee the contract takes when the game ends
| 🟢 |   🟢   | SetSNSCost  |   @external    |  Set the cost to make an SNS,  times by 10**18
|  🟢|  🟢   | SetSNS  |   @external    |  Set the SNS of the calling address
| 🟢 |  🔴 | WithdrawToken  |   @external    | Withdraw tokens from the contract
| 🟢 |  🔴 | GameLobbyStart  |   @external    |  Function called on the start of the lobby by the "host". pays wager into contract
| 🟢 |  🔴 | GameLobbyJoin  |   @external    |  Function called by the joiner. pays wager into contract
| 🟢 |  🔴 | GameOutcome  |   @external    |  Action depending on outcome of the game
| 🟢 |  🟢   | GetSNSFromAddress  |   @view    |  Given an SNS(felt) return the holder's address. Return 0 if not held
| 🟢 |   🟢  | GetAddressFromSNS  |   @view    |  Given an Address return the SNS associated. Return 0 if available
| 🟢 |  🟢| GetAcceptedTokenAddress  |   @view    |  Return the Address of the ERC20 token accepted for payments  
| 🟢 |   🟢  | GetSNSCost  |   @view    |  Get the cost of setting an SNS.  divide by 10**18 
| 🟢 |   🔴   | SeeBalanceOfContract  |   @view    |  Get the current balance of the contract  (possibly will be deleted in future)
| 🔴 |  🔴  | GameLobbyView  |   @view    |  Given a RoomCode of a current game (felt) return the address of the two players and the wager
<br/>


Most current deployed test contract: 0x05cb11861182a60720b1ed675b45120e3763b70726f6026cf7d0a86efe47e46a<br/><br/>



**CONTRACT 2: TALK TO REALMS NFT**

Contract used to get the data from the realms NFT to the game, data like the Realms available and the troops inside and the adventurers available




**CONTRACT 3: DATABASE ACCOUNT TROOPS**

Contract used as onchain database, when the player decideds its team it will be saved on the chain

<br/>
Additional Notes:  <br/>
Need to add all of the owner stuff and the asserts        <br/>
Look into Account abstraction <br/>
When modifying multiple realms instead of doing one trans per realms do one big transaction, maybe implement bitmanip function <br/>
Look into events      
There is an oversight on how to deal with the actual outcome of the game, there is nothing stopping the player from just going to the voyager and using the external func there                <br/>
__________________________________________<br/>
Other usefull links related to this project:     <br/>
https://github.com/jrkosinski/crypto-champ   <br/>
       https://github.com/jrkosinski/crypto-champ/blob/master/sports-bets/contracts/SportsBets.sol    <br/>
https://medium.com/visionary-hub/building-a-sport-betting-dapp-d5f1048ba524    <br/>

<br/><br/>
----------------------------------- REACT BACKEND (Last full code clean up and commenting 24/06/22)----------------------------------------
<br/>

| Progress    | Task        | Notes   |     
| ----------- | ----------- | -----------   |
| 🟢 |Implement Unity and be able to call functions|    |
| ⚫ |Full screen on Unity startup|    |
| 🟢 |Send transaction updates|    |
| 🟢 |Send address data on connect|    |
| 🟣 |Block game if the wallet is not connected or account is switched|    |
| 🟢 |Connect argent wallet|    |
| 🟣|Connect braavos wallet|    |
| 🟣 |Disconnect wallet voluntarily |    |
| 🟠 |Turn array from cairo to json to be sent to unity for troops|    |
| 🟢 |Handle view functions|    |
|🟢  |Handle uint256 values|    |
| 🟢 |Add token to wallet via code|    |
|🟢 |Add Util script|    |
| 🔴 |Add contract 1|    |
| 🔴 |Add contract 2|    |
| 🔴|Add contract 3|    |
| 🔴 |On contract 1 deduct fee for the contract to keep|    |


<br/>
Additional Notes:  <br/>
Open issue on the starknet react github for the braavos wallet <br/>

Other usefull links related to this project:


<br/><br/>
----------------------------------- UNITY PROJECT (Last full code clean up and commenting 25/06/22) ----------------------------------------
<br/>

| Progress    | Task        | Notes   |     
| ----------- | ----------- | -----------   |
| ⚫ |Autoconnect on game startup if server is available |  |
| 🔵 |Offline scene finished|  |
| 🟢 |Receive address data on connect|  |
| 🔴: |change from the playerprefs or put ifend regions int he code |  |
| 🔵 |Main util script to be accessed from everywhere|  |
| 🟢 |Check if two of the same players exist in the server if so kick|  |
|  ******  | ****** |  ******  |
| 🟢 |Host game menu section|  |
| 🟢 |join game menu section|  |
| 🔵 |Deck building menu section|  |
| 🟢|Loading menu section|  |
| 🟢 |Setting menu section|  |
| 🟠|Contract view menu section|  |
|🟢  |Receive transaction updates|  |
| 90% |Finish the menu UI|  |
| 🟢 |Show all availabe games|  |
| 🟢 |Basics of matchmaking and player made lobbies|  |
| 🟢 |Webhook to discord to be used as a database|  |
| 🟠 |Send webhooks to discord on starting lobby and joining lobby|  |
| 🟢 |Pop up error UI|  |
| 🟢 |Sorting algos for the various menus|  |
| 🔴 |Basic all roudn progression checks|  |
|  ******  | ****** |  ******  |
| 🟢 |Basics of RealmsUI |  |
| 🟢 |Basics of troopsUI|  |
| 🟠 |Basics of adventurerUI|  |
| 🔵 |Tooltip on hover over units and realms|  |
| 🟢 |Able to select the realms by looking for their ID|  |
| 🔵 |Player is able to make its team and save it to be then used in game|  |
| 🔴 |Receive data from NFT|  |
| 🔴 |Write data to Database account troops contract|  |
| 🔴 |Implement a resource folder so every prefab is available there in conjunction with the generalUtil script |  |
|  ******  | ****** |  ******  |
| 🔴 |function to update the player ont he server side with the client side data|  |
| 🔴 |categorize game state|  |
| 🟢 |Fix the names so they show in the lobby|  |
| 🔴 |Connect the skirmish main contract to the game |  |
| ⚫ |Only allowed to start the game after both players are ready|  |
| 🔵 |Turn based functionality setup|  |
| 🔵 |Once the game starts send data to server so both clients can communicate|  |
| 🔴 |Once a player places a card replicate action on the other client|  |
| 🔴 |Prohibit client from interacting with the other client's card|  |
| 🔴 |Add basic game score mechanic |  |
| 🔴 |Add basic server checks in the middle of moves to validate moves|  |
| 🔴 |Before the start of the game check the deck is valid|  |
| 🔴 |Deal with the outcome of the match|  |
| 🟠 |Deal with instances from either players disconnecting early or server failure|  |
| 🔴 |Deploy mock server on AWS|  |

<br/>
Additional Notes:<br/>


Other usefull links related to this project:


- - - -


### MORE COMING....

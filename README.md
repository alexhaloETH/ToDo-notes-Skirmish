
# Welcome to this GitHub # 

- - - -



:green_circle: --- Done<br/>
:red_circle: --- Not done<br/>
:orange_circle: --- Half way done<br/>
:large_blue_circle: --- Getting close to finishing<br/><br/>


:purple_circle: --- Error or major issue present <br/>
:black_circle: --- Probably impossible to do or most likely going to change <br/>

<br/>

### SKIRMISH COMPONENTS
<br/><br/>
----------------------------------- CAIRO CONTRACTS (Last full code clean up and commenting 25/06/22) --------------------------------------
<br/>
Test token for pay transactions: 0x03e41c33cfb4081c8a40f08bc61d7b62396485587415b967e1dc295a156d03e9
<br/><br/>

**CONTRACT 1: SKIRMISH MAIN CONTRACT**
<br/>

Main contract of the game 
<br/>

| Status      | Tested      | Function    | Type        | Description   |     
| ----------- | ----------- | ----------- | ----------- | ----------- |
| :green_circle: |   :green_circle:   | SetTokenAddress  |   @external    |  Set the token address to be payed with
| :green_circle: |   :green_circle:   | SetFee |   @external    |  Set the fee the contract takes when the game ends
| :green_circle: |   :green_circle:   | SetSNSCost  |   @external    |  Set the cost to make an SNS,  times by 10**18
| :green_circle: |   :green_circle:   | SetSNS  |   @external    |  Set the SNS of the calling address
| :green_circle: |  :red_circle: | WithdrawToken  |   @external    | Withdraw tokens from the contract
| :green_circle: |  :red_circle: | GameLobbyStart  |   @external    |  Function called on the start of the lobby by the "host". pays wager into contract
| :green_circle: |  :red_circle: | GameLobbyJoin  |   @external    |  Function called by the joiner. pays wager into contract
| :green_circle: |  :red_circle: | GameOutcome  |   @external    |  Action depending on outcome of the game
| :green_circle: |   :green_circle:   | GetSNSFromAddress  |   @view    |  Given an SNS(felt) return the holder's address. Return 0 if not held
| :green_circle: |   :green_circle:   | GetAddressFromSNS  |   @view    |  Given an Address return the SNS associated. Return 0 if available
| :green_circle: |   :green_circle:   | GetAcceptedTokenAddress  |   @view    |  Return the Address of the ERC20 token accepted for payments  
| :green_circle: |   :green_circle:   | GetSNSCost  |   @view    |  Get the cost of setting an SNS.  divide by 10**18 
| :green_circle: |   :red_circle:   | SeeBalanceOfContract  |   @view    |  Get the current balance of the contract  (possibly will be deleted in future)
| :red_circle: |  :red_circle:  | GameLobbyView  |   @view    |  Given a RoomCode of a current game (felt) return the address of the two players and the wager
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
| :green_circle: |Implement Unity and be able to call functions|    |
| :black_circle: |Full screen on Unity startup|    |
| :green_circle: |Send transaction updates|    |
| :green_circle: |Send address data on connect|    |
| :purple_circle: |Block game if the wallet is not connected or account is switched|    |
| :green_circle: |Connect argent wallet|    |
| :purple_circle: |Connect braavos wallet|    |
| :purple_circle: |Disconnect wallet voluntarily |    |
| :orange_circle: |Turn array from cairo to json to be sent to unity for troops|    |
| :green_circle: |Handle view functions|    |
| :green_circle: |Handle uint256 values|    |
| :green_circle: |Add token to wallet via code|    |
| :green_circle: |Add Util script|    |
| :red_circle: |Add contract 1|    |
| :red_circle: |Add contract 2|    |
| :red_circle: |Add contract 3|    |
| :red_circle: |On contract 1 deduct fee for the contract to keep|    |


<br/>
Additional Notes:  <br/>
Open issue on the starknet react github for the braavos wallet <br/>

Other usefull links related to this project:


<br/><br/>
----------------------------------- UNITY PROJECT (Last full code clean up and commenting 25/06/22) ----------------------------------------
<br/>

| Progress    | Task        | Notes   |     
| ----------- | ----------- | -----------   |
| :black_circle: |Autoconnect on game startup if server is available |  |
| :large_blue_circle: |Offline scene finished|  |
| :green_circle: |Receive address data on connect|  |
| :large_blue_circle: |Main util script to be accessed from everywhere|  |
| :green_circle: |Check if two of the same players exist in the server if so kick|  |
|  ******  | ****** |  ******  |
| :green_circle: |Host game menu section|  |
| :green_circle: |join game menu section|  |
| :large_blue_circle: |Deck building menu section|  |
| :green_circle: |Loading menu section|  |
| :green_circle: |Setting menu section|  |
| :orange_circle: |Contract view menu section|  |
| :green_circle: |Receive transaction updates|  |
| 90% |Finish the menu UI|  |
| :green_circle: |Show all availabe games|  |
| :green_circle: |Basics of matchmaking and player made lobbies|  |
| :green_circle: |Webhook to discord to be used as a database|  |
| :orange_circle: |Send webhooks to discord on starting lobby and joining lobby|  |
| :green_circle: |Pop up error UI|  |
| :green_circle: |Sorting algos for the various menus|  |
|  ******  | ****** |  ******  |
| :green_circle: |Basics of RealmsUI |  |
| :green_circle: |Basics of troopsUI|  |
| :orange_circle: |Basics of adventurerUI|  |
| :large_blue_circle: |Tooltip on hover over units and realms|  |
| :green_circle: |Able to select the realms by looking for their ID|  |
| :large_blue_circle: |Player is able to make its team and save it to be then used in game|  |
| :red_circle: |Receive data from NFT|  |
| :red_circle: |Write data to Database account troops contract|  |
| :red_circle: |Implement a resource folder so every prefab is available there in conjunction with the generalUtil script |  |
|  ******  | ****** |  ******  |
| :red_circle: |function to update the player ont he server side with the client side data|  |
| :red_circle: |categorize game state|  |
| :green_circle: |Fix the names so they show in the lobby|  |
|  :red_circle: |Connect the skirmish main contract to the game |  |
| :black_circle: |Only allowed to start the game after both players are ready|  |
| :large_blue_circle: |Turn based functionality setup|  |
| :orange_circle: |Once the game starts send data to server so both clients can communicate|  |
| :red_circle: |Once a player places a card replicate action on the other client|  |
| :red_circle: |Prohibit client from interacting with the other client's card|  |
| :red_circle: |Add basic game score mechanic |  |
|  :red_circle:|Add basic server checks in the middle of moves to validate moves|  |
| :red_circle: |Before the start of the game check the deck is valid|  |
| :red_circle:  |Deal with the outcome of the match|  |
| :orange_circle: |Deal with instances from either players disconnecting early or server failure|  |
| :red_circle: |Deploy mock server on AWS|  |

<br/>
Additional Notes:<br/>


Other usefull links related to this project:


- - - -


### MORE COMING....

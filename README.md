
# Welcome to this GitHub # 

- - - -


🔴 --- Not done<br/>
🟢 --- Done<br/>
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
| 🟢 |  🟢    | SetTokenAddress  |   @external    |  Set the token address to be payed with|
| 🟢 |  🟢  | SetFee |   @external    |  Set the fee the contract takes when the game ends|
| 🟢 |   🟢   | SetSNSCost  |   @external    |  Set the cost to make an SNS,  times by 10**18|
|  🟢|  🟢   | SetSNS  |   @external    |  Set the SNS of the calling address|
| 🟢 |  🔴 | WithdrawToken  |   @external    | Withdraw tokens from the contract|
| 🟢 |  🔴 | GameLobbyStart  |   @external    |  Function called on the start of the lobby by the "host". pays wager into contract|
| 🟢 |  🔴 | GameLobbyJoin  |   @external    |  Function called by the joiner. pays wager into contract|
| 🟢 |  🔴 | GameOutcome  |   @external    |  Action depending on outcome of the game|
| 🟢 |  🟢   | GetSNSFromAddress  |   @view    |  Given an SNS(felt) return the holder's address. Return 0 if not held|
| 🟢 |   🟢  | GetAddressFromSNS  |   @view    |  Given an Address return the SNS associated. Return 0 if available|
| 🟢 |  🟢| GetAcceptedTokenAddress  |   @view    |  Return the Address of the ERC20 token accepted for payments  |
| 🟢 |   🟢  | GetSNSCost  |   @view    |  Get the cost of setting an SNS.  divide by 10**18 |
| 🟢 |   🔴   | SeeBalanceOfContract  |   @view    |  Get the current balance of the contract  (possibly will be deleted in future)|
| 🟢 |  🔴  | GameLobbyView  |   @view    |  Given a RoomCode of a current game (felt) return the address of the two players and the wager|
| 🟢 |   🔴   | GetServerStatus  |   @view    |  |
| 🟢 |  🔴  | SetServerStatus  |   @external    |  |
| 🔴 |  🔴  | GetClientGameManager  |   @view    |  |
| 🔴 |  🔴  | SetClientGameManager  |   @external    |  |
<br/>


Most current deployed test contract: -------- <br/><br/>



**CONTRACT 2: TALK TO REALMS NFT**

| Status      | Tested      | Function    | Type        | Description   |     
| ----------- | ----------- | ----------- | ----------- | ----------- |
| 🔴 |  🔴    | GetAllRealmsOfAnAddress  |   @view    | |
| 🔴 |  🔴  | GetAllTroopsOfARealm |   @view    |  |

Contract used to get the data from the realms NFT to the game, data like the Realms available and the troops inside and the adventurers available
Just needs to be implemented into the realms repo 



**CONTRACT 3: DATABASE ACCOUNT TROOPS**
| Status      | Tested      | Function    | Type        | Description   |     
| ----------- | ----------- | ----------- | ----------- | ----------- |
| 🟢 |  🟢    | SetDeckData  |   @external    | |
| 🟢 |  🟢  | GetDeckData |   @view    |  |




Contract used as onchain database, when the player decideds its team it will be saved on the chain







<br/>
Additional Notes:  <br/>
Need to add all of the owner stuff and the asserts        <br/>
Look into Account abstraction <br/>
Look into events     
look into changing states of the games straight from cairo instead of doing something from the server cli <br/>
LOOK INTO SNARKS INSTEAD OF THE CURRENT WAY OF WINNING THE GAME (most likely STARKs) <br/>
Find ways to start to transition the server into the chain <br/>

__________________________________________<br/>
Other usefull links related to this project:     <br/>
https://github.com/jrkosinski/crypto-champ   <br/>
       https://github.com/jrkosinski/crypto-champ/blob/master/sports-bets/contracts/SportsBets.sol    <br/>
https://medium.com/visionary-hub/building-a-sport-betting-dapp-d5f1048ba524    <br/>
GitHub - iden3/snarkjs: zkSNARK implementation in JavaScript & WASM<br/>
iden3 | Circom<br/>

<br/><br/>
----------------------------------- REACT BACKEND (Last full code clean up and commenting 24/06/22)----------------------------------------
<br/>

| Progress    | Task        | Notes   |     
| ----------- | ----------- | -----------   |
| 🟢 |Implement Unity and be able to call functions|    |
| ⚫ |Full screen on Unity startup|  web.Js doesnt allow calls to  make applications full screen  |
| 🟢 |Send transaction updates|    |
| 🟢 |Send address data on connect|    |
| 🟣 |Block game if the wallet is not connected or account is switched|  contacted devs and they have opened a ticket  |
| 🟢 |Connect argent wallet|    |
| 🟣⚫ |Connect braavos wallet|  this is broken and probably wont be implemented in the final stage  |
| 🟣 |Disconnect wallet voluntarily |  contacted devs and they have opened a ticket  |
| 🔵 |Turn array from cairo to json to be sent to unity for troops|    |
| 🟢 |Handle view functions|    |
| 🟢 |Handle uint256 values|    |
| 🟢 |Add token to wallet via code|    |
| 🟢 |Add Util script|    |
| 🟢 |Add encryption and decryption|    |
| 🟢 |Multicall for the deckDataSet|    |
| 🟠 |Add contract 1|    |
| 🔴 |Add contract 2|    |
| 🔵 |Add contract 3|    |
| 🟠 |On contract 1 deduct fee for the contract to keep|    |
| 🔴 |Deploy Website somewhere|  |


<br/>
Additional Notes:  <br/>
Open issue on the starknet react github for the braavos wallet <br/>
implement the starknet ID  or look into it<br/>
Other usefull links related to this project:


<br/><br/>
----------------------------------- UNITY PROJECT (Last full code clean up and commenting 25/06/22) ----------------------------------------
<br/>

| Progress    | Task        | Notes   |     
| ----------- | ----------- | -----------   |
| ⚫ |Autoconnect on game startup if server is available | the first scene will be used as a landing page for the game/website so no autoconnect |
| 🔵 |Offline scene finished|  |
| 🟢 |Receive address data on connect|  |
| 🟠 |change from the playerprefs or put ifend regions int he code | the way that saved data is stored in between scenes is not a permanent way, if anything use react backend to store data inbetween scenes |
| 🔵 |Main util script to be accessed from everywhere|  |
| 🟢 |Check if two of the same players exist in the server if so kick|  |
| 🟠 |Implement keys used for encryption|    |
|  ******  | ****** |  ******  |
| 🟢 |Host game menu section|  |
| 🟢 |join game menu section|  |
| 🔵 |Deck building menu section|  |
| 🟢 |Loading menu section|  |
| 🟢 |Setting menu section|  |
| 🟠 |Contract view menu section| this menu is a mess  |
| 🟢 |Receive transaction updates|  |
| 🔵 |Finish the menu UI| check the contract menu and have the final UI in place |
| 🟢 |Show all availabe games|  |
| 🟢 |Basics of matchmaking and player made lobbies|  |
| 🟢 |Webhook to discord to be used as a database|  |
| 🟠 |Send webhooks to discord on starting lobby and joining lobby| all implemented in the Util script, just need to set up the lobby the correct way |
| 🟢 |Pop up error UI|  |
| 🟢 |Sorting algos for the various menus|  |
| 🔴 |Basic all roudn progression checks| example: the player is able to join a lobby without selecting a team, should not be allowed |
|  ******  | ****** |  ******  |
| 🟢 |Basics of RealmsUI |  |
| 🟢 |Basics of troopsUI|  |
| 🟠 |Basics of adventurerUI|  |
| 🔵 |Tooltip on hover over units and realms| core logic is done just needs to be implemented everywhere |
| 🟢 |Able to select the realms by looking for their ID|  |
| 🔵 |Player is able to make its team and save it to be then used in game| if the player goes back into the deckmenu there are errors, probably issues with references |
| 🔴 |Receive data from NFT|  |
| 🔴 |Lobby exists until the original host goes|  |
| 🔵 |Write data to Database account troops contract|  |
| ⚫ |Implement a resource folder so every prefab is available there in conjunction with the generalUtil script |  |
|  ******  | ****** |  ******  |
| 🔵 |function to update the player ont he server side with the client side data| use the specific targetRPC example to improve on the efficiency of the server calls |
| 🔴 |divide the game into different states/rounds|  |
| 🟢 |Fix the names so they show in the lobby|  |
| 🟠 |Connect the skirmish main contract to the game |  |
| ⚫ |Only allowed to start the game after both players are ready|  |
| 🔵 |Turn based functionality setup| there but not implemented with the card placing  |
| 🔵 |Once the game starts send data to server so both clients can communicate| this is implemented but for now only works with a button, should be called at the start of the scene |
| 🔵 |Once a player places a card replicate action on the other client| cards do appear on the other client but issue thrown, something along the lines of missing reference and its not turn based yet |
| 🔵 |Prohibit client from interacting with the other client's card| should be implemented but not tested |
| 🟠 |Add basic game score mechanic | score mechanic is there but for some reason only works on the first call, probable issue with the detection of child objects |
| 🟠 |Add basic server checks in the middle of moves to validate moves| previous states of the deck and possible cards are all stored in the turnmanager, just need to call it to compare so no "added" cards via exploits are possible |
| 🔴 |Before the start of the game check the deck is valid| same as above  ^^^^^^^^^^^^^^^^^^^ |
| 🔴 |Deal with the outcome of the match| there are no turns states implemented yet |
| 🟠 |Deal with instances from either players disconnecting early or server failure|  |
| 🔴 |Deploy mock server on AWS|  |

<br/>
Additional Notes:<br/>


Other usefull links related to this project:


- - - -


### MORE COMING....

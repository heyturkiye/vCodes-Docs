Welcome to the documentation for the vCodes API, Here you can learn how to use our API using an endpoint or our NPM Module!

# NPM Module
This part of the documentation goes through how to use our NPM Module, You can install it with the following command:
```
npm i vcodes.js --save
```
Alternatively, You can use YARN to download the module:
```
yarn add vcodes.js
```
# Defining The Module
Use this code to define the module within your setup:
```
const vCodes = require('vcodes.js');
const dbl = new vCodes("vCodes Bot Token");
```
Replace the vCodes Bot Token with your vCodes Bot Token found on your bot edit page at [vCodes.xyz](https://vcodes.xyz)

# Events
Certain events can be run on your setup using our NPM Module

## Ready Event
Find a certain bot on vCodes with this code
```
dbl.on("ready", (bot) => {
    console.log(`Bot named ${bot.username} successfully found on vCodes.`)
})

// => Bot named Allegro successfully found on vCodes.
```
## Vote Event
When someone votes for your bot on vCodes, Run some actions
```
dbl.on("vote", ({ user }) => {
    console.log(`${user.username} has voted for your bot on vCodes.`)
})

// => clqu has voted for your bot on vCodes.
```
If you want to see the bot's username, Use this:
```
dbl.on("vote", ({ user, bot }) => {
    console.log(`${user.username} has voted for your bot ${bot.username} on vCodes.`)
})

// => clqu has voted for your bot Allegro on vCodes.
```
# Statistics
Post your bots server count & shard count using this code
```
dbl.on("ready", (bot) => {
    console.log(`Bot named ${bot.username} successfully found on vCodes.`)
    let guildCount = 123;
    let shardCount = 123;
    dbl.stats(guildCount, shardCount, () => console.log("Stats updated for your bot on vCodes."));
})

// => Bot named Allegro successfully found on vCodes.
// => Stats updated for your bot on vCodes.
```
# Vote Checking
Check if a user has voted for your bot on vCodes
```
dbl.on("ready", (bot) => {
    console.log(`Bot named ${bot.username} successfully found on vCodes.`)
    dbl.checkVote("714451348212678658").then(value => console.log("Vote Control: "+ value))

    /*
        let guildCount = 1234;
        let shardCount = 5;
        dbl.stats(guildCount, shardCount, () => console.log("Stats updated on vCodes."));
    */
})

// => Bot named Allegro successfully finded on vCodes.
// => Vote Control: false
```
# Endpoints
Welcome to the part which doesn't use our NPM Module

# Reference
## Base URL
```
https://api.vcodes.xyz
```
## Versions
| Version   |      Status      |  Default |
|----------|:-------------:|------:|
| 1 |  Available | ✔️ |
    

    

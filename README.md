**NPM:** [npmjs.com/package/list-discordtownshop-com](https://www.npmjs.com/package/list-discordtownshop-com/)<br>



<a href="https://nodei.co/npm/list-discordtownshop-com"><img src="https://nodei.co/npm/listing-dtl-api.png?downloads=true&stars=true" alt="npm installnfo" /></a>


## Installation
*If you have trouble with the installation, please feel free to visit our [discord](https://discord.gg) address.*
- `npm i listing-dtl-api`

#### 1. Where can I get list.discordtownshop.com api?
  Ans: [JavaScript](https://www.npmjs.com/package/listing-dtl-api)
            

#### 2. How do I install it?
  Ans: JavaSciprt: npm i listing-dtl-api or npm install listing-dtl-api
          

#### 3. Does it have any GitHub Repository?
 Yes

#### 4. What is it's uses?
  Ans: To get the daily vote count, server count and information about your bot.
Examples:  avatar, botID, discriminator, shortDescription, prefix, votes, serverCount, ownerID, owner, co-owners, tags, longDescription, certificate etc.

#### 5. How can I get my bot's server count?
  `Ans: JavaScript:`
```js
const list = require("list-discordtownshop-com");
const dbl = new list("TOKEN-HERE", client);

client.on("ready", async () => {
  dbl.serverCount();
  console.log("Server count posted")
```

#### 6. How can I get my bot's vote count?
  `Ans:`
```js
let hasVote = await dbl.hasVoted("Your-bot-id");
  if(hasVote === true) {
    console.log("Voted")
  } else {
    console.log("Vote please.")
  }
  
  
  let search = await dbl.search("Your-bot-id")
  console.log(search)

```

#### 7. Full Example?
  `Ans:`
```js
const list = require("list-discordtownshop-com");
const dbl = new list("TOKEN-HERE", client);

client.on("ready", async () => {
  dbl.serverCount();
  console.log("Server count posted")
  
  let hasVote = await dbl.hasVoted("your-bot-id");
  if(hasVote === true) {
    console.log("Voted")
  } else {
    console.log("Vote please.")
  }
  
  
  let search = await dbl.search("listing-dtl-api")
  console.log(search)

  /* SearchResults
  {
    avatar: '',
    botID: '',
    username: '',
    discrim: '',
    shortDesc: '',
    prefix: '? [changable]',
    votes: 25,
    ownerID: '',
    owner: '',
    coowners: [ '' ],
    tags: [ 'Moderation', 'NSFW', 'Music' ],
    longDesc: longDesc,
    certificate: 'Certified'
  }
  */
});

```

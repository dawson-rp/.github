> Quick note: not all repositories here will be immediately available: I'm currently in the process of redacting identifiable information from the bots, but this will take some time.

# MINGLETON RPG
> A Discord-based RPG game developed by @zaccomode & @BenSaunders1.

This is essentially a custom recreation of popular Discord RPG bots that uses our own custom mechanics, items and currency. It was run on the Mingleton Discord server from April-September 2022, and is now open source because it is no longer in active development or usage. 
The entire RPG was built around a somewhat stable currency known as sussbuccs (internally: Dollars), with other mechanics such as gambling, item purchasing and combat to back it up.

Everything here is provided as-is; modification **will** be required to restore functionality to this project. Below is a high-level outline of the project, but will not describe the inner workings of every component.

## Functionality
Everything in the RPG reports directly to the REST [Master API](https://github.com/dawson-rp/master-api), which stored all information in a PostgreSQL database, all hosted on Heroku (the changes to Heroku's free plan is the reason this project is no longer developed). 
Each bot was then hosted independently and focused on individual aspects of the RPG.

## Bots
### Jimothy (master)
[Source code](https://github.com/dawson-rp/master-bot) | @zaccomode
The master bot for the Mingleton RPG that handled inventory management, profile viewing, factions, etc.

### Casino Royale (Casino bot)
[Source code](https://github.com/dawson-rp/casino-bot) | @zaccomode
Used the currency of the Mingleton RPG to create a text-based casino. Featured a coinflip and Blackjack game modes with wagers, etc.

### Bruh United (Store bot)
[Source code](https://github.com/dawson-rp/store-bot) | @zaccomode
Used Sussbuccs to allow users to purchase randomly-generated items. Items were generated had different types, rarities and statistics that were all randomly generated within defined ranges. A more detailed description of each can be found in the README of the repository.

### Baunders and Sons (Alternative store bot)
[Source code] | @BenSaunders1
Another store bot that interacted with the same Items API, but used a different item generation method to produce far more and more varied items.
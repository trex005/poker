# Poker &nbsp; &nbsp; [Demo](https://trexpoker.herokuapp.com/)
Simple poker application running on node.js
1. Front-end: AngularJS
2. Communication between front-end and server: socket.io
3. Database PostgreSQL (works without configuration on heroku)
## Requirements
Node & Yarn
## Instalation
    yarn
    yarn dev
Then should be available at http://localhost:8080

The first time each user logs in, their username and password will be securly saved to the database. Their available chips will be tracked along with a lifetime balance.
## Config
Edit the `tables-config.json` file to add or remove tables to play on
## Serverside
    node app.js
## Changelog
### 1.0.1 (2020-06-10)
* Add user tracking, including adding passwords, tracking bankroll and lifetime balance.
* Add sound when it is user's turn
* Add shuffle sound when new hand is being dealt
* Add `tables-config.json` option for users to automatically post blinds
* Prevent cards from wrapping on table
## TODO
* Add Time Limit option per table
* Add ability for users to reset password (will require an email address)
* Add Admin abilities:
  * Give players additional chips which will deduct it from lifetime balance.
  * Modify players' lifetime balance
* Add gameplay checkboxes:
  * Fold on your turn.
  * Call current bet.
Will be unavailable for 1.5 seconds after each raise to prevent accedentle calls of larger amounts.
  * Call any bet.
  * Automatically post blinds
Will be unavailable if table is set to post blinds automatically.
  * Sit out next hand.
 * Add play and bank time options to `tables-config.json`
* Add Rabbit Feature
* Add buttons for pot/half pot bet.
* Make work with ANY screen size
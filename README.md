
<p align="center">
    <a href="#"><img src="https://i.imgur.com/XXdD3AH.png" /></a>
    <br />
    <br />
    <a href="https://discord.gg/hRWra7r"><img alt="Discord" src="https://img.shields.io/discord/567034368002883594.svg?label=Discord&style=for-the-badge"></a>
    <a href="https://github.com/timedotcc/dlivetv-unofficial-api/blob/master/LICENSE"><img alt="GitHub" src="https://img.shields.io/github/license/timedotcc/dlivetv-unofficial-api.svg?style=for-the-badge"></a>
    <a href="https://nodei.co/npm/dlivetv-unofficial-api/"><img alt="npm" src="https://img.shields.io/npm/v/dlivetv-unofficial-api.svg?style=for-the-badge"></a>
    <a href="https://beerpay.io/timedotcc/dlivetv-unofficial-api"><img alt="Beerpay" src="https://img.shields.io/beerpay/timedotcc/dlivetv-unofficial-api.svg?label=Donate&style=for-the-badge"></a>
	<a href="#"><img alt="Codecov" src="https://img.shields.io/codecov/c/github/timedotcc/dlivetv-unofficial-api.svg?style=for-the-badge&token=7f6ffc31-4a5b-440e-acdd-fdb8327e40e7"></a>
    <br />
    <br />
    <a href="https://nodei.co/npm/dlivetv-unofficial-api/"><img src="https://nodei.co/npm/dlivetv-unofficial-api.png?compact=true"></a>
</p>

## Example
```js
let dlive = require('dlivetv-unofficial-api');

// Parameter 1: the channel name / blockchain username
// Parameter 2: Your access key for sending messages

let example1 = new dlive('pdp', 'abc');  // Joining PewDiePie
let example2 = new dlive('dlive-12278051', 'abc');  // Joining sampepper

example1.on('ChatText', (message) => {
    console.log(`Messages in Channel ${example1.getChannel}: ${message.content}`);
});

example2.sendMessage('Hello! Its me, a bot.');

example2.on('ChatText', (message) => {
    console.log(`Messages in Channel ${example2.getChannel}: ${message.content}`);
});
example2.on('ChatFollow', (message) => {
    // Say thanks to this user for his follow!
    example2.sendMessage(`Thanks for the follow, @${message.sender.displayname}`);
});
example2.on('ChatGift', (message) => {
    // Say thanks to this user for his gift!
    example2.sendMessage(`Thanks for ${message.amount}x ${message.gift}, @${message.sender.displayname}`);
});
```
## Todo

 - Message types:
     - [X] ChatText
	 - [X] ChatFollow
	 - [X] ChatGift
	 - [X] ChatDelete
- [X] Send messages
- [X] Get channel informations

## Examples and functions
	 
More [examples](https://github.com/timedotcc/dlivetv-unofficial-api/wiki/Examples) and [functions](https://github.com/timedotcc/dlivetv-unofficial-api/wiki/Functions) can you find in our [wiki](https://github.com/timedotcc/dlivetv-unofficial-api/wiki).

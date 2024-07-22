<h1 class="title">Massroom Docs</h1>

<a class="button" href="/">Back to Main</a>

Welcome to the Massroom Docs! Here you'll find everything you'll need to know about massroom, and building chatbots with pure vanilla js.

We also document our code here, all of it can be found in our [GitHub Repo](https://github.com/Massroom/massroom.github.io/).

---

## Source Code Documentation:

Massroom's core messaging system uses [Xano's](https://xano.com) realtime Websocket system. The frontend was by us.

### Message Displaying

To display messages, you can use the `displayMessages(message)` to input a message right before the end of the `messageList` HTML `<div>`.

eg.

```javascript
var clientMessage;

// code to handle message generation

displayMessage(clientMessage);
```

### Sending Messages

Uses Xano's API to send messages, this is considered a `public` message. All subscribed users **will** see this message, if you are making a chatbot, **do NOT** send account info over this method.

eg.

```javascript
var clientSendMessage
// use mainChannel to support the MAIN CHATROOM. Private chatrroms are currently broken.

mainChannel.message(clientSentMessage);
```

---

## Chat Commands Documentation:

#### Help Utility Commands

`/help` :
Gives a list of commands you can use. Bot reply is **private**.

`/help about`:
Returns the about us for Massroom. Bot reply is **private**.

`/ help text`:
Returns a small guide on how to send HTML over the input bar. Bot reply is **private**.

`/help account`:
Returns your account details without having to navigate to your dashboard. Bot reply is **private**.
If you aren't signed in, the Bot will not return any account details.

`/help faq`:
Still being worked on.

#### AI Chat Commands

`/ai ask *question here*` :
Returns a response from the AI. Bot reply is **private**.

`/ai story *story topic here*` :
Returns a story from the AI. Bot reply is **private**.

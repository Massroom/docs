<h1 class="title">Massroom Docs</h1>

<a class="button" href="/">Back to Main</a>

Welcome to the Massroom Docs! Here, you'll find comprehensive resources for building chatbots with pure vanilla JS and understanding massroom's functionality.

<table class="toc">
<tr>
<th>Table of Contents</th>
</tr>
<tr>
<td><a href="#source-code-documentation">Source Code Documentation</a></td>
</tr>
<tr>
<td><a href="#chat-commands-documentation">Chat Commands Documentation</a></td>
</tr>
<tr>
<td><a href="#chatbot-documentation">Chatbot Documentation</a></td>
</tr>
</table>

## Source Code Documentation

Massroom's core messaging system utilizes Xano's realtime Websocket system, with a custom-built frontend.

This can help you when building chatbots in Massroom.

### Message Displaying

Use the `displayMessages(message)` function to display messages in the `messageList` HTML `<div>`. For example:
```javascript
var clientMessage;
// code to handle message generation
displayMessage(clientMessage);
```

### Sending Messages

Leverage Xano's API to send messages, considered public messages visible to all subscribed users. Note that sensitive information, like account details, should not be sent via this method. For example:
```javascript
var clientSendMessage;
mainChannel.message(clientSentMessage);

// use mainChannel for the main
chatroom
```

## Chat Commands Documentation

### Help Utility Commands

- `/help`: Lists available commands (private bot reply)
- `/help about`: Returns the about us section for Massroom (private bot reply)
- `/help text`: Provides a guide on sending HTML over the input bar (private bot reply)
- `/help account`: Displays account details without navigating to the dashboard (private bot reply)
- `/help faq`: Currently under development

### AI Chat Commands

- `/ai ask *question here*`: Returns a response from the AI (private bot reply)
- `/ai story *story topic here*`: Generates a story from the AI (private bot reply)

## Chatbot Documentation

Here you'll find a quick-start guide on creating your very own Massroom Chatbots!
First, you'll need a Github account if you don't already have one, then head to our Github Repo and fork it. Under the directory `/js/bots/` create a file and give it a name that represents your bot, it must be in camelCase.

### Initialising the Chatbot

There are many ways to init a chatbot but the most common one is when a user clicks the send button. 
You'll need to assign a variable to the input value too!
An example is shown below:

```javascript
// init bot
sendButton.addEventListener('click', () => {
  console.log('bot ready');
  const message = messageInput.value; // get input value
  };
});
```

### Checking for a specific Command

#### Static Command (eg. /help)

Assuming you've stored input value as `message`, eg:

```javascript
// inside the event listener
if (message === '/command') {
  // do something
}
```

#### Dynamic Command (eg. /ai ask *input*)

Assuming you've stored input value as `message`, eg:

```javascript
if (message.startsWith('/command text')) {
    const text = message.slice('/command text'.length).trim();; // slice off the front part
    // do something
  };
```

### Registering a Chatbot

Now with the fork you have of our repo, simply open a Pull Request for that branch and after review (up to 7 days), we will merge the PR and your bot will be in Massroom!

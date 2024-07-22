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
<td><a href="#message-displaying">Message Displaying</a></td>
</tr>
<tr>
<td><a href="#sending-messages">Sending Messages</a></td>
</tr>
<tr>
<td><a href="#chat-commands-documentation">Chat Commands Documentation</a></td>
</tr>
<tr>
<td><a href="#help-utility-commands">Help Utility Commands</a></td>
</tr>
<tr>
<td><a href="#ai-chat-commands">AI Chat Commands</a></td>
</tr>
</table>

## Source Code Documentation

Massroom's core messaging system utilizes Xano's realtime Websocket system, with a custom-built frontend.

This can help you when building chatbots in Massroom.

### Message Displaying

Use the `displayMessages(message)` function to display messages in the `messageList` HTML `<div>`. For example:
```
var clientMessage;
// code to handle message generation
displayMessage(clientMessage);
```

### Sending Messages

Leverage Xano's API to send messages, considered public messages visible to all subscribed users. Note that sensitive information, like account details, should not be sent via this method. For example:
```
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


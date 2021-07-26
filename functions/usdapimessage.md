# $apiMessage
------------
## Description
```js
"sends a Message using raw discord api"
```
------------
## Status
```js
"BETA"
```
------------
## Usage
```js
"$apiMessage[content;embed;component;referenceMessageID:mentionTheUser(true/yes/false/no);return Id(yes/no)]"
```
-------------
## Fields

### Content
> ```js
> "sends the normal message"
> ```

### Embed
> ```js
> "sends the embedded message"
> ```
>**Note**:
>
> This uses embed-errors in their full form.
>
> example: {author:hi} won't work but {author:hi::} will
>
> available ones are same as in [interactionReply](./usdinteractionreply.md#embed)
>
> Color only supports hex code and int for now.
### Components
> Same as in [interactionReply](./usdinteractionreply.md#components)

### Reference 
> ```js
> "This is for replying to the user"
> ```
> **Format:** messageID:mentionTheUser(true/false)

### ReturnID
> ```js
> "returns the id of the message sent"
> ```
--------------

## Example
```js
bot.command({
name:"hi",
code:`
$apiMessage[hi;{author:hi::}{title:hello}{field:ok:lol:no}{color:#8700ff}{footer:hmmm:$authorAvatar};;$messageID:true;no]
`
})
```
--------------
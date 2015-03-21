iMessenger is a IM SDK / library for .Net, written in managed C# dedicated to .NET, Support XMPP(eXtensible Messaging and Presence Protocol).


---


```
using (Client client = XmppClient.Create(IP, PORT)) {
    client.RegisterReceiver(message => {
        if (message is ChatMessage) {
            Content content = (message as ChatMessage).Content;
            // todo ...

        } else if (message is RosterMessage) {
            Roster roster = (message as RosterMessage).Roster;
            // todo ...

        }
        // todo ...

    });

    Messenger messenger = new Messenger();
    messenger.Login(JID, PASSWORD, client);
    messenger.Send(TEXT, JID);
    messenger.Send(IMAGE, JID);
    messenger.Send(FILE, JID);
    // todo ...

    messenger.Send(CONTENT, JID);
    messenger.Send(MESSAGE, JID);
    messenger.Send(BYTES, JID);

    client.Close();
}
```



---

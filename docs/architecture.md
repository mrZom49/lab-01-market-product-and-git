## Product Choice

- Telegram
- <https://telegram.org/>
- Telegram is a simple, private online messanger

## Main components

![Telegram Component Diagram](diagrams/out/telegram/component-diagram/Component%20Diagram.svg)
[Telegram Component Diagram](diagrams\src\telegram\component-diagram.puml)

- Mobile App is probably the most used one. It gives people the ablility to text on the go.
- Auth & Session Service is used logging into accounts, and remembering sessions
- Media & File Service is in charge of media and file sharing on telegram
- Bot API Server allow for bots on telegram
- Web Client is for people who dont want to download the app

## Data flow

![Telegram Sequence Diagram](diagrams/out/telegram/sequence-diagram/Sequence%20Diagram.svg)
[Telegram Sequence Diagram](diagrams\src\telegram\sequence-diagram.puml)

### 3. Event Propogation (Fan-Out)

- Publish Event (NewMessageUpdate)
- Consume (Sync To Online Devices)
- Update UI (Double Tick if read)

In this group events such as sending a message or reading one sync on all devices\
It talks to mobile app, message service, kafka event box

## Deployment

![Telegram Deployment Diagram](diagrams/out/telegram/deployment-diagram/Deployment%20Diagram.svg)
[Telegram Deployment Diagram](diagrams\src\telegram\deployment-diagram.puml)\
Apps, API, Services and other

## Assumptions

- I assume Telegram is secure due to double cipher
- I assume internal infrastructure is complicated

## Open questions

- How messages are ciphered?
- How secret chats block screenshots

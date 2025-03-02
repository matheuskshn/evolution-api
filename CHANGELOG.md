# 1.5.3 (2023-10-06 18:55)

### Feature

* Swagger documentation
* Added base 64 sending option via webhook

### Fixed

* Remove rabbitmq queues when delete instances
* Improvement in restart instance to completely redo the connection
* Update node version: v20
* Correction of messages sent by the api and typebot not appearing in chatwoot
* Adjustment to start typebot, added startSession parameter
* Chatwoot now receives messages sent via api and typebot
* Fixed problem with starting with an input in typebot
* Added check to ensure variables are not empty before executing foreach in start typebot

# 1.5.2 (2023-09-28 17:56)

### Fixed

* Fix chatwootSchema in chatwoot model to store reopen_conversation and conversation_pending options
* Problem resolved when sending files from minio to typebot
* Improvement in the "startTypebot" method to create persistent session when triggered
* New manager for Evo 1.5.2 - Set Typebot update
* Resolved problems when reading/querying instances

# 1.5.1 (2023-09-17 13:50)

### Feature

* Added listening_from_me option in Set Typebot
* Added variables options in Start Typebot
* Added webhooks for typebot events
* Added ChamaAI integration
* Added webhook to send errors
* Added support for messaging with ads on chatwoot

### Fixed

* Fix looping connection messages in chatwoot
* Improved performance of fetch instances

# 1.5.0 (2023-08-18 12:47)

### Feature

* New instance manager in /manager route
* Added extra files for chatwoot and appsmith
* Added Get Last Message and Archive for Chat
* Added env var QRCODE_COLOR
* Added websocket to send events
* Added rabbitmq to send events
* Added Typebot integration
* Added proxy endpoint
* Added send and date_time in webhook data

### Fixed

* Solved problem when disconnecting from the instance the instance was deleted
* Encoded spaces in chatwoot webhook
* Adjustment in the saving of contacts, saving the information of the number and Jid
* Update Dockerfile
* If you pass empty events in create instance and set webhook it is understood as all
* Fixed issue that did not output base64 averages
* Messages sent by the api now arrive in chatwoot

### Integrations

- Chatwoot: v2.18.0 - v3.0.0
- Typebot: v2.16.0
- Manager Evolution API

# 1.4.8 (2023-07-27 10:27)

### Fixed

* Fixed error return bug

# 1.4.7 (2023-07-27 08:47)

### Fixed

* Fixed error return bug
* Fixed problem of getting message when deleting message in chatwoot
* Change in error return pattern

# 1.4.6 (2023-07-26 17:54)

### Fixed

* Fixed bug of creating new inbox by chatwoot
* When conversation reopens is pending when conversation pending is true
* Added docker-compose file with dockerhub image

# 1.4.5 (2023-07-26 09:32)

### Fixed

* Fixed problems in localization template in chatwoot
* Fix mids going duplicated in chatwoot

# 1.4.4 (2023-07-25 15:24)

### Fixed

* Fixed chatwoot line wrap issue
* Solved receive location in chatwoot
* When requesting the pairing code, it also brings the qr code
* Option reopen_conversation in chatwoot endpoint
* Option conversation_pending in chatwoot endpoint

# 1.4.3 (2023-07-25 10:51)

### Fixed

* Adjusts in settings with options always_online, read_messages and read_status
* Fixed send webhook for event CALL
* Create instance with settings

# 1.4.2 (2023-07-24 20:52)

### Fixed

* Fixed validation is set settings 
* Adjusts in group validations
* Ajusts in sticker message to chatwoot

# 1.4.1 (2023-07-24 18:28)

### Fixed

* Fixed reconnect with pairing code or qrcode
* Fixed problem in createJid

# 1.4.0 (2023-07-24 17:03)

### Features

* Added connection functionality via pairing code
* Added fetch profile endpoint in chat controller
* Created settings controller
* Added reject call and send text message when receiving a call
* Added setting to ignore group messages
* Added connection with pairing code in chatwoot with command /init:{NUMBER}
* Added encoding option in endpoint sendWhatsAppAudio

### Fixed

* Added link preview option in send text message
* Fixed problem with fileSha256 appearing when sending a sticker in chatwoot
* Fixed issue where it was not possible to open a conversation when sent at first by me on my cell phone in chatwoot
* Now it only updates the contact name if it is the same as the phone number in chatwoot
* Now accepts all chatwoot inbox templates
* Command to create new instances set to /new_instance:{NAME}:{NUMBER}
* Fix in chatwoot set, sign msg can now be disabled

### Integrations

- Chatwoot: v2.18.0 - v3.0.0 (Beta)

# 1.3.2 (2023-07-21 17:19)

### Fixed

* Fix in update settings that needed to restart after updated
* Correction in the use of the api with mongodb
* Adjustments to search endpoint for contacts, chats, messages and Status messages
* Now when deleting the instance, the data referring to it in mongodb is also deleted
* It is now validated if the instance name contains uppercase and special characters
* For compatibility reasons, container mode has been removed
* Added docker-compose files example

### Integrations

- Chatwoot: v2.18.0

# 1.3.1 (2023-07-20 07:48)

### Fixed

* Adjust in create store files

### Integrations

- Chatwoot: v2.18.0

# 1.3.0 (2023-07-19 11:33)

### Features

* Added messages.delete event
* Added restart instance endpoint
* Created automation for creating instances in the chatwoot bot with the command '#inbox_whatsapp:{INSTANCE_NAME}
* Change Baileys version to: 6.4.0
* Send contact in chatwoot
* Send contact array in chatwoot
* Added apiKey in webhook and serverUrl in fetchInstance if EXPOSE_IN_FETCH_INSTANCES: true
* Translation set to default (english) in chatwoot

### Fixed
 
* Fixed error to send message in large groups
* Docker files adjusted
* Fixed in the postman collection the webhookByEvent parameter by webhook_by_events
* Added validations in create instance
* Removed link preview endpoint, now it's done automatically from sending conventional text
* Added group membership validation before sending message to groups
* Adjusts in docker files
* Adjusts in returns in endpoints chatwoot and webhook
* Fixed ghost mentions in send text message
* Fixed bug that saved contacts from groups came without number in chatwoot
* Fixed problem to receive csat in chatwoot
* Fixed require fileName for document only in base64 for send media message
* Bug fix when sending mobile message change contact name to number in chatwoot
* Bug fix when connecting whatsapp does not send confirmation message
* Fixed quoted message with id or message directly
* Adjust in validation for mexican and argentine numbers
* Adjust in create store files

### Integrations

- Chatwoot: v2.18.0

# 1.2.2 (2023-07-15 09:36)

### Fixed

* Tweak in route "/" with version info
* Adjusts chatwoot version

### Integrations

- Chatwoot: v2.18.0

# 1.2.1 (2023-07-14 19:04)

### Fixed

* Adjusts in docker files
* Save picture url groups in chatwoot

# 1.2.0 (2023-07-14 15:28)

### Features

* Native integration with chatwoot
* Added returning or non-returning participants option in fetchAllGroups
* Added group integration to chatwoot
* Added automation on create instance to chatwoot
* Added verbose logs and format chatwoot service

### Fixed

* Adjusts in docker-compose files
* Adjusts in number validation for AR and MX numbers
* Adjusts in env files, removed save old_messages
* Fix when sending a message to a group I don't belong returns a bad request
* Fits the format on return from the fetchAllGroups endpoint
* Adjust in send document with caption from chatwoot
* Fixed message with undefind in chatwoot
* Changed message in path /
* Test duplicate message media in groups chatwoot
* Optimize send message from group with mentions
* Fixed name of the profile status in fetchInstances
* Fixed error 500 when logout in instance with status = close

# 1.1.5 (2023-07-12 07:17)

### Fixed

* Adjusts in temp folder
* Return with event send_message

# 1.1.4 (2023-07-08 11:01)

### Features

* Route to send status broadcast
* Added verbose logs
* Insert allContacts in payload of endpoint sendStatus

### Fixed

* Adjusted set in webhook to go empty when enabled false
* Adjust in store files
* Fixed the problem when do not save contacts when receive messages
* Changed owner of the jid for instanceName
* Create .env for installation in docker

# 1.1.3 (2023-07-06 11:43)

### Features

* Added configuration for Baileys log level in env
* Added audio to mp4 converter in optionally get Base64 From MediaMessage
* Added organization name in vcard
* Added email in vcard
* Added url in vcard
* Added verbose logs

### Fixed

* Added timestamp internally in urls to avoid caching
* Correction in decryption of poll votes
* Change in the way the api sent and saved the sent messages, now it goes in the messages.upsert event
* Fixed cash when sending stickers via url
* Improved how Redis works for instances
* Fixed problem when disconnecting the instance it removes the instance
* Fixed problem sending ack when preview is done by me
* Adjust in store files

# 1.1.2 (2023-06-28 13:43)

### Fixed

* Fixed baileys version in package.json
* Fixed problem that did not validate if the token passed in create instance already existed
* Fixed problem that does not delete instance files in server mode

# 1.1.1 (2023-06-28 10:27)

### Features

* Added group invitation sending
* Added webhook configuration per event in the individual instance registration

### Fixed

* Adjust dockerfile variables

# 1.1.0 (2023-06-21 11:17)

### Features

* Improved fetch instances endpoint, now it also fetch other instances even if they are not connected
* Added conversion of audios for sending recorded audio, now it is possible to send mp3 audios and not just ogg
* Route to fetch all groups that the connection is part of
* Route to fetch all privacy settings
* Route to update the privacy settings
* Route to update group subject
* Route to update group description
* Route to accept invite code
* Added configuration of events by webhook of instances
* Now the api key can be exposed in fetch instances if the EXPOSE_IN_FETCH_INSTANCES variable is set to true
* Added option to generate qrcode as soon as the instance is created
* The created instance token can now also be optionally defined manually in the creation endpoint
* Route to send Sticker

### Fixed

* Adjust dockerfile variables
* tweaks in docker-compose to pass variables
* Adjust the route getProfileBusiness to fetchProfileBusiness
* fix error after logout and try to get status or to connect again
* fix sending narrated audio on whatsapp android and ios
* fixed the problem of not disabling the global webhook by the variable
* Adjustment in the recording of temporary files and periodic cleaning
* Fix for container mode also work only with files
* Remove recording of old messages on sync

# 1.0.9 (2023-06-10)

### Fixed

* Adjust dockerfile variables

# 1.0.8 (2023-06-09)

### Features

* Added Docker compose file
* Added ChangeLog file

# 1.0.7 (2023-06-08)

### Features

* Ghost mention
* Mention in reply
* Profile photo change
* Profile name change
* Profile status change
* Sending a poll
* Creation of LinkPreview if message contains URL
* New webhooks system, which can be separated into a url per event
* Sending the local webhook url as destination in the webhook data for webhook redirection
* Startup modes, server or container
* Server Mode works normally as everyone is used to
* Container mode made to use one instance per container, when starting the application an instance is already created and the qrcode is generated and it starts sending webhook without having to call it manually, it only allows one instance at a time.
# ZetaPush Official Recipes

> This monorepo contains all official recipes

## Overview

Core recipes

- Config
- Room
- File
- Group
- Notification
- Organization
- Role
- User
- Utils
- Whiteboard

Plugin recipes

- User Email

## Documentation

Coming Soon

*No documentation will be provided for these particular macros as using them probably means you're advanced enough with the use of ZetaPush services.*

### Config ###

Config recipe has been created to easily store a global string or object. That's why the api is separated into two parts, `src/api/object` and `src/api/string`. The api verbs are the same for both part, and they consist of :

* get<Type>Config
* list<Type>Config
* remove<Type>Config
* set<Type>Config

Where <Type> is Object or String, depending on the type you want to manipulate. The config recipe will manipulate a Gda table impersonating a global user, and simplify you the use of a shared storage.


### Conversation ###

Conversation recipe, as the name suggests it, is designed for creating a conversation (= a list of messages shared between defined users) and adding/modifying messages in an existing conversation.

* addConversationMessage
* createConversation
* createOneToOneConversation
* getConversation
* getConversationMessageList
* getUserConversationList
* purgeConversationMessageList
* purgeConversationMessage

By using this recipe you will overpass the system of permissions and storage access which will be delegated to the macros listed above.

### File ###

File upload is a specificity of the HDFS storage. When uploading you first need the url where to upload the file. Then the upload is handled by the client, by example with an AJAX request.

* confirmFileUpload
* deleteFileEntry
* getFileEntry
* getFileEntryList
* requestFileUpload

### Group ###

Group recipe offers high level macros to interact with groups, and implements metadata to them. If you need a global group (global means public in this context), you may need Organization recipe.

* createGroup
* deleteGroup
* getGroup
* getGroupList
* getUserGroupList

* addGroupMember
* isMemberOf
* removeGroupMember

### Notification ###

TODO

### Organization ###

An organization is exactly what you need when you would like to have a "global" group where all users are in by default.
On their creation, users will be auto-addded to the organization set as default. You can visualize organizations as specific groups, attributed to a global user.

* createOrganization
* getDefaultOrganization
* setDefaultOrganization
* getOrganization
* getOrganizationList
* getUserOrganizationList

* addOrganizationMember
* removeOrganizationMember

* getUserContactList

### Role ###

Three entities : Member, Permission, Role

TODO

### User ###

Users can be managed from the user recipe. This recipe gives an access to several methods allowing creation of new user and modification of user informations such as the password, the avatar, or custom ones.

`> src/api/avatar`
* updateUserAvatar

`> src/api/password`
* confirmUserPassword
* resetUserPassword
* resetUserPasswordByLogin

`> src/api/user`
* createUser
* getUser
* getUserByLogin
* getUserList
* updateUser

*Without the ByLogin suffix, the current user key (matching __userKey) is used. ByLogin permits to chose the user to impersonate.*

### Utils ###

The utils recipe (used by most of the other recipes) include gestion of three entities : metadata, tags, targets. For each entity, get, remove and set are proposed.
Moreover utils recipe brings common macros and constants you may need such as hashing, mapping, generating uuid, global user, etc...

`> src/api/utils`
* explode
* hash
* implode
* map
* pagination
* reduce
* string
* uuid

`> src/api/<Type>`
* get<Type>
* remove<Type>
* set<Type>

Where <Type> is Metadata, Tags or Targets.

### Whiteboard ###

Whiteboard recipe is closely related to conversation recipe. It brings possibility to attribute a whiteboard to a conversation, which is just a set of objects added and linked to the conversation. Then you will be able to modify or remove these objects with the following methods.

* createWhiteboard

* addWhiteboardObject
* getWhiteboardObjectList
* purgeWhiteboardObjectList
* updateWhiteboardObject



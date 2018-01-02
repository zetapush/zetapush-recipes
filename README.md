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

### Organization ###

An organization is exactly what you need when you would like to have a "global" group where all users are by default.
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


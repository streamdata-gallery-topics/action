---
swagger: "2.0"
x-collection-name: AWS WorkDocs
x-complete: 0
info:
  title: AWS WorkDocs API Describe Document Versions
  version: 1.0.0
  description: Retrieves the document versions for the specified document.
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /?Action=AbortDocumentVersionUpload:
    get:
      summary: Abort Document Version Upload
      description: Aborts the upload of the specified document version that was previously
        initiated by.
      operationId: abortDocumentVersionUpload
      x-api-path-slug: actionabortdocumentversionupload-get
      parameters:
      - in: query
        name: DocumentId
        description: The ID of the document
        type: string
      - in: query
        name: VersionId
        description: The ID of the version
        type: string
      responses:
        200:
          description: OK
      tags:
      - Documents
  /?Action=ActivateUser:
    get:
      summary: Activate User
      description: Activates the specified user.
      operationId: activateUser
      x-api-path-slug: actionactivateuser-get
      parameters:
      - in: query
        name: UserId
        description: The ID of the user
        type: string
      responses:
        200:
          description: OK
      tags:
      - Users
  /?Action=AddResourcePermissions:
    get:
      summary: Add Resource Permissions
      description: Creates a set of permissions for the specified folder or document.
      operationId: addResourcePermissions
      x-api-path-slug: actionaddresourcepermissions-get
      parameters:
      - in: query
        name: ResourceId
        description: The ID of the resource
        type: string
      responses:
        200:
          description: OK
      tags:
      - Permissions
  /?Action=CreateFolder:
    get:
      summary: Create Folder
      description: Creates a folder with the specified name and parent folder.
      operationId: createFolder
      x-api-path-slug: actioncreatefolder-get
      parameters:
      - in: query
        name: Name
        description: The name of the new folder
        type: string
      - in: query
        name: ParentFolderId
        description: The ID of the parent folder
        type: string
      responses:
        200:
          description: OK
      tags:
      - Folders
  /?Action=CreateNotificationSubscription:
    get:
      summary: Create Notification Subscription
      description: Configure WorkDocs to use Amazon SNS notifications.
      operationId: createNotificationSubscription
      x-api-path-slug: actioncreatenotificationsubscription-get
      parameters:
      - in: query
        name: OrganizationId
        description: The ID of the organization
        type: string
      responses:
        200:
          description: OK
      tags:
      - Notifications
  /?Action=CreateUser:
    get:
      summary: Create User
      description: Creates a user in a Simple AD or Microsoft AD directory.
      operationId: createUser
      x-api-path-slug: actioncreateuser-get
      parameters:
      - in: query
        name: GivenName
        description: The given name of the user
        type: string
      - in: query
        name: OrganizationId
        description: The ID of the organization
        type: string
      - in: query
        name: Password
        description: The password of the user
        type: string
      - in: query
        name: StorageRule
        description: The amount of storage for the user
        type: string
      - in: query
        name: Surname
        description: The surname of the user
        type: string
      - in: query
        name: TimeZoneId
        description: The time zone ID of the user
        type: string
      - in: query
        name: Username
        description: The login name of the user
        type: string
      responses:
        200:
          description: OK
      tags:
      - Users
  /?Action=DeactivateUser:
    get:
      summary: Deactivate User
      description: Deactivates the specified user, which revokes the user's access
        to Amazon WorkDocs.
      operationId: deactivateUser
      x-api-path-slug: actiondeactivateuser-get
      parameters:
      - in: query
        name: UserId
        description: The ID of the user
        type: string
      responses:
        200:
          description: OK
      tags:
      - Users
  /?Action=DeleteDocument:
    get:
      summary: Delete Document
      description: Permanently deletes the specified document and its associated metadata.
      operationId: deleteDocument
      x-api-path-slug: actiondeletedocument-get
      parameters:
      - in: query
        name: DocumentId
        description: The ID of the document
        type: string
      responses:
        200:
          description: OK
      tags:
      - Documents
  /?Action=DeleteFolder:
    get:
      summary: Delete Folder
      description: Permanently deletes the specified folder and its contents.
      operationId: deleteFolder
      x-api-path-slug: actiondeletefolder-get
      parameters:
      - in: query
        name: FolderId
        description: The ID of the folder
        type: string
      responses:
        200:
          description: OK
      tags:
      - Folders
  /?Action=DeleteFolderContents:
    get:
      summary: Delete Folder Contents
      description: Deletes the contents of the specified folder.
      operationId: deleteFolderContents
      x-api-path-slug: actiondeletefoldercontents-get
      parameters:
      - in: query
        name: FolderId
        description: The ID of the folder
        type: string
      responses:
        200:
          description: OK
      tags:
      - Folders
  /?Action=DeleteNotificationSubscription:
    get:
      summary: Delete Notification Subscription
      description: Deletes the specified subscription from the specified organization.
      operationId: deleteNotificationSubscription
      x-api-path-slug: actiondeletenotificationsubscription-get
      parameters:
      - in: query
        name: OrganizationId
        description: The ID of the organization
        type: string
      - in: query
        name: SubscriptionId
        description: The ID of the subscription
        type: string
      responses:
        200:
          description: OK
      tags:
      - Notifications
  /?Action=DeleteUser:
    get:
      summary: Delete User
      description: Deletes the specified user from a Simple AD or Microsoft AD directory.
      operationId: deleteUser
      x-api-path-slug: actiondeleteuser-get
      parameters:
      - in: query
        name: UserId
        description: The ID of the user
        type: string
      responses:
        200:
          description: OK
      tags:
      - Users
  /?Action=DescribeDocumentVersions:
    get:
      summary: Describe Document Versions
      description: Retrieves the document versions for the specified document.
      operationId: describeDocumentVersions
      x-api-path-slug: actiondescribedocumentversions-get
      parameters:
      - in: query
        name: DocumentId
        description: The ID of the document
        type: string
      - in: query
        name: Fields
        description: Specify SOURCE to include initialized versions and a URL for
          the source document
        type: string
      - in: query
        name: Include
        description: A comma-separated list of values
        type: string
      - in: query
        name: Limit
        description: The maximum number of versions to return with this call
        type: string
      - in: query
        name: Marker
        description: The marker for the next set of results
        type: string
      responses:
        200:
          description: OK
      tags:
      - Documents
x-streamrank:
  polling_total_time_average: 0
  polling_size_download_average: 0
  streaming_total_time_average: 0
  streaming_size_download_average: 0
  change_yes: 0
  change_no: 0
  time_percentage: 0
  size_percentage: 0
  change_percentage: 0
  last_run: ""
  days_run: 0
  minute_run: 0
---
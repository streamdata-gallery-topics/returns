---
swagger: "2.0"
x-collection-name: MySpace Developers
x-complete: 0
info:
  title: My Space Get Statusmood Personid Selector Friendid History
  description: Returns History Friend.
  version: 1.0.0
host: api.myspace.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /1.0/statusmood/{personId}/{selector}:
    get:
      summary: Get Statusmood Personid Selector
      description: Returns a status for User.
      operationId: 1.0.statusmood.personId.selector.get
      x-api-path-slug: 1-0statusmoodpersonidselector-get
      parameters:
      - in: query
        name: count
        description: Only returns the nearest multiple of 3 compared to the original
          value
      - in: query
        name: fields
        description: The following field names are supported
      - in: query
        name: filterBy
        description: 'See: http://wiki'
      - in: query
        name: filterOp
        description: 'See: http://wiki'
      - in: query
        name: filterValue
        description: 'See: http://wiki'
      - in: query
        name: format
        description: Determines the format of the response
      - in: path
        name: personId
        description: The persons identifier
      - in: path
        name: selector
        description: Indicates which set of individuals to query for activities
      - in: query
        name: startIndex
        description: Indicates the index of the first item to retrieve from the query
          set
      responses:
        200:
          description: OK
      tags:
      - Statusmood
      - People
      - Selector
  /1.0/statusmood/{personId}/{selector}/history:
    get:
      summary: Get Statusmood Personid Selector History
      description: Returns History User.
      operationId: 1.0.statusmood.personId.selector.history.get
      x-api-path-slug: 1-0statusmoodpersonidselectorhistory-get
      parameters:
      - in: query
        name: count
        description: Only returns the nearest multiple of 3 compared to the original
          value
      - in: query
        name: fields
        description: The following field names are supported
      - in: query
        name: filterBy
        description: 'See: http://wiki'
      - in: query
        name: filterOp
        description: 'See: http://wiki'
      - in: query
        name: filterValue
        description: 'See: http://wiki'
      - in: query
        name: format
        description: Determines the format of the response
      - in: path
        name: personId
        description: The persons identifier
      - in: path
        name: selector
        description: Indicates which set of individuals to query for activities
      - in: query
        name: startIndex
        description: Indicates the index of the first item to retrieve from the query
          set
      responses:
        200:
          description: OK
      tags:
      - Statusmood
      - People
      - Selector
      - History
  /1.0/statusmood/{personId}/{selector}/{friendId}:
    get:
      summary: Get Statusmood Personid Selector Friendid
      description: Returns a status for Friend.
      operationId: 1.0.statusmood.personId.selector.friendId.get
      x-api-path-slug: 1-0statusmoodpersonidselectorfriendid-get
      parameters:
      - in: query
        name: count
        description: Only returns the nearest multiple of 3 compared to the original
          value
      - in: query
        name: fields
        description: The following field names are supported
      - in: query
        name: filterBy
        description: 'See: http://wiki'
      - in: query
        name: filterOp
        description: 'See: http://wiki'
      - in: query
        name: filterValue
        description: 'See: http://wiki'
      - in: query
        name: format
        description: Determines the format of the response
      - in: path
        name: friendId
        description: Is the same as {personId}, but for the persons friend
      - in: path
        name: personId
        description: The persons identifier
      - in: path
        name: selector
        description: Indicates which set of individuals to query for activities
      - in: query
        name: startIndex
        description: Indicates the index of the first item to retrieve from the query
          set
      responses:
        200:
          description: OK
      tags:
      - Statusmood
      - People
      - Selector
      - FriendId
  /1.0/statusmood/{personId}/{selector}/{friendId}/history:
    get:
      summary: Get Statusmood Personid Selector Friendid History
      description: Returns History Friend.
      operationId: 1.0.statusmood.personId.selector.friendId.history.get
      x-api-path-slug: 1-0statusmoodpersonidselectorfriendidhistory-get
      parameters:
      - in: query
        name: count
        description: Only returns the nearest multiple of 3 compared to the original
          value
      - in: query
        name: fields
        description: The following field names are supported
      - in: query
        name: filterBy
        description: 'See: http://wiki'
      - in: query
        name: filterOp
        description: 'See: http://wiki'
      - in: query
        name: filterValue
        description: 'See: http://wiki'
      - in: query
        name: format
        description: Determines the format of the response
      - in: path
        name: friendId
        description: Is the same as {personId}, but for the persons friend
      - in: path
        name: personId
        description: The persons identifier
      - in: path
        name: selector
        description: Indicates which set of individuals to query for activities
      - in: query
        name: startIndex
        description: Indicates the index of the first item to retrieve from the query
          set
      responses:
        200:
          description: OK
      tags:
      - Statusmood
      - People
      - Selector
      - FriendId
      - History
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
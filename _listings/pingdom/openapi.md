swagger: "2.0"
x-collection-name: Pingdom
x-complete: 1
info:
  title: Traceroute API
  description: the-traceroute-api-
  version: 1.0.0
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  ? |2-

        /api/{version}/analysis/{checkid}
  : ? |2-

          get
    : summary: Get Root Cause Analysis Results List
      description: Returns a list of the latest root cause analysis results for a
        specified check.
      operationId: get-root-cause-analysis-results-list
      x-api-path-slug: apiversionanalysischeckid-get
      parameters:
      - in: query
        name: from
        description: Return only results with timestamp of first test greater or equal
          to this value
        type: <td>integer</td>
      - in: query
        name: limit
        description: Limits the number of returned results to the specified quantity
        type: <td>integer</td>
      - in: query
        name: offset
        description: Offset for listing
        type: <td>integer</td>
      - in: query
        name: to
        description: Return only results with timestamp of first test less or equal
          to this value
        type: <td>integer</td>
      responses:
        "":
          description: ""
        400:
          description: Bad input parameter
        401:
          description: Bad or expired token
        403:
          description: Bad OAuth request (wrong consumer key, bad nonce, expired timestamp
        404:
          description: File or folder not found at the specified path
        405:
          description: Request method not expected (generally should be GET or POST)
        429:
          description: Your app is making too many requests and is being rate limited
        503:
          description: If the response includes the Retry-After header, this means
            your OAuth 1
        507:
          description: User is over Dropbox storage quota
        5xx:
          description: Server error
      tags:
      - Analysis
  ? |2-

        /api/{version}/checks
  : ? |2-

          get
    : summary: Get Check List
      description: Returns a list overview of all checks.
      operationId: |2-

        getApiVersionChecks
      x-api-path-slug: apiversionchecks-get
      parameters:
      - in: query
        name: include_tags
        description: Include tag list for each check
        type: <td>boolean</td>
      - in: query
        name: limit
        description: Limits the number of returned probes to the specified quantity
        type: <td>integer</td>
      - in: query
        name: offset
        description: Offset for listing
        type: <td>integer</td>
      - in: query
        name: tags
        description: Tag list separated by commas
        type: <td>string</td>
      responses:
        200:
          description: OK
      tags:
      - Checks
  ? |2-

        /api/{version}/credits
  : ? |2-

          get
    : summary: Get Credits List
      description: Returns information about remaining checks, SMS credits and SMS
        auto-refill status.
      operationId: get-credits-list
      x-api-path-slug: apiversioncredits-get
      responses:
        200:
          description: OK
      tags:
      - Credits
  ? |2-

        /api/{version}/probes
  : ? |2-

          get
    : summary: Get Probe Server List
      description: Returns a list of all Pingdom probe servers for Uptime and Transaction
        checks.
      operationId: get-probe-server-list
      x-api-path-slug: apiversionprobes-get
      parameters:
      - in: query
        name: includedeleted
        description: Include old probes that are no longer in use
        type: <td>boolean</td>
      - in: query
        name: limit
        description: Limits the number of returned probes to the specified quantity
        type: <td>integer</td>
      - in: query
        name: offset
        description: Offset for listing
        type: <td>integer</td>
      - in: query
        name: onlyactive
        description: Return only active probes
        type: <td>boolean</td>
      responses:
        "":
          description: ""
        400:
          description: Bad input parameter
        401:
          description: Bad or expired token
        403:
          description: Bad OAuth request (wrong consumer key, bad nonce, expired timestamp
        404:
          description: File or folder not found at the specified path
        405:
          description: Request method not expected (generally should be GET or POST)
        429:
          description: Your app is making too many requests and is being rate limited
        503:
          description: If the response includes the Retry-After header, this means
            your OAuth 1
        507:
          description: User is over Dropbox storage quota
        5xx:
          description: Server error
      tags:
      - Proves
  ? |2-

        /api/{version}/reports.email
  : ? |2-

          get
    : summary: Get Email Report Subscription List
      description: Returns a list of email report subscriptions.
      operationId: get-email-report-subscription-list
      x-api-path-slug: apiversionreports-email-get
      responses:
        "":
          description: ""
        400:
          description: Bad input parameter
        401:
          description: Bad or expired token
        403:
          description: Bad OAuth request (wrong consumer key, bad nonce, expired timestamp
        404:
          description: File or folder not found at the specified path
        405:
          description: Request method not expected (generally should be GET or POST)
        429:
          description: Your app is making too many requests and is being rate limited
        503:
          description: If the response includes the Retry-After header, this means
            your OAuth 1
        507:
          description: User is over Dropbox storage quota
        5xx:
          description: Server error
      tags:
      - Reports
  ? |2-

        /api/{version}/reports.public
  : ? |2-

          get
    : summary: Get Public Report List
      description: Returns a list of public (web-based) reports.
      operationId: get-public-report-list
      x-api-path-slug: apiversionreports-public-get
      responses:
        "":
          description: ""
        400:
          description: Bad input parameter
        401:
          description: Bad or expired token
        403:
          description: Bad OAuth request (wrong consumer key, bad nonce, expired timestamp
        404:
          description: File or folder not found at the specified path
        405:
          description: Request method not expected (generally should be GET or POST)
        429:
          description: Your app is making too many requests and is being rate limited
        503:
          description: If the response includes the Retry-After header, this means
            your OAuth 1
        507:
          description: User is over Dropbox storage quota
        5xx:
          description: Server error
      tags:
      - Reports
  ? |2-

        /api/{version}/reports.shared
  : ? |2-

          get
    : summary: Get Shared Reports (Banners) List
      description: Returns a list of shared reports (banners).
      operationId: get-shared-reports-banners-list
      x-api-path-slug: apiversionreports-shared-get
      responses:
        "":
          description: ""
        400:
          description: Bad input parameter
        401:
          description: Bad or expired token
        403:
          description: Bad OAuth request (wrong consumer key, bad nonce, expired timestamp
        404:
          description: File or folder not found at the specified path
        405:
          description: Request method not expected (generally should be GET or POST)
        429:
          description: Your app is making too many requests and is being rate limited
        503:
          description: If the response includes the Retry-After header, this means
            your OAuth 1
        507:
          description: User is over Dropbox storage quota
        5xx:
          description: Server error
      tags:
      - Reports
  ? |2-

        /api/{version}/results/{checkid}
  : ? |2-

          get
    : summary: Get Raw Check Results
      description: Return a list of raw test results for a specified check
      operationId: get-raw-check-results
      x-api-path-slug: apiversionresultscheckid-get
      parameters:
      - in: query
        name: from
        description: Start of period
        type: <td>integer</td>
      - in: query
        name: includeanalysis
        description: Attach available root cause analysis identifiers to corresponding
          results
        type: <td>boolean</td>
      - in: query
        name: limit
        description: Number of results to show (Will be set to 1000 if the provided
          value is greater than 1000)
        type: <td>integer</td>
      - in: query
        name: maxresponse
        description: Maximum response time (ms)
        type: <td>integer</td>
      - in: query
        name: minresponse
        description: Minimum response time (ms)
        type: <td>integer</td>
      - in: query
        name: offset
        description: Number of results to skip (Max value is 43200)
        type: <td>integer</td>
      - in: query
        name: probes
        description: Filter to only show results from a list of probes
        type: <td>string</td>
      - in: query
        name: status
        description: Filter to only show results with specified statuses
        type: <td>string</td>
      - in: query
        name: to
        description: End of period
        type: <td>integer</td>
      responses:
        200:
          description: OK
      tags:
      - Results
  ? |2-

        /api/{version}/settings
  : ? |2-

          get
    : summary: Get Account Settings
      description: Returns all account-specific settings.
      operationId: get-account-settings
      x-api-path-slug: apiversionsettings-get
      responses:
        "":
          description: ""
        400:
          description: Bad input parameter
        401:
          description: Bad or expired token
        403:
          description: Bad OAuth request (wrong consumer key, bad nonce, expired timestamp
        404:
          description: File or folder not found at the specified path
        405:
          description: Request method not expected (generally should be GET or POST)
        429:
          description: Your app is making too many requests and is being rate limited
        503:
          description: If the response includes the Retry-After header, this means
            your OAuth 1
        507:
          description: User is over Dropbox storage quota
        5xx:
          description: Server error
      tags:
      - Settings
  ? |2-

        /api/{version}/summary.hoursofday/{checkid}
  : ? |2-

          get
    : summary: Get Response Time Averages For Each Hour Of The Day
      description: Returns the average response time for each hour of the day (0-23)
        for a specific check over a selected time period. I.e. it shows you what an
        average day looks like during that time period.
      operationId: get-response-time-averages-for-each-hour-of-the-day
      x-api-path-slug: apiversionsummary-hoursofdaycheckid-get
      parameters:
      - in: query
        name: from
        description: Start time of period
        type: <td>integer</td>
      - in: query
        name: probes
        description: Filter to only use results from a list of probes
        type: <td>string</td>
      - in: query
        name: to
        description: End time of period
        type: <td>integer</td>
      - in: query
        name: uselocaltime
        description: If true, use the users local time zone for results (from and
          to parameters should still be specified in UTC)
        type: <td>boolean</td>
      responses:
        "":
          description: ""
        400:
          description: Bad input parameter
        401:
          description: Bad or expired token
        403:
          description: Bad OAuth request (wrong consumer key, bad nonce, expired timestamp
        404:
          description: File or folder not found at the specified path
        405:
          description: Request method not expected (generally should be GET or POST)
        429:
          description: Your app is making too many requests and is being rate limited
        503:
          description: If the response includes the Retry-After header, this means
            your OAuth 1
        507:
          description: User is over Dropbox storage quota
        5xx:
          description: Server error
      tags:
      - Summary
host: api.pingdom.com
basePath: /
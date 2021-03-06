---
swagger: "2.0"
x-collection-name: AWS Identity and Access Management
x-complete: 0
info:
  title: AWS Identity and Access Management API Get S A M L Provider
  version: 1.0.0
  description: |-
    Returns the SAML provider metadocument that was uploaded when the IAM SAML provider
          resource object was created or updated.
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /?Action=GetGroup:
    get:
      summary: Get Group
      description: Returns a list of IAM users that are in the specified IAM group.
      operationId: getGroup
      x-api-path-slug: actiongetgroup-get
      parameters:
      - in: query
        name: GroupName
        description: The name of the group
        type: string
      - in: query
        name: Marker
        description: Use this parameter only when paginating results and only after     you
          receive a response indicating that the results are truncated
        type: string
      - in: query
        name: MaxItems
        description: (Optional) Use this only when paginating results to indicate
          the     maximum number of items you want in the response
        type: string
      responses:
        200:
          description: OK
      tags:
      - Groups
  /?Action=GetOpenIDConnectProvider:
    get:
      summary: Get Open I D Connect Provider
      description: |-
        Returns information about the specified OpenID Connect (OIDC) provider resource object
              in IAM.
      operationId: getOpenIDConnectProvider
      x-api-path-slug: actiongetopenidconnectprovider-get
      parameters:
      - in: query
        name: OpenIDConnectProviderArn
        description: The Amazon Resource Name (ARN) of the OIDC provider resource
          object in IAM to get      information for
        type: string
      responses:
        200:
          description: OK
      tags:
      - OpenID Connect Providers
  /?Action=GetSAMLProvider:
    get:
      summary: Get S A M L Provider
      description: |-
        Returns the SAML provider metadocument that was uploaded when the IAM SAML provider
              resource object was created or updated.
      operationId: getSAMLProvider
      x-api-path-slug: actiongetsamlprovider-get
      parameters:
      - in: query
        name: SAMLProviderArn
        description: The Amazon Resource Name (ARN) of the SAML provider resource
          object in IAM to get      information about
        type: string
      responses:
        200:
          description: OK
      tags:
      - SAML Providers
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
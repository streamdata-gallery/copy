swagger: "2.0"
x-collection-name: Atlassian
x-complete: 1
info:
  title: Stride API
  description: this-service-provides-public-api-for-the-stride-
  version: 1.0.0
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /content/{id}/pagehierarchy/copy:
    post:
      summary: Copy page hierarchy
      description: |-
        Copy page hierarchy allows the copying of an entire hierarchy of pages and their associated properties, permissions and attachments.
         The id path parameter refers to the content id of the page to copy, and the new parent of this copied page is defined using the destinationPageId in the request body.
         The titleOptions object defines the rules of renaming page titles during the copy;
         for example, search and replace can be used in conjunction to rewrite the copied page titles.

         Response example:
         <pre><code>
         {
              "id" : "1180606",
              "links" : {
                   "status" : "/rest/api/longtask/1180606"
              }
         }
         </code></pre>
         Use the /longtask/<taskId> REST API to get the copy task status.
      operationId: com.atlassian.confluence.plugins.restapi.resources.PageHierarchyResource.copyPageHierarchy_post
      x-api-path-slug: contentidpagehierarchycopy-post
      parameters:
      - in: path
        name: id
      responses:
        200:
          description: OK
      tags:
      - Copy
      - Page
      - Hierarchy
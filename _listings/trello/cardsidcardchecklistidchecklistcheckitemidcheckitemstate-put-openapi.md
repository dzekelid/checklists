---
swagger: "2.0"
x-collection-name: Trello
x-complete: 0
info:
  title: Trello Put Cards Checklist Checkitem Checkitem State
  description: Put cards checklist checkitem checkitem state.
  termsOfService: https://trello.com/legal
  contact:
    name: Trello
    url: https://trello.com/home
  version: "1.0"
host: trello.com
basePath: /1
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /boards/{idBoard}/checklists:
    get:
      summary: Get Boards Checklists
      description: Get boards checklists.
      operationId: getBoardsChecklistsByIdBoard
      x-api-path-slug: boardsidboardchecklists-get
      parameters:
      - in: query
        name: cards
        description: 'One of: all, closed, none, open or visible'
      - in: query
        name: card_fields
        description: 'all or a comma-separated list of: badges, checkItemStates, closed,
          dateLastActivity, desc, descData, due, email, idAttachmentCover, idBoard,
          idChecklists, idLabels, idList, idMembers, idMembersVoted, idShort, labels,
          manualCoverAttachment, name, pos, shortLink, shortUrl, subscribed or url'
      - in: query
        name: checkItems
        description: 'One of: all or none'
      - in: query
        name: checkItem_fields
        description: 'all or a comma-separated list of: name, nameData, pos, state
          or type'
      - in: query
        name: fields
        description: 'all or a comma-separated list of: idBoard, idCard, name or pos'
      - in: query
        name: filter
        description: 'One of: all or none'
      - in: path
        name: idBoard
        description: board_id
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Boards
      - Checklists
    post:
      summary: Post Boards Checklists
      description: Post boards checklists.
      operationId: addBoardsChecklistsByIdBoard
      x-api-path-slug: boardsidboardchecklists-post
      parameters:
      - in: body
        name: body
        description: Attributes of Boards Checklists to be added
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: idBoard
        description: board_id
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Boards
      - Checklists
  /cards/{idCard}/checklists:
    get:
      summary: Get Cards Checklists
      description: Get cards checklists.
      operationId: getCardsChecklistsByIdCard
      x-api-path-slug: cardsidcardchecklists-get
      parameters:
      - in: query
        name: cards
        description: 'One of: all, closed, none, open or visible'
      - in: query
        name: card_fields
        description: 'all or a comma-separated list of: badges, checkItemStates, closed,
          dateLastActivity, desc, descData, due, email, idAttachmentCover, idBoard,
          idChecklists, idLabels, idList, idMembers, idMembersVoted, idShort, labels,
          manualCoverAttachment, name, pos, shortLink, shortUrl, subscribed or url'
      - in: query
        name: checkItems
        description: 'One of: all or none'
      - in: query
        name: checkItem_fields
        description: 'all or a comma-separated list of: name, nameData, pos, state
          or type'
      - in: query
        name: fields
        description: 'all or a comma-separated list of: idBoard, idCard, name or pos'
      - in: query
        name: filter
        description: 'One of: all or none'
      - in: path
        name: idCard
        description: card id or shortlink
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Cards
      - Checklists
    post:
      summary: Post Cards Checklists
      description: Post cards checklists.
      operationId: addCardsChecklistsByIdCard
      x-api-path-slug: cardsidcardchecklists-post
      parameters:
      - in: body
        name: body
        description: Attributes of Cards Checklists to be added
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: idCard
        description: card id or shortlink
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Cards
      - Checklists
  /cards/{idCard}/checklists/{idChecklist}:
    delete:
      summary: Delete Cards Checklists
      description: Delete cards checklists.
      operationId: deleteCardsChecklistsByIdCardByIdChecklist
      x-api-path-slug: cardsidcardchecklistsidchecklist-delete
      parameters:
      - in: path
        name: idCard
        description: card id or shortlink
      - in: path
        name: idChecklist
        description: idChecklist
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Cards
      - Checklists
  /checklists:
    post:
      summary: Post Checklists
      description: Post checklists.
      operationId: addChecklists
      x-api-path-slug: checklists-post
      parameters:
      - in: body
        name: body
        description: Attributes of Checklists to be added
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Checklists
  /checklists/{idChecklist}:
    delete:
      summary: Delete Checklists
      description: Delete checklists.
      operationId: deleteChecklistsByIdChecklist
      x-api-path-slug: checklistsidchecklist-delete
      parameters:
      - in: path
        name: idChecklist
        description: idChecklist
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Checklists
    get:
      summary: Get Checklists
      description: Get checklists.
      operationId: getChecklistsByIdChecklist
      x-api-path-slug: checklistsidchecklist-get
      parameters:
      - in: query
        name: cards
        description: 'One of: all, closed, none, open or visible'
      - in: query
        name: card_fields
        description: 'all or a comma-separated list of: badges, checkItemStates, closed,
          dateLastActivity, desc, descData, due, email, idAttachmentCover, idBoard,
          idChecklists, idLabels, idList, idMembers, idMembersVoted, idShort, labels,
          manualCoverAttachment, name, pos, shortLink, shortUrl, subscribed or url'
      - in: query
        name: checkItems
        description: 'One of: all or none'
      - in: query
        name: checkItem_fields
        description: 'all or a comma-separated list of: name, nameData, pos, state
          or type'
      - in: query
        name: fields
        description: 'all or a comma-separated list of: idBoard, idCard, name or pos'
      - in: path
        name: idChecklist
        description: idChecklist
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Checklists
    put:
      summary: Put Checklists
      description: Put checklists.
      operationId: updateChecklistsByIdChecklist
      x-api-path-slug: checklistsidchecklist-put
      parameters:
      - in: body
        name: body
        description: Attributes of Checklists to be updated
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: idChecklist
        description: idChecklist
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Checklists
  /checklists/{idChecklist}/board:
    get:
      summary: Get Checklists Board
      description: Get checklists board.
      operationId: getChecklistsBoardByIdChecklist
      x-api-path-slug: checklistsidchecklistboard-get
      parameters:
      - in: query
        name: fields
        description: 'all or a comma-separated list of: closed, dateLastActivity,
          dateLastView, desc, descData, idOrganization, invitations, invited, labelNames,
          memberships, name, pinned, powerUps, prefs, shortLink, shortUrl, starred,
          subscribed or url'
      - in: path
        name: idChecklist
        description: idChecklist
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Checklists
      - Board
  /checklists/{idChecklist}/board/{field}:
    get:
      summary: Get Checklists Board Field
      description: Get checklists board field.
      operationId: getChecklistsBoardByIdChecklistByField
      x-api-path-slug: checklistsidchecklistboardfield-get
      parameters:
      - in: path
        name: field
        description: field
      - in: path
        name: idChecklist
        description: idChecklist
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Checklists
      - Board
      - Field
  /checklists/{idChecklist}/cards:
    get:
      summary: Get Checklists Cards
      description: Get checklists cards.
      operationId: getChecklistsCardsByIdChecklist
      x-api-path-slug: checklistsidchecklistcards-get
      parameters:
      - in: query
        name: actions
        description: 'all or a comma-separated list of: addAttachmentToCard, addChecklistToCard,
          addMemberToBoard, addMemberToCard, addMemberToOrganization, addToOrganizationBoard,
          commentCard, convertToCardFromCheckItem, copyBoard, copyCard, copyCommentCard,
          createBoard, createCard, createList, createOrganization, deleteAttachmentFromCard,
          deleteBoardInvitation, deleteCard, deleteOrganizationInvitation, disablePowerUp,
          emailCard, enablePowerUp, makeAdminOfBoard, makeNormalMemberOfBoard, makeNormalMemberOfOrganization,
          makeObserverOfBoard, memberJoinedTrello, moveCardFromBoard, moveCardToBoard,
          moveListFromBoard, moveListToBoard, removeChecklistFromCard, removeFromOrganizationBoard,
          removeMemberFromCard, unconfirmedBoardInvitation, unconfirmedOrganizationInvitation,
          updateBoard, updateCard, updateCard:closed, updateCard:desc, updateCard:idList,
          updateCard:name, updateCheckItemStateOnCard, updateChecklist, updateList,
          updateList:closed, updateList:name, updateMember or updateOrganization'
      - in: query
        name: attachments
        description: A boolean value or &quot;cover&quot; for only card cover attachments
      - in: query
        name: attachment_fields
        description: 'all or a comma-separated list of: bytes, date, edgeColor, idMember,
          isUpload, mimeType, name, previews or url'
      - in: query
        name: before
        description: A date, or null
      - in: query
        name: checkItemStates
        description: true or false
      - in: query
        name: checklists
        description: 'One of: all or none'
      - in: query
        name: fields
        description: 'all or a comma-separated list of: badges, checkItemStates, closed,
          dateLastActivity, desc, descData, due, email, idAttachmentCover, idBoard,
          idChecklists, idLabels, idList, idMembers, idMembersVoted, idShort, labels,
          manualCoverAttachment, name, pos, shortLink, shortUrl, subscribed or url'
      - in: query
        name: filter
        description: 'One of: all, closed, none or open'
      - in: path
        name: idChecklist
        description: idChecklist
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: limit
        description: a number from 1 to 1000
      - in: query
        name: members
        description: true or false
      - in: query
        name: member_fields
        description: 'all or a comma-separated list of: avatarHash, bio, bioData,
          confirmed, fullName, idPremOrgsAdmin, initials, memberType, products, status,
          url or username'
      - in: query
        name: since
        description: A date, or null
      - in: query
        name: stickers
        description: true or false
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Checklists
      - Cards
  /checklists/{idChecklist}/cards/{filter}:
    get:
      summary: Get Checklists Cards Filter
      description: Get checklists cards filter.
      operationId: getChecklistsCardsByIdChecklistByFilter
      x-api-path-slug: checklistsidchecklistcardsfilter-get
      parameters:
      - in: path
        name: filter
        description: filter
      - in: path
        name: idChecklist
        description: idChecklist
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Checklists
      - Cards
      - Filter
  /checklists/{idChecklist}/checkItems:
    get:
      summary: Get Checklists Checkitems
      description: Get checklists checkitems.
      operationId: getChecklistsCheckItemsByIdChecklist
      x-api-path-slug: checklistsidchecklistcheckitems-get
      parameters:
      - in: query
        name: fields
        description: 'all or a comma-separated list of: name, nameData, pos, state
          or type'
      - in: query
        name: filter
        description: 'One of: all or none'
      - in: path
        name: idChecklist
        description: idChecklist
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Checklists
      - Checkitems
    post:
      summary: Post Checklists Checkitems
      description: Post checklists checkitems.
      operationId: addChecklistsCheckItemsByIdChecklist
      x-api-path-slug: checklistsidchecklistcheckitems-post
      parameters:
      - in: body
        name: body
        description: Attributes of Checklists Check Items to be added
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: idChecklist
        description: idChecklist
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Checklists
      - Checkitems
  /checklists/{idChecklist}/checkItems/{idCheckItem}:
    delete:
      summary: Delete Checklists Checkitems Checkitem
      description: Delete checklists checkitems checkitem.
      operationId: deleteChecklistsCheckItemsByIdChecklistByIdCheckItem
      x-api-path-slug: checklistsidchecklistcheckitemsidcheckitem-delete
      parameters:
      - in: path
        name: idCheckItem
        description: idCheckItem
      - in: path
        name: idChecklist
        description: idChecklist
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Checklists
      - Checkitems
      - Checkitem
    get:
      summary: Get Checklists Checkitems Checkitem
      description: Get checklists checkitems checkitem.
      operationId: getChecklistsCheckItemsByIdChecklistByIdCheckItem
      x-api-path-slug: checklistsidchecklistcheckitemsidcheckitem-get
      parameters:
      - in: query
        name: fields
        description: 'all or a comma-separated list of: name, nameData, pos, state
          or type'
      - in: path
        name: idCheckItem
        description: idCheckItem
      - in: path
        name: idChecklist
        description: idChecklist
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Checklists
      - Checkitems
      - Checkitem
  /checklists/{idChecklist}/idCard:
    put:
      summary: Put Checklists Card
      description: Put checklists card.
      operationId: updateChecklistsIdCardByIdChecklist
      x-api-path-slug: checklistsidchecklistidcard-put
      parameters:
      - in: body
        name: body
        description: Attributes of Checklists Id Card to be updated
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: idChecklist
        description: idChecklist
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Checklists
      - Card
  /checklists/{idChecklist}/name:
    put:
      summary: Put Checklists Name
      description: Put checklists name.
      operationId: updateChecklistsNameByIdChecklist
      x-api-path-slug: checklistsidchecklistname-put
      parameters:
      - in: body
        name: body
        description: Attributes of Checklists Name to be updated
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: idChecklist
        description: idChecklist
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Checklists
      - Name
  /checklists/{idChecklist}/pos:
    put:
      summary: Put Checklists Pos
      description: Put checklists pos.
      operationId: updateChecklistsPosByIdChecklist
      x-api-path-slug: checklistsidchecklistpos-put
      parameters:
      - in: body
        name: body
        description: Attributes of Checklists Pos to be updated
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: idChecklist
        description: idChecklist
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Checklists
      - Pos
  /checklists/{idChecklist}/{field}:
    get:
      summary: Get Checklists Field
      description: Get checklists field.
      operationId: getChecklistsByIdChecklistByField
      x-api-path-slug: checklistsidchecklistfield-get
      parameters:
      - in: path
        name: field
        description: field
      - in: path
        name: idChecklist
        description: idChecklist
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Checklists
      - Field
  /cards/{idCard}/checklist/{idChecklist}/checkItem:
    post:
      summary: Post Cards Checklist Checkitem
      description: Post cards checklist checkitem.
      operationId: addCardsChecklistCheckItemByIdCardByIdChecklist
      x-api-path-slug: cardsidcardchecklistidchecklistcheckitem-post
      parameters:
      - in: body
        name: body
        description: Attributes of Cards Checklist Check Item to be added
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: idCard
        description: card id or shortlink
      - in: path
        name: idChecklist
        description: idChecklist
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Cards
      - Checklist
      - Checkitem
  /cards/{idCard}/checklist/{idChecklist}/checkItem/{idCheckItem}:
    delete:
      summary: Delete Cards Checklist Checkitem Checkitem
      description: Delete cards checklist checkitem checkitem.
      operationId: deleteCardsChecklistCheckItemByIdCardByIdChecklistByIdCheckItem
      x-api-path-slug: cardsidcardchecklistidchecklistcheckitemidcheckitem-delete
      parameters:
      - in: path
        name: idCard
        description: card id or shortlink
      - in: path
        name: idCheckItem
        description: idCheckItem
      - in: path
        name: idChecklist
        description: idChecklist
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Cards
      - Checklist
      - Checkitem
      - Checkitem
  /cards/{idCard}/checklist/{idChecklist}/checkItem/{idCheckItem}/convertToCard:
    post:
      summary: Post Cards Checklist Checkitem Checkitem Converttocard
      description: Post cards checklist checkitem checkitem converttocard.
      operationId: addCardsChecklistCheckItemConvertToCardByIdCardByIdChecklistByIdCheckItem
      x-api-path-slug: cardsidcardchecklistidchecklistcheckitemidcheckitemconverttocard-post
      parameters:
      - in: path
        name: idCard
        description: card id or shortlink
      - in: path
        name: idCheckItem
        description: idCheckItem
      - in: path
        name: idChecklist
        description: idChecklist
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Cards
      - Checklist
      - Checkitem
      - Checkitem
      - Converttocard
  /cards/{idCard}/checklist/{idChecklist}/checkItem/{idCheckItem}/name:
    put:
      summary: Put Cards Checklist Checkitem Checkitem Name
      description: Put cards checklist checkitem checkitem name.
      operationId: updateCardsChecklistCheckItemNameByIdCardByIdChecklistByIdCheckItem
      x-api-path-slug: cardsidcardchecklistidchecklistcheckitemidcheckitemname-put
      parameters:
      - in: body
        name: body
        description: Attributes of Cards Checklist Check Item Name to be updated
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: idCard
        description: card id or shortlink
      - in: path
        name: idCheckItem
        description: idCheckItem
      - in: path
        name: idChecklist
        description: idChecklist
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Cards
      - Checklist
      - Checkitem
      - Checkitem
      - Name
  /cards/{idCard}/checklist/{idChecklist}/checkItem/{idCheckItem}/pos:
    put:
      summary: Put Cards Checklist Checkitem Checkitem Pos
      description: Put cards checklist checkitem checkitem pos.
      operationId: updateCardsChecklistCheckItemPosByIdCardByIdChecklistByIdCheckItem
      x-api-path-slug: cardsidcardchecklistidchecklistcheckitemidcheckitempos-put
      parameters:
      - in: body
        name: body
        description: Attributes of Cards Checklist Check Item Pos to be updated
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: idCard
        description: card id or shortlink
      - in: path
        name: idCheckItem
        description: idCheckItem
      - in: path
        name: idChecklist
        description: idChecklist
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Cards
      - Checklist
      - Checkitem
      - Checkitem
      - Pos
  /cards/{idCard}/checklist/{idChecklist}/checkItem/{idCheckItem}/state:
    put:
      summary: Put Cards Checklist Checkitem Checkitem State
      description: Put cards checklist checkitem checkitem state.
      operationId: updateCardsChecklistCheckItemStateByIdCardByIdChecklistByIdCheckItem
      x-api-path-slug: cardsidcardchecklistidchecklistcheckitemidcheckitemstate-put
      parameters:
      - in: body
        name: body
        description: Attributes of Cards Checklist Check Item State to be updated
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: idCard
        description: card id or shortlink
      - in: path
        name: idCheckItem
        description: idCheckItem
      - in: path
        name: idChecklist
        description: idChecklist
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Cards
      - Checklist
      - Checkitem
      - Checkitem
      - State
  /cards/{idCard}/checklist/{idChecklistCurrent}/checkItem/{idCheckItem}:
    put:
      summary: Put Cards Checklistcurrent Checkitem Checkitem
      description: Put cards checklistcurrent checkitem checkitem.
      operationId: updateCardsChecklistCheckItemByIdCardByIdChecklistCurrentByIdCheckItem
      x-api-path-slug: cardsidcardchecklistidchecklistcurrentcheckitemidcheckitem-put
      parameters:
      - in: body
        name: body
        description: Attributes of Cards Checklist Id Checklist Current Check Item
          to be updated
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: idCard
        description: card id or shortlink
      - in: path
        name: idCheckItem
        description: idCheckItem
      - in: path
        name: idChecklistCurrent
        description: idChecklistCurrent
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Cards
      - Checklistcurrent
      - Checkitem
      - Checkitem
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
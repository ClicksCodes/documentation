# ClicksForms
[Invite](https://discord.com/api/oauth2/authorize?client_id=805392054678192169&permissions=2416307200&scope=bot%20applications.commands)

## Index

Name                      | Description
--------------------------|----------------------------
[Endpoints](#endpoints)   | The list of endpoints
[Structures](#structures) | How to form data structures


## Endpoints

Method | Endpoint                   | Request data
-------|----------------------------|---------------------------------------------------------------------
GET    | [`/`](#root)               |
GET    | [`/forms`](#forms)         | `token: str` `guild: int`
GET    | [`/responses`](#responses) | `token: str` `guild: int`
GET    | [`/in/{guild}`](#inguild)  |
POST   | [`/upload`](#upload)       | `OPTIONAL token: str` `service: str` `service_url: str` `data: JSON`

-----

#### `/`
Gets the bots response time, in seconds <br><br>

#### `/forms`
Lists all forms in a guild <br>
```json
{
  "token": "str - The authorisation token. This endpoint is private, you must request an API key from PineappleFan",
  "guild": "int - The guild to get forms from"
}
```
<br>

#### `/responses`
Lists all responses in a guild <br>
Lists all forms in a guild <br>
```json
{
  "token": "str - The authorisation token. This endpoint is private, you must request an API key from PineappleFan",
  "guild": "int - The guild to get responses from"
}
```
<br>

#### `/in/{guild}`
Checks if the bot is in a specific guild <br><br>

#### `/upload`
Uploads a form to the bot for a custom service <br>
Lists all forms in a guild <br>
```json
{
  "token": "str - The authorisation token. This endpoint is private, you must request an API key from PineappleFan",
  "service": "str - The name of your service, e.g. Google Forms",
  "service_url": "str - The link to your service, e.g. https://forms.google.com",
  "data": "JSON - A ClicksForms form object"
}
```
<br>


## Structures

#### Form data
Form data is a JSON object, with required and optional arguments

Name               | Optional | Type                          | Default |  Description
-------------------|----------|-------------------------------|---------|-------------------------------------------------------------------------------
`active`           | True     | `bool`                        | `True`  | If users can apply to the form once downloaded
`anonymous`        | True     | `bool`                        | `False` | If the form should be anonymous (usernames not shown to admins)
`name`             | False    | `str`                         |         | The title of the form
`description`      | True     | `str`                         | `None`  | The description of the form
`required_roles`   | True     | `list[int]`                   | `[]`    | A list of roles required to complete the form
`disallowed_roles` | True     | `list[int]`                   | `[]`    | A list of roles that will stop users completing the form
`given_roles`      | True     | `list[int]`                   | `[]`    | A list of roles given to users when the form is completed, or when accepted
`removed_roles`    | True     | `list[int]`                   | `[]`    | A list of roles removed form users when the form is completed or when accepted
`auto_accept`      | True     | `bool`                        | `False` | If roles should be applied as soon as the form is completed
`questions`        | False    | [`list[question]`](#question) |         | The list of questions on the form

#### Question
Questions are a JSON object

Name          | Optional | Type                            | Default | Description
--------------|----------|---------------------------------|---------|---------------------------------
`type`        | False    | [`questionType`](#questionType) |         | The type of question
`title`       | False    | `str`                           |         | The title of the question
`description` | True     | `str`                           | `None`  | The description of the question
`colour`      | False    | [`colourString`](#colourString) |         | The colour of the question embed
`options`     | False    | [`questionData`](#questionData) |         | The question specific data

#### QuestionType
Question types are one of the following strings

Name               | Description
-------------------|--------------------------------------------------------------
`text`             | A text response
`number`           | An integer response
`multichoice`      | A list of options the user can choose a specified amount from
`fileupload`       | A file uploaded by the user
`time`             | A time response
`date`             | A date response
`text-decoration`  | Text shown to the user between questions
`image-decoration` | An image shown to the user between questions
`url-decoration`   | A link button given to the user

#### ColourString
Colour must be one of the following
- `red`
- `orange`
- `yellow`
- `green`
- `blue`
- `purple`
- `pink`
- `grey`

#### QuestionData
Extra data about a question. All arguments are required

Question type      | Arguments
-------------------|-------------------------------------------------------------------------------------------------------------
`text`             | `min: int >= 1` `max: int <= 2000`
`number`           | `min: int >= 2^32 ` `max: int <= 2^32`
`multichoice`      | `min: int >= 1` `max: int <= number of options` `options: [{MultipleChoiceOptions}](#MultipleChoiceOptions)`
`fileupload`       | None
`time`             | None
`date`             | None
`text-decoration`  | None
`image-decoration` | `url: str`
`url-decoration`   | `url: str`

#### MultipleChoiceOptions
A dictionary of options
```
{
  KEY: {VALUE}
  ...
}
```
`KEY` - An integer `0 <= n <= 24`
`VALUE` - `["title: str, 1 <= n <= 25", "description: str, 0 <= n <= 100"]`

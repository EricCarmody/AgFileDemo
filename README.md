# AgFileDemo
Okay so I do not have a ton of experience with APIs 
and wanted to try to go a little more in detail for this.
I added a lot of new things in the program.cs for myself
such as the file extenion provider and an attempt at the automopper and 
register the repo as well as the db context. I really like this style of program.cs

For the versioning I set up the base version to be always taken with out a user
specifying. I basically just set a base and did not have other versions supported or
created.

One thing I did not have time to implement would be token creation for
for securing the API. I think this would be critical if I had the time and if this 
was a live API.

This is able to upload a file, delete, download, or view them all. I tested
mostly in postman and sometimes using the dev browser as well.

You can see for Entity Framework I used a repo pattern and did pretty standard ops.
In my current position we use DTOs and only Ids for pretty much all database queries and op
but I didnt wait to go overboard with it here so I pass objects in sometimes.

This is my first time documenting an API readme so I hope these make sense to someone
besides myself.

Endpoints:

GET : /api/files
POST : /api/files
GET : /api/files/{fileid}
PUT : /api/files/{fileid}
PATCH : /api/files/{fileid}
DELETE : /api/files/{fileid}



POST 
Accept: application/json
Content-Type: application/json

{
  "Name": string,
  "Description": string
  "Data": string(base64)
}

For requests its just the ID

For Patch
Accept: application/json
Content-Type: application/json

{
  "Name": string,
  "Description": string
  "Data": string(base64)
}

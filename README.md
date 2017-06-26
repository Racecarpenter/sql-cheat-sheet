# sql-cheat-sheet&copy;

```

heyo dummy,
you're here because you forgot.
You forgot how SQL works.
Or you never knew how to do it anyways.
And you need me to help you.
Strap on your helmet dum-dum.
```

# HOW THE HECK DO I GET THIS THING RUNNING AGAIN?
After PostgreSQL is installed, run the following command in your terminal:

```

~ $ psql
psql (9.6.3)
Type "help" for help.

yourname=#

```
if you get an error message that says 'Database does not exist'
that means you don't have a user db created yet and you will have to run the following commands:

```

~ $ whoami
'your name'
~ $ createdb your name
~ $ psql
```

if you're still getting an error message, <a href="google.com">TRY GOOGLE</a> <br>
(idk why you didn't try google in the first place, freakin numbskull)

# ok, now what?

What do you mean "now what?"<br>
now, you get to use it.<br>
you can do <i>STUFF</i>.

for example:
```

-\dt
	-(describes tables)
-\l
	-(list all databases)
-\c + name of database
	-(connects to a given database)
-\?
	-(shows list of commands)
```

See, thats the stuff.

# HOW DO I CRUD THO RICHARD?
<sup>Richard was my fathers name, that was weird.</sup><br>
if you were too drunk to remember what CRUD is:
```

CREATE
READ
UPDATE
DESTROY
```
think you can handle that?
good, lets move on.

### IN ORDER TO CREATE

Before we create entries into the database table, we must know the value parameters for that table.
Here is an example of a table with its keys and parameters:

```

CREATE TABLE jabroni (
  id serial,
  name text,
  age integer,
  jabroni_rating integer,
  from text,
  father_is_jabroni boolean NOT NULL,
);
```
so in this above example,<br>
the name of the table is jabroni
<sup><i>(naturally)</sup></i><br>
and it has columns with the headings of:<br><ul>
<li>id</li>
<li>name</li>
<li>age</li>
<li>jabroni_rating</li>
<li>from</li>
<li>father_is_jabroni</li>
</ul><br>
the following <i>types</i> are the corresponding types of data that will be in that particular columns.

WE CAN ALSO ALTER THE TABLE BY USING COMMAND: ALTER TABLE (table name)

#### How are we doing now buddy?
so now that we know what the properties are and the value types of the data, WE CAN ACTUALLY PUT STUFF IN IT NOW (OMG YES PLEASE I CAN'T WAIT)<br>
<sup><i>i still hate you for making me do this</sup></i>

```

racecarpenter=# INSERT into jabroni VALUES(default, 'Fletcher Cove', 34, 2.5, 'Newport, Connecticut', true)
```
awww what happened?
nothing.
nothing happened at all.
you know why?
BECAUSE YOU DIDN'T PUT THE SEMI-COLON AT THE END
<sup><i>but you didn't tell me to use the semi-</i></sup><br>
just shutup. shut your face.
I know what I'm doing, lets not forget who came to who.<br>
#### all you have to do, is type in the semi-colon now and it will finish the command

this is because of a cool feature of PostgreSQL that allows it to use multiple-lines. neat stuff. moving on.

### HOW TO READ
haha, you can't even read this.
dummy.

```

racecarpenter=# SELECT * from jabroni;
```
this will give you all the entries with all the columns for that specific table.
but lets say you wanted to only see the name and whether their father was a jabroni, you could do this:

```
racecarpenter=# SELECT name, father_is_jabroni from jabroni;
```
you see now? neat stuff.
if only you could read that.

### HOW TO UPDATE

i'm getting bored:

```

racecarpenter=# UPDATE jabroni SET age = 64, jabroni_rating = 10000 WHERE name = 'Richard';
```
this would change any jabroni named Richards age to 64 and his jabroni rating to 10 thousand. what a mook.

### HOW TO DELETE

oh idk, maybe try:

```

racecarpenter=# DELETE from jabroni WHERE name='Fletcher Cove';
```
pretty straightforward. you're deleting entries FROM the table JABRONI on entries WHERE the NAME is 'FLETCHER COVE' SEMI-COLON;

moving on.

## thats pretty much it
I could give you a bunch more info on special commands that use math and relational data structuring to do more cool stuff, but theres too much to cover and again, thats what google is for.
hope you enjoyed getting schooled dummy dum-dum

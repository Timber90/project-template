# Irish Constituencies Neo4j Database
###### Student name, G00123456

## Introduction
My Project is about creating a database for the 2016 election in Ireland.
It includes the 40 constituencies in ireland and all the candidates what ran for office in the individual 
Constituency.
Data like the associated party of the candidate is stored the there gender/sex and if they were elected or not.



## Database
The database is a nea4j database. It is represented in graphs or rows.
To create the Databse I have used statement like bellow:

#### Create Statement Constituencies
Example
```(j:Constituencies { Constituency:'Dublin Bay North', Population :'146,512', Parlamentery_Seats:'5'}),

#### Create Statement Candidate
Example
```(au:Candidate {Candidate:'Kevin O Keeffe',    Party:'Fianna Fáil',    Constituency:'Cork East'  ,Sex:'M',    Elected:'Yes'}),

#### Relationship create statement
Example
```match (n{Constituency:"Carlow-Kilkenny"}), (d{Constituency:"Carlow–Kilkenny"}) create (n)-[r:FROM]->(d) return r


## Queries
Summarise your three queries here.
Then explain them one by one in the following sections.

#### Query one title
This query retreives the Bacon number of an actor...
```cypher
MATCH
	(Bacon)
RETURN
	Bacon;
```

#### Query two title
This query retreives the Bacon number of an actor...
```cypher
MATCH
	(Bacon)
RETURN
	Bacon;
```

#### Query three title
This query retreives the Bacon number of an actor...
```cypher
MATCH
	(Bacon)
RETURN
	Bacon;
```
#### Problems / Mistakes
In creating the Database I have made a by naming the name of the constituency of the constituency "constituency".

```CREATE (j:Constituencies { Constituency:'Dublin Bay North', Population :'146,512', Parlamentery_Seats:'5'}),

```
This mistake has resulted in a problem with the relationships since the candidates constituencies are also called constituency.

```(au:Candidate {Candidate:'Kevin O Keeffe',    Party:'Fianna Fáil',    Constituency:'Cork East'  ,Sex:'M',    Elected:'Yes'}),

The problem is that now when I create a relationship:

```match (n{Constituency:"Carlow-Kilkenny"}), (d{Constituency:"Carlow–Kilkenny"}) create (n)-[r:FROM]->(d) return n,d,r

Relationships are created that are not wanted. Every candidate has a relationship with every other candidate  who come from the same 
constituency.
To resolve this mistake I would have to change either the candidates or the constituencies "Constituesny" to another entry
Like Name.
But to do so I would have to recreate the hole database and since I did not save all the create statements I do not have time to resove this error.


## References
1. [Neo4J website](http://neo4j.com/), the website of the Neo4j database.
2. http://www.thejournal.ie/election-2016/constituency/11/
3. https://en.wikipedia.org/wiki/Parliamentary_constituencies_in_the_Republic_of_Ireland
4. http://neo4j.com/docs/stable/query-delete.html
5. http://irishpoliticalmaps.blogspot.ie/2015/06/confirmed-candidates-for-next-general_3.html
6. https://www.youtube.com/watch?v=bqvDSioHYq8
7. https://www.youtube.com/watch?v=Go3P73-KV30
8. https://www.youtube.com/watch?v=Go3P73-KV30
9. 

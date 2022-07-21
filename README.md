# mongodb

Prep: 
* insertiere die daten aus der movies json datei 

Queries: 
* alle filme aus dem jahr 2000 

db.uebungscollection.find({year: '2000'})

* alle filme aus den jahren 1994 oder 2001 

db.uebungscollection.find({year:{$in: ["1994","2001"]}})


* alle filme aus den jahren 1994 oder 2001 sortiert nach titel absteigend 

db.uebungscollection.find({year:{$in:["1994", "2001"]}}).sort({titel: -1})


* alle filme aus den jahren 1994 oder 2001 sortiert nach bewertung aufsteigen 

db.uebungscollection.find({year:{$in:["1994", "2001"]}}).sort({rate: 1})

* wieviele filme haben eine bewertung von genau 9.0 

db.uebungscollection.find({rate: "9.0"}).count()

* alle filme-titel + bewertung vom George Lucas 

db.uebungscollection.find({director: "George Lucas"},{title: 1, rate: 1})

* alle filme-titel + bewertung + genre vom Martin Scorsese, aufsteigend nach bewertung sortiert 

db.uebungscollection.find({director: "Martin Scorsese"},{title: 1, rate: 1, genre: 1}).sort({rate: 1})
![image](https://user-images.githubusercontent.com/102032081/180221366-6dd9dfc8-d578-4218-9f3b-70482de0543f.png)

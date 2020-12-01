import pprint
import pymongo
from pymongo import MongoClient,GEO2D,GEOSPHERE,InsertOne, DeleteOne, ReplaceOne
from datetime import datetime,time
from bson.son import SON
from collections import OrderedDict
client = MongoClient('mongodb://localhost:27017/')
#client = MongoClient('localhost', 27017)

# Collection the database
db=client.mydb
# Collection
students=db.Studrecords

#Query the database
list(students.find({"StudentsName":"Jane"}))

[{'_id': ObjectId('5fbf6a0d28f23736d002a04a'),
  'LastName': 'Dow',
  'profilecreated': datetime.datetime(2020, 11, 26, 2, 40, 45, 557000),
  'Score': 5.7,
  'StudentsName': 'Jane'},
 {'_id': ObjectId('5fbf6a2028f23736d002a04f'),
  'LastName': 'Dow',
  'profilecreated': datetime.datetime(2020, 11, 26, 2, 41, 4, 658000),
  'Score': 5.7,
  'StudentsName': 'Jane'},
 {'_id': ObjectId('5fbf6a2828f23736d002a055'),
  'LastName': 'Dow',
  'profilecreated': datetime.datetime(2020, 11, 26, 2, 41, 12, 524000),
  'Score': 5.2,
  'StudentsName': 'Jane'},
 {'_id': ObjectId('5fbf4a4928f23736d002a03a'),
  'profilecreated': datetime.datetime(2020, 11, 26, 0, 25, 13, 606000),
  'Score': 11.9,
  'StudentsName': 'Jane',
  'LastName': '$Name01'},
 {'_id': ObjectId('5fbf552028f23736d002a03f'),
  'profilecreated': datetime.datetime(2020, 11, 26, 1, 11, 28, 786000),
  'Score': 6.2,
  'StudentsName': 'Jane',
  'LastName': '$Name01'},
 {'_id': ObjectId('5fbf69a628f23736d002a045'),
  'profilecreated': datetime.datetime(2020, 11, 26, 2, 39, 2, 251000),
  'Score': 5.7,
  
  #Performing a mini Aggregation
 
 list(students.aggregate([{"$project":{"_id":0,"Score":1,"StudentsName"
                                   :1}},{"$match":{"StudentsName":"Jane"}},\
                      {"$group":{"_id":"Name","SumScore":{"$avg":"$Score"}}}]))
                  
 [{'_id': 'Name', 'SumScore': 6.733333333333333}]
  'StudentsName': 'Jane'}]

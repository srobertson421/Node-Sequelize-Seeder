#Seeding DB's with Node

Node has a plethora of other uses than just web servers. One major use of Node is to manipulate local files on you file-system ( read, write ) and use the data from those files to do other tasks. For this challenge you will be using Node to extract information from a CSV file ( comma separated list ). You will then take that data, parse it, and input it into your Postgres DB.

##Starting point

* Fork and clone this repo
* ```cd``` into folder and run ```npm init```
* run ```npm install --save pg pg-hstore sequelize```
* run ``` sequelize init```
* Next create your model according to the data you find in the CSV files ```sequelize model:create --name person --attributes firstName:string,lastName:string,email:string,gender:string,ip_address:string```
* Write code in the "db_seeder.js" file
* Run code via Node with ```node db_seeder.js```
* Use "MOCK_DATA_SMALL.csv" for initial testing as it only has 10 entries, "MOCK_DATA.csv" has 1000.

### Utilize the "fs" module
Node has a built-in module called "fs" that you can require at any time. it allows for reading and writing to the file-system. You will use this to take data out of the CSV file. Specifically look at the readFile method:

https://nodejs.org/api/fs.html#fs_fs_readfile_file_options_callback

Make sure to have PostgresQL running and run ```sequelize init``` in the directory in order to setup access to your DB, just like you would in your Express apps. You can then build a model to input data to the DB with.


## Bonus

* Covert the CSV file into a JSON file instead of populating the DB.

![Image description](https://i1.faceprep.in/ProGrad/face-logo-resized.png)

# ProGrad Lab | ProGrad Premier League








## What Should You Do
```
Fork this repo
Clone this repo
Practice Java JDBC - class and object, Statements, Connections and CRUD.
```

## How To Submit
```
Upon completion, run the following commands:

git add .
git commit -m "ProGrad ID"
git push origin master

And finally, create a pull request so your ProGrad Mentor (PM) can review your work.
```

## Instructions

1. ***Do not modify the entire code.***
2. ***Edit the code as per the instructions.***
3. ***Go to Java Resources -> src folder.***
4. ***You database connection code should exist inside the utlity package.***
5. ***Your CREATE, READ, UPDATE and DELETE code should exist inside the dao package.***
6. ***Once the progressions are completed follow the instructions to run the application and test your code.***
7. ***Add appropriate jars to your project directory.***
8. ***To add dependencies, right click on your project, select build path - configure build path - select libraries tab - select add external jars and add the downloaded jar files.***

## Required Dependencies
If you haven't downloaded OJDBC driver (ojdbc6.jar), then download using this link [https://www.oracle.com/database/technologies/jdbcdriver-ucp-downloads.html]

## Progression 0:
1. ***Right click on src folder and select new - file and name it as jdbc.properties.***
2. ***You can use the jdbc properties given below in the NOTE section.***

## Progression 1:

1. **Create a class called as `ConnectionManager` inside the utility package.**
2. **Create a method public static Connection getConnection() which returns a connection object.** 
3. **Use the method public static Properties loadPropertiesFile() to load the jdbc properties from the jdbc.properties file.**

## Progression 1:

1. **Create a class called as `Player` with below attributes,**
	- playerld- Long 
	- playerName- String 
2. **Include getter and setter methods for all the attributes.**
3. **Include constructor with below arguments public Player(playerld, playerName).**


## Progression 3:

1. **Create a dao-class called as `PlayerDAO` with below methods to handle all database related operations,**
	- **public List< Player > listAllPlayer() - Method used to fetch all the Player from players table belong to England team and returns the list of players.**
	- **Display the Players in ascending order based on name.**
	
## Progression 4:
1. **Create a controller called as Main inside the controller package.**
2. **Create appropriate objects for the Player and PlayerDAO.**
3. **Refer sample output for output format.**
	

_DAO Layer - Data access layer provides the gateway to create, reterive, update or delete any data in the database. All database related operations will be performed in this layer._


![1 2](https://user-images.githubusercontent.com/61002120/76416050-5807d380-63c0-11ea-8d52-9e8750e800f9.png)


### Note:

Use the below code to retreive the connection details from jdbc.properties to establish connection
```
public static Properties loadPropertiesFile() throws Exception {
	Properties prop = new Properties();	
	InputStream in = ConnectionManager.class.getClassLoader().getResourceAsStream("jdbc.properties");
	prop.load(in);
	in.close(); 
	return prop;
}
```
Create a file called as jdbc.properites. To create a file right click on the application - new - file - name the file as jdbc.properties.
```
jdbc.properties
#JDBC properties entry for ORACLE server
driver = oracle.jdbc.OracleDriver
url=jdbc:oracle:thin:@localhost:1521:xe
username=your_username
password=your_password

```

## Sample Output
``` 
List of all Player from Kolkata city 
1) Ankit Rajpoot 
2) Brad Hogg 
3) Chris Lynn 
4) Colin Munro 
5) Gautam Gambhir 
6) Jason Holder 
7) John Hastings 
```

![Image description](https://i1.faceprep.in/ProGrad/face-logo-resized.png)

# ProGrad Lab | ProGrad Premier League


## Progression 1:

Create Main.java with main method Create Player.java domain class with below attributes, 
```
playerld- Long 
playerName- String 
```


## Progression 2:

Include getter and setter method for all the attributes Include constructor with below arguments 
`public Player(playerld, playerName)`


## Progression 3:

Create PlayerDAO.java with below methods to handle all database related operations public List<Player> listAllPlayer() - Method used to fetch all the Player from players table belong to England team and returns the list of players. Display the Players in ascending order based on name. 

_DAO Layer - Data access layer provides the gateway to create, reterive, update or delete any data in the database. All database related operations will be performed in this layer. _



![1 2](https://user-images.githubusercontent.com/61002120/76416050-5807d380-63c0-11ea-8d52-9e8750e800f9.png)



### Note:

Use the below code to retreive the connection details from mysql.properties to establish connection
```
public static Properties loadPropertiesFile() throws Exception {
	Properties prop = new Properties();	
	InputStream in = ConnectionManager.class.getClassLoader().getResourceAsStream("jdbc.properties");
	prop.load(in);
	in.close(); 
	return prop;
}
```    

# Technical Challenge for Juniors

For this challenge, you are going to use the API of [bored API](https://www.boredapi.com/). This API gives us a random activity to do every time you call it, for example, if you make the following call:

```
GET https://www.boredapi.com/api/activity
```
You will get a response like this:

```json
{
    "activity": "Learn Express.js",
    "type": "education",
    "participants": 1,
    "price": 0.1,
    "link": "https://expressjs.com/",
    "key": "3943509",
    "accessibility": 0.1
}
```
For more details, check the [documentation](https://www.boredapi.com/documentation).

 We will use this API to create a simple program that will give us a random activity to do.

## Instructions
Clone this repository and create a new one on your own GitHub account. When you are done, please send us the link to your repository.

## Tasks

### API Calls
1. Create an API wrapper for bored API, This wrapper should have a method that returns a random activity, and should accept parameters to filter the activities by type, number of participants, price range, and accessibility range.

### Database
2. Write a class that will save the activities in a database, this class should have a method that will accept the activity as a parameter

3. Add another method that will return the latest activities saved in the database. The database can be any database you want (e.g. SQLite), but it should be a relational database.

### Command line program
3. Create a simple command line program that will use the API wrapper and the database class to get a random activity and save it in the database. The program should accept parameters to filter the activities by type, number of participants, price range, and accessibility range. The command should look like this:
    
    ```bash
    my_program new --type education --participants 1 --price_min 0.1 --price_max 30 --accessibility_min 0.1 --accessibility_max 0.5
    ```
This command should get a random activity with the type education, 1 participant, a price of 0.1, and an accessibility of 0.1 and save it in the database.


4. Add another command to the program that will return the last activities saved in the database. The command should look like this:
    
    ```bash
    my_program list
    ```
This command should return the last 5 activities saved in the database.


## Extra points
 - Make sure that you include a dependencies file (requirements.txt, gemfile, package.json, etc.). But don't include any virtual environment or packages installed in your repository.
 - Add unit tests for your work.


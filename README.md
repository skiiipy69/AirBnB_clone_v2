**Note**:

The AirBnB project arc, part of Holberton School's [Higher-level Programming track](https://github.com/allelomorph/holbertonschool-higher_level_programming/), spans 7 assignments and 4 repositories. All were team projects. In order to practice navigating an existing code base, for v2 through v4, students began that revision by forking a senior student team's repository for the previous version.

* [`AirBnB_clone`](https://github.com/allelomorph/AirBnB_clone/)
  * [(263) 0x00. AirBnB clone - The console](https://github.com/allelomorph/AirBnB_clone/blob/master/PROJECT_0x00.md)
  * [(268) 0x01. AirBnB clone - Web static](https://github.com/allelomorph/AirBnB_clone/blob/master/PROJECT_0x01.md)
* `AirBnB_clone_v2`
  * [(289) 0x02. AirBnB clone - MySQL](./PROJECT_0x02.md)
  * [(288) 0x03. AirBnB clone - Deploy static](./PROJECT_0x03.md)
  * [(290) 0x04. AirBnB clone - Web framework](./PROJECT_0x04.md)
* [`AirBnB_clone_v3`](https://github.com/allelomorph/AirBnB_clone_v3/)
  * [(301) 0x05. AirBnB clone - RESTful API](https://github.com/allelomorph/AirBnB_clone_v3/blob/master/PROJECT_0x05.md)
* [`AirBnB_clone_v4`](https://github.com/allelomorph/AirBnB_clone_v4/)
  * [(309) 0x06. AirBnB clone - Web dynamic](https://github.com/allelomorph/AirBnB_clone_v4/blob/master/PROJECT_0x06.md)

What follows below is an edited version of the README appearing in the forked v1 repository.

---

<center> <h1>AirBnB clone - MySQL</h1> </center>

This repository contains the third stage of a student project to build a clone an early version of the AirBnB website. The first stage implemented a JSON based file storage system and a REPL console to manage these objects in storage. In the second project students built static HTML and CSS for the front end. This stage now implements a second data storage engine, this time in a MySQL database, and the ability to switch between both means of storage. A new challenge was introduced also introduced for this project: starting not with the student's completed work from the first two stages, but with that of a student of a prior cohort, to practice working with a pre-existing code base.

Original code base for this project can be found at [https://github.com/justinmajetich/AirBnB_clone](https://github.com/justinmajetich/AirBnB_clone)

---

<center><h3>Repository Contents by Project Task</h3> </center>

| Tasks | Files | Description |
| ----- | ----- | ------ |
| 0. Fork me if you can! | N/A | Fork original repo to implement new features |
| 1. Bug free! | [/tests](https://github.com/allelomorph/AirBnB_clone_v2/tree/master/tests) | Unit testing for all relevant `.py` files |
| 2. Console improvements | [./console.py](https://github.com/allelomorph/AirBnB_clone_v2/blob/master/console.py), [/models](https://github.com/allelomorph/AirBnB_clone_v2/tree/master/models), [/tests](https://github.com/allelomorph/AirBnB_clone_v2/tree/master/tests) |  |
| 3. MySQL setup development |  |  |
| 4. MySQL setup test |  |  |
| 5. Delete object |  |  |
| 6. DBStorage - States and Cities |  |  |
| 7. DBStorage - User |  |  |
| 8. DBStorage - Place |  |  |
| 9. DBStorage - Review |  |  |
| 10. DBStorage - Amenity... and BOOM! |  |  |
<br>
<br>
<center> <h2>General Use</h2> </center>

1. First clone this repository.

3. Once the repository is cloned locate the "console.py" file and run it as follows:
```
/AirBnB_clone$ ./console.py
```
4. When this command is run the following prompt should appear:
```
(hbnb)
```
5. This prompt designates you are in the "HBnB" console. There are a variety of commands available within the console program.

##### Commands
    * create - Creates an instance based on given class

    * destroy - Destroys an object based on class and UUID

    * show - Shows an object based on class and UUID

    * all - Shows all objects the program has access to, or all objects of a given class

    * update - Updates existing attributes an object based on class name and UUID

    * quit - Exits the program (EOF will as well)


##### Alternative Syntax
Users are able to issue a number of console command using an alternative syntax:

        Usage: <class_name>.<command>([<id>[name_arg value_arg]|[kwargs]])
Advanced syntax is implemented for the following commands:

    * all - Shows all objects the program has access to, or all objects of a given class

        * count - Return number of object instances by class

    * show - Shows an object based on class and UUID

        * destroy - Destroys an object based on class and UUID

    * update - Updates existing attributes an object based on class name and UUID

<br>
<br>
<center> <h2>Examples</h2> </center>
<h3>Primary Command Syntax</h3>

###### Example 0: Create an object
Usage: create <class_name>
```
(hbnb) create BaseModel
```
```
(hbnb) create BaseModel
3aa5babc-efb6-4041-bfe9-3cc9727588f8
(hbnb)
```
###### Example 1: Show an object
Usage: show <class_name> <_id>

```
(hbnb) show BaseModel 3aa5babc-efb6-4041-bfe9-3cc9727588f8
[BaseModel] (3aa5babc-efb6-4041-bfe9-3cc9727588f8) {'id': '3aa5babc-efb6-4041-bfe9-3cc9727588f8', 'created_at': datetime.datetime(2020, 2, 18, 14, 21, 12, 96959),
'updated_at': datetime.datetime(2020, 2, 18, 14, 21, 12, 96971)}
(hbnb)
```
###### Example 2: Destroy an object
Usage: destroy <class_name> <_id>
```
(hbnb) destroy BaseModel 3aa5babc-efb6-4041-bfe9-3cc9727588f8
(hbnb) show BaseModel 3aa5babc-efb6-4041-bfe9-3cc9727588f8
** no instance found **
(hbnb)
```
###### Example 3: Update an object
Usage: update <class_name> <_id>
```
(hbnb) update BaseModel b405fc64-9724-498f-b405-e4071c3d857f first_name "person"
(hbnb) show BaseModel b405fc64-9724-498f-b405-e4071c3d857f
[BaseModel] (b405fc64-9724-498f-b405-e4071c3d857f) {'id': 'b405fc64-9724-498f-b405-e4071c3d857f', 'created_at': datetime.datetime(2020, 2, 18, 14, 33, 45, 729889),
'updated_at': datetime.datetime(2020, 2, 18, 14, 33, 45, 729907), 'first_name': 'person'}
(hbnb)
```
<h3>Alternative Syntax</h3>

###### Example 0: Show all User objects
Usage: <class_name>.all()
```
(hbnb) User.all()
["[User] (99f45908-1d17-46d1-9dd2-b7571128115b) {'updated_at': datetime.datetime(2020, 2, 19, 21, 47, 34, 92071), 'id': '99f45908-1d17-46d1-9dd2-b7571128115b', 'created_at': datetime.datetime(2020, 2, 19, 21, 47, 34, 92056)}", "[User] (98bea5de-9cb0-4d78-8a9d-c4de03521c30) {'updated_at': datetime.datetime(2020, 2, 19, 21, 47, 29, 134362), 'id': '98bea5de-9cb0-4d78-8a9d-c4de03521c30', 'created_at': datetime.datetime(2020, 2, 19, 21, 47, 29, 134343)}"]
```

###### Example 1: Destroy a User
Usage: <class_name>.destroy(<_id>)
```
(hbnb) User.destroy("99f45908-1d17-46d1-9dd2-b7571128115b")
(hbnb)
(hbnb) User.all()
(hbnb) ["[User] (98bea5de-9cb0-4d78-8a9d-c4de03521c30) {'updated_at': datetime.datetime(2020, 2, 19, 21, 47, 29, 134362), 'id': '98bea5de-9cb0-4d78-8a9d-c4de03521c30', 'created_at': datetime.datetime(2020, 2, 19, 21, 47, 29, 134343)}"]
```
###### Example 2: Update User (by attribute)
Usage: <class_name>.update(<_id>, <attribute_name>, <attribute_value>)
```
(hbnb) User.update("98bea5de-9cb0-4d78-8a9d-c4de03521c30", name "Todd the Toad")
(hbnb)
(hbnb) User.all()
(hbnb) ["[User] (98bea5de-9cb0-4d78-8a9d-c4de03521c30) {'updated_at': datetime.datetime(2020, 2, 19, 21, 47, 29, 134362), 'id': '98bea5de-9cb0-4d78-8a9d-c4de03521c30', 'name': 'Todd the Toad', 'created_at': datetime.datetime(2020, 2, 19, 21, 47, 29, 134343)}"]
```
###### Example 3: Update User (by dictionary)
Usage: <class_name>.update(<_id>, <dictionary>)
```
(hbnb) User.update("98bea5de-9cb0-4d78-8a9d-c4de03521c30", {'name': 'Fred the Frog', 'age': 9})
(hbnb)
(hbnb) User.all()
(hbnb) ["[User] (98bea5de-9cb0-4d78-8a9d-c4de03521c30) {'updated_at': datetime.datetime(2020, 2, 19, 21, 47, 29, 134362), 'name': 'Fred the Frog', 'age': 9, 'id': '98bea5de-9cb0-4d78-8a9d-c4de03521c30', 'created_at': datetime.datetime(2020, 2, 19, 21, 47, 29, 134343)}"]

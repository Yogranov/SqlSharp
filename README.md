SqlSharp makes the integration with SQL easy then ever.
<br>
Reading from DB example:
```
DataTable data = new MyDB().Where("Id", "1").Where("FirstName", "Yog")
.OrWhere("Email", "yog@gmail.com").Limit(2).Sort("DESC", "FirstName", "LastName").Get("Users","FirstName","LastName");
```


Writing to DB example:
```
var dbList = new List<DbListAdapter>();

dbList.Add(new DbListAdapter("FirstName", registerFirstName.Text));
dbList.Add(new DbListAdapter("LastName", registerLastName.Text));
dbList.Add(new DbListAdapter("Email", registerEmail.Text));
dbList.Add(new DbListAdapter("Password", registerPassword.Text));

new MyDB().Insert("Users", dbList);
```

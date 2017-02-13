var data = new MyDB ().Where ("Id", id).Limit(1).Get("Users");




var data = new MyDB().Where("Id", "1").Where("FirstName", "יוגב").OrWhere("Email", "asd").Limit(2).Sort("DESC", "FirstName", "LastName").Get("Users","FirstName","LastName");

            RptData.DataSource = data;
            RptData.DataBind ();



protected void BtnReg_Click(object sender, EventArgs e) {
            var dbList = new List<DbListAdapter>();

            dbList.Add(new DbListAdapter("FirstName", registerFirstName.Text));
            dbList.Add(new DbListAdapter("LastName", registerLastName.Text));
            dbList.Add(new DbListAdapter("Email", registerEmail.Text));
            dbList.Add(new DbListAdapter("Password", registerPassword.Text));

            new MyDB().Insert("Users", dbList);

        }
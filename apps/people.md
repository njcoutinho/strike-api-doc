# People
> Description goes here

## Get people
Returns all the people related to you in your account.

### Method
`GET /people`

### Example Request
`GET https://api.secure.strikebase.com/people?access_token='access_token'&format=json&show_all=1&is_archived=1`

### Parameters
#### Attributes
<table border="0">
	<tr>
		<td>
			<b>show_all</b><br/>
			<i>integer</i>
		</td>
		<td>
			Return all the active users in the account<br/>
			Allowed values (1)<br/> 
			Only admins have access
		</td>
	</tr>
	<tr>
		<td>
			<b>is_archived</b><br/>
			<i>integer</i>
		</td>
		<td>
			Return all archived and active users<br/>
			Allowed values (1)<br/>
			Default = NULL
		</td>
	</tr>	
</table>


		 

### Response
```json
{
   "count":2,
   "status":"success",
   "data":{
      "people":[
         {
            "id":"1",
            "company_id":"1",
            "fname":"Karen",
            "lname":"Williams",
            "gender":"f",
            "email":"karen@example.com",
            "is_account_holder":"1",
            "is_admin":"1",
            "timezone":"UP55",
            "designation":"Programmer",
            "company_name":"Acme",
            "picture":"",
            "country_id":null,
            "birthday":"Nov-26-2011",
            "joining_date":"Apr-13-2013",
            "tel_mobile":+911234567890,
            "tel_office":null,
            "tel_fax":null,
            "tel_home":null,
            "postalcode":"null",
            "city":"null",
            "is_archived":null,
            "is_lite":null,
            "is_deleted":null,
            "country_name":null,
            "timezone_data":"(UTC +5:30) Indian Standard Time, Sri Lanka Time",
            "is_verified":1,
            "projects":[
               {
                  "project_id":"1",
                  "name":"Website Redesign"
               }
            ]
         },
		 {
            "id":"2",
            "company_id":"1",
            "fname":"Zack",
            "lname":"Coulson",
            "gender":"m",
            "email":"zack@example.com",
            "is_account_holder":"0",
            "is_admin":"1",
            "timezone":"UP55",
            "designation":"Project Manager",
            "company_name":"Acme",
            "picture":"",
            "country_id":null,
            "birthday":"Nov-26-2011",
            "joining_date":"Jan-13-2010",
            "tel_mobile":+911234567890,
            "tel_office":null,
            "tel_fax":null,
            "tel_home":null,
            "postalcode":"null",
            "city":"null",
            "is_archived":null,
            "is_deleted":null,
            "country_name":null,
            "timezone_data":"(UTC +5:30) Indian Standard Time, Sri Lanka Time",
            "is_verified":1,
            "projects":[
               {
                  "project_id":"1",
                  "name":"Website Redesign"
               }
            ]
         },
      ]
   }
}
```

## Create user
Add a new user to your account

### Method
`POST /people`

### Example Request
``

### Parameters
#### Attributes
<table border="0">
	<tr>
		<td>
			<b>company_id</b><br/>
			<i>integer</i>
		</td>
		<td>
			Company id which the user will be added to<br/>
			<i>required</i>
		</td>
	</tr>
	<tr>
		<td>
			<b>project_ids</b><br/>
			<i>integer</i>
		</td>
		<td>
			Project id which the user will be added to
		</td>
	</tr>
	<tr>
		<td>
			<b>fname</b><br/>
			<i>string</i>
		</td>
		<td>
			User's first name<br/>
			<i>required</i>
		</td>
	</tr>
	<tr>
		<td>
			<b>lname</b><br/>
			<i>string</i>
		</td>
		<td>
			User's last name<br/>
			<i>required</i>
		</td>
	</tr>	
	<tr>
		<td>
			<b>email</b><br/>
			<i>string</i>
		</td>
		<td>
			User's email name<br/>
			<i>required</i>
		</td>
	</tr>
<tr>
		<td>
			<b>timezone</b><br/>
			<i>string</i>
		</td>
		<td>
			User's timezone<br/>
			<i>required</i>
		</td>
	</tr>	
	<tr>
		<td>
			<b>designation</b><br/>
			<i>string</i>
		</td>
		<td>
			User's designation<br/>
			<i>required</i>
		</td>
	</tr>	
	<tr>
		<td>
			<b>dateofbirth</b><br/>
			<i>string</i>
		</td>
		<td>
			User's date of birth
			
		</td>
	</tr>
<tr>
		<td>
			<b>gender</b><br/>
			<i>string</i>
		</td>
		<td>
			User gender<br/> 
			Allowed values m,f
			
		</td>
	</tr>	
	<tr>
		<td>
			<b>assign_is_admin</b><br/>
			<i>integer</i>
		</td>
		<td>
			To make a user an Account manage<br/>
			Allowed values = (1 or 0)<br/>
			Default = 0
			
		</td>
	</tr>
	
	<tr>
		<td>
			<b>assign_is_account_holder</b><br/>
			<i>integer</i>
		</td>
		<td>
			To make a user an Account Holder<br/>
			Allowed values = (1 or 0)<br/>
			Default = 0
			
		</td>
	</tr>
</table>


		 

### Response
```json
{
"status":"success","inserted_id":10
}
```

## Delete/Archive user
Delete/Archive users from account

### Method
`DELETE /people/1/`

### Parameters
#### Attributes
<table border="0">
	<tr>
		<td>
			<b>id</b><br/>
			<i>interger</i>
		</td>
		<td>
			User id to be archived/deleted 
		</td>
	</tr>
	<tr>
		<td>
			<b>permanent_delete</b><br/>
			<i>interger</i>
		</td>
		<td>
			To permanently delete a user
			<br/>Allowed values (1 or 0)
			<br/>Default = 0
		</td>
	</tr>	
</table>

### Response
```json
{
"status":"success"
}
```

## Unarchive user
Unarchive a user
### Method
`DELETE /people/id/undo`

### Parameters
#### Attributes
<table border="0">
	<tr>
		<td>
			<b>id</b><br/>
			<i>interger</i>
		</td>
		<td>
			User id to be unarchived
		</td>
	</tr>
	
</table>

### Response
```json
{
"status":"success"
}
```

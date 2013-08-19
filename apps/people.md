# People
> Description goes here

## Get people
Returns all the people related to you in your account.

### Example Request
`GET /people`

### Parameters
#### Attributes
<table border="0">
	<tr>
		<td>
			<b>show_all</b><br/>
			<i>integer</i>
		</td>
		<td>
			Return all the active users in the account,allowed values (1) (Only admins have access to this) 
		</td>
	</tr>
	<tr>
		<td>
			<b>is_archived</b><br/>
			<i>integer</i>
		</td>
		<td>
			Return all archived and active users, allowed values (1). Default = NULL
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
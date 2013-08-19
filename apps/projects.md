# Projects
> Description goes here

## GET /projects
Returns all the active projects from your account.

### Example Request
`GET /projects`

### Parameters
#### Attributes
<table border="0">
	<tr>
		<td>
			<b>format</b><br/>
			<i>string</i>
		</td>
		<td>
			Response format, allowed types (php,json, xml, jsonp). Default = json
		</td>
	</tr>
	<tr>
		<td>
			<b>is_archived</b><br/>
			<i>integer</i>
		</td>
		<td>
			Return all archived projects, allowed values (1). Default = NULL
		</td>
	</tr>	
</table>


		 

### Response
```json
{
   "count":2,
   "status":"success",
   "account_curr_project_limit":10,
   "account_curr_plan":"MICRO",
   "active_projects":"2",
   "data":{
      "projects":[
         {
            "id":"1",
            "parent_id":null,
            "name":"Website Redesign",
            "plan_start":"2013-08-16",
            "plan_completion":"2013-08-30",
            "status":"2",
            "last_update_id":null,
            "condition":"3",
            "user_id":"2053",
            "updated_time_stamp":"2013-08-16T09:02:13+05:30",
            "created_timestamp":"2012-08-15T06:30:00+05:30",
            "is_archived":null,
            "people_count":2,
            "user_info":[
               
            ],
            "users_count":2,
            "company_count":2,
            "company_info":[
              
            ],
            "sub_projects":[

            ]
         },
		 {
            "id":"1",
            "parent_id":null,
            "name":"StrikeBase",
            "plan_start":"2013-08-11",
            "plan_completion":"2013-09-30",
            "status":"2",
            "last_update_id":null,
            "condition":"3",
            "user_id":"2053",
            "updated_time_stamp":"2013-08-126T09:02:13+05:30",
            "created_timestamp":"2012-08-11T06:30:00+05:30",
            "is_archived":null,
            "people_count":2,
            "user_info":[
               
            ],
            "users_count":2,
            "company_count":2,
            "company_info":[
              
            ],
            "sub_projects":[

            ]
         }
      ]
   }
}

```




## GET /projects/id
Returns a specific project

### Example Request
`GET /projects/1`

### Parameters
#### Attributes
<table border="0">
	<tr>
		<td>
			<b>format</b><br/>
			<i>string</i>
		</td>
		<td>
			Response format, allowed types (php,json, xml, jsonp). Default = json
		</td>
	</tr>
	<tr>
		<td>
			<b>id</b><br/>
			<i>integer</i>
		</td>
		<td>
			Project id 
		</td>
	</tr>	
</table>


		 

### Response
```json
{
   "count":1,
   "status":"success",
   "data":{
      "id":"1",
      "name":"Website Redesign",
      "plan_start":"2013-08-16",
      "plan_completion":"2013-08-30",
      "status":"2",
      "created_by":{
         "id":"6",
         "fname":"Karen",
         "lname":"Williams",
         "email":"karen@example.com",
		 "company_id":"1",
         "is_admin":"1",
         "company_info":{
         "id":"1",
            "name":"Acme"
         },
         "is_connected":1
      },
      "custom_fields":[

      ],
      "activity":[
    
      ],
      "company_info":{
         "1":{
            "id":"1",
            "name":"Acme"
         }
      },
      "is_archived":null,
      "people_count":10
   }
}
```

## POST /projects/id/archive
To archive a specific project

### Example Request
`POST /projects/1/archive`

### Parameters
#### Attributes
<table border="0">
	<tr>
		<td>
			<b>id</b><br/>
			<i>integer</i>
		</td>
		<td>
			Project id 
		</td>
	</tr>	
</table>

### Response
```json
{ 
"status":"success",
"archived_project_id":"5"
}
```

## POST /projects/id/unarchive
To unarchive a specific project

### Example Request
`POST /projects/1/unarchive`

### Parameters
#### Attributes
<table border="0">
	<tr>
		<td>
			<b>id</b><br/>
			<i>integer</i>
		</td>
		<td>
			Project id 
		</td>
	</tr>	
</table>

### Response
```json
{ 
"status":"success",
"deleted_project_id":"5",
"connected_users" : "15_20_12_9" }
}
```




## DELETE /projects/id
Deletes a specific project. Only admins have acess.

### Example Request
`DELETE /projects/1`

### Parameters
#### Attributes
<table border="0">
	<tr>
		<td>
			<b>id</b><br/>
			<i>integer</i>
		</td>
		<td>
			Project id 
		</td>
	</tr>	
</table>

### Response
```json
{
"status":"success",
"deleted_project_id":"5"
}
```

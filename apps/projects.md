# Projects
> Description goes here

## Get projects
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




## Get project
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

## People on a project
To return a list of all the users on a project

### Example Request
`POST /projects/1/people`

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
   "count":2,
   "status":"success",
   "data":{
      "people":[
         {
            "id":"9",
            "dst":null,
            "fname":"Michael",
            "lname":"Scott",
            "email":"michael@acme.com",
            "gender":"m",
            "picture":"",
            "designation":"Project Manager",
            "is_archived":null,
            "timezone":"UP55",
            "company_id":"1",
           
            "is_admin":"1",
           
            "tel_mobile":"",
            "tel_office":"",
            "tel_fax":"",
            "tel_home":"",
            
            "company_info":{
               "id":"1",
               "name":"Acme"
            },
            "is_connected":1,
          
         },
		 {
            "id":"9",
            "dst":null,
            "fname":"Karen",
            "lname":"Williams",
            "email":"karen@example.com",
            "gender":"m",
            "picture":"",
            "designation":"Design Head",
            "is_archived":null,
            "timezone":"UP55",
            "company_id":"1",
            "is_lite":null,
            "is_admin":"1",
            "role":null,
            "tel_mobile":"",
            "tel_office":"",
            "tel_fax":"",
            "tel_home":"",
           
            "company_info":{
               "id":"1",
               "name":"Acme"
            },
            "is_connected":1,
           
         }
		 
      ]
	}
}
```

## Create project
To create a new project

### Example Request
`POST /projects`

### Parameters
#### Attributes
<table border="0">
	<tr>
		<td>
			<b>name</b><br/>
			<i>string</i>
		</td>
		<td>
			Project name 
		</td>
	</tr>
<tr>
		<td>
			<b>plan_start</b><br/>
			<i>date</i>
		</td>
		<td>
			Project planned start date
		</td>
	</tr>	
<tr>
		<td>
			<b>plan_completion</b><br/>
			<i>date</i>
		</td>
		<td>
			Project planned completion date
		</td>
	</tr>	
<tr>
		<td>
			<b>parent_id</b><br/>
			<i>integer</i>
		</td>
		<td>
			Parent project (while creating a sub-project, default = NULL) 
		</td>
	</tr>	
<tr>
		<td>
			<b>copy_people_project_id</b><br/>
			<i>integer</i>
		</td>
		<td>
			Project id from where the people should be copied over
		</td>
	</tr>	
</table>

### Response
```json
{ 
"status":"success",
"inserted_id":id, 
"name":"Alpha", 
"plan_start":"2013-06-17", 
"plan_completion":"2013-08-18", 
"parent_id":NULL, 
"data_status":"2", 
"user_ids":"20" 
}
```

## Update project
Update a project's details
### Example Request
`POST /project/id`

### Parameters
#### Attributes
<table border="0">
	<tr>
		<td>
			<b>name</b><br/>
			<i>string</i>
		</td>
		<td>
			Project name 
		</td>
	</tr>
<tr>
		<td>
			<b>plan_start</b><br/>
			<i>date</i>
		</td>
		<td>
			Project planned start date
		</td>
	</tr>	
<tr>
		<td>
			<b>plan_completion</b><br/>
			<i>date</i>
		</td>
		<td>
			Project planned completion date
		</td>
	</tr>	
<tr>
		<td>
			<b>parent_id</b><br/>
			<i>integer</i>
		</td>
		<td>
			Parent project (while creating a sub-project, default = NULL) 
		</td>
	</tr>	
<tr>
		<td>
			<b>copy_people_project_id</b><
			<i>integer</i>
		</td>
		<td>
			Project id from where the people should be copied over
		</td>
	</tr>	
</table>

### Response
```json
{ 
"status":"success",
"inserted_id":id, 
"name":"Alpha", 
"plan_start":"2013-06-17", 
"plan_completion":"2013-08-18", 
"parent_id":NULL, 
"data_status":"2", 
"user_ids":"20" 
}
```


## Archive project
To archive a specific project

### Example Request
`POST /projects/5/archive`

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

## Unarchive project
To unarchive a specific project

### Example Request
`POST /projects/5/unarchive`

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

## Upgrade a sub-project
Upgrades a sub-project to a main project

### Example Request
`POST /projects/1/upgrade`

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
"id" : "1" }
}
```




## Delete project
Deletes a specific project. Only admins have acess.

### Example Request
`DELETE /projects/5`

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

## Remove people from a project
Removes users on a project

### Example Request
`DELETE /projects/1/people`

### Parameters
#### Attributes
<table border="0">
	<tr>
		<td>
			<b>people_ids</b><br/>
			<i>String</i>
		</td>
		<td>
			User id, multiple users can be deleted by separating with underscores i.e. 1_2_3 
		</td>
	</tr>	
</table>

### Response
```json
{ 
"status":"success",
"user_ids":["1","2","3","6","5"],
"connected_users":"7_37_8_50_45_61_2201_10" 
}
```

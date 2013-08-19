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
            "created_timestamp":"2012-04-04T06:30:00+05:30",
            "is_archived":null,
            "people_count":2,
            "user_info":[
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
                  "is_connected":1
               },
			   {
                  "id":"9",
                  "dst":null,
                  "fname":"Holly",
                  "lname":"Flax",
                  "email":"holly@example.com",
                  "gender":"m",
                  "picture":"",
                  "designation":"Developer",
                  "is_archived":null,
                  "timezone":"UP55",
                  "company_id":"1",
                  "is_admin":"1",
                  "tel_mobile":"",
                  "tel_office":"",
                  "tel_fax":"",
                  "tel_home":"",
                  "company_info":{
                     "id":"2",
                     "name":"Dunder Mifflin"
                  },
                  "is_connected":1
               }
            ],
            "users_count":2,
            "company_count":2,
            "company_info":[
               {
                  "id":"1",
                  "name":"Acme"
               },
               {
                  "id":"2",
                  "name":"Dunder Mifflin"
               }
              
              
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
```php
array(
	'count' => 1,
	'status' => 'success',
	'data' => array(
				'projects' => array(
								0 => array(
										'id'				=> '25',
										'parent_id'			=> NULL,
										'name'				=> 'Coffee shop website redesign',
										'plan_start' 		=> '',
										'plan_completion' 	=> '2014-05-16',
										'status' 			=> '2', 
										'last_update_id'	=> NULL,
										'condition' 		=> '1',
										'user_id' 			=> NULL, 
										'updated_time_stamp'=> '2013-07-20T10:18:45+05:30',
										'created_timestamp' => '2013-07-20T10:18:45+05:30',
										'is_archived' 		=> NULL,
										'people_count' 		=> 1,
										'user_info' 		=> array (),
										'sub_projects' 		=> array (),
										'custom_fields'		=> array(),
										'activity'			=> array(),
										last_update_id' 	=> '56',
										
										
								)
								
				)
	)
		
);
```


## DELETE /projects/id
Deletes a specific folder. Only admins have acess.

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

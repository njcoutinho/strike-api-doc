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
```php
array(
	'count' => 2,
	'status' => 'success',
	'account_curr_project_limit' => -1,
	'account_curr_plan' => 'ENTERPRISE',
	'results_total_count' => '20',
	'active_projects' => '20',
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
										'sub_projects' => array ()
								),
								1 => array(
										'id'				=> '26',
										'parent_id'			=> NULL,
										'name'				=> 'Acme iPhone App',
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
										'sub_projects' => array ()
										
								)
				)
	)
		
);
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

# Notes
> Description goes here

## Get Notes
Returns all the notes related to you in your account.

### Method
`GET /notes`

### Example Request
`GET  https://api.secure.strikebase.com/notes?access_token='access_token’&format=php`

### Parameters
#### Attributes

<table border="0">
	<tr>
		<td>
			<b>project_ids </b><br/>
			<i>integer</i>
		</td>
		<td>
			Get the notes from particular project <br/>
			Default = NULL
		</td>
	</tr>
	
	<tr>
		<td>
			<b>is_favourite  </b><br/>
			<i>integer</i>
		</td>
		<td>
			Get the favourite notes related to user <br/>
			Allowed values (1)<br/> 
			Default = NULL
		</td>
	</tr>
	
	<tr>
		<td>
			<b>is_public  </b><br/>
			<i>integer</i>
		</td>
		
		<td>
			Get the public notes related to user <br/>
			Allowed values (1)<br/> 
			Default = NULL
		</td>
	</tr>
	
	<tr>
		<td>
			<b>is_archived  </b><br/>
			<i>integer</i>
		</td>
		<td>
			Get all the archived notes related to user<br/>
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
        "notes":[
            {
                "note_id":"807",
                "is_read":1,
                "is_public":"1",
                "title":null,
                "is_favourite":null,
                "content":"Note by the admin for&nbsp; everyon eto edit",
                "content_id":"1763",
                "is_archived":null,
                "last_version_id":"1763",
                "shared_users":[
                ],
                "version_count":"1",
                "project_info":"Day Light Saving Project - day light sub",
                "creator_info":{
                    "id":"29",
                    "dst":null,
                    "fname":"Hari",
                    "lname":"Singh",
                    "email":"hari12@gdiz.com",
                    "gender":"m",
                    "picture":"https:\/\/s3.amazonaws.com\/strikebase_profile_TEST\/1_29_t1360986501.jpg",
                    "designation":"dev",
                    "is_archived":null,
                    "timezone":"UP55",
                    "company_id":"582",
                    "is_lite":null,
                    "is_admin":"1",
                    "role":null,
                    "tel_mobile":null,
                    "tel_office":null,
                    "tel_fax":null,
                    "tel_home":null,
                    "send_email_is_online":"1",
                    "company_info":{
                        "id":"582",
                        "name":"C-Company(don't delete user\/company)"
                    },
                    "is_connected":1
                },
                "created_time_stamp":"2013-08-09T13:24:21+05:30",
                "updated_time_stamp":"2013-08-09T13:24:21+05:30"
            },
            {
                "note_id":"806",
                "is_read":1,
                "is_public":"1",
                "title":null,
                "is_favourite":null,
                "content":"Public not on the sub project check this&nbsp;",
                "content_id":"1762",
                "is_archived":null,
                "last_version_id":"1762",
                "shared_users":[
                    {
                        "id":"29",
                        "dst":null,
                        "fname":"Hari",
                        "lname":"Singh",
                        "email":"hari12@gdiz.com",
                        "gender":"m",
                        "picture":"https:\/\/s3.amazonaws.com\/strikebase_profile_TEST\/1_29_t1360986501.jpg",
                        "designation":"dev",
                        "is_archived":null,
                        "timezone":"UP55",
                        "company_id":"582",
                        "is_lite":null,
                        "is_admin":"1",
                        "role":null,
                        "tel_mobile":null,
                        "tel_office":null,
                        "tel_fax":null,
                        "tel_home":null,
                        "send_email_is_online":"1",
                        "company_info":{
                            "id":"582",
                            "name":"C-Company(don't delete user\/company)"
                        },
                        "is_connected":1
                    }
                ],
                "version_count":"1",
                "project_info":"Day Light Saving Project - day light sub",
                "creator_info":{
                    "id":"2083",
                    "dst":null,
                    "fname":"Apple",
                    "lname":"Group",
                    "email":"applu@gdiz.com",
                    "gender":"m",
                    "picture":"https:\/\/s3.amazonaws.com\/strikebase_profile_TEST\/1_2083_t1363677441.jpg",
                    "designation":"Devepoler",
                    "is_archived":null,
                    "timezone":"UM7",
                    "company_id":"582",
                    "is_lite":null,
                    "is_admin":null,
                    "role":null,
                    "tel_mobile":null,
                    "tel_office":null,
                    "tel_fax":null,
                    "tel_home":null,
                    "send_email_is_online":"1",
                    "company_info":{
                        "id":"582",
                        "name":"C-Company(don't delete user\/company)"
                    },
                    "is_connected":1
                },
                "created_time_stamp":"2013-08-09T13:18:44+05:30",
                "updated_time_stamp":"2013-08-09T13:20:13+05:30"
            }
        ]
    }

}
```







## Get Notes Details
Returns the note details related to user in your account.

### Method
`GET /notes/id`

### Example Request
`GET  https://api.secure.strikebase.com/notes/249?access_token='access_token’&format=php`



### Response
```json
{

    "count":1,
    "status":"success",
    "data":{
        "id":"875",
        "note_id":"249",
        "method":"1",
        "auto_save":"1",
        "is_project_update":null,
        "is_archived":null,
        "is_public":null,
        "notes_permission":null,
        "updated_time_stamp":"2013-07-06T17:01:55+05:30",
        "project_id":"809",
        "project_info":{
            "id":"809",
            "name":"StrikeBase v2"
        },
        "content":"Base camp Data Push<br \/>\n<br \/>\n1) Database -&gt; import_map , import_cron , account_basecamp<br \/>\n2) cron_bc_model<br \/>\n3) cron helper<br \/>\n4) accounts_model<br \/>\n4) projects_model -- get_account_project_name , create<br \/>\n5) companies_model<br \/>\n6) People_model - create_people<br \/>\n7) threads_model<br \/>\n8) calendar_model<br \/>\n9) time_model<br \/>\n10) basecamp controller<br \/>",
        "version":"3",
        "created_time_stamp":"2013-07-06T16:32:31+05:30",
        "shared_user":[
        ],
        "creator_info":{
            "id":"136",
            "dst":null,
            "fname":"Swapnil",
            "lname":"Bangad",
            "email":"swapnil@gdiz.com",
            "gender":"m",
            "picture":"https:\/\/d2zc3me2o4gzwx.cloudfront.net\/4_136_t1366804845.jpg",
            "designation":"API Manager",
            "is_archived":null,
            "timezone":"UP55",
            "company_id":"58",
            "is_lite":null,
            "is_admin":null,
            "role":"128",
            "tel_mobile":"+919420859733",
            "tel_office":null,
            "tel_fax":null,
            "tel_home":null,
            "send_email_is_online":"1",
            "company_info":{
                "id":"58",
                "name":"GDiz"
            },
            "is_connected":1
        },
        "activity_count":3,
        "history":[
            {
                "id":"174088",
                "element_id":"249",
                "user_id":"136",
                "type":"23",
                "project_id":"809",
                "pulse_id":"171509",
                "is_update":"1",
                "content":"{\"action\":2301,\"note_id\":\"249\",\"note_content_id\":\"875\",\"version\":\"3\"}",
                "action_id":"2301",
                "source":"3",
                "create_date":"2013-07-06T17:01:55+05:30",
                "processes_count":0,
                "posted_by":{
                    "id":"136",
                    "fname":"Swapnil",
                    "lname":"Bangad",
                    "name":"Swapnil Bangad",
                    "picture":"https:\/\/d2zc3me2o4gzwx.cloudfront.net\/4_136_t1366804845.jpg",
                    "designation":"API Manager",
                    "gender":"m"
                },
                "details":{
                    "action":2301,
                    "content":{
                        "content":"%s by %s",
                        "params":[
                            [
                                "Version 3",
                                "bu",
                                23,
                                "875",
                                "",
                                ""
                            ],
                            [
                                "Swapnil Bangad",
                                "b",
                                6,
                                "136",
                                "He",
                                ""
                            ]
                        ],
                        "processes":[
                        ]
                    }
                },
                "time_stamp":"2013-07-06T17:01:55+05:30",
                "project_name":"StrikeBase v2",
                "action":"2301",
                "parent_project":null,
                "is_archived":null,
                "likes_info":[
                ],
                "is_like":0,
                "likes_count":0
            },
            {
                "id":"174087",
                "element_id":"249",
                "user_id":"136",
                "type":"23",
                "project_id":"809",
                "pulse_id":"171509",
                "is_update":"1",
                "content":"{\"action\":2301,\"note_id\":\"249\",\"note_content_id\":\"874\",\"version\":\"2\"}",
                "action_id":"2301",
                "source":"3",
                "create_date":"2013-07-06T16:56:09+05:30",
                "processes_count":0,
                "posted_by":{
                    "id":"136",
                    "fname":"Swapnil",
                    "lname":"Bangad",
                    "name":"Swapnil Bangad",
                    "picture":"https:\/\/d2zc3me2o4gzwx.cloudfront.net\/4_136_t1366804845.jpg",
                    "designation":"API Manager",
                    "gender":"m"
                },
                "details":{
                    "action":2301,
                    "content":{
                        "content":"%s by %s",
                        "params":[
                            [
                                "Version 2",
                                "bu",
                                23,
                                "874",
                                "",
                                ""
                            ],
                            [
                                "Swapnil Bangad",
                                "b",
                                6,
                                "136",
                                "He",
                                ""
                            ]
                        ],
                        "processes":[
                        ]
                    }
                },
                "time_stamp":"2013-07-06T16:56:09+05:30",
                "project_name":"StrikeBase v2",
                "action":"2301",
                "parent_project":null,
                "is_archived":null,
                "likes_info":[
                ],
                "is_like":0,
                "likes_count":0
            }
        ],
        "last_comment_id":"174153"
    }

}
```




## Get Notes Versions
Returns the particular version of note related to user in your account.

### Method
`GET /notes/id/version/version_id`

### Example Request
`GET  https://api.secure.strikebase.com/notes/344/version/1391?access_token='access_token’&format=php`



### Response
```json
{

    "data":{
        "is_latest_version":null,
        "is_public":null,
        "version_id":"1391",
        "creator_id":"136",
        "note_id":"344",
        "is_read":"1",
        "is_favourite":"1",
        "auto_save":null,
        "content":"Calendar<br \/>\n\/calendar<br \/>\n<br \/>\n<br \/>\nType: GET<br \/>\n<br \/>\nDescription : To get calendar Events to&nbsp; which&nbsp; user belongs;",
        "created_time_stamp":"2013-07-26 06:03:04",
        "updated_time_stamp":"2013-07-26 06:03:04",
        "project_info":{
            "id":"809",
            "name":"StrikeBase v2"
        }
    },
    "count":1,
    "status":"success"

}
```


## Get Notes Comments
Returns the comments particular note related to user in your account.

### Method
`GET /notes/id/comments`

### Example Request
`GET  https://api.secure.strikebase.com/notes/626/comments?access_token='access_token’&format=php&last_comment_id= 84318`

#### Attributes

<table border="0">
	<tr>
		<td>
			<b>last_comment_id </b><br/>
			<i>integer</i>
		</td>
		
		<td>
			Get all the comments <br/>
			required<br/>
			Default = NULL
		</td>
	</tr>
</table>

### Response
```json
{

  (
	  'count' => 1,
	  'status' => 'success',
	  'data' => 
	  array 
	  (
		'last_comment_id' => '84318',
		'note_id' => '626',
		'type' => 23,
		'comments_count' => 14,
		'history' => 
		array 
		(
		  0 => 
		  array 
		  (
			'id' => '84328',
			'element_id' => '626',
			'user_id' => '22',
			'type' => '23',
			'project_id' => '2223',
			'pulse_id' => '111639',
			'is_update' => '1',
			'content' => '{"action":2308,"note_id":"626","note_content_id":"1434","version":"3","old_project":"2223","old_project_name":"Appnostic - Apnostic demo","new_project":null,"new_project_name":null}',
			'action_id' => '2308',
			'source' => '1',
			'create_date' => '2013-07-30T13:42:28+03:00',
			'processes_count' => 0,
			'posted_by' => 
			array (
			  'id' => '22',
			  'fname' => 'Suryakant',
			  'lname' => '1',
			  'name' => 'Suryakant 1',
			  'picture' => 'https://d2zc3me2o4gzwx.cloudfront.net/default_15.jpg',
			  'designation' => 'Developer',
			  'gender' => 'm',
			),
			'details' => 
			array (
			  'action' => 2308,
			  'content' => 
			  array 
			  (
					'content' => '%s updated  project of this note to %s',
					'params' => 
					array 
					(
					  0 => 
					  array 
					  (
							0 => 'Suryakant 1',
							1 => 'b',
							2 => 6,
							3 => '22',
							4 => 'He',
							5 => '',
					  ),
					  1 => 
					  array 
					  (
							0 => 'None',
							1 => 'b',
							2 => '',
							3 => '',
							4 => '',
							5 => '',
					  ),
					),
					'processes' => 
					array (
					),
			  ),
			),
			'time_stamp' => '2013-07-30T13:42:28+03:00',
			'project_name' => 'Appnostic - Apnostic demo',
			'action' => '2308',
			'parent_project' => NULL,
			'is_archived' => NULL,
		  ),
		),
	  ),
	)
}
```


## Create notes
Add a new note to your account

### Method
`POST /notes`

### Example Request
`POST  : https://api.secure.strikebase.com/notes?access_token='access_token'&format=json`

### Parameters
#### Attributes

<table border="0">
	<tr>
		<td>
			<b>content</b><br/>
			<i>string</i>
		</td>
		<td>
			Data to be passed  in note<br/>
			required
		</td>
	</tr>
	
	<tr>
		<td>
			<b>project_ids</b><br/>
			<i>integer</i>
		</td>
		<td>
			Project id to which the note will be added to<br/>
		</td>
	</tr>
	
	<tr>
		<td>
			<b>is_public </b><br/>
			<i>integer</i>
		</td>
		<td>
			To make the note as public <br/>
			Allowed values (1)<br/> 
			Default = NULL
		</td>
	</tr>
	
</table>

### Response
```json
{
	"note_id":633,
	"status":"success"
} 
```



## Update notes
Update a particular note to your account

### Method
`POST /notes/id`

### Example Request
`POST  : https://api.secure.strikebase.com/notes/633?access_token='access_token'&format=json`

### Parameters
#### Attributes

<table border="0">
	<tr>
		<td>
			<b>content</b><br/>
			<i>string</i>
		</td>
		<td>
			Data to be passed  in note<br/>
			required
		</td>
	</tr>
	
	<tr>
		<td>
			<b>project_ids</b><br/>
			<i>integer</i>
		</td>
		<td>
			Project id to which the note will be updated to<br/>
		</td>
	</tr>
	
	<tr>
		<td>
			<b>is_public </b><br/>
			<i>integer</i>
		</td>
		<td>
			To make the note as public <br/>
			Allowed values (1)<br/> 
			Default = NULL
		</td>
	</tr>
	
	<tr>
		<td>
			<b>is_private </b><br/>
			<i>integer</i>
		</td>
		<td>
			To make the note as private <br/>
			Allowed values (1)<br/> 
			Default = NULL
		</td>
	</tr>
	
</table>

### Response
```json
{
	"note_id":633,
	"status":"success"
} 
```



## Share notes
To share a private note from your account

### Method
`POST /notes/id/share`

### Example Request
`POST  : https://api.secure.strikebase.com/notes/633/share?access_token='access_token'&format=json`

### Parameters
#### Attributes

<table border="0">
	<tr>
		<td>
			<b>people_ids</b><br/>
			<i>string</i>
		</td>
		<td>
			People ids to be passed to be shared<br/>
			required<br/>
			Example : people_ids = '1_2_3_4'
		</td>
	</tr>
</table>

### Response
```json
{
	"status":"success"
} 
```





## Mark and unmark note as favourite
To Mark and unmark note as favourite from your account

### Method
`POST /notes/id/mark_as_favourite`

### Example Request
`POST  : https://api.secure.strikebase.com/notes/633/mark_as_favourite?access_token='access_token'&format=json`

### Parameters
#### Attributes

<table border="0">
	<tr>
		<td>
			<b>unmark</b><br/>
			<i>integer</i>
		</td>
		<td>
			To unmark note as favourite<br/>
			Allowed values (1)<br/> 
			Default = NULL
		</td>
	</tr>
</table>

### Response
```json
{
	"status":"success"
} 
```



## Delete note
To delete the note permanently from your account

### Method
`DELETE /notes/id/content`

### Example Request
`DELETE  : https://api.secure.strikebase.com/notes/633/content?access_token='access_token'&format=json`


### Response
```json
{
	"status":"success"
} 
```


## Archive note
To archive the note from your account

### Method
`DELETE /notes/id/content/content_id`

### Example Request
`DELETE  : https://api.secure.strikebase.com/notes/633/content/365?access_token='access_token'&format=json`


### Response
```json
{
	"status":"success"
} 
```



## Unshare note
To remove people the private note from your account

### Method
`DELETE /notes/id/unshared`

### Example Request
`DELETE  : https://api.secure.strikebase.com/notes/633/unshared?access_token='access_token'&format=json`

<table border="0">
	<tr>
		<td>
			<b>people_ids</b><br/>
			<i>string</i>
		</td>
		<td>
			People ids to be passed to be unshared<br/>
			required<br/>
			Example : people_ids = '1_2_3_4'
		</td>
	</tr>
</table>

### Response
```json
{
	"status":"success"
} 
```


## Unarchive note
To unarchive the note from your account

### Method
`DELETE /notes/id/undo`

### Example Request
`DELETE  : https://api.secure.strikebase.com/notes/633/content/365?access_token='access_token'&format=json`


### Response
```json
{
	"status":"success"
} 
```
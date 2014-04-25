# Files
> Description goes here

## Get files
Return all the files related to user.

### Method
`GET /files`

### Example Request
`GET https://api.secure.strikebase.com/files?access_token='access_token'&format='json'`

### Parameters
#### Attributes

<table border="0">
	<tr>
		<td>
			<b>project_ids</b><br/>
			<i>integer</i>
		</td>	
		<td>
			Return all files related to project<br/>
			Default = NULL
		</td>
	</tr>
	
	
	<tr>
		<td>
			<b>parent_id</b><br/>
			<i>integer</i>
		</td>	
		<td>
			Return all files inside the parent folder<br/>
			Default = NULL
		</td>
	</tr>
	
	<tr>
		<td>
			<b>show_deleted</b><br/>
			<i>integer</i>
		</td>	
		<td>
			Return all archived and active folders related to user<br/>
			Allowed values(1)<br/>
			Default = NULL
		</td>
	</tr>
	
	
	<tr>
		<td>
			<b>hide_projects</b><br/>
			<i>integer</i>
		</td>	
		<td>
			Return all files and folder at root level<br/>
			Allowed values(1)<br/>
			Default = NULL
		</td>
	</tr>
	
	
	<tr>
		<td>
			<b>get_shared </b><br/>
			<i>integer</i>
		</td>	
		<td>
			Return all shared folder related to logged user<br/>
			Allowed value(1)<br/>
			Default = NULL
		</td>
	</tr>
	
	<tr>
		<td>
			<b>order </b><br/>
			<i>string</i>
		</td>	
		<td>
			Return all files and folder according to order in ascending or descending<br/>
			Allowed value(asc OR desc)<br/>
			Default = asc
		</td>
	</tr>
	
	
	<tr>
		<td>
			<b>order_by </b><br/>
			<i>string</i>
		</td>	
		<td>
			Return all files and folder according to ordering<br/>
			Allowed value(updated_time_stamp OR name OR extension OR size)<br/>
			Default = updated_time_stamp
		</td>
	</tr>
	
</table>
	
### Response
```json
{

    "status":"success",
    "count":2,
    "data_usage":"3722228",
    "storage_limit":16777216,
    "results_total_count":"1",
    "results_limit":50,
    "results_offset":0,
    "data":{
        "files":[
            {
                "id":0,
                "creator_id":0,
                "version_id":null,
                "version_count":null,
                "is_folder":"1",
                "parent_id":null,
                "project_id":"1",
                "path":null,
                "description":null,
                "is_share":null,
                "name":"Appnostic",
                "created_time_stamp":"2012-04-04T06:30:00+05:30",
                "updated_time_stamp":null,
                "account_id":"1",
                "is_archived":null,
                "thumb_url":null,
                "file_url":null,
                "md5":null,
                "full_path":"Appnostic",
                "update_microtime":0,
                "size":0,
                "creator_info":null,
                "extension":""
            },
            {
                "id":"3744",
                "creator_id":"20",
                "is_public":null,
                "version_id":"3786",
                "version_count":"1",
                "is_folder":null,
                "parent_id":null,
                "project_id":null,
                "path":"\/3744",
                "description":null,
                "is_share":null,
                "name":"gdiz8-20130705100512.zip",
                "created_time_stamp":"2013-07-08T10:28:05+05:30",
                "updated_time_stamp":"2013-07-16T08:50:00+05:30",
                "account_id":"1",
                "is_archived":null,
                "update_microtime":"47770",
                "is_deleted":null,
                "thumb_url":null,
                "small_thumb_url":null,
                "size":"50344",
                "file_url":"https:\/\/api.secure.striketest.com\/gateway\/1\/373\/?expires=1376649290&signature=a9e56bd681b7cff8e89bdf097e925b9e&file_name=gdiz8-20130705100512.zip&size=50344&user_id=20",
                "extension":"zip",
                "md5":"6bf4b58c298f093d981533f20ac7400b",
                "share_ids":"",
                "shared_count":0,
                "creator_info":{
                    "id":"20",
                    "dst":null,
                    "fname":"Swapnil",
                    "lname":"Bangad",
                    "email":"swapnil1@gdiz.com",
                    "gender":"m",
                    "picture":"https:\/\/s3.amazonaws.com\/strikebase_profile_TEST\/1_20_t1365482377.jpg",
                    "designation":"programmer",
                    "is_archived":null,
                    "timezone":"UP55",
                    "company_id":"1",
                    "is_lite":null,
                    "is_admin":"1",
                    "role":null,
                    "tel_mobile":"+919420859733",
                    "tel_office":"26387661",
                    "tel_fax":"26387661",
                    "tel_home":"26387661",
                    "send_email_is_online":"1",
                    "company_info":{
                        "id":"1",
                        "name":"GDiz Test 1"
                    },
                    "is_connected":1
                },
                "file_source_id":"3744",
                "full_path":"gdiz8-20130705100512.zip"
            }
        ],
        "paths":[
        ]
    }

}
```






## Get files details
Return all the details of files and folder related to user.

### Method
`GET /files/id`

### Example Request
`GET https://api.secure.strikebase.com/files/3744?access_token='access_token'&format='json'`

### Parameters
#### Attributes

<table border="0">
	<tr>
		<td>
			<b>id</b><br/>
			<i>integer</i>
		</td>	
		<td>
			Return details of files and folder related to user<br/>
			required
		</td>
	</tr>
</table>

	
### Response
```json	
{

    "count":1,
    "status":"success",
    "data":{
        "file":{
            "id":"3744",
            "name":"gdiz8-20130705100512.zip",
            "is_share":null,
            "description":"",
            "created_time_stamp":"2013-07-08T10:28:05+05:30",
            "updated_time_stamp":"2013-07-16T08:50:00+05:30",
            "is_folder":null,
            "version_count":"1",
            "path_info":[
                {
                    "id":"3744",
                    "name":"gdiz8-20130705100512.zip"
                }
            ],
            "inherited":null,
            "is_owner":1,
            "file_size":"50344",
            "extension":"zip",
            "file_url":"https:\/\/api.secure.striketest.com\/gateway\/1\/373\/?expires=1376649397&signature=abc065e988c75e90c81eca51c0a5f824&file_name=gdiz8-20130705100512.zip&size=50344&user_id=20",
            "user_info":{
                "id":"20",
                "dst":null,
                "fname":"Swapnil",
                "lname":"Bangad",
                "email":"swapnil1@gdiz.com",
                "gender":"m",
                "picture":"https:\/\/s3.amazonaws.com\/strikebase_profile_TEST\/1_20_t1365482377.jpg",
                "designation":"programmer",
                "is_archived":null,
                "timezone":"UP55",
                "company_id":"1",
                "is_lite":null,
                "is_admin":"1",
                "role":null,
                "tel_mobile":"+919420859733",
                "tel_office":"26387661",
                "tel_fax":"26387661",
                "tel_home":"26387661",
                "send_email_is_online":"1",
                "company_info":{
                    "id":"1",
                    "name":"GDiz Test 1"
                },
                "is_connected":1
            },
            "project_info":[
            ],
            "activity":[
                {
                    "id":"58024",
                    "element_id":"3744",
                    "user_id":"20",
                    "type":"19",
                    "project_id":null,
                    "pulse_id":"98872",
                    "is_update":"1",
                    "content":"{\"id\":3744,\"action\":1914,\"name\":\"gdiz8-20130705100512.zip\"}",
                    "action_id":"1914",
                    "source":"1",
                    "create_date":"2013-07-08T10:28:09+05:30",
                    "processes_count":0,
                    "posted_by":{
                        "id":"20",
                        "fname":"Swapnil",
                        "lname":"Bangad",
                        "name":"Swapnil Bangad",
                        "picture":"https:\/\/s3.amazonaws.com\/strikebase_profile_TEST\/1_20_t1365482377.jpg",
                        "designation":"programmer",
                        "gender":"m"
                    },
                    "details":{
                        "action":1914,
                        "content":{
                            "content":"%s uploaded %s",
                            "params":[
                                [
                                    "Swapnil Bangad",
                                    "b",
                                    6,
                                    "20",
                                    "He",
                                    ""
                                ],
                                [
                                    "gdiz8-20130705100512.zip",
                                    "bu",
                                    19,
                                    "3744",
                                    "this file",
                                    ""
                                ]
                            ],
                            "processes":[
                            ]
                        }
                    },
                    "time_stamp":"2013-07-08T10:28:09+05:30",
                    "action":"1914",
                    "parent_project":null,
                    "is_archived":null,
                    "likes_info":[
                    ],
                    "is_like":0,
                    "likes_count":0
                }
            ],
            "activity_count":1,
            "last_update_id":"98872",
            "comments_count":1,
            "last_comment_id":"58024",
            "shared_info":[
            ]
        }
    }

}
```

## Get files versions
Return all the versions of the particular files related to user.

### Method
`GET /files/id/versions`

### Example Request
`GET https://api.secure.strikebase.com/files/3744/versions?access_token='access_token'&format='json'`

### Parameters
#### Attributes

<table border="0">
	<tr>
		<td>
			<b>id</b><br/>
			<i>integer</i>
		</td>	
		<td>
			Pass only files id whose version required <br/>
			required
		</td>
	</tr>
	
	<tr>
		<td>
			<b>versions</b><br/>
			<i>string</i>
		</td>	
		<td>
			required
		</td>
	</tr>
	
</table>

	
### Response
```json	

{

    "count":1,
    "data":{
        "versions":[
            {
                "big_thumb_url":null,
                "small_thumb_url":null,
                "id":"3744",
                "version_id":"3786",
                "creator_id":"20",
                "is_folder":null,
                "parent_id":null,
                "path":"\/3744",
                "name":"gdiz8-20130705100512.zip",
                "extension":"zip",
                "created_time_stamp":"2013-07-08T10:28:05+05:30",
                "file_size":"50344",
                "updated_time_stamp":"2013-07-08T10:28:05+05:30",
                "md5":"6bf4b58c298f093d981533f20ac7400b",
                "file_url":"https:\/\/api.secure.striketest.com\/gateway\/1\/373\/?expires=1376649526&signature=3aa9314f3f8ded5ffcc57bc87a6dcb60&file_name=gdiz8-20130705100512.zip&size=50344&user_id=20",
                "creator_info":{
                    "id":"20",
                    "dst":null,
                    "fname":"Swapnil",
                    "lname":"Bangad",
                    "email":"swapnil1@gdiz.com",
                    "gender":"m",
                    "picture":"https:\/\/s3.amazonaws.com\/strikebase_profile_TEST\/1_20_t1365482377.jpg",
                    "designation":"programmer",
                    "is_archived":null,
                    "timezone":"UP55",
                    "company_id":"1",
                    "is_lite":null,
                    "is_admin":"1",
                    "role":null,
                    "tel_mobile":"+919420859733",
                    "tel_office":"26387661",
                    "tel_fax":"26387661",
                    "tel_home":"26387661",
                    "send_email_is_online":"1",
                    "company_info":{
                        "id":"1",
                        "name":"GDiz Test 1"
                    },
                    "is_connected":1
                }
            }
        ]
    },
    "status":"success"

}
```



## Get files comments
Return all the comments of the particular files related to user.

### Method
`GET /files/id/comments`

### Example Request
`GET https://api.secure.strikebase.com/files/3744/comments?access_token='access_token'&last_comment_id=77190`

### Parameters
#### Attributes

<table border="0">
	<tr>
		<td>
			<b>id</b><br/>
			<i>integer</i>
		</td>	
		<td>
			Pass only files id whose comments required <br/>
			required
		</td>
	</tr>
	
	<tr>
		<td>
			<b>comments</b><br/>
			<i>string</i>
		</td>	
		<td>
			required
		</td>
	</tr>
	
	<tr>
		<td>
			<b>last_comment_id</b><br/>
			<i>integer</i>
		</td>	
		<td>
			Get all the comments after last comment id <br/>
			required
		</td>
	</tr>
</table>

### Response
```json	
{

    "count":1,
    "status":"success",
    "data":{
        "file":{
            "last_comment_id":"58024",
            "type":19,
            "comments_count":1,
            "comments":
			[
                {
                    "id":"58024",
                    "element_id":"3744",
                    "user_id":"20",
                    "type":"19",
                    "project_id":null,
                    "pulse_id":"98872",
                    "is_update":"1",
                    "content":"{\"id\":3744,\"action\":1914,\"name\":\"gdiz8-20130705100512.zip\"}",
                    "action_id":"1914",
                    "source":"1",
                    "create_date":"2013-07-08T10:28:09+05:30",
                    "processes_count":0,
                    "posted_by":{
                        "id":"20",
                        "fname":"Swapnil",
                        "lname":"Bangad",
                        "name":"Swapnil Bangad",
                        "picture":"https:\/\/s3.amazonaws.com\/strikebase_profile_TEST\/1_20_t1365482377.jpg",
                        "designation":"programmer",
                        "gender":"m"
                    },
                    "details":{
                        "action":1914,
                        "content":{
                            "content":"%s uploaded %s",
                            "params":[
                                [
                                    "Swapnil Bangad",
                                    "b",
                                    6,
                                    "20",
                                    "He",
                                    ""
                                ],
                                [
                                    "gdiz8-20130705100512.zip",
                                    "bu",
                                    19,
                                    "3744",
                                    "this file",
                                    ""
                                ]
                            ],
                            "processes":[
                            ]
                        }
                    },
                    "time_stamp":"2013-07-08T10:28:09+05:30",
                    "action":"1914",
                    "parent_project":null,
                    "is_archived":null,
                    "likes_info":[
                    ],
                    "is_like":0,
                    "likes_count":0
                }
            ],
            "activity_count":1,
            "id":"3744"
        }
    }

}

```
	
	
	

## Get files download link
Return all the download link of the particular files related to user.

### Method
`GET /files/id/download`

### Example Request
`GET : https://api.secure.strikebase.com/files/1052/download?access_token='access_token'&is_download=1`

### Parameters
#### Attributes

<table border="0">
	<tr>
		<td>
			<b>id</b><br/>
			<i>integer</i>
		</td>	
		<td>
			Pass only files id whose download link required <br/>
			required
		</td>
	</tr>
	
	<tr>
		<td>
			<b>download</b><br/>
			<i>string</i>
		</td>	
		<td>
			required
		</td>
	</tr>
	
	<tr>
		<td>
			<b>is_download</b><br/>
			<i>integer</i>
		</td>	
		<td>
			Returns the download link <br/>
			Allowed value(1)<br/>
			Default = NULL
		</td>
	</tr>
</table>	


### Response
```json	
{

    "status":"success",
    "file_url":"https:\/\/api.secure.striketest.com\/gateway\/1\/212\/?expires=1376650756&signature=a6cae5b66e7fe8891d859b4e0714c216&file_name=0014_projects.js&size=148484&user_id=20"

}
```



## Create Folder or upload files
Create Folder or upload files

### Method
`POST /files`

### Example Request
`POST : https://api.secure.strikebase.com/files?access_token='access_token&format='json'`

### Parameters
#### Attributes

<table border="0">
	<tr>
		<td>
			<b>description</b><br/>
			<i>string</i>
		</td>	
		<td>
			To provide the description to folder<br/>
			Applicable only for folder
		</td>
	</tr>
	
	<tr>
		<td>
			<b>parent_id</b><br/>
			<i>integer</i>
		</td>	
		<td>
			Pass folder_id in which file to be uploaded  or folder to be created.<br/>
			Default = NULL
		</td>
	</tr>
	
	<tr>
		<td>
			<b>project_ids</b><br/>
			<i>integer</i>
		</td>	
		<td>
			Pass project_id in which file to be uploaded  or folder to be created.<br/>
			Default = NULL
		</td>
	</tr>
	
	<tr>
		<td>
			<b>is_folder</b><br/>
			<i>integer</i>
		</td>	
		<td>
			To create a new folder<br/>
			Allowed value(1)<br/>
			Default = NULL
		</td>
	</tr>
	
	<tr>
		<td>
			<b>name</b><br/>
			<i>string</i>
		</td>	
		<td>
			Name of the folder<br/>
			required
		</td>
	</tr>
	
	<tr>
		<td>
			<b>previous_version </b><br/>
			<i>integer</i>
		</td>	
		<td>
			while uploading same file with different content , pass previous_version id of the file which will create a new version<br/>
			Default = NULL
		</td>
	</tr>
	
	<tr>
		<td>
			<b>is_private </b><br/>
			<i>integer</i>
		</td>	
		<td>
			To make the folder as private<br/>
			Applicable only while creating Folder<br/>
			Allowed Value(1)<br/>
			Default = NULL
		</td>
	</tr>
	
	<tr>
		<td>
			<b>people_ids </b><br/>
			<i>string</i>
		</td>	
		<td>
			To share the private folder with people <br/>
			Applicable only while creating Folder<br/>
			Exam : people_ids= '1_2_3_4'<br/>
			Default = NULL
		</td>
	</tr>
	
	
	<tr>
		<td>
			<b>people_ids </b><br/>
			<i>string</i>
		</td>	
		<td>
			To share the private folder with people <br/>
			Applicable only while creating Folder<br/>
			Exam : people_ids= '1_2_3_4'<br/>
			Default = NULL
		</td>
	</tr>
	
	
	<tr>
		<td>
			<b>ids </b><br/>
			<i>string</i>
		</td>	
		<td>
			Pass files ids <br/>
			Applicable only while copying or moving files or folder<br/>
			Exam : ids= '1_2_3_4'<br/>
			Default = NULL
		</td>
	</tr>
	
	
	<tr>
		<td>
			<b>copy </b><br/>
			<i>integer</i>
		</td>	
		<td>
			To copy the files  and folder <br/>
			Applicable only while copying or moving files or folder<br/>
			Allowed Value(1)<br/>
			Default = NULL
		</td>
	</tr>
	
	
	<tr>
		<td>
			<b>target_ids </b><br/>
			<i>integer</i>
		</td>	
		<td>
			Pass the folder id in which FIles and folder to be copied or moved  <br/>
			Applicable only while copying or moving files or folder<br/>
			Default = NULL
		</td>
	</tr>
	
</table>

### Response
```json	
{
  "status":"success",
}
```


## Update folder and  files
To update the name and description of the files and folder

### Method
`POST /files/id`

### Example Request
`POST : https://api.secure.strikebase.com/files/3478?access_token='access_token&format='json'`

### Parameters
#### Attributes

<table border="0">

	<tr>
		<td>
			<b>id</b><br/>
			<i>integer</i>
		</td>	
		<td>
			Pass the file or folder id to be updated<br/>
			required
		</td>
	</tr>
	
	<tr>
		<td>
			<b>description</b><br/>
			<i>string</i>
		</td>	
		<td>
			To provide the description to folder<br/>
			Applicable only for folder
		</td>
	</tr>
	
	<tr>
		<td>
			<b>name</b><br/>
			<i>string</i>
		</td>	
		<td>
			Pass name of file or folder.<br/>
			required
		</td>
	</tr>
</table>	

###Response
```json	
{
"status":"success"
}
```



## share the Folder
To share the folder with people

### Method
`POST /files/id/share`

### Example Request
`POST : https://api.secure.strikebase.com/files/3478/share?access_token='access_token&format='json'`

### Parameters
#### Attributes

<table border="0">
	<tr>
		<td>
			<b>id</b><br/>
			<i>integer</i>
		</td>	
		<td>
			pass the folder id to be shared<br/>
			Applicable only for folder
		</td>
	</tr>
	
	<tr>
		<td>
			<b>share</b><br/>
			<i>string</i>
		</td>	
		<td>
			required
		</td>
	</tr>
	
	<tr>
		<td>
			<b>people_ids</b><br/>
			<i>string</i>
		</td>	
		<td>
			pass the people ids to be shared<br/>
			Example : people_ids = '1_2_3_4'<br/>
			Applicable only for folder<br/>
			required
		</td>
	</tr>
</table>

### Response
```json	
{
"status":"success"
}
```




	
## Comment on any Folder or file
To comment on folder or file

### Method
`POST /files/id/comments`

### Example Request
`GET : https://api.secure.strikebase.com/files/3478/comments?access_token='access_token&format='json'`

### Parameters
#### Attributes

<table border="0">
	<tr>
		<td>
			<b>id</b><br/>
			<i>integer</i>
		</td>	
		<td>
			pass the folder id to be shared<br/>
			Applicable only for folder<br/>
			required
		</td>
	</tr>
	
	<tr>
		<td>
			<b>content</b><br/>
			<i>string</i>
		</td>	
		<td>
			pass the content to be posted<br/>
			required
		</td>
	</tr>
</table>



### Response
```json	
{
"status":"success"
}
```	


## Archive OR delete on any Folder or file
To Archive OR delete on any Folder or file

### Method
`DELETE /files`

### Example Request
`DELETE : https://api.secure.strikebase.com/files?access_token='access_token&format='json'`

### Parameters
#### Attributes

<table border="0">
	<tr>
		<td>
			<b>ids</b><br/>
			<i>string</i>
		</td>	
		<td>
			pass the folder id or file ids to be archived or deleted <br/>
			Example : ids = '1_2_3_4'
			required
		</td>
	</tr>
	
	<tr>
		<td>
			<b>undo</b><br/>
			<i>integer</i>
		</td>	
		<td>
			To Unarchive the folder or file<br/>
			Allowed Value(1)<br/>
			required
		</td>
	</tr>
	
	
	<tr>
		<td>
			<b>permanent</b><br/>
			<i>string</i>
		</td>	
		<td>
			To Delete the folder or file permanently<br/>
			Allowed Value(1)<br/>
			Default = NULL <br/>
			
		</td>
	</tr>
</table>	

### Response
```json	
{
"status":"success"
}
```	



## Archive Folder or file
To Archive Folder or file

### Method
`DELETE /files/id`

### Example Request
`DELETE : https://api.secure.strikebase.com/files/3601?access_token='access_token&format='json'`

### Parameters
#### Attributes

<table border="0">
	<tr>
		<td>
			<b>id</b><br/>
			<i>integer</i>
		</td>	
		<td>
			pass the folder id or file ids to be archived <br/>
			required
		</td>
	</tr>
</table>	

### Response
```json	
{
"status":"success"
}
```



### To remove people from share folder
To remove people from share folder

### Method
`DELETE /files/id/share`

### Example Request
`DELETE : https://api.secure.strikebase.com/files/3601/share?access_token='access_token&format='json'`

### Parameters
#### Attributes

<table border="0">
	<tr>
		<td>
			<b>id</b><br/>
			<i>integer</i>
		</td>	
		<td>
			pass the folder id from which people to be removed from share <br/>
			required
		</td>
	</tr>
	
	<tr>
		<td>
			<b>share</b><br/>
			<i>string</i>
		</td>	
		<td>
			required
		</td>
	</tr>
	
	<tr>
		<td>
			<b>people_ids</b><br/>
			<i>string</i>
		</td>	
		<td>
			pass the people id to be removed from share <br/>
			required
		</td>
	</tr>
	
</table>	

### Response
```json	
{
"status":"success"
}
```



## To delete the version of the file
`DELETE /files/id/version`

### Example Request
`DELETE : https://api.secure.strikebase.com/files/3605/version?access_token='access_token&format='json'`

### Parameters
#### Attributes

<table border="0">
	<tr>
		<td>
			<b>id</b><br/>
			<i>integer</i>
		</td>	
		<td>
			pass the file id from which people to be removed from share <br/>
			required
		</td>
	</tr>
	
	<tr>
		<td>
			<b>version_id</b><br/>
			<i>integer</i>
		</td>	
		<td>
			pass the version id to be removed from file <br/>
			required
		</td>
	</tr>
	
</table>	

### Response
```json	
{
"status":"success"
}
```


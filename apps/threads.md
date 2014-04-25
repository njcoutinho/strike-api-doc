# Threads (formerly known as messages)
> Description goes here

## Get threads
Return all the threads related to user.

### Method
`GET /threads`

### Example Request
`GET https://api.secure.strikebase.com/threads?access_token='access_token'&format='json'`

### Parameters
#### Attributes

<table border="0">
	<tr>
		<td>
			<b>project_ids</b><br/>
			<i>integer</i>
		</td>	
		<td>
			Return all threads related to project<br/>
			Default = NULL
		</td>
	</tr>
	
	<tr>
		<td>
			<b>is_archived</b><br/>
			<i>integer</i>
		</td>	
		<td>
			Return all archived threads <br/>
			Allowed values (1)<br/> 
			Default = NULL
		</td>
	</tr>
	
	<tr>
		<td>
			<b>thread_type</b><br/>
			<i>integer</i>
		</td>	
		<td>
			Return all archived lists of the project<br/>
			Allowed values (1 OR 2)<br/> 
			1 = one on one threads. <br/>
			2 = Group threads <br/>
			Default = NULL
		</td>
	</tr>
</table>

### Response
```json
{
  'count' => 1,
  'status' => 'success',
  'data' => 
  array {
    'threads' => 
    array {
      0 => 
      array {
        'thread_id' => '7414',
        'thread_creator' => '20',
        'last_message' => 
        array {
          'content' => '<p>You\'re welcome</p><p>test</p>',
          'questions' => 
          array {
          },
          'todos' => 
          array {
          },
          'tasks' => 
          array {
          },
          'posted_by' => 
          array {
            'id' => '9',
          },
        },
        'is_cc' => 0,
        'is_read' => 1,
        'is_public' => 0,
        'is_archived' => NULL,
        'project_id' => NULL,
        'project_name' => NULL,
        'update_time' => '2013-08-05T10:45:06+05:30',
        'cc' => 
        array {
        },
        'user_id' => '22_15_10_41_59_40_45_2201_9_69_7_6_20_2672_2791_2790_2752_39_37',
        'people' => 
        array {
          0 => 
          array {
            'id' => '9',
            'dst' => '1',
            'fname' => 'Aalok',
            'lname' => 'Banjare',
            'email' => 'alok@gdiz.com',
            'gender' => 'm',
            'picture' => 'https://d2zc3me2o4gzwx.cloudfront.net/default_19.jpg',
            'designation' => 'Software Developer',
            'is_archived' => NULL,
            'timezone' => 'UP55',
            'company_id' => '1',
            'is_lite' => NULL,
            'is_admin' => '1',
            'role' => NULL,
            'tel_mobile' => '+919503448820',
            'tel_office' => '909090999090',
            'tel_fax' => '909090999090',
            'tel_home' => '909090999090',
            'send_email_is_online' => '1',
            'company_info' => 
            array {
              'id' => '1',
              'name' => 'GDiz Test 1',
            },
            'is_connected' => 1,
            'is_left' => 0,
          },
          
        },
        'subject' => ' Aalok, Alok, Alok2, Ankit, Jill, Karen, New user, newtest, Pankaj, Phunsuk, Ranjit, Ranjit 1, Savata, Sherman, surya, Suryakant, test &amp; Zack',
      },
    },
  },
}

```

	
	
## Get particular threads
Return particular threads details related to user.

### Method
`GET /threads`

### Example Request
`GET https://api.secure.strikebase.com/threads/7414?access_token='access_token'&format='json'`

### Parameters
#### Attributes

<table border="0">
	<tr>
		<td>
			<b>id</b><br/>
			<i>integer</i>
		</td>	
		<td>
			Return particular threads details<br/>
			Default = NULL
		</td>
	</tr>
</table>

### Response
```json
{
  'count' => 1,
  'status' => 'success',
  'data' => 
  array {
    'thread_id' => '7414',
    'user_id' => '9_37_40_15_59_6_2752_2791_39_2672_45_2201_41_10_69_22_20_2790_7',
    'thread_creator' => '20',
    'is_public' => 0,
    'update_time' => '2013-08-05T10:45:06+05:30',
    'is_all_deleted' => 0,
    'has_left' => 0,
    'is_blocked' => 0,
    'is_project_blocked' => 0,
    'is_archived' => 0,
    'last_message_id' => '11526',
    'subject' => ' Aalok, Alok, Alok2, Ankit, Jill, Karen, New user, newtest, Pankaj, Phunsuk, Ranjit, Ranjit 1, Savata, Sherman, surya, Suryakant, test &amp; Zack',
    'tags' => 
    array {
    },
    'result_offset' => 0,
    'people' => 
    array {
      0 => 
      array {
        'id' => '9',
        'dst' => '1',
        'fname' => 'Aalok',
        'lname' => 'Banjare',
        'email' => 'alok@gdiz.com',
        'gender' => 'm',
        'picture' => 'https://d2zc3me2o4gzwx.cloudfront.net/default_19.jpg',
        'designation' => 'Software Developer',
        'is_archived' => 0,
        'timezone' => 'UP55',
        'company_id' => '1',
        'is_lite' => NULL,
        'is_admin' => '1',
        'role' => NULL,
        'tel_mobile' => '+919503448820',
        'tel_office' => '909090999090',
        'tel_fax' => '909090999090',
        'tel_home' => '909090999090',
        'send_email_is_online' => '1',
        'company_info' => 
        array {
          'id' => '1',
          'name' => 'GDiz Test 1',
        },
        'is_connected' => 1,
        'is_left' => 0,
      },
           
    },
    'cc' => 
    array {
    },
    'messages' => 
    array {
      0 => 
      array {
        'source' => '2',
        'message_id' => '11526',
        'create_date' => '2013-08-05T10:45:06+05:30',
        'posted_by' => 
        array {
          'id' => '9',
          'dst' => '1',
          'fname' => 'Aalok',
          'lname' => 'Banjare',
          'email' => 'alok@gdiz.com',
          'gender' => 'm',
          'picture' => 'https://d2zc3me2o4gzwx.cloudfront.net/default_19.jpg',
          'designation' => 'Software Developer',
          'is_archived' => NULL,
          'timezone' => 'UP55',
          'company_id' => '1',
          'is_lite' => NULL,
          'is_admin' => '1',
          'role' => NULL,
          'tel_mobile' => '+919503448820',
          'tel_office' => '909090999090',
          'tel_fax' => '909090999090',
          'tel_home' => '909090999090',
          'send_email_is_online' => '1',
          'company_info' => 
          array {
            'id' => '1',
            'name' => 'GDiz Test 1',
          },
          'is_connected' => 1,
        },
        'tags' => 
        array {
        },
        'project_id' => NULL,
        'project_name' => NULL,
        'content' => '<p>You\'re welcome</p><p>test</p>',
        'questions' => 
        array {
        },
        'todos' => 
        array {
        },
        'tasks' => 
        array {
        },
        'approvals' => 
        array {
        },
        'is_read' => '1',
        'app_id' => NULL,
        'app_name' => NULL,
        'attachments' => 
        array {
        },
      },
    },
  },
}

```	





## Create threads
To create a new thread.

### Method
`POST /threads`

### Example Request
`POST https://api.secure.strikebase.com/threads?access_token='access_token'&format='json'`

### Parameters
#### Attributes

<table border="0">
	<tr>
		<td>
			<b>to</b><br/>
			<i>string</i>
		</td>	
		<td>
			To create a thread between users<br/>
			Applicable only for private threads<br/>
			Format : to = '1_2_3'
			Default = NULL
		</td>
	</tr>
	
	<tr>
		<td>
			<b>message</b><br/>
			<i>string</i>
		</td>	
		<td>
			To send the message content to users<br/>
			Default = NULL
		</td>
	</tr>
	
	<tr>
		<td>
			<b>project_ids</b><br/>
			<i>integer</i>
		</td>	
		<td>
			To create a thread for particular project<br/>
			Default = NULL
		</td>
	</tr>
	
	<tr>
		<td>
			<b>send_email</b><br/>
			<i>integer</i>
		</td>	
		<td>
			To get email of the message <br/>
			Allowed values (1)<br/>
			Default = NULL
		</td>
	</tr>
	
	
	<tr>
		<td>
			<b>subject</b><br/>
			<i>string</i>
		</td>	
		<td>
			To create a subject for the thread<br/>
			Applicable only for public threads and group thread<br/>
			Default = NULL
		</td>
	</tr>
	
	<tr>
		<td>
			<b>is_private</b><br/>
			<i>integer</i>
		</td>	
		<td>
			To make the thread as public or private <br/>
			Allowed values (1)<br/>
			1 = private <br/>
			Default = NULL
		</td>
	</tr>
</table>

### Response
```json
{
"thread _id":633,
"status":"success"
}

```




## Send Message
To send message to particular thread.

### Method
`POST /threads/id`

### Example Request
`POST https://api.secure.strikebase.com/threads/633?access_token='access_token'&format='json'`

### Parameters
#### Attributes

<table border="0">
	
	<tr>
		<td>
			<b>message</b><br/>
			<i>string</i>
		</td>	
		<td>
			To send the message content<br/>
			required
		</td>
	</tr>
	
	<tr>
		<td>
			<b>project_ids</b><br/>
			<i>integer</i>
		</td>	
		<td>
			Message related to particular project<br/>
			Default = NULL
		</td>
	</tr>
	
	<tr>
		<td>
			<b>send_email</b><br/>
			<i>integer</i>
		</td>	
		<td>
			To get email of the message <br/>
			Allowed values (1)<br/>
			Default = NULL
		</td>
	</tr>
	
	
	<tr>
		<td>
			<b>subject</b><br/>
			<i>string</i>
		</td>	
		<td>
			To create a subject for the thread<br/>
			Applicable only for public threads and group thread<br/>
			Default = NULL
		</td>
	</tr>
	
	
</table>

### Response
```json
{
"thread _id":633,
"status":"success"
}

```



## Archive thread
To archive the particular thread.

### Method
`POST /threads/id/archive`

### Example Request
`POST https://api.secure.strikebase.com/threads/633/archive?access_token='access_token'&format='json'`

### Parameters
#### Attributes

<table border="0">
	
	<tr>
		<td>
			<b>id</b><br/>
			<i>integer</i>
		</td>	
		<td>
			Pass the thread id to be archived<br/>
			required
		</td>
	</tr>
	
	<tr>
		<td>
			<b>archive</b><br/>
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
	"status":"success"
}

```	




## Unarchive thread
To unarchive the archive thread.

### Method
`POST /threads/id/unarchive`

### Example Request
`POST https://api.secure.strikebase.com/threads/633/unarchive?access_token='access_token'&format='json'`

### Parameters
#### Attributes

<table border="0">
	
	<tr>
		<td>
			<b>id</b><br/>
			<i>integer</i>
		</td>	
		<td>
			Pass the thread id to be archived<br/>
			required
		</td>
	</tr>
	
	<tr>
		<td>
			<b>unarchive</b><br/>
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
	"status":"success"
}

```	





## Leave thread
To Leave the thread.

### Method
`POST /threads/id/leave`

### Example Request
`POST https://api.secure.strikebase.com/threads/633/leave?access_token='access_token'&format='json'`

### Parameters
#### Attributes

<table border="0">
	
	<tr>
		<td>
			<b>id</b><br/>
			<i>integer</i>
		</td>	
		<td>
			Pass the thread id to be archived<br/>
			required
		</td>
	</tr>
	
	<tr>
		<td>
			<b>leave</b><br/>
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
	"status":"success"
}

```	




## Add people to thread
To Add people to particular thread(Applicable only on group threads).

### Method
`POST /threads/id/add`

### Example Request
`POST https://api.secure.strikebase.com/threads/633/add?access_token='access_token'&format='json'`

### Parameters
#### Attributes

<table border="0">
	<tr>
		<td>
			<b>id</b><br/>
			<i>integer</i>
		</td>	
		<td>
			Pass the thread id to be archived<br/>
			required
		</td>
	</tr>
	
	<tr>
		<td>
			<b>add</b><br/>
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
			Pass people ids to be added to thread. <br/>
			Format : people_ids = '1_2_3_4'<br/>
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



## Remove people from thread
To Remove people from particular thread(Applicable only for private group thread).

### Method
`POST /threads/id/remove`

### Example Request
`POST https://api.secure.strikebase.com/threads/633/remove?access_token='access_token'&format='json'`

### Parameters
#### Attributes

<table border="0">
	<tr>
		<td>
			<b>id</b><br/>
			<i>integer</i>
		</td>	
		<td>
			Pass the thread id from which user to be removed<br/>
			required
		</td>
	</tr>
	
	<tr>
		<td>
			<b>remove</b><br/>
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
			Pass people ids to be removed to thread. <br/>
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



## Delete Messages
To Delete messages from particular thread.

### Method
`DELETE /threads/id/messages`

### Example Request
`DELETE https://api.secure.strikebase.com/threads/633/messages?access_token='access_token'&format='json'`

### Parameters
#### Attributes

<table border="0">
	<tr>
		<td>
			<b>id</b><br/>
			<i>integer</i>
		</td>	
		<td>
			Pass the thread id from which message to be removed<br/>
			required
		</td>
	</tr>
	
	<tr>
		<td>
			<b>messages</b><br/>
			<i>string</i>
		</td>	
		<td>
			required
		</td>
	</tr>
	
	<tr>
		<td>
			<b>message_ids</b><br/>
			<i>string</i>
		</td>	
		<td>
			Pass message ids to be deleted from thread for logged user only. 
			Format : message_ids = '1_2_3_4'
			Default = NULL (Delete all messages from the thread for logged user)
		</td>
	</tr>
	
</table>	

### Response
```json
{
	"status":"success"
}

```	


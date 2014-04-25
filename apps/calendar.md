# Calendar
> Description goes here

## Get calendar
Returns all the calendar and calendar events related to you in your account.

### Method
`GET /calendar`

### Example Request
`GET https://api.secure.strikebase.com/calendars?access_token='access_token'&from=2013-06-01&to=2013-07-30&calendar_ids=1_3&project_ids=1_2_4&include_general=1&my_cards=1&team_cards=1&archived_cards=1`

### Parameters
#### Attributes

<table border="0">
	<tr>
		<td>
			<b>is_calendar</b><br/>
			<i>integer</i>
		</td>
		
		<td>
			Allowed values (1)<br/> 
			Default = NULL
		</td>
	</tr>
	<tr>
		<td>
			<b>from</b><br/>
			<i>date</i>
		</td>
		<td>
			Return all calendar events from the given date<br/>
			Allowed values (date)<br/>
			Default = current date
		</td>
	</tr>	
	
	<tr>
		<td>
			<b>to</b><br/>
			<i>date</i>
		</td>
		<td>
			Return all calendar events till the given date<br/>
			Allowed values (date)<br/>
			Default = 7th date from the current date
		</td>
	</tr>

	<tr>
		<td>
			<b>project_ids</b><br/>
			<i>integer</i>
		</td>
		<td>
			Return all calendar events for the given project<br/>
			Default = NULL
		</td>
	</tr>

	<tr>
		<td>
			<b>calendar_ids</b><br/>
			<i>string</i>
		</td>
		<td>
			Return all calendar events for the given calendar <br/>
			pass multiple calendar_ids with underscore seperated. Example : calendar_ids = 1_2_3_4
			Default = NULL
		</td>
	</tr>

	<tr>
		<td>
			<b>include_general</b><br/>
			<i>integer</i>
		</td>
		<td>
			Return all the calendar event related to user whose calendar does not exist in the account<br/>
			Allowed values (1)<br/> 
			Default = NULL
		</td>
	</tr>
	
	
	<tr>
		<td>
			<b>include_project</b><br/>
			<i>integer</i>
		</td>
		<td>
			Return all the project whose start date or end date lies between passed calendar event from date and to date in the account<br/>
			Allowed values (1)<br/> 
			Default = NULL
		</td>
	</tr>
	
	<tr>
		<td>
			<b>my_cards</b><br/>
			<i>integer</i>
		</td>
		<td>
			Return all the tasks whose deadline ranges between passed calendar from date and to date related to user in the account<br/>
			Allowed values (1)<br/> 
			Default = NULL
		</td>
	</tr>
	
	<tr>
		<td>
			<b>team_cards</b><br/>
			<i>integer</i>
		</td>
		<td>
			Return all the tasks whose deadline ranges between passed calendar from date and to date related to account excluding users cards in the account<br/>
			Allowed values (1)<br/> 
			Default = NULL
		</td>
	</tr>
	
	<tr>
		<td>
			<b>archived_cards</b><br/>
			<i>integer</i>
		</td>
		<td>
			Return all the archived tasks in the account<br/>
			Allowed values (1)<br/> 
			Only applicable for my_cards and team_cards<br/>
			Default = NULL
		</td>
	</tr>

</table>


		 

### Response
```json
{
	"status":"success",
	"count":1,
	"data":
	{
		"events":
		[
			{
				"type":20,
				"calendar_info":[
				],
				"start":"2013-08-16T00:00:00+05:30",
				"end":"2013-08-16T00:00:00+05:30",
				"source_id":"5452",
				"id":"5452_1376611200",
				"name":"Test 213",
				"user_id":"20",
				"creator_info":
				{
					"id":"15",
					"dst":"1",
					"fname":"Ankit",
					"lname":"Choubey",
					"email":"ankit@gdiz.com",
					"gender":"m",
					"picture":"https:\/\/d2zc3me2o4gzwx.cloudfront.net\/default_18.jpg",
					"designation":"Tester",
					"is_archived":null,
					"timezone":"UP55",
					"company_id":"1",
					"is_lite":null,
					"is_admin":"1",
					"role":null,
					"tel_mobile":"+3589420859733",
					"tel_office":"9420859733",
					"tel_fax":"9420859733",
					"tel_home":"9420859733",
					"send_email_is_online":"1",
					"company_info":
						{
							"id":"1",
							"name":"GDiz Test 1"
						},
					"is_connected":1
				},
				"description":null,
				"is_series":0,
				"time_stamp":"2013-08-16 00:00:00",
				"duration":"0",
				"is_all_day":true,
				"details":
				{
					"place":null,
					"privacy":null,
					"is_infinite":null,
					"reminders":null,
					"guest_info":
					[
						{
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
							"company_info":
							{
							"id":"1",
							"name":"GDiz Test 1"
							},
							"is_connected":1,
							"response":null
						}
						
					],
					"project_info":[
					],
					"attachments":[
					],
					"show_me_as":null,
					"guest_permissions":"2",
					"key":10
				}
			}
		]
	}
}
```


## Create calendar
Add a new calendar and calendar event to your account

### Method
`POST /calendar`

### Example Request
`POST  : https://api.secure.strikebase.com/calendar?access_token='access_token'&format=json`

### Parameters
#### Attributes

<table border="0">
	<tr>
		<td>
			<b>is_calendar</b><br/>
			<i>integer</i>
		</td>
		<td>
			To create a new calendar<br/>
			Allowed values (1)<br/> 
			Default = NULL
		</td>
	</tr>
	
	
	<tr>
		<td>
			<b>calendar_name </b><br/>
			<i>string</i>
		</td>
		<td>
			To give name to calendar<br/>
			Only applicable for is_calendar<br/>
			Required if is_calendar is passed
		</td>
	</tr>
	
	<tr>
		<td>
			<b>color</b><br/>
			<i>integer</i>
		</td>
		<td>
			color will be added <br/>
			Allowed values (1 to 11)<br/> 
			Default = 1
		</td>
	</tr>
	
	<tr>
		<td>
			<b>from</b><br/>
			<i>date and time</i>
		</td>
		<td>
			Calendar events to be created for given date<br/>
			Allowed values (date and time)<br/>
			Required if is_calendar is not passed
		</td>
	</tr>
	
	<tr>
		<td>
			<b>to</b><br/>
			<i>date and time</i>
		</td>
		<td>
			Calendar events to date<br/>
			Allowed values (date and time)<br/>
			Required if is_calendar is not passed
		</td>
	</tr>
	
	<tr>
		<td>
			<b>title </b><br/>
			<i>string</i>
		</td>
		<td>
			Title of calendar event<br/>
			Required if is_calendar is not passed
		</td>
	</tr>
	
	
	<tr>
		<td>
			<b>description </b><br/>
			<i>string</i>
		</td>
		<td>
			Description of calendar event<br/>
		</td>
	</tr>
	
	<tr>
		<td>
			<b>place </b><br/>
			<i>string</i>
		</td>
		<td>
			Place of the event<br/>
		</td>
	</tr>
	
	
	<tr>
		<td>
			<b>privacy </b><br/>
			<i>integer</i>
		</td>
		<td>
			To make the event private or public <br/>
			Allowed values (1)<br/> 
			Default = NULL (public)
		</td>
	</tr>
	
		
	<tr>
		<td>
			<b>project_ids</b><br/>
			<i>integer</i>
		</td>
		<td>
			Project id to which the event will be added to<br/>
		</td>
	</tr>
	
	<tr>
		<td>
			<b>guest </b><br/>
			<i>string</i>
		</td>
		<td>
			To add the guest to the Event <br/>
			only applicable for private event<br/>
			Default = NULL 
		</td>
	</tr>
	
	
	
	<tr>
		<td>
			<b>guest_permissions </b><br/>
			<i>integer</i>
		</td>
		<td>
			To add the permission for guest <br/>
			Allowed values (1,2)<br/> 
			1 : Guest can modify event <br/>
			2 : Guest can only invite others <br/>
			Default = 1 <br/>
			only applicable for private event and guest is passed
		</td>
	</tr>
	
	
	<tr>
		<td>
			<b>is_all_day </b><br/>
			<i>integer</i>
		</td>
		<td>
			To make the event as all day event <br/>
			Allowed values (1)<br/> 
			Default = NULL <br/>
		</td>
	</tr>
	
	
	<tr>
		<td>
			<b>reminder_type </b><br/>
			<i>integer</i>
		</td>
		<td>
			To make the event as all day event <br/>
			Allowed values (1 to 4)<br/> 
			Default = NULL <br/>
			Required if reminder_value is passed
		</td>
	</tr>
	
	
	<tr>
		<td>
			<b>reminder_value </b><br/>
			<i>integer</i>
		</td>
		<td>
			To pass reminder value to the event <br/>
			Default = NULL <br/>
			Required if reminder_type is passed
		</td>
	</tr>
	
	
	
	<tr>
		<td>
			<b>repeats </b><br/>
			<i>string</i>
		</td>
		<td>
			To make the event repetitive <br/>
			Default = NULL <br/>
			Format :  [{"repeat":"1 to 4", "repeats_every":"1", "repeats_on":"1 to 7", "end":"" }] <br/>
			<h5> 1)  repeat : 1 = Daily , 2 = Weekly , 3 = Monthly , 4 = Yearly<br/>
			2)  repeats_every : Integer less than 30 <br/>
			3)  repeats_on : 1= Monday , 2= Tuesday ....... 7 = Sunday <br/>
			4)  End :  0 = Events created daily , Integer = Number of Events created , date = (Date-Format : Year-month-day) . Event will be created till the date passed </h5>
			
			
		</td>
	</tr>
	
</table>


		 

### Response
```json
	{ 
		"status":"success",
		"ids":5182
	}
```






## Update calendar
Update calendar and calendar event to your account

### Method
`POST /calendar/id`

### Example Request
`POST  : https://api.secure.strikebase.com/calendar/6?access_token='access_token'&format=json`

### Parameters
#### Attributes

<table border="0">
	<tr>
		<td>
			<b>is_calendar</b><br/>
			<i>integer</i>
		</td>
		<td>
			To update calendar<br/>
			Allowed values (1)<br/> 
			Default = NULL
		</td>
	</tr>
	
	
	<tr>
		<td>
			<b>calendar_name </b><br/>
			<i>string</i>
		</td>
		<td>
			Calendar name<br/>
			Only applicable for is_calendar<br/>
			Required if is_calendar is passed
		</td>
	</tr>
	
	<tr>
		<td>
			<b>color</b><br/>
			<i>integer</i>
		</td>
		<td>
			color will be added <br/>
			Allowed values (1 to 11)<br/> 
			Default = 1<br/>
			Applicable only when is_calendar is passed
		</td>
	</tr>
	
	<tr>
		<td>
			<b>from</b><br/>
			<i>date and time</i>
		</td>
		<td>
			Calendar events to be updated for given date<br/>
			Allowed values (date and time)<br/>
			Required if is_calendar is not passed 
		</td>
	</tr>
	
	<tr>
		<td>
			<b>to</b><br/>
			<i>date and time</i>
		</td>
		<td>
			Calendar events to date<br/>
			Allowed values (date and time)<br/>
			Required if is_calendar is not passed 
		</td>
	</tr>
	
	<tr>
		<td>
			<b>title </b><br/>
			<i>string</i>
		</td>
		<td>
			Title of calendar event<br/>
			Required if is_calendar is not passed
		</td>
	</tr>
	
	
	<tr>
		<td>
			<b>description </b><br/>
			<i>string</i>
		</td>
		<td>
			Description of calendar event<br/>
		</td>
	</tr>
	
	<tr>
		<td>
			<b>place </b><br/>
			<i>string</i>
		</td>
		<td>
			Place of the event<br/>
		</td>
	</tr>
	
	
	<tr>
		<td>
			<b>privacy </b><br/>
			<i>integer</i>
		</td>
		<td>
			To make the event private or public <br/>
			Applicable only for creator and Admin <br/>
			Allowed values (1)<br/> 
			Default = NULL (public)
			
		</td>
	</tr>
	
		
	<tr>
		<td>
			<b>project_ids</b><br/>
			<i>integer</i>
		</td>
		<td>
			Project id to which the event will be updated to
		</td>
	</tr>
	
		
	
	<tr>
		<td>
			<b>guest_permissions </b><br/>
			<i>integer</i>
		</td>
		<td>
			To update the permission for guest <br/>
			Allowed values (1 , 2)<br/> 
			1 : Guest can modify event <br/>
			2 : Guest can only invite others <br/>
			Default = 1 <br/>
			only applicable for private event and guest exist on the event
		</td>
	</tr>
	
	
	<tr>
		<td>
			<b>is_all_day </b><br/>
			<i>integer</i>
		</td>
		<td>
			To make the event as all day event <br/>
			Allowed values (1)<br/> 
			Default = NULL <br/>
		</td>
	</tr>
	
	
	<tr>
		<td>
			<b>reminder_type </b><br/>
			<i>integer</i>
		</td>
		<td>
			To make the event as all day event <br/>
			Allowed values (1 to 4)<br/> 
			Default = NULL <br/>
			Required if reminder_value is passed
		</td>
	</tr>
	
	
	<tr>
		<td>
			<b>reminder_value </b><br/>
			<i>integer</i>
		</td>
		<td>
			To pass reminder value to the event <br/>
			Default = NULL <br/>
			Required if reminder_type is passed
		</td>
	</tr>
	
	
	
	<tr>
		<td>
			<b>repeats </b><br/>
			<i>string</i>
		</td>
		<td>
			To make the event repetitive <br/>
			Default = NULL <br/>
			Format :  [{"repeat":"1 to 4", "repeats_every":"1", "repeats_on":"1 to 7", "end":"" }] <br/>
			<h5> 1)  repeat : 1 = Daily , 2 = Weekly , 3 = Monthly , 4 = Yearly<br/>
			2)  repeats_every : Integer less than 30 <br/>
			3)  repeats_on : 1= Monday , 2= Tuesday ....... 7 = Sunday <br/>
			4)  End :  0 = Events created daily , Integer = Number of Events created , date = (Date-Format : Year-month-day) . Event will be created till the date passed </h5>
			
		</td>
	</tr>
	
	
	<tr>
		<td>
			<b>type </b><br/>
			<i>integer</i>
		</td>
		<td>
			To update repetitive event<br/>
			Allowed values (1 OR 2 OR 3)<br/> 
			1. Only this Event.
			2. All Following.
			3. All the Event.
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








## Update calendar event response
Update particular calendar event response to your account

### Method
`POST /calendar/id/response`

### Example Request
`POST : https://api.secure.strikebase.com/calendar/1/response?access_token='access_token'&format=json`

### Parameters
#### Attributes

<table border="0">
	<tr>
		<td>
			<b>status</b><br/>
			<i>integer</i>
		</td>
		<td>
			To update the response to calendar event<br/>
			required<br/>
			Allowed values (1,2,3)<br/> 
			1. Yes <br/>
			2. May Be <br/>
			3 . No <br/>
			
		</td>
	</tr>
	
	
	<tr>
		<td>
			<b>type</b><br/>
			<i>integer</i>
		</td>
		<td>
			To pass type of calendar event<br/>
			required only for repetitive event<br/>
			Allowed values (1,2)<br/> 
			1. Only this Event
			2. All the Event in series
			Default = NULL
		</td>
	</tr>
	
	
	<tr>
		<td>
			<b>date</b><br/>
			<i>date</i>
		</td>
		<td>
			To pass the date of event<br/>
			required only for repetitive event and type = 1 <br/>
			Allowed values (date)<br/> 
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




## Update calendar event guest
To add guest to particular event

### Method
`POST /calendar/id/add_people`

### Example Request
`POST : https://api.secure.strikebase.com/calendar/1/add_people?access_token='access_token'&format=json`

### Parameters
#### Attributes

<table border="0">
	<tr>
		<td>
			<b>guest</b><br/>
			<i>string</i>
		</td>
		<td>
			To pass the user id to be added as guest in calendar event<br/>
			Example : guest = 1_2_3_4 <br/>
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



## Update calendar event
To move event from one date to another date

### Method
`POST /calendar/id/date`

### Example Request
`POST : https://api.secure.strikebase.com/calendar/1/date?access_token='access_token'&format=json`

### Parameters
#### Attributes

<table border="0">
	<tr>
		<td>
			<b>updated_from</b><br/>
			<i>date and time</i>
		</td>
		<td>
			To pass start date and time to be update from date<br/>
			required
		</td>
	</tr>
	
	
	<tr>
		<td>
			<b>updated_to</b><br/>
			<i>date and time</i>
		</td>
		<td>
			To pass start date and time to be update till date<br/>
			required
		</td>
	</tr>
	
	
	<tr>
		<td>
			<b>original_from</b><br/>
			<i>date and time</i>
		</td>
		<td>
			To pass original date and time of from date of event<br/>
			required
		</td>
	</tr>
	
	
	
	<tr>
		<td>
			<b>original_to</b><br/>
			<i>date and time</i>
		</td>
		<td>
			To pass original date and time of end date of event<br/>
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






## Delete calendar
Delete calendar and calendar event 

### Method
`DELETE /calendar/id/`

### Example Request
`DELETE: https://api.secure.strikebase.com/calendar/1?access_token='access_token'&format=json`

### Parameters
#### Attributes

<table border="0">
	<tr>
		<td>
			<b>from</b><br/>
			<i>date and time</i>
		</td>
		<td>
			To delete the event for particular date <br/>
			Only for repetitive events and type = 1 <br/>
		</td>
	</tr>
	
	<tr>
		<td>
			<b>type</b><br/>
			<i>integer</i>
		</td>
		<td>
			To pass the type accordingly (1,2,3)<br/>
			Only applicable for repetitive event and compulsary<br/>
			1. Only this event <br/>
			2. All the following Event <br/>
			3. All the Event in series <br/>
			default = NULL<br/>
		</td>
	</tr>
	
	<tr>
		<td>
			<b>is_calendar</b><br/>
			<i>integer</i>
		</td>
		<td>
			Deletes the calendar from the account<br/>
		</td>
	</tr>
	
	
</table>

### Response
```json
{
"status":"success"
}
```




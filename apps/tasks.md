# Tasks (formerly known as Cards)
> Description goes here

## Get lists
Return all the lists in a project board.

### Method
`GET /lists`

### Example Request
``

### Parameters
#### Attributes
<table border="0">
	<tr>
		<td>
			<b>project_ids</b><br/>
			<i>integer</i>
		</td>
		<td>
			Project id the lists belong to<br/>
		</td>
	</tr>
	<tr>
		<td>
			<b>show_archived</b><br/>
			<i>integer</i>
		</td>
		<td>
			Return all archived lists of the project<br/>
			Allowed values (1)<br/>
			Default = NULL
		</td>
	</tr>	
</table>

### Response
```json

```

## Create list
Create a List for a projecy board

### Method
`GET /lists`

### Example Request
``

### Parameters
#### Attributes
<table border="0">
	<tr>
		<td>
			<b>project_ids</b><br/>
			<i>integer</i>
		</td>
		<td>
			Project id the lists belong to<br/>
		</td>
	</tr>
	<tr>
		<td>
			<b>list_ids</b><br/>
			<i>string</i>
		</td>
		<td>
			Tasks from this list can only be moved to the following lists<br/>
			Format: Underscore separated ids i.e. 1_2_3<br/>
			Default = 0
		</td>
	</tr>
	<tr>
		<td>
			<b>min_cards</b><br/>
			<i>integer</i>
		</td>
		<td>
			Minimum number to tasks allowed in the list<br/>
			
		</td>
	</tr>
	<tr>
		<td>
			<b>max_cards</b><br/>
			<i>integer</i>
		</td>
		<td>
			Maximum number to tasks allowed in the list<br/>
			
		</td>
	</tr>
	<tr>
		<td>
			<b>is_complete</b><br/>
			<i>integer</i>
		</td>
		<td>
			Mark the status of all tasks in this list as complete<br/>
			Allowed values (1,0)<br/>
			Default value (0)
		</td>
	</tr>
<tr>
		<td>
			<b>is_progress</b><br/>
			<i>integer</i>
		</td>
		<td>
			Mark the status of all tasks in this list as in progress<br/>
			Allowed values (1,0)<br/>
			Default value (0)
		</td>
	</tr>	
</table>

### Response
```json

```

## Move tasks to another list
Move tasks from one lists to another list

### Method
`POST /lists/id/move`

### Example Request
``

### Parameters
#### Attributes
<table border="0">
	<tr>
		<td>
			<b>target_project_ids</b><br/>
			<i>integer</i>
		</td>
		<td>
			Destination list's project id<br/>
			<i>required</i>
		</td>
	</tr>
	<tr>
		<td>
			<b>project_ids</b><br/>
			<i>integer</i>
		</td>
		<td>
			Source list's project id<br/>
			<i>required</i>
		</td>
	</tr>
	<tr>
		<td>
			<b>to_list</b><br/>
			<i>integer</i>
		</td>
		<td>
			Destinations list's id<br/>
		</td>
	</tr>	
	<tr>
		<td>
			<b>to_list</b><br/>
			<i>integer</i>
		</td>
		<td>
			Destinations list's id<br/>
		</td>
	</tr>	
</table>

### Response
```json

```

## Copy lists
Create a copy of a list

### Method
`POST /lists/id/copy`

### Example Request
``

### Parameters
#### Attributes
<table border="0">
	<tr>
		<td>
			<b>target_project_ids</b><br/>
			<i>integer</i>
		</td>
		<td>
			Destination list's project id<br/>
			<i>required</i>
		</td>
	</tr>
	<tr>
		<td>
			<b>project_ids</b><br/>
			<i>integer</i>
		</td>
		<td>
			Source list's project id<br/>
			<i>required</i>
		</td>
	</tr>
	<tr>
		<td>
			<b>id</b><br/>
			<i>integer</i>
		</td>
		<td>
			Source list's id<br/>
		</td>
	</tr>	
	<tr>
		<td>
			<b>name</b><br/>
			<i>string</i>
		</td>
		<td>
			New list's name<br/>
		</td>
	</tr>	
</table>

### Response
```json

```



## Copy list tasks
Copy tasks from one list to another

### Method
`POST /lists/id/copy_cards`

### Example Request
``

### Parameters
#### Attributes
<table border="0">
	<tr>
		<td>
			<b>target_project_ids</b><br/>
			<i>integer</i>
		</td>
		<td>
			Destination list's project id<br/>
			<i>required</i>
		</td>
	</tr>
	<tr>
		<td>
			<b>project_ids</b><br/>
			<i>integer</i>
		</td>
		<td>
			Source list's project id<br/>
			<i>required</i>
		</td>
	</tr>
	<tr>
		<td>
			<b>to_list</b><br/>
			<i>integer</i>
		</td>
		<td>
			Destinations list's id<br/>
		</td>
	</tr>	
	<tr>
		<td>
			<b>to_list</b><br/>
			<i>integer</i>
		</td>
		<td>
			Destinations list's id<br/>
		</td>
	</tr>	
</table>

### Response
```json

```

## Empty list
Empty the list i.e. (remove all tasks from the list)

### Method
`POST /lists/id/empty_list`

### Example Request
``

### Parameters
#### Attributes
<table border="0">
	<tr>
		<td>
			<b>id</b><br/>
			<i>integer</i>
		</td>
		<td>
			List ID<br/>
			<i>required</i>
		</td>
	</tr>
	<tr>
		<td>
			<b>project_ids</b><br/>
			<i>integer</i>
		</td>
		<td>
			Source list's project id<br/>
			<i>required</i>
		</td>
	</tr>
	
</table>

### Response
```json

```

## Archive/Delete list
Archive or permanently delete a list

### Method
`DELETE /lists/id/`

### Example Request
``

### Parameters
#### Attributes
<table border="0">
	<tr>
		<td>
			<b>id</b><br/>
			<i>integer</i>
		</td>
		<td>
			List ID<br/>
			<i>required</i>
		</td>
	</tr>
	<tr>
		<td>
			<b>project_ids</b><br/>
			<i>integer</i>
		</td>
		<td>
			Source list's project id<br/>
			<i>required</i>
		</td>
	</tr>
	<tr>
		<td>
			<b>is_deleted</b><br/>
			<i>integer</i>
		</td>
		<td>
			Permanently delete lis<br/>
			allowed values (1)<br/>
			
		</td>
	</tr>
	
</table>

### Response
```json

```



## Unarchive list
Unarchive a list

### Method
`POST /lists/id/unarchive_list`

### Example Request
``

### Parameters
#### Attributes
<table border="0">
	<tr>
		<td>
			<b>id</b><br/>
			<i>integer</i>
		</td>
		<td>
			List ID<br/>
			<i>required</i>
		</td>
	</tr>
	<tr>
		<td>
			<b>project_ids</b><br/>
			<i>integer</i>
		</td>
		<td>
			Source list's project id<br/>
			<i>required</i>
		</td>
	</tr>
	
</table>

### Response
```json

```

---

## Get Tasks(Cards)
Get Tasks for a particular list

### Method
`GET /cards`

### Example Request
``

### Parameters
#### Attributes
<table border="0">
	<tr>
		<td>
			<b>list_id</b><br/>
			<i>integer</i>
		</td>
		<td>
			Souce list ID<br/>
			<i>required</i>
		</td>
	</tr>
	<tr>
		<td>
			<b>project_ids</b><br/>
			<i>integer</i>
		</td>
		<td>
			Task project id<br/>
			Default = NULL
			
		</td>
	</tr>
	<tr>
		<td>
			<b>project_ids</b><br/>
			<i>integer</i>
		</td>
		<td>
			Task project id<br/>
			
		</td>
	</tr>
	<tr>
		<td>
			<b>is_archived</b><br/>
			<i>integer</i>
		</td>
		<td>
			Return all archived tasks<br/>
			Default = 1
			
		</td>
	</tr>
	
	<tr>
		<td>
			<b>is_watched</b><br/>
			<i>integer</i>
		</td>
		<td>
			Return all watched tasks<br/>
			Default = 1
			
		</td>
	</tr>
	
	<tr>
		<td>
			<b>creator_id</b><br/>
			<i>integer</i>
		</td>
		<td>
			Return all tasks created by a specific user<br/>
			
			
		</td>
	</tr>
	
	<tr>
		<td>
			<b>limit</b><br/>
			<i>integer</i>
		</td>
		<td>
			Number of results to be returned<br/>
			Default = 50 max = 100
			
		</td>
	</tr>
	
</table>

### Response
```json

```

## Get Task(Card)
Get a particular Task

### Method
`GET /cards/id`

### Example Request
``

### Parameters
#### Attributes
<table border="0">
	<tr>
		<td>
			<b>id</b><br/>
			<i>integer</i>
		</td>
		<td>
			Task ID<br/>
			<i>required</i>
		</td>
	</tr>
</table>

### Response
```json

```

## Create Task(Card)
Create a Task

### Method
`POST /cards`

### Example Request
``

### Parameters
#### Attributes
<table border="0">
	<tr>
		<td>
			<b>name</b><br/>
			<i>string</i>
		</td>
		<td>
		
			Task name<br/>
			<i>required</i>
		</td>
	</tr>
	<tr>
		<td>
			<b>description</b><br/>
			<i>string</i>
		</td>
		<td>
			Task description<br/>
			
		</td>
	</tr>
	<tr>
		<td>
			<b>project_ids</b><br/>
			<i>integer</i>
		</td>
		<td>
			Project ID to which the task belongs to<br/>
			<i>required</i>
			
		</td>
	</tr>
	<tr>
		<td>
			<b>people_ids</b><br/>
			<i>string</i>
		</td>
		<td>
			Project ID to which the task belongs to<br/>
			<i>required</i>
			
		</td>
	</tr>
</table>

### Response
```json

```

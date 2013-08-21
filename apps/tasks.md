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

## Move tasks to another lists
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
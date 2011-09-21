VMG Chosen Member
========
Fieldtype for Expression Engine 2
--------

**VMG Chosen Member** is a fieldtype allowing the selection of one or more members. It includes autocomplete capabilities and the friendly selection/listing of large numbers of users using the Chosen (http://harvesthq.github.com/chosen/) JavaScript plugin.


Installation
-------
*	Upload ee2/third_party/vmg_chosen_member to system/expressionengine/third_party
*	Upload themes/third_party/vmg_chosen_member to themes/third_party
*	Install the fieldtype by going to Add-Ons &rarr; Fieldtypes
*	Ensure that both the Fieldtype and Module are installed


Single Variable Tag
-------
	{custom_field}
> Outputs the pipe (|) delimited list of member IDs.

Variable Tag Pair
-------
	{custom_field}
		<h2>{screen_name}</h2>
		<p>Email: {email}</p>
		<p>Some custom member field: {some_custom_member_field}</p>
	{/custom_field}
> Outputs member data for the selected members and provides access to all data tags.

> ### Parameters
*	**disable** = "member_data"
>> Setting *disable* to *member_data* will skip loading custom member fields.
*	**prefix** = "my_"
>> By providing a prefix, all data tags will be parsed prepended with the string of your choosing. This can be helpful for avoiding naming collisions.
*	**group_id** = "1|2|3"
>> While you can limit selections to specific member groups in the field's settings, this parameter allows you to further limit results on output.
*	**orderby** = "email"
>> The *orderby* parameter sets the display order of the output.
*	**sort** = "asc"
>> The *sort* order will be applied if you specify an *orderby* parameter.
*	**limit** = "1"
>> The *limit* parameter will set the number of results that will be returned.


:total_members Tag
-------
	{custom_member_field:total_members}
> Outputs the total number of members selected within the field.

Support within other fieldtypes
--------
VMG Chosen Member can be used within Matrix (http://pixelandtonic.com/matrix/) and Low Variables (http://gotolow.com/addons/low-variables/).

Warranty/License
--------
There's no warranty of any kind. If you find a bug, please tell report it or submit a pull request with a fix. It's provided completely as-is; if something breaks, you lose data, or something else bad happens, the author(s) and owner(s) of this plugin are in no way responsible.
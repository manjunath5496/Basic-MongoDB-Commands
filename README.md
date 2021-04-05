# Basic MongoDB Commands

<table width="667">
<tbody>
<tr>
<td width="349">
<p>db.help()</p>
</td>
<td colspan="2" width="318">
<p>&nbsp;get a list of commands</p>
</td>
</tr>
<tr>
<td width="349">
<p>show dbs</p>
</td>
<td colspan="2" width="318">
<p>&nbsp;print a list of all databases on the server</p>
</td>
</tr>
<tr>
<td width="349">
<p>use myTestDB</p>
</td>
<td colspan="2" width="318">
<p>create new database "<strong>myTestDB</strong>"</p>
</td>
</tr>
<tr>
<td width="349">
<p>db</p>
</td>
<td colspan="2" width="318">
<p>know your current selected database</p>
</td>
</tr>
<tr>
<td width="349">db.dropDatabase()
<p>&nbsp;</p>
</td>
<td colspan="2" width="318">
<p>drop the current selected database</p>
</td>
</tr>
<tr>
<td width="349">
<p>db.createCollection("Employee")</p>
</td>
<td colspan="2" width="318">
<p>create new collection "<strong>Employee</strong>"</p>
</td>
</tr>
<tr>
<td width="349">
<p>show collections</p>
</td>
<td colspan="2" width="318">
<p>print a list of all collections created</p>
</td>
</tr>
<tr>
<td width="349">
<p>db.Employee.drop()</p>
</td>
<td colspan="2" width="318">
<p>drop the collection "<strong>Employee</strong>"</p>
</td>
</tr>
<tr>
<td width="349">
<p>db.Employee.insert({name: 'Raj', address: 'Bangalore'})</p>
</td>
<td colspan="2" width="318">
<p>insert document in collection "<strong>Employee</strong>"</p>
</td>
</tr>
<tr>
<td width="349">
<p>db.Employee.find()</p>
<p>&nbsp;</p>
</td>
<td colspan="2" width="318">
<p>list the documents in collection "<strong>Employee</strong>"</p>
</td>
</tr>
<tr>
<td colspan="3" width="667">
<p>&nbsp;</p>
<p>{ "_id" : ObjectId("60658a0dbe02cfa1d386ab52"), "name" : "Raj", "address" : "Bangalore" }</p>
<p>&nbsp;</p>
</td>
</tr>
<tr>
<td width="349">
<p>db.Employee.update({'name' : 'Raj'}, {$set: {'name' : 'Albert'}})</p>
</td>
<td colspan="2" width="318">
<p>update the document in collection "<strong>Employee</strong>"</p>
<p>&nbsp;</p>
</td>
</tr>
<tr>
<td width="349">
<p>db.Employee.find()</p>
<p>&nbsp;</p>
</td>
<td colspan="2" width="318">
<p>list the documents in collection "<strong>Employee</strong>"</p>
</td>
</tr>
<tr>
<td colspan="3" width="667">
<p>&nbsp;</p>
<p>&nbsp;</p>
<p>{ "_id" : ObjectId("60658a0dbe02cfa1d386ab52"), "name" : "Albert", "address" : "Bangalore" }</p>
<p>&nbsp;</p>
</td>
</tr>
<tr>
<td width="349">
<p>&nbsp;</p>
<p>db.Employee.save({"_id": new ObjectId("60658a0dbe02cfa1d386ab53"), name: "Newton", address: "Delhi"});</p>
<p>&nbsp;</p>
</td>
<td colspan="2" width="318">
<p>save document in collection "<strong>Employee</strong>"</p>
<p>&nbsp;</p>
</td>
</tr>
<tr>
<td width="349">
<p>db.Employee.find()</p>
<p>&nbsp;</p>
</td>
<td colspan="2" width="318">
<p>list the documents in collection "<strong>Employee</strong>"</p>
</td>
</tr>
<tr>
<td colspan="3" width="667">
<p>&nbsp;</p>
<p>{ "_id" : ObjectId("60658a0dbe02cfa1d386ab52"), "name" : "Albert", "address" : "Bangalore" }</p>
<p>{ "_id" : ObjectId("60658a0dbe02cfa1d386ab53"), "name" : "Newton", "address" : "Delhi" }</p>
<p>&nbsp;</p>
<p>&nbsp;</p>
</td>
</tr>
<tr>
<td width="349">
<p>db.Employee.remove({'name': 'Albert'})</p>
<p>&nbsp;</p>
</td>
<td colspan="2" width="318">
<p>delete document in collection "<strong>Employee</strong>"</p>
</td>
</tr>
<tr>
<td width="349">
<p>db.Employee.find()</p>
<p>&nbsp;</p>
</td>
<td colspan="2" width="318">
<p>list the documents in collection "<strong>Employee</strong>"</p>
<p>&nbsp;</p>
</td>
</tr>
<tr>
<td colspan="3" width="667">
<p>{ "_id" : ObjectId("60658a0dbe02cfa1d386ab53"), "name" : "Newton", "address" : "Delhi" }</p>
<p>&nbsp;</p>
<p>&nbsp;</p>
</td>
</tr>
<tr>
<td colspan="2" width="355">
<p>db.getUsers();</p>
<p>&nbsp;</p>
<p>&nbsp;</p>
</td>
<td width="312">
<p>list down all the users of current database</p>
<p>&nbsp;</p>
</td>
</tr>
<tr>
<td colspan="2" width="355">
<p>show roles</p>
<p>&nbsp;</p>
</td>
<td width="312">
<p>list down all the roles</p>
</td>
</tr>
<tr>
<td colspan="2" width="355">
<p>db.Employee.dataSize()</p>
</td>
<td width="312">
<p>get the size of the collection "<strong>Employee</strong>"</p>
</td>
</tr>
<tr>
<td colspan="2" width="355">
<p>db.Employee.storageSize()</p>
</td>
<td width="312">
<p>get the total size of document stored in the collection "<strong>Employee</strong>"</p>
</td>
</tr>
<tr>
<td colspan="2" width="355">
<p>db.Employee.totalSize()</p>
</td>
<td width="312">
<p>&nbsp;get the total size in bytes for both collection data and indexes</p>
<p>&nbsp;</p>
</td>
</tr>
<tr>
<td colspan="2" width="355">
<p>db.Employee.totalIndexSize()</p>
</td>
<td width="312">
<p>get the total size of all indexes in the collection "<strong>Employee</strong>"</p>
<p>&nbsp;</p>
</td>
</tr>
</tbody>
</table>

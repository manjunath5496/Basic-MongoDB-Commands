# Basic MongoDB Commands

<table style="width: 816px;">
<tbody>
<tr>
<td style="width: 461px;">
<p>db.help()</p>
</td>
<td style="width: 456px;" colspan="2">
<p>&nbsp;get a list of commands</p>
</td>
</tr>
<tr>
<td style="width: 461px;">
<p>show dbs</p>
</td>
<td style="width: 456px;" colspan="2">
<p>&nbsp;print a list of all databases on the server</p>
</td>
</tr>
<tr>
<td style="width: 461px;">
<p>use myTestDB</p>
</td>
<td style="width: 456px;" colspan="2">
<p>create new database "<strong>myTestDB</strong>"</p>
</td>
</tr>
<tr>
<td style="width: 461px;">
<p>db</p>
</td>
<td style="width: 456px;" colspan="2">
<p>know your current selected database</p>
</td>
</tr>
<tr>
<td style="width: 461px;">db.dropDatabase()
<p>&nbsp;</p>
</td>
<td style="width: 456px;" colspan="2">
<p>drop the current selected database</p>
</td>
</tr>
<tr>
<td style="width: 461px;">
<p>db.createCollection("Employee")</p>
</td>
<td style="width: 456px;" colspan="2">
<p>create new collection "<strong>Employee</strong>"</p>
</td>
</tr>
<tr>
<td style="width: 461px;">
<p>show collections</p>
</td>
<td style="width: 456px;" colspan="2">
<p>print a list of all collections created</p>
</td>
</tr>
<tr>
<td style="width: 461px;">
<p>db.Employee.drop()</p>
</td>
<td style="width: 456px;" colspan="2">
<p>drop the collection "<strong>Employee</strong>"</p>
</td>
</tr>
<tr>
<td style="width: 461px;">
<p>db.Employee.insert({name: 'Raj', address: 'Bangalore'})</p>
</td>
<td style="width: 456px;" colspan="2">
<p>insert document in collection "<strong>Employee</strong>"</p>
</td>
</tr>
<tr>
<td style="width: 461px;">
<p>db.Employee.find()</p>
<p>&nbsp;</p>
</td>
<td style="width: 456px;" colspan="2">
<p>list the documents in collection "<strong>Employee</strong>"</p>
</td>
</tr>
<tr>
<td style="width: 917px;" colspan="3">
<p>&nbsp;</p>
<p>{ "_id" : ObjectId("60658a0dbe02cfa1d386ab52"), "name" : "Raj", "address" : "Bangalore" }</p>
<p>&nbsp;</p>
</td>
</tr>
<tr>
<td style="width: 461px;">
<p>db.Employee.update({'name' : 'Raj'}, {$set: {'name' : 'Albert'}})</p>
</td>
<td style="width: 456px;" colspan="2">
<p>update the document in collection "<strong>Employee</strong>"</p>
<p>&nbsp;</p>
</td>
</tr>
<tr>
<td style="width: 461px;">
<p>db.Employee.find()</p>
<p>&nbsp;</p>
</td>
<td style="width: 456px;" colspan="2">
<p>list the documents in collection "<strong>Employee</strong>"</p>
</td>
</tr>
<tr>
<td style="width: 917px;" colspan="3">
<p>&nbsp;</p>
<p>&nbsp;</p>
<p>{ "_id" : ObjectId("60658a0dbe02cfa1d386ab52"), "name" : "Albert", "address" : "Bangalore" }</p>
<p>&nbsp;</p>
</td>
</tr>
<tr>
<td style="width: 461px;">
<p>&nbsp;</p>
<p>db.Employee.save({"_id": new ObjectId("60658a0dbe02cfa1d386ab53"), name: "Newton", address: "Delhi"});</p>
<p>&nbsp;</p>
</td>
<td style="width: 456px;" colspan="2">
<p>save document in collection "<strong>Employee</strong>"</p>
<p>&nbsp;</p>
</td>
</tr>
<tr>
<td style="width: 461px;">
<p>db.Employee.find()</p>
<p>&nbsp;</p>
</td>
<td style="width: 456px;" colspan="2">
<p>list the documents in collection "<strong>Employee</strong>"</p>
</td>
</tr>
<tr>
<td style="width: 917px;" colspan="3">
<p>&nbsp;</p>
<p>{ "_id" : ObjectId("60658a0dbe02cfa1d386ab52"), "name" : "Albert", "address" : "Bangalore" }</p>
<p>{ "_id" : ObjectId("60658a0dbe02cfa1d386ab53"), "name" : "Newton", "address" : "Delhi" }</p>
<p>&nbsp;</p>
<p>&nbsp;</p>
</td>
</tr>
<tr>
<td style="width: 461px;">
<p>db.Employee.remove({'name': 'Albert'})</p>
<p>&nbsp;</p>
</td>
<td style="width: 456px;" colspan="2">
<p>delete document in collection "<strong>Employee</strong>"</p>
</td>
</tr>
<tr>
<td style="width: 461px;">
<p>db.Employee.find()</p>
<p>&nbsp;</p>
</td>
<td style="width: 456px;" colspan="2">
<p>list the documents in collection "<strong>Employee</strong>"</p>
<p>&nbsp;</p>
</td>
</tr>
<tr>
<td style="width: 917px;" colspan="3">
<p>{ "_id" : ObjectId("60658a0dbe02cfa1d386ab53"), "name" : "Newton", "address" : "Delhi" }</p>
<p>&nbsp;</p>
<p>&nbsp;</p>
</td>
</tr>
<tr>
<td style="width: 464px;" colspan="2">
<p>db.getUsers();</p>
<p>&nbsp;</p>
<p>&nbsp;</p>
</td>
<td style="width: 453px;">
<p>list down all the users of current database</p>
<p>&nbsp;</p>
</td>
</tr>
<tr>
<td style="width: 464px;" colspan="2">
<p>show roles</p>
<p>&nbsp;</p>
</td>
<td style="width: 453px;">
<p>list down all the roles</p>
</td>
</tr>
<tr>
<td style="width: 464px;" colspan="2">
<p>db.Employee.dataSize()</p>
</td>
<td style="width: 453px;">
<p>get the size of the collection "<strong>Employee</strong>"</p>
</td>
</tr>
<tr>
<td style="width: 464px;" colspan="2">
<p>db.Employee.storageSize()</p>
</td>
<td style="width: 453px;">
<p>get the total size of document stored in the collection "<strong>Employee</strong>"</p>
</td>
</tr>
<tr>
<td style="width: 464px;" colspan="2">
<p>db.Employee.totalSize()</p>
</td>
<td style="width: 453px;">
<p>&nbsp;get the total size in bytes for both collection data and indexes</p>
<p>&nbsp;</p>
</td>
</tr>
<tr>
<td style="width: 464px;" colspan="2">
<p>db.Employee.totalIndexSize()</p>
</td>
<td style="width: 453px;">
<p>get the total size of all indexes in the collection "<strong>Employee</strong>"</p>
<p>&nbsp;</p>
</td>
</tr>
</tbody>
</table>

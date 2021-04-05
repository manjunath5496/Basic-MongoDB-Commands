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
</br>
<h2> Papers </h2>

<ul>

                             

 <li><a target="_blank" href="https://github.com/manjunath5496/Basic-MongoDB-Commands/blob/master/m(1).pdf" style="text-decoration:none;">Modeling and Querying Data in MongoDB</a></li>

 <li><a target="_blank" href="https://github.com/manjunath5496/Basic-MongoDB-Commands/blob/master/m(2).pdf" style="text-decoration:none;">MongoDB Operations Best Practices</a></li>

<li><a target="_blank" href="https://github.com/manjunath5496/Basic-MongoDB-Commands/blob/master/m(3).pdf" style="text-decoration:none;">Automatic Mapping of MySQL Databases to NoSQL MongoDB</a></li>
 <li><a target="_blank" href="https://github.com/manjunath5496/Basic-MongoDB-Commands/blob/master/m(4).pdf" style="text-decoration:none;">Using MongoDB for Social Networking Website</a></li>                              
<li><a target="_blank" href="https://github.com/manjunath5496/Basic-MongoDB-Commands/blob/master/m(5).pdf" style="text-decoration:none;">performance evaluation of MySQL and MongoDB</a></li>
<li><a target="_blank" href="https://github.com/manjunath5496/Basic-MongoDB-Commands/blob/master/m(6).pdf" style="text-decoration:none;">CRUD Operations in MongoDB</a></li>
 <li><a target="_blank" href="https://github.com/manjunath5496/Basic-MongoDB-Commands/blob/master/m(7).pdf" style="text-decoration:none;">A Mapping-based Method to Query MongoDB Documents with SPARQL</a></li>

 <li><a target="_blank" href="https://github.com/manjunath5496/Basic-MongoDB-Commands/blob/master/m(8).pdf" style="text-decoration:none;"> A Comparative Study: MongoDB vs. MySQL </a></li>
   <li><a target="_blank" href="https://github.com/manjunath5496/Basic-MongoDB-Commands/blob/master/m(9).pdf" style="text-decoration:none;"A Comparative Study: MongoDB vs
MySQL</a></li>
  
   
 <li><a target="_blank" href="https://github.com/manjunath5496/Basic-MongoDB-Commands/blob/master/m(10).pdf" style="text-decoration:none;">Insights from Student Solutions to MongoDB Homework Problems</a></li>                              
<li><a target="_blank" href="https://github.com/manjunath5496/Basic-MongoDB-Commands/blob/master/m(11).pdf" style="text-decoration:none;">Security Analysis of MongoDB and its Comparison with Relational Databases</a></li>
<li><a target="_blank" href="https://github.com/manjunath5496/Basic-MongoDB-Commands/blob/master/m(12).pdf" style="text-decoration:none;">Assessing the vulnerabilities and securing MongoDB and Cassandra databases</a></li>
<li><a target="_blank" href="https://github.com/manjunath5496/Basic-MongoDB-Commands/blob/master/m(13).pdf" style="text-decoration:none;">MongoDB on AWS: 
Guidelines and Best Practices</a></li>

<li><a target="_blank" href="https://github.com/manjunath5496/Basic-MongoDB-Commands/blob/master/m(14).pdf" style="text-decoration:none;">Expressivity and Complexity of MongoDB Queries</a></li>
                              
<li><a target="_blank" href="https://github.com/manjunath5496/Basic-MongoDB-Commands/blob/master/m(15).pdf" style="text-decoration:none;">A Formal Presentation of MongoDB (Extended Version)</a></li>

<li><a target="_blank" href="https://github.com/manjunath5496/Basic-MongoDB-Commands/blob/master/m(16).pdf" style="text-decoration:none;">Comparative Analysis of MongoDB Deployments in Diverse Application Areas</a></li>

  <li><a target="_blank" href="https://github.com/manjunath5496/Basic-MongoDB-Commands/blob/master/m(17).pdf" style="text-decoration:none;">Analysis on Database Security Model Against NOSQL Injection</a></li>   
  
<li><a target="_blank" href="https://github.com/manjunath5496/Basic-MongoDB-Commands/blob/master/m(18).pdf" style="text-decoration:none;">A review of comparison between NoSQL Databases: MongoDB and CouchDB</a></li> 

  
<li><a target="_blank" href="https://github.com/manjunath5496/Basic-MongoDB-Commands/blob/master/m(19).pdf" style="text-decoration:none;">A Study on Join Operations in MongoDB Preserving Collections Data Models for Future Internet Applications</a></li> 

<li><a target="_blank" href="https://github.com/manjunath5496/Basic-MongoDB-Commands/blob/master/m(20).pdf" style="text-decoration:none;">Getting Started with Amazon DocumentDB (with MongoDB Compatibility)</a></li>

<li><a target="_blank" href="https://github.com/manjunath5496/Basic-MongoDB-Commands/blob/master/m(21).pdf" style="text-decoration:none;">Dell EMC PowerStore: MongoDB Solution
Guide</a></li>
<li><a target="_blank" href="https://github.com/manjunath5496/Basic-MongoDB-Commands/blob/master/m(22).pdf" style="text-decoration:none;">MongoDB with Privacy Access Control</a></li> 
 <li><a target="_blank" href="https://github.com/manjunath5496/Basic-MongoDB-Commands/blob/master/m(23).pdf" style="text-decoration:none;">A comprehensive comparison of SQL and MongoDB databases</a></li> 
 

   <li><a target="_blank" href="https://github.com/manjunath5496/Basic-MongoDB-Commands/blob/master/m(24).pdf" style="text-decoration:none;">An Analysis Of Query Performance: Mongodb N Sql</a></li>
 
   <li><a target="_blank" href="https://github.com/manjunath5496/Basic-MongoDB-Commands/blob/master/m(25).pdf" style="text-decoration:none;">MongoDB and NoSQL Databases</a></li>                              
 <li><a target="_blank" href="https://github.com/manjunath5496/Basic-MongoDB-Commands/blob/master/m(26).pdf" style="text-decoration:none;">Learning MongoDB</a></li>
 <li><a target="_blank" href="https://github.com/manjunath5496/Basic-MongoDB-Commands/blob/master/m(27).pdf" style="text-decoration:none;">MongoDB Tutorial for Beginners</a></li>
   
 
   <li><a target="_blank" href="https://github.com/manjunath5496/Basic-MongoDB-Commands/blob/master/m(28).pdf" style="text-decoration:none;">The Little MongoDB Book</a></li>
 
   <li><a target="_blank" href="https://github.com/manjunath5496/Basic-MongoDB-Commands/blob/master/m(29).pdf" style="text-decoration:none;">MongoDB Architecture Guide</a></li>                              

  <li><a target="_blank" href="https://github.com/manjunath5496/Basic-MongoDB-Commands/blob/master/m(30).pdf" style="text-decoration:none;">NoSQL Databases: MongoDB vs Cassandra</a></li>
 
   <li><a target="_blank" href="https://github.com/manjunath5496/Basic-MongoDB-Commands/blob/master/m(31).pdf" style="text-decoration:none;">MongoDB – a comparison with NoSQL databases</a></li> 
    <li><a target="_blank" href="https://github.com/manjunath5496/Basic-MongoDB-Commands/blob/master/m(32).pdf" style="text-decoration:none;">MongoDB - Cheat Sheet</a></li> 

   <li><a target="_blank" href="https://github.com/manjunath5496/Basic-MongoDB-Commands/blob/master/m(33).pdf" style="text-decoration:none;">Analysis
of NoSQL Databases: Mongodb, HBase, Neo4J</a></li>                              

  <li><a target="_blank" href="https://github.com/manjunath5496/Basic-MongoDB-Commands/blob/master/m(34).pdf" style="text-decoration:none;">Mongodb Databases In Big Data
Applications In Transportation Industry</a></li> 
 
  <li><a target="_blank" href="https://github.com/manjunath5496/Basic-MongoDB-Commands/blob/master/m(35).pdf" style="text-decoration:none;">Optimized Infrastructure for Big Data Analytics on MongoDB</a></li> 

  <li><a target="_blank" href="https://github.com/manjunath5496/Basic-MongoDB-Commands/blob/master/m(36).pdf" style="text-decoration:none;">Tunable Consistency in MongoDB</a></li> 
 
<li><a target="_blank" href="https://github.com/manjunath5496/Basic-MongoDB-Commands/blob/master/m(37).pdf" style="text-decoration:none;">An Analysis and Overview of MongoDB Security</a></li>
 <li><a target="_blank" href="https://github.com/manjunath5496/Basic-MongoDB-Commands/blob/master/m(38).pdf" style="text-decoration:none;">MapReduce Performance in MongoDB Sharded Collections</a></li>
<li><a target="_blank" href="https://github.com/manjunath5496/Basic-MongoDB-Commands/blob/master/m(39).pdf" style="text-decoration:none;">Formalizing MongoDB Queries</a></li>
 <li><a target="_blank" href="https://github.com/manjunath5496/Basic-MongoDB-Commands/blob/master/m(40).pdf" style="text-decoration:none;">M2Onto: an Approach and a Tool to Learn OWL Ontology from MongoDB Database</a></li>                              
<li><a target="_blank" href="https://github.com/manjunath5496/Basic-MongoDB-Commands/blob/master/m(41).pdf" style="text-decoration:none;">Performance Benchmark
Postgresql / Mongodb</a></li>
<li><a target="_blank" href="https://github.com/manjunath5496/Basic-MongoDB-Commands/blob/master/m(42).pdf" style="text-decoration:none;">Security Analysis of MongoDB</a></li>
 
  <li><a target="_blank" href="https://github.com/manjunath5496/Basic-MongoDB-Commands/blob/master/m(43).pdf" style="text-decoration:none;">The Application of
NoSQL MongoDB in Developing the EPR System for Managing Human Resources</a></li>
 <li><a target="_blank" href="https://github.com/manjunath5496/Basic-MongoDB-Commands/blob/master/m(44).pdf" style="text-decoration:none;">Proposed Architecture of MongoDB-Hive Integration</a></li>
   <li><a target="_blank" href="https://github.com/manjunath5496/Basic-MongoDB-Commands/blob/master/m(45).pdf" style="text-decoration:none;">An Application of MongoDB to Enterprise System Manipulating Enormous Data</a></li>  
   
<li><a target="_blank" href="https://github.com/manjunath5496/Basic-MongoDB-Commands/blob/master/m(46).pdf" style="text-decoration:none;">A Novel Approach of Using MongoDB for Big Data Analytics</a></li> 
                             
<li><a target="_blank" href="https://github.com/manjunath5496/Basic-MongoDB-Commands/blob/master/m(47).pdf" style="text-decoration:none;">From Relational Model to Rich Document Data Models - Best Practices Using MongoDB</a></li>
</ul>









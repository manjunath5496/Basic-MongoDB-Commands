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

                             

 <li><a target="_blank" href="https://github.com/manjunath5496/Basic-MongoDB-Commands/blob/master/m(1).pdf" style="text-decoration:none;">CoqIOA: A Formalization of IO Automata in the
Coq Proof Assistant</a></li>

 <li><a target="_blank" href="https://github.com/manjunath5496/Basic-MongoDB-Commands/blob/master/m(2).pdf" style="text-decoration:none;">An Offline Foundation for
Online Accountable Pseudonyms</a></li>

<li><a target="_blank" href="https://github.com/manjunath5496/Basic-MongoDB-Commands/blob/master/m(3).pdf" style="text-decoration:none;">A Programming Language
Based on Classical Logic</a></li>
 <li><a target="_blank" href="https://github.com/manjunath5496/Basic-MongoDB-Commands/blob/master/m(4).pdf" style="text-decoration:none;">The Scalable Commutativity Rule:
Designing Scalable Software for Multicore Processors</a></li>                              
<li><a target="_blank" href="https://github.com/manjunath5496/Basic-MongoDB-Commands/blob/master/m(5).pdf" style="text-decoration:none;">Mobile Computing with the Rover Toolkit</a></li>
<li><a target="_blank" href="https://github.com/manjunath5496/Basic-MongoDB-Commands/blob/master/m(6).pdf" style="text-decoration:none;">Improving Network Connection Locality on Multicore Systems</a></li>
 <li><a target="_blank" href="https://github.com/manjunath5496/Basic-MongoDB-Commands/blob/master/m(7).pdf" style="text-decoration:none;">Asynchronous intrusion recovery
for interconnected web services</a></li>

 <li><a target="_blank" href="https://github.com/manjunath5496/Basic-MongoDB-Commands/blob/master/m(8).pdf" style="text-decoration:none;"> Performance Optimization of the VDFS Verified
File System </a></li>
   <li><a target="_blank" href="https://github.com/manjunath5496/Basic-MongoDB-Commands/blob/master/m(9).pdf" style="text-decoration:none;">Algorand: Scaling Byzantine Agreements
for Cryptocurrencies</a></li>
  
   
 <li><a target="_blank" href="https://github.com/manjunath5496/Basic-MongoDB-Commands/blob/master/m(10).pdf" style="text-decoration:none;">Alpaca: Extensible Authorization for Distributed Services </a></li>                              
<li><a target="_blank" href="https://github.com/manjunath5496/Basic-MongoDB-Commands/blob/master/m(11).pdf" style="text-decoration:none;">A Concurrency-Optimal Binary Search Tree</a></li>
<li><a target="_blank" href="https://github.com/manjunath5496/Basic-MongoDB-Commands/blob/master/m(12).pdf" style="text-decoration:none;">Alpenhorn: Bootstrapping Secure Communication without Leaking Metadata</a></li>
<li><a target="_blank" href="https://github.com/manjunath5496/Basic-MongoDB-Commands/blob/master/m(13).pdf" style="text-decoration:none;">Amber: Decoupling User Data from Web Applications</a></li>

<li><a target="_blank" href="https://github.com/manjunath5496/Basic-MongoDB-Commands/blob/master/m(14).pdf" style="text-decoration:none;">Quboid: A Workstation for Safer Web Interaction</a></li>
                              
<li><a target="_blank" href="https://github.com/manjunath5496/Basic-MongoDB-Commands/blob/master/m(15).pdf" style="text-decoration:none;">Argosy: Verifying Layered Storage Systems with
Recovery Refinement</a></li>

<li><a target="_blank" href="https://github.com/manjunath5496/Basic-MongoDB-Commands/blob/master/m(16).pdf" style="text-decoration:none;">LRC: Dependency-Aware Cache Management
for Data Analytics Clusters</a></li>

  <li><a target="_blank" href="https://github.com/manjunath5496/Basic-MongoDB-Commands/blob/master/m(17).pdf" style="text-decoration:none;">Make Least Privilege a Right (Not a Privilege)</a></li>   
  
<li><a target="_blank" href="https://github.com/manjunath5496/Basic-MongoDB-Commands/blob/master/m(18).pdf" style="text-decoration:none;">Labels and Event Processes
in the Asbestos Operating System</a></li> 

  
<li><a target="_blank" href="https://github.com/manjunath5496/Basic-MongoDB-Commands/blob/master/m(19).pdf" style="text-decoration:none;">Privacy-Preserving Browser-Side Scripting With BFlow</a></li> 

<li><a target="_blank" href="https://github.com/manjunath5496/Basic-MongoDB-Commands/blob/master/m(20).pdf" style="text-decoration:none;">The benefits and costs of writing a
POSIX kernel in a high-level language</a></li>

<li><a target="_blank" href="https://github.com/manjunath5496/Basic-MongoDB-Commands/blob/master/m(21).pdf" style="text-decoration:none;">The Benefits and Costs of Writing a POSIX Kernel in a High-Level Language</a></li>
<li><a target="_blank" href="https://github.com/manjunath5496/Basic-MongoDB-Commands/blob/master/m(22).pdf" style="text-decoration:none;">LLVM: A Compilation Framework for
Lifelong Program Analysis and Transformation</a></li> 
 <li><a target="_blank" href="https://github.com/manjunath5496/Basic-MongoDB-Commands/blob/master/m(23).pdf" style="text-decoration:none;">The Benefits and Costs of Writing a POSIX
Kernel in a High-Level Language [Cody Cutler]</a></li> 
 

   <li><a target="_blank" href="https://github.com/manjunath5496/Basic-MongoDB-Commands/blob/master/m(24).pdf" style="text-decoration:none;">Separating Web Applications from User Data Storage with BSTORE</a></li>
 
   <li><a target="_blank" href="https://github.com/manjunath5496/Basic-MongoDB-Commands/blob/master/m(25).pdf" style="text-decoration:none;">A Methodical Study of Web Crawler</a></li>                              
 <li><a target="_blank" href="https://github.com/manjunath5496/Basic-MongoDB-Commands/blob/master/m(26).pdf" style="text-decoration:none;">Certifying a File System Using
Crash Hoare Logic: Correctness in the Presence of Crashes</a></li>
 <li><a target="_blank" href="https://github.com/manjunath5496/Basic-MongoDB-Commands/blob/master/m(27).pdf" style="text-decoration:none;">A Differential Approach to
Undefined Behavior Detection</a></li>
   
 
   <li><a target="_blank" href="https://github.com/manjunath5496/Basic-MongoDB-Commands/blob/master/m(28).pdf" style="text-decoration:none;">Reducing Pause Times with Clustered Collection</a></li>
 
   <li><a target="_blank" href="https://github.com/manjunath5496/Basic-MongoDB-Commands/blob/master/m(29).pdf" style="text-decoration:none;">Reducing Pause Times With Clustered Collection [Cody Cutler] </a></li>                              

  <li><a target="_blank" href="https://github.com/manjunath5496/Basic-MongoDB-Commands/blob/master/m(30).pdf" style="text-decoration:none;">Certifying Program Execution with Secure Processors</a></li>
 
   <li><a target="_blank" href="https://github.com/manjunath5496/Basic-MongoDB-Commands/blob/master/m(31).pdf" style="text-decoration:none;">Providing a Shared File System in the Hare
POSIX Multikernel</a></li> 
    <li><a target="_blank" href="https://github.com/manjunath5496/Basic-MongoDB-Commands/blob/master/m(32).pdf" style="text-decoration:none;">Linux kernel vulnerabilities:
State-of-the-art defenses and open problems</a></li> 

   <li><a target="_blank" href="https://github.com/manjunath5496/Basic-MongoDB-Commands/blob/master/m(33).pdf" style="text-decoration:none;">Robust and Efficient Data Management for a Distributed Hash Table</a></li>                              

  <li><a target="_blank" href="https://github.com/manjunath5496/Basic-MongoDB-Commands/blob/master/m(34).pdf" style="text-decoration:none;">Choosing Internet Paths with High Bulk Transfer Capacity</a></li> 
 
  <li><a target="_blank" href="https://github.com/manjunath5496/Basic-MongoDB-Commands/blob/master/m(35).pdf" style="text-decoration:none;">Melody: A Distributed Music-Sharing System</a></li> 

  <li><a target="_blank" href="https://github.com/manjunath5496/Basic-MongoDB-Commands/blob/master/m(36).pdf" style="text-decoration:none;">A Keyword-Set Search System for Peer-to-Peer
Networks</a></li> 
 
<li><a target="_blank" href="https://github.com/manjunath5496/Basic-MongoDB-Commands/blob/master/m(37).pdf" style="text-decoration:none;">Herodotus: A Peer-to-PeerWeb Archival System</a></li>
 <li><a target="_blank" href="https://github.com/manjunath5496/Basic-MongoDB-Commands/blob/master/m(38).pdf" style="text-decoration:none;">A case study of server selection</a></li>
<li><a target="_blank" href="https://github.com/manjunath5496/Basic-MongoDB-Commands/blob/master/m(39).pdf" style="text-decoration:none;">The Scalable Commutativity Rule:
Designing Scalable Software for Multicore Processors</a></li>
 <li><a target="_blank" href="https://github.com/manjunath5496/Basic-MongoDB-Commands/blob/master/m(40).pdf" style="text-decoration:none;">Programming language optimizations for modular router configurations</a></li>                              
<li><a target="_blank" href="https://github.com/manjunath5496/Basic-MongoDB-Commands/blob/master/m(41).pdf" style="text-decoration:none;">Fast Bug Finding in Lock-Free Data Structures with
CB-DPOR</a></li>
<li><a target="_blank" href="https://github.com/manjunath5496/Basic-MongoDB-Commands/blob/master/m(42).pdf" style="text-decoration:none;">Finding Linearization Violations in Lock-Free
Concurrent Data Structures</a></li>
 
  <li><a target="_blank" href="https://github.com/manjunath5496/Basic-MongoDB-Commands/blob/master/m(43).pdf" style="text-decoration:none;">The Scalable Commutativity Rule:
Designing Scalable Software for Multicore Processors</a></li>
 <li><a target="_blank" href="https://github.com/manjunath5496/Basic-MongoDB-Commands/blob/master/m(44).pdf" style="text-decoration:none;">SCTP in Go</a></li>
   <li><a target="_blank" href="https://github.com/manjunath5496/Basic-MongoDB-Commands/blob/master/m(45).pdf" style="text-decoration:none;">Cloud Based Web Scraping for Big Data Applications</a></li>  
   
<li><a target="_blank" href="https://github.com/manjunath5496/Basic-MongoDB-Commands/blob/master/m(46).pdf" style="text-decoration:none;">Conclave: secure multi-party computation on big data</a></li> 
                             
<li><a target="_blank" href="https://github.com/manjunath5496/Basic-MongoDB-Commands/blob/master/m(47).pdf" style="text-decoration:none;">Corey: An Operating System for Many Cores</a></li>
</ul>









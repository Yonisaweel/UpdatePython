# Algorithm for file updates in Python

<h2>Description</h2>
Our task is to create an algorithm that uses Python code to check whether a particular 'allow list' contains any IP addresses identified on the 'remove list'. If so, we should remove those IP addresses from the file containing the allow list.
<br />


<h2>Languages and Utilities Used</h2>

- <b>Python</b>

<h2>Environments Used </h2>

- <b>https://www.w3schools.com</b>

<h2>Program walk-through:</h2>

<p align="center">
<h3>Open the file that contains the allow list:</h3> 
To open the file containing the allow list, we must first assign the <b>“allow_list.txt”</b> file to a variable named <b>import_file</b>. To do so, we must write it as <b>import_file = “allow_list.txt”</b> 
Once assigned, we can use the with keyword before the  Open() function to open the file contained in the allow_list.txt list. Since we are not modifying the data, we will use “r” to open it in read mode. And lastly, we must store it in a variable called file. In Python, this will be written as with open(import_file, “r”) as file:
<br />
  <br/>
<img src="https://i.imgur.com/pXMrT4H.png" height="50%" width="50%" alt="Python Steps"/>
  <h3> Read the file contents</h3>
  To read the file contents, we must use the <b>.read()</b> method. This converts the contents of the allow list file into a string. This method is added directly after the variable, and will be written as <b>file.read()</b>

Lastly, we will store this string in a variable called <b>ip_addresses</b>. To do so, we use the = operator and write it as <b>ip_addresses = file.read()</b>
<br />
<img src="https://i.imgur.com/i1WCjaO.png" height="50%" width="50%" alt="Python Steps"/>
<br />
<br />
<h3>Convert the string into a list:</h3> 
To convert the string into a list, we must use the <b>.split()</b> method. This converts the <b>ip_addresses</b> string into a list. Just like in the previous task, we must assign it to a variable. This time, we will assign it to the same variable, essentially re-assigning the format of <b>ip_addresses</b>. This will be written as <b>ip_addresses = ip_addresses.split()</b>

<img src="https://i.imgur.com/c3RsFqO.png" height="50%" width="50%" alt="Python Steps"/>
<br />
<h3>Iterate through the remove list: </h3>
To iterate through the remove list, we must use an iterative statement using a <b>for</b> loop. We will define a loop variable named element to loop through <b>ip_addresses</b>. Combining all of this, with a colon, gives us this statement - <b>for element in ip_addresses:</b>
<img src="https://i.imgur.com/nT9nMM7.png" height="50%" width="50%" alt="Python Steps"/>
<br />
<br />
<h3>Remove IP addresses that are on the remove list:  </h3>
To remove the IP addresses that appear on the remove list, we must use a conditional statement using <b>if</b>. If the <b>element</b> appears in the <b>remove_list</b> (This will be written as <b>if element in remove_list:</b> ), we must use the <b>.remove()</b> function to remove it. We will indent the next line and write it as <b>ip_addresses.remove(element)</b>
<img src="https://i.imgur.com/pwLeU2F.png" height="50%" width="50%" alt="Python Steps"/>
<br />
<br />
<h3>Update the file with the revised list of IP addresses:  </h3>
To update the file with the revised list of IP addresses, we must convert <b>“ip_addresses”</b>  back to a string. We do this by using the .join() function. Before the function, we will use <b>“\n”</b> so that it selects every string in the list and places each on a new line. This will be written as  <b>ip_addresses = “\n”.join(ip_addresses)</b>

Once assigned, we can use the <b>with</b> keyword before the  <b>Open()</b> function to open the file contained in the <b>allow_list.txt</b> list. Since we are replacing the data, we will use “w” to open it in write mode. And lastly, we must store it in a variable called <b>file</b>. In Python, this will be written as <b>with open(import_file, “w”) as file:</b>

To update the file contents, we must use the <b>.write()</b> method. This method is added directly after the variable, and will be written as <b>file.write(ip_addresses)</b>

<img src="https://i.imgur.com/V4xzzdm.png" height="50%" width="50%" alt="Python Steps"/>
<br />
<br />
<h2>Summary:</h2> 
  <br />
In this example, we created an algorithm that removes specific IP addresses and updates the list. We accomplished this by opening the text file using the <b>open()</b> function. We read it using the <b>.read()</b> function. We then created a loop to iterate through the <b>remove_list</b>, remove the IP addresses found in that list, and then update the <b>import_file</b> list.
</p>

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>

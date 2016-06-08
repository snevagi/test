
YODA Web Interface
==================

YODA Web supports the following actions: 
* Sign in (see [Sign in to Yoda Audit](#Sign_in_to_Yoda_Audit)) - sign in to use the tool
* Verification of Ownership (see [Verify Code Ownership](#Verify_Code_Ownership)) - for the assigned code owner to accept (verify) ownership assignments
* Decline Ownership Assignment (see [Decline Code Ownership](#Decline_Code_Ownership)) - to decline an assignment
* Reassignment of Ownership (see [Reassign Code Ownership](#Reassign_Code_Ownership)) - to suggest a new owner of a code file
* Query Ownership (see [Query Code Ownership](#Query_Code_Ownership)) - to identify what files a given person has been assigned or owns, or to identify who owns a given file

For information about the status of various elements of the code, refer to the following web pages: 
* IPOS Daemons and Libraries - <http://confluence.sj.us.am.ericsson.se/display/pduipseosmod/IPOS+Daemons+and+Libraries>
* Daemon Status Summary - <http://confluence.sj.us.am.ericsson.se/display/pduipseosmod/Daemon+Status+Summary>
* IPOS Libraries Status - <http://confluence.sj.us.am.ericsson.se/display/pduipseosmod/IPOS+Libraries+Status>

Use of YODA falls under one of three roles: 
* **Manager** - responsible for timely follow-throughs on code reviews, bug correction, design reviews, escalations, CI standards, and SQR accountability. These responsibilities include the following:  Maintaining code ownership assignments
	- Ensuring that all files have owners
	- Training team members and developing training documentation in a particular code area
	- Enforcing organization, coding standards, and style guidelines
	- Improving architectural integrity of one or more code areas

- **Code Owner** - responsible for reviewing code and API changes, documentation, test plans, and regression suite enhancements before general availability (GA). This responsibility includes the following:  Establishing policies and standards governing architectural evolution, integrity, and documentation
	- Ensuring long-term code quality
	- Maintaining and improving SRQ levels
	- Maintaining and improving SQR

- **Code Modifier** - responsible for making sure that the modified code meets coding, testing, and architectural standards set by the Code Owner. These responsibilities include the following:  Creating and updating unit test cases
	- Updating regression packages
	- Updating CI standards
	- Improving build time
	- Handling change requests (CRs)
	- Documenting changes

<h1 id='Sign_in_to_Yoda_Audit'>Sign in to YODA Audit</h1>
1. Sign on to YODA Audit. Go to <https://yoda.sj.us.am.ericsson.se/>
	![alt tag](img/name)|
	---|
	Yoda Sign In Dialog Box|
	![alt tag](img/name)|
	---|
	Yoda Sign In Dialog Box|
	Enter your signum and LAN password, then click <tt>Log In</tt>. The initial query dialog box is displayed.
	![alt tag](img/name)|
	---|
	Initial Query Dialog Box|
2. Enter your initial query. You have the following options:
	* SIGNUM - enter a specific signum or a regular expression. The example shows "XR%", which indicates a search that includes those files assigned to anyone whose signum begins with "XR".
	* Filename or Regex - enter the path or partial for a filename. If you prefer, enter a regular expression for the filename. By defaut the expression is "%" which searches for all filenames. The example searches for filenames located within the "comp" directory.
	* Project:Branch - Choose the project path and the branch of the file from the dropdown list. As shown in the example, the option "all:all" searches the list of files in all the projects and branches.
	* Show - place a check in the box beside <tt>Verified Files</tt>, <tt>Unverified FIles</tt>, or both.
3. Click <tt>Search</tt>. The search results are displayed.
	![alt tag]((img/name))|
	---|
	Audit Search Results|
	You have the following options:
	* Sign Out - click Logout <signum> in the upper right corner. The initial Log In screen is displayed.
	* Verification of Ownership (see Verify Code Ownership) - to accept (verify) ownership assignments; verification indicates that you understand your roles and responsibilities
	* Decline Ownership Assignment (see Decline Code Ownership) - to decline an assignment and let your manager determine the owner
	* Reassignment of Ownership (see Reassign Code Ownership) - to suggest the correct owner of a code file
	* Query Ownership (see Query Code Ownership) - to identify what files a given person is assigned or owns, or to identify who owns a given file
	
<h1 id='Reassign_Code_Ownership'>Reassign Code Ownership</h1>
1. Sign on to YODA Audit and enter your initial query with your signum (see [Sign in to Yoda Audit](#Sign_in_to_Yoda_Audit)) or, if you are already logged in, enter a new query (see [Query Code Ownership](#Query_Code_Ownership)). A regular expression in the <tt>Filename</tt> field is useful to limit the files for reassignment.
2. Select the files you want to reassign. Either click the button to <tt>Mark All Reassign</tt> or click the radio button next to each file to reassign ownership.
3. In the <tt>Reassign to</tt> field, enter the signum of the person you believe is the proper owner of the selected files.
	![alt tag]((img/name))|
	---|
	Audit Reassignment|
4. Click <tt>Save</tt>. YODA marks the files as assigned to the signum you supplied.

<h1 id='Decline_Code_Ownership'>Decline Code Ownership</h1>
Decline ownership if you do not accept the assignment of one or more files assigned to you.
1. Sign on to YODA Audit and enter your initial query (see [Sign in to Yoda Audit](#Sign_in_to_Yoda_Audit)) or, if you are already logged in, enter a new query (see [Query Code Ownership](#Query_Code_Ownership)). In the query, enter your signum and, if possible, a regular expression to limit the number of files returned.
2. Select the files whose assignment you want to decline. Either click the button to <tt>Mark All Declined</tt> or click the radio button in the Decline columns next to each file to decline ownership assignment.
	![alt tag](img/name)|
	---|
	Audit Decline Dialog Box|
3. Click <tt>Save<tt>. YODA marks the files to indicate that they need to be assigned.

<h1 id='Verify_Code_Ownership'>Verify Code Ownership</h1>
Verify ownership if you accept the assignment of one or more files assigned to you.
1. Sign on to YODA Audit and enter your initial query (see [Sign in to Yoda Audit](#Sign_in_to_Yoda_Audit)) or, if you are already logged in, enter a new query (see [Query Code Ownership](#Query_Code_Ownership)). In the query, enter your signum and select <tt>Show Unverified files</tt>.
2. Select the files whose assignment you want to accept. Either click the button to <tt>Mark All Verified</tt> or click the radio button in the Verified columns next to each file to decline ownership assignment.
	![alt tag](img/name)|
	---|
	Audit Verify Dialog Box|
3. Click <tt>Save</tt>. YODA marks the files to indicate that you have accepted ownership (verified).

<h1 id='Query_Code_Ownership>Query Code Ownership<h1>
The instructions in this section assume that you have already logged in as described in [Sign in to Yoda Audit](#Sign_in_to_Yoda_Audit), and you want to look at a new set of files.
1. Change one or more search criteria.
</br>	You have the following options:
		* SIGNUM - enter a specific signum or a regular expression. The example shows "%", which indicates a search that includes those files assigned to anyone.
		* Filename or Regex - enter the path or partial for a filename. If you prefer, enter a regular expression for the filename. The example searches for all filenames located in any "layer2/bridge" subdirectory within the "pkt" directory.
		* Show - place a check in the box beside <tt>Verified Files</tt>, <tt>Unverified Files</tt>, or both.
		![alt tag](img/name)|
		---|
		Query Criteria|
2. Click <tt>Search</tt>.
</br>	The search results are displayed.
		![alt tag](img/name)|
		---|
		Query Results|
		You have the following options:
		* Sign Out - click <tt>Logout <signum></tt> in the upper right corner. The initial <tt>Log In screen</tt> is displayed.
		* Verification of Ownership (see [Verify Code Ownership](#Verify_Code_Ownership)) - to accept (verify) ownership assignments; verification indicates that you understand your roles and responsibilities
		* Decline Ownership Assignment (see [Decline Code Ownership](#Decline_Code_Ownership)) - to decline an assignment and let your manager determine the owner
		* Reassignment of Ownership (see [Reassign Code Ownership](#Reassign_Code_Ownership)) - to suggest the correct owner of a code file
		* Query Ownership (see [Query Code Ownership](#Query_Code_Ownership)) - to identify what files a given person is assigned or owns, or to identify who owns a given file

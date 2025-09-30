# SIEM with Splunk

## Objective
<p>The objective of this lab was to gain hands-on experience with Splunk for security information and event management (SIEM). The focus was on learning how to search, filter, and analyze system logs, create structured views, and build custom dashboards to visualize and monitor log data effectively.</p>

<br><br>

## Skills Learned
<ul>
  <li>Navigated Splunk apps and accessed the Search & Reporting module.</li>
  <li>Performed basic searches using wildcards (*) to view all collected events.</li>
  <li>Explored Windows Event Viewer to understand system and security logs.</li>
  <li>Cleared security event logs to generate fresh data for analysis.</li>
  <li>Used field/value selections in Splunk to:
    <ul>
      <li>Add filters to refine search results.</li>
      <li>Exclude unnecessary data from queries.</li>
      <li>Remove filters to broaden results.</li>
    </ul>
  </li>
  <li>Created structured Table Views to simplify log analysis.</li>
  <li>Customized data presentation by selecting/deselecting log fields.</li>
  <li>Designed a custom Dashboard using Dashboard Studio:
    <ul>
      <li>Added and configured panels with SPL queries.</li>
      <li>Used <code>| fields -</code> command to remove irrelevant fields.</li>
      <li>Saved and set the dashboard as the home/default view.</li>
    </ul>
  </li>
  <li>Gained practical knowledge of SPL (Search Processing Language) for log filtering and visualization.</li>
</ul>

<br><br>

## Tools used
<ul>
  <li>Splunk Enterprise – for log collection, searching, filtering, visualization, and dashboard creation.</li>
  <li>Windows Event Viewer – for accessing, clearing, and reviewing Windows system, application, and security logs.</li>
  <li>Search Processing Language (SPL) – Splunk’s query language used to filter, refine, and present log data.</li>
</ul>

<br><br>

## Basic Splunk Search

<p>navigate through apps and click search & reporting</p>
<img width="275" height="362" alt="image" src="https://github.com/user-attachments/assets/1893a74c-4214-459d-adb3-a2aa50525667" />

<br><br>

<p>
In the search bar, typed * and pressed ENTER.

This displayed all events collected from the local system.
</p>
<img width="1172" height="501" alt="image" src="https://github.com/user-attachments/assets/9c56cd8e-967e-4193-8b26-4d718366a045" />

<br><br>

<p>
Opened Event Viewer on the PC.

This tool is used to view system, security, and application logs.  
</p>
<img width="368" height="575" alt="image" src="https://github.com/user-attachments/assets/1a016631-d5dd-4562-abc1-4c4e69338954" />

<br><br>

<p>
In Event Viewer, navigated to Windows Logs → Security.

Right-clicked Security and selected Clear Log.

This action removed all previous security log entries.  
</p>
<img width="1068" height="702" alt="image" src="https://github.com/user-attachments/assets/780af2c3-53ce-4bce-ab80-d61a7b2a508e" />


<br><br>

<p>
While searching, clicked on a field/value to narrow down results.

Used “Add to search” option to refine the query.
</p>
<img width="543" height="466" alt="image" src="https://github.com/user-attachments/assets/d15aa915-1293-4f67-a2a3-1ec62d615bf0" />
<img width="1119" height="546" alt="image" src="https://github.com/user-attachments/assets/8bf30ebd-7925-4aab-bd96-2139917ceddc" />

<br><br>

<p>
While searching, also had the option to exclude items using Exclude from search.

Could also remove filters using Remove from search.

This helps refine results further.  
</p>
<img width="310" height="39" alt="image" src="https://github.com/user-attachments/assets/ed504c82-0f29-4cec-a0a4-e8516eee24a2" />
<img width="439" height="232" alt="image" src="https://github.com/user-attachments/assets/81bdbfc5-3942-43a5-a6f5-223800d7c1ce" />

<br><br>

## Create Table

<p>
Copied the input from the search bar.

Selected Create Table View to display the results in a structured table format.
</p>
<img width="1565" height="101" alt="image" src="https://github.com/user-attachments/assets/2f85c2c9-d1dc-4f89-9d64-fdb1e699150e" />

<br><br>

<p>
On the left panel, different log types were available for selection.

Deselected “Raw” logs to simplify the table view.  
</p>
<img width="1593" height="630" alt="image" src="https://github.com/user-attachments/assets/ca056290-5a1a-4235-b62a-140576d99a02" />

<br><br>

<p>
After adjusting selections, the view displayed a table with only the chosen fields.

This made the data easier to read and analyze.  
</p>
<img width="1081" height="264" alt="image" src="https://github.com/user-attachments/assets/476b0e80-43fd-4ff8-a83f-087b9c79ee52" />

<br><br>

## Create Dashboard

<p>
Opened Dashboards section.

Clicked Create New Dashboard to start building a custom one.
</p>
<img width="535" height="72" alt="image" src="https://github.com/user-attachments/assets/6bc06a4d-e4ac-4424-8b15-c209f8abd05d" />

<br><br>

<p>
Set Dashboard Title as Clear Logs.

Chose Dashboard Studio as the type.

Selected Grid layout mode for organizing panels.  
</p>
<img width="638" height="711" alt="image" src="https://github.com/user-attachments/assets/a69128a3-4e51-4734-819a-721fde043358" />

<br><br>

<p>
In Dashboard Studio, clicked the chart icon.

Added a table visualization to the dashboard.
</p>
<img width="522" height="334" alt="image" src="https://github.com/user-attachments/assets/18a1e045-d508-49a8-a2bf-d948dc5d5dfe" />

<br><br>

<p>
Added an SPL query to the table panel.

Pasted the search bar input from earlier into the query field.

Select apply and close

This populated the table with filtered log data. 

</p>
<img width="336" height="164" alt="image" src="https://github.com/user-attachments/assets/31d5635a-4f2e-4e0f-a5ad-e4d58efc699e" />

<br><br>

<p>
Used the | fields - command in SPL to remove unwanted columns.

This keeps the table focused only on the relevant fields.
</p>
<img width="332" height="155" alt="image" src="https://github.com/user-attachments/assets/daf92fef-ec34-49c4-baea-7a9a277f9a61" />
<p>before.</p>
<img width="1217" height="473" alt="image" src="https://github.com/user-attachments/assets/3686b50e-fb63-40f4-afdb-9c6dc6af782a" />
<p>after.</p>
<img width="1216" height="470" alt="image" src="https://github.com/user-attachments/assets/ff1498c8-a0fc-41fd-ac47-14ae20e50194" />

<br><br>

<p>Set the title to Clear Logs and Click Save</p>
<img width="334" height="82" alt="image" src="https://github.com/user-attachments/assets/3c5854e2-43ce-4e08-866a-5e38e3cd479c" />

<br><br>

<p>
Went back to the Dashboards section.

Located and clicked on the Clear Logs dashboard to open it.
</p>
<img width="1596" height="599" alt="image" src="https://github.com/user-attachments/assets/df973200-5448-4019-afd2-d9d5a9353823" />

<br><br>

<p>
Opened the Actions menu in Dashboards.

Selected Set as Home Dashboard to make Clear Logs the default view.  
</p>
<img width="1577" height="581" alt="image" src="https://github.com/user-attachments/assets/22e534bf-2a82-41c1-9ae6-85e3faf0f914" />

<br><br>

<p>
The Clear Logs dashboard is now saved under the Search & Reporting application.

Can access it directly from there anytime.
</p>
<img width="1574" height="714" alt="image" src="https://github.com/user-attachments/assets/9331100e-72a8-489c-b801-f6248ef4a90c" />
















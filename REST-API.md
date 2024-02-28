#  CometaRestAPIBackend

Any actions you can execute on the Cometa Frontend User Interface can be triggered programmatically via REST API. Cometa uses [Django](https://www.djangoproject.com/) for the backend REST API services. It is implemented in python.

Find below a short overview over REST API endpoints to use. Further down you find details on the specific endpoints, like Post parameters and Json results to be expected.

This documentation is work in progress and could need some help.


Execute a Feature / Test from Django
>* POST /backend/exectest/

Account roles
>* GET /backend/api/account_roles/

Accounts
>* GET /backend/api/accounts/
>* PATCH /backend/api/accounts/<user_id>/
>* DELETE /backend/api/accounts/<user_id>/

Actions
>* GET /backend/api/actions/

Applications
>* GET /backend/api/applications/
>* POST /backend/api/applications/

Browsers
>* GET /backend/api/browsers/

Departments
>* GET /backend/api/departments/
>* GET /backend/user/departments/

Environments
>* GET /backend/api/environments/
>* POST /api/environments/

Feature Results
>* GET /api/feature_results/<feature_id>/
>* POST /api/feature_results/

Features
>* GET /backend/api/features/
>* POST /api/features/

Folders
>* GET /backend/api/folders/
>* POST /backend/api/folders/
>* PATCH /backend/api/folders
>* DELETE /backend/api/folders/<folder_id>/remove/

Step Results
>* GET /backend/api/feature_results/<feature_result_id>/step_results/
>* POST /backend/api/feature_results/<feature_result_id>/step_results/

Steps
>* GET /backend/steps/<feature_id>/
>* POST /backend/steps/<feature_id>/patch/

Screenshots
>* GET /backend/screenshots/<step_result_id>/
>* GET /backend/screenshot/<screenshot_name>/
>* GET /backend/removeScreenshot/<screenshot_name>/

Variables
>* GET /backend/api/variables/<environment_name>/
>* POST /backend/api/variables/
>* DELETE /backend/api/variables/<variable_id>/

Others
>* GET /backend/addoidcaccount/
>* GET /backend/steps/<step_result_id>/pixel_diff/<pixel_diff>/
>* GET /backend/updateTask/
>* GET /backend/getJson/<feature_id>/
>* GET /backend/killTask/<feature_id>/
>* GET /backend/killTaskPID/<pid>/
>* GET /backend/stepsByName/
>* GET /backend/schedule/<feature_id>/
>* GET /backend/exectest/
>* GET /backend/info/
>* GET /backend/encrypt/
>* GET /backend/parseActions/
>* GET /backend/browsers/browserstack/
>* GET /backend/feature_results/<feature_result_id>/log/
>* GET /backend/feature_results/<feature_result_id>/remove/<feature_result_id>/
>* GET /backend/feature_runs/<run_id>/remove/

For more details see http://your_server:8000/docs/

All create <code>POST</code> methods returns code <code>201</code> and row inserted, if it is created correctly.
All request body parameters should be "application/json", unless specified.
All request responses are in JSON format, unless specified.

##  Execute a Feature / Test from Django

#### <code>POST /backend/exectest/</code>

##### Headers

* <code>HTTP_X_SERVER</code>: Confidential ... or none
* <code>AMVARAORIGIN</code>: CRONTAB ... or empty
* <code>Content-Type: application/json</code>

##### Request body

<pre><code class="json">
{
  "feature_id": 169,
  "wait": false
}
</code></pre>

Example Curl:
<pre>
curl -vvv --data '{"feature_id":147,"wait":false}' -H "Content-Type: application/json" -H "X_SERVER: none" -H "AMVARAORIGIN: CRONTAB" -X POST http://behave:8001/run_test/
</pre>

Implemented by: Alex

Changelog:
* 13.07.2020 RRO documentation and fixing latest changes breaking scheduling

#  %{color:#584492}Account roles%

###  <code>GET /backend/api/account_roles/</code>

Retrieve all available roles for accounts, this is used for Admin --> Accounts and will be empty if the user doesn't have permissions to it.

##### Request Examples

<code>http://localhost:8000/backend/api/account_roles/</code>

##### Output Example

<pre><code class="json">
[
  {
    "account_role_id":1,
    "user":1,
    "department":1
  },
  {
    "account_role_id":2,
    "user":2,
    "department":1
  }
]
</code></pre>

#  %{color:#584492}Accounts%

###  <code>GET /backend/api/accounts/</code>

Retrieve all available accounts in database, will be empty is user doesn't have enough permissions.

##### Request Examples

<code>http://localhost:8000/backend/api/accounts/</code>

##### Output Example

<pre><code class="json">
[
  {
    "user_id":2,
    "name":"Alex",
    "email":"alexb@gmail.com",
    "user_role":"DEVOPS",
    "created_on":"2020-07-17T13:50:56.584849",
    "last_login":"2020-07-17T21:07:47.920158",
    "favourite_browsers":[],
    "user_permissions": {},
    "departments":["Default"]
  }
]
</code></pre>

###  <code>PATCH /backend/api/accounts/<user_id>/</code>

Modify account information.

##### Request body

<pre><code class="javascript">
user_id: number;
name: string;
email: string;
user_role: string;
departments: number[];
created_on?: string;
last_login?: string;
</code></pre>

##### Request Examples

<code>http://localhost:8000/backend/api/accounts/26/</code>

###  <code>DELETE /backend/api/accounts/<user_id>/</code>

Delete an account by UserID

#  %{color:#584492}Actions%

###  <code>GET /backend/api/actions/</code>

Retrieve available actions.

#  %{color:#584492}Applications%

###  <code>GET /backend/api/applications/</code>

Retrieve available applications for the current user.

##### Request Examples

<code>http://localhost:8000/backend/api/applications/</code>

##### Output Example

<pre><code class="json">
[
  {
    "app_id": 1,
    "app_name": "App 1",
    "slug": "app-1"
  },
  {
    "app_id": 2,
    "app_name": "App 2",
    "slug": "app-2"
  }
]
</code></pre>

###  <code>POST /backend/api/applications/</code>

Create application.

##### Request Body

<pre><code class="javascript">
app_name: string;
</code></pre>

#  %{color:#584492}Browsers%

###  <code>GET /backend/api/browsers/</code>

Retrieve local browsers.

##### Request Examples

<code>http://localhost:8000/api/browsers/</code>

##### Output Example

<pre><code class="json">
[
  {
    "browser_id": 1,
    "browser_json": {
      "os": "Generic",
      "device": null,
      "browser": "chrome",
      "os_version": "Selenium",
      "real_mobile": false,
      "browser_version": "69"
    }
  }
]
</code></pre>

#  %{color:#584492}Departments%

###  <code>GET /backend/api/departments/</code>

Retrieve all available departments for the current logged user.
*NOTE:* If the current logged user has permissions of Admin/SUPERUSER, all departments in database will be retrieved.

##### Request Examples

<code>http://localhost:8000/backend/api/departments/</code>

##### Output Example

<pre><code class="json">
[
  {
    "department_id": 1,
    "department_name": "Department 1",
    "slug": "department-1"
  },
  {
    "department_id": 2,
    "department_name": "Department 2",
    "slug": "department-2"
  }
]
</code></pre>

###  <code>GET /backend/user/departments/</code>

Retrieve the available departments for the current logged user, only retrieves the departments assigned to the user.

##### Request Examples

<code>http://localhost:8000/backend/user/departments/</code>

##### Output Example

<pre><code class="json">
[
  {
    "department_id": 1,
    "department_name": "Department 1",
    "slug": "department-1"
  },
  {
    "department_id": 2,
    "department_name": "Department 2",
    "slug": "department-2"
  }
]
</code></pre>

#  %{color:#584492}Environments%

###  <code>GET /backend/api/environments/</code>

Retrieve environments available for the current logged user.

##### Request Examples

<code>http://localhost:8000/backend/api/environments/</code>

##### Output Example

<pre><code class="json">
[  
  {  
    "environment_id":1,
    "environment_name":"Environment 1"
  },
  {  
    "environment_id":2,
    "environment_name":"Environment 2"
  }
]
</code></pre>

###  <code>POST /api/environments/</code>

Create environment.

##### Request Body

<pre><code class="javascript">
environment_name: string;
</code></pre>

#  %{color:#584492}Feature Results%

###  <code>GET /api/feature_results/<feature_id>/</code>

Retrieve feature results.

##### Request Example

<code>http://localhost:8000/api/feature_results/26/</code>

##### Output Example

<pre><code class="json">
[  
  {  
    "feature_result_id":1730421,
    "feature_id":1,
    "result_date":"2018-04-04T22:46:36.247605Z",
    "feature_name":"Feature",
    "app_id":8,
    "app_name":"MIF",
    "environment_id":32,
    "environment_name":"ENV-1",
    "department_id":7,
    "department_name":"Dep-8",
    "browser_id":8,
    "browser_name":"Firefox",
    "total":89,
    "fails":94,
    "ok":67,
    "skipped":55,
    "execution_time":"5.57",
    "pixel_diff":2242,
    "success_rate":91,
    "screen_style":"/code/file.png",
    "screen_actual":"/code/file.png",
    "screen_diff":"/code/file.png"
  }
]
</code></pre>

###  <code>POST /api/feature_results/</code>

Create a new feature result (actually only used for behave).

##### Request Body

| *Parameter*    | *Type*                     | *Required* | 
|   feature_id  |    IntegerField       | Yes     |         
|   result_date        | Datetime        |  Yes    | 
|   feature_name   | CharField(max_length=100)            |   Yes   | 
|   app_id   | IntegerField       |   Yes   | 
|   app_name   | .CharField(max_length=100)    |   YEs   | 
|   environment_id         | IntegerField |  Yes    | 
|   environment_name     | CharField(max_length=10) | Yes | 
|   department_id     | CharField(max_length=10) | Yes | 
|   department_name     | CharField(max_length=100) | Yes | 
|   browser_id     | CharField(max_length=10) | Yes | 
|   browser_name     | CharField(max_length=100) | Yes | 
|   total     | IntegerField | Yes | 
|   fails     | IntegerField | Yes | 
|   ok     | IntegerField | Yes | 
|   skipped     | IntegerField | Yes | 
|   execution_time     | DecimalField(decimal_places=2, max_digits=10) | Yes | 
|   pixel_diff     | IntegerField | Yes | 
|   success     | BooleanField | Yes | 
|   screen_style     | CharField(max_length=100) | Yes | 
|   screen_actual     | CharField(max_length=100) | Yes | 
|   screen_diff     | CharField(max_length=100) | Yes | 

#  %{color:#584492}Features%

###  <code>GET /backend/api/features/</code>

Retrieve feature information's.

##### Request Examples

<code>http://localhost:8000/backend/api/features/</code>

###  <code>POST /api/features/</code>

Create feature.

##### Request Body

<pre><code class="javascript">
feature_name: string;
app_id: number;
app_name: string;
description: string;
environment_id: number;
environment_name: string;
browser_id: number;
browser_name: string;
browser_code: string;
department_id: number;
department_name: string;
steps: number;
schedule: string;
steps_content: GroupContent[];
wait: boolean;
browsers: BrowserstackBrowser[];
cloud: string;
depends_on_other: boolean;
send_mail: boolean;
email_address: string[];
email_subject: string;
email_body: string;
last_edited: number;
video: boolean;
</code></pre>

The schedule is saved in the crontab file inside cometa_behave docker.  
To view crontab inside container: <code>root@883b40ddbed0:/opt/code/behave_django# cat /etc/cron.d/crontab</code>
To view it outside: <code>cat  behave/schedules/crontab</code>

The output when an error occurs can be:

status code 400
<pre><code class="json">
{
  "Error": "Invalid app_id , not found in Application model"
}
</code></pre>

status code 500
<pre><code class="json">
{
  "Error" : "Schedule was not saved"
}
</code></pre>

#  %{color:#584492}Folders%

###  <code>GET /backend/api/folders/</code>

Retrieve available folders and feature of the current user.

##### Response schema example

<pre><code class="json">
{
  "features": Feature[],
  "folders": [
    {
      "features": Feature[],
      "folder_id": 1,
      "folders": [],
      "name": "New",
      "owner": 1,
      "parent_id": null
    }
  ]
}
</code></pre>

###  <code>POST /backend/api/folders/</code>

Create a folder.

##### Request body

<pre><code class="javascript">
name: string;
parent_id?: number;
</code></pre>

*NOTES:* If no parent_id is provided, it is null or 0, the parent folder will be the Home folder.

Also, to move a folder to inside another folder, provide the following in the same request:

<pre><code class="javascript">
old_folder: number;
new_folder: number;
</code></pre>

Both parameters are IDs.

###  <code>PATCH /backend/api/folders</code>

Rename a folder by FolderID.

##### Request body

<pre><code class="javascript">
folder_id: number;
folder_name: string;
</code></pre>

###  <code>DELETE /backend/api/folders/<folder_id>/remove/</code>

Deletes a folder by FolderID

#  %{color:#584492}Step Results%

###  <code>GET /backend/api/feature_results/<feature_result_id>/step_results/</code>

Retrieve step results for a given feature_result_id.

##### Request Examples

<code>http://localhost:8000/backend/api/feature_results/18599/step_results/</code>

##### Output Example

<pre><code class="json">
[
  {
    "step_result_id":9919776,
    "feature_result_id":18599,
    "step_name":"Step-9919776",
    "execution_time":"-0.95",
    "pixel_diff":2866,
    "ok":50,
    "fails":39,
    "skipped":96,
    "success":74
  }
]
</code></pre>


###  <code>POST /backend/api/feature_results/<feature_result_id>/step_results/</code>

Create a step result (mostly used for behave).

##### Request Body

| *Parameter*    | *Type*                     | *Required* | 
|   feature_result_id  |    IntegerField       | Yes     |         
|   step_name        | CharField(max_length=100)        |  Yes    |
|   step_id          | IntegerField  | Yes |
|   execution_time     | DecimalField(decimal_places=2, max_digits=10) | Yes | 
|   pixel_diff     | IntegerField | Yes | 
|   success        | BooleanField | Yes |

#  %{color:#584492}Steps%

###  <code>GET /backend/steps/<feature_id>/</code>

Retrieve the steps defined for a given feature.

##### Request Examples

<code>http://localhost:8000/backend/api/steps/</code>

##### Output Example

<pre><code class="json">
[
  {
    "id": 1,
    "feature_id": 1,
    "step_name": "Step 1",
    "enabled": true
  },
  {
    "id": 2,
    "feature_id": 2,
    "step_name": "Step 2"
  }
]
</code></pre>

###  <code>POST /backend/steps/<feature_id>/patch/</code>

Save the feature and steps info.

##### Request Body

<pre><code class="javascript">
feature_id: number;
steps: any;
description: string;
environment_id: number;
environment_name: string;
app_id: number;
app_name: string;
department_id: number;
department_name: string;
depends_on_other: boolean;
cloud: string;
browsers: BrowserstackBrowser[];
send_mail: boolean;
email_address: string[];
email_subject: string;
email_body: string;
send_mail_on_error: boolean;
last_edited: number;
video: boolean;
</code></pre>

#  %{color:#584492}Screenshots%

###  <code>GET /backend/screenshots/<step_result_id>/</code>

Retrieve available screenshot for a given step result.

##### Response example:

<pre><code class="json">
["AMVARA_63.png", "AMVARA_63_style.png", "AMVARA_63.png_diff.png"]
</code></pre>

###  <code>GET /backend/screenshot/<screenshot_name>/</code>

Retrieve screenshot from Django.
*NOTES:* Django will automatically compress the image at 70%, it will also detect if the requesting browser is WebP compatible and serve the image as WebP instead of JPG.

###  <code>GET /backend/removeScreenshot/<screenshot_name>/</code>

Deletes a screenshot from the server.
*NOTES:* If the screenshot removal requested is about the style/template version, another removal request should be done to remove the original template file, for example for a given feature and step index (index of step ignoring previous disabled steps):

<pre>http://localhost:8000/backend/removeScreenshot/AMVARA_23_4.png/</pre>

#  %{color:#584492}Variables%

###  <code>GET /backend/api/variables/<environment_name>/</code>

Retrieve variables names and values for a given environment.

###  <code>POST /backend/api/variables/</code>

Set variables for a given environment.

##### Request body

<pre><code class="json">
{
  "environment_name": "ENV-3",
  "variables": [
    {
      "variable_name": "password",
      "variable_value": "12345"
    }
  ]
}
</code></pre>

###  <code>DELETE /backend/api/variables/<variable_id>/</code>

Remove variable by it's ID.

#  %{color:#584492}Others%

###  <code>GET /backend/addoidcaccount/</code>

Retrieves the OIDC Account information.

###  <code>GET /backend/steps/<step_result_id>/pixel_diff/<pixel_diff>/</code>

Used from Behave to update the Pixel Difference on running features.

###  <code>GET /backend/updateTask/</code>

Used from Behave to update the task status of running features.

##### Request body

<pre><code class="javascript">
action: 'start' | 'finish';
browser: BrowserstackBrowser;
feature_id: number;
pid: number;
</code></pre>

###  <code>GET /backend/getJson/<feature_id>/</code>

Retrieves the JSON information of a given feature.

###  <code>GET /backend/killTask/<feature_id>/</code>

Kills all running feature results by it's Feature ID.

###  <code>GET /backend/killTaskPID/<pid>/</code>

Kill a specific running feature result.

###  <code>GET /backend/stepsByName/</code>

Retrieves the definition for a given feature name.

##### Request body

<pre><code class="javascript">
feature_name: string;
</code></pre>

###  <code>GET /backend/schedule/<feature_id>/</code>

Set schedule for a given feature.

##### Request body

<pre><code class="javascript">
schedule: string;
</code></pre>

*NOTES:* The format for the schedule is the same as in Cron. Leave empty to remove the schedule.

###  <code>GET /backend/exectest/</code>

Executes a given feature.

##### Request body

<pre><code class="javascript">
feature_id: number;
</code></pre>

###  <code>GET /backend/info/</code>

Retrieves some useful information from the server, like the compilation version.

###  <code>GET /backend/encrypt/</code>

Let the user encrypt or decrypt a value using the server token.

##### Request body

<pre><code class="javascript">
action: 'encrypt' | 'decrypt';
text: string;
</code></pre>

###  <code>GET /backend/parseActions/</code>

Using this API endpoint updates the available actions, parsing the actions.py file and saving it on database. It also sends a WebSocket Event to front in order to automatically update the actions without any reload.

###  <code>GET /backend/browsers/browserstack/</code>

Retrieves Browsertstack usable browsers.

###  <code>GET /backend/feature_results/<feature_result_id>/log/</code>

Retrieves the log information for a given feature result.

###  <code>GET /backend/feature_results/<feature_result_id>/remove/<feature_result_id>/</code>

Removes a feature result by it's ID. It will also remove the parent run object if it is finally empty.

###  <code>GET /backend/feature_runs/<run_id>/remove/</code>

Removes a feature run by it's ID. It will also remove all child feature results.
[![license](https://img.shields.io/github/license/mashape/apistatus.svg?maxAge=2592000)](https://opensource.org/licenses/MIT)


Rundeck Jobs Log GROK pattern for Graylog
==============================================

Pattern
-------

	"name":"RUNDECKJOBSLOG",
	"pattern":"\\[%{TIMESTAMP_ISO8601:rundeck_job_timestamp}\\] %{USERNAME:rundeck_job_user} %{WORD:rundeck_job_action} \\[%{DATA:rundeck_job_id}\\] %{WORD:rundeck_job_project} \\\"%{DATA:rundeck_job_jobname}\\\" \\(%{WORD:rundeck_job_commit}\\)"

Example message
---------------

	[2018-02-09 10:05:21,431] User1 modify [bed3228c-1eba-4448-b322-3363de3597fc] ProjectName "Group/JobName job1" (update)

Fields
------

	rundeck_job_timestamp: 2018-02-09 10:05:21,431
	rundeck_job_user: User1
	rundeck_job_action: modify
	rundeck_job_jobname: Group/JobName job1
	rundeck_job_project: ProjectName
	rundeck_job_commit: update
	rundeck_job_id: bed3228c-1eba-4448-b322-3363de3597fc
	

Installation
------------

Go to **Graylog Web Interface** -> **System** -> **Content Packs** then select *content_pack.json* file and upload it.

[![screen1](https://i.imgbox.com/HAsDC4FR.png)](https://i.imgbox.com/wP2n4HXH.png)
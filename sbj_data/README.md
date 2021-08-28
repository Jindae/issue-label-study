## Subject Information

Information and statistics collected and produced during the study, which includes projects, issues and labels.   
Detailed description for the files can be found [here](#headers).  
You can match entries between files using ```project_id```, ```issue_id```, and ```label_id```.   

- ```projects.csv```: information of the projects.
- ```project_close_dist.csv```: distribution of close rate and time for the projects.
- ```multi-prj-issue-ratio.csv```: the ratio of no-label, single, and multi label issues for Multi group projects.
- ```labels.tar.gz```: a compressed file for ```labels.csv```, which contains label information.

For issue data, we have large files which are not suitable for GitHub.   
Hence we share it via an external link [issue_data.tar.gz](https://seoultechackr-my.sharepoint.com/:u:/g/personal/jindae_kim_seoultech_ac_kr/EeD1xk4hmQJLq6aHm1DrvgUByMJRX5BBHE1-eAACov414w?e=YVCC55).   

## Headers

### projects.csv

- ```project_id```: the unique id of the current project.
- ```name```: project's name.
- ```language```: a representative language used in the project.
- ```issues```, ```closed_issues```: the number of issues and closed issues.
- ```total_labels```, ```default_labels```, ```custom_labels```: the numbers of total, default and custom labels defined in the project.
- ```forked```: the number of projects which forked the project.
- ```stars```, ```subscribers```, ```watchers```: the number of starts, subscribers and watchers of the project.
- ```created_at```: the timestamp when the project was created. 
- ```updated_at```: the timestamp of the most recent update of the project.
- ```used_total```, ```used_default```, ```used_custom```: the numbers of total, default and custom labels actually used in the project.
- ```nolabel```, ```single```, ```multi```: the numbers of issues with no, single, and multiple labels.
- ```nolabel_closed```, ```single_closed```, ```multi_closed```: the numbers of closed issues with no, single, and multiple labels.
- ```label_group```: the label group of the project - ```nolabel```|```single```|```multi```.

### project_close_dist.csv

- ```project_id```: the unique id of the project.
- ```label```: the project's label group - ```No Label```|```Single```|```Multi```.
- ```close_rate```: the average close rate of issues in the project.
- ```close_time```: the average close time of issues in the project.

### multi-prj-issue-ratio.csv

- ```NoLabel```: the ratio of no-label issues in the project.
- ```Single```: the ratio of single-label issues in the project.
- ```Multi```: the ratio of multi-label issues in the project.

### issues.csv (from issue_data.tar.gz)

- ```issue_id```: the unique id of the issue.
- ```project_id```: the unique id of a project which the issue was reported.
- ```issue_number```: the unique issue number within the project.
- ```state```: the state of the issue. e.g., ```open```, ```closed```.
- ```labels```: the number of labels assigned to the issue.
- ```created_at```: the timestamp when the issue was created.
- ```closed_at```: the timestamp when the issue was closed. Empty when it is not closed.

### issue_stat.csv (from issue_data.tar.gz)

- ```issue_id```: the unique id of the issue.
- ```label```: the label group of the issue - ```No Label```|```Single```|```Multi```.
- ```comments```: the number of comments of the issue.
- ```title_length```: the length of the issue's title.
- ```body_length```: the length of the issue's body.

### issue_close_time_dist.csv (from issue_data.tar.gz)

- ```issue_id```: the unique id of the issue.
- ```project_id```: the unique id of a project which the issue was reported.
- ```label```: the label group of the issue - ```No Label```|```Single```|```Multi```.
- ```close_time(days)```: the issue close time in days.

### labels.csv (from labels.tar.gz)

- ```project_id```: the unique id of a project which the issue was reported.
- ```issue_id```: the unique id of the issue.
- ```label_id```: the unique id of the label assigned to the issue.
- ```name```: the label's name.

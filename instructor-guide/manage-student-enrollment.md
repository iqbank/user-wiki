---
layout: default
title: Manage User Enrollment
parent: Instructor Guide
nav_order: 5
---
# Manage User Enrollment

{: .note-title }
> Note:
>
> This feature is only available to course instructors.

## Table of Contents
- [Bulk Enroll Users by CSV](#bulk-enroll-users-by-csv)
  - [CSV Format](#csv-format)
  - [Upload CSV](#upload-csv)
  - [Upload Results](#upload-results)
- [Individually Enrolling a User](#individually-enrolling-a-user)
- [Managing Enrolled Users](#managing-enrolled-users)

## Bulk Enroll Users by CSV 

The **Bulk Student Import** page allows instructors to enroll a list of users in a course using information provided in a CSV file. 

### CSV Format

Click on **Download Template** to download a starter CSV file. Ensure that the completed file meets the following formatting requirements:

- **Required headers**: `email`, `utorid`, `courseRole`, `fromDate`, `toDate`.

- **Course Role**: `courseRole` should be `STUDENT`, `TA`, or `INSTRUCTOR`.

- **Enrollment dates**: `fromDate` and `toDate` are optional and must use the YYYY-MM-DD format (eg: 2026-09-01).

- **Other constraints**: 
    - Only existing IQBank users can be imported. 
    - Each user is matched using both `email` and `utorid`. 
    - Rows that do not match an existing account are reported as errors, and no new accounts are created. If users need accounts created, please see [Accessing IQBank]({{ "/getting-started/accessing-iqbank.html" | relative_url }}) for further details.

![Bulk Student Import CSV Format]({{ "/assets/images/instructor-guide/bulk-student-import-csv-format.png" | relative_url }})
{: .guide-image .guide-image--medium }

### Upload CSV
After completing the CSV file, upload it to IQBank. Files must have a **.csv** extension, and be no larger than **5 MB**.

![Upload Bulk Student Import CSV]({{ "/assets/images/instructor-guide/bulk-student-import-csv.png" | relative_url }})
{: .guide-image .guide-image--medium }

### Upload Results
After the import runs, you will see a summary of:
- **Assigned**: Users successfully enrolled
- **Duplicates**: Number of rows skipped because the user was already enrolled
- **Errors**: Rows that could not be processed, listed individually

![Upload Bulk Student Import Success]({{ "/assets/images/instructor-guide/bulk-student-import-success.png" | relative_url }})
{: .guide-image .guide-image--medium }

*Example result after successfully enrolling two existing IQBank users using a properly formatted CSV file*
{: .guide-caption }

## Individually Enrolling a User

This option allow instructors to enroll a single existing IQBank user in a course.

From the **Management Tools** panel on the **Manage Course page**, click on **Add Student**.

![Add student page]({{ "/assets/images/instructor-guide/add-single-student.png" | relative_url }})
{: .guide-image .guide-image--medium }

In the **Add User to Course** window, complete the following fields, then click **Add User**: 

- **UTORid** (eg: `doejohn`)
- **Email address** (eg: `john.doe@mail.utoronto.ca`)
- **Course role** (one of `STUDENT`, `TA`, or `INSTRUCTOR`)
- **(Optional) From Date and To Date**: The period (YYYY-MM-DD) the role is active for. Leave these fields blank for an enrollment with no start and end date.
- **Other constraints**:
    - Both the UTORid and the email must match the same existing IQBank account. If they do not, a message will display: *"No existing user matches that UTORid and email."*
    - Adding a student to a course does not create an IQBank account for them. Please see [Accessing IQBank]({{ "/getting-started/accessing-iqbank.html" | relative_url }}) for details on obtaining an account.

![Add student panel]({{ "/assets/images/instructor-guide/add-single-student-panel.png" | relative_url }})
{: .guide-image .guide-image--small }

## Managing Enrolled Users

The **Enrolled Users** table at the bottom of the **Course Management** page lists everyone enrolled in the course (10 users at a time), with columns for:

- Name
- UTORid
- Email
- Role
- Enrolled (Start date)
- Ends (End date, if one was set)

Instructors can manage enrolled users using the following actions:

- **Search**: Use the search bar to find a user, and the **Search by** dropdown beside it to choose whether you are searching by Name, UTORid, or Email.

- **Filter**: Use the **Role** dropdown to show only Instructors, TAs, or Students. The default is "All roles".

- **Change a user’s role**: Use the **Role** dropdown in the user’s row to assign them the Instructor, TA, or Student role.

- **Unenroll a user**: Click on the (x) button at the far right of a user's row to unenroll them from the course. Instructors will be asked to confirm before the change takes effect.

![Manage Enrolled Users]({{ "/assets/images/instructor-guide/manage-enrolled-users.png" | relative_url }})
{: .guide-image .guide-image--medium }

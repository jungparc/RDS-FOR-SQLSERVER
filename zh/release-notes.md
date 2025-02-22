## Database > RDS for MS-SQL > Release Notes

### March 15, 2022

#### Added Features

* Added maintenance management function

#### Bug Fixes

* Fixed a bug where `,` could be inserted into numeric parameters

### January 11, 2022

#### Bug Fixes

* Fixed an issue where DB instance creation fails intermittently

### December 14, 2021

#### Feature Improvements

* Improved to display the name in addition to CIDR when selecting a subnet while creating an instance
* Changed the data path of the master database to the data volume

#### Bug Fixes

* Fixed a bug where you could select an event code that cannot be subscribed to when registering or modifying an event subscription
* Fixed a bug where unnecessary storage remained intermittently when deleting a DB instance
* Fixed an issue where, after restarting a DB instance, the DB instance is intermittently changed to connection unavailable status
* Fixed an issue where, when modifying a DB instance, the DB instance is temporarily changed to available status intermittently even though the task is not completed
* Fixed an issue where the disk transfer rate was displayed incorrectly on the server dashboard

### November 9, 2021

#### Added Features

* Added a feature to send email and SMS notifications on scheduled hypervisor migrations

#### Bug Fixes

* Fixed an issue where CloudTrail's response body is truncated if it is long

#### Others

* Added billing for root volumes

### October 12, 2021

#### Feature Improvements

* Changed the code so that, when a version error occurs while restoring from backup in object storage, the error is recorded in event log.
* Added performance metrics collection items.
* Modified the error message displayed when backup deletion fails, to indicate in detail which operation caused the failure.
* Added a feature to perform scheduled hypervisor migration on the RDS for MS-SQL web console.

### September 14, 2021

#### Bug Fixes

* Fixed a bug where manual backup could be performed during the rebuilding of monitoring server.
* Fixed a bug where the database operated as if dropping had succeeded even if it failed due to an MS-SQL issue while dropping the database with a drop procedure.

### August 10, 2021

#### Feature Improvements

* Modified to verify the integrity of the file by checking the checksum when uploading/downloading a file.
* Fixed to return an error when the quota is insufficient by performing a quota check in advance when creating instances, changing types, and expanding storage.

#### Bug Fixes

* Fixed an issue where the database items in the web console were incorrectly synchronized when repeatedly creating and deleting databases in instances with high availability.
* Fixed an issue where backups failed intermittently when repeatedly creating and deleting databases in instances with high availability.
* Fixed an issue where it was impossible to restore when trying to restore to a specific point in time.
* Fixed an issue where backups in use for restore could be deleted
* Fixed an issue where the log could not be looked up in SQL Server 2017 Standard (14.0.3294.2)

### July 13, 2021

#### Added Features

* Force restart feature added

#### Bug Fixes

* Fixed a bug in which the reset button in the event list doesn’t work

### June 15, 2021

* Added the notification group feature
* Added user group feature

### May 11, 2021

### Feature Updates

* Added the checkbox that selects all backups

### April 13, 2021

#### Features Development

* Modified the system so that users can select multiple backups and delete them at once
* Modified the system so that object storages can be restored with a different name

#### Features Updates

* Modified the system so that instances of which memory is less than 8GB cannot access the high availability feature

### March 9, 2021

####  Bug Fixes

* Added a verification logic to prevent the use of a manual backup of database of which recovery model is `SIMPLE` for restoration of high availability configuration

### February 9, 2021

#### Feature Updates

* New instance type supported (x1 type)

#### Bug Fixes

* Fixed an issue where manual backup of a database of which recovery model is set to `SIMPLE` fails

### January 12, 2021

#### Feature Development

- Added the Stored Procedure for deleting databases

#### Feature Updates

- Fixed the application to leave additional server events for creating instance
- Fixed the application to display the instance type category in the same manner as in the Compute & Network service
- Fixed the application to leave events on promoted primary servers when an auto failover occurs.

#### Bug Fixes

- Fixed a bug where an error would occur when restoring a previous backup after an auto failover.
- Fixed a bug where the database of the web console would sometimes be exposed multiple times on a high availability DB instance.
- Fixed a bug where an error would occur when restoring to the point in time right after creating instance
- Fixed a bug where a DB instance with a completed failover would often fail to edit.
- Fixed a bug where the name of a DB instance with a completed failover would not be exposed on the web console usage page under specific conditions.

### December 15, 2020

#### Feature Development

- High availability DB instance feature added

### October 13, 2020

#### Bug Fixes

- Fixed a bug of DB instance restoration failure where it is rolled back to the time it was created

### September 15, 2020

#### Feature Updates

- Updated UX for a more subdivided representation of DB instance status

#### Bug Fixes

- Fixed a bug of failure to roll back to a certain point of time right after a new database is created
- Fixed a UI bug where the date insertion component failed to operate properly when Japanese was selected

#### Others

- Excluded c2.c2m2 instance from instances that can be generated

### August 11, 2020

#### Feature Updates

- Updated UX to use DB instance type and storage size of the original DB instance as default

#### Bug Fixes

- Fixed a bug that only allows restoration to 5 minutes before a desired time point.
- Fixed a bug where attempts to access a DB instance creator page are led to an error page in the absence of a subnet.

### July 14, 2020

#### Release of Alpha Service 

* TOAST Relational Database Service for SQL Server (RDS for MS-SQL) provides Microsoft SQL Server in the cloud environment.

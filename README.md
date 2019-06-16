# Advanced Performance Tuning for Oracle - Public Download page
This is where the latest release of APTO will reside.

APTO Release notes:
---- v3.0-3.7
[ x ] Show all CPU perf reports 
[ x ] Use passwords in Database domain class
[ x ] Create alternate logins per DB
[ x ] Create icons for DB Application types
[ x ] Create local DB user with all HIST-tables
[ x ] Make connectionpool reconnect when conn lost
[ x ] Remove Jenkins dependency completely from perf tool
[ x ] Purge perf tables periodically from grails
[ x ] Schedule periodic pulls every hour, 
[ x ] Enroll new databases into new Perf Tool DB
[ x ] Fix all labels
[ x ] Create grails build-environment on Jenkins
[ x ] Figure out why initial rendering of perf summary doesn't display SQL table (Related to initial fetch from target DB)
[ x ] Fix extra padding around objects
[ x ] Make application auto-encrypt new entries on first pass
[ x ] Obfuscate passwords in Database domain class
[ x ] Introduce system defaults as separate table
		=> Include SYS in active sessions Y/N
		=> # of samples for profiling
[ x ] Time-out connection to a target oracle database after a configurable # of seconds 
[ x ] Added error messages when DB connections fail for easier troubleshooting
[ x ] Fix user role icons in role view (Remove RICEW manager reference)
[ x ] Add test connection button on DB list page
[ x ] Show all IO perf reports 
[ x ] Fixed datatype text on imageURL columns
[ x ] Allow real-time tkprof to work even when single quotes in queries of session traced
[ x ] Collect SQLText on snapshot for remaining unknown queries
[ x ] Figure out error when deleting database types
[ x ] Fix bug in average CPU for 24hrs
[ x ] No longer pull PL/SQL as top SQLs
[ x ] Sort databases in DB lists for both mgmt and perf listing
[ x ] Fixed purging of non-existing databases
[ x ] Add ROLE_USER automatically for new users
[ x ] Sort users alphabetically
[ x ] Make all environment-names uppercase
[ x ] Encrypt options with "password" as part of name
[ x ] Moved settings to new generic options table 
[ x ] Add year/mm/dd to logging
[ x ] Make perf top SQL list fit on page width (Now it's being cut off with no scrollbar)
[ x ] Display explain plan for a specific query
[ x ] Option to use simple v$session query to avoid perf issues
[ x ] Fixed bug that made CPU time and executions sometimes be displayed as a negative number 
due to statistics resetting / SQLAREA flushing or plans changing
[ x ] Direct link to DB management page from perf summary if ROLE_ADMIN
[ x ] Direct link to perf report from DB management page
[ x ] Fixed 12c privilege issue with sys.user$
[ x ] Fetch explain plan from currently connected node (No support for RAC easy to implement)
[ x ] Add top 10 SQL by hour in separate page
[ x ] Add top 10 Sysevents by hour in separate page
[ x ] Introduced pull of V$SYS_EVENT for overall event statistics to database repository
[ x ] Add email to users and email plugin
[ x ] Add login-URL to settings to include in invite-email
[ x ] Option to disable mail
[ x ] Allow user to control wether or not users should be emailed when creating user
[ x ] Improved navigation between reports
[ x ] Also retrieve entire SQL when running explain (fetch from opdb)
[ x ] Fetch DB version from DB and place on main page
[ x ] Verify that dictionary read account has appropriate system privilege
----- v3.8
[ x ] Add logos to top sysevents and top sql by hour as well
[ x ] Limit top events by hour to events with wait > 0s
----- v3.9.1
[ x ] Fixed bug that sorts top wait events by hour incorrectly
[ x ] Fixed bug with sysmetric summary not being collected properly
[ x ] Set session timeout to 1hr
----- v3.10.2
[ x ] Healthcheck page: With query to find missing foreign key indexes:
[ x ] Healthcheck show users with default passwords
[ x ] Fixed dependency on sys.user$ grant
----- v3.11
[ x ] Show Almost expired pwd in healthcheck
[ x ] Remove USER_ROLE requirement, and change security to authenticated only
[ x ] Removed role management, only ROLE_ADMIN remains
[ x ] Added email option to control who receives the support emails when errors occur
[ x ] Added functionality to trigger snapshots in all databases
[ x ] Fixed bug in Enq: TM Contention extract in healthcheck
----- v3.11.1
[ x ] Removed ROLE management, not needed for this version
[ x ] Enhanced reports, no longer report first hour as huge numbers when there has been an outage in tool
----- v3.11.2
[ x ] Fixed performance issue with new outage filtering in postgres
------ v3.12.0
[ x ] Improved logging in MailService, to see when emails are being sent or attempted sent
[ x ] Split common services into com.accenture.common to better enable reuse across assets
[ x ] Introduced Environment Types [DEV/TEST/QA/PROD]

------ v3.13
[ x ] Show current indexing / table stats (DBA_IND_COLUMNS for a table explained)
[ x ] Bug; CLOBs showing as oracle.sql.CLOB@10fb4d95, will now show max 4000 characters

------ v3.14
[ x ] Added additional explain plan information, indexing and stats for tables involved in query

------ v3.15
[ x ] Made version that allows to connect to the Oracle DBs using different protocol than TCP

------ v3.16
[ x ] Bugfix on Edit Database Type

------ v3.17
[ x ] Added dbversion to database list on main page
[ x ] Fixed copyright year cosmetic issue (From 2016 => 2017)
[ x ] Fixed bug causing program to be blank on 12c

------ v3.18
[ X ] In explain plan view for a SQL, show owner/name of code object, and line #
[ X ] DB Summary Page - Show if DB not in archivelog
[ X ] Add RMAN backup summary status to DB list showing failures/success last two weeks
[ X ] If V$RMAN_BACKUP_JOB_DETAILS contain failed jobs last two weeks, display warning
[ X ] if V$RMAN_BACKUP_JOB_DETAILS don’t contain successful INCR BACKUP in last two weeks, display warning
[ X ] Added SQL explain plan to current SQL in Active sessions view
[ X ] Cosmetic fixes on RMAN status colors
[ X ] Added detail button on RMAN status to show output in last two weeks from RMAN jobs

------ v3.19
[ X ] Make RMAN details toggled to Admin view only as option, default No
[ X ] Secure RMAN details to check roleAdmin of current user if admin only option set
[ X ] Indicate cartesian joins on queries with red to help analysis in explain plan
[ X ] Show # of CPU seconds in last 24h per DB on summary page

------ v3.20_Build_452
[ X ] Add default DB types with images for the commonly used ERPs and apps (EBS, PSFT, Siebel)
[ X ] Add OEM/Dev Tools CPU curve on second graph showing overhead CPU
[ X ] Cosmetic; Improved version numbering for build counting

------ v4.0_Build_453
[ X ] Add tooltip descriptive text on how to analyze graphs in performance report
[ X ] Shows disable statements to disable the auto-task subsystem in healthcheck
[ X ] Cloud reporting (Central multi-tenancy cloud repository across clients) Cannot see realtime or explain plan
[ X ] Healthcheck also shows queries with full table scans / cartesian joins taking a lot of CPU
[ X ] Snapshot history of V$SESSION to drill active sessions during a certain hour

------ v4.0_Build_454
[ X ] About page added with link to newest versions
[ X ] Show CPU(s) and executions in explain plan
[ X ] Added generation timestamp on all pages 

------ v4.0_Build_455
[ X ] Introduce Monitoring Group (With one or more DBs)
[ X ] Monitoring - Custom rules implemented, allowing you to write your own SQL
[ X ] Monitoring - Notify DBAs for each DB triggering monitoring alerts
[ X ] Auto-create APTO_HIST tables
[ X ] Show sessions and processes allocation vs. max over time

------ v4.0_Build_461
[ X ] Improved logging around autogeneration of the postgres DB, showing schema structures

------ v4.1_Build_462
[ X ] SQL-ID editor, to flag and update attributes about a SQL-ID manually / manage aliases tied [ X ] Cosmetic - removed 5 ‘-’ characters on explanatory comment block dividers
[ X ] Cosmetic - Rearranged columns to show program/line before SQL on main report
to a specific SQL-ID (Same query has same SQL-ID across databases)
[ X ] Also shows function-based index expression columns on explain plan (DBA_IND_EXPRESSIONS)

------ v4.2_Build_464
[ X ] Fixed performance issue with Exadata RAC databases during profiling - Samplecount should now work with 1000 samples again

------ v4.2_Build_465
[ X ] Active sessions and session history now shows the hostname the session is coming from
[ X ] Environment Type role based access. Admin can see all environment types.
[ X ] Show version in footer on all pages, along with current date/time
[ X ] Monitoring page showing monitoring alert history 


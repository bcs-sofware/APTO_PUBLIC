<h1>Advanced Performance Tuning for Oracle - Public Download page</h1>
<b>This is where the latest release of APTO will reside.</b>

<h2>APTO Release notes:</h2>

<h3>v4.9_Build_484 - 2020 JAN 6</h3>
[ X ] Fixed bug in purge causing purge job to fail on a daily basis - Leading to growing repository size over time

<h3>v4.9_Build_483 - 2019 DEC 11</h3>
[ X ] Fixed bug that skewed/misreported 24h CPU and only accounted for one of the RAC nodes in RAC cluster
[ X ] Increase retention of lower-impact queries to closer align hourly CPU usage on SQL rather than just accounting for the highest impacting queries.

<h3>v4.9_Build_482 - 2019 NOV 13</h3>
[ X ] Fixed bug that would sometimes not show the tables/indexes for a explained query in a RAC DB

<h3>v4.9_Build_481 - 2019 AUG 17</h3>
[ X ] Healthcheck now isolates objects that need to be reorganized due to high write contention (enq: TX - allocate ITL entry)
<br>[ X ] Ability to drill down on sysevent to isolate SQLs causing certain event waits
<br>[ X ] Show top 15 sysevent waits in main page with drilldown capability to find underlying SQLs
<br>[ X ] Improved explain plan to not show duplicate plans in a RAC DB

<h3>v4.8_Build_479 - 2019 AUG 14</h3>
[ X ] Improved performance of health-check, no longer show cartesian join (Use explain)
<br>[ X ] Now correctly maps queries to the user running them, not the schema parsing them

<h3>v4.7_Build_477 - 2019 AUG 13</h3>
[ X ] Show how long ago the last snapshot was taken on top of performance summary page
<br>[ X ] Properly purge all APTO tables in Postgres repository
<br>[ X ] Optimized snapshot speed to only pull queries that are consuming a significant amount of resources on an hourly basis. Expect approximately 10x faster snapshots
<br>[ X ] More consistently store SQL queries that are being captured in various pages, to minimize the chance of empty explain plan page showing up when clicking on SQL ID buttons.

<h3>v4.6_Build_474 - 2019 JUL 30</h3>
[ X ] Also shows DB cache advisor to help optimize memory allocation in instance

<h3>v4.5_Build_473 - 2019 JUL 20</h3>
[ X ] Fixed bug with program name not fetched correctly in systems using EBR (Edition Based Redefintition)
<br>[ X ] Option to limit # of executions that control flagging for unbound SQL (default 1000)
<br>[ X ] Fixed bug showing too high CPU 24h on databases recently added (First snapshot will not count towards total)
<br>[ X ] In top per hour listings, color code #1, 2 and 3 in varying degrees of red

<h3>v4.5_Build_472 - 2019 JUL 14</h3>
[ X ] Also show service accounts / schemas from unbound SQL in module CPU piechart

<h3>v4.5_Build_470 - 2019 JUL 07</h3>
[ X ] Fixed explain plan not showing on RAC if running DBMS_XPLAN in wrong RAC node
<br>[ X ] Fixed bug in explain plan erroring out of SQL ID no longer in memory
<br>[ X ] Fixed bug not showing tables with full table scans in health check

<h3>v4.4_Build_469 - 2019 JUL 02</h3>
[ X ] Added more debugging in DatabaseService.explainStatement
<br>[ X ] Fixed bug in retrieving segment sizes on RAC databases in certain situations during explain plan

<h3>v4.4_Build_468 - 2019 JUN 29</h3>
[ X ] Performance Report now shows areas of system running unbound SQL (Lack of cursor sharing causing parse overhead)
<br>[ X ] Reskinned for company

<h3>v4.3_Build_467 - 2019 JUN 24</h3>
[ X ] Active sessions now also show the blocking sessions information
<br>[ X ] Add segment size information for table stats during explain
<br>[ X ] Updated icons for various options
<br>[ X ] When a monitoring rule throws an exception, log that in the monitoring history
<br>[ X ] Sort lists in indexReport based on environmentType sorting + alphabetically
<br>[ X ] Fixed bug in graph for CPU second trend by hour on Dev Tools
<br>[ X ] Added ETL/ODI series to overall CPU usage graph
<br>[ X ] Added top 10 modules on CPU to overall performance report
<br>
<h3>v4.2_Build_465 - 2019 JUN 16</h3>
[ X ] Active sessions and session history now shows the hostname the session is coming from
<br>[ X ] Environment Type role based access. Admin can see all environment types.
<br>[ X ] Show version in footer on all pages, along with current date/time
<br>[ X ] Monitoring page showing monitoring alert history 
<h3>v4.2_Build_464 - 2019 JUN 08</h3>
[ X ] Fixed performance issue with Exadata RAC databases during profiling - Samplecount should now work with 1000 samples again
<br>
<h3>v4.1_Build_462 - 2019 MAY 30</h3>
[ X ] SQL-ID editor, to flag and update attributes about a SQL-ID manually / manage aliases tied 
<br>[ X ] Cosmetic - removed 5 ‘-’ characters on explanatory comment block dividers
<br>[ X ] Cosmetic - Rearranged columns to show program/line before SQL on main report
<br>to a specific SQL-ID (Same query has same SQL-ID across databases)
<br>[ X ] Also shows function-based index expression columns on explain plan (DBA_IND_EXPRESSIONS)
<br>
<h3>v4.0_Build_461 - 2018 AUG 09</h3>
[ X ] Improved logging around autogeneration of the postgres DB, showing schema structures
<br>
<h3>v4.0_Build_455 - 2017 OCT 10</h3>
[ X ] Introduce Monitoring Group (With one or more DBs)
<br>[ X ] Monitoring - Custom rules implemented, allowing you to write your own SQL
<br>[ X ] Monitoring - Notify DBAs for each DB triggering monitoring alerts
<br>[ X ] Auto-create APTO_HIST tables
<br>[ X ] Show sessions and processes allocation vs. max over time
<br>
<h3>v4.0_Build_454</h3>
[ X ] About page added with link to newest versions
<br>[ X ] Show CPU(s) and executions in explain plan
<br>[ X ] Added generation timestamp on all pages 
<br>
<h3>v4.0_Build_453</h3>
[ X ] Add tooltip descriptive text on how to analyze graphs in performance report
<br>[ X ] Shows disable statements to disable the auto-task subsystem in healthcheck
<br>[ X ] Cloud reporting (Central multi-tenancy cloud repository across clients) Cannot see realtime or explain plan
<br>[ X ] Healthcheck also shows queries with full table scans / cartesian joins taking a lot of CPU
<br>[ X ] Snapshot history of V$SESSION to drill active sessions during a certain hour
<br>
<h3>v3.20_Build_452</h3>
[ X ] Add default DB types with images for the commonly used ERPs and apps (EBS, PSFT, Siebel)
<br>[ X ] Add OEM/Dev Tools CPU curve on second graph showing overhead CPU
<br>[ X ] Cosmetic; Improved version numbering for build counting
<br>
<h3>v3.19</h3>
[ X ] Make RMAN details toggled to Admin view only as option, default No
<br>[ X ] Secure RMAN details to check roleAdmin of current user if admin only option set
<br>[ X ] Indicate cartesian joins on queries with red to help analysis in explain plan
<br>[ X ] Show # of CPU seconds in last 24h per DB on summary page
<br>
<h3>v3.18</h3>
[ X ] In explain plan view for a SQL, show owner/name of code object, and line #
<br>[ X ] DB Summary Page - Show if DB not in archivelog
<br>[ X ] Add RMAN backup summary status to DB list showing failures/success last two weeks
<br>[ X ] If V$RMAN_BACKUP_JOB_DETAILS contain failed jobs last two weeks, display warning
<br>[ X ] if V$RMAN_BACKUP_JOB_DETAILS don’t contain successful INCR BACKUP in last two weeks, display warning
<br>[ X ] Added SQL explain plan to current SQL in Active sessions view
<br>[ X ] Cosmetic fixes on RMAN status colors
<br>[ X ] Added detail button on RMAN status to show output in last two weeks from RMAN jobs
<br>
<h3>v3.17</h3>
[ x ] Added dbversion to database list on main page
<br>[ x ] Fixed copyright year cosmetic issue (From 2016 => 2017)
<br>[ x ] Fixed bug causing program to be blank on 12c
<br>
<h3>v3.16</h3>
[ x ] Bugfix on Edit Database Type
<br>
<h3>v3.15</h3>
[ x ] Made version that allows to connect to the Oracle DBs using different protocol than TCP
<br>
<h3>v3.14</h3>
[ x ] Added additional explain plan information, indexing and stats for tables involved in query
<br>
<h3>v3.13</h3>
[ x ] Show current indexing / table stats (DBA_IND_COLUMNS for a table explained)
<br>[ x ] Bug; CLOBs showing as oracle.sql.CLOB@10fb4d95, will now show max 4000 characters
<br>
<h3>v3.12.0</h3>
[ x ] Improved logging in MailService, to see when emails are being sent or attempted sent
<br>[ x ] Split common services into com.accenture.common to better enable reuse across assets
<br>[ x ] Introduced Environment Types [DEV/TEST/QA/PROD]
<br>

<h3>v3.11.2</h3>
[ x ] Fixed performance issue with new outage filtering in postgres

<h3>v3.11.1</h3>
[ x ] Removed ROLE management, not needed for this version
<br>[ x ] Enhanced reports, no longer report first hour as huge numbers when there has been an outage in tool

<h3>v3.11</h3>
[ x ] Show Almost expired pwd in healthcheck
<br>[ x ] Remove USER_ROLE requirement, and change security to authenticated only
<br>[ x ] Removed role management, only ROLE_ADMIN remains
<br>[ x ] Added email option to control who receives the support emails when errors occur
<br>[ x ] Added functionality to trigger snapshots in all databases
<br>[ x ] Fixed bug in Enq: TM Contention extract in healthcheck

<h3>v3.10.2</h3>
[ x ] Healthcheck page: With query to find missing foreign key indexes:
<br>[ x ] Healthcheck show users with default passwords
<br>[ x ] Fixed dependency on sys.user$ grant

<h3>v3.9.1</h3>
[ x ] Fixed bug that sorts top wait events by hour incorrectly
<br>[ x ] Fixed bug with sysmetric summary not being collected properly
<br>[ x ] Set session timeout to 1hr

<h3>v3.8</h3>
[ x ] Add logos to top sysevents and top sql by hour as well
<br>[ x ] Limit top events by hour to events with wait > 0s

<h3>v3.0-3.7</h3>
[ x ] Show all CPU perf reports 
<br>[ x ] Use passwords in Database domain class
<br>[ x ] Create alternate logins per DB
<br>[ x ] Create icons for DB Application types
<br>[ x ] Create local DB user with all HIST-tables
<br>[ x ] Make connectionpool reconnect when conn lost
<br>[ x ] Remove Jenkins dependency completely from perf tool
<br>[ x ] Purge perf tables periodically from grails
<br>[ x ] Schedule periodic pulls every hour, 
<br>[ x ] Enroll new databases into new Perf Tool DB
<br>[ x ] Fix all labels
<br>[ x ] Create grails build-environment on Jenkins
<br>[ x ] Figure out why initial rendering of perf summary doesn't display SQL table (Related to initial fetch from target DB)
<br>[ x ] Fix extra padding around objects
<br>[ x ] Make application auto-encrypt new entries on first pass
<br>[ x ] Obfuscate passwords in Database domain class
<br>[ x ] Introduce system defaults as separate table
<br>		=> Include SYS in active sessions Y/N
<br>		=> # of samples for profiling
<br>[ x ] Time-out connection to a target oracle database after a configurable # of seconds 
<br>[ x ] Added error messages when DB connections fail for easier troubleshooting
<br>[ x ] Fix user role icons in role view (Remove RICEW manager reference)
<br>[ x ] Add test connection button on DB list page
<br>[ x ] Show all IO perf reports 
<br>[ x ] Fixed datatype text on imageURL columns
<br>[ x ] Allow real-time tkprof to work even when single quotes in queries of session traced
<br>[ x ] Collect SQLText on snapshot for remaining unknown queries
<br>[ x ] Figure out error when deleting database types
<br>[ x ] Fix bug in average CPU for 24hrs
<br>[ x ] No longer pull PL/SQL as top SQLs
<br>[ x ] Sort databases in DB lists for both mgmt and perf listing
<br>[ x ] Fixed purging of non-existing databases
<br>[ x ] Add ROLE_USER automatically for new users
<br>[ x ] Sort users alphabetically
<br>[ x ] Make all environment-names uppercase
<br>[ x ] Encrypt options with "password" as part of name
<br>[ x ] Moved settings to new generic options table 
<br>[ x ] Add year/mm/dd to logging
<br>[ x ] Make perf top SQL list fit on page width (Now it's being cut off with no scrollbar)
<br>[ x ] Display explain plan for a specific query
<br>[ x ] Option to use simple v$session query to avoid perf issues
<br>[ x ] Fixed bug that made CPU time and executions sometimes be displayed as a negative number due to statistics resetting / SQLAREA flushing or plans changing
<br>[ x ] Direct link to DB management page from perf summary if ROLE_ADMIN
<br>[ x ] Direct link to perf report from DB management page
<br>[ x ] Fixed 12c privilege issue with sys.user$
<br>[ x ] Fetch explain plan from currently connected node (No support for RAC easy to implement)
<br>[ x ] Add top 10 SQL by hour in separate page
<br>[ x ] Add top 10 Sysevents by hour in separate page
<br>[ x ] Introduced pull of V$SYS_EVENT for overall event statistics to database repository
<br>[ x ] Add email to users and email plugin
<br>[ x ] Add login-URL to settings to include in invite-email
<br>[ x ] Option to disable mail
<br>[ x ] Allow user to control wether or not users should be emailed when creating user
<br>[ x ] Improved navigation between reports
<br>[ x ] Also retrieve entire SQL when running explain (fetch from opdb)
<br>[ x ] Fetch DB version from DB and place on main page
<br>[ x ] Verify that dictionary read account has appropriate system privilege

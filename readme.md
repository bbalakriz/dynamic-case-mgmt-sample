Users:  biz02 to use kie-server APIs
	biz01 to access tasks

Case Start
============

bala-case-proj_1.0.0-SNAPSHOT
bala-case-proj.fraud-mgmt

{
  "case-data" : {
    "request" : "Assess the risk associated with the fraud occurred using the card 0934 3349 3440 XXXX"
  },
  "case-user-assignments" : {
  },
  "case-group-assignments" : { "riskManager" : "IT", "cardBlocker" : "IT"},
  "case-data-restrictions" : { }
}

Dynamically any milestone be activated depending upon the external event.

Update case data
==================

bala-case-proj_1.0.0-SNAPSHOT
FRAUD--0000000001

newIssueRequired
complianceCheckComplete

true

Case can be closed at any point in time

Case close
===========

bala-case-proj_1.0.0-SNAPSHOT
FRAUD--0000000001
""


Case re-open
===============

bala-case-proj_1.0.0-SNAPSHOT
bala-case-proj.fraud-mgmt
FRAUD--0000000001

{
    "request" : "Please reassess the case. Customer reported a problem.."
}


Complete approve task
=======================
bala-case-proj_1.0.0-SNAPSHOT
23
true
{
    "isHighRisk": true
}


{
    "additionalInfo": "added additional details"
}


Dynamic task creation
=======================

bala-case-proj_1.0.0-SNAPSHOT
FRAUD--0000000001

{
 "name" : "Courtesy Call",
 "data" : {
   "reason" : "Just to follow up on the fraud"
  },
 "subject" : "Dynamic user task",
 "actors" : "",
 "groups" : "IT"
}


Cases with Stage
=================
bala-case-proj_1.0.0-SNAPSHOT
bala-case-proj.stages

{
  "case-data" : {
    "start" : true
  },
  "case-user-assignments" : {
  },
  "case-group-assignments" : { "testGroup" : "IT"},
  "case-data-restrictions" : { }
}


Start stage 2 using data id
============================
bala-case-proj_1.0.0-SNAPSHOT
STAGE--0000000001

caseFile_stage2

true


Start a task inside stage 2
==============================
bala-case-proj_1.0.0-SNAPSHOT
STAGE--0000000001
Stage 2
Task 2
{}


******************************************************************************************************************************
******************************************************************************************************************************
******************************************************************************************************************************

Case Start
============

bala-case-proj_1.0.0-SNAPSHOT
bala-case-proj.simple-case

{
  "case-data" : {
    "request" : "WFH: New desk request. Please approve."
  },
  "case-user-assignments" : {
  },
  "case-group-assignments" : { "approver" : "IT"},
  "case-data-restrictions" : { }
}

Update case data
==================

bala-case-proj_1.0.0-SNAPSHOT
BALA-0000000005

needMoreInfo
notificationComplete
true

Case close
===========

bala-case-proj_1.0.0-SNAPSHOT
BALA-0000000001
""


Case re-open
===============

bala-case-proj_1.0.0-SNAPSHOT
bala-case-proj.simple-case
BALA-0000000001

{
  "case-data" : {
    "request" : "Checking to see if this gets updated."
  },
  "case-user-assignments" : {

  },
  "case-group-assignments" : {"approver": "IT" },
  "case-data-restrictions" : { }
}


Complete approve task
=======================
bala-case-proj_1.0.0-SNAPSHOT
23
true
{
    "approved_": true
}


{
    "additionalInfo": "added a pic of my current work desk"
}


Dynamic task creation
=======================

bala-case-proj_1.0.0-SNAPSHOT
CASE-0000000003

{
 "name" : "testDynamicTask",
 "data" : {
   "reason" : "Fixed spec"
  },
 "subject" : "Test for dynamic user task",
 "actors" : "",
 "groups" : "testGroup"
}

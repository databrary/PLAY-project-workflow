User story development
================
Rick O. Gilmore & David Millman
2017-08-31 16:05:36

-   [Background](#background)
-   [Workflow](#workflow)
    -   [File name conventions](#file-name-conventions)
    -   [Play Staff create volumes for Data Collector labs](#play-staff-create-volumes-for-data-collector-labs)
    -   [Data Collector collects video and other data](#data-collector-collects-video-and-other-data)
    -   [Data Collector uploads video and data to Databrary](#data-collector-uploads-video-and-data-to-databrary)
    -   [QA Manager conducts QA](#qa-manager-conducts-qa)
        -   [Play Staff decide whether or not QA failures go into PLAY Additional Data Superset](#play-staff-decide-whether-or-not-qa-failures-go-into-play-additional-data-superset)
        -   [Coding Manager assigns videos that pass QA for coding & transcription](#coding-manager-assigns-videos-that-pass-qa-for-coding-transcription)
    -   [Data Coders transcribe or code videos](#data-coders-transcribe-or-code-videos)
    -   [Data Coders upload transcriptions and/or coding files to Databrary](#data-coders-upload-transcriptions-andor-coding-files-to-databrary)
    -   [PLAY Staff check transcription and coding files for reliability](#play-staff-check-transcription-and-coding-files-for-reliability)
    -   [PLAY Staff add transcription and coding files that pass reliability check to PLAY Superset](#play-staff-add-transcription-and-coding-files-that-pass-reliability-check-to-play-superset)
    -   [PLAY PIs share PLAY Superset and Additional Data Superset with all PLAY AIs](#play-pis-share-play-superset-and-additional-data-superset-with-all-play-ais)
    -   [PLAY PIs share PLAY volume with all Databrary AIs](#play-pis-share-play-volume-with-all-databrary-ais)

Background
==========

See [PLAY-planning](PLAY-planning.md).

Workflow
========

File name conventions
---------------------

-   As super user, I can create and enforce a file naming standard that will apply across all PLAY Project files, videos, survey data, audio recordings, and Datavyu files. For example <site-id-number>*<participant-id-number>*<data_type>.{.mp4, .csv, opf, ...}. The mapping between the <site-id-numbers> and the AI's lab is not disclosed.
-   As super user, I can use the <site-id-number> to assign components to a PLAY AI's Queue. As an implementation idea, we could use existing Party IDs.

Play Staff create volumes for Data Collector labs
-------------------------------------------------

-   As super user, I can create volumes for PLAY data collection sites that will become part of the PLAY collection. These volumes will have standard volume metadata across the 30 sites (e.g. same thumbnail icon, funding). They will PLAY PIs as owners. (Maybe implemented like this: As super user, I can create volumes for PLAY data collection based on a list of users. The list could be a CSV with user ID/email accounts.)
-   As a super user I can assign ownership of a PLAY volume to the Data Collector.
-   As a Data Collector, I can create Databrary Affiliates from my Research Assistants who have read/write privileges on the PLAY Volume assigned to me, but I may not share the PLAY Volume with anyone who is not my affiliate until the end of the PLAY Project.
-   As PLAY staff I can notify the Data Collector PI that a volume has been assigned to them, what privileges they have, and how they can further delegate authority to contribute to the volume.

Data Collector collects video and other data
--------------------------------------------

-   No new features required.

Data Collector uploads video and data to Databrary
--------------------------------------------------

-   As Data Collector, I want to be able to alert PLAY QA staff that a new session has been uploaded and is ready for QA Manager Queue.

QA Manager conducts QA
----------------------

-   As QA Manager, I want to notify the Data Collector when a video passes QA. If a video does *not* pass QA, I want to be able to notify the Data Collector why it did not pass. (Implementation could be via email.)

### Play Staff decide whether or not QA failures go into PLAY Additional Data Superset

-   As QA Manager, I want to assign videos that do not pass QA but which are still usable to the PLAY Additional Data Superset.

### Coding Manager assigns videos that pass QA for coding & transcription

-   As super user I want to select sessions from different Data Collector volumes and put them in a Data Coder's Queue. The sessions I select must have some way to indicate to the Data Coder what coding pass should be applied (e.g., language, physical activity, object, emotion). The Data Coder co-owns (with PLAY Staff) the sessions assigned for coding.
-   As Data Coder, I have access to the videos assigned to me in my Queue but no other data or metadata about the session the video is part of.
-   As Coding Manager, I can notify a Data Coder when a video has been added to the Data Coder's Queue. The notification includes information about which coding pass should be applied and where to access the video(s). This could be implemented in email.

Data Coders transcribe or code videos
-------------------------------------

-   No new Databrary features required.

Data Coders upload transcriptions and/or coding files to Databrary
------------------------------------------------------------------

-   As Data Coder, I want to upload the Datavyu file from my coding pass to the Coding Manager's Queue.
-   As Coding Manager, I want to receive a notification when a coding pass has been uploaded to the Coding Queue.

PLAY Staff check transcription and coding files for reliability
---------------------------------------------------------------

-   No new Databrary features required.

PLAY Staff add transcription and coding files that pass reliability check to PLAY Superset
------------------------------------------------------------------------------------------

-   As the Coding Manager, I can create a group of sessions that contains videos + coding spreadsheets that have passed QA and reliability checks. (This collection will be the primary way to access/view the project’s shared data.)

PLAY PIs share PLAY Superset and Additional Data Superset with all PLAY AIs
---------------------------------------------------------------------------

-   As PI, I can add other PLAY AIs as Collaborators on the PLAY Superset and Additional Data Superset.

PLAY PIs share PLAY volume with all Databrary AIs
-------------------------------------------------

-   As PI, I can change the sharing level on the PLAY Superset and Additional Data Superset to Shared. This behavior is similar to that with Volumes.

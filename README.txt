YouTube Provider 0.1
----------------------

Summary
-------
YouTube Provider is an implementation of the Providers module. It takes a YouTube
user's username, makes an API call to get that user's uploads, and creates nodes
for each uploaded video returned from the API call.

Installation
------------
1) Download and enable the Providers module[2].

2) Enable this module.

3) Extract youtube_video_content_type.rar into your modules directory and enable it.


Usage
-----
1) Navigate to Structure > Providers (/admin/structure/providers/)

2) Click 'add' in the YouTube Provider row

3) Create the new provider.
   a) Title        - The title of the provider.
   b) Username     - The username of the YouTube user whose uploads you want to import.
   c) Max Results  - The maximum number of items to return with each API call[3].
   d) Start Index  - The position in the user's upload history to begin importing items[4].
   e) Content Type - The content type to use when creating nodes. Select 'YouTube Video',
                     which is the content type created in step 3 of installation.
   f) Node Author  - The user who will be shown as the node author.
  
4) Click 'Save'. This will save the provider and redirect you to that provider's page (/provider/pid)

5) You can click the 'Update' tab to import new items. A success message will display how
   many videos were creates and updated. Updates will also run with cron, and messages will
   be stored in the watchdog table.


Authors
-------
jtrost


Footnotes
---------
[1] https://developers.google.com/youtube/2.0/developers_guide_protocol_video_feeds#User_Uploaded_Videos
[2] https://drupal.org/sandbox/jtrost/2049659
[3] https://developers.google.com/youtube/2.0/reference?csw=1#max-resultssp
[4] https://developers.google.com/youtube/2.0/reference?csw=1#start-indexsp
A simple tool to transcode recorded Zoom sessions.

Transcoding Zoom recordings to mpeg can be a heafty effort
for a laptop and will definitly make some fan noise.

To use the zoom transcoding job after a recorded zoom session 
you can follow these steps:
1. stop the post meeting trancoding on your laptop by killing the transcoding window that pops up after your meeting ends..
2. then use globus to transfer your zoom directory for the meeting (~/Documents/Zoom/date-channel) to your cluster zoomerang directory
3. once globus is complete...
4. on the cluster `cd zoomerang/<mtg dir>; sbatch ../zoomerang`
5. wait for the job complete.
6. rclone it up to online storage and send people the link.

Note: the vnc wrapper script doesn't work well with single quotes in file names.
Unfortunately "...User's..." is the default naming covention used by zoom.
Rename these dirs before you try to transcode them (or fix the script ;).

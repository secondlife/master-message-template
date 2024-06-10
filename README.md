#Second Life Master Message Template#
The Second Life (SL) "master message template" is the official public description all of the UDP messages the SL service uses to communicate between participants: client and servers.
Malformed or unexpected messages that do not agree with the message template used by the SL servers will be dropped, and may cause an active SL session connection to be terminated.

When building the SL client from scratch there is a step where the local `message_template.msg` may be compared to this "master message template" and analyzed for compatibility with the SL service.
This online compile-time check only happens if `message_template.msg` has a different SHA1 sum than what is stored in the local `message_template.msg.sha1` file.
Some differences between local and master message template are allowed, however any local message config that is is incompatible with the master message template's version will cause the build to fail.

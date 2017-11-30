# tripleo-rsyslog-ansible
An Ansible role for setting up an OpenStack cloud with Rsyslog based logging
designed to be used with a containerized TripleO deployment.

I'm not well versed in how the THT work so bear with me on the brainstorm here
pull requests welcome of course.

Some heat template calls this playbook, this playbook runs against various overcloud
nodes and depending on the settings copies over all the rsyslog template files. Then
later on a rsyslog container is spun up that is poitned at these on disk config files
and log collection begins.

My big concern is over legacy log files, if we do find them should we add them? should
we not even look for them and have this be journald driven no matter what? Other than
that some help setting up tht to call this is all that's needed to get itr ready.

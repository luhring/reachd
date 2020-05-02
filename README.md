# reachd

A daemon that assists with Reach analyses by running directly on compute nodes

## Operation

`reachd` is intended to run as a system daemon, starting at boot via the operating system's init system. reachd's function is to wait for jobs to be available and then to perform jobs.

The primary kind of job is conducting a reachability test.

### Reachability Tests

Just like with `reach`, reachd focuses on two subjects: the source and the destination. And again, the objective is to determine what traffic can originate at the source and reach the destination. What's unique to reachd is the fact that the analysis can now operate at the compute layer, verifying that — regardless of any configuration — traffic has actually been able to flow from the source to the destination compute node. This is made possible because reachd is actually a running process on the source and on the destination.

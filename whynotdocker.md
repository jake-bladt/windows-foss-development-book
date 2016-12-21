# Why not just docker?

Docker is an awesome tool. Containers are lightweight, relatively easily configured, etc. For running environments, I love docker.

Docker and the underlying technology LCX are built for portability and, as such, references to specific details of the host system are frowned upon.

(explain mounting host volumes on Docker)

On top of that, docker requires a linux host to run in. It doesn't even work natively on the Mac's POSIX-derived OS. That means that, in order to run docker, you first need to launch a VM and, in order to do that, you need a VM host (usually Oracle Virtual Box.) Running a development environment in Docker on Windows is not a lightweight process. It's running a container inside a VM, managed by a VM manager. And, it doesn't play nicely with changes made to local volumes after launch.

Since I already need OVB and a VM to host docker, I might as well drop docker out of the toolchain and use Vagrant (what Vagrant is.)

I'm not saying it's impossible to use docker to host your own development environment or that you shouldn't. I'm explaining why I generally don't.

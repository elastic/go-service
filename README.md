⚠️ We created this repository in June 2024 as a fork of https://github.com/kardianos/service because, at the time, we felt the project was not being maintained (the latest commit at the time was from February 2023 and our [question](https://github.com/kardianos/service/issues/396) about the project's status went unanswered for a couple of weeks. The project seems to be [active](https://github.com/kardianos/service/issues/395#issuecomment-2165690250) [again](https://github.com/kardianos/service/commit/4ac50d86f345e891c3616fc55c813d7ad587cd43) so we are archiving this fork.

# service [![GoDoc](https://godoc.org/github.com/kardianos/service?status.svg)](https://godoc.org/github.com/kardianos/service)

service will install / un-install, start / stop, and run a program as a service (daemon).
Currently supports Windows XP+, Linux/(systemd | Upstart | SysV), and OSX/Launchd.

Windows controls services by setting up callbacks that is non-trivial. This
is very different then other systems. This package provides the same API
despite the substantial differences.
It also can be used to detect how a program is called, from an interactive
terminal or from a service manager.

## BUGS
 * Dependencies field is not implemented for Linux systems and Launchd.
 * OS X when running as a UserService Interactive will not be accurate.

SMTP Router
====================

A lightweight SMTP server written in Go.

### What is SMTP Router?

It's an SMTP server written in Go. Server does flow as: 
- Receives mail traffic, 
- Read TO field, 
- By TO field it detects what oncall schedule to read (.csv file) 
- It reads the correspodning oncall schedule and detects oncall TO list for the moment, and forwared the email to that TO list.

its on prem, simple version of xMatters/PageDuty.

### Features

#### Main Features

- Config hot-reloading. Add/Remove/Enable/Disable servers without restarting. 
Reload TLS configuration, change most other settings on the fly.
- Be a gentleman to the garbage collector: resources are pooled & recycled where possible.
- Modern TLS support (STARTTLS or SMTPS).
- Dynamic file reload

#### Backend Features

- Arranged as workers running in parallel, using a producer/consumer type structure, 
 taking advantage of Go's channels and go-routines. 

#### Dependencies


Thanks to:
----------
* https://github.com/dvcrn
* https://github.com/athoune
* https://github.com/Xeoncross


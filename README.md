# Quander Rekeningoverzicht

[![GoDoc](https://godoc.org/github.com/middelink/rekeningoverzicht-qander?status.svg)](https://godoc.org/github.com/middelink/rekeningoverzicht-qander)
[![License](https://img.shields.io/github/license/middelink/rekeningoverzicht-qander.svg)](https://github.com/middelink/rekeningoverzicht-qander/blob/master/LICENSE)
[![Build Status](https://travis-ci.org/middelink/rekeningoverzicht-qander.svg?branch=master)](https://travis-ci.org/middelink/rekeningoverzicht-qander)
[![Coverage Status](https://coveralls.io/repos/github/middelink/rekeningoverzicht-qander/badge.svg?branch=master)](https://coveralls.io/github/middelink/rekeningoverzicht-qander?branch=master)
[![Go Report Card](https://goreportcard.com/badge/github.com/middelink/rekeningoverzicht-qander)](https://goreportcard.com/report/github.com/middelink/rekeningoverzicht-qander)

## TL;DR

* rekeningoverzicht-qander is a small program which logs into the
  Qander webUI and retrieves the last (or all) statements. It then
  creates an email with the statements attached.

## Command Line Flags

* `--all`
    	Download all statements (as opposed to the last)
*  `--days` int
    	How old can the statement be before we skip it (days)
*  `--pass` string
    	Qander password to log in with (required)
*  `--smtp` string
    	SMTPserver to send message over (e.g. smtp.iaf.nl:587) (required)
*  `--smtp_pass` string
    	Optional SMTP password to log in with
*  `--smtp_to` string
    	Comma seperated list of email recipients (required)
*  `--smtp_user` string
    	Optional SMTP username to log in with
*  `--user` string
    	Qander username to log in with (required)

## Installation

I presume you have a working experiance with go, a system with crontab
and in general some sys admin knowledge as I am not able to support you
with questions on every conveivable way to build, install and start this
program at regular monthly intervals.

### Building the binary

* Clone, download, copy/paste the source files onto your local disk.
* Execute `go build .` to create the rekeningoverzicht-qander binary.
* Copy the binary to /usr/local/sbin.

## Credits

Qander uses
[gomail.v2](https://gopkg.in/gomail.v2)

# LDAP Tool Box Self Service Password

[![CII Best Practices](https://bestpractices.coreinfrastructure.org/projects/372/badge)](https://bestpractices.coreinfrastructure.org/projects/372)
[![Build Status](https://travis-ci.org/ltb-project/self-service-password.svg?branch=master)](https://travis-ci.org/ltb-project/self-service-password)
[![Documentation Status](https://readthedocs.org/projects/self-service-password/badge/?version=latest)](https://self-service-password.readthedocs.io/en/latest/?badge=latest)

## Presentation

Self Service Password is a PHP application that allows users to change their password in an LDAP directory.

The application can be used on standard LDAPv3 directories (OpenLDAP, OpenDS, ApacheDS, Sun Oracle DSEE, Novell, etc.) and also on Active Directory.

![Screenshot](http://ltb-project.org/wiki/_media/documentation/self-service-password/1.0/ssp_1_0_change_password.png?w=800&h=666&tok=abc22c)

It has the following features:
* Samba mode to change Samba passwords
* Active directory mode
* Local password policy:
  * Minimum/maximum length
  * Forbidden characters
  * Upper, Lower, Digit or Special characters counters
  * Reuse old password check
  * Password same as login
  * Complexity (different class of characters)
* Help messages
* Reset by questions
* Reset by mail challenge (token sent by mail)
* Reset by SMS (trough external Email 2 SMS service or SMS API)
* Change SSH Key in LDAP directory
* Captcha (built-in)
* Mail notification after password change
* Hook script before and after password change

## Prerequisite

* PHP extensions required:
  * php-openssl (token crypt, probably built-in)
  * php-mbstring (reset mail)
  * php-curl (haveibeenpwned api)
  * php-ldap
  * php-filter
* strong cryptography functions available (for random_compat, php 7 or libsodium or /dev/urandom readable or php-mcrypt extension installed)
* valid PHP mail server configuration (reset mail)
* valid PHP session configuration (reset mail)

## Documentation

Documentation is available on https://self-service-password.readthedocs.io/en/latest/

## Download

Tarballs and packages for Debian and Red Hat are available on http://ltb-project.org/wiki/download#self_service_password

Debian and Red Hat repositories are also available, see [installation instructions](https://self-service-password.readthedocs.io/en/latest/installation.html).

## Source code

Source codes are available on https://github.com/ltb-project/self-service-password

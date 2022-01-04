* [x] Description of Organization
* [x] Reason for PSL Inclusion
* [x] DNS verification via dig
* [x] Run Syntax Checker (make test)

* [x] Each domain listed in the PRIVATE section has and shall maintain at least two years remaining on registration, and we shall keep the _PSL txt record in place


__Submitter affirms the following:__ 
  * [x] We are listing any third party limits that we seek to work around in our rationale such as those between IOS 14.5+ and Facebook (see [Issue #1245](https://github.com/publicsuffix/list/issues/1245) as a well-documented example)
  * [x] This request was _not_ submitted with the objective of working around other third party limits
  * [x] The [Guidelines](https://github.com/publicsuffix/list/wiki/Guidelines) were carefully _read_ and _understood_, and this request conforms
  * [x] The submission follows the [guidelines](https://github.com/publicsuffix/list/wiki/Format) on formatting

---
__For Private section requests that are submitting entries for domains that match their organization website's primary domain:__

``` 
Seriously, carefully read the downline flow of the PSL and the guidelines.
Your request could very likely alter the cookie and certificate (as well as other) behaviours on your 
core domain name in ways that could be problematic for your business.

Rollback is really not predicatable, as those who use or incorporate the PSL do what they do, and when.
It is not within the PSL volunteers' control to do anything about that.  

The volunteers are busy with new requests, and rollbacks are lowest priority, so if something gets broken 
it will stay that way for an indefinitely long while.
```
(Link: [about propogation/expectations](https://github.com/publicsuffix/list/wiki/Guidelines#appropriate-expectations-on-derivative-propagation-use-or-inclusion))

 * [x] Yes, I understand.  I could break my organization's website cookies etc. and the rollback timing, etc is acceptable.  Proceed.
---

Description of Organization
====

Organization Website: https://www.cu.tn

Software development self-hosted services that provide software development services. As part of the services we provide, we host source code, issues, and related project information in a self-hosted GitLab instance.

Reason for PSL Inclusion
====

We are using the domain cu.al and cu.tn exclusively to host websites via Gitlab Pages. They recommend adding the Gitlab Pages domain to the PSL, see https://docs.gitlab.com/ee/administration/pages/index.html#add-the-domain-to-the-public-suffix-list

Therefore we think it is prudent to list cu.al and cu.tn as a public suffix as each subdomain under it is used by a different entity or person. They should not set/see cookies for other entities / persons.

DNS Verification via dig
=======

```
dig +short TXT _psl.cu.tn
"https://github.com/publicsuffix/list/pull/1497"
```

```
dig +short TXT _psl.cu.al
"https://github.com/publicsuffix/list/pull/1497"
```

make test
https://gist.github.com/ducbo/df53d865e85eef077490f3f0ce23bb72

Related wontfix: #1419 https://github.com/publicsuffix/list/pull/1419

---
title: File and Process Contexts
description: Learn how SELinux labels files and processes
attribution_url: https://selinuxproject.org/page/BasicConcepts
next_tutorials: ['rules', 'temp_set_file_context']
---

Every process and object in the system has a context (also known as a label).
This is an attribute used to determine if an access should be allowed between
a process and an object. For example, a user process might have the context of
user_u:user_r:user_t, and file in the user's home directory might have the
context user_u:object_r:user_home_t. A SELinux context consists of three
required fields, and one optional field:

`user:role:type:range`

The first field is the SELinux user. The second field is the role. The third
field in the type. The forth field is the MLS range; this field is optional,
and will be discussed later. The following is an example context:

`system_u:system_r:xserver_t`

In this context, the user is system_u, the role is system_r, and the type is
xserver_t. The following is an example context, with the MLS field:

<p style="padding-top:30px">
  <h2>Tools</h2>
</p>

* The [`ps`](https://linux.die.net/man/1/ps) command, when used with the `-Z`
option will show process contexts.
* The [`ls`](https://linux.die.net/man/1/ls) command shows file contexts when
used with the `-Z` option.

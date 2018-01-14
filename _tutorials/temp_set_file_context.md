---
title: Changing a File Context
description: Learn how to change a file context
attribution_url: https://selinuxproject.org/page/Guide/Contexts
next_tutorials: ['perm_set_file_context']
---

Assuming you know the file context you want to specify, you can specify it
using the `chcon` command. The following example sets the file "/tmp/myfile"
to _user_home_t_.

```
$ touch /tmp/myfile
$ ls -Z /tmp/myfile
unconfined_u:object_r:user_tmp_t:s0 /tmp/myfile
$ chcon -t user_home_t /tmp/myfile
$ ls -Z /tmp/myfile
unconfined_u:object_r:user_home_t:s0 /tmp/myfile
```

<p style="padding-top:30px">
  <h2>Tools</h2>
</p>

* [`chcon`](https://linux.die.net/man/1/chcon) changes the file SELinux
security context.

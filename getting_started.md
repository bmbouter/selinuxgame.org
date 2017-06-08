---
layout: page
title: Getting Started
---

Getting started has two parts:

1. [Install Vagrant](https://www.vagrantup.com/downloads.html). To quote the
   Vagrant docs, "Installing Vagrant is extremely easy."

2. Download the SELinux Game Vagrant File which defines all of the Vagrant
   boxes.

{% highlight shell %}
    wget {{ site.baseurl }}{% link Vagrantfile %}
{% endhighlight %}

3. From the same Directory as `Vagrantfile`, run `vagrant up` which should
   display output like the following:

{% highlight shell %}
[user@localhost vagrant_test]$ vagrant status
Current machine states:

broken_antivirus          not created (libvirt)
fresh_pulp                not created (libvirt)
new_ways                  not created (libvirt)
stayin_alive              not created (libvirt)

This environment represents multiple VMs. The VMs are all listed
above with their current state. For more information about a specific
VM, run `vagrant status NAME`.

{% endhighlight %}

4.Play a [Scenario]({{ site.baseurl }}{% link scenarios.md %}).

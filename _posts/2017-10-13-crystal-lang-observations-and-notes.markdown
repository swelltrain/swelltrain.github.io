---
layout: post
title:  "Crystal Lang Random Observations"
date:   2017-10-13 06:37:22 -0700
---

### Better Spec Output For Git Commits
{% highlight ruby %}
  # in spec_helper.cr
  Spec.override_default_formatter(Spec::VerboseFormatter.new)
{% endhighlight %}

### Code Layout
{% highlight text %}
/module_name
  /src
    module_name.cr
    /module_name
      thing.cr
        #contains
          module ModuleName
            class Thing

  /spec
    thing_spec.cr
      #contains
        include ModuleName
{% endhighlight %}

---
title: 'Eco (Embedded Coffee Script) Error - Unexpected dedent'
author: admin
layout: post
permalink: /2012/01/29/eco-embedded-coffee-script-error-unexpected-dedent/
categories:
  - Javascript
---


Ran into this error when testing out eco (Embedded Coffee Script) templates.

Parse error on line #: unexpected dedent
(in C:/project/app/assets/javascripts/backbone/templates/dartboard.jst.eco)

Broken code:
{% codeblock lang:coffeescript %}
<% if 7 > 3 %>
  teststring
<% end %>
{% endcodeblock %}

Fixed Code:
{% codeblock lang:coffeescript %}
<% if 7 > 3: %>
  teststring
<% end %>
{% endcodeblock %}

Notice the **colon**, this is telling coffeescript that the next line is indented. It’s document here: [https://github.com/sstephenson/eco][1] it had just slipped my mind.

 [1]: https://github.com/sstephenson/eco "https://github.com/sstephenson/eco"

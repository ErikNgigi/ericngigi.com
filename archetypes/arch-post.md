---
title: "{{ replace .Name "-" " " | title }}"
summary: ""
date: {{ .Date }}
author: "Eric Ngigi"
image: ""
tags: ["Arch Linux", "Tutorial"]
categories: ["Linux"]
weight: {{ printf "%02d" (add (len (readDir "content/post/linux")) 1) }}
---

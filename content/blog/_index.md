---
title: "Blog"
date: 2022-06-11T17:17:38+02:00
author: Ondrej Markus
draft: false

slug: blog
description: "Explore articles about learning, games and design."
summary: "Explore articles about learning, games and design."

cover:
  image: ""
  alt: ""
  caption: ""
  relative: false
  responsiveImages: false

---

<ul class="terms-tags">
    {{- $type := .Type }}
    {{- range $key, $value := .Data.Terms.Alphabetical }}
    {{- $name := .Name }}
    {{- $count := .Count }}
    {{- with site.GetPage (printf "/%s/%s" $type $name) }}
    <li>
        <a href="{{ .Permalink }}">{{ .Name }} <sup><strong><sup>{{ $count }}</sup></strong></sup> </a>
    </li>
    {{- end }}
    {{- end }}
</ul>
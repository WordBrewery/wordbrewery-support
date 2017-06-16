+++
date = "2017-03-27T14:05:40-04:00"
title = "index"

+++

{{ partial "header.html" . }}
{{ partial "subheader.html" . }}

<section id="main">
  <div>
   <h1 id="title">{{ .Title }}</h1>
        <ul id="list">
            {{ range where .Data.Pages "Section" "subscriptions" }}
                {{ .Render "li"}}
            {{ end }}

        </ul>
  </div>
</section>

{{ partial "footer.html" . }}


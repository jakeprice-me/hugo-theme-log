# Tech Notes

## Summary

A flat directory of notes and knowledge on technical topics.

## Categories



## Notes

{{ range $name, $pages := .Site.Taxonomies.categories }}
### {{ $name }}
<ul>
  {{ range where $pages "Type" "in" "content/tech-notes/*" }}
    {{ $is_private := default .Params.private false }}
    {{ if not $is_private }}
<li>{{ .Title }}</li>
    {{ end }}
  {{ end }}
</ul>
{{ end }}



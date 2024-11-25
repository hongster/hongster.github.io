{{ $data := index .Site.Data.food (.Get 0) }}

{{ range $index, $shops := $data.food }}

# {{ $index }}

    {{ range $shops }}
**{{ .name }}**

        {{ range .addresses }}

- [{{ .address }}]({{ .link }})

        {{ end }}

    {{ end }}

---

{{ end }}
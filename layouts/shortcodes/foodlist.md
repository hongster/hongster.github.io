{{ $data := index .Site.Data.food (.Get 0) }}

{{ range $index, $shops := $data.food }}

# {{ $index }}

    {{ range $shops }}
**{{ .name }}**

Address: [{{ .address }}]({{ .link }})
    {{ end }}

{{ end }}
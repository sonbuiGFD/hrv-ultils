**include file hrv.search-form.min.js before close body tag**

```sh
{{ 'hrv.search-form.js' | asset_url | script_tag }}
```

**add custom tag for plugin**

```sh
<div data-search-form >
    <input class="form-control" search-form-input />
    <ul>
        {% for vendor in shop.vendors %}
            <li search-form-item data-key="{{ vendor }}">
               { vendor }}
            </li>
        {% endfor %}
    </ul>
</div>
```

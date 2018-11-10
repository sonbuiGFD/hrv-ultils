**include file hrv.search-form.min.js before close body tag**

```sh
{{ 'hrv.search-form.js' | asset_url | script_tag }}
```

**add custom tag for plugin**

```sh
<div data-search-form class="block_content">
    <input class="form-control" search-form-input />
    <ul>
        {% for vendor in shop.vendors %}
            <li  search-form-item data-key="{{ vendor }}">
                <input
                        id="filer-vendor-{{ forloop.index }}"
                        type="checkbox"
                        name="filer-vendor-{{ forloop.index }}"
                        value="(vendor:product**{{vendor}})"
                        filter-option
                        data-label="{{ vendor }}"
                        data-id="filer-vendor-{{ forloop.index }}"
                    >
                <label for="filer-vendor-{{ forloop.index }}">{{ vendor }}</label>
            </li>
        {% endfor %}
    </ul>
</div>
```

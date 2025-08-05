---
{"publish":true,"title":{"{ title }":null},"created":"2025-05-24T17:36:34.666+01:00","modified":"2025-07-07T16:21:14.406+01:00","published":"2025-07-07T16:21:14.406+01:00","cssclasses":""}
---

# {{title}}

>[!meta]- Abstract
{{abstractNote}}

> [!meta]- Metadata
> zotero_link:: {{pdfZoteroLink}}
> Authors:: {% for auth in authors.split(', ') -%} {%- if auth -%} [[people/{{auth}}\|{{auth}}]], {% endif -%} {%- endfor%}
> Related:: {% for relation in relations -%} {%- if relation.citekey -%} [[{{relation.title}}]], {% endif -%} {%- endfor%}
> url:: {{url}}
> doi:: {{doi}}
> bibliography:: {{bibliography}}

---
## My Notes
{% persist "notes" %}

model::
techniques::
problems::
lbs::

{% endpersist %}
---
{"publish":true,"title":{"{ title }":null},"created":"2025-05-24T17:36:34.685+01:00","modified":"2025-05-24T17:36:24.188+01:00","published":"2025-05-24T17:36:24.188+01:00","cssclasses":""}
---


>[!meta] Abstract
{{abstractNote}}

> [!meta] Metadata
> zotero_link:: {{pdfZoteroLink}}
> Authors:: {% for auth in authors.split(', ') -%} {%- if auth -%} [[people/{{auth}}\|{{auth}}]], {% endif -%} {%- endfor%}
> Related:: {% for relation in relations -%} {%- if relation.citekey -%} [[{{relation.title}}]], {% endif -%} {%- endfor%}
> url:: {{url}}
> doi:: {{doi}}
> bibliography:: {{bibliography}}


---
# Self Notes
{% persist "notes" %}


{% endpersist %}

# Reading notes

{% persist "annotations" %}

{%-  
set zoteroColors = {  
"#2ea8e5": "blue",  
"#5fb236": "green",  
"#a28ae5": "purple",  
"#ff6666": "red",  
"#ffd400": "yellow",  
"#f19837": "orange",  
"#aaaaaa": "grey",  
"#e56eee": "magenta"  
}  
-%}

{%-  
set colorHeading = {  
"blue": "Theorems and Corollaries",  
"green": "Lemmas",  
"purple": "Claims and Propositions",  
"red": "❓Open Problems",  
"yellow": "Upper and Lowerbounds",  
"orange": "Observations",  
"grey": "Definitions",  
"magenta": "📄 Important references"  
}  
-%}

{%- macro calloutHeader(type) -%}  
{%- switch type -%}  
{%- case "highlight" -%}  
Highlight  
{%- case "image" -%}  
Image  
{%- default -%}  
Note  
{%- endswitch -%}  
{%- endmacro %}

{%- set newAnnot = [] -%}  
{%- set newAnnotations = [] -%}  
{%- set annotations = annotations | filterby("date", "dateafter", lastImportDate) %}

{% if annotations.length > 0 %}  
_Imported: {{importDate | format("YYYY-MM-DD HH:mm")}}_


{%- for annot in annotations -%}


{%- if annot.color in zoteroColors -%}
    {%- set customColor = zoteroColors[annot.color] -%}
{%- elif annot.colorCategory|lower in colorHeading -%}
	{%- set customColor = annot.colorCategory|lower -%}
{%- else -%}
    {%- set customColor = "other" -%}
{%- endif -%}

{%- set newAnnotations = (newAnnotations.push({"annotation": annot, "customColor": customColor}), newAnnotations) -%}


{%- endfor -%}

{#- INSERT ANNOTATIONS -#}  
{#- Loops through each of the available colors and only inserts matching annotations -#}  
{#- This is a workaround for inserting categories in a predefined order (instead of using groupby & the order in which they appear in the PDF) -#}

{%- for color, heading in colorHeading -%}  
{%- for entry in newAnnotations | filterby ("customColor", "startswith", color) -%}  
{%- set annot = entry.annotation -%}

{%- if entry and loop.first %}

### {{colorHeading[color]}}

{%- endif %}

{{calloutHeader(annot.type)}} ([page.{{annot.pageLabel}}](zotero://open-pdf/library/items/%7B%7Bannot.attachment.itemKey%7D%7D?page=%7B%7Bannot.pageLabel%7D%7D&annotation=%7B%7Bannot.id%7D%7D))

{%- if annot.annotatedText %}

> {{annot.annotatedText|nl2br}} {% if annot.hashTags %}{{annot.hashTags}}{% endif -%}  
> {%- endif %}

{%- if annot.imageRelativePath %}

> “” could not be found.  
> {%- endif %}

{%- if annot.ocrText %}

> {{annot.ocrText}}  
> {%- endif %}

{%- if annot.comment %}

> - **{{annot.comment|nl2br}}**  
>     {%- endif -%}

{%- endfor -%}  
{%- endfor -%}  
{% endif %}  
{% endpersist %}
---
layout: page
title: Techniques
permalink: /techniques/
---

{% include search_type.html %}

<table>
    <colgroup>
        <col width="5%" />
        <col width="5%" />
        <col width="10%" />
        <col width="80%" />
    </colgroup>
    <thead>
        <tr>
            <th>Name</th>
            <th>Id</th>
            <th>Theme</th>
            <th>Description</th>
        </tr>
    </thead>
    <tbody id="myTable">
        {%- for post in site.categories.techniques %}
        {%- if post.enabled == true %}
        <tr>
        {% assign tmp = threat_actor[1] -%}
            <td markdown="span"><a href="{{ site.url }}{{ site.baseurl }}/{{ post.permalink }}">{{ post.title }}</a></td>
            <td markdown="span">{{ post.Id }}</td>
            <td markdown="span">{{ post.theme }}</td>
            <td markdown="span">{{ post.description }}</td>
        </tr>
        {%- endif -%}
        {% endfor %}
    </tbody>
</table>
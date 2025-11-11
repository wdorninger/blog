---
title: "Fuzzy Matching"
layout: single
tags: [tech, fuzzy]
categories: [finance]
author_profile: true
---

# Postgres
The below shows how fuzzy matching can be done in Postgres using the pg_trgm extension. The example query finds all legal entity names similar to "GOLDEN".

{% highlight sql %}
CREATE EXTENSION IF NOT EXISTS pg_trgm;

SELECT *
  FROM lei_reference_data
 WHERE e_legalname <% 'GOLDEN';
{% endhighlight %}

![2025-11-12-fuzzy-matching-query1.png](../assets/images/2025-11-12-fuzzy-matching-query1.png)

The above is good however if one looks at the explain plan one sees that it performs a full table scan. To improve performance one can create a trigram 
index on the column being searched. The index will speed up similarity operations like <% and functions like similarity()

{% highlight sql %}
CREATE INDEX lei_reference_data_i003 ON lei_reference_data USING gin (e_legalname gin_trgm_ops);
{% endhighlight %}


Show the similarity score for each match:

{% highlight sql %}
SELECT similarity(e_legalname, 'GOLDENSOURCE'), *
  FROM lei_reference_data
 WHERE e_legalname <% 'GOLDENSOURCE'
 ORDER BY similarity(e_legalname, 'GOLDENSOURCE') desc
{% endhighlight %}

![2025-11-12-fuzzy-matching-query2.png](../assets/images/2025-11-12-fuzzy-matching-query2.png)



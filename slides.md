---
# You can also start simply with 'default'
theme: seriph
# random image from a curated Unsplash collection by Anthony
# like them? see https://unsplash.com/collections/94734566/slidev
background: https://cover.sli.dev
# some information about your slides (markdown enabled)
title: Faster, Better, Stronger JPA
info: |
  ## Slidev Starter Template
  Presentation slides for developers.

  Learn more at [Sli.dev](https://sli.dev)
# apply unocss classes to the current slide
class: text-center
# https://sli.dev/features/drawing
drawings:
  persist: false
# slide transition: https://sli.dev/guide/animations.html#slide-transitions
transition: slide-left
# enable MDC Syntax: https://sli.dev/features/mdc
mdc: true
---

# Faster, Better, Stronger JPA

Make your persistence layer faster

<div class="pt-12">
  <span @click="$slidev.nav.next" class="px-2 py-1 rounded cursor-pointer" hover="bg-white bg-opacity-10">
    Press Space for next page <carbon:arrow-right class="inline"/>
  </span>
</div>


<!--
The last comment block of each slide will be treated as slide notes. It will be visible and editable in Presenter Mode along with the slide. [Read more in the docs](https://sli.dev/guide/syntax.html#notes)
-->

---
transition: fade-out
---

# Who am i?

Java Developer

- **Experience** - 15 years Java, Spring, JPA, Hibernate, Apache Wicket, JavaScript, Vue.js, ...
- **LinkedIn** - https://www.linkedin.com/in/robert-niestroj/
- **Stackoverflow** - https://stackoverflow.com/users/534877/robert-niestroj
- **X/Twitter** - https://x.com/NiestrojRobert

--- 
layout: quote
---
# Performance problem with Databases in one sentence


"Too much data is being fetched 
 or 
same data is being fetched too many times"

_Someone on Twitter_

---

# Logging

How to know what is going on?

<v-clicks>

`spring.jpa.show-sql=true`

`spring.jpa.properties.hibernate.format_sql=true`

`spring.jpa.properties.hibernate.highlight_sql=true`

`spring.jpa.properties.hibernate.use_sql_comments=true`

`@Meta` - https://docs.spring.io/spring-data/data-jpa/docs/3.3.0/api/org/springframework/data/jpa/repository/Meta.html

`spring.jpa.properties.hibernate.generate_statistics=true`

`spring.jpa.properties.hibernate.session.events.log.LOG_QUERIES_SLOWER_THAN_MS=20`

</v-clicks>

---

# Logging

Visual VM JDBC Profiling



--- 

# Projections

How to fetch less data

 - DTO Projections
 - Interface Based Projections

--- 

# Modifying Queries

But i need to modify my data!

@Modifying

---

# Derived delete Queries

It's just a delete

https://docs.spring.io/spring-data/jpa/reference/jpa/query-methods.html#jpa.modifying-queries.derived-delete


--- 

# @DynamicUpdate

@DynamicUpdate

---

# References

Can we save that one query too?

getOne()



---

# @OneToMany

Think twice

How many?

--- 

# Dynamic Queries

It's not always easy

Search form

---

# N+1 problem

You are gonna do what?

Fetch parent and each child

---

# N+1 problem

Join fetch and entity graph

Rescue


--- 
layout: end
---

# Q&A

Questions and Answers
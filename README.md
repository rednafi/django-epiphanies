<div align="center">

![img](./art/logo.png)
<strong>>> <i>Lessons, musings, and resources on web development with Django</i> <<</strong>

&nbsp;

</div>

## Architecture

* [Django for Startup Founders: A Better Software Architecture for SAAS Startups & Consumer Apps](https://alexkrupp.typepad.com/sensemaking/2021/06/django-for-startup-founders-a-better-software-architecture-for-saas-startups-and-consumer-apps.html) -> An opinionated guideline to structuring Django applications for maximum efficiency.

* [Django Structure for Scale & Longevitiy](https://www.youtube.com/watch?v=yG3ZdxBb1oo) -> Designing **thin** Model driven applications around **selectors** and **services**.

* [Fat Models are Considered Harmful](https://news.ycombinator.com/item?id=23322880) -> A hackernews discussion on why **Fat Models** recommendation is one of the most destructive architecture patterns.

* [Spontaneous Transition from Monolithic to Microservice Oriented Architecture](https://doordash.engineering/2020/12/02/how-doordash-transitioned-from-a-monolith-to-microservices/) -> Microservices are cute when you get to build them from scratch. However, often it becomes a necessity to break down a gargantuan monolith into mutliple service-oriented entities to keep up with the business requirements. This article contains wisdoms on how Doordash attempted that back in Q4 2019.

## Performance Optimizations

* [Django Database Optimization Tips](https://betterprogramming.pub/django-database-optimization-tips-4e11631dbc2c) -> A few common DB optimizations with examples.

* [Mitigating (n+1) Query Issues with select_related() & prefetch_related()](https://docs.djangoproject.com/en/dev/ref/models/querysets/#prefetch-related) -> I find that the Django documentation does a better job at explaining the role of `select_related` and `prefetch_related` methods for query optimizations than most other resources. Check out the section where the doc explains how to use `Prefetch` object to further control the prefetch operation. It's crazy powerful.

* Django [Select Related](https://www.youtube.com/watch?v=mO-pfdJpnBA) & [Prefetch Related](https://www.youtube.com/watch?v=5-UN4YPDDQc) Examples -> Two YouTube videos that I found useful to understand select and prefetch related methods. However, first, you should definitely go through the documentation listed above. It's awesome.

* [PostgreSQL Indexing : How, Why, and When - Curtis Maloney](https://www.youtube.com/watch?v=clrtT_4WBAw) -> Here, the speaker adds indexes on a simple PostgreSQL table incrementally and runs `Explain` on different queriers to showcase the performance improvements.

* [Unlocking the full potential of PostgreSQL indexes in Django - Haki Benita](https://www.youtube.com/watch?v=BhxCYK6TCwo) -> While, the loop of adding the default B-Tree index to the target columns and running `Explain` on the query works well enough, the latest version of Django opens up the opportunities of leveraging more esoteric indexes offered by PostgreSQL. Apart from **B-Tree Index**, the presenter also explores **Inclusive Index**, **Partial Index**, **Function Based Index**, **Hash Index**, and Block Range Index aka **BRIN**.

* [Re-Introducing Hash Indexes in PostgreSQL - Haki Benita](https://hakibenita.com/postgresql-hash-index#conclusion) -> Prior to PostgreSQL 10, **Hash** indexes were extremely limited compared to the default B-Tree indexes and offered too little to be considered as a viable alternative. However, a few things has changed since then and this post stacks Hash indexes against B-Tree.

* [Hunting Performance in Django Code - Sümer Cip](https://www.youtube.com/watch?v=ZBJ30MAlc_0) -> This talk offers a great starting point for learning about
performance profilers for your Python application. It primarily talks about the distinctions between different **tracing** and **sampling** profilers.
## Misc

* [Customize the Django Admin With Python](https://realpython.com/customize-django-admin-python/) -> Quick customization of Django Admin using only Python.

* [How to Add a Text Filter to Django Admin](https://hakibenita.com/how-to-add-a-text-filter-to-django-admin) -> Django's admin panel is a great way to quickly build admin specific CRUD pages. However, one caveat is that the built-in search doesn't scale very well. This post shows a way to extend the built-in filters to achieve auto-complete-like features in the pages containing object tables.

* [Django Transactions: Past, Present, and Future - Christophe Pettus](https://www.youtube.com/watch?v=ppwT0u98TmQ) -> An overiew of the evolution and the quirks of Django transactions in PostgreSQL context.

## Django Rest FrameWork

* [DRF Serializer Relations](https://www.django-rest-framework.org/api-guide/relations/) -> DRF serializer relations can be confusing at times. At my workplace, we were using `HyperlinkedModelSerializer` for everything and this would at times, lead to confusing errors. By default, when `ModelSerializer` is used to serialize a model, DRF uses `PrimaryKeyRelatedField` to resolve field relationships. However, it uses `HyperlinkedRelatedField` to resolve relationships if `HyperlinkedModelSerializer` is used instead.

## Tools & Projects

* [Django Template Delocalized](https://github.com/rednafi/django-template-delocalized) -> A comprehensive POC of decoupling template rendition to a separate Django application.

* [Hook Slinger](https://github.com/rednafi/hook-slinger) -> Webhook as a standalone service.

* [PyInstrument](https://github.com/joerick/pyinstrument) -> Call stack profiler for Python. Shows why your code is slow!

## Books

* [Architecture Patterns with Python - Harry Percival & Bob Gregory](https://www.goodreads.com/book/show/50083115-architecture-patterns-with-python) -> A deep dive into DDD and Event-driven architecture patterns in the Python ecosystem. The book also talks about strategies to exercise DDD and event-driven architecture practices within the realm of a highly opinionated environment like Django.

* [Django for Beginners - William Vincent](https://djangoforbeginners.com/) -> An excellent guide to dipping your toes into the Django ecosystem.

* [Django for Professionals - William Vincent](https://djangoforprofessionals.com/) -> A comprehensive guide to productionizing your first Django application.

* [Django for APIs - William Vincent](https://djangoforapis.com/) -> A practitioner's guide to building REST APIs with Django Rest Framework. This book assumes previous exposure to Django.

<div align="center">
<i> ✨ 🍰 ✨ </i>
</div>

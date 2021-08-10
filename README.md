<div align="center">

![img](./art/logo.png)
<strong>>> <i>Lessons, musings, and resources on web development with Django</i> <<</strong>

&nbsp;

</div>

## Architecture

* [Django for Startup Founders: A Better Software Architecture for SAAS Startups & Consumer Apps](https://alexkrupp.typepad.com/sensemaking/2021/06/django-for-startup-founders-a-better-software-architecture-for-saas-startups-and-consumer-apps.html) -> An opinionated guideline to structuring Django applications for maximum efficiency.

* [Django Structure for Scale & Longevitiy](https://www.youtube.com/watch?v=yG3ZdxBb1oo) -> Designing **thin** Model driven applications around **selectors** and **services**.

* [Fat Models are Considered Harmful](https://news.ycombinator.com/item?id=23322880) -> A hackernews discussion on why **Fat Models** recommendation is one of the most destructive architecture patterns.

## Performance Optimizations

* [Django Database Optimization Tips](https://betterprogramming.pub/django-database-optimization-tips-4e11631dbc2c) -> A few common DB optimizations with examples.

* [Mitigating (n+1) Query Issues with select_related() & prefetch_related()](https://docs.djangoproject.com/en/dev/ref/models/querysets/#prefetch-related) -> I find that the Django documentation does a better job at explaining the role of `select_related` and `prefetch_related` methods for query optimizations than most other resources. Check out the section where the doc explains how to use `Prefetch` object to further control the prefetch operation. It's crazy powerful.

* Django [Select Related](https://www.youtube.com/watch?v=mO-pfdJpnBA) & [Prefetch Related](https://www.youtube.com/watch?v=5-UN4YPDDQc) Examples -> Two YouTube videos that I found useful to understand select and prefetch related methods. However, first, you should definitely go through the documentation listed above. It's awesome.


## Misc

* [How to Add a Text Filter to Django Admin](https://hakibenita.com/how-to-add-a-text-filter-to-django-admin) -> Django's admin panel is a great way to quickly build admin specific CRUD pages. However, one caveat is that the built-in search doesn't scale very well. This post shows a way to extend the built-in filters to achieve auto-complete-like features in the pages containing object tables.

## Django Rest FrameWork

* [DRF Serializer Relations](https://www.django-rest-framework.org/api-guide/relations/) -> DRF serializer relations can be confusing at times. At my workplace, we were using `HyperlinkedModelSerializer` for everything and this would at times, lead to confusing errors. By default, when `ModelSerializer` is used to serialize a model, DRF uses `PrimaryKeyRelatedField` to resolve field relationships. However, it uses `HyperlinkedRelatedField` to resolve relationships if `HyperlinkedModelSerializer` is used instead.

## Projects

* [Django Template Delocalized](https://github.com/rednafi/django-template-delocalized) -> A comprehensive POC of decoupling template rendition to a separate Django application.

* [Hook Slinger](https://github.com/rednafi/hook-slinger) -> Webhook as a standalone service.

## Books

* [Architecture Patterns with Python - Harry Percival & Bob Gregory](https://www.goodreads.com/book/show/50083115-architecture-patterns-with-python) -> A deep dive into DDD and Event-driven architecture patterns in the Python ecosystem. The book also talks about strategies to exercise DDD and event-driven architecture practices within the realm of a highly opinionated environment like Django.

* [Django for Beginners - William Vincent](https://djangoforbeginners.com/) -> An excellent guide to dipping your toes into the Django ecosystem.

* [Django for Professionals - William Vincent](https://djangoforprofessionals.com/) -> A comprehensive guide to productionizing your first Django application.

* [Django for APIs - William Vincent](https://djangoforapis.com/) -> A practitioner's guide to building REST APIs with Django Rest Framework. This book assumes previous exposure to Django.

<div align="center">
<i> ✨ 🍰 ✨ </i>
</div>

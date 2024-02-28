---
title: hot django questions
---

## What are the different model inheritance styles in Django?

In Django, there are three types of inheritance.

Abstract base classes - When the parent class contains common fields and the parent class table is undesirable, use this.

Multi-table inheritance - When the parent class has common fields, but the parent class table already exists in the database on its own, use this.

Proxy models - Use this when you want to change the parent class's behavior, for as by modifying the order or adding a new model manager.

After going through some of the basic Django interview questions and answers, it is time we increase the difficulty level with the intermediate Django interview questions and answers.

## What's the use of a session framework?

The session structure enables per-site-visitor storage and retrieval of any type of data. It abstracts the sending and receiving of cookies and keeps data on the server side.

## List several caching strategies supported by Django

Django supports these caching strategies:

Database caching
In-memory caching
File System Caching
Memcached

## What do you use django.test.Client class for?

The Client class acts like a dummy web browser, enabling users to test views and interact with Django-powered applications programmatically. This is especially useful when performing integration testing.

## What is mixin?

In Django, a mixin is a Python class that is inherited by another class to carry out extra functions. Classes that can be reused and scaled are mixins. A unique form of multiple inheritances is a mixin. Mixins are typically employed in two contexts:

You wish to give a class several optional features.
You wish to apply a specific feature to numerous classes.

## How to combine multiple QuerySets in a View?

QuerySets can be combined into another QuerySet, and they do not have to be from the same model.

To merge QuerySets from the same model, use the Python union operator.

The union operator can be used to combine two or more QuerySets with the following syntax:

model_combination = model_set1 | model_set2 | model_set3

Additionally, you can concatenate two or more QuerySets from other models by using the chain() method from the Itertools package.

from itertools import chain

model_combination = list(chain(model_set1, model_set2))

As an alternative, you can merge two or more QuerySets from other models using union(), passing all=TRUE to allow for duplication.

model_combination = model_set1.union(model_set2, all=TRUE)  

## Mention the ways used for the customization of the functionality of the Django admin interface

Numerous customization options are available in the Django admin interface, and additional admin interfaces can even be created to enable user separation through permissions. The ModelAdmin class, which serves as a representation of a model in the administration interface, can be used to perform the majority of adjustments.

## Difference between select_related and prefetch_related?

Django's select-related and prefetch-related functions are intended to reduce the number of database queries that are generated when related objects are accessed.

When a query is executed, select related() "follows" foreign-key relationships and choose extra related-object data.

Prefetch related() performs the "joining" in Python by performing a separate lookup for each relationship.

When picking a single object, such as an OneToOneField or a ForeignKey, users utilize the select-related function. When retrieving a "set" of items, such as ManyToManyFields or reverse ForeignKeys, users utilize prefetch related.

## Explain Q objects in Django ORM

When writing complex queries, Q objects are employed because filter() functions only allow you to 'AND' the conditions; whereas, Q objects allow you to 'OR' the conditions.

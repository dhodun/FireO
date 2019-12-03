---
layout: default
title: Getting Data
parent: Querying Data
nav_order: 1
---

# Getting Data
{: .no_toc }

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

Read documents from Google's Firestore

## Single Document
Read single document from collection

### Example Usage
{: .no_toc }

```python
u = User.collection.get(user_key)

print(u.name)
print(u.key)
```

## Multiple documents
Read multiple documents by providing **key list**

```python
User.collection.get_all(key_list)
```

## All Documents
Read all documents from collection

### Example Usage
{: .no_toc }

```python
user_list = User.collection.fetch()

for user in user_list:
    print(user.id, user.name)
```

`fetch()` method return `generator`

## Sub Collection
Get child documents from collection

### Example Usage
{: .no_toc }

```python
users = User.collection.parent(parent_key).fetch()

for user in users:
    print(user.id, user.name)
```

## Get Rote collections
FireO allow you to get all root collections

```python
fireo.list_collections()
```

## Get Sub collections
You can get `subcollection` of any `document`

```python
post = Post.collection.get(post_key)
post.list_subcollections()
```
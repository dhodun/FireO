---
layout: default
title: Utils
nav_order: 7
---

# Utils
{: .no_toc }

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## Parent from key
Get parent collection path from `key`

```python
parent_collection = utils.get_parent(key)
```

## Parent doc from key
Get parent document path from `key`

```python
parent_doc = utils.get_parent_doc(key)
```

## Id from key
Get `id` from `key`

```python
id = utils.get_id(key)
```

## Key from id
Get `key` from `id` and `model`

```python
key = utils.generateKeyFromId(model, key)
```
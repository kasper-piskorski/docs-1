---
pageTitle: Concept API
keywords: grakn, concept, api
longTailKeywords: grakn concept api, concept api
Summary: Concept Hierarchy in Grakn.
toc: false
---

## Concept Architecture
Anything in Grakn, whether a concept type or a data instance, is a [Concept](../04-concept-api/01-concept.md). The diagram below, illustrates how the Concept superclass is inherited by its direct and indirect descendants.

![Concept Hierarchy](../images/concept-api/overview_hierarchy.png)

**Type** refers to a Concept Type as defined in the [schema](../10-schema/00-overview.md#grakn-data-model).

**Thing** refers to an instance of data that is an instantiation of a Concept Type.

**Rule** refers to a [Graql Rule](../10-schema/03-rules.md).

<div class="note">
[Important]
The methods called on Concepts are bound to the [transaction](../03-client-api/00-overview.md#transaction) that was used to retrieve the concept initially. As soon as the transaction in question is closed, methods can no longer be called on the retrieved Concepts. To continue using the Concept API on a concept, we must retrieve that concept again with a newly created transaction.
</div>

In the sections that follow, we learn about the methods available on [Concept](../04-concept-api/01-concept.md), [Type](/docs/concept-api/type.md#type-methods), [EntityType](/docs/concept-api/type.md#entitytype-methods), [AttributeType](/docs/concept-api/type.md#attributetype-methods), [RelationType](/docs/concept-api/type.md#relationtype-methods), [Thing](../04-concept-api/04-thing.md#thing-methods), [Attribute](../04-concept-api/04-thing.md#attribute-methods), [Relation](../04-concept-api/04-thing.md#relation-methods) and [Rule](../04-concept-api/03-rule.md).

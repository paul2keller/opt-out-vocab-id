---
title: "Proposal for an Opt-Out Vocabulary"
abbrev: "Opt-Out Vocab"
category: info

docname: draft-keller-aipref-vocab
submissiontype: IETF  
number:
date:
consensus: true
v: 3
area: AREA
workgroup: WG Working Group
keyword:
 - AI Preferences
 - Opt-Out
 - Vocabulary
venue:
  group: WG
  type: Working Group
  mail: ai-control@ietf.org
  arch: https://example.com/WG
  github: paul2keller/opt-out-vocab-id
  latest: https://example.com/LATEST

author:
 -
    fullname: Paul Keller
    organization: Open Future
    email: paul@openfuture.eu

normative:

* [RFC9309](https://datatracker.ietf.org/doc/rfc9309/): Robots Exclusion Protocol

informative:

* [A Vocabulary for Opting Out of AI Training and Other Forms of TDM](https://openfuture.eu/publication/a-vocabulary-for-opting-out-of-ai-training-and-other-forms-of-tdm/), Paul Keller (2025)
* [Directive (EU) 2019/790 of the European Parliament and of the Council of 17 April 2019 on copyright and related rights in the Digital Single Market](https://eur-lex.europa.eu/eli/dir/2019/790/oj/eng)

--- abstract

This document proposes a standardized vocabulary of use cases that can be targeted when expressing machine-readable opt-outs related to Text and Data Mining (TDM) and AI training. The vocabulary is agnostic to specific opt-out mechanisms and enables declaring parties to communicate restrictions or permissions regarding the use of their digital assets in a structured and interoperable manner. It defines three key use cases—TDM, AI Training, and Generative AI Training—which can be referenced by opt-out systems to ensure consistent interpretation across different implementations.

--- middle

# Introduction

TODO Introduction


# Conventions and Definitions

{::boilerplate bcp14-tagged}

# Purpose

The purpose of this document is to provide a common vocabulary that can be used for machine-readable opt-outs by parties who wish to restrict the use of their assets for the purpose of AI training and other forms of Text and Data Mining (TDM).

The elements of the vocabulary can be used to describe, in a standardized way, the types of uses that a declaring party may wish to restrict (or allow), thereby ensuring that opt-outs can be communicated, processed and stored in a consistent and interoperable manner.

The vocabulary is agnostic to the technical implementations of opt-out systems and is designed to ensure that opt-out information can be effectively exchanged between different systems. The vocabulary is intended to govern the use of works in the context of training AI models and other forms of TDM but does not concern itself with the collection of training data (crawling). In particular the vocabulary is not intended for expressing instructions or restrictions related to crawling for the purpose of building a search index, as there are already more specific standards and protocols for this purpose including but not limited to [RFC9309](https://datatracker.ietf.org/doc/rfc9309/).

The vocabulary is intended to both work in contexts where such opt-outs expressed to the declaring party give rise to legal obligation (such as rights reservation made by rightholders) and in contexts where this is not the case. It is without prejudice to applicable laws and the applicability of exceptions and limitations.

# Definitions

* **Asset:** A digital file or stream of data, usually with associated metadata.
* **Declaring party:** The entity that expresses an opt-out with regards to an Asset.

# Vocabulary Structure

The vocabulary consists of the overarching TDM (Text and Data Mining) category and a number of specific use cases that can be addressed independently. The overarching category `TDM` is based on the definition of Text and Data Mining in [Article 2(2) of the European Union Directive on Copyright in the Digital Single Market](https://eur-lex.europa.eu/eli/dir/2019/790/oj/eng#art_2).

# Proposed Vocabulary

The following categories are defined for use in the opt-out vocabulary:

* **TDM**: Text and Data Mining. The act of using one or more assets in the context of any automated analytical technique aimed at analyzing text and data in digital form in order to generate information which includes but is not limited to patterns, trends and correlations.
* **AI Training**: The act of training AI models
* **Generative AI Training**: The act of training General Purpose AI models that have the capacity to generate text, images or other forms of synthetic content, or the act of training other types of AI models that have the purpose of generating text, images or other forms of synthetic content.

This list of specific use cases may be expanded in the future, should a consensus emerge between stakeholders, to include categories that address additional use cases as they emerge. In addition to these categories defined in the vocabulary, it is also expected that some systems implementing this vocabulary may extend this list with additional categories for their particular needs.

## Relationship with more specific instructions

The vocabulary does not preclude the use of other specific categories. Any opt-outs based on this vocabulary shall not be interpreted as restricting the use of the work(s) strictly for the purpose of search and discovery as long as no restriction is declared through search-specific means such as [RFC9309](https://datatracker.ietf.org/doc/rfc9309/).

When using this vocabulary more specific instructions — either based on the vocabulary or derived from other protocols — should be given preference over less specific ones.

## Relationship between categories

The TDM category is the overarching category that includes the AI training category. Generative AI training is a subset of the AI training category. Both AI training and generative AI training are considered to be forms of TDM. As such, when a Declaring Party opts out of TDM, they also opt out of these categories. AI model developers processing opt-outs must therefore interpret an opt-out from TDM to also mean an opt-out from Generative AI Training and AI Training.

The figure below shows the relationship between the currently defined categories:

Systems referencing the vocabulary must not introduce additional categories that include existing categories defined in the vocabulary or otherwise include additional hierarchical relationships.

# Usage

The vocabulary may be used by declaring that an opt-out system or entity expressing or processing opt-outs uses the terms defined in the "Proposed Vocabulary" section above, directly or via mappings, in accordance with how they are defined in this document.

# Security Considerations

TODO Security


# IANA Considerations

This document has no IANA actions.

--- back

# Acknowledgments
{:numbered="false"}

TODO acknowledge.

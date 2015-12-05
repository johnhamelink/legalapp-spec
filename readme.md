# LegalApp Spec

## What is this document?

This document attempts to record and address the specific needs of the LegalApp
document specification. The LegalApp document specification (LDS) is required
to be able to create a conditional logic definition for complex legal documents
with a large (but finite) number of combinations.

This document also comes with a [counterpart JSON reference](sample_doc.json), which will be unit
tested against.

## LDS overview

The LDS consists of three distinct types of data:

 - Content snippets
 - Directives, such as:
   - Iterators
 - Dependencies:
   - Data Dependencies

This document will describe in detail how these data types fit together and can
be used to construct complex documents with lots of conditional logic.

### Content Snippets

Content Snippets provide chunks of plaintext, formatted in
[CommonMark](http://commonmark.org/).  Content Snippets are generally enveloped
by logical structures.

#### Interpolation

References to data dependencies can be placed inside the Content Snippets,
which can optionally be defined through a directive. If left unresolved, an
attempt will be made server-side to resolve the dependency, and failing that,
the user will be prompted to fill in the necessary details, which are then saved.

### Directives

Directives are structural data that define logic that helps determine which
content should be displayed, as well as allowing for iteration over data.

#### Example Iterator Types:

 - Loop Syntax (More info is #TODO)
 - If Syntax (More info is #TODO)

### Dependencies

Dependencies help to provide content. They perform a lookup from three places, first to last:

 - Definitions list (More info is #TODO)
 - API Endpoint (More info is #TODO)
 - User Prompt (More info is #TODO)


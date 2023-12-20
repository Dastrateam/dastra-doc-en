# Create a relationship between treatments

In Dastra you can create relationships between your processes to make them easier to manage.&#x20;

These relationships are possible between processes located in the same workspace but also within different workspaces.

## Add a relationship

To do this, go to a treatment record and select the "Relationships" tab located at the top of the record.

<figure><img src="../../.gitbook/assets/Capture d’écran 2023-02-06 à 10.34.30.png" alt=""><figcaption></figcaption></figure>

Next, you will need to select a relationship type.

<figure><img src="../../.gitbook/assets/Capture d’écran 2023-02-06 à 10.37.45.png" alt=""><figcaption></figcaption></figure>

You can select the type of relationship between treatments.

<figure><img src="../../.gitbook/assets/Capture d’écran 2023-02-06 à 10.38.41.png" alt=""><figcaption></figcaption></figure>

## Relationship details

### Is a child of:&#x20;

Hierarchical relationship allowing graphic visualization. No slavishness between the fields.&#x20;

The treatment A is hierarchically under the treatment B.

### Is parent of:&#x20;

Hierarchical relationship allowing graphic visualization. No slavishness between the fields.&#x20;

Processing A is hierarchically above processing B.&#x20;

### Is related to:

Simple logical link between 2 processes, no slavishness between the two nor control rule.&#x20;

### Has the following duplicated:

This relationship allows to keep track of the duplicated elements from this treatment. A relational link is created automatically when a treatment is duplicated.&#x20;

### Is copied from:

This relationship is used to keep track of the source of the duplicate treatment. A relational link is created automatically when a treatment is duplicated.

### Is master of:&#x20;

The fields of the original treatment (A) replace the fields of the target treatment (B).&#x20;

Strict linkage between treatment A and treatment B. The pre-existing fields of treatment B are deleted when the link is set up. The fields in Treatment B that are slaved to Treatment A are not modifiable in Treatment B, and no new fields can be added, deleted or modified. As long as the referential elements are retained, the pre-existing fields in Processing B are restored when the link is revoked.

### Is slave of:

The fields of the target treatment (B) replace the fields of the original treatment (A).&#x20;

Strict linkage between treatment B and treatment A. The pre-existing fields of A are deleted when the link is set up. Fields in A that are slaved to B are not modifiable in A, and no new fields can be added, deleted or modified. As long as the referential elements are preserved, pre-existing fields in B are restored when the link is revoked.

### Inherited from (Soft inheritance):

The target process (B) automatically inherits the fields from the original process (A).&#x20;

It's possible to add, delete or modify new fields in treatment B, but cannot modify the fields inherited from treatment A. Any modification in the fields of treatment A is automatically reflected in the fields inherited from treatment B. When the link is revoked, the fields inherited from treatment A become editable again in treatment B. The fields that existed in treatment B before the link was set up are kept after the link is created.

### Is tutor of (Soft inheritance):

The original process (A) automatically passes its fields to the target process (B).&#x20;

The target process B automatically inherits the fields of the original process A. The target process B can add, delete or modify new fields, but cannot modify the fields inherited from process A. Any changes to the fields in Process A are automatically reflected in the fields inherited from Process B. When the link is revoked, the inherited fields become editable again in treatment B. The fields that existed in B before the link was created are kept after the link is created.

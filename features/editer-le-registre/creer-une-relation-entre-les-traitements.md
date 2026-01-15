# Create relationships between processing activities

In Dastra you can create relationships between your processings to make them easier to manage.&#x20;

These relationships are possible between processings located in the same workspace.

## Why create relationships between processing?

Relationships between processings can be used to materialize responsibility relationships between the various entities responsible for processing. For example, in a corporate group, you can set up a relationship between a processing operation carried out by the parent company and the processing operations carried out by the subsidiaries.&#x20;

This is often the case for processing relating to the group's general administration, such as human resources management, accounting, supplier management, etc.

> A parent company X implements payroll processing on behalf of its subsidiaries Y and Z. In entity X, a "payroll management" process (P1) is created as a subcontractor. From this process, we can create a strong inheritance relationship with two other processing (C1 and C2) located in Y and Z, which will be created as data controllers. In this way, updates to P1 will be automatically relayed to C1 and C2.

## Add a relationship

To do this, go to a processing and select the "Relationships" tab located at the top of the record.

<figure><img src="../../.gitbook/assets/Capture d’écran 2023-02-06 à 10.34.30.png" alt=""><figcaption></figcaption></figure>

Next, you will need to select a relationship type.

<figure><img src="../../.gitbook/assets/Capture d’écran 2023-02-06 à 10.37.45.png" alt=""><figcaption></figcaption></figure>

You can select the type of relationship between processing activities.

<figure><img src="../../.gitbook/assets/Capture d’écran 2023-02-06 à 10.38.41.png" alt=""><figcaption></figcaption></figure>

### Types of relationships

There are two types of relationships:

1. **Declarative relationships :** Used to establish a simple link between two processes (without functional dependency).
2. **Functional relationships :** Allow fields to be transferred or inherited from one process to another.



### **Declarative relationships** :

#### Is the child of:

Hierarchical relationship allowing structured reading of processes, **without functional dependency** between fields.

> Processing A is hierarchically linked to Processing B.

#### Is parent of:

Hierarchical relationship allowing structured reading of processes, **without functional dependency** between fields.

> Processing A is hierarchically above Processing B.

#### Is related to :&#x20;

Simple logical link between two processes, without functional dependency or interdependence between fields.

> Processing A is related to processing  B.

#### Is copied from :

This relationship allows you to keep track of items duplicated from this process. This relationship is created automatically when a process is duplicated.

> Processing A is the source (of duplication) of Processing B.

#### Has the following duplicate :&#x20;

This relationship allows you to keep track of the source of the processing duplication. This relationship is created automatically when a processingt is duplicated.

> Processing A is a duplicate of Processing B.

###

### **Functional relationships** :

#### Is master of :

The fields in target processing A completely replace those in original processing B.

{% hint style="warning" %}
With the exception of the fields in tab 1 “General” and the documents associated with processing in tab 11 “Documentation.”
{% endhint %}

* Strict relationship between A and B.
* Pre-existing fields in B are deleted when the link is created.
* Fields inherited from A **cannot be modified or deleted**, and no new fields can be added to B.
* If the link is deleted, the original fields in B are restored (the repository elements are retained).



#### Is slave of :

The fields in target treatment B completely replace those in the original treatment A.

{% hint style="warning" %}
With the exception of the fields in tab 1 “General” and the documents associated with processing in tab 11 “Documentation.”
{% endhint %}

* Strict relationship between B and A.
* Pre-existing fields in A are deleted when the link is created.
* Fields inherited from B **cannot be modified or deleted**, and no new fields can be added to A.
*   If the link is deleted, the original fields in B are restored (the repository elements are retained).<br>

    <div data-gb-custom-block data-tag="hint" data-style="danger" class="hint hint-danger"><p>A process can only be slave of one process at a time.</p></div>

####

#### **Is tutor of (soft inheritance) :**

The source process A automatically transmits its fields to the target process B.

{% hint style="warning" %}
With the exception of the fields in tab 1 “General” and the documents associated with processing in tab 11 “Documentation.”
{% endhint %}

* A transfers its fields to B.
* The inherited fields cannot be modified in B.
* B can add, modify, or delete its own fields.
* Any modification to the fields in A is automatically reflected in B.
* If the link is deleted, the inherited fields become modifiable again.
* The pre-existing fields in B are retained.



#### **Inherited from (soft inheritance) :**

The source process B automatically transmits its fields to the target process A.

{% hint style="warning" %}
With the exception of the fields in tab 1 “General” and the documents associated with processing in tab 11 “Documentation.”
{% endhint %}

* B inherits the fields from A.
* The inherited fields cannot be modified in B.
* B can add, modify, or delete its own fields.
* Any modification to the fields in A is automatically reflected in B.
* If the link is deleted, the inherited fields become modifiable again.
* The pre-existing fields in B are retained.

{% hint style="danger" %}
A process can only inherit from one process at a time.
{% endhint %}

####

### Summary table of relationships:

| **Type of relationship**                                                           | **Tab 1 – “General”** | **Tabs 2 to 10** (business fields) | **Documentation uploaded in tab 11 – “Documentation”** | **Modifiability of fields specific to the target treatment** |
| ---------------------------------------------------------------------------------- | --------------------- | ---------------------------------- | ------------------------------------------------------ | ------------------------------------------------------------ |
| **Hierarchical/logical relationships** (Parent/Child/Related to/Copied by/Copy of) | No impact             | No impact                          | No impact                                              | No impact                                                    |
| **Is master of**                                                                   | ❌ Not transmitted     | ✅ Transmitted                      | ❌ Not transmitted                                      | ❌ Unable to add/edit/delete                                  |
| **Is slave of**                                                                    | ❌ Not inherited       | ✅ Inherited                        | ❌ Not inherited                                        | ❌ Unable to add/edit/delete                                  |
| **Is tutor of (soft inheritance)**                                                 | ❌ Not transmitted     | ✅ Transmitted                      | ❌ Not transmitted                                      | ✅ Addition/modification/deletion possible                    |
| **Inherited from (soft inheritance)**                                              | ❌ Not inherited       | ✅ Inherited                        | ❌ Not inherited                                        | ✅ Addition/modification/deletion possible                    |


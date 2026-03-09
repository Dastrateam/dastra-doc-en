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

### **Functional relationships** :

Functional relationships allow fields to be transferred or inherited from one processing to another.

**Is source of (strict inheritance)**

{% hint style="warning" %}
The source processing **A** transmits all its fields to the dependent processing **B**, except for the fields in tab 1 **“General”** and the documents associated with the processing in tab 11 **“Documentation.”**
{% endhint %}

This creates a strict relationship between **A (source)** and **B (dependent)**.

When the relationship is created:

* Pre-existing fields in **B** are deleted.
* Fields inherited from **A** cannot be modified or deleted in **B**.
* No new fields can be added in **B**.

Any modification made in **A** is automatically reflected in **B**.

If the relationship is removed:

* The inherited fields become editable again.
* The original fields in **B** are restored (repository elements are retained).

***

**Is dependent on (strict inheritance)**

Processing **A** depends on processing **B** and inherits its fields.

{% hint style="warning" %}
All fields from **B** replace those in **A**, except for the fields in tab 1 **“General”** and the documents associated with the processing in tab 11 **“Documentation.”**
{% endhint %}

This creates a strict relationship between **B (source)** and **A (dependent)**.

When the relationship is created:

* Pre-existing fields in **A** are deleted.
* Fields inherited from **B** cannot be modified or deleted in **A**.
* No new fields can be added in **A**.

Any modification made in **B** is automatically reflected in **A**.

If the relationship is removed:

* The inherited fields become editable again.
* The original fields in **A** are restored (repository elements are retained).

{% hint style="info" %}
A processing can only be **dependent on one source processing at a time**.
{% endhint %}

#### **Is source of (soft inheritance) :**

The source processing **A** automatically transmits its fields to the dependent processing **B**, except for the fields in tab 1 **“General”** and the documents associated with the processing in tab 11 **“Documentation.”**

{% hint style="warning" %}
With the exception of the fields in tab 1 “General” and the documents associated with processing in tab 11 “Documentation.”
{% endhint %}

This creates a soft inheritance relationship between **A (source)** and **B (dependent)**.

* Fields inherited from **A** cannot be modified in **B**.
* **B** can add, modify, or delete its own fields.
* Any modification made in **A** is automatically reflected in **B**.

If the relationship is removed:

* The inherited fields become editable again.
* The pre-existing fields in **B** are retained.

#### Is dependent on (soft inheritance)

Processing **A** depends on processing **B** and inherits its fields, except for the fields in tab 1 **“General”** and the documents associated with the processing in tab 11 **“Documentation.”**

{% hint style="warning" %}
With the exception of the fields in tab 1 “General” and the documents associated with processing in tab 11 “Documentation.”
{% endhint %}

This creates a soft inheritance relationship between **B (source)** and **A (dependent)**.

* Fields inherited from **B** cannot be modified in **A**.
* **A** can add, modify, or delete its own fields.
* Any modification made in **B** is automatically reflected in **A**.

If the relationship is removed:

* The inherited fields become editable again.
* The pre-existing fields in **A** are retained.

{% hint style="info" %}
A processing can only be **dependent on one source processing at a time**.
{% endhint %}

### Summary table of relationships:

| Type of relationship                                                                   | Tab 1 – “General” | Tabs 2 to 10 (business fields) | Documentation uploaded in tab 11 “Documentation” | Modifiability of fields specific to the target processing |
| -------------------------------------------------------------------------------------- | ----------------- | ------------------------------ | ------------------------------------------------ | --------------------------------------------------------- |
| Hierarchical / logical relationships (Parent/Child / Related to / Copied by / Copy of) | No impact         | No impact                      | No impact                                        | No impact                                                 |
| **Is source of (strict inheritance)**                                                  | ❌ Not transmitted | ✅ Transmitted                  | ❌ Not transmitted                                | ❌ Unable to add/edit/delete                               |
| **Is dependent on (strict inheritance)**                                               | ❌ Not inherited   | ✅ Inherited                    | ❌ Not inherited                                  | ❌ Unable to add/edit/delete                               |
| **Is source of (soft inheritance)**                                                    | ❌ Not transmitted | ✅ Transmitted                  | ❌ Not transmitted                                | ✅ Addition / modification / deletion possible             |
| **Is dependent on (soft inheritance)**                                                 | ❌ Not inherited   | ✅ Inherited                    | ❌ Not inherited                                  | ✅ Addition / modification / deletion possible             |


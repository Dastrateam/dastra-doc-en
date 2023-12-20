---
description: Learn how to activate and use the processing freshness option
---

# Processing freshness

The freshness of a processing is an indicator of when it was last updated. Freshness will decrease as the expiry date of the processing approaches. This feature is a simple and fun way of ensuring that the information in your record of processings is always up to date.

### Activate the processing freshness option

Processing freshness is optional and deactivated by default.&#x20;

To activate the option, go to your record of processings, click on the action selector for the "New data processing" button and then on "Enable processings freshness".&#x20;

This action is reserved for your workspace administrators.

<figure><img src="../../.gitbook/assets/image (316).png" alt=""><figcaption></figcaption></figure>

The following window appears, giving you the option of setting the expiry interval for your processing. The freshness of a processing corresponds to the number of days between the last date on which the processing was marked as fresh and the expiry date of the processing.&#x20;

The expiry date is a date in the future calculated from the last date on which the processing was marked as fresh, to which we add the expiry interval. Please note that this expiry interval will be the same for all processing in your register.&#x20;

A second option allows you to mark all the processing in your register as fresh when you activate the option (this will start a freshness cycle for all the processing in the register immediately).

<figure><img src="../../.gitbook/assets/image (319).png" alt=""><figcaption></figcaption></figure>

_Example: Today is 04/07/2023, I activate the freshness of processing option in my record of processings and set an expiry interval of 1 month. I tick the option "set all of your processings as fresh as of today" and validate. The expiry date for my processing is calculated as 04/08/2023 (last date on which my processing was marked fresh, 04/07/2023, to which we add the expiry interval, 1 month). I reconnect on 15/07/2023, and my processing still has 20 days of freshness left (the difference between the expiry date and today's date)._

### Disable the processing freshness option&#x20;

To deactivate the option, go to your record of processings, click on the action selector for the "New data processing" button and then on "Disable processing freshness option".&#x20;

This action is reserved for your workspace administrators. Each processing will retain the last date on which it was marked as fresh if you decide to reactivate the option in the future.

<figure><img src="../../.gitbook/assets/image (317).png" alt=""><figcaption></figcaption></figure>

### Freshness indicators&#x20;

Once the option has been activated, you will find freshness indicators for your processing in several places. Please note that freshness is only displayed for **published processings** that have been **marked as fresh at least once** (either when the option is activated via the "mark all your processings as fresh as of today" selector, or manually in a processing record).

#### In the right-hand menu of your processing record&#x20;

You will find the freshness indicator in the top right-hand corner of your processing record (provided that the processing has been published and marked as fresh at least once). This indicator consists of a label with the values "Fresh", "Relatively fresh" and "Expired", a colour (green, yellow and red respectively), a progress bar that decreases as the expiry date approaches, a button for marking the processing as fresh and the number of days remaining or overdue in relation to the expiry date.

<figure><img src="../../.gitbook/assets/image (321).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (318).png" alt=""><figcaption><p>In mobile view, you will also find this indicator in the navigation bar at the top of your processing record.</p></figcaption></figure>

#### In the freshness column of your processing register

&#x20;By displaying the freshness column in the list view of your processing register, you can find the indicator for each processing record that meets the display conditions (published processing with at least one date on which it was identified as fresh).

<figure><img src="../../.gitbook/assets/image (315).png" alt=""><figcaption></figcaption></figure>

### Mark as fresh

You can decide to refresh a processing at any time, without necessarily waiting for the expiry date.&#x20;

To do this, click on "mark as fresh" to display the window for refreshing a processing (in mobile display, this window can be accessed by clicking on the leaf freshness icon):

<figure><img src="../../.gitbook/assets/image (314).png" alt=""><figcaption></figcaption></figure>

By marking the processing as fresh, you will restart a freshness cycle from today's date until the next expiry date. The expiry date is calculated by default according to the freshness policy of your workspace (freshness interval applied when the processing freshness option is activated). You can decide to ignore this default date and apply a specific expiry date to this processing by ticking the "Change expiry date" option and selecting a new date (the expiry date must be at least D+1).

### Important information about how freshness works&#x20;

Please note that we treat the date on which a processing record is updated (when the record is saved, for example) independently of the date on which a processing was identified as fresh. It is therefore necessary to click on "mark as fresh" to (re)initialise the freshness date of a processing record.&#x20;

### Notifications&#x20;

The owner of a processing that has become outdated will receive a warning email to remind them that one of their treatments has not been reviewed for a long time and that it is time to refresh it.

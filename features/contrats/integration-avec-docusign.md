# Docusign integration

We have implemented a native integration between Dastra and DocuSign, the global leader in electronic signatures, allowing you to send, sign, and track the status of a signature directly from Dastra's contract module.

To set up and access this integration in the signature section of a contract, please go to the settings of your workspace, navigate to the integrations tab, and configure it accordingly.

Once the DocuSign integration is open, please click on "Add Integration". You will then be redirected to DocuSign authentication to link your DocuSign account with Dastra. After the connection is established, you will need to enter your DocuSign AccountId and your DocuSign Account Base URI in Dastra.

<figure><img src="../../.gitbook/assets/image (358).png" alt=""><figcaption></figcaption></figure>

Once these fields are filled out, you have completed the integration setup. You can now navigate to the contract module and manage the signing of your contracts electronically.

### DocuSign Signing Interface

Below is the signing interface for a contract via DocuSign (accessible from the "Add Signature" button next to a signatory).

To validate this page, you must have:

* An actor (signer) with a valid email address.
* A document attachment to be signed in PDF, DOC, or DOCX format.
* A title for the signing invitation email.

You can also add detailed instructions for signing the document. These instructions will be included in the signing invitation email and will be visible to the signatory in the DocuSign interface when they access the document to sign.

<figure><img src="../../.gitbook/assets/image (359).png" alt=""><figcaption></figcaption></figure>

Once the signature is sent, its status is automatically synchronized with your contract and will be updated whenever there is a status change on the DocuSign side.

<figure><img src="../../.gitbook/assets/image (360).png" alt=""><figcaption></figcaption></figure>

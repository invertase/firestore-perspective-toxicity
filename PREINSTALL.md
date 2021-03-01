Use this extension to get toxicity scores from [Perspective
API](perspectiveapi.com) for comments
written to a Cloud Firestore collection.

This extension runs Perspective API on the string field you specify for each
document in your collection. The API uses machine learning models to score the 
perceived impact a comment might have on a conversation. This extension gives 
your text scores for the following attributes: TOXICITY, SEVERE_TOXICITY,
IDENTITY_ATTACK, INSULT, PROFANITY, and THREAT. It is run when a new document is
added to your collection or an existing document is modified.

# Additional setup

Before you can use this extension, you will need to enable Perspective API.
Follow [the instructions on our Get Started page](https://support.perspectiveapi.com/s/docs-get-started)
to request API access and then [enable the API and create an API
key](https://support.perspectiveapi.com/s/docs-enable-the-api).

By default, you're granted quota for 1 QPS to Perspective API. For additional
QPS, fill out a [quota increase
request](https://support.perspectiveapi.com/s/request-quota-increase) as needed. Note
that if you add or update documents at a rate higher than your allotted QPS,
you may exceed quota and the extension will fail to score your documents.

# Billing

This extension uses other Firebase or Google Cloud services which may have
  associated charges:

*   Cloud Firestore
*   Cloud Functions

When you use Firebase Extensions, you're only charged for the underlying
resources that you use. A paid-tier billing plan is only required if the
extension uses a service that requires a paid-tier plan, for example calling to
a Google Cloud API or making outbound network requests to non-Google services.
All Firebase services offer a free tier of usage.
[Learn more about Firebase billing.](https://firebase.google.com/pricing)

Perspective API is free for all amounts of quota. Any costs associated with this
extension come from the Firebase and Google Cloud Platform services listed above.
---
  title: Decisions about analytics
  date: 2022-06-14
---

It’s important for us to be able to understand how people are using the eligibility checker, but we also need to protect people's right to privacy while they use the service.

To help us do this, we looked at three options.

First, we considered Google Analytics, which we could tailor to stay compliant with GDPR. That would mean:
- enabling the ‘Anonymise IP’ setting
- enabling pseudonymisation of IDs
- including Google as a data processor in the privacy policy
- finding a way to ask for consent for the Google Analytics cookies
- disabling data-sharing in the Google Analytics settings
- disabling advertising data acquisition in Google Analytics settings
- ensuring we have an agreement with Google Ireland Ltd and not Google LLC so data is processed in Europe, not the US

We also looked at Ahoy + Blazer, which would keep all tracking local and anonymous. This would require:
- storing all events in a local database
- configuring without cookies and with IP masking
- creating dashboards/queries in Blazer to visualise the usage
- creating a recurring task to delete data at the end of the retention period

Then we explored [DfE Analytics](https://github.com/DFE-Digital/dfe-analytics), which is the preferred option within DfE and requires:
- sending all events to a BigQuery database using the dfe-analytics Gem
- configuring without cookies and with IP masking
- creating dashboards/queries in Data Studio to visualise the usage
- use a paid service such as [Fathom](https://usefathom.com/)– easy to add to the app, so we’re GDPR compliant out-of-the-box


#### What we went for

After considering the options, we went for DfE Analytics. It gives us the most control and allows us to progressively enhance the analytics capabilities as required. It also has the least amount of bureaucracy associated with signing agreements and updating policies.

Finally, it’s also the preferred option within DfE and we can make improvements to the analytics library for other users as we develop our service.


#### What we still need to do

We need to set up DfE Analytics in accordance with our requirements, both creating the integration with BigQuery and the dashboards/queries to visualise the data.

It's worth noting that DfE Analytics is perhaps the least mature of the options, and there’s a risk associated with this – we'd be an early adopter. However, as the aim of the library is to streamline analytics for all DfE teams down the line, we can help with that goal.

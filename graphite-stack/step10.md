
### Count of success vs error.

Counts of status code types can tell us many things:

- **When the number of successful calls go down or falls to zero while error calls rise**

    It's clear that there is some issue. For many API's there will be a baseline, especially for outward facing API's. We cannot expect all API's to be perfect, with no erroring calls, but we can know what behaviour we consider "normal" and acceptable by the KPI's and act when our metrics differ.

- **The total count of successes and errors also shows us how much traffic is hitting the API.**

    If we see the count rise and more error rise as well, it may be that the API cannot handle the load it is receiving. 

### Duration / Latency

Latency is useful in a number of ways:

- **When the latency is longer than usual but the count of calls hasn't increased substantially**

    This suggests that there is something wrong with the API or with the work happening before a response is given. If a response takes too long it can lead to broken Service Level Agreements (SLAs), timeouts and, concerning to most, a loss of earnings.

- **When the latency is longer than usual and the count of calls has increased**

    This would suggest that the API is struggling with the amount of traffic it is receiving. 

- **If the successful latency is longer, and the error count has gone up**

    Again, this suggests that something has gone awry ad that the calls are at risk of timing out. 

The ideal situation is a short latency for both errors (if there are any) and successes, a high success rate and low error rate. There are numerous behaviours that can suggest things going wrong in the API just by these few baseline metrics.

You can now set up the baseline metrics for measuring the health of your APIs.
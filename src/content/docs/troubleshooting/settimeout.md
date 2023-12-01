---
title: setTimeout
lastUpdated: 2023-12-01
tableOfContents: false
---

You can use `setTimeout`, but it has some quirks:

1. We recommend that you wrap the timeout in a promise and await it. (Otherwise
   we may kill your evaluation prematurely if we fail to detect that it’s still
   waiting on a timeout.)

   <div class="not-content">
     <iframe src="https://www.val.town/embed/stevekrouse.delayEx" width="100%" frameborder="no" style="height: 400px;">
       &#x20;
     </iframe>
   </div>

2. We don’t limit the duration of your timeout, but we do limit the duration of
   val execution (1 min for free accounts and 5 min for paid), so any timeout
   longer than this will not execute.
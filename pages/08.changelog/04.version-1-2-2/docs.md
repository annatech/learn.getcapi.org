---
title: 'Version 1.2.2'
taxonomy:
    category:
        - docs
---

## Overview

cAPI Core v1.2.2 is a minor bug fix release to fix an error which broke the DELETE /user/edit/:id method. Also changed instances of $app->request->post() to $app->request->params() to resolve issue with Swagger UI successfully submitting form request to API during testing.

Updated documentation can be found here:
http://learn.getcapi.org 
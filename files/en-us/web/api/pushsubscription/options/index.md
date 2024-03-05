---
title: PushSubscription.options
slug: Web/API/PushSubscription/options
page-type: web-api-instance-property
tags:
  - API
  - Property
  - Push API
  - PushManager
  - Reference
  - Service Worker
browser-compat: api.PushSubscription.options
---

{{APIRef("Push API")}}

The **`options`** read-only property
of the {{domxref("PushSubscription")}} interface is an object containing the options
used to create the subscription.

## Value

An read-only {{domxref("PushSubscriptionOptions")}} object containing the following values:

- `userVisibleOnly`
  - : A boolean, indicating that the returned push
    subscription will only be used for messages whose effect is made visible to the user.
- `applicationServerKey`
  - : A public key your push server will use to send
    messages to client apps via a push server. This value is part of a signing key pair
    generated by your application server, and usable with elliptic curve digital signature
    (ECDSA), over the P-256 curve.

## Specifications

{{Specifications}}

## Browser compatibility

{{Compat}}
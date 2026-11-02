# Contributing

Start from `main` and create a focused `feature/`, `fix/`, or `docs/` branch. Keep behavior changes and documentation accurate together.

```sh
npm ci
npm run validate
npm run package:metadata
```

The tests use an in-memory double of the Script API. It can't prove platform behavior: on the sandbox, it had passed several real bugs. For a platform change, run the [sandbox smoke test](docs/prime-membership-deployment.md#sandbox-smoke-test), and check every `dw.*` call against the Script API reference.

Preserve these rules:

- only `activateFromOrder` and the verified review path change entitlements, from the order's state on the server; nothing in a request can mark a payment as paid;
- entitlements come from the membership custom object on every call; a customer group can narrow a benefit, never grant one;
- amounts are integer cents, and a monetary benefit always has per-order and annual caps; invalid configuration grants nothing;
- a storefront request creates few custom objects, because the platform allows 10 per request across all cartridges; an order gets one usage row;
- a custom object query uses at most 4 custom attribute expressions (the tests enforce it);
- every job can be repeated without double effects, and only the job sends e-mail.

Keep credentials and generated output out of Git. Add new attributes to the metadata and to [docs/prime-membership-data-model.md](docs/prime-membership-data-model.md).

See [NOTICE.md](NOTICE.md) for attribution and terms.

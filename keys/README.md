# Public verification keys

PRISM beta updates are signed with Ed25519.
Only **public** keys belong in this repository.

| key_id | status | notes |
|---|---|---|
| `prism-beta-test-ed25519-1` | **TEST ONLY — not trusted in customer builds** | Fixture for isolated unit/dev tests with `allowTestKeys`. Packaged production/beta customer builds must **not** accept this key. Production trust remains empty until the owner pins a real public key via the offline owner key procedure. |

Public SPKI (base64) for the fixture key (tests only):

```
MCowBQYDK2VwAyEA+WOHp/1dY33xkOvPTU6T0i/1lIUvSvx7iPHtIEhl95g=
```

Private keys are never published here.
Production private keys must never enter Git, CI, chat, or the application.
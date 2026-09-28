# rust-device-rules

**Open constitution for long-running Rust device daemons** — shared Cursor agent
rules (`.mdc`) for a privileged, native process on constrained devices
(platform backends, local IPC, small footprint).

Rules describe **how to code**. They do **not** contain product requirements,
product names, storage class catalogs, cloud schema catalogs, or topology
locks (e.g. sole MQTT gateway) — those live in each consumer repo under
`docs/specification/`.

Shared practices (DI/singleton concepts, fail-fast, SDD, testing tiers) follow
naming from [`python-services-rules`](https://github.com/drivestream-lab/python-services-rules)
and sibling packs; Rust idioms are craft detail inside those topics.

| | |
|---|---|
| **License** | [MIT](LICENSE) |
| **Version** | see [`VERSION`](VERSION) (currently **0.1.0**) · [CHANGELOG](CHANGELOG.md) |
| **Mount path** | `.cursor/rules/` (git submodule) |
| **Scaffold** | `rust-device-foundation` (when published) |

**Scope boundary:** long-running Rust **device daemon** chassis. **Not** for
cloud Rust services, embedded C (Vigil), or one-shot CLIs.

---

## Layout

```text
rust-device-rules/
  VERSION
  README.md
  CHANGELOG.md
  code-guidelines-index.mdc
  architecture.mdc
  platform-backends.mdc
  process-lifecycle.mdc
  local-ipc.mdc
  resource-governance.mdc
  cloud-adapter.mdc
  credential-store.mdc
  dependency-injection.mdc
  fail-fast.mdc
  logging-observability.mdc
  rust-tooling.mdc
  testing-verify-flows.mdc
  spec-driven-development.mdc
  rust-device-adr.mdc
```

---

## Adoption

```bash
rm -rf .cursor/rules
git submodule add https://github.com/drivestream-lab/rust-device-rules.git .cursor/rules
cd .cursor/rules && git checkout v0.1.0 && cd ../..
git add .gitmodules .cursor/rules
git commit -m "Add rust-device Cursor rules at .cursor/rules (v0.1.0)"
```

---

## Related repositories

| Repo | Role |
|------|------|
| `rust-device-foundation` | Cookiecutter for a Rust device daemon |
| `edge-agent-rules` | Python Edge Agent craft — do **not** mount here |
| `python-services-rules` | FastAPI services — do **not** mount here |

---

## License

MIT — see [LICENSE](LICENSE).

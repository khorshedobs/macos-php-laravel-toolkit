# macOS PHP & Laravel Diagnostic Toolkit

Read-only macOS diagnostic & migration bash utilities for PHP, Laravel, and WordPress developers. Run them directly with `curl | bash` — no dependencies or system mutations required.

## Utilities

### 1. Local SSL & `.test` DNS Doctor (`macos-local-ssl-doctor.sh`)
Diagnoses `/etc/resolver/test`, `dscacheutil`, ports `80`/`443` conflicts, and macOS Keychain Root CA trust issues for local `.test` domains.

```bash
curl -fsSL https://stratosapp.dev/tools/macos-local-ssl-doctor.sh | bash -s -- myapp.test
```

### 2. Native vs. Docker Stack Benchmark (`macos-laravel-stack-benchmark.sh`)
Compares native Nginx / PHP-FPM RSS memory usage and PHP / Artisan startup latency against Docker Desktop on Apple Silicon and Intel Macs.

```bash
curl -fsSL https://stratosapp.dev/tools/macos-laravel-stack-benchmark.sh | bash -s -- .
```

### 3. Laravel Sail / Docker-to-Native Migrator (`laravel-docker-to-native-migrator.sh`)
Non-destructively inspects `docker-compose.yml` and `.env` in any Laravel project and generates ready-to-use `.env.native` and `.stratos.json` configuration files without touching your existing setup.

```bash
curl -fsSL https://stratosapp.dev/tools/laravel-docker-to-native-migrator.sh | bash -s -- .
```

## Requirements

- macOS (Apple Silicon M1–M4 or Intel)
- `bash` and `curl` (included with macOS)

## License

MIT License — see [LICENSE](./LICENSE) for details.

---

Built by [Stratos](https://stratosapp.dev) — Native Swift macOS PHP (8.1–8.6), Laravel & WordPress local dev stack.

## Avazbek Yuldashev

Backend engineer · Java · Spring Boot · PostgreSQL

![My contribution graph, eaten by a snake](https://raw.githubusercontent.com/AvazbekYuldashev/AvazbekYuldashev/output/github-snake.svg)

---

I build REST APIs and Telegram bots — mostly authentication, role-based access, and the integrations a product needs before it can reach real users: SMS gateways, email, file storage, multi-currency money records.

Currently working on **Debt-Book**, a debt and cash-flow ledger for small businesses: per-business workspaces, multi-currency balances, SMS verification, and an Expo mobile client. The schema evolves through versioned Flyway migrations; it runs behind nginx under systemd.

### Day to day

```
Java 21 · Spring Boot 3 · Spring Security · Spring Data JPA · PostgreSQL · Flyway
JWT · springdoc-openapi · Maven · Telegram Bot API · React Native (Expo)
```

### How I structure things

- **Feature-sliced packages, not layer-sliced.** `client/`, `money/`, `expense/`, `sms/` — each owns its controller, service, repository and DTOs.
- **Hexagonal boundaries where the domain earns them.** In the vacancy bot every feature splits into `domain / application / infrastructure / presentation`.
- **One typed exception hierarchy and a single handler,** instead of `try/catch` scattered across services.
- **Schema changes as versioned migrations,** never by hand against a live database.
- **Separate profiles for local, dev and prod** — no environment branching in code.

### Elsewhere

[Telegram](https://t.me/Greed_Coder)

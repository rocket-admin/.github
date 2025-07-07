# 🚀 Rocket Admin

[![license: BSL 1.1](https://img.shields.io/badge/license-BSL%201.1-blue.svg)](LICENSE) [![Docker Pulls](https://img.shields.io/docker/pulls/rocketadmin/rocketadmin)](https://hub.docker.com/r/rocketadmin/rocketadmin) [![Helm Chart](https://img.shields.io/badge/helm-chart-blue)](https://artifacthub.io/packages/helm/rocketadmin/rocketadmin)

Launch a production‑grade, fully‑featured, **white‑label admin panel** in minutes.

Rocket Admin gives your team a secure visual interface on top of your databases—no boilerplate admin code, no manual SQL queries, and no vendor lock‑in.

---

## ✨ Features

* **No‑code schema introspection** – plug in any PostgreSQL, MySQL, MSSQL, Oracle or MongoDB database and get an instant admin panel.
* **Smart editing & bulk operations** – filter, sort, edit and delete rows with spreadsheet‑like ease.
* **Custom Actions & Webhooks** – trigger your own business logic (refunds, bans, emails, …) directly from the UI.
* **Widgets & Related Items** – visualise state with icons, images or charts and traverse relationships across tables.
* **Granular access control** – roles, column‑level permissions, audit trail & MFA ready.
* **Self‑hosted or SaaS** – run a single Docker container, deploy with Helm, or use our cloud.
* **AI Insights (optional)** – ask GPT‑powered questions about your data and get instant answers.
* **White‑label** – bring your own logo, colours and domain.

## 📦 Repositories

| Repository                                                               | Description                                                                                     |
| ------------------------------------------------------------------------ | ----------------------------------------------------------------------------------------------- |
| [`rocketadmin`](https://github.com/rocket-admin/rocketadmin)             | Core application (TypeScript, NestJS + Vue).                                                    |
| [`helm-chart`](https://github.com/rocket-admin/helm-chart)               | Helm chart to run Rocket Admin on Kubernetes.                                                   |
| [`rocketadmin-agent`](https://github.com/rocket-admin/rocketadmin-agent) | Lightweight Docker agent that connects to remote databases (archived – use core image instead). |
| [`rocketadmin-cli`](https://github.com/rocket-admin/rocketadmin-cli)     | Experimental CLI generator (archived).                                                          |
| [`ng2-json-editor`](https://github.com/rocket-admin/ng2-json-editor)     | Angular JSON editor component.                                                                  |
| [`nghacks`](https://github.com/rocket-admin/nghacks)                     | UI utility components for Angular & Material.                                                   |
| [`.github`](https://github.com/rocket-admin/.github)                     | Community health files (this README).                                                           |

## 🚀 Quick start

### Docker (single container)

```bash
docker pull rocketadmin/rocketadmin
docker run -p 8080:8080 \
  -e DATABASE_URL="postgresql://user:pass@db/rocketadmin?ssl_mode=require" \
  -e JWT_SECRET="$(openssl rand -hex 32)" \
  -e PRIVATE_KEY="$(openssl rand -hex 32)" \
  rocketadmin/rocketadmin
```

Open [http://localhost:8080](http://localhost:8080) and log in with the credentials printed to the container logs.
For all environment variables see the [image README](https://github.com/rocket-admin/rocketadmin#environment-variables).

### Kubernetes / Helm

```bash
helm repo add rocketadmin https://charts.rocketadmin.com
helm repo update
helm install my-rocketadmin rocketadmin/rocketadmin
```

Customise via `values.yaml` (replicas, ingress, OpenAI key, SMTP, …) – see [`helm-chart`](https://github.com/rocket-admin/helm-chart) for options.

### Cloud

No infra? Sign up for our Hosted plan at [https://app.rocketadmin.com](https://app.rocketadmin.com) (30‑day free trial).

## 📚 Documentation

* **Docs:** [https://docs.rocketadmin.com](https://docs.rocketadmin.com)
* **Help centre & guides:** [https://help.rocketadmin.com](https://help.rocketadmin.com)

## 💬 Community & Support

* **GitHub Issues** – bug reports & feature requests
* **Discord** – [https://discord.gg/rocketadmin](https://discord.gg/rocketadmin)
* **Email** – [support@rocketadmin.com](mailto:support@rocketadmin.com)

## 🛡️ Security

We follow security best practices, run a coordinated disclosure programme and offer private on-prem deployments for customers with strict compliance needs. Please see [SECURITY.md](./SECURITY.md) for details.

## 🤝 Contributing

1. Fork this repo and create your feature branch (`git checkout -b feature/my-awesome-feature`)
2. Commit your changes (`git commit -m 'feat: add awesome feature'`)
3. Push to the branch (`git push origin feature/my-awesome-feature`)
4. Open a Pull Request

All contributors are expected to follow our [Code of Conduct](./CODE_OF_CONDUCT.md).

## 📅 Roadmap

We keep our product backlog public in the [Discussions](https://github.com/rocket-admin/rocketadmin/discussions) tab. Up‑vote the issues that matter to you!

## ⚖️ License

Rocket Admin is distributed under the **Business Source License 1.1**.
The Change License is **MPL 2.0** and becomes effective four years after each release. See the [LICENSE](https://github.com/rocket-admin/rocketadmin/blob/main/LICENSE) file for details.

---

> Built with ❤️ by the Rocket Admin & Short.io teams – because every app deserves an awesome admin panel.

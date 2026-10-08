

---

## 📄 File 2: `multi-tier-architecture.md`

```markdown
# Multi-Tier Architecture

## What is a Two-Tier Architecture?

A **two-tier architecture** is a software design pattern where an application is divided into two distinct layers or "tiers" that communicate with each other over a network. In cloud and containerized environments, each tier typically runs as its own independent service (container), allowing it to be scaled, updated, and maintained separately.

In this mission, the two tiers are:

1. **The Web/Application Tier** — Nextcloud
2. **The Database Tier** — MariaDB

---

## The Web/Application Tier

**Role:** The web/application tier is the layer that users interact with directly. It is responsible for:

- Serving the **user interface** (HTML, CSS, JavaScript) to the browser.
- Handling **HTTP/HTTPS requests** from clients.
- Executing **business logic** — in this case, Nextcloud's file management, sharing, and user authentication.
- Communicating with the database tier to read and write data.

In our deployment, the **Nextcloud container** acts as this tier. It listens on port `80` inside the container, which is mapped to port `8080` on the host machine so users can access it through a browser.

---

## The Database Tier

**Role:** The database tier is the layer responsible for **persistent data storage**. It is responsible for:

- Storing **user accounts** and authentication credentials.
- Storing **file metadata** (file names, sizes, ownership, sharing permissions).
- Ensuring **data integrity** and consistency through transactions.
- Providing **query responses** to the application tier.

In our deployment, the **MariaDB 10.6 container** acts as this tier. It stores all of Nextcloud's persistent data and is only accessible to the application tier — not directly to end users.

---

## Why Separate Them?

Separating the web server and the database into two containers is better than packing them into one because:

1. **Scalability** — Each tier can be scaled independently. If the application experiences high traffic, you can spin up more Nextcloud containers without duplicating the database.
2. **Security** — The database tier can be isolated on an internal network, so it is not directly exposed to the internet. Only the application tier can communicate with it.
3. **Maintainability & Resilience** — Updates, backups, or failures in one tier do not affect the other. For example, the database can be upgraded or restored without redeploying the web application.

This separation mirrors how real enterprise systems are built — each tier has a single responsibility, making the system more robust, secure, and easier to manage.

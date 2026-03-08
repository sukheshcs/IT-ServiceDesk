<h1 align="center">IT ServiceDesk 🛡️</h1>

<p align="center">
  <strong>A modern, enterprise-grade ITIL-based ticketing and service management solution built for Windows 11.</strong>
</p>

<p align="center">
  <img src="StoreAssets/SuperHeroArt_1920x1080.png" alt="IT ServiceDesk Hero Art" width="100%">
</p>

## 📌 Overview

**IT ServiceDesk** is a powerful desktop application designed to streamline IT support operations. Built with modern UI paradigms like Glassmorphism and Windows 11 Mica materials, it offers a seamless and premium experience for both end-users and IT technicians. From managing incidents and tracking Service Level Agreements (SLAs) to hosting a self-service knowledge base, IT ServiceDesk centralizes your entire IT support workflow.

## ✨ Key Features

*   **Role-Based Access Control:** Secure workspaces specifically designed for Standard Employees, IT Technicians, and System Administrators.
*   **Comprehensive Ticketing:** Full ITIL incident tracking with categories, priority levels, assignments, device context, and resolution history.
*   **Real-Time Dashboards:** Instant insights into ticket volumes, technician workloads, SLA breaches, and unassigned issues.
*   **Knowledge Base Management:** End-users can search troubleshooting guides and self-help articles to reduce incoming ticket volume.
*   **Detailed Analytics & Reporting:** Track key performance metrics and export comprehensive CSV reports for IT audits.
*   **Flexible Deployment:** Supports local SQLite databases for standalone use or shared network drives for team-wide collaboration without complex cloud setups.
*   **Stunning User Interface:** A fluid, premium design using the WinUI 3 framework, featuring immersive backdrop materials, theme transitions, and custom synthesized color palettes.
*   **Multi-Architecture Support:** Optimized AOT (Ahead-of-Time) compilation supporting `x86`, `x64`, and `ARM64` Windows devices natively.

## 🚀 Getting Started

### Prerequisites

*   **OS:** Windows 10 Version 2004 (Build 19041) or higher / Windows 11.
*   **.NET SDK:** .NET 10.0 or later.
*   **IDE:** Visual Studio 2022 (with the .NET desktop development and Universal Windows Platform development workloads).



## ⚙️ Network Database Configuration

Here is how to make the application save your database to a new shared location so that multiple people on your network can access the same live Helpdesk system:

1. **Save Your Settings:** Open the Settings page within the app, enter your new path (e.g., `\\Sharedserver\sharedfolder`), scroll down, and click the **Save Settings** button. This will successfully write your new path to the application's configuration file.
2. **Restart the Application:** Close the IT ServiceDesk application completely and open it again.
3. **What happens next depends on what you want to do:**
   * **Option A (Start fresh):** If you just want a completely brand new, empty database for your network to share, you don't need to do anything else! As soon as the app re-opens, it will automatically detect the new path and generate a fresh `ServiceDeskAI360.db` file right there in your `\\Sharedserver\sharedfolder`.
   * **Option B (Keep your existing tickets/users):** If you want to move the tickets and test users you've already created over to the network, you need to manually copy your existing database file *before* you reopen the app.
     1. Open Windows File Explorer and type `%LocalAppData%` into the top address bar.
     2. Find the existing `ServiceDeskAI360.db` file.
     3. Copy and paste that file directly into your `\\sharedserver\sharefolder` path.
     4. Now, when you re-open the app, it will read your old data from the new network location!

Once the `.db` file is living in that shared folder, anyone else on your network who installs the app just needs to type that exact same path into their Settings page, and you will all be instantly connected to the same live Helpdesk system!

## 🛠️ Technology Stack

*   **Framework:** .NET 10.0
*   **UI Toolkit:** WinUI 3 (Windows App SDK)
*   **Architecture Pattern:** MVVM (Model-View-ViewModel) via `CommunityToolkit.Mvvm`
*   **Database:** SQLite (Entity Framework Core)
*   **Packaging:** MSIX

## 📂 Project Structure

*   `/Views` - Contains all XAML UI definitions (Dashboard, Tickets, Settings, etc.).
*   `/ViewModels` - Contains the business logic and state management for each view.
*   `/Models` - Contains the Entity Framework Core data models (Ticket, User, Category).
*   `/Services` - Contains isolated services for Database access, Dialog management, and specific business needs.
*   `/Assets` & `/StoreAssets` - Contains the application icons, splash screens, and Microsoft Store promotional imagery.

## 🤝 Contributing

Contributions, issues, and feature requests are welcome!
Feel free to check the [issues page](https://github.com/yourusername/IT-ServiceDesk/issues).

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---
<p align="center">Developed with ❤️ by the IT ServiceDesk Team</p>

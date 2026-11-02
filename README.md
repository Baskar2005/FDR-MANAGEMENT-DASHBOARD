# FDR Sentinel

### Fixed Deposit Receipt and Security Deposit Management Dashboard

FDR Sentinel is a browser-based prototype for organizing and monitoring Fixed Deposit Receipts (FDRs) and security deposits submitted by AICTE-approved institutions. It brings the main stages of the FDR lifecycle into one dashboard: recording submissions, reviewing verification status, tracking maturity dates, and monitoring renewal and release requests.

> **Project demonstration:** [Open FDR Sentinel](https://baskar2005.github.io/FDR-MANAGEMENT-DASHBOARD/)

The project is designed to demonstrate a clear administrative workflow using sample data. It does not connect to live AICTE or bank systems and must not be used to authorize financial transactions.

## The problem

FDR information may be submitted and maintained across separate documents and manual processes. This makes it harder for administrators to get a consistent view of each instrument, identify approaching maturity dates, follow up on pending checks, and keep a clear history of decisions.

## The proposed solution

FDR Sentinel presents FDR records and their review status in a centralized dashboard. Administrators can use the prototype to review sample submissions, search and filter the register, monitor upcoming maturity dates, and follow simulated verification, clearance, renewal, and release workflows.

## Main capabilities

- **Portfolio overview:** Summary cards, status distribution, institution exposure, and maturity schedule.
- **FDR register:** Search, filter, inspect, and add sample records.
- **Institution view:** Review FDR totals and pending items by institution.
- **Verification queue:** Identify records awaiting review and record a simulated verification action.
- **Clearance workflow:** Demonstrate progression through review stages.
- **Maturity monitoring:** Identify upcoming or past maturity dates and record a simulated renewal.
- **Release requests:** Demonstrate a structured release/refund request and review status.
- **Alerts and audit history:** Review sample notifications and a log of actions taken in the demo.
- **CSV export:** Download the displayed FDR register for reporting demonstrations.

## Demonstration workflow

1. Review the portfolio summary and identify pending or expiring items.
2. Search or filter the FDR register to find an institution or instrument.
3. Open a record and review its submitted details and current status.
4. Demonstrate a verification, clearance, renewal, or release action.
5. Review the resulting status, notification, and audit history.
6. Export the sample register as CSV if a report is needed.

## Technology

- HTML for the dashboard structure
- CSS for responsive layout and visual presentation
- JavaScript for sample records, dashboard rendering, filters, workflows, charts, and CSV export
- Browser `localStorage` for persistence between page reloads in the same browser

The prototype runs as a static website. It requires no build tools, package installation, backend server, or database.

## Run locally

1. Clone the repository:

   ```bash
   git clone https://github.com/Baskar2005/FDR-MANAGEMENT-DASHBOARD.git
   ```

2. Open `index.html` in a current browser, or serve the repository directory using any static web server.

The demonstration data is stored in browser `localStorage`. To reset it, clear the site's local storage in browser developer tools and reload the page.

## Deployment

GitHub Pages deployment is configured through the workflow in `.github/workflows/deploy-pages.yml`. Each push to the `main` branch builds and publishes the static project.

To enable deployment in the repository:

1. Open **Settings → Pages** on GitHub.
2. Set the build and deployment source to **GitHub Actions**.
3. Push a change to `main` or run the **Deploy FDR Sentinel to GitHub Pages** workflow from the **Actions** tab.
4. After the workflow succeeds, open the project demonstration link above.

## Scope and limitations

This is a functional demonstration, not a production financial-management system.

- All records are synthetic sample data; do not enter confidential or real financial information.
- Verification, approval, release, notifications, and institutional actions are simulated. No live bank or AICTE verification is performed.
- A PDF or user-entered record is not independently authenticated by this prototype.
- Browser storage is local to the browser and is not a shared or protected institutional database.
- Authentication, role-based permissions, server-side audit storage, encrypted document storage, and live integrations are not implemented.
- Demo approvals do not authorize a bank transfer or release of funds.

## Future scope

With appropriate institutional authorization and security review, future versions could add authenticated user roles, protected centralized storage, secure document handling, independently verified bank responses, configurable reminders, and production audit controls.

## Project presentation

**Short judge-facing summary:**
“FDR Sentinel is a centralized dashboard prototype for tracking institutional Fixed Deposit Receipts from submission through verification, maturity, renewal, and release review. It gives administrators a consolidated view of sample records, pending actions, and upcoming expirations. The demonstration uses synthetic data and simulated workflows; live financial verification and production security controls are outside its current scope.”

## License

This project is distributed under the MIT License. See [LICENSE](LICENSE).

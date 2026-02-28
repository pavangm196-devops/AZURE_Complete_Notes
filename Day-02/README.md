
##   ***CLOUD SERVICE MODELS & AZURE ACCOUNT SETUP 🚀***

***1. THE THREE PILLARS OF CLOUD SERVICES 🏗️***
In the cloud, you don't always have to manage everything. Depending on your needs, you choose a "Service Model."

**A. IaaS** (Infrastructure as a Service)
What it is: You rent the "raw" hardware (Virtual Machines, Storage, Networking).

You Manage: The Operating System (Windows/Linux), Middleware, Runtime, Data, and Apps.

Azure Manages: The physical servers, virtualization layer, and networking cables.

Best For: Migrating existing applications from your office to the cloud.

Analogy: Renting a House. The landlord provides the structure, but you bring your own furniture and do the cleaning.

**B. PaaS** (Platform as a Service)
What it is: A platform where you just upload your code. You don't care about the OS or patching.

You Manage: Only the Application and Data.

Azure Manages: Everything else (OS, Middleware, Runtime, Hardware).

Best For: Developers who want to focus on coding, not server maintenance.

Analogy: Staying in a Hotel. You don't clean the room or fix the plumbing; you just stay there and use the facilities.

**C. SaaS** (Software as a Service)
What it is: Fully functional software delivered over the web.

You Manage: Only the users and settings.

Azure Manages: Everything (The App, Data, OS, Hardware).

Best For: Standard business tools.

Analogy: Dining in a Restaurant. You just sit down and eat. You don't cook or wash dishes.

## ***2. SHARED RESPONSIBILITY COMPARISON 🤝***

Feature	On-Premises	IaaS	PaaS	SaaS

Physical Data Center	You	Azure	Azure	Azure

Networking/Firewalls	You	Azure	Azure	Azure

Operating System	You	You	Azure	Azure

Applications	You	You	You	Azure

Data & Access	You	You	You	You

Crucial Note: No matter which model you pick, Data and Access (Identity) are ALWAYS your responsibility!

 ## ***3. SETTING UP YOUR AZURE FREE ACCOUNT 🛠️***
To start the hands-on labs, you need an Azure account. Microsoft offers a Free Trial:

$200 Credit: For the first 30 days (to explore any service).

12 Months Free: Popular services (like specific VM sizes and SQL databases).

Always Free: 55+ services (like Azure Functions and Active Directory).

Requirements for Signup:
Microsoft Account: (Outlook/Hotmail/Gmail).

Phone Number: For verification.

Credit/Debit Card: For identity verification only. Azure will NOT charge you unless you manually upgrade to "Pay-As-You-Go."

## ***4. AZURE SUBSCRIPTIONS & TENANTS 📂***

Tenant (Azure AD/Entra ID): Represents your organization (e.g., yourname.onmicrosoft.com).

**Subscription:** The "Billing Meter." You can have multiple subscriptions under one tenant (e.g., one for Dev, one for Production).

**Management Groups:** Used to manage multiple subscriptions at once.

##  ***5. KEY TAKEAWAYS FROM DAY 02 💡***
Use IaaS when you need total control over the OS.

Use PaaS to deploy apps quickly without managing servers.

Use SaaS for ready-to-use software (like Office 365).

Always set up Budget Alerts in your free account to avoid unexpected costs.

personal-finance-tracker/
├── README.md                      # Root project instructions
├── .gitignore                    # Common ignores for Flutter, Node, CDK
├── infra/                        # AWS CDK infrastructure as code
│   ├── bin/
│   │   └── infra.ts              # CDK app entry point
│   ├── lib/
│   │   └── infra-stack.ts        # Define Lambda, API Gateway, DynamoDB
│   ├── cdk.json
│   └── package.json              # CDK dependencies
├── backend/                      # Node.js Lambda handlers
│   ├── src/
│   │   ├── expenses.ts           # Lambda for expenses
│   │   ├── summary.ts            # Lambda for summary endpoints
│   ├── package.json
│   └── tsconfig.json
├── frontend/                     # Flutter project (mobile/web/macos)
│   ├── lib/
│   │   ├── main.dart             # Flutter app entry point
│   │   ├── models/
│   │   ├── services/
│   │   └── screens/
│   ├── android/
│   ├── ios/
│   ├── macos/
│   ├── pubspec.yaml
│   └── analysis_options.yaml
├── scripts/                      # Optional helper scripts
│   └── local-dev.sh              # Script to run local backend and frontend
└── Makefile                      # Optional: `make run`, `make deploy` etc.

---

# 💸 Personal Finance Tracker

A cross-platform personal finance tracker that helps you track expenses, income, credit card transactions, and visualize budgets. Built with Flutter, AWS Lambda, API Gateway, and DynamoDB. Infrastructure managed via AWS CDK.

---

## 🧱 Folder Structure

| Folder      | Description |
|-------------|-------------|
| `frontend/` | Flutter app for Android, iOS, macOS, and Web |
| `backend/`  | Node.js-based AWS Lambda functions |
| `infra/`    | AWS CDK code to deploy API Gateway, Lambda, DynamoDB |
| `scripts/`  | Helper scripts for development |
| `Makefile`  | Optional commands to automate dev/deploy |

---

## 🚀 Getting Started

### 1. Clone the Repository
```bash
git clone https://github.com/yourname/personal-finance-tracker.git
cd personal-finance-tracker
```

### 2. Install Dependencies

#### CDK Infra
```bash
cd infra
npm install
```

#### Backend Lambdas
```bash
cd ../backend
npm install
```

#### Flutter Frontend
```bash
cd ../frontend
flutter pub get
```

---

## 🌐 Running Locally

### Start Local Flutter App
```bash
cd frontend
flutter run
```

### Deploy Backend (Lambda + API Gateway + DynamoDB)
```bash
cd infra
cdk deploy
```

> 💡 You must have AWS CLI configured and bootstrapped for CDK.

---

## ⚙️ Technologies Used

- **Frontend**: Flutter (Material Design)
- **Backend**: Node.js (AWS Lambda)
- **Database**: DynamoDB (On-Demand mode)
- **Infra as Code**: AWS CDK (TypeScript)

---

## 📊 Features

- Add & track income/expenses
- Tag transactions
- Credit card handling & mapping
- Visual dashboard (charts, filters, slicers)
- Monthly summaries & budget limits
- macOS, Android, iOS from single Flutter codebase

---

## 📦 Deployment Targets

- Flutter app: Android, iOS, macOS
- Backend: AWS Lambda via CDK
- Database: DynamoDB

---

## 📌 TODO (Planned)

- Add user authentication (AWS Cognito)
- Add notifications/reminders
- Add recurring transaction support
- Export reports to PDF/CSV
- Web frontend hosting (optional)

---

## 📄 License

MIT License © 2025 Your Name

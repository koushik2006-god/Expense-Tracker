# Expense Tracker Web Application

A comprehensive full-stack expense tracking application designed for both college students and office workers. Built with React, TypeScript, Tailwind CSS, and Supabase.

## Features

### Core Features
- **User Authentication**: Secure email/password authentication with Supabase
- **User Types**: Separate category presets for students and professionals
- **Dashboard**: Real-time overview of total balance, income, and expenses
- **Transaction Management**: Add, edit, and delete transactions
- **Smart Categorization**:
  - Students: Tuition, books, accommodation, food, etc.
  - Professionals: Salary, rent, bills, utilities, etc.
- **Date Tracking**: Record transactions with specific dates
- **Search & Filter**: Filter by date range (today, week, month) and transaction type
- **Data Visualization**: Visual expense breakdown by category
- **Budget Limits**: Set monthly budgets per category with customizable alerts
- **Export Data**: Download transaction history as CSV
- **Dark Mode**: Toggle between light and dark themes
- **Responsive Design**: Mobile-friendly interface

### Student Categories
**Income**: Scholarship, Part-time Job, Allowance, Gift
**Expenses**: Tuition Fees, Books & Supplies, Food & Dining, Transportation, Accommodation, Entertainment, Shopping, Health

### Professional Categories
**Income**: Salary, Bonus, Freelance, Investment, Gift
**Expenses**: Rent, Utilities, Groceries, Transportation, Dining Out, Shopping, Entertainment, Healthcare, Insurance, Bills, Subscriptions, Travel

## Technology Stack

### Frontend
- React 18 with TypeScript
- Tailwind CSS for styling
- Lucide React for icons
- Vite for build tooling

### Backend
- Supabase (PostgreSQL database)
- Supabase Auth for authentication
- Row Level Security (RLS) for data protection

## Project Structure

```
src/
├── components/
│   ├── Auth/
│   │   ├── Login.tsx
│   │   └── Register.tsx
│   └── Dashboard/
│       ├── Dashboard.tsx
│       ├── Header.tsx
│       ├── SummaryCards.tsx
│       ├── TransactionModal.tsx
│       ├── TransactionList.tsx
│       ├── FilterBar.tsx
│       ├── Charts.tsx
│       └── BudgetAlerts.tsx
├── contexts/
│   └── AuthContext.tsx
├── lib/
│   └── supabase.ts
├── utils/
│   └── categories.ts
├── App.tsx
└── main.tsx
```

## Database Schema

### Tables
1. **user_profiles**: Stores user preferences (type, theme, currency)
2. **transactions**: Stores all income and expense records
3. **budgets**: Stores monthly budget limits per category

All tables have Row Level Security enabled to ensure users can only access their own data.

## Getting Started

### Prerequisites
- Node.js 18+ installed
- A Supabase account and project

### Installation

1. Install dependencies:
```bash
npm install
```

2. Configure Supabase:
   - The `.env` file already contains your Supabase credentials
   - The database schema has been automatically set up

3. Run the development server:
```bash
npm run dev
```

4. Build for production:
```bash
npm run build
```

## Usage Guide

### First Time Setup
1. **Register**: Create an account and select your user type (Student or Professional)
2. **Add Transaction**: Click "Add Transaction" to record your first income or expense
3. **Set Budgets**: Navigate to the budget section to set monthly spending limits
4. **Explore**: Use filters to view transactions by period and type

### Daily Use
1. **Track Expenses**: Quickly add expenses with category, amount, and date
2. **Monitor Budget**: Check budget alerts to stay within limits
3. **Analyze Spending**: View visual breakdown of expenses by category
4. **Export Data**: Download your transaction history for external analysis

### Features Walkthrough

#### Adding Transactions
- Click "Add Transaction" button
- Select income or expense
- Choose appropriate category
- Enter amount and description
- Select date
- Click "Add Transaction"

#### Setting Budgets
- Scroll to "Monthly Budgets" section
- Click "Add Budget"
- Select category
- Set monthly limit amount
- Set alert threshold percentage (e.g., 80%)
- Visual indicators show budget usage status

#### Filtering Transactions
- Use the search bar to find specific transactions
- Filter by period: All Time, Today, This Week, This Month
- Filter by type: All, Income Only, Expense Only

#### Exporting Data
- Click "Export CSV" button
- CSV file downloads with all filtered transactions
- Open in Excel, Google Sheets, or any spreadsheet application

## Security Features

- Email/password authentication
- Row Level Security (RLS) on all database tables
- User data isolation (users can only access their own data)
- Secure session management
- Environment variable protection

## Deployment

### Frontend (Netlify)
1. Connect your repository to Netlify
2. Add environment variables in Netlify dashboard
3. Deploy

### Backend
The backend is already deployed on Supabase. No additional deployment needed.

## Support

For issues or questions, please check:
- Supabase documentation: https://supabase.com/docs
- React documentation: https://react.dev
- Tailwind CSS documentation: https://tailwindcss.com

## License

This project is open source and available for personal and educational use.

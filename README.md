# Dynamic Data Table Manager

A comprehensive data table management application built with Next.js 14, Redux Toolkit, and Material UI.

## Features

### Core Features
- **Table View**: Display data with Name, Email, Age, Role columns
- **Sorting**: Click column headers to sort (ASC/DESC toggle)
- **Global Search**: Search across all fields
- **Pagination**: Client-side pagination (10 rows per page)

### Dynamic Columns
- **Manage Columns Modal**: Add new fields like Department, Location
- **Show/Hide Columns**: Toggle column visibility with checkboxes
- **Persistent Settings**: Column visibility saved in localStorage

### Import & Export
- **CSV Import**: Upload and parse CSV files with error handling
- **CSV Export**: Export current table view to CSV (visible columns only)

### Bonus Features
- **Inline Editing**: Double-click to edit fields inline
- **Input Validation**: Age must be a number
- **Row Actions**: Edit and Delete with confirmation
- **Responsive Design**: Works on all screen sizes

## Tech Stack

- **React 18** / **Next.js 14** (App Router)
- **Redux Toolkit** for state management
- **Material UI (v5+)** for components
- **TypeScript** for type safety
- **PapaParse** for CSV parsing
- **FileSaver.js** for CSV export
- **Redux Persist** for localStorage persistence

## Getting Started

1. Install dependencies:
```bash
npm install
```

2. Run the development server:
```bash
npm run dev
```

3. Open [http://localhost:3000](http://localhost:3000) in your browser.

## Usage

### Managing Columns
1. Click "Manage Columns" button
2. Use checkboxes to show/hide columns
3. Add new columns by typing a name and clicking "Add"

### Importing Data
1. Click "Import CSV" button
2. Select a CSV file with headers matching table columns
3. Data will be added to the existing table

### Exporting Data
1. Click "Export CSV" button
2. Only visible columns will be included in the export
3. Current search/filter results will be exported

### Inline Editing
1. Click the edit icon next to any row
2. Click on any cell to edit inline
3. Press Enter or click outside to save
4. Use "Save All" or "Cancel All" for bulk operations

## Project Structure

```
src/
├── app/
│   ├── layout.tsx          # Root layout with providers
│   └── page.tsx            # Main page component
├── components/
│   ├── DataTable.tsx       # Main table component
│   ├── EditableCell.tsx    # Inline editing component
│   └── ManageColumnsModal.tsx # Column management modal
├── store/
│   ├── store.ts            # Redux store configuration
│   └── tableSlice.ts       # Table state management
├── types/
│   └── index.ts            # TypeScript interfaces
└── utils/
    ├── csvUtils.ts         # CSV import/export utilities
    └── theme.ts            # MUI theme configuration
```
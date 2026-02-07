# Admin Dashboard 

The Admin Dashboard is a Flutter-based application designed for store administrators to manage the ApnaMart platform efficiently. It provides tools for product management, order processing, and sales analytics.

## Features

*   **Dashboard Overview:** View key metrics and sales charts.
*   **Product Management:** Add, edit, and delete products with ease.
*   **Image Uploads:** Upload product images directly to Firebase Storage.
*   **Order Management:** Track and update the status of customer orders.
*   **Analytics:** Visual implementation of sales data using charts.

## Tech Stack & Key Dependencies

*   **SDK:** Flutter (Designed for Flutter 3.x)
*   **State Management:** Flutter Riverpod
*   **Backend:** Firebase (Core, Auth, Firestore, Storage)
*   **Navigation:** Routemaster
*   **Charting:** `fl_chart` for data visualization
*   **Utilities:** `fpdart`, `uuid`, `intl`

## Setup Instructions

1.  **Install Dependencies:**
    Navigate to the `AdminApp` directory and run:
    ```bash
    flutter pub get
    ```

2.  **Firebase Configuration:**
    *   This app connects to the same Firebase project as the Customer App.
    *   Add `google-services.json` (for Android) to `android/app/`.
    *   Add `GoogleService-Info.plist` (for iOS) to `ios/Runner/`.
    *   Ensure Firestore security rules allow admin access as configured in your backend.

3.  **Run the App:**
    ```bash
    flutter run
    ```

## Notes

*   This app focuses on administrative tasks and assumes an authenticated admin user (setup via Firebase Auth directly or a seed script is recommended for the first admin).

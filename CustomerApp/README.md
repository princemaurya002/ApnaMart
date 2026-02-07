This is the customer-facing mobile application, architected to support any retail vertical.

**Current Context:** The app is tailored for a **Pharmacy** experience, allowing users to browse medicines, upload prescriptions, and order health essentials.

## Features (Pharmacy Edition)

*   **Medicine & Product Browsing:** Detailed catalogs with categories like 'Prescription Drugs', 'OTC', 'Wellness', etc.
*   **Smart Search:** Find medicines by name, generic composition, or ailment.
*   **Prescription Upload:** Securely upload doctor's prescriptions for order verification.
*   **Health Dashboard:** Track health metrics or subscription refills (if enabled).
*   **Secure Authentication:** User sign-up and login powered by Firebase Auth.
*   **Shopping Cart:** Add items, view dosage instructions (if applicable), and checkout.
*   **Checkout & Payments:** Integration with **Stripe** and **PayPal** for secure transactions.
*   **Order History:** Track medicine delivery status and view past purchases.
*   **User Profile:** Manage delivery addresses and saved health info.
*   **Local Storage:** Uses Hive for efficient local data caching and offline access.

## Tech Stack & Key Dependencies

*   **SDK:** Flutter (Compatible with version `<3.0.0` as per `pubspec.yaml`)
*   **State Management:** Flutter Riverpod & GetX
*   **Backend:** Firebase (Core, Auth, Firestore, Storage)
*   **Navigation:** Routemaster
*   **Payments:** `flutter_stripe`, `flutter_paypal`, `flutter_paypal_checkout`
*   **Utilities:** `fpdart`, `flutter_dotenv`, `http`, `uuid`
*   **UI Components:** `fluttertoast`, `dotted_line`, `flutter_dash`

## Setup Instructions

1.  **Install Dependencies:**
    Navigate to the `CustomerApp` directory and run:
    ```bash
    flutter pub get
    ```

2.  **Environment Variables:**
    This project uses `flutter_dotenv`. Ensure you have a `.env` file in the root of `CustomerApp` with necessary API keys (e.g., Stripe keys, Base URLs).
    *Example `.env` structure:*
    ```env
    STRIPE_PUBLISHABLE_KEY=pk_test_...
    STRIPE_SECRET_KEY=sk_test_...
    ```

3.  **Firebase Configuration:**
    *   Ensure you have a Firebase project set up.
    *   Add `google-services.json` (for Android) to `android/app/`.
    *   Add `GoogleService-Info.plist` (for iOS) to `ios/Runner/`.

4.  **Run the App:**
    ```bash
    flutter run
    ```

## Notes

*   Ensure specific platform configurations (Android `minSdkVersion`, iOS Podfile settings) are met for payment gateway integrations.

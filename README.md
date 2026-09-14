# 🛒 Dynamic Product Listing & Filtering App

A modern, responsive Flutter application demonstrating dynamic product rendering using `ListView.builder`, ephemeral state management with `setState`, real-time search, and category-based filtering workflows.

---

## 📸 Overview

This application showcases a real-world product catalog interface with interactive features including:

* **Dynamic Data Modeling**: A structured `Product` data model isolating application logic from the UI layout.


* **Real-Time Search**: Instant filtering that evaluates string matching across search queries.


* **Category Filtering**: Horizontal interactive filter chips extracted dynamically from the dataset's categories (e.g., Electronics, Apparel).


* **INR (₹) Currency Formatting**: Styled pricing displayed in Indian Rupees without decimal padding.


* **Custom Empty State**: A modern visual indicator that renders when no products match the selected search or filter criteria.



---

## 📁 Project Architecture & File Organization

The application adheres to a clean separation of concerns, isolating the application configuration and interactive UI from the underlying data model:

```plaintext
lib/
├── main.dart       # Application Entry Point, Material App Theme & Interactive UI Screen
└── product.dart    # Product Data Model Class & In-Memory Sample Dataset

```

---

## 🛠️ Features Breakdown

### 1. Product Data Model (`product.dart`)

* Defines the core `Product` model containing strictly typed attributes: `id`, `name`, `category`, `price`, `icon`, and `themeColor`.


* Provides an in-memory sample product array utilized for dynamic rendering pipelines.



### 2. State Management & Logic (`main.dart`)

* Maintains local reactive state lifecycle via `setState()` to update the `_filteredProducts` list when search queries or filters change.


* Utilizes a `TextEditingController` to capture real-time text input queries, featuring a dynamic clear (X) control.



### 3. Responsive Material 3 UI

* Replaces default app bars with custom header components featuring dynamic titles and subtitles.


* Employs `ListView.builder` for highly efficient virtualized rendering of both horizontal category chips and vertical product items.


* Leverages `AnimatedContainer` for smooth selection states, borders, and active shadows on category pills.



---

## 🚀 Getting Started

### Prerequisites

* [Flutter SDK](https://docs.flutter.dev/get-started/install?utm_source=gemini) installed.
* Dart SDK installed.
* An IDE such as VS Code or Android Studio with Flutter extensions.

### Installation & Run

1. **Clone the repository:**
```bash
git clone <repository-url>
cd modern_store

```


2. **Fetch dependencies:**
```bash
flutter pub get

```


3. **Run the app:**
```bash
flutter run

```



---

## 💻 Tech Stack

* **Framework:** Flutter (Material 3 enabled)
* **Language:** Dart
* **State Management:** Ephemeral State (`StatefulWidget` / `setState`)
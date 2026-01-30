# CareerNode — Job Search Portal (React)

CareerNode is a responsive job aggregator application built to streamline job search and application workflows. This project demonstrates dynamic data filtering, client-side route guarding, and robust API response handling.

### 🔑 Demo Credentials
*Use these mock credentials to evaluate the protected routes:*
- **Username:** `rahul` 
- **Password:** `rahul@2021`

---
## 🚀 Key Features

* **Secure Access Control:** Implemented client-side route guarding and JWT-based persistent login sessions.
* **Dynamic Data Filtering:** Integrated with **RESTful APIs** to filter listings by salary ranges, employment types, and search queries.
* **Managed UI States:** Developed specific UI handlers for **Loading**, **Success**, and **Failure** responses, including integrated retry logic.
* **Responsive Design:** Built with a mobile-first approach using Styled Components for a consistent experience across all devices.
* **Deep Linking:** Implemented dynamic URL query parameter construction to ensure search results remain consistent across page refreshes.

## 🛠️ Tech Stack

* **Frontend:** React.js, React Router, Styled Components
* **State Management:** Component-level state & Props
* **Icons:** React Icons (BsSearch, MdLocationOn, etc.)
* **Data Integration:** RESTful APIs, JSON Web Tokens (JWT)

---

## 📂 Application Structure

The application is structured into modular components to ensure maintainability and clear separation of concerns:



* **App.js:** Configures public and protected routes via React Router.
* **Jobs Dashboard:** Manages search inputs, multi-select filter groups, and the main job listing feed.
* **JobItemDetails:** Handles data fetching for individual listings and similar job recommendations.
* **Authentication Logic:** Handles session validation and client-side redirect logic.

---

## ⚙️ Setup & Installation

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/amsanthosht/CareerNode.git](https://github.com/amsanthosht/CareerNode.git)
    ```
2.  **Install dependencies:**
    ```bash
    npm install
    ```
3.  **Start the development server:**
    ```bash
    npm start
    ```

---

## 📝 Technical Implementation Details

### Data Fetching Strategy
The portal utilizes dynamic URL construction for API requests. Filters are managed as query parameters to keep the UI in sync with the data layer:
```javascript
// Example of a multi-filter API call construction
const apiUrl = `https://apis.ccbp.in/jobs?employment_type=${selectedTypes}&minimum_package=${minSalary}&search=${searchText}`;

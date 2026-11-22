<<<<<<< HEAD
# DearFSD – Full Stack Development Lab

A collection of practical experiments and applications developed as part of the Full Stack Development Lab.

## ⚡ Step-by-Step Fast Deployment Guide (For Friends & Classmates)

### 📌 Step 1: Get the Code to Your Own GitHub

Choose either **Option A** or **Option B**:

* **Option A (The Fork Method – 5 Seconds, Fastest):**
  1. Open [https://github.com/Mahe13185/DearFSD](https://github.com/Mahe13185/DearFSD).
  2. Click the **Fork** button (top right) → **Create fork**.
  3. You now have the repo at: `https://github.com/<YOUR-USERNAME>/DearFSD`.
  *(Note: It will say "forked from Mahe13185/DearFSD" on your GitHub).*

* **Option B (Clone & Upload as a Fresh Repo – No "Forked From" Tag):**
  1. Create a new empty repository on your GitHub (e.g. `DearFSD`).
  2. In your computer's terminal:
     ```bash
     git clone https://github.com/Mahe13185/DearFSD.git
     cd DearFSD
     git remote set-url origin https://github.com/<YOUR-USERNAME>/DearFSD.git
     git push -u origin main
     ```

---

### ⚡ Step 2: Deploy All 10 React Frontend Apps to Vercel (Local Terminal / VS Code)

Now that you have your repository on GitHub:

1. **Open VS Code (or Terminal) on your computer** and clone your repository:
   ```bash
   git clone https://github.com/<YOUR-USERNAME>/DearFSD.git
   cd DearFSD
   ```
2. **Log into Vercel CLI (Required first time):**
   ```bash
   npm run login:vercel
   ```
   *(Choose **Continue with GitHub** or Email and approve in the browser).*

3. **Run the automated deploy command in that terminal:**
   ```bash
   npm run deploy:vercel
   ```
   * It will automatically build and deploy all 10 React applications to your Vercel account.
   * It will automatically update your local `README.md` with your personal live URLs.
   * It will display your live projects table (`npx vercel project ls`) in the terminal.

4. **Command to view all your live Vercel links anytime:**
   ```bash
   npx vercel project ls
   ```

> [!TIP]
> **Switching Vercel Accounts:** If your computer is already logged into another Vercel account and you want to deploy to your own or your friend's account, run:
> ```bash
> npm run logout:vercel
> npm run login:vercel
> ```

---

### 🌐 Step 3: Deploy All Backend Services to Render (1-Click Blueprint)

1. Open [dashboard.render.com](https://dashboard.render.com) (sign in with your GitHub).
2. Click **New +** → **Blueprint**.
3. Select your repository: **`DearFSD`**.
4. Render will read `render.yaml` and configure all 7 backend web services automatically.
5. Click **Apply**. Render will build and deploy all 7 services in parallel.

#### 📌 Where to Find YOUR Own Live Render Links:
On Render, each account receives its own unique URLs (Render automatically appends a short unique identifier, e.g. `-xxxx.onrender.com`):
1. In your **[Render Dashboard](https://dashboard.render.com)**, click on your **`DearFSD`** Blueprint group.
2. All 7 services are listed in a table, with each service's **own live `.onrender.com` URL** displayed right under its name!
3. Click on any service to copy your personal live URL or test its endpoints.

---

### 💻 Step 4: In Case Sir Asks for Terminal cURL Commands (CRUD Testing)

> [!TIP]
> If your instructor asks you to execute **cURL commands in the terminal** to demonstrate CRUD operations directly, use the commands below.
> 
> *Replace `<YOUR-FILE-PERSISTENT-DOMAIN-URL>` with your own Render domain from Step 3 (e.g. `file-persistent-app.onrender.com` or `file-persistent-app-xxxx.onrender.com`).*

#### 📁 Faculty File Persistence API (`/api/v1/faculty`)
*Demonstrates File-based JSON persistence (`fs.readFileSync` / `fs.writeFileSync`) in Node.js & Express.*

| Operation | HTTP Method | Endpoint | Purpose |
|---|:---:|---|---|
| **Create** | `POST` | `/api/v1/faculty` | Add a new faculty member |
| **Read All** | `GET` | `/api/v1/faculty` | Retrieve all faculty records |
| **Read by ID** | `GET` | `/api/v1/faculty/:id` | Fetch specific faculty by ID |
| **Update** | `PUT` | `/api/v1/faculty/:id` | Modify faculty details |
| **Delete** | `DELETE` | `/api/v1/faculty/:id` | Remove faculty record |

##### 1. CREATE — Add New Faculty (POST):
```bash
curl -X POST https://<YOUR-FILE-PERSISTENT-DOMAIN-URL>/api/v1/faculty -H "Content-Type: application/json" -d '{"id":3,"name":"Dr.Kumar","department":"CSE","subject":"Java"}'
```

##### 2. READ ALL — Get All Faculty (GET):
```bash
curl -X GET https://<YOUR-FILE-PERSISTENT-DOMAIN-URL>/api/v1/faculty
```

##### 3. READ BY ID — Get Faculty by ID (GET):
```bash
curl -X GET https://<YOUR-FILE-PERSISTENT-DOMAIN-URL>/api/v1/faculty/3
```

##### 4. UPDATE — Modify Faculty by ID (PUT):
```bash
curl -X PUT https://<YOUR-FILE-PERSISTENT-DOMAIN-URL>/api/v1/faculty/3 -H "Content-Type: application/json" -d '{"name":"Dr.Kumar","department":"AI & DS","subject":"Python"}'
```

##### 5. DELETE — Remove Faculty by ID (DELETE):
```bash
curl -X DELETE https://<YOUR-FILE-PERSISTENT-DOMAIN-URL>/api/v1/faculty/3
```

---

## 🌐 Reference Live Demos (Deployed by Mahendra Gampala)

> [!NOTE]
> The links below are live reference deployments created by the author for testing and previewing. When you deploy via the steps above, your own links will be generated in your Vercel and Render dashboards.

### React Frontend Applications (Vercel)

| No. | Experiment Name | Live Demo | Deploy to Your Vercel | Status |
|---:|---|---|:---:|:---:|
| 1 | React Conditional Rendering | [Live Demo](https://react-conditional-rendering-mocha.vercel.app/) | [![Deploy](https://vercel.com/button)](https://vercel.com/new/clone?repository-url=https%3A%2F%2Fgithub.com%2FMahe13185%2FDearFSD&project-name=react-conditional-rendering&root-directory=react-conditional-rendering-app%2Freact-conditional-rendering-app-main) | ✅ Live |
| 2 | React Form Events | [Live Demo](https://react-form-events-drab.vercel.app/) | [![Deploy](https://vercel.com/button)](https://vercel.com/new/clone?repository-url=https%3A%2F%2Fgithub.com%2FMahe13185%2FDearFSD&project-name=react-form-events&root-directory=react-form-events-app%2Freact-form-events-app-main) | ✅ Live |
| 3 | React Frontend CRUD | [Live Demo](https://react-frontend-crud-rho.vercel.app/) | [![Deploy](https://vercel.com/button)](https://vercel.com/new/clone?repository-url=https%3A%2F%2Fgithub.com%2FMahe13185%2FDearFSD&project-name=react-frontend-crud&root-directory=react-frontend-crud-app%2Freact-frontend-crud-app-main) | ✅ Live |
| 4 | React HTML Render | [Live Demo](https://react-html-render-gamma.vercel.app/) | [![Deploy](https://vercel.com/button)](https://vercel.com/new/clone?repository-url=https%3A%2F%2Fgithub.com%2FMahe13185%2FDearFSD&project-name=react-html-render&root-directory=react_html_render_app%2Freact_html_render_app) | ✅ Live |
| 5 | React JSX Render | [Live Demo](https://react-jsx-render.vercel.app/) | [![Deploy](https://vercel.com/button)](https://vercel.com/new/clone?repository-url=https%3A%2F%2Fgithub.com%2FMahe13185%2FDearFSD&project-name=react-jsx-render&root-directory=react_jsx_render_app%2Freact_jsx_render_app) | ✅ Live |
| 6 | React Nested Components | [Live Demo](https://react-nested-components-two.vercel.app/) | [![Deploy](https://vercel.com/button)](https://vercel.com/new/clone?repository-url=https%3A%2F%2Fgithub.com%2FMahe13185%2FDearFSD&project-name=react-nested-components&root-directory=react_multiple_components%2Freact_multiple_components) | ✅ Live |
| 7 | React Rendering Lists | [Live Demo](https://react-rendering-lists-bay.vercel.app/) | [![Deploy](https://vercel.com/button)](https://vercel.com/new/clone?repository-url=https%3A%2F%2Fgithub.com%2FMahe13185%2FDearFSD&project-name=react-rendering-lists&root-directory=react-rendering-lists-app%2Freact-rendering-lists-app-main) | ✅ Live |
| 8 | React State Events | [Live Demo](https://react-state-events-seven.vercel.app/) | [![Deploy](https://vercel.com/button)](https://vercel.com/new/clone?repository-url=https%3A%2F%2Fgithub.com%2FMahe13185%2FDearFSD&project-name=react-state-events&root-directory=react-state-events-app%2Freact-state-events-app-main) | ✅ Live |
| 9 | React Router | [Live Demo](https://react-router-beta-swart.vercel.app/) | [![Deploy](https://vercel.com/button)](https://vercel.com/new/clone?repository-url=https%3A%2F%2Fgithub.com%2FMahe13185%2FDearFSD&project-name=react-router&root-directory=react-router-app%2Freact-router-app-main) | ✅ Live |

### MERN Stack Application

| Component | Experiment / Service | Live Demo | Deploy to Your Vercel | Platform |
|---|---|---|:---:|:---:|
| Frontend | MERN CRUD Frontend | [Live Demo](https://mern-crud-frontend-steel.vercel.app/) | [![Deploy](https://vercel.com/button)](https://vercel.com/new/clone?repository-url=https%3A%2F%2Fgithub.com%2FMahe13185%2FDearFSD&project-name=mern-crud-frontend&root-directory=mern-crud-app%2Fmern-crud-app-main%2Ffrontend) | Vercel |
| Backend | MERN CRUD Posts API | [Live API](https://full-stack-development-lab.onrender.com/) | *(Via Render Blueprint)* | Render |

### Backend Applications (Render)

| No. | Experiment Name | Live Deployment URL | Status |
|---:|---|---|:---:|
| 1 | Products File Persistence | [Live API](https://file-persistent-app.onrender.com/api/v1/faculty) | ✅ Live |
| 2 | MongoDB Express | [Live API](https://mongodb-express-app-xky0.onrender.com/api/v1/books) | ✅ Live |
| 3 | MongoDB Mongoose Movies | [Live API](https://mongodb-mongoose-movies-app-zzof.onrender.com/) | ✅ Live |
| 4 | MVC Auth | [Live API](https://mvc-auth-app-zegs.onrender.com/) | ✅ Live |
| 5 | MVC Express | [Live API](https://mvc-express-app-fc7f.onrender.com/api/v1/movies) | ✅ Live |
| 6 | Template Engine EJS | [Live API](https://template-engine-ejs-app-9nip.onrender.com/) | ✅ Live |
| 7 | Express Middleware API | [Live API](https://express-middleware-api.onrender.com/) | ✅ Live |

---

## Technologies Used

- HTML, CSS, JavaScript
- React.js
- Node.js
- Express.js
- MongoDB
- Mongoose
- EJS

## Project Structure

| Folder | Description |
|---|---|
| React applications | React concepts and frontend experiments |
| Express applications | Express.js and middleware experiments |
| MongoDB applications | MongoDB and Mongoose integration |
| MERN application | Full-stack CRUD application |

## Applications

### React
- JSX Rendering
- Multiple Components
- HTML Rendering
- Conditional Rendering
- Rendering Lists
- State and Events
- Form Events
- React Router
- Frontend CRUD

### Backend
- File Persistent Application
- Non-Persistent Application
- Express Middleware API
- MongoDB Express Application
- Mongoose Express Application
- MVC Express Application
- MVC Authentication Application
- EJS Template Engine

### MERN
- MERN CRUD Application

## Running an Application

Navigate to the respective application directory:

```bash
cd path/to/application
npm install
npm run dev
```

For applications using a start script:

```bash
npm start
```

Refer to each application's package.json for its available scripts.

## Deployment

- Frontend applications are deployed using Vercel.
- Backend applications are deployed using Render.

## 👤 Author & Credits

* **Author:** **Mahendra Gampala**
* **GitHub:** [@Mahe13185](https://github.com/Mahe13185)
* **LinkedIn:** [Mahendra Gampala](https://www.linkedin.com/in/mahendragampala)
* **Repository:** [https://github.com/Mahe13185/DearFSD](https://github.com/Mahe13185/DearFSD)

⭐ **If you found this repository or automated deployment useful, please star the repo and follow me on [GitHub](https://github.com/Mahe13185) & [LinkedIn](https://www.linkedin.com/in/mahendragampala)!**
=======
# fsd2
>>>>>>> b1e8c32a6928b8884f8c86a0119bb49b1bf605d5

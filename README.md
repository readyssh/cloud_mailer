## 📧 CloudMailer – Simple Email Newsletter App

Cloudmailer: End-to-end Secure Cloud Infrastructure &amp; Monitoring Deployment On Aws Eks Using Jenkins, Helm, Prometheus &amp; Kubernetes
its is a simple email-sending app built with **Node.js**, **AWS SES**, and a minimal **HTML/CSS/JS** frontend. It allows users to send emails using AWS SES securely.

---

### 📂 Project Structure

```
project/
├── index.js         # Backend (Express + AWS SES)
├── index.html       # Frontend HTML page
├── script.js        # Frontend JS
├── style.css        # Styling
├── Dockerfile       # Docker config
├── .env             # Environment variables (not committed)
└── README.md        # Project guide
```

---

### 🚀 Features

* Send emails using AWS SES
* Works on all platforms (Linux, Mac, Windows)
* Dockerized for easy deployment

---

### ✅ Prerequisites

* [Node.js](https://nodejs.org/) installed (if running locally)
* [Docker](https://www.docker.com/) installed (if running with container)
* AWS account with:

  * Verified email address in **SES**
  * SES out of sandbox or verified recipient

---

### 🔧 Environment Setup

Create a `.env` file in the root directory with the following content:

```env
AWS_ACCESS_KEY_ID=your_aws_access_key_id
AWS_SECRET_ACCESS_KEY=your_aws_secret_access_key
AWS_REGION=YOUR_region
SOURCE_EMAIL=your_verified_ses_email@example.com
```

> 💡 Never commit the `.env` to GitHub! Add it to `.gitignore`.

---

### 🖥️ Run Locally (Without Docker)

1. Clone the repo:

```bash
git clone https://github.com/readyssh/cloud_mailer.git
cd cloudmailer
```

2. Install dependencies:

```bash
npm install
```

3. Create a `.env` file (see above).

4. Start the server:

```bash
node index.js
```

5. Open the frontend:

```bash
xdg-open index.html  # On Linux
start index.html     # On Windows
open index.html      # On Mac
```

---

### 🐳 Run Using Docker

1. Build the Docker image:

```bash
docker build -t cloudmailer .
```

2. Run the container:

```bash
docker run -d -p 5000:5000 --env-file .env cloudmailer
```

3. Access it in browser:

```bash
http://localhost:5000
```

---

### 🐳 Push to Docker Hub

If you want to push this to Docker Hub:

```bash
docker tag cloudmailer your-dockerhub-username/cloudmailer:latest
docker login
docker push your-dockerhub-username/cloudmailer:latest
```

Then run it from anywhere with:

```bash
docker run -d -p 5000:5000 --env-file .env your-dockerhub-username/cloudmailer:latest
```

---

### 📸 Screenshot

Add a screenshot here if needed:

```
📨 | Simple Email Sender UI
```

---

### 📬 Note

If you’re still in the AWS SES sandbox, you can **only email verified addresses** unless you request sandbox removal.

---

### 🧑‍💻 Author

**Readyssh** – **Visit** - [GitHub](https://github.com/readyssh)

---

# 🌚 Node.js Metrics App  

A Node.js application that exposes metrics for monitoring with **Prometheus** and visualization in **Grafana**.  
This setup allows users to easily deploy the app using **Docker Compose**.

---

## 🚀 Features  

✅ Node.js API with **/metrics** endpoint for Prometheus  
✅ Pre-configured **Prometheus** to scrape metrics from the app  
✅ Pre-installed **Grafana** for visualizing application performance  
✅ Ready-to-use **Docker Compose** setup for easy deployment  

---

## 👥 Installation  

### 1️⃣ **Download the Prebuilt Archive**  
You can download the **prebuilt setup** from the repository:  

[Download nodejs-monitoring-setup.tar.gz](https://github.com/omarfarook/nodejs-metrics-app/blob/main/nodejs-monitoring-setup.tar.gz)

### 2️⃣ **Extract the Archive**  
```sh
tar -xzf nodejs-monitoring-setup.tar.gz
cd nodejs-metrics-app
```

---

## 🏢 Running the Application  

### **Using Docker Compose**  
Simply run the following command to start **Node.js, Prometheus, and Grafana**:  

```sh
docker-compose up --build -d
```

📌 **This will:**  
✅ Build and start the **Node.js app**  
✅ Start **Prometheus** to collect metrics  
✅ Start **Grafana** for visualization  

---

## 👼 Accessing the Services  

### **1️⃣ Node.js App**  
```sh
http://localhost:3001
```
- This serves the **Node.js application**.

### **2️⃣ Metrics Endpoint**  
```sh
http://localhost:3001/metrics
```
- Exposes application metrics for **Prometheus**.

### **3️⃣ Prometheus Dashboard**  
```sh
http://localhost:9090
```
- Use this to **query and analyze collected metrics**.

### **4️⃣ Grafana Dashboard**  
```sh
http://localhost:3000
```
- Default login credentials:
  - **Username**: `admin`
  - **Password**: `admin`
- Preconfigured **Prometheus Data Source** is available.

---

## 🌍 Prometheus Query Examples  

#### **Get All Metrics From the App**  
```promql
{job="nodejs-metrics-app"}
```

#### **Track Total HTTP Requests**  
```promql
nodejs_http_requests_total
```

#### **Monitor CPU Usage**  
```promql
process_cpu_seconds_total
```

#### **Check Memory Usage**  
```promql
process_resident_memory_bytes
```

---

## 🛠️ Stopping the Services  

To stop and remove all running containers, run:  
```sh
docker-compose down
```

To clean up **all volumes and images**:  
```sh
docker system prune -a
```

---

## 🔧 Development & Customization  

### **Modify the Node.js App**  
After extracting the archive:
1. **Navigate to the app folder**  
   ```sh
   cd app
   ```
2. **Make changes to the code** (e.g., `server.js`)
3. **Rebuild and restart**  
   ```sh
   docker-compose up --build -d
   ```

### **Update the Prometheus Configuration**  
Modify `prometheus/prometheus.yml` to change scrape settings.

---

## 🌟 Deployment  

To run this setup on another machine:
1. **Download and extract the tarball**
2. **Run `docker-compose up --build -d`**
3. **Monitor the app with Prometheus & Grafana**

---

## 📚 License  

This project is licensed under the **MIT License**.

---

🚀 **Happy Monitoring!** Let me know if you need further improvements! 🎯


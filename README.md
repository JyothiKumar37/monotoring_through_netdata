# System Monitoring with Netdata

This project demonstrates how to monitor **system resources and Docker containers** using **Netdata**, a free and open-source real-time monitoring tool.  

---

## Setup & Installation

### 1. Run Netdata with Docker
`
docker run -d --name=netdata \
  -p 19999:19999 \
  --cap-add SYS_PTRACE \
  --security-opt apparmor=unconfined \
  netdata/netdata

-d → Run in detached mode

-p 19999:19999 → Exposes Netdata dashboard on port 19999

--cap-add SYS_PTRACE and --security-opt apparmor=unconfined → Required for some monitoring features

2. Access the Dashboard

Open your browser and go to:

 http://localhost:19999

If deployed on a server, replace localhost with the server’s IP:

http://<server-ip>:19999

What You Can Monitor

CPU Usage (per core and overall)

Memory Usage (RAM, swap)

Disk I/O & Storage

Network traffic

Docker containers (CPU, memory, network usage for each container)

System load & uptime

Alerts & Logs
Netdata provides real-time alerts for resource thresholds.

Logs are stored in:

/var/log/netdata

Outcome:
By completing this task, you will:
✔ Understand how to use Netdata for lightweight system monitoring
✔ Monitor containers, system performance, and alerts in real time
✔ Gain experience in running monitoring tools via Docker.

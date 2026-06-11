# 🚀 ROS Noetic Cloud Deployment on AWS EC2

## 📌 Project Title
Deploying ROS Noetic on AWS Cloud (EC2) for Remote Robotics Development

---

## 🎯 Objective
The objective of this project is to deploy **ROS (Robot Operating System) Noetic** on a cloud-based Ubuntu environment using AWS EC2.  
This enables developers to remotely run, test, and simulate robotic applications without needing local ROS installation.

---

## ☁️ Cloud Platform Used
- Amazon Web Services (AWS)
- EC2 (Elastic Compute Cloud)

---

## 💻 System Configuration

- **Operating System:** Ubuntu 20.04 LTS  
- **Instance Type:** t2.micro  
- **Storage:** 30 GB EBS Volume  
- **Region:** AWS Free Tier eligible setup  

---

## 🤖 ROS Version
- ROS Noetic Ninjemys

---

## 🛠️ Tools & Technologies Used
- ROS Noetic
- Ubuntu Linux
- AWS EC2
- Git & GitHub
- Catkin Workspace

---

## ⚙️ Installation Steps Followed

### 1. Launch EC2 Instance
- Created an AWS EC2 instance with Ubuntu 20.04 LTS
- Allocated 30GB storage
- Connected via SSH

### 2. Update System
```bash
sudo apt update && sudo apt upgrade -y
````

### 3. Configure ROS Repository

```bash
sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list'
```

### 4. Add ROS Key

```bash
sudo apt install curl -y
curl -s https://raw.githubusercontent.com/ros/rosdistro/master/ros.asc | sudo apt-key add -
```

### 5. Install ROS Noetic

```bash
sudo apt update
sudo apt install ros-noetic-desktop-full -y
```

### 6. Environment Setup

```bash
echo "source /opt/ros/noetic/setup.bash" >> ~/.bashrc
source ~/.bashrc
```

### 7. Verify Installation

```bash
rosversion -d
```

Expected output:

```
noetic
```

---

## 🧪 Testing & Validation

### Start ROS Master:

```bash
roscore
```

If successful, output shows:

```
started core service [/rosout]
```

---

## 📂 Project Structure

```
ros-noetic-aws-ec2-deployment/
│
├── src/
│   └── my_first_ros/        # Custom ROS package
├── screenshots/            # Proof of execution
├── .gitignore
└── README.md
```

---

## 📸 Screenshots Included

* AWS EC2 instance running (t2.micro)
* Ubuntu 20.04 verification
* ROS Noetic installation verification (`rosversion -d`)
* `roscore` running successfully
* Storage configuration (30 GB EBS)

---

## 📌 Key Features

* Cloud-based ROS setup
* No local installation required
* Remote robotics development environment
* Scalable infrastructure using AWS

---

## 🎯 Outcome

Successfully deployed **ROS Noetic on AWS EC2 Ubuntu 20.04 instance**, verified installation, and tested ROS core services.
This setup enables remote robotic simulation and development from anywhere.

---

## 👨‍💻 Author

Cloud Robotics Developer (Student Project)

---

## 📎 Conclusion

This project demonstrates cloud deployment skills, Linux system administration, ROS setup, and basic DevOps practices using AWS EC2.


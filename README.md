# TRANG TRẠI THÔNG MINH

<div align="center">

<p align="center">
  <img src="images/logo.png" alt="DaiNam University Logo" width="200"/>
  <img src="images/AIoTLab_logo.png" alt="AIoTLab Logo" width="170"/>
</p>

[![Made by AIoTLab](https://img.shields.io/badge/Made%20by%20AIoTLab-blue?style=for-the-badge)]((https://www.facebook.com/DNUAIoTLab))
[![Faculty of IT](https://img.shields.io/badge/Faculty%20of%20Information%20Technology-green?style=for-the-badge)]((https://fitdnu.net/))
[![DaiNam University](https://img.shields.io/badge/DaiNam%20University-red?style=for-the-badge)](https://dainam.edu.vn)

</div>

<h3 align="center">🔬 Hệ thống nuôi lợn thông minh kết hợp AI điều khiển thiết bị</h3>

<p align="center">
  <strong>Giải pháp ứng dụng IoT và AI vào chăn nuôi hiện đại</strong>
</p>

<p align="center">
  <a href="#-architecture">Hệ thống</a> •
  <a href="#-key-features">Tính năng</a> •
  <a href="#-tech-stack">Công nghệ</a> •
  <a href="#-installation">Cài đặt</a> •
  <a href="#-getting-started">Bắt đầu</a> •
  <a href="#-documentation">Tài liệu</a>
</p>

## 🏗️ Hệ thống

<p align="center">
  <img src="images/HeThong.png" alt="System Architecture" width="800"/>
</p>

Hệ thống trang trại thông minh được xây dựng với các thành phần chính:

- **ESP32 (Master)**: Nhận dữ liệu từ các Arduino UNO, gửi lên website qua Flask + WebSocket.
- **UNO1**: Hiển thị thời gian thực, hẹn giờ cho lợn ăn bằng động cơ bước và vít tải. Bật đèn tự động dựa trên cảm biến LDR.
- **UNO2**: Đo nhiệt độ, độ ẩm (DHT11), đo mực nước trong máng (Water Sensor). Tự động bơm nước khi dưới ngưỡng.
- **UNO3**: Cảm biến khí gas MQ135, cảnh báo bằng còi khi vượt ngưỡng.
- **ESP32-CAM**: Giám sát chuồng lợn qua video trực tiếp.
- **AI (Google Speech-to-Text)**: Nhận diện giọng nói để điều khiển máy bơm, động cơ bước và đèn LED.

## ✨ Tính năng

### 🧠 Công nghệ AI tiên tiến
- **Nhận diện giọng nói**: Chuyển đổi giọng nói thành lệnh điều khiển.
- **Xử lý ngữ cảnh**: Xác định hành động phù hợp với từng câu lệnh

### ⚡ Kiến trúc hiệu suất cao
- **Giao tiếp I2C**: UNO gửi dữ liệu nhanh chóng về ESP32 Master.
- **Kết nối WebSocket**: ESP32 gửi dữ liệu lên website theo thời gian thực

### 📊 Giám sát toàn diện
- **Cảnh báo tự động**: Khi mức nước thấp, khí gas vượt ngưỡng
- **Giao diện trực quan**: Hiển thị trạng thái thiết bị và thông tin môi trường

## 🔧 Công nghệ sử dụng

<div align="center">

### Phần cứng
[![ESP32](https://img.shields.io/badge/ESP32-blue?style=for-the-badge)](https://www.espressif.com/)
[![Arduino](https://img.shields.io/badge/Arduino-00979D?style=for-the-badge&logo=arduino&logoColor=white)](https://www.arduino.cc/)
[![DHT11](https://img.shields.io/badge/DHT11-Sensor-green?style=for-the-badge)]()
[![MQ135](https://img.shields.io/badge/MQ135-Gas%20Sensor-red?style=for-the-badge)]()

### Phần mềm
[![Flask](https://img.shields.io/badge/Flask-000000?style=for-the-badge&logo=flask&logoColor=white)](https://flask.palletsprojects.com/)
[![WebSocket](https://img.shields.io/badge/WebSocket-0078D7?style=for-the-badge)]()
[![Google Speech-to-Text](https://img.shields.io/badge/Google%20STT-yellow?style=for-the-badge)](https://cloud.google.com/speech-to-text)

</div>

## 📥 Cài đặt

### 🛠️ Yêu cầu hệ thống

- 🐍 **Python** `3.8+`
- 📡 **ESP32 & Arduino IDE**
- 💾 **RAM** `4GB+`
- 📶 **WiFi** kết nối internet

### ⚙️ Thiết lập môi trường

1. **Cài đặt thư viện Python**
   ```bash
   pip install flask flask-socketio google-cloud-speech
   ```
2. **Nạp code vào ESP32 & Arduino**
   - Sử dụng Arduino IDE nạp code cho UNO.
   - Sử dụng ESP-IDF hoặc Arduino IDE để nạp code cho ESP32.

3. **Chạy Server Flask**
   ```bash
   python app.py
   ```

## 🚀 Bắt đầu sử dụng

### 📡 Gửi lệnh giọng nói
```python
from speech_control import send_command
send_command("bật đèn")
```

### 📊 Xem dữ liệu cảm biến
```python
from get_sensor_data import get_data
print(get_data())
```

## 📚 Tài liệu

- 📖 [Hướng dẫn cài đặt](docs/installation.md)
- 🎛 [Cấu hình ESP32 & Arduino](docs/esp32-arduino.md)
- 🤖 [Sử dụng AI nhận diện giọng nói](docs/speech-ai.md)

## 📝 Giấy phép

© 2025 AIoTLab, Khoa CNTT, Đại học Đại Nam. Bản quyền thuộc về nhóm phát triển.

---

<div align="center">

### 🚀 Được

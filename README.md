# M.E.O ESP FIRMWARE

# Bắt đầu

1. Clone mã nguồn về máy
```
git clone https://github.com/makerhanoi/meo-esp-firmware
```
2. Sửa device_id trong mã nguồn
```
const char* device_id = "team09_1";
```
3. Kết nối đến WIFI của Board. Mặc định tên WiFi là ESP_8266_ + device_id
```
Ví dụ: ESP_8266_team08_1
```
4. Truy cập local IP của Wifi để tùy chỉnh các thông số. Thường local IP sẽ là: 192.168.4.1

5. Thiết lập Wifi cũng như Mosquitto server


# Reset các thiết lập có sẵn 
Uncomment đoạn code sau
```
//wifiManager.resetSettings();
```
Sau đó upload code lên board

# Trao đổi dữ liệu với NodeRED sử dụng M.E.O Module

Viết lại các hàm Function_F1 -> Function_F5 để thực hiện các trigger từ trên NodeRED

Viết lại các hàm Virtual_U1 -> Virtual_U5 để đọc các thông số từ cảm biến khác nhau và truyền lên NodeRED

Ngoài ra có các thông số cài đặt của MEO Module trên NodeRED giúp định nghĩa các port cần nhận dữ liệu từ firmware


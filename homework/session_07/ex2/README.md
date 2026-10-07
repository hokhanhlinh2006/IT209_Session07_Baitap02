# Bài 2: Quản trị Tường lửa UFW cho Cụm Dịch vụ Multi-port

Đây là báo cáo kết quả thiết lập tường lửa UFW theo yêu cầu của Bài 2.

## 1. Các lệnh đã cấu hình
```bash
sudo ufw default deny incoming
sudo ufw default allow outgoing
sudo ufw allow 22/tcp
sudo ufw allow 80/tcp
sudo ufw allow 8082/tcp
sudo ufw enable
```

## 2. Kết quả kiểm tra lệnh (ufw status verbose)

Thực thi lệnh: `sudo ufw status verbose`

**Kết quả báo cáo:**
```text
Status: active
Logging: on (low)
Default: deny (incoming), allow (outgoing), disabled (routed)
New profiles: skip

To                         Action      From
--                         ------      ----
22/tcp                     ALLOW IN    Anywhere
80/tcp                     ALLOW IN    Anywhere
8082/tcp                   ALLOW IN    Anywhere
22/tcp (v6)                ALLOW IN    Anywhere (v6)
80/tcp (v6)                ALLOW IN    Anywhere (v6)
8082/tcp (v6)              ALLOW IN    Anywhere (v6)
```

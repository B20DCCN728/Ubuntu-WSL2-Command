# 🌐 Ubuntu/WSL2 Command Reference (Basic → Advanced)

---

## 📂 1. File & Directory Commands
| **Lệnh** | **Mô tả** | **Ví dụ** |
|----------|-----------|-----------|
| `pwd` | Hiển thị thư mục hiện tại | `pwd` → `/home/user` |
| `ls -lh` | Liệt kê file với chi tiết | `ls -lh` |
| `cd <dir>` | Chuyển thư mục | `cd /etc` |
| `touch <file>` | Tạo file rỗng | `touch test.txt` |
| `cat <file>` | Xem nội dung file | `cat test.txt` |
| `less <file>` | Xem file theo trang | `less /var/log/syslog` |
| `nano / vim <file>` | Chỉnh sửa file | `nano test.txt` |
| `cp file1 file2` | Copy file | `cp a.txt b.txt` |
| `mv old new` | Đổi tên / di chuyển | `mv old.txt new.txt` |
| `rm <file>` | Xóa file | `rm test.txt` |
| `mkdir <dir>` | Tạo thư mục | `mkdir mydir` |
| `rmdir <dir>` | Xóa thư mục rỗng | `rmdir mydir` |
| `find /path -name "*.txt"` | Tìm file | `find /etc -name "hosts"` |
| `grep "text" file` | Tìm chuỗi trong file | `grep "root" /etc/passwd` |
| `stat <file>` | Thông tin chi tiết file | `stat test.txt` |
| `head -n 10 <file>` | Xem 10 dòng đầu | `head -n 10 log.txt` |
| `tail -n 10 <file>` | Xem 10 dòng cuối | `tail -n 10 log.txt` |

---

## 👤 2. User & Permission Management
| **Lệnh** | **Mô tả** | **Ví dụ** |
|----------|-----------|-----------|
| `whoami` | Tên user hiện tại | `whoami` → `user` |
| `id` | UID, GID của user | `id` |
| `adduser <name>` | Tạo user mới | `sudo adduser alice` |
| `passwd <name>` | Đổi mật khẩu | `passwd alice` |
| `su <name>` | Đổi user | `su root` |
| `sudo <cmd>` | Chạy với quyền root | `sudo apt update` |
| `chmod 755 file` | Đổi quyền file | `chmod 755 script.sh` |
| `chown user:group file` | Đổi chủ sở hữu | `chown alice:alice file.txt` |

---

## ⚙️ 3. Process & System Management
| **Lệnh** | **Mô tả** | **Ví dụ** |
|----------|-----------|-----------|
| `ps aux` | Liệt kê tiến trình | `ps aux | grep ssh` |
| `top / htop` | Theo dõi CPU/RAM | `top` |
| `kill -9 PID` | Dừng tiến trình | `kill -9 1234` |
| `df -h` | Dung lượng ổ đĩa | `df -h` |
| `free -h` | RAM hiện tại | `free -h` |
| `uptime` | Thời gian hoạt động | `uptime` |
| `vmstat` | Thống kê bộ nhớ/CPU | `vmstat 2` |
| `iostat` | Thống kê I/O | `iostat` |
| `systemctl status <service>` | Trạng thái dịch vụ | `systemctl status ssh` |
| `journalctl -xe` | Log hệ thống | `journalctl -xe` |

---

## 🌐 4. Networking
| **Lệnh** | **Mô tả** | **Ví dụ** |
|----------|-----------|-----------|
| `ping <host>` | Kiểm tra kết nối | `ping google.com` |
| `curl <url>` | Tải nội dung web | `curl https://example.com` |
| `wget <url>` | Tải file | `wget https://file.zip` |
| `ip addr` | Xem IP | `ip addr` |
| `netstat -tulnp` | Cổng & dịch vụ | `netstat -tulnp` |
| `ssh user@host` | Kết nối SSH | `ssh root@192.168.1.1` |
| `scp file user@host:/path` | Copy qua SSH | `scp a.txt root@server:/tmp` |
| `traceroute host` | Theo dõi đường đi gói tin | `traceroute google.com` |
| `dig domain` | Truy vấn DNS | `dig example.com` |

---

## 📦 5. Package Management (APT)
| **Lệnh** | **Mô tả** | **Ví dụ** |
|----------|-----------|-----------|
| `apt update` | Cập nhật danh sách gói | `sudo apt update` |
| `apt upgrade` | Nâng cấp gói | `sudo apt upgrade` |
| `apt install <pkg>` | Cài gói | `sudo apt install nginx` |
| `apt remove <pkg>` | Gỡ gói | `sudo apt remove nginx` |
| `apt search <pkg>` | Tìm gói | `apt search curl` |
| `apt autoremove` | Xóa gói thừa | `sudo apt autoremove` |
| `apt purge <pkg>` | Gỡ hoàn toàn gói | `sudo apt purge nginx` |
| `apt-cache show <pkg>` | Thông tin chi tiết gói | `apt-cache show curl` |

---

## 🗜️ 6. Archive & Compression
| **Lệnh** | **Mô tả** | **Ví dụ** |
|----------|-----------|-----------|
| `tar -czvf file.tar.gz dir/` | Nén gzip | `tar -czvf backup.tar.gz mydir/` |
| `tar -xzvf file.tar.gz` | Giải nén gzip | `tar -xzvf backup.tar.gz` |
| `zip -r file.zip dir/` | Nén zip | `zip -r archive.zip mydir/` |
| `unzip file.zip` | Giải nén zip | `unzip archive.zip` |

---

## 🔧 7. Advanced System Administration
| **Lệnh** | **Mô tả** | **Ví dụ** |
|----------|-----------|-----------|
| `crontab -e` | Lập lịch cronjob | `crontab -e` |
| `alias ll='ls -lah'` | Tạo alias | `alias gs='git status'` |
| `history` | Lịch sử lệnh | `history | tail -n 5` |
| `export VAR=value` | Biến môi trường | `export PATH=$PATH:/opt/bin` |
| `mount / umount` | Mount/Unmount ổ đĩa | `mount /dev/sdb1 /mnt` |
| `rsync -av src/ dest/` | Đồng bộ dữ liệu | `rsync -av mydir/ backup/` |
| `tmux / screen` | Quản lý session | `tmux new -s work` |

---

## 💻 8. Programming & DevOps
| **Lệnh** | **Mô tả** | **Ví dụ** |
|----------|-----------|-----------|
| `gcc file.c -o file` | Compile C | `gcc hello.c -o hello` |
| `python3 script.py` | Chạy Python | `python3 app.py` |
| `node app.js` | Chạy Node.js | `node app.js` |
| `git clone <repo>` | Clone repo | `git clone https://github.com/...` |
| `git status` | Trạng thái git | `git status` |
| `docker ps` | Container đang chạy | `docker ps` |
| `docker images` | Danh sách images | `docker images` |
| `kubectl get pods` | Kubernetes | `kubectl get pods` |

---

## 🖥️ 9. WSL2-Specific Commands (Windows)
| **Lệnh** | **Mô tả** | **Ví dụ** |
|----------|-----------|-----------|
| `wsl --list --verbose` | Liệt kê distro | `wsl --list --verbose` |
| `wsl --set-default <distro>` | Đặt mặc định | `wsl --set-default Ubuntu` |
| `wsl --install -d Ubuntu` | Cài Ubuntu | `wsl --install -d Ubuntu` |
| `wsl --terminate <distro>` | Dừng distro | `wsl --terminate Ubuntu` |
| `wsl --export <distro> file.tar` | Xuất distro | `wsl --export Ubuntu backup.tar` |
| `wsl --import <distro> <path> file.tar` | Nhập lại | `wsl --import Ubuntu D:\\WSL backup.tar` |
| `wsl --shutdown` | Tắt toàn bộ WSL | `wsl --shutdown` |
| `wsl --update` | Cập nhật WSL | `wsl --update` |
| `wsl --status` | Trạng thái WSL | `wsl --status` |
| `wsl --set-version <distro> 2` | Chuyển sang WSL2 | `wsl --set-version Ubuntu 2` |
| `wsl --unregister <distro>` | Xóa distro | `wsl --unregister Ubuntu` |


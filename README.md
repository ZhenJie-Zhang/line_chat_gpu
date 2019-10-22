# 如何使用
```
git clone https://github.com/ZhenJie-Zhang/line_chat_gpu.git
cd line_chatbot_quick_template
sudo docker-compose up -d
sudo docker exec -it line-chat-bot-jupyter bash
cd /root; jupyter notebook --allow-root
```
# 使用瀏覽器進入 (範例:http://IP:8888)
進入後會詢問登入密碼，docker的`line-chat-bot-jupyter`容器內預設jupyter notebook密碼為123456
password = 123456


# docker-compose up -d 之後ELK連線失敗
![](https://paper-attachments.dropbox.com/s_05E5F1F8781875F732E4AE85C8772E32CCD2F20F18A6433A64FB355FDEA18D5C_1571725950883_image.png)


原文網址：https://kknews.cc/code/jr3x5qq.html
## 檢查運行的實例

    sudo docker-compose ps
![](https://paper-attachments.dropbox.com/s_05E5F1F8781875F732E4AE85C8772E32CCD2F20F18A6433A64FB355FDEA18D5C_1571725824444_image.png)


錯誤解決

- max virtual memory areas vm.max_map_count [65530] is too low, increase to at least [262144]
- 解決方法：
- `sudo vi /etc/sysctl.conf`添加以下內容：
    vm.max_map_count=262144
- 並執行`sudo sysctl -p`

![](https://paper-attachments.dropbox.com/s_05E5F1F8781875F732E4AE85C8772E32CCD2F20F18A6433A64FB355FDEA18D5C_1571747823962_image.png)

![](https://paper-attachments.dropbox.com/s_05E5F1F8781875F732E4AE85C8772E32CCD2F20F18A6433A64FB355FDEA18D5C_1571726115355_image.png)

![](https://paper-attachments.dropbox.com/s_05E5F1F8781875F732E4AE85C8772E32CCD2F20F18A6433A64FB355FDEA18D5C_1571726204327_image.png)

![](https://paper-attachments.dropbox.com/s_05E5F1F8781875F732E4AE85C8772E32CCD2F20F18A6433A64FB355FDEA18D5C_1571749926133_image.png)

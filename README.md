# Injector_blueteam

Thử thách gồm 2 file

![image](https://user-images.githubusercontent.com/72652376/217188135-efd5f071-d41e-4291-803f-f4021a680449.png)


#1. What is the computer's name?

Kiểm tra tại: \REGISTRY\MACHINE\SYSTEM\ControlSet001\Control\ComputerName\ComputerName

![image](https://user-images.githubusercontent.com/72652376/217188576-edc313d7-53c6-4673-b631-e569363be995.png)

Đáp án: **WIN-L0ZZQ76PMUF**



#2. What is the Timezone of the compromised machine? Format: UTC+0 (no-space)

Kiểm tra tại: SYSTEM\ControlSet001\Control\TimeZoneInformation

![image](https://user-images.githubusercontent.com/72652376/217189046-4835b572-ac7c-4165-9a8c-d772eb578e83.png)

Đáp án:

#3. What was the first vulnerability the attacker was able to exploit?

#4.What is the OS build number?

#5.How many users are on the compromised machine?

#7.What is the name of the vulnerable web app installed on the webserver?

![image](https://user-images.githubusercontent.com/72652376/217189651-691c852e-ba06-41c9-a369-544c94964d79.png)

Đọc log thì có thể thấy web app được cài trên webserver là **DVWA**

#8.What is the user agent used in the HTTP requests sent by the SQL injection attack tool?

![image](https://user-images.githubusercontent.com/72652376/217190302-7194ff1b-2e8a-4067-99cb-f96a6851958b.png)

Kiểm tra log thì có thể thấy dùng sqlmap để scan SQL injection

Đáp án:  **sqlmap/1.0-dev-nongit-20150902**

#11.How many users were added by the attacker?

Toàn bộ số lượng user ở trên là 4. Trong đó có 2 user được tạo gần nhất

![image](https://user-images.githubusercontent.com/72652376/217190961-a159d1de-aee5-4561-a0ca-3687f9a24df6.png)

Đáp án: **2**

#12.When did the attacker create the first user?

Theo hình trên thì nghĩa là user1 được hacker tạo đầu tiên

Đáp án:  **2015-09-02 09:05:06 UTC**

#13.What is the NThash of the user's password set by the attacker?

![image](https://user-images.githubusercontent.com/72652376/217194762-090e8e51-b892-4c9e-bed9-95ee15119990.png)

Check hash pass của các user đã có.

Đáp án: **817875ce4794a9262159186413772644**

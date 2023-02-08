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

Đáp án: **UTC-7**

#3. What was the first vulnerability the attacker was able to exploit?

Đọc log access

![image](https://user-images.githubusercontent.com/72652376/217410935-27f991a3-fb78-4065-a701-d476e60ff511.png)


#4.What is the OS build number?

#5.How many users are on the compromised machine?

#7.What is the name of the vulnerable web app installed on the webserver?

![image](https://user-images.githubusercontent.com/72652376/217189651-691c852e-ba06-41c9-a369-544c94964d79.png)

Đọc log thì có thể thấy web app được cài trên webserver là **DVWA**

#8.What is the user agent used in the HTTP requests sent by the SQL injection attack tool?

![image](https://user-images.githubusercontent.com/72652376/217190302-7194ff1b-2e8a-4067-99cb-f96a6851958b.png)

Kiểm tra log thì có thể thấy dùng sqlmap để scan SQL injection

Đáp án:  **sqlmap/1.0-dev-nongit-20150902**


10.The attacker tried to update some firewall rules using netsh command. Provide the value of the type parameter in the executed command?

![image](https://user-images.githubusercontent.com/72652376/217409290-224710b2-b51e-43ff-868d-f5f05f63d170.png)

Đáp án:**remotedesktop**

#11.How many users were added by the attacker?

Toàn bộ số lượng user ở trên là 4. Trong đó có 2 user được tạo gần nhất

![image](https://user-images.githubusercontent.com/72652376/217190961-a159d1de-aee5-4561-a0ca-3687f9a24df6.png)

Đáp án: **2**

#12.When did the attacker create the first user?

Theo thời gian trên thì nghĩa là user1 được hacker tạo đầu tiên

Đáp án:  **2015-09-02 09:05:06 UTC**

#13.What is the NThash of the user's password set by the attacker?

![image](https://user-images.githubusercontent.com/72652376/217194762-090e8e51-b892-4c9e-bed9-95ee15119990.png)

Check hash pass của các user đã có.

Đáp án: **817875ce4794a9262159186413772644**

#14.What is The MITRE ID corresponding to the technique used to keep persistence?

Create Account: Local Account search trên MITRE có thể thấy được ID là ** T1136.001**

#15.The attacker uploaded a simple command shell through file upload vulnerability. Provide the name of the URL parameter used to execute commands?

![image](https://user-images.githubusercontent.com/72652376/217200279-33c42264-a1bb-4c71-af64-dbe3b0cebd4c.png)

Trả lời: **CMD**

#16. One of the uploaded files by the attacker has an md5 that starts with "559411". Provide the full hash.

Kiểm tra tại thư mục upload 

![image](https://user-images.githubusercontent.com/72652376/217412545-b7fb1414-6c60-4edb-95c5-13712358a07a.png)

Đáp án: **5594112b531660654429f8639322218b**

#17. The attacker used Command Injection to add user "hacker" to the "Remote Desktop Users" Group. Provide the IP address that was part of the executed command?

Đọc log thì chỉ thấy 1 IP duy nhất là **192.168.56.102** thực hiện attack

![image](https://user-images.githubusercontent.com/72652376/217409686-3ebb8cf3-18dc-4e5f-b3cf-45d5cd6ce60d.png)

Đáp án:**192.168.56.102**

#18.The attacker dropped a shellcode through SQLi vulnerability. The shellcode was checking for a specific version of PHP. Provide the PHP version number?

![image](https://user-images.githubusercontent.com/72652376/217411820-0eb0dc5c-3237-4001-b5ce-f00adfa629a9.png)

Có 1 số file tìm thấy khi attacker khai thác sql vul. Kiểm tra đoạn hex

![image](https://user-images.githubusercontent.com/72652376/217411987-f6496905-dab7-443a-b522-581295016aeb.png)

Decode ra có đáp án là **4.1.0**




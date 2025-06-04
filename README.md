<div align="start">
<h1>Simple Portscanning.py</h1>
</div>

```python
import socket 

ports = [21,22,80,443,445,3306,25]

for port in ports:
        client = socket.socket(socket.AF_INET, socket.SOCK_STREAM)
        client.settimeout(0.5)
        code = client.connect_ex(("siteexample.com", port))
        if code == 0:
                print(port, "OPEN")
        else:
                print(port, "ClOSE")

```

<p>While I'm learning cyber security, I decided to create a portscanning system using the socket module from the python library.</p>

<h1> How it works: </h1>

Basically, you add the desired website or IP where it says ```"siteexample.com"``` and it will check ports ```[21,22,80,443,445,3306,25]``` in the ```ports``` variable.<br>
You can add or remove as many doors as you want.

<h1>A pratical example: </h1>

![tela scan2](https://github.com/user-attachments/assets/9ce71db1-1ad3-4434-b3db-391c1a8c82e3)


In this case, I'm using  ```client.connect_x(("bancocn.com", port))``` which is a website provided by the course "Introdução ao Hacking e Pentest 2.0" that I'm currently using to learn about Pentesting (I'm not doing anything illegal, I swear)

That's all, thanks for reading!




System operacyjny w środowisku sieciowym
=========================================

Charakterystyka systemu operacyjnego
------------------------------------

| Charakterystyka | wartość           | komentarzu |
| ------------- |:-------------:| -----:|
| nazwa      | linux | Ubuntu |
| program (parametry sieci)      | Oracle VM VirtualBOX | Mostkowana karta sieciowa (bridged)  |


Konfiguracja połączenia sieciowego
----------------------------------

| Parametr | wartość           | komentarzu |
| ------------- |:-------------:| -----:|
| Adres IP      | 10.0.2.15 | przydzielony przez DHCP |
| Maska podsieci      | 255.255.0.0| route -n |
| Brama      | 169.254.0.0 | route -n |
| DNS 1      | 10.10.0.8 | Network settings |
| DNS 2      | 10.10.0.4 | Network settings |

Schemat sieci
-------------
![alt schemat](https://github.com/Nissmel/sk-2019/blob/master/Untitled%20Diagram.png)

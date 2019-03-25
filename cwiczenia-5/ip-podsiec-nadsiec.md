Podsieci i nadsieci IP
----------------------

adresacja
-----------------------------------------------------
| PC     |  interfejs   | adres  |
| --------- |:-------------| :---------------| 
| ``PC1``   | enp0s3 | 192.168.100.5/24     |
| ``PC-R-1``| enp0s3 | 192.168.100.4/24      |
| ``PC-R-1``| enp0s8 | 192.168.200.100/29     |
| ``PC-R-2``| enp0s3 | 192.168.200.101/29     |
| ``PC-R-2``| enp0s8 | 192.168.0.68/29   |
| ``PC-R-2``| enp0s9 | 192.168.0.68/27 |

routing
-------

| destination | trasa | interfejs  |
| --------- |:-------------| :---------------| 
| ``PC1``     |  | |
| ``default`` | 192.168.100.1 | enp0s3 ``ip route add default via 192.168.100.1``| 
| ``PC-R-1``  |  |        |
| ``192.168.100.0/24`` | 192.168.100.1  | enp0s3      |
| ``192.168.200.0/24``  | 192.168.200.1 | enp0s8      |

<h3>Można dzielić</h3>

| destination | trasa | interfejs  |
| --------- |:-------------| :---------------| 
| ``192.168.0.0/24``  | 192.168.200.2 | enp0s8      |
| ``192.168.0.128/24``  | 192.168.200.2 | enp0s8      |
| ``192.168.0.192/24``  | 192.168.200.2 | enp0s8      |

<h3>Na raz</h3>

| destination | trasa | interfejs  |
| --------- |:-------------| :---------------| 
| ``192.168.0.64/24``  | 192.168.200.1 | enp0s8      |

<h3>PC_R-2</h3>

| destination | trasa | interfejs  |
| --------- |:-------------| :---------------| 
| ``192.168.0.64/24``  | 192.168.200.2 | enp0s3      |
| ``192.168.0.64/24``  | 192.168.200.1 | enp0s3      |
| ``192.168.0.64/24``  | 192.168.0.65 | enp0s8      |
| ``192.168.0.64/24``  | 192.168.0.129 | enp0s9      |
| ``192.168.0.64/24``  | 192.168.0.193 | enp0s10      |

Zadanie
------------

![zadanie 5](https://github.com/Nissmel/sk-2019/blob/master/cwiczenia-5/pobrane.svg)

1.
   * Przygotuj konfigurację sieci zgodnie z powyższym diagramem
   * W pierwszej kolejności przygotuj ``PC1``, ``PC-R-1``, ``PC-R-2``, ``PC-2``
   * Do konfiguracji wykorzystaj dane z tabeli powyżej
   * Rozszerz istniejącą konfigurację dzieląc istnijącą sieć dla ``PC2`` na 3 podsieci zgodnie z diagramem
   * Przetestuj połączenie pomiędzy wszystkimi elementami sieci ``PC1->PC2`` ``PC1->PC4``
   * Zapewnij permanentną konfigurację, dodając odpowiednie wpisy w plikach konfiguracji

Zadanie do domu
---------------

1. Wykorzystując program dia oraz ikony CISCO
  * Przygotuj diagram powyższej sieci uwzględniając urządzenia tj:
    * ROUTER
    * SWITCH
    * PC
  * Uzupełnij diagram o adresację sieci oraz poszczególnych urządzeń
  

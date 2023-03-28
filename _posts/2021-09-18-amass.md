---
layout: post
title: "OWASP AMASS -- Culegere de informații și date"
date: '2021-09-18 08:53:56 +0300'
---

OWASP AMASS -- Culegere de informații și date
---------------------------------------------

![](https://securitypatch.ro/wp-content/uploads/2021/10/amass.jpg "amass")

AMASS conceput de OWASP şi dezvoltat de Jeff Foley în limbajul GOLANG reprezintă o unealtă open-source care poate fi utilă în maparea rețelelor și descoperirea de elemente de infrastructură, recunoaștere activă precum și identificare de date suplimentare.

Pentru ca AMASS să fie capabil de asemenea task-uri, este necesară integrarea sa cu servicii externe și API-uri pentru o eficiență cât mai mare și o putere de procesare la nivel local. Pentru descoperirea și culegerea de date, AMASS se bazează în principal pe DNS, HTTP sau SSL/TLS.

Instalarea
----------

Pentru a instala AMASS se poate extrage ultima versiune de pe Github https://github.com/OWASP/Amass/releases, alegând pachetul corespunzător în funcție de configurația echipamentului.

Pentru a ne asigura de integritatea documentului, după instalare putem verifica checksum-ul <https://github.com/OWASP/Amass/releases/download/v3.13.4/amass_checksums.txt>

"shasum -c amass_checksums.txt"

După verificarea integrității, putem începe prin a-l dezarhiva și pentru acordarea privilegiilor de execuție:

"chmod +x amass"\
"./amass"

Dacă toate cele de mai sus au fost configurate, putem trece la configurarea API-urilor. După configurare, poate fi startat procesul de verificare.

În cadrul documentului config.ini (<https://github.com/OWASP/Amass/blob/master/examples/config.ini>) se regăsește lista cu API-urile serviciilor compatibile, având posibilitatea de a alege platforme gratuite sau cu abonament plătit.

Utilizarea
----------

Toate comenzile și documentația sunt disponibile aici:

<https://github.com/OWASP/Amass/blob/master/doc/user_guide.md>

<https://github.com/OWASP/Amass/blob/master/doc/tutorial.md>

-   *amass intel* -- Descoperă ținte pentru enumerare
-   *amass enum* -- Realizează enumerare și topografia rețelei
-   *amass viz* -- Vizualizează rezultatele enumerației
-   *amass track* -- Descoperă diferențele dintre enumerații
-   *amass db* -- Manipulează graficul AMASS și baza de date
-   *amass dns* -- Descoperă nume DNS la o performanță ridicată

Printre capabilitățile AMASS se regăsește și căutarea DNS-urilor. Spre exemplu, unde flag-ul "-active" ne oferă un rezultat proactiv și flag-ul "-src" ne arată sursa informațiilor.

$ amass intel -addr 1.1.1.1 -src\
[reverse DNS] one.one.one\
Amass intel -active -addr 1.1.1.1 -src one.one.one 130 x\
[Reverse DNS] one.one\
[Active Cert] cloudflare-dns.com

Recunoaștere
------------

Vom utiliza subcomanda "enum" unde vom obține detalii din surse diferite despre ținta noastră:

În cazul de față, folosim flag-ul -d pentru domeniu, -src și config pentru a specifica unde avem config.ini cu API-urile noastre.

În exemplul de mai jos putem observa că AMASS și-a extras datele din Ask.com, descoperind prezența WAF-ului de la Cloudflare și că are doar două domenii/subdomenii cunoscute.

$ amass enum -d securitypatch.ro -src -config- Documents/config.ini

[Ask] www.securitypatch.ro\
[DNS] securitypatch.ro\
OWASP Amass v3.13.4 https://github.com/OWASP/Amass\
--------------------------------------------------------------------\
2 names discovered -- scrape: 1, cert: 1\
----------------------------------------------------------------------\
ASN: 13335 -- Cloudflare, Inc. (CLOUD14) -- CLOUDFLARENET-AS Cloudflare, Inc.\
2606:4700:3036::/48 1 Subdomain Name(s)\
2606:4700:3031::/48 1 Subdomain Name(s)\
172.67.0.0/16 2 Subdomain Name(s)\
104.21.32.0/20 2 Subdomain Name(s)

În concluzie, AMASS reprezintă o unealtă estrem de puternică prin care se poate analiza infrastructura unei ținte, domeniile și subdomeniile utilizate, schimbările realizate la nivel DNS, recunoaștere, topografie, ajutând totodată la identificarea altor elemente utile.

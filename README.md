Windows 10 / 11

Télécharger Python : v3.10 ou v3.9

100% sûr !

Mise à jour fréquente

Peut avoir quelques bugs

Python fourni

AVERTISSEMENT : De nombreuses personnes vendent ou distribuent GANG-Nuker !

N'INSTALLEZ PAS GANG-Nuker à partir d'un autre endroit que cette page, sinon vous risquez d'être piraté ou arnaqué.

Installation
Version du code source (plus compliquée mais moins buguée)

Télécharger GANG-Nuker.zip
Extraire le fichier
Appuyer sur "Install.bat" dans le dossier GANG
Une fois que tous les modules ont été installés, GANG se lancera automatiquement !
Profitez-en !
REMARQUE : Pour ouvrir GANG-Nuker, appuyez simplement sur "start.bat" à chaque fois !
REMARQUE : Assurez-vous d'avoir Python 3.9+ et qu'il est ajouté au PATH.

Version compilée (plus facile mais plus buguée)

Télécharger : https://github.com/TT-Tutorials/GANG-Nuker/releases
Extraire le fichier
Télécharger la dernière version (GANG-Nuker.zip) et extraire l'exécutable
Lancer le programme et profitez-en !
💻〢Exemple de support de proxy :

python
Copier le code
def fetchProxies(url, custom_regex):
    global proxylist
    try:
        proxylist = requests.get(url, timeout=5).text
    except Exception:
        pass
    finally:
        proxylist = proxylist.replace('null', '')
    custom_regex = custom_regex.replace('%ip%', '([0-9]{1,3}\\.[0-9]{1,3}\\.[0-9]{1,3}\\.[0-9]{1,3})')
    custom_regex = custom_regex.replace('%port%', '([0-9]{1,5})')
    for proxy in re.findall(re.compile(custom_regex), proxylist):
        proxieslog.append(f"{proxy[0]}:{proxy[1]}")

proxysources = [
    ["http://spys.me/proxy.txt","%ip%:%port% "],
    ["https://proxylist.icu/proxy/", "<td>%ip%:%port%</td><td>http<"],
    ["https://proxylist.icu/proxy/1", "<td>%ip%:%port%</td><td>http<"],
    ["https://proxylist.icu/proxy/2", "<td>%ip%:%port%</td><td>http<"],
    ["https://proxylist.icu/proxy/3", "<td>%ip%:%port%</td><td>http<"],
    ["https://proxylist.icu/proxy/4", "<td>%ip%:%port%</td><td>http<"],
    ["https://proxylist.icu/proxy/5", "<td>%ip%:%port%</td><td>http<"],
    ["http://www.httptunnel.ge/ProxyListForFree.aspx"," target=\"_new\">%ip%:%port%</a>"],
    ["https://www.us-proxy.org/", "<tr><td>%ip%<\\/td><td>%port%<\\/td><td>(.*?){2}<\\/td><td class='hm'>.*?<\\/td><td>.*?<\\/td><td class='hm'>.*?<\\/td><td class='hx'>(.*?)<\\/td><td class='hm'>.*?<\\/td><\\/tr>"],
    ["https://free-proxy-list.net/", "<tr><td>%ip%<\\/td><td>%port%<\\/td><td>(.*?){2}<\\/td><td class='hm'>.*?<\\/td><td>.*?<\\/td><td class='hm'>.*?<\\/td><td class='hx'>(.*?)<\\/td><td class='hm'>.*?<\\/td><\\/tr>"],
    ["https://www.sslproxies.org/", "<tr><td>%ip%<\\/td><td>%port%<\\/td><td>(.*?){2}<\\/td><td class='hm'>.*?<\\/td><td>.*?<\\/td><td class='hm'>.*?<\\/td><td class='hx'>(.*?)<\\/td><td class='hm'>.*?<\\/td><\\/tr>"],
    ["https://raw.githubusercontent.com/sunny9577/proxy-scraper/master/proxies.json", "\"ip\":\"%ip%\",\"port\":\"%port%\","],
    ["https://raw.githubusercontent.com/fate0/proxylist/master/proxy.list", '"host": "%ip%".*?"country": "(.*?){2}",.*?"port": %port%'],
    ["https://raw.githubusercontent.com/clarketm/proxy-list/master/proxy-list.txt", '%ip%:%port% (.*?){2}-.-S \\+'],
    ["https://raw.githubusercontent.com/opsxcq/proxy-list/master/list.txt", '%ip%", "type": "http", "port": %port%'],
    ["https://www.hide-my-ip.com/proxylist.shtml", '"i":"%ip%","p":"%port%",'],
    ["https://api.proxyscrape.com/?request=getproxies&proxytype=http&timeout=6000&country=all&ssl=yes&anonymity=all", "%ip%:%port%"],
    ["https://raw.githubusercontent.com/TheSpeedX/SOCKS-List/master/http.txt", "%ip%:%port%"],
    ["https://raw.githubusercontent.com/shiftytr/proxy-list/master/proxy.txt", "%ip%:%port%"],
    ["https://raw.githubusercontent.com/scidam/proxy-list/master/proxy.json", '"ip": "%ip%",\n.*?"port": "%port%",']
]
threads = [] 
for url in proxysources:
    t = threading.Thread(target=fetchProxies, args=(url[0], url[1]))
    threads.append(t)
    t.start()
for t in threads:
    t.join()

proxies = list(set(proxieslog))
with open(temp, "w") as f:
    for proxy in proxies:
        for i in range(random.randint(7, 10)):
            f.write(f"{proxy}\n")
execution_time = (time.time() - startTime)
💻〢Téléchargement automatique des modules :

python
Copier le code
import os 
import threading

try:
    import EXAMPLE v1
except:
    os.system("pip install EXAMPLE v1")
    import EXAMPLE v1

try:
    import EXAMPLE v2
except:
    os.system("pip install EXAMPLE v2")
    import EXAMPLE v2









ChatGPT peut faire des erreurs. Envisagez de vérifier les informations importantes.

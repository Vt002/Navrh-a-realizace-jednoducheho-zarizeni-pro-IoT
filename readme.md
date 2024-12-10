[Co dodělat ]: #
[nic ]: #




# Návrh a realizace jednoduchého zařízení pro IoT

## Cíl

- Studenti budou rozlišovat mezi klasickou automatizací a IoT jak v domácnosti, tak průmyslu
- Dokáží popsat základní požadavky kladené na zařízení IoT, a to i z hlediska safety a security
- Popíší vybraný hardware
- A naprogramují jednoduché IoT zařízení

## Ověření cílů

Návrh a realizace jednoduchého zařízení pro IoT

1. Vysvětlete, co to je internet věcí (IoT) 
2. Základní požadavky kladené na IoT zařízení
3. IoT zařízení z hlediska bezpečnosti a zabezpečení (safety a security)
4. Příklad realizace HW a SW jednoduchého zařízení pro IoT

## Úlohy

### 1. Co je to IoT

1. Podívejte se níže na definice IoT a automatizace a popište v čem se od sebe liší. 

> :key: **IoT**
>
> Internet of Things (Internet věcí)
> IIoT, též Industry 4.0 je IoT v průmyslu.
> Internet věcí. Online. In: Wikipedia: the free encyclopedia. San Francisco (CA): Wikimedia Foundation, 2024, 6. 12. 2024 v 23:12. Dostupné z: https://cs.wikipedia.org/wiki/Internet_v%C4%9Bc%C3%AD. [cit. 2024-12-09].

> :key: **Automatizace**
>
> Automatizace. Online. In: Wikipedia: the free encyclopedia. San Francisco (CA): Wikimedia Foundation, 2024, 6. 12. 2024 v 23:10. Dostupné z: https://cs.wikipedia.org/wiki/Automatizace. [cit. 2024-12-09].

2. Popište základní požadavky na IoT a automatizaci a to jak z pohledu samotné funkčnosti a odolnosti zařízení, tak i z pohledu safety a security. Následně **prodiskutujte**, co je stejné a v čem se IoT od automatizace liší. :smiley:

3. Vyberte si určitý segment produktů pro IoT (podle vašich zájmů) a podívejte se jaké jsou v této oblasti novinky. Následně během **diskuze** sdělte zjištěné informace ostatním. :smiley:


### 2. Komunikace MCU s okolím

1. Připojte MCU k počítači a zprovozněte obousměrnou komunikaci po sériové lince s terminálem (někdy se též označuje jako monitor). 

2. Nastavte BT nebo WIFI a opět zkuste zprovoznit, tentokrát bezdrátovou komunikaci. K přijímání a odesílání dat můžete zkusit opět terminál. 


### 3. IoT lampička

1. Vytvořte z MCU jednoduchý HTML server. Na webové stránce bude tlačítko (lze použít dvě tlačítka) a kontloka (stačí v podobě URL odkazu a textu), tlačítko bude zapínat/vypínat LED připojenou k MCU, kontrolka zobrazí aktuální stav této LED. 

2. Místo realizace webového serveru připojte MCU k IoT cloudové službě (např. [Blynk IoT](https://blynk.io/), [Arduino Cloud](https://www.arduino.cc/),...) a ovládejte LED přes prostředí této cloudové služby.


### 4. IoT senzor teploty (příp. i vlhkosti)

1. K MCU připojte senzor/čidlo teploty a posílejte tato data do počítače po sériové lince.

2. Porovnejte měření teploty s jiným teploměrem a zkuste určit charakter chyba měření. Následně navrhněte, jak by se tyto chyby dali eliminovat.

    <details>
        <summary> :bulb: Tip: </summary>
            Pro porovnání bude potřeba změřit více hodnot a sestavit graf. Čím větší rozsah senzoru/čidla je proměřen, tím budou některé druhy chyb viditelnější. Podobně to platí i o počtu naměřených hodnot. Některé druhy chyb se dají eleminovat např. přičtením/odečtením konstanty, jiné mají charakter matematické funkce, další chyby se dají odstranit stálejším měřícím prostředím, eliminováním vnějších vlivů, a některé chyby nelze v našich podmínkách eliminovat vůbec.
    </details>

> :key: **Chyba měření**
>
> Chyba měření. Online. In: Wikipedia: the free encyclopedia. San Francisco (CA): Wikimedia Foundation, 2024, 8. 10. 2024 v 17:34. Dostupné z: https://cs.wikipedia.org/wiki/Chyba_m%C4%9B%C5%99en%C3%AD. [cit. 2024-12-10].

3. Opět připojte MCU ke cloudové službě (např. [Tmep](https://tmep.cz/), [Blynk IoT](https://blynk.io/), [Arduino Cloud](https://www.arduino.cc/),...) a naprogramujte jednoduchý IoT teploměr (případně vlhkoměr). 

Pozn.: Pokud bydlíte ve starším domě a řešíte problém tvorby plísní na zdech, zkuste tento senzor vlhkosti použít k dlouhodobému měření. Pokud bude po většinu času relativní vlhkost výrazně vyšší jak 50 %, je třeba primárně zajistit lepší odvětrání vlhkého vzduchu, jelikož relativní vlhkost nad 50 % podporuje tvorbu těchto plísní. Samozřejmě toto řešení nemusí stačit, ale může napomoci řešení problému.
Pokud se rozhodnete používat neplacenou verzi cloudové služby, zjistěte si, zda vaše data nejsou veřejná. Měření teploty a vlhkosti v interiéru může být jednou z bezpečnostních hrozeb.
V případě venkovní meteostanice tento problém tolik nehrozí.
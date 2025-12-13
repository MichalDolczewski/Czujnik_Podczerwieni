# 🚀 Zdalnie Sterowany Przełącznik LED IR (PNP Switch Demonstrator)

## 🌟 Opis Projektu

Ten projekt prezentuje budowę i działanie układu do zdalnego sterowania oświetleniem LED, wykorzystującego sygnały podczerwone (IR). Głównym celem projektu jest demonstracja:

1.  **Integracji Czujnika IR (TSOP34838):** Układ odbiera sygnał z dowolnego pilota IR i przetwarza go na sygnał sterujący.
2.  **Zastosowania Tranzystora PNP (S8550) jako Wzmacniacza/Przełącznika:** Tranzystor PNP jest użyty jako przełącznik górnej strony (**High-Side Switch**), który kontroluje przepływ prądu do diod LED. Tranzystor wzmacnia słaby prąd z wyjścia TSOP do poziomu wymaganego przez diody LED.

**Status Nasycenia:** Ze względu na specyficzne parametry użytego modelu tranzystora S8550 oraz ograniczenia prądowe sterownika (TSOP), układ **demonstruje wyraźne włączanie/wyłączanie LED**, jednak tranzystor może pracować w **obszarze aktywnym** (z $V_{CE}$ wyższym niż typowe $0.2 \text{V}$), zamiast idealnego nasycenia. Pomimo to, funkcjonalność sterowania jest w pełni zachowana.

---

## 📋 Użyte Komponenty (Bill of Materials – BOM)

| Komponent | Symbol | Wartość/Typ | Funkcja | Ilość |
| :--- | :--- | :--- | :--- | :--- |
| Tranzystor PNP | T1 | **S8550** | Wzmacniacz prądu | 1 |
| Odbiornik IR | U1 | **TSOP34838** | Odbiór sygnału z pilota IR (wyjście LOW-Active) | 1 |
| Dioda LED | D1, D2, D3 | **Czerwona, Zielona, Niebieska** | Obciążenie / Wskaźniki świetlne | 3 |
| Rezystory LED | R4, R5, R6 | **100 $\Omega$** | Ograniczenie prądu dla każdej diody LED (połączenie równoległe) | 3 |
| Rezystor Bazy | R\_base | **1 k$\Omega$** | Bezpieczne ograniczenie prądu $I_B$ | 1 |
| Kondensator Filtracji | C1 | **220 $\mu\text{F}$** | Filtracja tętnień zasilania (elektrolityczny) | 1 |
| Kondensator Odprzęgający| C2 | **100 $\text{nF}$** | Odprzęganie szumów (ceramiczny) | 1 |
| Zasilanie | BAT1 | **4.5 V** (3x AA) | Źródło zasilania układu | 1 |

---

## 📐 Schemat Ideowy

Poniżej znajduje się schemat ideowy, który przedstawia prawidłową konfigurację **przełącznika górnej strony (PNP High-Side Switch)**, sterowanego z TSOP.

![Schemat ideowy przełącznika IR z tranzystorem PNP S8550](images/schemat_finalny.png)

---

## 📸 Galeria Zdjęć

### Zdjęcie Ukończonego Układu

![Zdjęcie gotowego układu na płytce stykowej](images/uklad_gotowy.jpg)

### Weryfikacja Działania (Wzmacnianie Prądu)

Zdjęcie lub wykres z pomiaru potwierdzające spadek napięcia na tranzystorze ($V_{CE}$) w stanie WŁĄCZ (nawet jeśli jest w obszarze aktywnym).

**[MIEJSCE NA WYKRES LUB ZDJĘCIE POMIARU $V_{CE}$]**

---

## 📺 Demonstracja Działania (Video)

Poniższy link prowadzi do pełnej demonstracji wideo, która przedstawia włączanie i wyłączanie diod LED za pomocą pilota IR, pokazując udaną integrację TSOP i tranzystora.

```markdown
**Link do Wideo:** [https://youtu.be/](https://youtu.be/)[TWÓJ_LINK_DO_WIDEO]

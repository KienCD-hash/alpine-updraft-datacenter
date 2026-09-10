# Thermodynamische und techno-ökonomische Bewertung unterirdischer Naturzug-Schrägschächte zur passiven Kühlung und Energierückgewinnung in Hyperscale-KI-Rechenzentren

**Autor:** Chu Duc Kien (mailiekien@icloud.com)  
**Status:** Ausgearbeitetes Paper (Open Publication)  
**Datum:** 11. September 2026  
**Format:** IEEEtran / Academic Research Paper  

---

## Abstract
Der exponentielle Anstieg von Trainingslasten künstlicher Intelligenz erfordert Rechenzentrumsleistungen im dreistelligen Megawatt-Bereich. Herkömmliche Kühlinfrastrukturen stoßen durch extremen Hilfsstrombedarf (Power Usage Effectiveness, PUE) und massiven Frischwasserverbrauch (Water Usage Effectiveness, WUE) an ökologische und infrastrukturelle Grenzen. Dieser Beitrag untersucht ein neuartiges Anlagenkonzept: die Kopplung eines flüssigkeitsgekühlten 100-MW-KI-Rechenzentrums mit einem bergmännisch aufgefahrenen Schrägschacht ($\Delta z = 1.500\,\text{m}$) zur Realisierung eines passiven Naturzug-Kühlsystems mit integrierter Energierückgewinnung. 

Thermodynamische Berechnungen zeigen, dass bei einer Kühlwassertemperatur von $60\,^\circ\text{C}$ ein kontinuierlicher Auftrieb mit einem Massenstrom von rund $4.480\,\text{kg/s}$ induziert wird. Neben der vollständigen Eliminierung des mechanischen Kühlstrombedarfs ($\sim 4{,}0\,\text{MW}_{\text{el}}$) und des jährlichen Wasserbedarfs ($\sim 1{,}58 \cdot 10^6\,\text{m}^3$) ermöglicht eine Basisturbine die Rückspeisung von rund $2{,}25\,\text{MW}_{\text{el}}$, wodurch der rechnerische PUE auf unter **1,01** sinkt. Eine techno-ökonomische Lebenszyklusanalyse belegt, dass sich die Mehrinvestition des Schachtbaus durch jährliche Betriebskosteneinsparungen von über **10 Mio. Euro** amortisiert.

---

## Key Performance Indicators (KPIs)

| Metrik / Parameter | Konventionelles RZ (100 MW) | Alpine Hangkanal-Kopplung | Vorteil |
|---|---|---|---|
| **PUE (Power Usage Effectiveness)** | 1,15 – 1,25 | **< 1,01** (rechnerisch ~1,0075) | Eliminierung von ~4 MW Kühlstrom |
| **WUE (Water Usage Effectiveness)** | 1,5 – 2,0 L/kWh (~1,58 Mrd. L/Jahr) | **0,0 L/kWh** | 100% Einsparung von Trinkwasser |
| **Rückverstromung (Turbine)** | 0,0 MW | **+2,25 MWel** | Dauerhafte Stromeinspeisung ins Netz |
| **Jährliche OPEX-Ersparnis** | Reference | **~10,17 Mio. € / Jahr** | Strom + Wasser + Wartung |
| **50-Jahre Kapitalwert (NPV50)** | Reference | **+162,3 Mio. €** | Trotz ~198 Mio. € Netto-CapEx |

---

## Systemarchitektur & Kernerkenntnisse

```mermaid
graph TD
    A["100 MW KI-Rechenzentrum (SXM5 H100 / Blackwell Racks)"] -->|Direct Liquid Cooling 60°C| B["Flüssig-Luft-Wärmetauscher am Schachtfuß"]
    B -->|Erwärmt Zuluft 20°C auf 40°C| C["3.000 m Schrägschacht (1.500 m Höhendifferenz)"]
    C -->|Thermosiphon / Kamineffekt ~4.480 kg/s| D["Axial-Basisturbinen am Fußpunkt"]
    D -->|2,25 MW Netto-Stromerzeugung| E["Rückspeisung / Eigenverbrauch"]
    C -->|Austritt am Gipfelportal| F["Passiver Naturzug-Kühlturm (Zero Fans & Zero Water)"]
```

### Die 3 Kernhebel des Konzepts:
1. **Der Perspektivenwechsel (Vom Kraftwerk zum Kühler):**  
   Klassische Solar- / Aufwindkraftwerke scheiterten historisch oft an niedrigen Wirkungsgraden (2–5%). Als **passiver Kühler** genutzt, kehrt sich die Logik um: Der Schacht ersetzt teure Lüfterwände und Chiller, spart ~4 MW Hilfsstrom und liefert als *Gratis-Nebenprodukt* 2,25 MW echten Strom.
2. **Zero Water Consumption:**  
   Keine evaporative Kühlung. Vermeidet den Verbrauch von 1,58 Milliarden Litern Trinkwasser pro Jahr.
3. **Physische Resilienz im Berg:**  
   Unterirdische Kaverne im Granit-/Gneisgestein bietet Höchstschutz vor Witterung, Lawinen, EMP und Sabotage.

---

## Projektdateien im Workspace

- [`paper.tex`](file:///Users/chuk/.gemini/antigravity/scratch/rechenzenter/paper.tex) - Vollständiger, kompilierbarer LaTeX-Code im IEEEtran-Format.
- [`paper_konzept.md`](file:///Users/chuk/.gemini/antigravity/scratch/rechenzenter/paper_konzept.md) - Diese Dokumentation.
- [`README.md`](file:///Users/chuk/.gemini/antigravity/scratch/rechenzenter/README.md) - Projekt-Übersicht & Anleitung.

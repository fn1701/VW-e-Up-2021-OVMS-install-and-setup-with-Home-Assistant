# VW e-Up! Installation OVMS

Basierend auf [https://docs.openvehicles.com/en/latest/components/vehicle\_vweup/docs/#variant-1](https://docs.openvehicles.com/en/latest/components/vehicle_vweup/docs/#variant-1)

Verbindung zum Comfort-CAN über den OCU-T26A-Stecker herstellen

Es muss eine Verbindung zwischen dem OBD2- und dem OCU-Anschluss hergestellt werden. Wenn das OVMS in der Nähe des OBD2-Anschlusses installiert wird, muss ein Kabel zum Anschluss an den T26A-Stecker angefertigt werden (oder das T26A-Kabel dort angezapft werden). Wird das OVMS anstelle des OCU installiert, muss der OBD2-CAN-Bus von dort verbunden werden.

Ein Adapterkabel muss mit den folgenden Verbindungen hergestellt werden:

<details>
<summary>Bild: OVMS-OBD2-T26A-Cable.jpg</summary>

[![OVMS-OBD2-T26A-Cable.jpg](images/OVMS-OBD2-T26A-Cable.jpg)](https://docs.openvehicles.com/en/latest/_images/DSC00373_1024.JPG)

</details>

Das Kabel zwischen dem OBD-Stecker und dem DB9-F-Stecker muss **verdrillt** sein, um Übertragungsprobleme zu vermeiden. Ein gutes Kabel dafür ist ein doppelt geschirmtes CAT-5- oder CAT-6-Netzwerkkabel. Achten Sie darauf, **CAN High**, **CAN Low** UND **Masse** zu verbinden.

> \[!NOTE]
> Die Pin-Nummerierung des VW T26a folgt nicht dem IT-Standard (Zick-Zack), sondern hat stattdessen die Pins 1–13 von links nach rechts in der oberen Reihe und 14–26 von links nach rechts in der unteren Reihe. Siehe Bild oben.

<details>
<summary>Bild: T26a-Pins.jpg</summary>

[![T26a-Pins.jpg](images/T26a-Pins.jpg)](https://docs.openvehicles.com/en/latest/_images/T26a-Pins.jpg)

</details>

| T26 | DB9-F | OBD | Signal                    |
| --- | ----- | --- | ------------------------- |
| 26  | 3     | 4   | Masse / Fahrzeug-Minus    |
| -   | 2     | 14  | can1 L (OBD2 CAN Low)     |
| -   | 7     | 6   | can1 H (OBD2 CAN High)    |
| -   | 4     | -   | can2 L (nicht verwendet)  |
| -   | 5     | -   | can2 H (nicht verwendet)  |
| 2   | 6     | -   | can3 L (Comfort-CAN Low)  |
| 14  | 8     | -   | can3 H (Comfort-CAN High) |
| 1   | 9     | -   | +12V Bordspannung         |

<details>
<summary>Bild: OVMS-OBD2-T26A-Cable_Schematic.svg</summary>

![OVMS-OBD2-T26A-Cable_Schematic.svg](images/OVMS-OBD2-T26A-Cable_Schematic.png)
</details>
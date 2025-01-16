# FIDO - Passwordless Authentication Process

## Warum sind Passwörter unsicher?

Passwörter gelten als unsicher, da viele Menschen einfache oder wiederholte Passwörter nutzen, die leicht erraten werden können. Zudem sind sie anfällig für Angriffe wie Phishing, Brute-Force-Versuche und Datenlecks, wodurch sie oft eine Schwachstelle im Sicherheitskonzept darstellen.

## Wie funktioniert eine passwortlose Anmeldung?

Eine passwortlose Anmeldung ersetzt Passwörter durch ein Public-/Private-Key-Verfahren. Dabei generiert ein Gerät, wie ein Smartphone oder Sicherheitsschlüssel, ein Schlüsselpaar. Der private Schlüssel bleibt sicher auf dem Gerät, während der öffentliche Schlüssel mit dem Server geteilt wird. Zur Authentifizierung signiert der private Schlüssel eine serverseitige Herausforderung, die der Server mit dem öffentlichen Schlüssel überprüft.

## Warum ist die Anmeldung mit einer PIN vorteilhaft?

Eine PIN wird ausschließlich lokal auf dem Gerät verarbeitet und niemals über das Netzwerk übertragen. Dadurch wird sie sicherer gegen Angriffe von außen. Die PIN entsperrt den privaten Schlüssel des Geräts, der dann für die Anmeldung genutzt wird. Dies kombiniert die Einfachheit einer PIN mit der Sicherheit kryptografischer Verfahren.

## Welche Faktoren spielen bei der Authentifizierung eine Rolle?

Ein Authentifizierungsverfahren kann folgende Faktoren umfassen:
1. **Wissen**: Etwas, das der Benutzer kennt (z. B. Passwort oder PIN).
2. **Besitz**: Etwas, das der Benutzer besitzt (z. B. Smartphone oder Sicherheitsschlüssel).
3. **Biometrie**: Etwas, das der Benutzer ist (z. B. Fingerabdruck oder Gesichtserkennung).

## Wie können Passwörter durch Passkeys ersetzt werden?

Ein Passkey basiert auf der Verwendung von kryptografischen Schlüsseln. Der private Schlüssel bleibt sicher auf dem Gerät, während der öffentliche Schlüssel auf dem Server gespeichert wird. Statt ein Passwort einzugeben, signiert der private Schlüssel eine serverseitige Anfrage, was sicherer ist, da der private Schlüssel nie das Gerät verlässt.

## Wie funktioniert das Public-/Private-Key-Verfahren?

Dieses Verfahren nutzt ein Schlüsselpaar:
- **Privater Schlüssel**: Wird auf dem Gerät sicher gespeichert und signiert Anfragen.
- **Öffentlicher Schlüssel**: Wird mit dem Server geteilt und dient der Verifikation.

Bei der Anmeldung signiert der private Schlüssel eine serverseitige Herausforderung, und der Server prüft die Signatur mit dem öffentlichen Schlüssel. Dadurch wird sichergestellt, dass nur das Gerät mit dem privaten Schlüssel die Anmeldung durchführen kann.

## Wie funktioniert das digitale Signieren?

Digitale Signaturen entstehen so:
1. Der Benutzer erstellt mit seinem privaten Schlüssel eine Signatur einer Nachricht (z. B. einer Authentifizierungsanfrage).
2. Die signierte Nachricht wird an den Server gesendet.
3. Der Server nutzt den öffentlichen Schlüssel, um die Authentizität der Signatur zu prüfen und die Nachricht zu validieren.

## Zeichnung

Erstellen Sie eine Zeichnung mit folgenden Elementen:
1. Ein Smartphone oder Sicherheitsschlüssel, der eine Herausforderung signiert.
2. Ein Server, der die Signatur überprüft.
3. Symbole für private und öffentliche Schlüssel (z. B. ein Schloss für den privaten Schlüssel und ein offenes Schloss für den öffentlichen Schlüssel).

## Was macht das FIDO-Verfahren so sicher?

Das FIDO-Verfahren schützt vor Phishing, Passwortdiebstahl und anderen Angriffen, da keine Passwörter genutzt werden. Es setzt auf moderne Sicherheitsstandards wie starke Verschlüsselung und Multi-Faktor-Authentifizierung, die den Besitz eines Geräts und/oder biometrische Daten kombiniert.

## Warum ist das System noch nicht weit verbreitet?

Das FIDO-System ist noch nicht allgegenwärtig, da:
1. Unternehmen zunächst in die neue Technologie investieren müssen.
2. Nicht alle Nutzer über die notwendigen Geräte verfügen.
3. Zeit und Schulungen nötig sind, um Benutzer und IT-Abteilungen mit der neuen Methode vertraut zu machen.

![image](Bilder/Fido.png)
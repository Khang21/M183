# Lern-Bericht
Khang Cung

## Einleitung

Wir befinden uns im Modul 1. In diesem Modul erweitern wir unser JSF wissen und lernen über potenzielle Hacking Angriff.

## Was habe ich gelernt?
Ich habe sehr viele Hacking Methoden gelernt, aber in diesem Lernbericht werde ich über die "Session Pinning" Methode gehen.

## Beschreibung

Session Fixation ist ein Angriff, der es einem Angreifer ermöglicht, eine gültige Benutzersitzung zu kapern. Der Angriff nutzt eine Einschränkung in der Art und Weise aus, wie die Webanwendung die Sitzungs-ID verwaltet, genauer gesagt die anfällige Webanwendung. Bei der Authentifizierung eines Benutzers wird keine neue Sitzungs-ID zugewiesen, so dass es möglich ist, eine bestehende Sitzungs-ID zu verwenden. Der Angriff besteht darin, sich eine gültige Sitzungsnummer zu beschaffen, einen Benutzer dazu zu bringen, sich mit dieser Sitzungsnummer zu authentifizieren, und dann die vom Benutzer bestätigte Sitzung durch die Kenntnis der verwendeten Sitzungsnummer zu entführen. Der Angreifer muss eine legitime Sitzungs-ID für eine Webanwendung bereitstellen und versuchen, den Browser des Opfers dazu zu bringen, diese zu verwenden.

![image](https://media.geeksforgeeks.org/wp-content/uploads/20220711160012/sessionfixationattack.png)


![image](https://i.ibb.co/0M1h1PJ/Screenshot-2022-12-14-225843.png)
```
http://localhost:8080/InsecureApp/faces/secured/index.xhtml;jsessionid=25e3a632733dc737e26b434912ef
```
Falls der böser Hacker diesen Session Link bekommen kann, nachdem der Benutzer sich eingeloggt hat, könnte er auf Daten vom Benutzer klauen. 

Natürlich kann man diesen Problem lösen. Jedoch ist es wenig kompliziert. <br>
-Die Standardmethode besteht darin, die Sitzungs-ID direkt nach der Anmeldung des Benutzers zu ändern. Dadurch werden die meisten Schwachstellen bei der Sitzungsfixierung beseitigt.<br>
-Außerdem sollten Sie Sitzungs-IDs nach einer Zeitüberschreitung ungültig machen. So sollte beispielsweise nach 10 Minuten ohne Aktivität eine automatische Abmeldung erfolgen. Dies gibt dem Angreifer ein kleines Zeitfenster, in dem er die feste Sitzungs-ID verwenden kann.
-etc.

## Verifikation

Am kurzen Erklärungstext zum Session Pinning, kann man erkennen, dass ich verstanden habe, wie man eine unsichere Seite ein Passwort vom Benutzer oder besser vom Admin bekommen. 

# Reflektion zum Arbeitsprozess

Ich bin nicht zur Frieden mit meiner Arbeitseinteilung. Ich hatte immer länger gebraucht als die eingeschätzte Zeit. Ich weiss nicht, ob es nur bei mir der Fall ist oder ob ich einfach die Aufgaben zu wenig verstehe. 

Für JSF gibt es auf Youtube nicht bis gar keine Tutorials 

**VBV**: Ich werde bei neueren Aufträge die Präsentationen genauer durch lesen.

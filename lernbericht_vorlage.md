# Lern-Bericht
Khang Cung

## Einleitung

Wir befinden uns im Modul 1. In diesem Modul erweitern wir unser JSF wissen und lernen über potenzielle Hacking Angriff.

## Was habe ich gelernt?
Ich habe sehr viele Hacking Methoden gelernt, aber in diesem Lernbericht werde ich über die "Session Pinning" Methode gehen.

## Beschreibung

Session Fixation ist ein Angriff, der es einem Angreifer ermöglicht, eine gültige Benutzersitzung zu kapern. Der Angriff nutzt eine Einschränkung in der Art und Weise aus, wie die Webanwendung die Sitzungs-ID verwaltet, genauer gesagt die anfällige Webanwendung. Bei der Authentifizierung eines Benutzers wird keine neue Sitzungs-ID zugewiesen, so dass es möglich ist, eine bestehende Sitzungs-ID zu verwenden. Der Angriff besteht darin, sich eine gültige Sitzungsnummer zu beschaffen, einen Benutzer dazu zu bringen, sich mit dieser Sitzungsnummer zu authentifizieren, und dann die vom Benutzer bestätigte Sitzung durch die Kenntnis der verwendeten Sitzungsnummer zu entführen. Der Angreifer muss eine legitime Sitzungs-ID für eine Webanwendung bereitstellen und versuchen, den Browser des Opfers dazu zu bringen, diese zu verwenden.

Übersetzt mit www.DeepL.com/Translator (kostenlose Version)
![image](https://media.geeksforgeeks.org/wp-content/uploads/20220711160012/sessionfixationattack.png)


![image](https://i.ibb.co/0M1h1PJ/Screenshot-2022-12-14-225843.png)
```
http://localhost:8080/InsecureApp/faces/secured/index.xhtml;jsessionid=25e3a632733dc737e26b434912ef
```
Falls der böser Hacker diesen Session Link bekommen kann, nachdem der Benutzer sich eingeloggt hat, könnte er auf Daten vom Benutzer klauen. 

Auf der 1. Seite wird der Benutzer seinen Namen in einem Textfeld eingeben müssen. Danach auf die Submit Link klicken, welches ihn auf der Seite 2 weiterleitet.
Dazwischen wird das Programm durch die HelloManagedBean Controller laufen. Im Controller wird die obrigen Code durchlaufen. Der Benutzers Name wird im Variable lastName gespeichert.
Auf der 2. Seite wird die oben gespeicherte Variable wieder mit #{ControllerName.Variable} aufgerufen. 

## Verifikation

Am kurzen Erklärungstext zum ManagedBean, kann man erkennen, dass ich verstanden habe, wie man Eingaben von einer Seite auf der anderen anzeigen kann. 
Der Code beinhaltet, die wichtigsten Stellen, zum dies wiederherzustellen.

# Reflektion zum Arbeitsprozess

Ich bin mit meiner Arbeit bisher in JSF zufrieden. Ich lerne nicht gerne, neue Sprachen, weil ich bisher schon viele gelernt habe. Aber bei JSF war es eine Ausnahme, weil wir immernoch mit HTML und Java programmieren, jedoch wird es nur bei der HTML Seite anders. Dies war mir eine Herausforderung am Anfang, aber nach der Zeit verlief es mir gut.

Ich habe zur Beginn dieses Projektes sehr viel Mühe gehabt, überhaupt die Vorlage Page zu starten. Wir hatten meiner Meinung nach zu wenig Zeit gehabt, die nötigen JDKs und Netbeans etc zu installieren.

**VBV**: Ich werde bei neueren Aufträge einen kurzen Pseudo Code schreiben, damit ich schneller Fehlern beheben kann

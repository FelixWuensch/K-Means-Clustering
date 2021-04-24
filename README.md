# K-Means-Clustering
Prüfungsaufgabe 1 - Dritter Teil

Um dieses Projekt zu starten, folgen Sie dem Binder Badge:      [![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/FelixWuensch/K-Means-Clustering/main)

# Ausführung der Übungsaufgabe

!!! Alle Befehle werden ausgeführt in dem die Zeile ausgewählt wird und anschließend mit Shift (Großschreibtaste) und Enter gestartet wird !!!

1. Im ersten Schritt müssen alle benötigten Libraries installiert und importiert werden, so dass im Folgenden alle Befehle erfolgreich ausgeführt werden können.

2. Danach werden unsere Daten im CSV Format eingelesen.

3. Daraufhin werden die Daten wieder begutachtet mit den üblichen drei Funktionen: .info(), .descrive(), .head().

4. Dann gehen wir über und starten mit der explorativen Datenanalyse. Dafür erstellen wir einen Scatterplot von "Grad.Rate" vs. "Room.Board" und lassen diese nach dem Kriterium „Privat aufteilen. Dabei lassen wir uns jedoch die Regressionsgerade nicht anzeigen. Das gleiche machen wir noch einmal mit "F.Undergrad" vs. "Outstate".

5. Im fünften Schritt wird ein Histogramm mit zwei Betrachtungen erstellt. Dafür soll die Spalte "Out of State Tuition" aufgeteilt werden nach der Spalte "Private". Dasselbe lassen wir und noch einmal anzeigen für die Spalte "Grad.Rate". Beim Betrachten dieses zweiten Histogramms fällt auf, dass es einen Wert über 100 gibt. Da die Daten die Abschlussrate ("Grad.Rate") betrachten, ist es jedoch nicht möglich, dass es über 100 Prozent gibt. Somit müssen wir den Wert anpassen, was wir im nächsten Schritt unternehmen. Dazu lassen wir uns anzeigen, welche Universität dies ist und setzen dann den Wert dieser Universität auf 100. Dann lassen wir uns das Histogramm noch mal mit dem Korrigierten Wert anzeigen und nun macht das ganze auch Sinn.

6. Dann beginnen wir mit der Vorbereitung für das Clustern. Dafür importieren wir die entsprechenden Funktionen von Sklearn. Als zweites erstellen wir dann auch gleich ein K Means Modell mit 2 Clustern. Dann trainieren wir die Daten mit der fit-Methode und den Daten, außer der „Private“ Spalte und lassen uns dann die Cluster Zentrumsvektoren ausgeben.

7. Nach dem wir das Model trainiert haben, müssen wir uns noch die „Private“ Spalte konvertieren, da Boolean Werte nicht verarbeitet werden können. Dafür schreiben wir uns eine Methode, welche die „True“ Werte in eine „1“ umwandelt und die „False“ Werte in eine „0“. Die Methode wenden wir dann auf die „Private“ Spalte an und lassen uns den Head des Dataframes mit unserer neuen Spalte anzeigen.

8. Dann importieren wir die Confusion Matrix und den Classification Report und lassen uns direkt die Confusion Matrix ausgeben, mit der Dataframe Spalte „Clustering“, welche wir eingefügt haben, und den K Means Labels. Ebenso lassen wir uns den Classification Report mit diesen Parametern ausgeben. Daraus lässt sich wieder ablesen wie gut die Werte vorhergesagt wurden. Anhand des F1-Scores zeigt sich, dass die Werte gut sind, da man berücksichtigen muss das es sich hierbei ja um eine Unsupervised Methode handelt.


Damit ist das Kapitel des K-Means-Clustering abgeschlossen. Wir haben uns dafür die Daten genauer angeschaut mit der explorativen Datenanalyse. Dann haben wir das Model erstellt, trainiert und die Spalte „Clustering eingeführt und die Daten in ein verarbeitbares Format konvertiert. Zu guter Letzt haben wir die Genauigkeit des Clusters angeschaut und bewertet. Somit gehen wir weiter zum Thema Recomender Systems.


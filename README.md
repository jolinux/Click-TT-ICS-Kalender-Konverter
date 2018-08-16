# Click-TT-ICS-Kalender-Konverter


Click-TT verwaltet viele Tischtennisspiele in Deutschland. Auch in meinem Dorf wird vereinsmäßig Tischtennis gespielt.
Nach den Spielterminfestlegungen der jeweiligen Spielklassen wird von Click-TT eine CSV-Datei mit allen 
Spielterminen meines Vereins in den Downloadbereich eingestellt. (Achtung: dieser ist nur über Login erreichbar)

Hier möchte ich meine kleine Toolsammlung vorstellen, mit der man von dem Click-TT-CSV-Format vollautomatisch 
zu einer bzw. mehreren Manschafts- ICS-Kalenderdatei kommt.


Herzstück ist das Bash-Script 

convert_csv_to_ics.sh

( Gefunden habe ich es im Internet https://www.openoffice-forum.de/viewtopic.php?t=5400#p13776 , als Orginalquelle wird das
Macwelt-Forum benannt. Danke an den Ersteller John L. vom 18.08.2010) 


Das Orginal kommt wegen Funktionslücken so nicht zum Einsatz, es wird ersetzt durch eine Erweiterung als

my_convert_csv_to_ics.sh

*****************************************************************************************************************
Ein vorgesetztes Aufruf-Script übernimmt die gesamte Steuerung. 
Hier wären auch die Anpassung für einen anderen Verein vorzunehmen.

- alle echo-Anweisungen mit String "MTV-..."
- alle awk-Anweisungen mit "MTV Vollbüttel"
- alle grep-Anweisungen mit "MTV...."
abändern

csv-ics.sh


Diesem Script wird das Argument click-tt.csv (z.B. Vereinsspielplan_20180815134857.csv ) übergeben


so ist der Aufruf:

./csv-ics.sh Vereinsspielplan_20180815134857.csv


*****************************************************************************************************************
Ein zusätzlich notwendiges awk-Script ist 

daten_merge.awk

*****************************************************************************************************************
Die drei Daten sind in der Zip-Datei.


Viel Spaß

Jörg Alpers
 


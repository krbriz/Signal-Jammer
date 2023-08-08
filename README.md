# Signal-Jammer
Visas signālu bloķētāju shēmas parasti sastāv no trīs “apakšķēdēm”: frekvences pastiprinātāja, frekvences regulētāja un sprieguma kontroles ķēdes . Šajā shēmā pastiprinātāja daļa sastāv no tranzistora Q1 un kondensatoriem C4 un C5, kurus izmanto, lai pastiprinātu signālu, kas plūst no regulējošās ķēdes. Frekvences regulējošā ķēdes daļa sastāv no maiņkondensatora un divām spolēm – L1 un L2. Šādi tiek radīta ķēde, kas darbojas kā filtrs. Ņemot vērā, ka koplietošanas reģions ir 2400-2483,5 Mhz, nepieciešams antenas komponenti uzstādīt tā, lai eksperimentu rezultātā varētu regulēt frekvenci. Lai regulētu frekvenci tiek izvēlēts maiņkondensators.
Lai aprēķinātu nominālus antenas slēguma daļā, tiek izmantota sekojoša formula: 
F=1/((2*pi*√(((L1*L2)*C_maiņkond)))   ).  Kā “izejas” frekvence tiek iestatīta vidējā frekvence koplietošanas reģionā. 2,442*10^9=1/((2*3,1416*√(((L1*L2)*C_maiņkond)))   ).  Ja mēs uzdodam L_1=L_2=4,7*10^(-6) H jeb 4,7 uH, tad sanāk sekojošs vienādojums: 1/(6,2832 sqrt(1/(〖2,2〗^6*〖2,2〗^6 )*Cmaiņkond))=2,442*10^9 , izsakot C_maiņkond, iegūstam:  4,9*10^(-13)  F jeb 0,38 pF. Saskaņā ar katalogiem šāda nomināla maiņkondensators ir pieejams (piem. Murata Electronics piedāvā maiņkondensatoru ar regulēšanas iespējām no 0.25-0.7 pF vai 0.30-1.25 pF). Sanāk, ka spoles nomināls ir samērā liels – 4,9 uH.
# LT Spice simulācija
![PCB](./LT_spice1.PNG)

![Case](./LT_spice2.PNG)

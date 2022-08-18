Praksa pri AFormX

ukazi:

- blockMesh 
- snappyHexMesh (-overwrite) 
    - v datoteki snappyHexMeshDict - spremeniti ime datoteke, jo poimenovati in ta name uporabiti skozi celotno datoteko
    ime datoteke spremeniti tudi v imeniku 0/ (ime je trup)
    - (-overwrite) vse zapiše v file 0 in ne naredi file 1, 2, 3.
        - če narediš file 1, 2, 3
        controlDict vrstico startFrom spremeni v latestTime
        kopiraš file (količine) iz 0 v 3 
        checkBox v ParaView: Skip Zero Time 
- checkMesh
- simpleFoam -postProcess -func yPlus - vrednosti y+, y+ = količina celic nad površjem 
- surfaceCheck <file.stl> - preveri površino, če je vse closed in če se vse dotika 
- surfaceAdd <file1.stl> <file2.stl> output - združi datoteki file1 in file2
- surfaceFeatureExtract - v sodelovanju z surfaceFeatureExtractDict izvozi površje, da lahko potem sMH lepo prilagodi površje
- surfaceFeatureEdges - cfMesh

decomposeParDict: 
 - uporabi metodo scotch, ker razdeli število celic enakomerno med vse procesorje in poskrbi, da je najmanj face-ov
 - poženi decomposePar 
 - mpirun (komunikacija med procesorji) -np 4 (stevilo procesov - jeder) simpleFoam -parallel
 - reconstructPar

uporabljena kalkulatorja za izračun k, \omega:

https://www.omnicalculator.com/physics/reynolds-number#laminar-vs-turbulent-flow-laminar-flow-reynolds-number-turbulent-flow-reynolds-number

http://ichrome.com/blogs/archives/342

Reynold's number for airplanes: http://www.aerodrag.com/Articles/ReynoldsNumber.htm

StackExchange - Reynold's number: https://engineering.stackexchange.com/questions/5713/how-to-determine-the-characteristic-length-in-reynolds-number-calculations-in-ge

več objektov v enem .stl file-u https://www.cfd-online.com/Forums/openfoam/218118-naming-regions-stl-file-snappyhexmesh.html

y+ https://www.simscale.com/forum/t/what-is-y-yplus/82394 (also poglej Fluid Mechanics 101)

maybe baby - https://www.cfd-online.com/Forums/openfoam-pre-processing/178127-one-more-time-wall-functions-sst.html

ReThetat - https://www.openfoam.com/documentation/guides/latest/doc/guide-turbulence-ras-k-omega-sst-lm.html in u_infinity naj bi bil bulk flow condition - hitrost, ki jo ima večina kapljevine (CFDYourself - what is ReThetat?)
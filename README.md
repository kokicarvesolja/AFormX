Praksa pri AFormX

Ta file vsebuje tudi ukaze z razlago za OpenFOAM 

blockMesh 
snappyHexMesh (-overwrite) 
    - v datoteki snappyHexMeshDict - spremeniti ime datoteke, jo poimenovati in ta name uporabiti skozi celotno datoteko
    ime datoteke spremeniti tudi v imeniku 0/ (ime je trup)
    - (-overwrite) vse zapiše v file 0 in ne naredi file 1, 2, 3.
        - če narediš file 1, 2, 3
        controlDict vrstico startFrom spremeni v latestTime
        kopiraš file (količine) iz 0 v 3 
        checkBox v ParaView: Skip Zero Time 
checkMesh

uporabljena kalkulatorja za izračun k, \omega, 

https://www.omnicalculator.com/physics/reynolds-number#laminar-vs-turbulent-flow-laminar-flow-reynolds-number-turbulent-flow-reynolds-number

http://ichrome.com/blogs/archives/342

Reynold's number for airplanes: http://www.aerodrag.com/Articles/ReynoldsNumber.htm

StackExchange - Reynold's number: https://engineering.stackexchange.com/questions/5713/how-to-determine-the-characteristic-length-in-reynolds-number-calculations-in-ge

simpleFoam -postProcess -func yPlus

surfaceAdd file1 file2 output

več objektov v enem .stl file-u https://www.cfd-online.com/Forums/openfoam/218118-naming-regions-stl-file-snappyhexmesh.html

y+ https://www.simscale.com/forum/t/what-is-y-yplus/82394 (also poglej Fluid Mechanics 101)


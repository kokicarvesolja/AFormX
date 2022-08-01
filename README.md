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
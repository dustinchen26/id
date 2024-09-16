# NR_gNBId_CellId_nRPCI_nRTCI_calculator

● online_calculator : https://dustinchen26.github.io/id

## Process
```
1CU_1DU_2RU 做handover
============================================================================================================
//cell_1
64bits=22bits                 14bits         10bits     18bits
       gNBIdLength
       0000000000000001110111 00000000000001 0000010011 000000000000000000=523367808237568 (填到cell_2的nRTCI)
       119                    1              19
nRTCI= (gNBId                 cellLocalId )  nRPCI      padding
                              CellId
       (nrCellId=nCI                      )
	   <nrCellId><nCI>0001DC001 HEX
============================================================================================================
//cell_2
64bits=22bits                 14bits         10bits     18bits
       gNBIdLength
       0000000000000001110111 00000000000010 0000010100 000000000000000000=523368076935168 (填到cell_1的nRTCI)
       119                    2              20
nRTCI= (gNBId                 cellLocalId )  nRPCI      padding
                              CellId
       (nrCellId=nCI                      )
============================================================================================================
```

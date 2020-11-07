---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 71302FB6-7E2B-4972-A743-AB537AC7CD79
online version: ''
schema: 2.0.0
ms.openlocfilehash: 79e194e0f8dda4392dec191881702c680bf172ac
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946552"
---
# Get-AzureStorSimpleAccessControlRecord

## Sinopse
Obtém registros de controle de acesso em uma configuração de serviço.

## SYNTAX

```
Get-AzureStorSimpleAccessControlRecord [-ACRName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Get-AzureStorSimpleAccessControlRecord** Obtém registros de controle de acesso na configuração do serviço StorSimple Manager.
Este cmdlet obtém todos os registros ou um registro nomeado.

Os registros de controle de acesso são recipientes de parâmetros do iniciador iSCSI.
Esses parâmetros especificam quais iniciadores podem acessar um volume.
Quando um iniciador iSCSI tenta se conectar a um volume, seu aparelho verifica os registros de controle de acesso atribuídos a esse volume.
Se os parâmetros do iniciador iSCSI corresponderem a uma das entradas em um registro de controle de acesso mapeado para esse volume, o iniciador iSCSI poderá se conectar.

## EXEMPLOS

### Exemplo 1: obter todos os registros de controle de acesso
```
PS C:\>Get-AzureStorSimpleAccessControlRecord
InstanceId                           Name                        InitiatorName               VolumeCount
----------                           ----                        -------------               -----------
01a31aa5-14de-4b77-b926-2842577f540e Windows_XYUSFL718-RV_ACR    iqn.1991-05.com.microsof... 3
071c282d-0cd2-4c5f-b687-48966037ba48 Linux_XYUSFL719_ACR         iqn.1994-05.com.redhat:a... 3
4600eade-71f8-4d04-baec-0e7cf1d1e8fb Windows_XYUSFL720_ACR       iqn.1991-05.com.microsof... 9
d508d6f0-fcda-4624-b223-c0b307d6113e Linux_XYUSFL350_ACR         iqn.1991-05.com.microsof... 9
```

Esse comando obtém todos os registros de controle de acesso.

### Exemplo 2: obter um registro de controle de acesso específico
```
PS C:\>Get-AzureStorSimpleAccessControlRecord -ACRName "Acr11"
VERBOSE: ClientRequestId: 61f261c7-acd3-4bcc-922a-ddfd85eb767b_PS
VERBOSE: ClientRequestId: 49c6a4c7-d299-46fd-a553-034c52b47487_PS

GlobalId            : 
InitiatorName       : iqn-contoso63
InstanceId          : 55f24643-ab3a-4098-ade2-aa2b1a3ab18c
Name                : Acr11
OperationInProgress : None
VolumeCount         : 6

VERBOSE: Access Control Record with given name Acr11 is found!
```

Esse comando obtém o registro de controle de acesso chamado Acr11.

## OS

### -ACRName
Especifica o nome de um registro de controle de acesso a ser obtido.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Perfil
Especifica um perfil do Azure.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### Nenhuma

## EXIBE

### AccessControlRecord, IList\<AccessControlRecord\>
Esse cmdlet retorna um objeto **AccessControlRecord** ou um **objeto \<AccessControlRecord\> IList** .
Um objeto **AccessControlRecord** contém os seguintes campos: 

- **GlobalId** ( **cadeia** ) 
- **Initiatorname** ( **cadeia de caracteres** ) 
- **InstanceId** ( **cadeia** ) 
- **Name** ( **cadeia** ) 
- **OperationInProgress** ( **OperationInProgress** ) 
- **VolumeCount** ( **int** )

## INFORMA

## LINKS RELACIONADOS

[New-AzureStorSimpleAccessControlRecord](./New-AzureStorSimpleAccessControlRecord.md)

[Remove-AzureStorSimpleAccessControlRecord](./Remove-AzureStorSimpleAccessControlRecord.md)

[Set-AzureStorSimpleAccessControlRecord](./Set-AzureStorSimpleAccessControlRecord.md)



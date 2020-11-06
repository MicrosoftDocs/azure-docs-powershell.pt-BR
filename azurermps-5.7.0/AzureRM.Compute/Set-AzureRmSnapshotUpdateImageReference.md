---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmSnapshotUpdateImageReference.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmSnapshotUpdateImageReference.md
ms.openlocfilehash: fa6b3e16fd137453229232405d31cd7665ccd18e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427606"
---
# Set-AzureRmSnapshotUpdateImageReference

## Sinopse
Define as propriedades de referência de imagem em um objeto de atualização de instantâneo.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
Set-AzureRmSnapshotUpdateImageReference [-SnapshotUpdate] <SnapshotUpdate> [[-Id] <String>] [[-Lun] <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **set-AzureRmSnapshotUpdateImageReference** define as propriedades de referência de imagem em um objeto de atualização de instantâneo.

## EXEMPLOS

### Exemplo 1
```
PS C:\> $snapshotupdateconfig = New-AzureRmSnapshotUpdateConfig -SnapshotSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption FromImage;
PS C:\> $image = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/images/TestImage123';        
PS C:\> $snapshotupdateconfig = Set-AzureRmSnapshotUpdateImageReference -Snapshot $snapshotupdateconfig -Id $image -Lun 0;
PS C:\> Update-AzureRmSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -SnapshotUpdate $snapshotupdateconfig;
```

O primeiro comando cria um objeto de atualização de instantâneo local com o tamanho 10GB em Premium_LRS tipo de conta de armazenamento.  Ele também define o tipo de sistema operacional Windows.
O segundo comando define a ID da imagem e o número da unidade lógica 0 para o objeto de atualização do instantâneo.
O último comando usa o objeto de atualização de instantâneo e atualiza um instantâneo existente com o nome "Snapshot01" no grupo de recursos "ResourceGroup01".

## OS

### -ID
Especifica a ID.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -LUN
Especifica o número da unidade lógica (LUN).

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SnapshotUpdate
Especifica um objeto de atualização de instantâneo local.

```yaml
Type: SnapshotUpdate
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Confirme
Solicita confirmação antes de executar o cmdlet.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Mostra o que aconteceria se o cmdlet fosse executado. O cmdlet não é executado.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### Microsoft. Azure. Management. COMPUTE. Models. SnapshotUpdate
System. String System. Nullable ' 1 [System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]

## EXIBE

### Microsoft. Azure. Management. COMPUTE. Models. SnapshotUpdate

## INFORMA

## LINKS RELACIONADOS


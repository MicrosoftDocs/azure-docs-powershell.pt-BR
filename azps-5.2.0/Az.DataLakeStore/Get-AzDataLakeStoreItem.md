---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: ECA70C6C-E0B0-445D-BCAD-041625FAC632
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItem.md
ms.openlocfilehash: ad741d955399b355534074737741b153d8d48690
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98260566"
---
# Get-AzDataLakeStoreItem

## Sinopse
Obtém os detalhes de um arquivo ou pasta no data Lake Store.

## SYNTAX

```
Get-AzDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Get-AzDataLakeStoreItem** Obtém os detalhes de um arquivo ou pasta no repositório data Lake.

## EXEMPLOS

### Exemplo 1: obter detalhes de um arquivo do repositório data Lake
```
PS C:\>Get-AzDataLakeStoreItem -AccountName "ContosoADL" -Path "/MyFiles/Test.csv"
```

Este comando obtém os detalhes do arquivo Test.csv do repositório data Lake.

## OS

### -Conta
Especifica o nome da conta do data Lake Store.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Caminho
Especifica o caminho do repositório data Lake do qual obter detalhes de um item, começando com o diretório raiz (/).

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### System. String

### Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStorePathInstance

## EXIBE

### Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreItem

## INFORMA

## LINKS RELACIONADOS

[Export-AzDataLakeStoreItem](./Export-AzDataLakeStoreItem.md)

[Get-AzDataLakeStoreChildItem](./Get-AzDataLakeStoreChildItem.md)

[Import-AzDataLakeStoreItem](./Import-AzDataLakeStoreItem.md)

[Ingressar em AzDataLakeStoreItem](./Join-AzDataLakeStoreItem.md)

[Mover-AzDataLakeStoreItem](./Move-AzDataLakeStoreItem.md)

[New-AzDataLakeStoreItem](./New-AzDataLakeStoreItem.md)

[Remove-AzDataLakeStoreItem](./Remove-AzDataLakeStoreItem.md)

[Test-AzDataLakeStoreItem](./Test-AzDataLakeStoreItem.md)



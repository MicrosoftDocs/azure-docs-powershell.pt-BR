---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 4E9EA2E9-4BE2-4530-BC2B-D369C016CD8C
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/join-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Join-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Join-AzDataLakeStoreItem.md
ms.openlocfilehash: 1d361149109b654cf3e7fa45e133b9daff84c21c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98426625"
---
# Join-AzDataLakeStoreItem

## Sinopse
Une um ou mais arquivos para criar um arquivo no data Lake Store.

## SYNTAX

```
Join-AzDataLakeStoreItem [-Account] <String> [-Paths] <DataLakeStorePathInstance[]>
 [-Destination] <DataLakeStorePathInstance> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Join-AzDataLakeStoreItem** une um ou mais arquivos para criar um arquivo no data Lake Store.

## EXEMPLOS

### Exemplo 1: unir dois itens
```
PS C:\>Join-AzDataLakeStoreItem -AccountName "ContosoADL" -Paths "/MyFiles/File01.txt","/MyFiles/File02.txt" -Destination "/MyFiles/CombinedFile.txt"
```

Este comando une File01.txt e File02.txt para criar o arquivo CombinedFile.txt.

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

### -Destino
Especifica o caminho do repositório data Lake para o item associado, começando com o diretório raiz (/).

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Force
Indica que essa operação pode substituir o arquivo de destino, caso ele já exista.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Caminhos
Especifica uma matriz de caminhos do repositório de data Lake dos arquivos a serem combinados, começando com o diretório raiz (/).

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance[]
Parameter Sets: (All)
Aliases: Path

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Confirme
Solicita confirmação antes de executar o cmdlet.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Mostra o que aconteceria se o cmdlet fosse executado.
O cmdlet não é executado.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### System. String

### Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStorePathInstance []

### Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStorePathInstance

### System. Management. Automation. SwitchParameter

## EXIBE

### System. String

## INFORMA

## LINKS RELACIONADOS

[Get-AzDataLakeStoreItem](./Get-AzDataLakeStoreItem.md)

[Export-AzDataLakeStoreItem](./Export-AzDataLakeStoreItem.md)

[Import-AzDataLakeStoreItem](./Import-AzDataLakeStoreItem.md)

[New-AzDataLakeStoreItem](./New-AzDataLakeStoreItem.md)

[Remove-AzDataLakeStoreItem](./Remove-AzDataLakeStoreItem.md)

[Test-AzDataLakeStoreItem](./Test-AzDataLakeStoreItem.md)



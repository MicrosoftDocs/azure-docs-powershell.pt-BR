---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 415C5854-FE03-4D4E-BE84-408EA5F95E34
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/set-azdatalakestoreitemowner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemOwner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemOwner.md
ms.openlocfilehash: fc7c0e7ff8ef86b4a33f93e6b1286bb6e0baa00d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98426587"
---
# Set-AzDataLakeStoreItemOwner

## Sinopse
Modifica o proprietário de um arquivo ou pasta no data Lake Store.

## SYNTAX

```
Set-AzDataLakeStoreItemOwner [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Type] <Owner>
 [-Id] <Guid> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **set-AzDataLakeStoreItemOwner** modifica o proprietário de um arquivo ou pasta no repositório data Lake.

## EXEMPLOS

### Exemplo 1: definir o proprietário de um item
```
PS C:\>Set-AzDataLakeStoreItemOwner -AccountName "ContosoADL" -Path / -Type User -Id (Get-AzADUser -Mail "PattiFuller@contoso.com").ObjectId
```

Esse comando define o proprietário do diretório raiz como Patti a Pereira.

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

### -ID
Especifica a ID de objeto do usuário, grupo ou entidade de serviço do diretório do AzureActive a ser usado como proprietário.

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PassThru
Indica que o proprietário atualizado resultante deve ser retornado.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Caminho
Especifica o caminho do repositório data Lake do item a ser modificado, começando com o diretório raiz (/).

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

### -Digite
Especifica o tipo de proprietário a ser definido.
Os valores aceitáveis para esse parâmetro são: usuário e grupo.

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+Owner
Parameter Sets: (All)
Aliases:
Accepted values: User, Group

Required: True
Position: 2
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

### Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStorePathInstance

### Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreEnums + Owner

### System. GUID

### System. Management. Automation. SwitchParameter

## EXIBE

### System. String

## INFORMA

## LINKS RELACIONADOS

[Get-AzDataLakeStoreItemOwner](./Get-AzDataLakeStoreItemOwner.md)



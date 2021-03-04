---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/powershell/module/az.datamigration/New-AzDataMigrationService
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationService.md
ms.openlocfilehash: 7d36860991d5b6b12fb23044cc607044fb87bfa6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892979"
---
# New-AzDataMigrationService

## SYNOPSIS
Cria uma nova instância do Serviço de Migração de Banco de Dados do Azure.

## SINTAXE

```
New-AzDataMigrationService -ResourceGroupName <String> -Name <String> -Location <String> -Sku <String>
 -VirtualSubnetId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
O New-AzDataMigrationService cmdlet cria uma nova instância do Serviço de Migração de Banco de Dados do Azure. Este cmdlet leva em nome do Grupo de Recursos do Azure existente, o nome exclusivo para a nova instância do Serviço de Migração de Banco de Dados do Azure a ser criado, a região na qual a instância é provisionada, o nome da SKU de Trabalho do DMS e o nome da Sub-rede Virtual do Azure na qual o serviço deve residir. Não há parâmetro para o nome da assinatura, pois é esperado que o usuário especifique a assinatura padrão da sessão de logon do Azure ou execute o Get-AzSubscription -SubscriptionName "MySubscription" | Select-AzSubscription selecionar outra assinatura.

## EXEMPLOS

### Exemplo 1
```
PS C:\> New-AzDataMigrationService -ResourceGroupName myResourceGroup -Name TestService -Location "Central US" -Sku Basic_2vCores -VirtualSubnetId $virtualSubNetId
```

O exemplo acima mostra como criar uma nova instância do Serviço de Migração de Banco de Dados do Azure chamado TestService na região central dos EUA.

## PARÂMETROS

### -DefaultProfile
As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.

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

### -Location
O local da instância do Serviço de Migração de Banco de Dados do Azure a ser criado, que corresponde a uma região do Azure.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Nome do Serviço de Migração de Banco de Dados.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
O nome do grupo de recursos.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Sku
O sku da instância do Serviço de Migração de Banco de Dados do Azure. Os valores possíveis atualmente são Basic_1vCore,Basic_2vCores,GeneralPurpose_4vCores

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VirtualSubnetId
O nome da sub-rede na rede virtual especificada a ser usada para a instância do Serviço de Migração de Banco de Dados do Azure.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirm
Solicita a confirmação antes de executar o cmdlet.

```yaml
Type: System.Management.Automation.SwitchParameter
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
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### Nenhum

## SAÍDAS

### Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService

## NOTES

## LINKS RELACIONADOS

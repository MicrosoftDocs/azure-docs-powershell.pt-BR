---
external help file: Microsoft.Azure.Commands.PolicyInsights.dll-Help.xml
Module Name: AzureRM.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.policyinsights/stop-azurermpolicyremediation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PolicyInsights/Commands.PolicyInsights/help/Stop-AzureRmPolicyRemediation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PolicyInsights/Commands.PolicyInsights/help/Stop-AzureRmPolicyRemediation.md
ms.openlocfilehash: 6e36b2ce8fb03173bfaab80b68c219873875526c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428419"
---
# Stop-AzureRmPolicyRemediation

## Sinopse
Cancela uma remediação de política em andamento.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

### ByName (padrão)
```
Stop-AzureRmPolicyRemediation -Name <String> [-Scope <String>] [-ManagementGroupName <String>]
 [-ResourceGroupName <String>] [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### ByResourceId
```
Stop-AzureRmPolicyRemediation -ResourceId <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByInputObject
```
Stop-AzureRmPolicyRemediation -InputObject <PSRemediation> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Stop-AzureRmPolicyRemediation** cancela uma remediação em andamento da política. Implantações ativas serão canceladas e nenhuma nova implantação será criada.

## EXEMPLOS

### Exemplo 1: cancelar uma correção de política em escopo do grupo de recursos
```
PS C:\> Stop-AzureRmPolicyRemediation -ResourceGroupName "myRG" -Name "remediation1"
```

Este comando cancela a correção chamada "remediation1" no grupo de recursos "myRG".

### Exemplo 2: cancelar uma correção de grupo de gerenciamento via tubulação
```
PS C:\> $remediation = Get-AzureRmPolicyRemediation -ManagementGroupName "mg1" -Name "remediation1"
PS C:\> $remediation | Stop-AzureRmPolicyRemediation
```

Este comando cancela a correção chamada ' remediation1 ' no grupo de gerenciamento ' MG1 '.

## OS

### -AsJob
Execute o cmdlet em segundo plano.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
O objeto remediate.

```yaml
Type: Microsoft.Azure.Commands.PolicyInsights.Models.Remediation.PSRemediation
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ManagementGroupName
ID do grupo de gerenciamento.

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Nome
Nome do recurso.

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PassThru
Retorne true se o comando for concluído com êxito.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Nome do grupo de recursos.

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceId
ID do recurso.

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Escopo
Escopo do recurso.
:.
'/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
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
Default value: None
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
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### System. String

### Microsoft. Azure. Commands. PolicyInsights. Models. remediation. PSRemediation

## EXIBE

### System. Boolean

## INFORMA

## LINKS RELACIONADOS

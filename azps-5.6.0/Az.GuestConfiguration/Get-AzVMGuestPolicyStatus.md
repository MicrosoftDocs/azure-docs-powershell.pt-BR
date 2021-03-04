---
external help file: Microsoft.Azure.PowerShell.Cmdlets.GuestConfiguration.dll-Help.xml
Module Name: Az.GuestConfiguration
online version: https://docs.microsoft.com/powershell/module/az.guestconfiguration/get-AzVMGuestPolicyStatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/GuestConfiguration/GuestConfiguration/help/Get-AzVMGuestPolicyStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/GuestConfiguration/GuestConfiguration/help/Get-AzVMGuestPolicyStatus.md
ms.openlocfilehash: 3edb92ae8c46ab67e0e22ee808e38dad7101bfdf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890266"
---
# Get-AzVMGuestPolicyStatus

## SYNOPSIS
Obtém status da política de configuração de convidado (detalhado) para uma iniciativa do tipo "Configuração de Convidado" atribuída a uma VM.
Uma iniciativa é uma política do tipo de definição "Iniciativa".

## SINTAXE

### VmScope (Padrão)
```
Get-AzVMGuestPolicyStatus [-ResourceGroupName] <String> [-VMName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### InitiativeIdScope
```
Get-AzVMGuestPolicyStatus [-ResourceGroupName] <String> [-VMName] <String> [-InitiativeId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### InitiativeNameScope
```
Get-AzVMGuestPolicyStatus [-ResourceGroupName] <String> [-VMName] <String> [-InitiativeName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ReportIdScope
```
Get-AzVMGuestPolicyStatus [-ReportId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRIPTION
O Get-AzVMGuestPolicyStatus cmdlet obtém status de política de configuração de convidado para uma iniciativa do tipo "Configuração de Convidado" atribuída a uma VM.
Uma iniciativa é uma política do tipo de definição "Iniciativa".
Este cmdlet obtém status de conformidade da VM e os motivos pelos quais ele não está em conformidade com as políticas individuais na iniciativa.

## EXEMPLOS

### Exemplo 1
```powershell
PS C:\> Get-AzVMGuestPolicyStatus -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName"
```

Obter todos os status de política de configuração de convidado mais recentes para uma VM.
O status inclui o status de conformidade da VM para cada política em todas as iniciativas do tipo "Configuração de Convidados", motivos de conformidade, hora da verificação de conformidade, informações de recurso que foram verificadas para conformidade.
Os resultados incluem status mais recentes e não incluem status históricos anteriores.

### Exemplo 2
```powershell
PS C:\> Get-AzVMGuestPolicyStatus -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeId "/providers/Microsoft.Authorization/policySetDefinitions/3fa7cbf5-c0a4-4a59-85a5-cca4d996d5af"
```

Obter os status da política de configuração de convidado mais recentes por ID de iniciativa. O status inclui o status de conformidade da VM para cada política na iniciativa, motivos de conformidade, hora da verificação de conformidade, informações de recurso que foram verificadas para conformidade.
Os resultados não incluem status anteriores gerados, apenas inclui o status mais recente para cada política na iniciativa.

### Exemplo 3
```powershell
PS C:\> Get-AzVMGuestPolicyStatus -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeName "b5a822e0-ba98-4e54-9278-5d9833aa9b17"
```

Obter os status da política de configuração de convidado mais recentes pelo nome da iniciativa.
O status inclui o status de conformidade da VM para cada política na iniciativa, motivos de conformidade, hora da verificação de conformidade, informações de recurso que foram verificadas para conformidade.
Os resultados não incluem status anteriores gerados, apenas inclui o status mais recente para cada política na iniciativa.

### Exemplo 4
```powershell
PS C:\> Get-AzVMGuestPolicyStatus -ReportId "/subscriptions/4e6c6ed2-0bf6-41d7-9d21-a452c2cc7920/resourceGroups/MyResourceGroupName/providers/Microsoft.Compute/virtualMachines/MyVMName/providers/Microsoft.GuestConfiguration/guestConfigurationAssignments/MaximumPasswordAge/reports/c271f845-2c0a-4456-a441-e48fc332d0ac"
```

Obter o status da política de configuração de convidado por ReportId.
ReportId é a propriedade ReportId que pode ser encontrada nos resultados do Get-AzVMGuestPolicyStatus por nome initiativeId ou Initiative (consulte outros exemplos)

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

### -InitiativeId
ID de definição de uma política em que o tipo de definição é Iniciativa e categoria é Configuração de Convidado

```yaml
Type: System.String
Parameter Sets: InitiativeIdScope
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InitiativeName
Nome de uma política em que o tipo de definição é Iniciativa e categoria é Configuração de Convidado

```yaml
Type: System.String
Parameter Sets: InitiativeNameScope
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReportId
ID de um status de política de Configuração de Convidado.
Uma política em que o tipo de definição é Iniciativa e categoria é Configuração de Convidado deve ser atribuída a um escopo para obter status.

```yaml
Type: System.String
Parameter Sets: ReportIdScope
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Nome do grupo de recursos.

```yaml
Type: System.String
Parameter Sets: VmScope, InitiativeIdScope, InitiativeNameScope
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VMName
Nome da VM.

```yaml
Type: System.String
Parameter Sets: VmScope, InitiativeIdScope, InitiativeNameScope
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### Nenhum
## SAÍDAS

### Microsoft.Azure.Commands.GuestConfiguration.Models.PolicyStatusDetailed
## NOTES

## LINKS RELACIONADOS

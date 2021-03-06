---
external help file: Microsoft.Azure.PowerShell.Cmdlets.GuestConfiguration.dll-Help.xml
Module Name: Az.GuestConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.guestconfiguration/get-azvmguestpolicystatushistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/GuestConfiguration/GuestConfiguration/help/Get-AzVMGuestPolicyStatusHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/GuestConfiguration/GuestConfiguration/help/Get-AzVMGuestPolicyStatusHistory.md
ms.openlocfilehash: 929bc417cf4b84800635b85e7f503972509aa7fc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117643"
---
# Get-AzVMGuestPolicyStatusHistory

## Sinopse
Obtém o histórico de status da política de configuração de convidado para uma iniciativa do tipo "Configuração de Convidado" atribuída a um VM.
Uma iniciativa é uma política de tipo de definição "Iniciativa".

## Sintaxe

### InitiativeNameScope (Padrão)
```
Get-AzVMGuestPolicyStatusHistory [-ResourceGroupName] <String> [-VMName] <String> [-InitiativeName] <String>
 [-ShowOnlyChange] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### InitiativeIdScope
```
Get-AzVMGuestPolicyStatusHistory [-ResourceGroupName] <String> [-VMName] <String> [[-InitiativeId] <String>]
 [-ShowOnlyChange] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Descrição
O Get-AzVMGuestPolicyStatusHistory cmdlet obtém o histórico de status de conformidade das políticas de configuração de convidado para uma iniciativa do tipo "Configuração de Convidado" atribuída a um VM.
Uma iniciativa é uma política de tipo de definição "Iniciativa".
Use Get-AzVMGuestPolicyStatus cmdlet para obter detalhes sobre um único status de conformidade usando ReportId que pode ser encontrado na saída de Get-AzVMGuestPolicyStatusHistory cmdlet.

## Exemplos

### Exemplo 1
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeId "/providers/Microsoft.Authorization/policySetDefinitions/3fa7cbf5-c0a4-4a59-85a5-cca4d996d5af" -ShowOnlyChange
```

Obtém o histórico de status de conformidade por ID de iniciativa. A opção ShowOnlyChange mostra apenas as alterações de status de histórico.
Ignora os status que não foram alterados entre duas verificações de conformidade.

### Exemplo 2
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeName "b5a822e0-ba98-4e54-9278-5d9833aa9b17" -ShowOnlyChange
```

Obtém o histórico de status de conformidade pelo nome da iniciativa.
A opção ShowOnlyChange mostra apenas as alterações de status de histórico.
Ignora os status que não foram alterados entre duas verificações de conformidade.

### Exemplo 3
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -ShowOnlyChange
```

Obtém histórico de status de conformidade para todas as políticas de configuração de convidado atribuídas ao VM.
A opção ShowOnlyChange mostra apenas as alterações de status de histórico.
Ignora os status que não foram alterados entre duas verificações de conformidade.

### Exemplo 4
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeId "/providers/Microsoft.Authorization/policySetDefinitions/3fa7cbf5-c0a4-4a59-85a5-cca4d996d5af"
```

Obtém o histórico de status de conformidade por ID de iniciativa.

### Exemplo 5
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeName "b5a822e0-ba98-4e54-9278-5d9833aa9b17"
```

Obtém o histórico de status de conformidade pelo nome da iniciativa.

### Exemplo 6
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName"
```
Obtém histórico de status de conformidade para todas as políticas de configuração de convidado atribuídas ao VM.

### Exemplo 7
```powershell
PS C:\>$x = Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName"
PS C:\>$x[10].ReportId
/subscriptions/4e6c6ed2-0bf6-41d7-9d21-a452c2cc7920/resourceGroups/MyResourceGroupName/providers/Microsoft.Compute/virtualMachines/MyVMName/providers/Microsoft.GuestConfiguration/guestConfigurationAssignments/MaximumPasswordAge/reports/c271f845-2c0a-4456-a441-e48fc332d0ac
PS C:\> Get-AzVMGuestPolicyStatus -ReportId $x[10].ReportId
```

Obter status da política de configuração de convidado pelo ReportId.
O ReportId é a propriedade ReportId que pode ser encontrada nos resultados de Get-AzVMGuestPolicyStatusHistory. (consulte outros exemplos)

## Parâmetros

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.

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

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Nomeda Iniciativa
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

### -ResourceGroupName
Nome do grupo de recursos.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ShowOnlyChange
Mostra as alterações de status de histórico somente para políticas de configuração de convidado.
Ignora os status que não foram alterados entre duas auditorias de status de conformidade.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -VMName
Nome do VM.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## Entradas

### Nenhum
## Saídas

### Microsoft.Azure.Commands.GuestConfiguration.Models.PolicyStatus
## Notas

## LINKS RELACIONADOS

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.GuestConfiguration.dll-Help.xml
Module Name: Az.GuestConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.guestconfiguration/get-azvmguestpolicystatushistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/GuestConfiguration/GuestConfiguration/help/Get-AzVMGuestPolicyStatusHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/GuestConfiguration/GuestConfiguration/help/Get-AzVMGuestPolicyStatusHistory.md
ms.openlocfilehash: 929bc417cf4b84800635b85e7f503972509aa7fc
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93948263"
---
# Get-AzVMGuestPolicyStatusHistory

## Sinopse
Obtém o histórico de status de conformidade da política de configuração de convidado para uma iniciativa do tipo "configuração de convidado" que é atribuído a uma VM.
Uma iniciativa é uma política de tipo de definição "iniciativa".

## SYNTAX

### InitiativeNameScope (padrão)
```
Get-AzVMGuestPolicyStatusHistory [-ResourceGroupName] <String> [-VMName] <String> [-InitiativeName] <String>
 [-ShowOnlyChange] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### InitiativeIdScope
```
Get-AzVMGuestPolicyStatusHistory [-ResourceGroupName] <String> [-VMName] <String> [[-InitiativeId] <String>]
 [-ShowOnlyChange] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet Get-AzVMGuestPolicyStatusHistory Obtém o histórico do status de conformidade das políticas de configuração de convidado para uma iniciativa do tipo "configuração de convidado" que é atribuído a uma VM.
Uma iniciativa é uma política de tipo de definição "iniciativa".
Use o cmdlet Get-AzVMGuestPolicyStatus para obter detalhes de um único status de conformidade usando o ReportID que pode ser encontrado na saída do cmdlet Get-AzVMGuestPolicyStatusHistory.

## EXEMPLOS

### Exemplo 1
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeId "/providers/Microsoft.Authorization/policySetDefinitions/3fa7cbf5-c0a4-4a59-85a5-cca4d996d5af" -ShowOnlyChange
```

Obtém o histórico de status de conformidade por ID da iniciativa. ShowOnlyChange opção mostra apenas alterações de status históricas.
Ignora status que não foram alterados entre duas verificações de conformidade.

### Exemplo 2
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeName "b5a822e0-ba98-4e54-9278-5d9833aa9b17" -ShowOnlyChange
```

Obtém o histórico do status de conformidade por nome da iniciativa.
A opção ShowOnlyChange mostra apenas alterações de status históricas.
Ignora status que não foram alterados entre duas verificações de conformidade.

### Exemplo 3
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -ShowOnlyChange
```

Obtém o histórico de status de conformidade para todas as políticas de configuração de convidado atribuídas à VM.
A opção ShowOnlyChange mostra apenas alterações de status históricas.
Ignora status que não foram alterados entre duas verificações de conformidade.

### Exemplo 4
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeId "/providers/Microsoft.Authorization/policySetDefinitions/3fa7cbf5-c0a4-4a59-85a5-cca4d996d5af"
```

Obtém o histórico de status de conformidade por ID da iniciativa.

### Exemplo 5
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeName "b5a822e0-ba98-4e54-9278-5d9833aa9b17"
```

Obtém o histórico do status de conformidade por nome da iniciativa.

### Exemplo 6
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName"
```
Obtém o histórico de status de conformidade para todas as políticas de configuração de convidado atribuídas à VM.

### Exemplo 7
```powershell
PS C:\>$x = Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName"
PS C:\>$x[10].ReportId
/subscriptions/4e6c6ed2-0bf6-41d7-9d21-a452c2cc7920/resourceGroups/MyResourceGroupName/providers/Microsoft.Compute/virtualMachines/MyVMName/providers/Microsoft.GuestConfiguration/guestConfigurationAssignments/MaximumPasswordAge/reports/c271f845-2c0a-4456-a441-e48fc332d0ac
PS C:\> Get-AzVMGuestPolicyStatus -ReportId $x[10].ReportId
```

Obter status da política de configuração de convidado por ReportID.
O ReportID é a Propriedade ReportID que pode ser encontrada nos resultados de Get-AzVMGuestPolicyStatusHistory. (por favor, consulte outros exemplos)

## OS

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

### -Initiativeid
A ID da definição de uma política na qual o tipo de definição é iniciativa e categoria é configuração de convidado

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

### -Initiativename
O nome de uma política em que o tipo de definição é iniciativa e categoria é configuração de convidado

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
Mostra as alterações do status histórico somente para políticas de configuração de convidado.
Ignora status que não foram alterados entre duas execuções de auditoria de status de conformidade.

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
Nome da VM.

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
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### Nenhuma
## EXIBE

### Microsoft. Azure. Commands. GuestConfiguration. Models. PolicyStatus
## INFORMA

## LINKS RELACIONADOS

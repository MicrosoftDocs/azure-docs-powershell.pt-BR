---
external help file: Microsoft.Azure.PowerShell.Cmdlets.GuestConfiguration.dll-Help.xml
Module Name: Az.GuestConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.guestconfiguration/get-AzVMGuestPolicyStatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/GuestConfiguration/GuestConfiguration/help/Get-AzVMGuestPolicyStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/GuestConfiguration/GuestConfiguration/help/Get-AzVMGuestPolicyStatus.md
ms.openlocfilehash: c1bf608c76c547360d9d7a48f4ba74c1713ee049
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93596388"
---
# Get-AzVMGuestPolicyStatus

## Sinopse
Obtém status da política de configuração de convidado (detalhado) para uma iniciativa do tipo "configuração de convidado" que é atribuído a uma VM.
Uma iniciativa é uma política de tipo de definição "iniciativa".

## SYNTAX

### VmScope (padrão)
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

## DESCRITIVO
O cmdlet Get-AzVMGuestPolicyStatus Obtém status da política de configuração de convidado para uma iniciativa do tipo "configuração de convidado" que é atribuído a uma VM.
Uma iniciativa é uma política de tipo de definição "iniciativa".
Esse cmdlet obtém status de conformidade da VM e os motivos pelos quais ele não é compatível com as políticas individuais na iniciativa.

## EXEMPLOS

### Exemplo 1
```powershell
PS C:\> Get-AzVMGuestPolicyStatus -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName"
```

Obtenha todos os status da política de configuração de convidado mais recente para uma VM.
O status inclui o status de conformidade da VM para cada política em todas as iniciativas do tipo "configuração de convidado", motivos de conformidade, hora da verificação de conformidade, informações sobre recursos que foram verificadas quanto à conformidade.
Os resultados incluem status mais recentes, não inclui status histórico anterior.

### Exemplo 2
```powershell
PS C:\> Get-AzVMGuestPolicyStatus -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeId "/providers/Microsoft.Authorization/policySetDefinitions/3fa7cbf5-c0a4-4a59-85a5-cca4d996d5af"
```

Obtenha os status da política de configuração de convidado mais recente por ID da iniciativa. O status inclui o status de conformidade da VM para cada política na iniciativa, motivos de conformidade, hora da verificação de conformidade, informações sobre o recurso que foram verificadas quanto à conformidade.
Os resultados não incluem o status anterior gerado, ele apenas inclui o status mais recente de cada política na iniciativa.

### Exemplo 3
```powershell
PS C:\> Get-AzVMGuestPolicyStatus -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeName "b5a822e0-ba98-4e54-9278-5d9833aa9b17"
```

Obtenha os status da política de configuração de convidado mais recente por nome da iniciativa.
O status inclui o status de conformidade da VM para cada política na iniciativa, motivos de conformidade, hora da verificação de conformidade, informações sobre o recurso que foram verificadas quanto à conformidade.
Os resultados não incluem o status anterior gerado, ele apenas inclui o status mais recente de cada política na iniciativa.

### Exemplo 4
```powershell
PS C:\> Get-AzVMGuestPolicyStatus -ReportId "/subscriptions/4e6c6ed2-0bf6-41d7-9d21-a452c2cc7920/resourceGroups/MyResourceGroupName/providers/Microsoft.Compute/virtualMachines/MyVMName/providers/Microsoft.GuestConfiguration/guestConfigurationAssignments/MaximumPasswordAge/reports/c271f845-2c0a-4456-a441-e48fc332d0ac"
```

Obter status da política de configuração de convidado por ReportID.
O ReportID é a Propriedade ReportID que pode ser encontrada nos resultados de Get-AzVMGuestPolicyStatus por initiativeid ou nome da iniciativa (consulte outros exemplos)

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

Required: True
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

### -ReportID
ID de um status de política de configuração de convidado.
Uma política na qual o tipo de definição é iniciativa e categoria é a configuração de convidado deve ser atribuída a um escopo para obter status.

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
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### Nenhuma
## EXIBE

### Microsoft. Azure. Commands. GuestConfiguration. Models. PolicyStatusDetailed
## INFORMA

## LINKS RELACIONADOS

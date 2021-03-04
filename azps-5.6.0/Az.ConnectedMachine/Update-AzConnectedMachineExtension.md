---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/powershell/module/az.connectedmachine/update-azconnectedmachineextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Update-AzConnectedMachineExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Update-AzConnectedMachineExtension.md
ms.openlocfilehash: e6da084f13d85f8c4f5a8934cd5fd4f05882c251
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101893192"
---
# Update-AzConnectedMachineExtension

## SYNOPSIS
A operação para criar ou atualizar a extensão.

## SINTAXE

### UpdateExpanded (Padrão)
```
Update-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-AutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-ProtectedSetting <IMachineExtensionUpdatePropertiesProtectedSettings>] [-Publisher <String>]
 [-Setting <IMachineExtensionUpdatePropertiesSettings>] [-Tag <Hashtable>] [-Type <String>]
 [-TypeHandlerVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### Atualização
```
Update-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 -ExtensionParameter <IMachineExtensionUpdate> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### UpdateViaIdentity
```
Update-AzConnectedMachineExtension -InputObject <IConnectedMachineIdentity>
 -ExtensionParameter <IMachineExtensionUpdate> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### UpdateViaIdentityExpanded
```
Update-AzConnectedMachineExtension -InputObject <IConnectedMachineIdentity> [-AutoUpgradeMinorVersion]
 [-ForceRerun <String>] [-ProtectedSetting <IMachineExtensionUpdatePropertiesProtectedSettings>]
 [-Publisher <String>] [-Setting <IMachineExtensionUpdatePropertiesSettings>] [-Tag <Hashtable>]
 [-Type <String>] [-TypeHandlerVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## DESCRIPTION
A operação para criar ou atualizar a extensão.

## EXEMPLOS

### Exemplo 1: atualizar uma extensão
```powershell
PS C:\> $splat = @{
            ResourceGroupName = "connectedMachines"
            MachineName = "linux-eastus1_1"
            Name = "customScript"
            Settings = @{
                commandToExecute = "ls -l"
            }
        }
PS C:\> Update-AzConnectedMachineExtension @splat

Name         Location ProvisioningState
----         -------- -----------------
customScript eastus   Succeeded
```

Atualiza uma extensão em um computador específico.

### Exemplo 2: atualizar uma extensão com o local especificado por meio do pipeline
```powershell
PS C:\> $extToUpdate = Get-AzConnectedMachineExtension -ResourceGroupName connectedMachines -MachineName linux-eastus1_1 -Name customScript
PS C:\> $extToUpdate | Update-AzConnectedMachineExtension -Settings @{
                commandToExecute = "ls -l"
            }

Name         Location ProvisioningState
----         -------- -----------------
customScript eastus   Succeeded
```

Atualiza uma extensão específica passada pelo pipeline.
Aqui estamos usando a extensão passada por meio do pipeline para nos ajudar a identificar em qual extensão queremos operar e estamos especificando o que desejamos alterar por meio dos parâmetros normais (como `-Settings` )

### Exemplo 3: atualizar uma extensão com parâmetros de extensão especificados por meio do pipeline
```powershell
PS C:\> $extToUpdate = Get-AzConnectedMachineExtension -ResourceGroupName connectedMachines -MachineName linux-eastus1_1 -Name customScript
PS C:\> # Update the settings on the object that will be used via the pipeline
PS C:\> $extToUpdate.Setting.commandToExecute = "ls -l"
PS C:\> $splat = @{
            ResourceGroupName = "connectedMachines"
            MachineName = "linux-eastus1_1"
            Name = "customScript"
        }
PS C:\> $extToUpdate | Update-AzConnectedMachineExtension @splat

Name         Location ProvisioningState
----         -------- -----------------
customScript eastus   Succeeded
```

Atualiza uma extensão específica passada pelo pipeline.
Aqui estamos usando a extensão passada por meio do pipeline para fornecer as alterações que desejamos fazer na extensão.
O local da extensão não é recuperado por meio do pipeline, mas sim pelos parâmetros especificados normalmente (pelo parâmetro splat).

### Exemplo 4: usando um objeto extension como o local e os parâmetros para atualização
```powershell
PS C:\> $extToUpdate = Get-AzConnectedMachineExtension -ResourceGroupName connectedMachines -MachineName linux-eastus1_1 -Name customScript
PS C:\> # Update the settings on the object that will be used via the pipeline
PS C:\> $extToUpdate.Setting.commandToExecute = "ls -l"
PS C:\> $extToUpdate | Update-AzConnectedMachineExtension -ExtensionParameter $extToUpdate

Name         Location ProvisioningState
----         -------- -----------------
customScript eastus   Succeeded
```

Atualiza uma extensão específica passada pelo pipeline.
Aqui estamos usando a extensão passada por meio do pipeline para nos ajudar a identificar em qual extensão queremos operar.
Além disso, estamos usando os parâmetros do objeto extension para especificar o que atualizar.

## PARÂMETROS

### -AsJob
Executar o comando como um trabalho

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

### -AutoUpgradeMinorVersion
Indica se a extensão deve usar uma versão secundária mais recente se uma estiver disponível no momento da implantação.
No entanto, uma vez implantado, a extensão não atualizará versões secundárias, a menos que seja reimplantada, mesmo com essa propriedade definida como true.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: UpdateExpanded, UpdateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ExtensionParameter
Descreve uma Atualização de Extensão de Máquina.
Para construir, consulte a seção NOTES para propriedades EXTENSIONPARAMETER e crie uma tabela de hash.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtensionUpdate
Parameter Sets: Update, UpdateViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ForceRerun
Como o manipulador de extensão deve ser forçado a atualizar mesmo que a configuração da extensão não tenha sido alterada.

```yaml
Type: System.String
Parameter Sets: UpdateExpanded, UpdateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Parâmetro Identity Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.IConnectedMachineIdentity
Parameter Sets: UpdateViaIdentity, UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -MachineName
O nome do computador onde a extensão deve ser criada ou atualizada.

```yaml
Type: System.String
Parameter Sets: Update, UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
O nome da extensão do computador.

```yaml
Type: System.String
Parameter Sets: Update, UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NoWait
Executar o comando de forma assíncrona

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

### -ProtectedSetting
A extensão pode conter protectedSettings ou protectedSettingsFromKeyVault ou nenhuma configuração protegida.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtensionUpdatePropertiesProtectedSettings
Parameter Sets: UpdateExpanded, UpdateViaIdentityExpanded
Aliases: ProtectedSettings

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Publisher
O nome do editor do manipulador de extensão.

```yaml
Type: System.String
Parameter Sets: UpdateExpanded, UpdateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
O nome do grupo de recursos.

```yaml
Type: System.String
Parameter Sets: Update, UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Setting
Configurações públicas formatadas Json para a extensão.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtensionUpdatePropertiesSettings
Parameter Sets: UpdateExpanded, UpdateViaIdentityExpanded
Aliases: Settings

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionId
Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.
A ID da assinatura faz parte do URI para cada chamada de serviço.

```yaml
Type: System.String
Parameter Sets: Update, UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### -Tag
Marcas de recurso

```yaml
Type: System.Collections.Hashtable
Parameter Sets: UpdateExpanded, UpdateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Type
Especifica o tipo da extensão; um exemplo é "CustomScriptExtension".

```yaml
Type: System.String
Parameter Sets: UpdateExpanded, UpdateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TypeHandlerVersion
Especifica a versão do manipulador de scripts.

```yaml
Type: System.String
Parameter Sets: UpdateExpanded, UpdateViaIdentityExpanded
Aliases:

Required: False
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
Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtensionUpdate

### Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.IConnectedMachineIdentity

## SAÍDAS

### Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension

## NOTES

ALIASES

PROPRIEDADES DE PARÂMETRO COMPLEXO

Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas. Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.


EXTENSIONPARAMETER <IMachineExtensionUpdate> : Descreve uma Atualização de Extensão de Máquina.
  - `[Tag <IUpdateResourceTags>]`: Marcas de recurso
    - `[(Any) <String>]`: Isso indica que qualquer propriedade pode ser adicionada a esse objeto.
  - `[AutoUpgradeMinorVersion <Boolean?>]`: Indica se a extensão deve usar uma versão secundária mais recente se uma estiver disponível no momento da implantação. No entanto, uma vez implantado, a extensão não atualizará versões secundárias, a menos que seja reimplantada, mesmo com essa propriedade definida como true.
  - `[ForceUpdateTag <String>]`: Como o manipulador de extensão deve ser forçado a atualizar mesmo que a configuração da extensão não tenha sido alterada.
  - `[ProtectedSetting <IMachineExtensionUpdatePropertiesProtectedSettings>]`: A extensão pode conter protectedSettings ou protectedSettingsFromKeyVault ou nenhuma configuração protegida.
  - `[Publisher <String>]`: O nome do editor do manipulador de extensão.
  - `[Setting <IMachineExtensionUpdatePropertiesSettings>]`: Configurações públicas formatadas Json para a extensão.
  - `[Type <String>]`: Especifica o tipo da extensão; um exemplo é "CustomScriptExtension".
  - `[TypeHandlerVersion <String>]`: Especifica a versão do manipulador de scripts.

INPUTOBJECT <IConnectedMachineIdentity> : Parâmetro Identity
  - `[ExtensionName <String>]`: O nome da extensão do computador.
  - `[Id <String>]`: Caminho da identidade do recurso
  - `[Name <String>]`: O nome da máquina híbrida.
  - `[ResourceGroupName <String>]`: O nome do grupo de recursos.
  - `[SubscriptionId <String>]`: Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure. A ID da assinatura faz parte do URI para cada chamada de serviço.

## LINKS RELACIONADOS


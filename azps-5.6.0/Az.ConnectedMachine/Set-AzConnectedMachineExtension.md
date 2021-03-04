---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/powershell/module/az.connectedmachine/set-azconnectedmachineextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Set-AzConnectedMachineExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Set-AzConnectedMachineExtension.md
ms.openlocfilehash: accea82dd6594d71f627d6c3e32943d004fa35e3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101893195"
---
# <span data-ttu-id="e62b3-101">Set-AzConnectedMachineExtension</span><span class="sxs-lookup"><span data-stu-id="e62b3-101">Set-AzConnectedMachineExtension</span></span>

## <span data-ttu-id="e62b3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e62b3-102">SYNOPSIS</span></span>
<span data-ttu-id="e62b3-103">A operação para criar ou atualizar a extensão.</span><span class="sxs-lookup"><span data-stu-id="e62b3-103">The operation to create or update the extension.</span></span>

## <span data-ttu-id="e62b3-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="e62b3-104">SYNTAX</span></span>

### <span data-ttu-id="e62b3-105">UpdateExpanded (Padrão)</span><span class="sxs-lookup"><span data-stu-id="e62b3-105">UpdateExpanded (Default)</span></span>
```
Set-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 -Location <String> [-SubscriptionId <String>] [-AutoUpgradeMinorVersion] [-ExtensionType <String>]
 [-ForceRerun <String>] [-ProtectedSetting <IMachineExtensionPropertiesProtectedSettings>]
 [-Publisher <String>] [-Setting <IMachineExtensionPropertiesSettings>] [-Tag <Hashtable>]
 [-TypeHandlerVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="e62b3-106">Atualização</span><span class="sxs-lookup"><span data-stu-id="e62b3-106">Update</span></span>
```
Set-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 -ExtensionParameter <IMachineExtension> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e62b3-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="e62b3-107">DESCRIPTION</span></span>
<span data-ttu-id="e62b3-108">A operação para criar ou atualizar a extensão.</span><span class="sxs-lookup"><span data-stu-id="e62b3-108">The operation to create or update the extension.</span></span>

## <span data-ttu-id="e62b3-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e62b3-109">EXAMPLES</span></span>

### <span data-ttu-id="e62b3-110">Exemplo 1: definir uma extensão em um computador</span><span class="sxs-lookup"><span data-stu-id="e62b3-110">Example 1: Set an extension on a machine</span></span>
```powershell
PS C:\> $Settings = @{ "commandToExecute" = "powershell.exe -c Get-Process" }
PS C:\> Set-AzConnectedMachineExtension -Name custom -ResourceGroupName ContosoTest -MachineName win-eastus1 -Location eastus -Publisher "Microsoft.Compute" -TypeHandlerVersion 1.10 -Settings $Settings -ExtensionType CustomScriptExtension

Name   Location ProvisioningState
----   -------- -----------------
custom eastus   Succeeded
```

<span data-ttu-id="e62b3-111">Define uma extensão em um computador.</span><span class="sxs-lookup"><span data-stu-id="e62b3-111">Sets an extension on a machine.</span></span>

### <span data-ttu-id="e62b3-112">Exemplo 2: definir uma extensão com parâmetros de extensão especificados por meio do pipeline</span><span class="sxs-lookup"><span data-stu-id="e62b3-112">Example 2: Set an extension with extension parameters specified via the pipeline</span></span>
```powershell
PS C:\> $otherExtension = Get-AzConnectedMachineExtension -Name custom -ResourceGroupName ContosoTest -MachineName other
PS C:\> $otherExtension | Set-AzConnectedMachineExtension -Name custom -ResourceGroupName ContosoTest -MachineName important

Name   Location ProvisioningState
----   -------- -----------------
custom eastus   Succeeded
```

<span data-ttu-id="e62b3-113">Isso define uma extensão com os parâmetros de extensão fornecidos pelo objeto passado por meio do pipeline.</span><span class="sxs-lookup"><span data-stu-id="e62b3-113">This sets an extension with the extension parameters provided by the object passed in via the pipeline.</span></span>
<span data-ttu-id="e62b3-114">Isso é ótimo se você quiser pegar os parâmetros de uma máquina e aplicá-los a outro computador.</span><span class="sxs-lookup"><span data-stu-id="e62b3-114">This is great if you want to grab the parameters of one machine and apply it to another machine.</span></span>

## <span data-ttu-id="e62b3-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="e62b3-115">PARAMETERS</span></span>

### <span data-ttu-id="e62b3-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e62b3-116">-AsJob</span></span>
<span data-ttu-id="e62b3-117">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="e62b3-117">Run the command as a job</span></span>

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

### <span data-ttu-id="e62b3-118">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="e62b3-118">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="e62b3-119">Indica se a extensão deve usar uma versão secundária mais recente se uma estiver disponível no momento da implantação.</span><span class="sxs-lookup"><span data-stu-id="e62b3-119">Indicates whether the extension should use a newer minor version if one is available at deployment time.</span></span>
<span data-ttu-id="e62b3-120">No entanto, uma vez implantado, a extensão não atualizará versões secundárias, a menos que seja reimplantada, mesmo com essa propriedade definida como true.</span><span class="sxs-lookup"><span data-stu-id="e62b3-120">Once deployed, however, the extension will not upgrade minor versions unless redeployed, even with this property set to true.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e62b3-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e62b3-121">-DefaultProfile</span></span>
<span data-ttu-id="e62b3-122">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e62b3-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e62b3-123">-ExtensionParameter</span><span class="sxs-lookup"><span data-stu-id="e62b3-123">-ExtensionParameter</span></span>
<span data-ttu-id="e62b3-124">Descreve uma extensão de máquina.</span><span class="sxs-lookup"><span data-stu-id="e62b3-124">Describes a Machine Extension.</span></span>
<span data-ttu-id="e62b3-125">Para construir, consulte a seção NOTES para propriedades EXTENSIONPARAMETER e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="e62b3-125">To construct, see NOTES section for EXTENSIONPARAMETER properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension
Parameter Sets: Update
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e62b3-126">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="e62b3-126">-ExtensionType</span></span>
<span data-ttu-id="e62b3-127">Especifica o tipo da extensão; um exemplo é "CustomScriptExtension".</span><span class="sxs-lookup"><span data-stu-id="e62b3-127">Specifies the type of the extension; an example is "CustomScriptExtension".</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e62b3-128">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="e62b3-128">-ForceRerun</span></span>
<span data-ttu-id="e62b3-129">Como o manipulador de extensão deve ser forçado a atualizar mesmo que a configuração da extensão não tenha sido alterada.</span><span class="sxs-lookup"><span data-stu-id="e62b3-129">How the extension handler should be forced to update even if the extension configuration has not changed.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e62b3-130">-Location</span><span class="sxs-lookup"><span data-stu-id="e62b3-130">-Location</span></span>
<span data-ttu-id="e62b3-131">A localização geográfica onde o recurso mora</span><span class="sxs-lookup"><span data-stu-id="e62b3-131">The geo-location where the resource lives</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e62b3-132">-MachineName</span><span class="sxs-lookup"><span data-stu-id="e62b3-132">-MachineName</span></span>
<span data-ttu-id="e62b3-133">O nome do computador onde a extensão deve ser criada ou atualizada.</span><span class="sxs-lookup"><span data-stu-id="e62b3-133">The name of the machine where the extension should be created or updated.</span></span>

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

### <span data-ttu-id="e62b3-134">-Name</span><span class="sxs-lookup"><span data-stu-id="e62b3-134">-Name</span></span>
<span data-ttu-id="e62b3-135">O nome da extensão do computador.</span><span class="sxs-lookup"><span data-stu-id="e62b3-135">The name of the machine extension.</span></span>

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

### <span data-ttu-id="e62b3-136">-NoWait</span><span class="sxs-lookup"><span data-stu-id="e62b3-136">-NoWait</span></span>
<span data-ttu-id="e62b3-137">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="e62b3-137">Run the command asynchronously</span></span>

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

### <span data-ttu-id="e62b3-138">-ProtectedSetting</span><span class="sxs-lookup"><span data-stu-id="e62b3-138">-ProtectedSetting</span></span>
<span data-ttu-id="e62b3-139">A extensão pode conter protectedSettings ou protectedSettingsFromKeyVault ou nenhuma configuração protegida.</span><span class="sxs-lookup"><span data-stu-id="e62b3-139">The extension can contain either protectedSettings or protectedSettingsFromKeyVault or no protected settings at all.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtensionPropertiesProtectedSettings
Parameter Sets: UpdateExpanded
Aliases: ProtectedSettings

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e62b3-140">-Publisher</span><span class="sxs-lookup"><span data-stu-id="e62b3-140">-Publisher</span></span>
<span data-ttu-id="e62b3-141">O nome do editor do manipulador de extensão.</span><span class="sxs-lookup"><span data-stu-id="e62b3-141">The name of the extension handler publisher.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e62b3-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e62b3-142">-ResourceGroupName</span></span>
<span data-ttu-id="e62b3-143">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e62b3-143">The name of the resource group.</span></span>

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

### <span data-ttu-id="e62b3-144">-Setting</span><span class="sxs-lookup"><span data-stu-id="e62b3-144">-Setting</span></span>
<span data-ttu-id="e62b3-145">Configurações públicas formatadas Json para a extensão.</span><span class="sxs-lookup"><span data-stu-id="e62b3-145">Json formatted public settings for the extension.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtensionPropertiesSettings
Parameter Sets: UpdateExpanded
Aliases: Settings

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e62b3-146">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e62b3-146">-SubscriptionId</span></span>
<span data-ttu-id="e62b3-147">Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="e62b3-147">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="e62b3-148">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="e62b3-148">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e62b3-149">-Tag</span><span class="sxs-lookup"><span data-stu-id="e62b3-149">-Tag</span></span>
<span data-ttu-id="e62b3-150">Marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="e62b3-150">Resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e62b3-151">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="e62b3-151">-TypeHandlerVersion</span></span>
<span data-ttu-id="e62b3-152">Especifica a versão do manipulador de scripts.</span><span class="sxs-lookup"><span data-stu-id="e62b3-152">Specifies the version of the script handler.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e62b3-153">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e62b3-153">-Confirm</span></span>
<span data-ttu-id="e62b3-154">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e62b3-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e62b3-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e62b3-155">-WhatIf</span></span>
<span data-ttu-id="e62b3-156">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e62b3-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e62b3-157">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e62b3-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e62b3-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e62b3-158">CommonParameters</span></span>
<span data-ttu-id="e62b3-159">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e62b3-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e62b3-160">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e62b3-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e62b3-161">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e62b3-161">INPUTS</span></span>

### <span data-ttu-id="e62b3-162">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span><span class="sxs-lookup"><span data-stu-id="e62b3-162">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span></span>

## <span data-ttu-id="e62b3-163">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="e62b3-163">OUTPUTS</span></span>

### <span data-ttu-id="e62b3-164">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span><span class="sxs-lookup"><span data-stu-id="e62b3-164">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span></span>

## <span data-ttu-id="e62b3-165">NOTES</span><span class="sxs-lookup"><span data-stu-id="e62b3-165">NOTES</span></span>

<span data-ttu-id="e62b3-166">ALIASES</span><span class="sxs-lookup"><span data-stu-id="e62b3-166">ALIASES</span></span>

<span data-ttu-id="e62b3-167">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="e62b3-167">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e62b3-168">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="e62b3-168">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e62b3-169">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e62b3-169">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e62b3-170">EXTENSIONPARAMETER <IMachineExtension> : descreve uma extensão de máquina.</span><span class="sxs-lookup"><span data-stu-id="e62b3-170">EXTENSIONPARAMETER <IMachineExtension>: Describes a Machine Extension.</span></span>
  - <span data-ttu-id="e62b3-171">`Location <String>`: A localização geográfica onde o recurso mora</span><span class="sxs-lookup"><span data-stu-id="e62b3-171">`Location <String>`: The geo-location where the resource lives</span></span>
  - <span data-ttu-id="e62b3-172">`[Tag <ITrackedResourceTags>]`: Marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="e62b3-172">`[Tag <ITrackedResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="e62b3-173">`[(Any) <String>]`: Isso indica que qualquer propriedade pode ser adicionada a esse objeto.</span><span class="sxs-lookup"><span data-stu-id="e62b3-173">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="e62b3-174">`[AutoUpgradeMinorVersion <Boolean?>]`: Indica se a extensão deve usar uma versão secundária mais recente se uma estiver disponível no momento da implantação.</span><span class="sxs-lookup"><span data-stu-id="e62b3-174">`[AutoUpgradeMinorVersion <Boolean?>]`: Indicates whether the extension should use a newer minor version if one is available at deployment time.</span></span> <span data-ttu-id="e62b3-175">No entanto, uma vez implantado, a extensão não atualizará versões secundárias, a menos que seja reimplantada, mesmo com essa propriedade definida como true.</span><span class="sxs-lookup"><span data-stu-id="e62b3-175">Once deployed, however, the extension will not upgrade minor versions unless redeployed, even with this property set to true.</span></span>
  - <span data-ttu-id="e62b3-176">`[ForceUpdateTag <String>]`: Como o manipulador de extensão deve ser forçado a atualizar mesmo que a configuração da extensão não tenha sido alterada.</span><span class="sxs-lookup"><span data-stu-id="e62b3-176">`[ForceUpdateTag <String>]`: How the extension handler should be forced to update even if the extension configuration has not changed.</span></span>
  - <span data-ttu-id="e62b3-177">`[MachineExtensionType <String>]`: Especifica o tipo da extensão; um exemplo é "CustomScriptExtension".</span><span class="sxs-lookup"><span data-stu-id="e62b3-177">`[MachineExtensionType <String>]`: Specifies the type of the extension; an example is "CustomScriptExtension".</span></span>
  - <span data-ttu-id="e62b3-178">`[ProtectedSetting <IMachineExtensionPropertiesProtectedSettings>]`: A extensão pode conter protectedSettings ou protectedSettingsFromKeyVault ou nenhuma configuração protegida.</span><span class="sxs-lookup"><span data-stu-id="e62b3-178">`[ProtectedSetting <IMachineExtensionPropertiesProtectedSettings>]`: The extension can contain either protectedSettings or protectedSettingsFromKeyVault or no protected settings at all.</span></span>
  - <span data-ttu-id="e62b3-179">`[Publisher <String>]`: O nome do editor do manipulador de extensão.</span><span class="sxs-lookup"><span data-stu-id="e62b3-179">`[Publisher <String>]`: The name of the extension handler publisher.</span></span>
  - <span data-ttu-id="e62b3-180">`[Setting <IMachineExtensionPropertiesSettings>]`: Configurações públicas formatadas Json para a extensão.</span><span class="sxs-lookup"><span data-stu-id="e62b3-180">`[Setting <IMachineExtensionPropertiesSettings>]`: Json formatted public settings for the extension.</span></span>
  - <span data-ttu-id="e62b3-181">`[TypeHandlerVersion <String>]`: Especifica a versão do manipulador de scripts.</span><span class="sxs-lookup"><span data-stu-id="e62b3-181">`[TypeHandlerVersion <String>]`: Specifies the version of the script handler.</span></span>

## <span data-ttu-id="e62b3-182">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e62b3-182">RELATED LINKS</span></span>


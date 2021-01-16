---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedmachine/set-azconnectedmachineextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Set-AzConnectedMachineExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Set-AzConnectedMachineExtension.md
ms.openlocfilehash: b136f5194bdc7e0f4b4dfc969564d7ef8476d9bf
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98257075"
---
# <span data-ttu-id="d6cbc-101">Set-AzConnectedMachineExtension</span><span class="sxs-lookup"><span data-stu-id="d6cbc-101">Set-AzConnectedMachineExtension</span></span>

## <span data-ttu-id="d6cbc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d6cbc-102">SYNOPSIS</span></span>
<span data-ttu-id="d6cbc-103">A operação para criar ou atualizar a extensão.</span><span class="sxs-lookup"><span data-stu-id="d6cbc-103">The operation to create or update the extension.</span></span>

## <span data-ttu-id="d6cbc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d6cbc-104">SYNTAX</span></span>

### <span data-ttu-id="d6cbc-105">UpdateExpanded (padrão)</span><span class="sxs-lookup"><span data-stu-id="d6cbc-105">UpdateExpanded (Default)</span></span>
```
Set-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 -Location <String> [-SubscriptionId <String>] [-AutoUpgradeMinorVersion] [-ExtensionType <String>]
 [-ForceRerun <String>] [-ProtectedSetting <IMachineExtensionPropertiesProtectedSettings>]
 [-Publisher <String>] [-Setting <IMachineExtensionPropertiesSettings>] [-Tag <Hashtable>]
 [-TypeHandlerVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="d6cbc-106">Atualização</span><span class="sxs-lookup"><span data-stu-id="d6cbc-106">Update</span></span>
```
Set-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 -ExtensionParameter <IMachineExtension> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d6cbc-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d6cbc-107">DESCRIPTION</span></span>
<span data-ttu-id="d6cbc-108">A operação para criar ou atualizar a extensão.</span><span class="sxs-lookup"><span data-stu-id="d6cbc-108">The operation to create or update the extension.</span></span>

## <span data-ttu-id="d6cbc-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d6cbc-109">EXAMPLES</span></span>

### <span data-ttu-id="d6cbc-110">Exemplo 1: definir uma extensão em um computador</span><span class="sxs-lookup"><span data-stu-id="d6cbc-110">Example 1: Set an extension on a machine</span></span>
```powershell
PS C:\> $Settings = @{ "commandToExecute" = "powershell.exe -c Get-Process" }
PS C:\> Set-AzConnectedMachineExtension -Name custom -ResourceGroupName ContosoTest -MachineName win-eastus1 -Location eastus -Publisher "Microsoft.Compute" -TypeHandlerVersion 1.10 -Settings $Settings -ExtensionType CustomScriptExtension

Name   Location ProvisioningState
----   -------- -----------------
custom eastus   Succeeded
```

<span data-ttu-id="d6cbc-111">Define uma extensão em um computador.</span><span class="sxs-lookup"><span data-stu-id="d6cbc-111">Sets an extension on a machine.</span></span>

### <span data-ttu-id="d6cbc-112">Exemplo 2: definir uma extensão com parâmetros de extensão especificados via pipeline</span><span class="sxs-lookup"><span data-stu-id="d6cbc-112">Example 2: Set an extension with extension parameters specified via the pipeline</span></span>
```powershell
PS C:\> $otherExtension = Get-AzConnectedMachineExtension -Name custom -ResourceGroupName ContosoTest -MachineName other
PS C:\> $otherExtension | Set-AzConnectedMachineExtension -Name custom -ResourceGroupName ContosoTest -MachineName important

Name   Location ProvisioningState
----   -------- -----------------
custom eastus   Succeeded
```

<span data-ttu-id="d6cbc-113">Isso define uma extensão com os parâmetros de extensão fornecidos pelo objeto passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="d6cbc-113">This sets an extension with the extension parameters provided by the object passed in via the pipeline.</span></span>
<span data-ttu-id="d6cbc-114">Isso é ótimo se você quiser pegar os parâmetros de uma máquina e aplicá-la a outro computador.</span><span class="sxs-lookup"><span data-stu-id="d6cbc-114">This is great if you want to grab the parameters of one machine and apply it to another machine.</span></span>

## <span data-ttu-id="d6cbc-115">OS</span><span class="sxs-lookup"><span data-stu-id="d6cbc-115">PARAMETERS</span></span>

### <span data-ttu-id="d6cbc-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d6cbc-116">-AsJob</span></span>
<span data-ttu-id="d6cbc-117">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="d6cbc-117">Run the command as a job</span></span>

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

### <span data-ttu-id="d6cbc-118">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="d6cbc-118">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="d6cbc-119">Indica se a extensão deve usar uma versão secundária mais recente, se disponível no momento da implantação.</span><span class="sxs-lookup"><span data-stu-id="d6cbc-119">Indicates whether the extension should use a newer minor version if one is available at deployment time.</span></span>
<span data-ttu-id="d6cbc-120">Depois de implantada, no entanto, a extensão não atualizará versões secundárias, a menos que reimplantada, mesmo com essa propriedade definida como true.</span><span class="sxs-lookup"><span data-stu-id="d6cbc-120">Once deployed, however, the extension will not upgrade minor versions unless redeployed, even with this property set to true.</span></span>

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

### <span data-ttu-id="d6cbc-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6cbc-121">-DefaultProfile</span></span>
<span data-ttu-id="d6cbc-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d6cbc-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d6cbc-123">-ExtensionParameter</span><span class="sxs-lookup"><span data-stu-id="d6cbc-123">-ExtensionParameter</span></span>
<span data-ttu-id="d6cbc-124">Descreve uma extensão de máquina.</span><span class="sxs-lookup"><span data-stu-id="d6cbc-124">Describes a Machine Extension.</span></span>
<span data-ttu-id="d6cbc-125">Para construir, consulte a seção notas para propriedades EXTENSIONPARAMETER e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="d6cbc-125">To construct, see NOTES section for EXTENSIONPARAMETER properties and create a hash table.</span></span>

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

### <span data-ttu-id="d6cbc-126">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="d6cbc-126">-ExtensionType</span></span>
<span data-ttu-id="d6cbc-127">Especifica o tipo da extensão; um exemplo é "CustomScriptExtension".</span><span class="sxs-lookup"><span data-stu-id="d6cbc-127">Specifies the type of the extension; an example is "CustomScriptExtension".</span></span>

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

### <span data-ttu-id="d6cbc-128">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="d6cbc-128">-ForceRerun</span></span>
<span data-ttu-id="d6cbc-129">Como o manipulador de extensão deve ser forçado a atualizar mesmo que a configuração de extensão não tenha sido alterada.</span><span class="sxs-lookup"><span data-stu-id="d6cbc-129">How the extension handler should be forced to update even if the extension configuration has not changed.</span></span>

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

### <span data-ttu-id="d6cbc-130">-Local</span><span class="sxs-lookup"><span data-stu-id="d6cbc-130">-Location</span></span>
<span data-ttu-id="d6cbc-131">A localização geográfica onde reside o recurso</span><span class="sxs-lookup"><span data-stu-id="d6cbc-131">The geo-location where the resource lives</span></span>

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

### <span data-ttu-id="d6cbc-132">-MachineName</span><span class="sxs-lookup"><span data-stu-id="d6cbc-132">-MachineName</span></span>
<span data-ttu-id="d6cbc-133">O nome da máquina na qual a extensão deve ser criada ou atualizada.</span><span class="sxs-lookup"><span data-stu-id="d6cbc-133">The name of the machine where the extension should be created or updated.</span></span>

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

### <span data-ttu-id="d6cbc-134">-Nome</span><span class="sxs-lookup"><span data-stu-id="d6cbc-134">-Name</span></span>
<span data-ttu-id="d6cbc-135">O nome da extensão da máquina.</span><span class="sxs-lookup"><span data-stu-id="d6cbc-135">The name of the machine extension.</span></span>

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

### <span data-ttu-id="d6cbc-136">-Nowait</span><span class="sxs-lookup"><span data-stu-id="d6cbc-136">-NoWait</span></span>
<span data-ttu-id="d6cbc-137">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="d6cbc-137">Run the command asynchronously</span></span>

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

### <span data-ttu-id="d6cbc-138">-ProtectedSetting</span><span class="sxs-lookup"><span data-stu-id="d6cbc-138">-ProtectedSetting</span></span>
<span data-ttu-id="d6cbc-139">A extensão pode conter o protectedSettings ou o protectedSettingsFromKeyVault ou nenhuma configuração protegida.</span><span class="sxs-lookup"><span data-stu-id="d6cbc-139">The extension can contain either protectedSettings or protectedSettingsFromKeyVault or no protected settings at all.</span></span>

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

### <span data-ttu-id="d6cbc-140">-Publisher</span><span class="sxs-lookup"><span data-stu-id="d6cbc-140">-Publisher</span></span>
<span data-ttu-id="d6cbc-141">O nome do fornecedor do manipulador de extensão.</span><span class="sxs-lookup"><span data-stu-id="d6cbc-141">The name of the extension handler publisher.</span></span>

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

### <span data-ttu-id="d6cbc-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6cbc-142">-ResourceGroupName</span></span>
<span data-ttu-id="d6cbc-143">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d6cbc-143">The name of the resource group.</span></span>

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

### <span data-ttu-id="d6cbc-144">-Configuração</span><span class="sxs-lookup"><span data-stu-id="d6cbc-144">-Setting</span></span>
<span data-ttu-id="d6cbc-145">Configurações públicas formatadas como JSON para a extensão.</span><span class="sxs-lookup"><span data-stu-id="d6cbc-145">Json formatted public settings for the extension.</span></span>

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

### <span data-ttu-id="d6cbc-146">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d6cbc-146">-SubscriptionId</span></span>
<span data-ttu-id="d6cbc-147">Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="d6cbc-147">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="d6cbc-148">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="d6cbc-148">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="d6cbc-149">-Marca</span><span class="sxs-lookup"><span data-stu-id="d6cbc-149">-Tag</span></span>
<span data-ttu-id="d6cbc-150">Marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="d6cbc-150">Resource tags.</span></span>

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

### <span data-ttu-id="d6cbc-151">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="d6cbc-151">-TypeHandlerVersion</span></span>
<span data-ttu-id="d6cbc-152">Especifica a versão do manipulador de script.</span><span class="sxs-lookup"><span data-stu-id="d6cbc-152">Specifies the version of the script handler.</span></span>

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

### <span data-ttu-id="d6cbc-153">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d6cbc-153">-Confirm</span></span>
<span data-ttu-id="d6cbc-154">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d6cbc-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d6cbc-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d6cbc-155">-WhatIf</span></span>
<span data-ttu-id="d6cbc-156">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d6cbc-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d6cbc-157">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d6cbc-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d6cbc-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6cbc-158">CommonParameters</span></span>
<span data-ttu-id="d6cbc-159">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6cbc-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6cbc-160">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d6cbc-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6cbc-161">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d6cbc-161">INPUTS</span></span>

### <span data-ttu-id="d6cbc-162">Microsoft. Azure. PowerShell. cmdlets. ConnectedMachine. Models. Api20200802. IMachineExtension</span><span class="sxs-lookup"><span data-stu-id="d6cbc-162">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span></span>

## <span data-ttu-id="d6cbc-163">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d6cbc-163">OUTPUTS</span></span>

### <span data-ttu-id="d6cbc-164">Microsoft. Azure. PowerShell. cmdlets. ConnectedMachine. Models. Api20200802. IMachineExtension</span><span class="sxs-lookup"><span data-stu-id="d6cbc-164">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span></span>

## <span data-ttu-id="d6cbc-165">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d6cbc-165">NOTES</span></span>

<span data-ttu-id="d6cbc-166">ALIASES</span><span class="sxs-lookup"><span data-stu-id="d6cbc-166">ALIASES</span></span>

<span data-ttu-id="d6cbc-167">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="d6cbc-167">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d6cbc-168">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="d6cbc-168">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d6cbc-169">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d6cbc-169">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d6cbc-170">EXTENSIONPARAMETER <IMachineExtension> : descreve uma extensão de máquina.</span><span class="sxs-lookup"><span data-stu-id="d6cbc-170">EXTENSIONPARAMETER <IMachineExtension>: Describes a Machine Extension.</span></span>
  - <span data-ttu-id="d6cbc-171">`Location <String>`: A localização geográfica onde reside o recurso</span><span class="sxs-lookup"><span data-stu-id="d6cbc-171">`Location <String>`: The geo-location where the resource lives</span></span>
  - <span data-ttu-id="d6cbc-172">`[Tag <ITrackedResourceTags>]`: Marcas do recurso.</span><span class="sxs-lookup"><span data-stu-id="d6cbc-172">`[Tag <ITrackedResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="d6cbc-173">`[(Any) <String>]`: Isso indica que qualquer propriedade pode ser adicionada a esse objeto.</span><span class="sxs-lookup"><span data-stu-id="d6cbc-173">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="d6cbc-174">`[AutoUpgradeMinorVersion <Boolean?>]`: Indica se a extensão deve usar uma versão secundária mais recente, se disponível no momento da implantação.</span><span class="sxs-lookup"><span data-stu-id="d6cbc-174">`[AutoUpgradeMinorVersion <Boolean?>]`: Indicates whether the extension should use a newer minor version if one is available at deployment time.</span></span> <span data-ttu-id="d6cbc-175">Depois de implantada, no entanto, a extensão não atualizará versões secundárias, a menos que reimplantada, mesmo com essa propriedade definida como true.</span><span class="sxs-lookup"><span data-stu-id="d6cbc-175">Once deployed, however, the extension will not upgrade minor versions unless redeployed, even with this property set to true.</span></span>
  - <span data-ttu-id="d6cbc-176">`[ForceUpdateTag <String>]`: Como o manipulador de extensão deve ser forçado a atualizar mesmo que a configuração de extensão não tenha sido alterada.</span><span class="sxs-lookup"><span data-stu-id="d6cbc-176">`[ForceUpdateTag <String>]`: How the extension handler should be forced to update even if the extension configuration has not changed.</span></span>
  - <span data-ttu-id="d6cbc-177">`[MachineExtensionType <String>]`: Especifica o tipo da extensão; um exemplo é "CustomScriptExtension".</span><span class="sxs-lookup"><span data-stu-id="d6cbc-177">`[MachineExtensionType <String>]`: Specifies the type of the extension; an example is "CustomScriptExtension".</span></span>
  - <span data-ttu-id="d6cbc-178">`[ProtectedSetting <IMachineExtensionPropertiesProtectedSettings>]`: A extensão pode conter o protectedSettings ou o protectedSettingsFromKeyVault ou nenhuma configuração protegida.</span><span class="sxs-lookup"><span data-stu-id="d6cbc-178">`[ProtectedSetting <IMachineExtensionPropertiesProtectedSettings>]`: The extension can contain either protectedSettings or protectedSettingsFromKeyVault or no protected settings at all.</span></span>
  - <span data-ttu-id="d6cbc-179">`[Publisher <String>]`: O nome do fornecedor do manipulador de extensão.</span><span class="sxs-lookup"><span data-stu-id="d6cbc-179">`[Publisher <String>]`: The name of the extension handler publisher.</span></span>
  - <span data-ttu-id="d6cbc-180">`[Setting <IMachineExtensionPropertiesSettings>]`: Configurações públicas formatadas por JSON para a extensão.</span><span class="sxs-lookup"><span data-stu-id="d6cbc-180">`[Setting <IMachineExtensionPropertiesSettings>]`: Json formatted public settings for the extension.</span></span>
  - <span data-ttu-id="d6cbc-181">`[TypeHandlerVersion <String>]`: Especifica a versão do manipulador de script.</span><span class="sxs-lookup"><span data-stu-id="d6cbc-181">`[TypeHandlerVersion <String>]`: Specifies the version of the script handler.</span></span>

## <span data-ttu-id="d6cbc-182">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d6cbc-182">RELATED LINKS</span></span>


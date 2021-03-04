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
# <span data-ttu-id="cf117-101">Update-AzConnectedMachineExtension</span><span class="sxs-lookup"><span data-stu-id="cf117-101">Update-AzConnectedMachineExtension</span></span>

## <span data-ttu-id="cf117-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cf117-102">SYNOPSIS</span></span>
<span data-ttu-id="cf117-103">A operação para criar ou atualizar a extensão.</span><span class="sxs-lookup"><span data-stu-id="cf117-103">The operation to create or update the extension.</span></span>

## <span data-ttu-id="cf117-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="cf117-104">SYNTAX</span></span>

### <span data-ttu-id="cf117-105">UpdateExpanded (Padrão)</span><span class="sxs-lookup"><span data-stu-id="cf117-105">UpdateExpanded (Default)</span></span>
```
Update-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-AutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-ProtectedSetting <IMachineExtensionUpdatePropertiesProtectedSettings>] [-Publisher <String>]
 [-Setting <IMachineExtensionUpdatePropertiesSettings>] [-Tag <Hashtable>] [-Type <String>]
 [-TypeHandlerVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="cf117-106">Atualização</span><span class="sxs-lookup"><span data-stu-id="cf117-106">Update</span></span>
```
Update-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 -ExtensionParameter <IMachineExtensionUpdate> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="cf117-107">UpdateViaIdentity</span><span class="sxs-lookup"><span data-stu-id="cf117-107">UpdateViaIdentity</span></span>
```
Update-AzConnectedMachineExtension -InputObject <IConnectedMachineIdentity>
 -ExtensionParameter <IMachineExtensionUpdate> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="cf117-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="cf117-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzConnectedMachineExtension -InputObject <IConnectedMachineIdentity> [-AutoUpgradeMinorVersion]
 [-ForceRerun <String>] [-ProtectedSetting <IMachineExtensionUpdatePropertiesProtectedSettings>]
 [-Publisher <String>] [-Setting <IMachineExtensionUpdatePropertiesSettings>] [-Tag <Hashtable>]
 [-Type <String>] [-TypeHandlerVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="cf117-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="cf117-109">DESCRIPTION</span></span>
<span data-ttu-id="cf117-110">A operação para criar ou atualizar a extensão.</span><span class="sxs-lookup"><span data-stu-id="cf117-110">The operation to create or update the extension.</span></span>

## <span data-ttu-id="cf117-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cf117-111">EXAMPLES</span></span>

### <span data-ttu-id="cf117-112">Exemplo 1: atualizar uma extensão</span><span class="sxs-lookup"><span data-stu-id="cf117-112">Example 1: Update an extension</span></span>
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

<span data-ttu-id="cf117-113">Atualiza uma extensão em um computador específico.</span><span class="sxs-lookup"><span data-stu-id="cf117-113">Updates an extension on a specific machine.</span></span>

### <span data-ttu-id="cf117-114">Exemplo 2: atualizar uma extensão com o local especificado por meio do pipeline</span><span class="sxs-lookup"><span data-stu-id="cf117-114">Example 2: Update an extension with location specified via the pipeline</span></span>
```powershell
PS C:\> $extToUpdate = Get-AzConnectedMachineExtension -ResourceGroupName connectedMachines -MachineName linux-eastus1_1 -Name customScript
PS C:\> $extToUpdate | Update-AzConnectedMachineExtension -Settings @{
                commandToExecute = "ls -l"
            }

Name         Location ProvisioningState
----         -------- -----------------
customScript eastus   Succeeded
```

<span data-ttu-id="cf117-115">Atualiza uma extensão específica passada pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="cf117-115">Updates a specific extension passed in via the pipeline.</span></span>
<span data-ttu-id="cf117-116">Aqui estamos usando a extensão passada por meio do pipeline para nos ajudar a identificar em qual extensão queremos operar e estamos especificando o que desejamos alterar por meio dos parâmetros normais (como `-Settings` )</span><span class="sxs-lookup"><span data-stu-id="cf117-116">Here we are using the extension passed in via the pipeline to help us identify which extension we want to operate on and are specifying what we want to change via the normal parameters (like `-Settings`)</span></span>

### <span data-ttu-id="cf117-117">Exemplo 3: atualizar uma extensão com parâmetros de extensão especificados por meio do pipeline</span><span class="sxs-lookup"><span data-stu-id="cf117-117">Example 3: Update an extension with extension parameters specified via the pipeline</span></span>
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

<span data-ttu-id="cf117-118">Atualiza uma extensão específica passada pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="cf117-118">Updates a specific extension passed in via the pipeline.</span></span>
<span data-ttu-id="cf117-119">Aqui estamos usando a extensão passada por meio do pipeline para fornecer as alterações que desejamos fazer na extensão.</span><span class="sxs-lookup"><span data-stu-id="cf117-119">Here we are using the extension passed in via the pipeline to provide the changes we want to make on the extension.</span></span>
<span data-ttu-id="cf117-120">O local da extensão não é recuperado por meio do pipeline, mas sim pelos parâmetros especificados normalmente (pelo parâmetro splat).</span><span class="sxs-lookup"><span data-stu-id="cf117-120">The location of the extension is not retrieved via the pipeline but rather via the parameters specified normally (by the splat parameter).</span></span>

### <span data-ttu-id="cf117-121">Exemplo 4: usando um objeto extension como o local e os parâmetros para atualização</span><span class="sxs-lookup"><span data-stu-id="cf117-121">Example 4: Using an extension object as both the location and parameters for updating</span></span>
```powershell
PS C:\> $extToUpdate = Get-AzConnectedMachineExtension -ResourceGroupName connectedMachines -MachineName linux-eastus1_1 -Name customScript
PS C:\> # Update the settings on the object that will be used via the pipeline
PS C:\> $extToUpdate.Setting.commandToExecute = "ls -l"
PS C:\> $extToUpdate | Update-AzConnectedMachineExtension -ExtensionParameter $extToUpdate

Name         Location ProvisioningState
----         -------- -----------------
customScript eastus   Succeeded
```

<span data-ttu-id="cf117-122">Atualiza uma extensão específica passada pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="cf117-122">Updates a specific extension passed in via the pipeline.</span></span>
<span data-ttu-id="cf117-123">Aqui estamos usando a extensão passada por meio do pipeline para nos ajudar a identificar em qual extensão queremos operar.</span><span class="sxs-lookup"><span data-stu-id="cf117-123">Here we are using the extension passed in via the pipeline to help us identify which extension we want to operate on.</span></span>
<span data-ttu-id="cf117-124">Além disso, estamos usando os parâmetros do objeto extension para especificar o que atualizar.</span><span class="sxs-lookup"><span data-stu-id="cf117-124">In addition to that, we are using the parameters of the extension object to specify what to update.</span></span>

## <span data-ttu-id="cf117-125">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="cf117-125">PARAMETERS</span></span>

### <span data-ttu-id="cf117-126">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cf117-126">-AsJob</span></span>
<span data-ttu-id="cf117-127">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="cf117-127">Run the command as a job</span></span>

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

### <span data-ttu-id="cf117-128">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="cf117-128">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="cf117-129">Indica se a extensão deve usar uma versão secundária mais recente se uma estiver disponível no momento da implantação.</span><span class="sxs-lookup"><span data-stu-id="cf117-129">Indicates whether the extension should use a newer minor version if one is available at deployment time.</span></span>
<span data-ttu-id="cf117-130">No entanto, uma vez implantado, a extensão não atualizará versões secundárias, a menos que seja reimplantada, mesmo com essa propriedade definida como true.</span><span class="sxs-lookup"><span data-stu-id="cf117-130">Once deployed, however, the extension will not upgrade minor versions unless redeployed, even with this property set to true.</span></span>

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

### <span data-ttu-id="cf117-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf117-131">-DefaultProfile</span></span>
<span data-ttu-id="cf117-132">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="cf117-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cf117-133">-ExtensionParameter</span><span class="sxs-lookup"><span data-stu-id="cf117-133">-ExtensionParameter</span></span>
<span data-ttu-id="cf117-134">Descreve uma Atualização de Extensão de Máquina.</span><span class="sxs-lookup"><span data-stu-id="cf117-134">Describes a Machine Extension Update.</span></span>
<span data-ttu-id="cf117-135">Para construir, consulte a seção NOTES para propriedades EXTENSIONPARAMETER e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="cf117-135">To construct, see NOTES section for EXTENSIONPARAMETER properties and create a hash table.</span></span>

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

### <span data-ttu-id="cf117-136">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="cf117-136">-ForceRerun</span></span>
<span data-ttu-id="cf117-137">Como o manipulador de extensão deve ser forçado a atualizar mesmo que a configuração da extensão não tenha sido alterada.</span><span class="sxs-lookup"><span data-stu-id="cf117-137">How the extension handler should be forced to update even if the extension configuration has not changed.</span></span>

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

### <span data-ttu-id="cf117-138">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cf117-138">-InputObject</span></span>
<span data-ttu-id="cf117-139">Parâmetro Identity Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="cf117-139">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="cf117-140">-MachineName</span><span class="sxs-lookup"><span data-stu-id="cf117-140">-MachineName</span></span>
<span data-ttu-id="cf117-141">O nome do computador onde a extensão deve ser criada ou atualizada.</span><span class="sxs-lookup"><span data-stu-id="cf117-141">The name of the machine where the extension should be created or updated.</span></span>

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

### <span data-ttu-id="cf117-142">-Name</span><span class="sxs-lookup"><span data-stu-id="cf117-142">-Name</span></span>
<span data-ttu-id="cf117-143">O nome da extensão do computador.</span><span class="sxs-lookup"><span data-stu-id="cf117-143">The name of the machine extension.</span></span>

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

### <span data-ttu-id="cf117-144">-NoWait</span><span class="sxs-lookup"><span data-stu-id="cf117-144">-NoWait</span></span>
<span data-ttu-id="cf117-145">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="cf117-145">Run the command asynchronously</span></span>

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

### <span data-ttu-id="cf117-146">-ProtectedSetting</span><span class="sxs-lookup"><span data-stu-id="cf117-146">-ProtectedSetting</span></span>
<span data-ttu-id="cf117-147">A extensão pode conter protectedSettings ou protectedSettingsFromKeyVault ou nenhuma configuração protegida.</span><span class="sxs-lookup"><span data-stu-id="cf117-147">The extension can contain either protectedSettings or protectedSettingsFromKeyVault or no protected settings at all.</span></span>

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

### <span data-ttu-id="cf117-148">-Publisher</span><span class="sxs-lookup"><span data-stu-id="cf117-148">-Publisher</span></span>
<span data-ttu-id="cf117-149">O nome do editor do manipulador de extensão.</span><span class="sxs-lookup"><span data-stu-id="cf117-149">The name of the extension handler publisher.</span></span>

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

### <span data-ttu-id="cf117-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf117-150">-ResourceGroupName</span></span>
<span data-ttu-id="cf117-151">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="cf117-151">The name of the resource group.</span></span>

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

### <span data-ttu-id="cf117-152">-Setting</span><span class="sxs-lookup"><span data-stu-id="cf117-152">-Setting</span></span>
<span data-ttu-id="cf117-153">Configurações públicas formatadas Json para a extensão.</span><span class="sxs-lookup"><span data-stu-id="cf117-153">Json formatted public settings for the extension.</span></span>

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

### <span data-ttu-id="cf117-154">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cf117-154">-SubscriptionId</span></span>
<span data-ttu-id="cf117-155">Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="cf117-155">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="cf117-156">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="cf117-156">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="cf117-157">-Tag</span><span class="sxs-lookup"><span data-stu-id="cf117-157">-Tag</span></span>
<span data-ttu-id="cf117-158">Marcas de recurso</span><span class="sxs-lookup"><span data-stu-id="cf117-158">Resource tags</span></span>

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

### <span data-ttu-id="cf117-159">-Type</span><span class="sxs-lookup"><span data-stu-id="cf117-159">-Type</span></span>
<span data-ttu-id="cf117-160">Especifica o tipo da extensão; um exemplo é "CustomScriptExtension".</span><span class="sxs-lookup"><span data-stu-id="cf117-160">Specifies the type of the extension; an example is "CustomScriptExtension".</span></span>

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

### <span data-ttu-id="cf117-161">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="cf117-161">-TypeHandlerVersion</span></span>
<span data-ttu-id="cf117-162">Especifica a versão do manipulador de scripts.</span><span class="sxs-lookup"><span data-stu-id="cf117-162">Specifies the version of the script handler.</span></span>

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

### <span data-ttu-id="cf117-163">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cf117-163">-Confirm</span></span>
<span data-ttu-id="cf117-164">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cf117-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cf117-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cf117-165">-WhatIf</span></span>
<span data-ttu-id="cf117-166">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="cf117-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cf117-167">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="cf117-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cf117-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf117-168">CommonParameters</span></span>
<span data-ttu-id="cf117-169">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cf117-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf117-170">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cf117-170">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf117-171">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cf117-171">INPUTS</span></span>

### <span data-ttu-id="cf117-172">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtensionUpdate</span><span class="sxs-lookup"><span data-stu-id="cf117-172">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtensionUpdate</span></span>

### <span data-ttu-id="cf117-173">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.IConnectedMachineIdentity</span><span class="sxs-lookup"><span data-stu-id="cf117-173">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.IConnectedMachineIdentity</span></span>

## <span data-ttu-id="cf117-174">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="cf117-174">OUTPUTS</span></span>

### <span data-ttu-id="cf117-175">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span><span class="sxs-lookup"><span data-stu-id="cf117-175">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span></span>

## <span data-ttu-id="cf117-176">NOTES</span><span class="sxs-lookup"><span data-stu-id="cf117-176">NOTES</span></span>

<span data-ttu-id="cf117-177">ALIASES</span><span class="sxs-lookup"><span data-stu-id="cf117-177">ALIASES</span></span>

<span data-ttu-id="cf117-178">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="cf117-178">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="cf117-179">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="cf117-179">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="cf117-180">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="cf117-180">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="cf117-181">EXTENSIONPARAMETER <IMachineExtensionUpdate> : Descreve uma Atualização de Extensão de Máquina.</span><span class="sxs-lookup"><span data-stu-id="cf117-181">EXTENSIONPARAMETER <IMachineExtensionUpdate>: Describes a Machine Extension Update.</span></span>
  - <span data-ttu-id="cf117-182">`[Tag <IUpdateResourceTags>]`: Marcas de recurso</span><span class="sxs-lookup"><span data-stu-id="cf117-182">`[Tag <IUpdateResourceTags>]`: Resource tags</span></span>
    - <span data-ttu-id="cf117-183">`[(Any) <String>]`: Isso indica que qualquer propriedade pode ser adicionada a esse objeto.</span><span class="sxs-lookup"><span data-stu-id="cf117-183">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="cf117-184">`[AutoUpgradeMinorVersion <Boolean?>]`: Indica se a extensão deve usar uma versão secundária mais recente se uma estiver disponível no momento da implantação.</span><span class="sxs-lookup"><span data-stu-id="cf117-184">`[AutoUpgradeMinorVersion <Boolean?>]`: Indicates whether the extension should use a newer minor version if one is available at deployment time.</span></span> <span data-ttu-id="cf117-185">No entanto, uma vez implantado, a extensão não atualizará versões secundárias, a menos que seja reimplantada, mesmo com essa propriedade definida como true.</span><span class="sxs-lookup"><span data-stu-id="cf117-185">Once deployed, however, the extension will not upgrade minor versions unless redeployed, even with this property set to true.</span></span>
  - <span data-ttu-id="cf117-186">`[ForceUpdateTag <String>]`: Como o manipulador de extensão deve ser forçado a atualizar mesmo que a configuração da extensão não tenha sido alterada.</span><span class="sxs-lookup"><span data-stu-id="cf117-186">`[ForceUpdateTag <String>]`: How the extension handler should be forced to update even if the extension configuration has not changed.</span></span>
  - <span data-ttu-id="cf117-187">`[ProtectedSetting <IMachineExtensionUpdatePropertiesProtectedSettings>]`: A extensão pode conter protectedSettings ou protectedSettingsFromKeyVault ou nenhuma configuração protegida.</span><span class="sxs-lookup"><span data-stu-id="cf117-187">`[ProtectedSetting <IMachineExtensionUpdatePropertiesProtectedSettings>]`: The extension can contain either protectedSettings or protectedSettingsFromKeyVault or no protected settings at all.</span></span>
  - <span data-ttu-id="cf117-188">`[Publisher <String>]`: O nome do editor do manipulador de extensão.</span><span class="sxs-lookup"><span data-stu-id="cf117-188">`[Publisher <String>]`: The name of the extension handler publisher.</span></span>
  - <span data-ttu-id="cf117-189">`[Setting <IMachineExtensionUpdatePropertiesSettings>]`: Configurações públicas formatadas Json para a extensão.</span><span class="sxs-lookup"><span data-stu-id="cf117-189">`[Setting <IMachineExtensionUpdatePropertiesSettings>]`: Json formatted public settings for the extension.</span></span>
  - <span data-ttu-id="cf117-190">`[Type <String>]`: Especifica o tipo da extensão; um exemplo é "CustomScriptExtension".</span><span class="sxs-lookup"><span data-stu-id="cf117-190">`[Type <String>]`: Specifies the type of the extension; an example is "CustomScriptExtension".</span></span>
  - <span data-ttu-id="cf117-191">`[TypeHandlerVersion <String>]`: Especifica a versão do manipulador de scripts.</span><span class="sxs-lookup"><span data-stu-id="cf117-191">`[TypeHandlerVersion <String>]`: Specifies the version of the script handler.</span></span>

<span data-ttu-id="cf117-192">INPUTOBJECT <IConnectedMachineIdentity> : Parâmetro Identity</span><span class="sxs-lookup"><span data-stu-id="cf117-192">INPUTOBJECT <IConnectedMachineIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="cf117-193">`[ExtensionName <String>]`: O nome da extensão do computador.</span><span class="sxs-lookup"><span data-stu-id="cf117-193">`[ExtensionName <String>]`: The name of the machine extension.</span></span>
  - <span data-ttu-id="cf117-194">`[Id <String>]`: Caminho da identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="cf117-194">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="cf117-195">`[Name <String>]`: O nome da máquina híbrida.</span><span class="sxs-lookup"><span data-stu-id="cf117-195">`[Name <String>]`: The name of the hybrid machine.</span></span>
  - <span data-ttu-id="cf117-196">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="cf117-196">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="cf117-197">`[SubscriptionId <String>]`: Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="cf117-197">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="cf117-198">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="cf117-198">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="cf117-199">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cf117-199">RELATED LINKS</span></span>


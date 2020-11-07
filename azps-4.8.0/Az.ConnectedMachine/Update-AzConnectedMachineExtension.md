---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedmachine/update-azconnectedmachineextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Update-AzConnectedMachineExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Update-AzConnectedMachineExtension.md
ms.openlocfilehash: 95334b4f67685183e499518b068f1003f5bb6547
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93955026"
---
# <span data-ttu-id="35d71-101">Update-AzConnectedMachineExtension</span><span class="sxs-lookup"><span data-stu-id="35d71-101">Update-AzConnectedMachineExtension</span></span>

## <span data-ttu-id="35d71-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="35d71-102">SYNOPSIS</span></span>
<span data-ttu-id="35d71-103">A operação para criar ou atualizar a extensão.</span><span class="sxs-lookup"><span data-stu-id="35d71-103">The operation to create or update the extension.</span></span>

## <span data-ttu-id="35d71-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="35d71-104">SYNTAX</span></span>

### <span data-ttu-id="35d71-105">UpdateExpanded (padrão)</span><span class="sxs-lookup"><span data-stu-id="35d71-105">UpdateExpanded (Default)</span></span>
```
Update-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-AutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-ProtectedSetting <IMachineExtensionUpdatePropertiesProtectedSettings>] [-Publisher <String>]
 [-Setting <IMachineExtensionUpdatePropertiesSettings>] [-Tag <Hashtable>] [-Type <String>]
 [-TypeHandlerVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="35d71-106">Atualização</span><span class="sxs-lookup"><span data-stu-id="35d71-106">Update</span></span>
```
Update-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 -ExtensionParameter <IMachineExtensionUpdate> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="35d71-107">UpdateViaIdentity</span><span class="sxs-lookup"><span data-stu-id="35d71-107">UpdateViaIdentity</span></span>
```
Update-AzConnectedMachineExtension -InputObject <IConnectedMachineIdentity>
 -ExtensionParameter <IMachineExtensionUpdate> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="35d71-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="35d71-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzConnectedMachineExtension -InputObject <IConnectedMachineIdentity> [-AutoUpgradeMinorVersion]
 [-ForceRerun <String>] [-ProtectedSetting <IMachineExtensionUpdatePropertiesProtectedSettings>]
 [-Publisher <String>] [-Setting <IMachineExtensionUpdatePropertiesSettings>] [-Tag <Hashtable>]
 [-Type <String>] [-TypeHandlerVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="35d71-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="35d71-109">DESCRIPTION</span></span>
<span data-ttu-id="35d71-110">A operação para criar ou atualizar a extensão.</span><span class="sxs-lookup"><span data-stu-id="35d71-110">The operation to create or update the extension.</span></span>

## <span data-ttu-id="35d71-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="35d71-111">EXAMPLES</span></span>

### <span data-ttu-id="35d71-112">Exemplo 1: atualizar uma extensão</span><span class="sxs-lookup"><span data-stu-id="35d71-112">Example 1: Update an extension</span></span>
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

<span data-ttu-id="35d71-113">Atualiza uma extensão em um computador específico.</span><span class="sxs-lookup"><span data-stu-id="35d71-113">Updates an extension on a specific machine.</span></span>

### <span data-ttu-id="35d71-114">Exemplo 2: atualizar uma extensão com local especificado via pipeline</span><span class="sxs-lookup"><span data-stu-id="35d71-114">Example 2: Update an extension with location specified via the pipeline</span></span>
```powershell
PS C:\> $extToUpdate = Get-AzConnectedMachineExtension -ResourceGroupName connectedMachines -MachineName linux-eastus1_1 -Name customScript
PS C:\> $extToUpdate | Update-AzConnectedMachineExtension -Settings @{
                commandToExecute = "ls -l"
            }

Name         Location ProvisioningState
----         -------- -----------------
customScript eastus   Succeeded
```

<span data-ttu-id="35d71-115">Atualiza uma extensão específica passada pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="35d71-115">Updates a specific extension passed in via the pipeline.</span></span>
<span data-ttu-id="35d71-116">Aqui estamos usando a extensão passada pelo pipeline para nos ajudar a identificar em qual extensão queremos operar e estamos especificando o que queremos alterar pelos parâmetros normais (como `-Settings` )</span><span class="sxs-lookup"><span data-stu-id="35d71-116">Here we are using the extension passed in via the pipeline to help us identify which extension we want to operate on and are specifying what we want to change via the normal parameters (like `-Settings`)</span></span>

### <span data-ttu-id="35d71-117">Exemplo 3: atualizar uma extensão com parâmetros de extensão especificados via pipeline</span><span class="sxs-lookup"><span data-stu-id="35d71-117">Example 3: Update an extension with extension parameters specified via the pipeline</span></span>
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

<span data-ttu-id="35d71-118">Atualiza uma extensão específica passada pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="35d71-118">Updates a specific extension passed in via the pipeline.</span></span>
<span data-ttu-id="35d71-119">Aqui estamos usando a extensão passada pelo pipeline para fornecer as alterações que desejamos fazer na extensão.</span><span class="sxs-lookup"><span data-stu-id="35d71-119">Here we are using the extension passed in via the pipeline to provide the changes we want to make on the extension.</span></span>
<span data-ttu-id="35d71-120">O local da extensão não é recuperado via pipeline, mas por meio dos parâmetros especificados normalmente (pelo parâmetro splat).</span><span class="sxs-lookup"><span data-stu-id="35d71-120">The location of the extension is not retrieved via the pipeline but rather via the parameters specified normally (by the splat parameter).</span></span>

### <span data-ttu-id="35d71-121">Exemplo 4: usando um objeto de extensão como o local e os parâmetros para atualização</span><span class="sxs-lookup"><span data-stu-id="35d71-121">Example 4: Using an extension object as both the location and parameters for updating</span></span>
```powershell
PS C:\> $extToUpdate = Get-AzConnectedMachineExtension -ResourceGroupName connectedMachines -MachineName linux-eastus1_1 -Name customScript
PS C:\> # Update the settings on the object that will be used via the pipeline
PS C:\> $extToUpdate.Setting.commandToExecute = "ls -l"
PS C:\> $extToUpdate | Update-AzConnectedMachineExtension -ExtensionParameter $extToUpdate

Name         Location ProvisioningState
----         -------- -----------------
customScript eastus   Succeeded
```

<span data-ttu-id="35d71-122">Atualiza uma extensão específica passada pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="35d71-122">Updates a specific extension passed in via the pipeline.</span></span>
<span data-ttu-id="35d71-123">Aqui estamos usando a extensão passada pelo pipeline para nos ajudar a identificar em qual extensão queremos operar.</span><span class="sxs-lookup"><span data-stu-id="35d71-123">Here we are using the extension passed in via the pipeline to help us identify which extension we want to operate on.</span></span>
<span data-ttu-id="35d71-124">Além disso, estamos usando os parâmetros do objeto de extensão para especificar o que atualizar.</span><span class="sxs-lookup"><span data-stu-id="35d71-124">In addition to that, we are using the parameters of the extension object to specify what to update.</span></span>

## <span data-ttu-id="35d71-125">OS</span><span class="sxs-lookup"><span data-stu-id="35d71-125">PARAMETERS</span></span>

### <span data-ttu-id="35d71-126">-AsJob</span><span class="sxs-lookup"><span data-stu-id="35d71-126">-AsJob</span></span>
<span data-ttu-id="35d71-127">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="35d71-127">Run the command as a job</span></span>

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

### <span data-ttu-id="35d71-128">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="35d71-128">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="35d71-129">Indica se a extensão deve usar uma versão secundária mais recente, se disponível no momento da implantação.</span><span class="sxs-lookup"><span data-stu-id="35d71-129">Indicates whether the extension should use a newer minor version if one is available at deployment time.</span></span>
<span data-ttu-id="35d71-130">Depois de implantada, no entanto, a extensão não atualizará versões secundárias, a menos que reimplantada, mesmo com essa propriedade definida como true.</span><span class="sxs-lookup"><span data-stu-id="35d71-130">Once deployed, however, the extension will not upgrade minor versions unless redeployed, even with this property set to true.</span></span>

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

### <span data-ttu-id="35d71-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35d71-131">-DefaultProfile</span></span>
<span data-ttu-id="35d71-132">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="35d71-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="35d71-133">-ExtensionParameter</span><span class="sxs-lookup"><span data-stu-id="35d71-133">-ExtensionParameter</span></span>
<span data-ttu-id="35d71-134">Descreve uma atualização de extensão da máquina.</span><span class="sxs-lookup"><span data-stu-id="35d71-134">Describes a Machine Extension Update.</span></span>
<span data-ttu-id="35d71-135">Para construir, consulte a seção notas para propriedades EXTENSIONPARAMETER e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="35d71-135">To construct, see NOTES section for EXTENSIONPARAMETER properties and create a hash table.</span></span>

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

### <span data-ttu-id="35d71-136">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="35d71-136">-ForceRerun</span></span>
<span data-ttu-id="35d71-137">Como o manipulador de extensão deve ser forçado a atualizar mesmo que a configuração de extensão não tenha sido alterada.</span><span class="sxs-lookup"><span data-stu-id="35d71-137">How the extension handler should be forced to update even if the extension configuration has not changed.</span></span>

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

### <span data-ttu-id="35d71-138">-InputObject</span><span class="sxs-lookup"><span data-stu-id="35d71-138">-InputObject</span></span>
<span data-ttu-id="35d71-139">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="35d71-139">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="35d71-140">-MachineName</span><span class="sxs-lookup"><span data-stu-id="35d71-140">-MachineName</span></span>
<span data-ttu-id="35d71-141">O nome da máquina na qual a extensão deve ser criada ou atualizada.</span><span class="sxs-lookup"><span data-stu-id="35d71-141">The name of the machine where the extension should be created or updated.</span></span>

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

### <span data-ttu-id="35d71-142">-Nome</span><span class="sxs-lookup"><span data-stu-id="35d71-142">-Name</span></span>
<span data-ttu-id="35d71-143">O nome da extensão da máquina.</span><span class="sxs-lookup"><span data-stu-id="35d71-143">The name of the machine extension.</span></span>

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

### <span data-ttu-id="35d71-144">-Nowait</span><span class="sxs-lookup"><span data-stu-id="35d71-144">-NoWait</span></span>
<span data-ttu-id="35d71-145">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="35d71-145">Run the command asynchronously</span></span>

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

### <span data-ttu-id="35d71-146">-ProtectedSetting</span><span class="sxs-lookup"><span data-stu-id="35d71-146">-ProtectedSetting</span></span>
<span data-ttu-id="35d71-147">A extensão pode conter o protectedSettings ou o protectedSettingsFromKeyVault ou nenhuma configuração protegida.</span><span class="sxs-lookup"><span data-stu-id="35d71-147">The extension can contain either protectedSettings or protectedSettingsFromKeyVault or no protected settings at all.</span></span>

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

### <span data-ttu-id="35d71-148">-Publisher</span><span class="sxs-lookup"><span data-stu-id="35d71-148">-Publisher</span></span>
<span data-ttu-id="35d71-149">O nome do fornecedor do manipulador de extensão.</span><span class="sxs-lookup"><span data-stu-id="35d71-149">The name of the extension handler publisher.</span></span>

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

### <span data-ttu-id="35d71-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35d71-150">-ResourceGroupName</span></span>
<span data-ttu-id="35d71-151">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="35d71-151">The name of the resource group.</span></span>

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

### <span data-ttu-id="35d71-152">-Configuração</span><span class="sxs-lookup"><span data-stu-id="35d71-152">-Setting</span></span>
<span data-ttu-id="35d71-153">Configurações públicas formatadas como JSON para a extensão.</span><span class="sxs-lookup"><span data-stu-id="35d71-153">Json formatted public settings for the extension.</span></span>

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

### <span data-ttu-id="35d71-154">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="35d71-154">-SubscriptionId</span></span>
<span data-ttu-id="35d71-155">Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="35d71-155">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="35d71-156">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="35d71-156">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="35d71-157">-Marca</span><span class="sxs-lookup"><span data-stu-id="35d71-157">-Tag</span></span>
<span data-ttu-id="35d71-158">Marcas de recurso</span><span class="sxs-lookup"><span data-stu-id="35d71-158">Resource tags</span></span>

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

### <span data-ttu-id="35d71-159">-Digite</span><span class="sxs-lookup"><span data-stu-id="35d71-159">-Type</span></span>
<span data-ttu-id="35d71-160">Especifica o tipo da extensão; um exemplo é "CustomScriptExtension".</span><span class="sxs-lookup"><span data-stu-id="35d71-160">Specifies the type of the extension; an example is "CustomScriptExtension".</span></span>

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

### <span data-ttu-id="35d71-161">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="35d71-161">-TypeHandlerVersion</span></span>
<span data-ttu-id="35d71-162">Especifica a versão do manipulador de script.</span><span class="sxs-lookup"><span data-stu-id="35d71-162">Specifies the version of the script handler.</span></span>

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

### <span data-ttu-id="35d71-163">-Confirme</span><span class="sxs-lookup"><span data-stu-id="35d71-163">-Confirm</span></span>
<span data-ttu-id="35d71-164">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="35d71-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="35d71-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35d71-165">-WhatIf</span></span>
<span data-ttu-id="35d71-166">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="35d71-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="35d71-167">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="35d71-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="35d71-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35d71-168">CommonParameters</span></span>
<span data-ttu-id="35d71-169">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35d71-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35d71-170">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="35d71-170">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35d71-171">SENSORES</span><span class="sxs-lookup"><span data-stu-id="35d71-171">INPUTS</span></span>

### <span data-ttu-id="35d71-172">Microsoft. Azure. PowerShell. cmdlets. ConnectedMachine. Models. Api20200802. IMachineExtensionUpdate</span><span class="sxs-lookup"><span data-stu-id="35d71-172">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtensionUpdate</span></span>

### <span data-ttu-id="35d71-173">Microsoft. Azure. PowerShell. cmdlets. ConnectedMachine. Models. IConnectedMachineIdentity</span><span class="sxs-lookup"><span data-stu-id="35d71-173">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.IConnectedMachineIdentity</span></span>

## <span data-ttu-id="35d71-174">EXIBE</span><span class="sxs-lookup"><span data-stu-id="35d71-174">OUTPUTS</span></span>

### <span data-ttu-id="35d71-175">Microsoft. Azure. PowerShell. cmdlets. ConnectedMachine. Models. Api20200802. IMachineExtension</span><span class="sxs-lookup"><span data-stu-id="35d71-175">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span></span>

## <span data-ttu-id="35d71-176">INFORMA</span><span class="sxs-lookup"><span data-stu-id="35d71-176">NOTES</span></span>

<span data-ttu-id="35d71-177">ALIASES</span><span class="sxs-lookup"><span data-stu-id="35d71-177">ALIASES</span></span>

<span data-ttu-id="35d71-178">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="35d71-178">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="35d71-179">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="35d71-179">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="35d71-180">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="35d71-180">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="35d71-181">EXTENSIONPARAMETER <IMachineExtensionUpdate> : descreve uma atualização de extensão da máquina.</span><span class="sxs-lookup"><span data-stu-id="35d71-181">EXTENSIONPARAMETER <IMachineExtensionUpdate>: Describes a Machine Extension Update.</span></span>
  - <span data-ttu-id="35d71-182">`[Tag <IUpdateResourceTags>]`: Marcas de recurso</span><span class="sxs-lookup"><span data-stu-id="35d71-182">`[Tag <IUpdateResourceTags>]`: Resource tags</span></span>
    - <span data-ttu-id="35d71-183">`[(Any) <String>]`: Isso indica que qualquer propriedade pode ser adicionada a esse objeto.</span><span class="sxs-lookup"><span data-stu-id="35d71-183">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="35d71-184">`[AutoUpgradeMinorVersion <Boolean?>]`: Indica se a extensão deve usar uma versão secundária mais recente, se disponível no momento da implantação.</span><span class="sxs-lookup"><span data-stu-id="35d71-184">`[AutoUpgradeMinorVersion <Boolean?>]`: Indicates whether the extension should use a newer minor version if one is available at deployment time.</span></span> <span data-ttu-id="35d71-185">Depois de implantada, no entanto, a extensão não atualizará versões secundárias, a menos que reimplantada, mesmo com essa propriedade definida como true.</span><span class="sxs-lookup"><span data-stu-id="35d71-185">Once deployed, however, the extension will not upgrade minor versions unless redeployed, even with this property set to true.</span></span>
  - <span data-ttu-id="35d71-186">`[ForceUpdateTag <String>]`: Como o manipulador de extensão deve ser forçado a atualizar mesmo que a configuração de extensão não tenha sido alterada.</span><span class="sxs-lookup"><span data-stu-id="35d71-186">`[ForceUpdateTag <String>]`: How the extension handler should be forced to update even if the extension configuration has not changed.</span></span>
  - <span data-ttu-id="35d71-187">`[ProtectedSetting <IMachineExtensionUpdatePropertiesProtectedSettings>]`: A extensão pode conter o protectedSettings ou o protectedSettingsFromKeyVault ou nenhuma configuração protegida.</span><span class="sxs-lookup"><span data-stu-id="35d71-187">`[ProtectedSetting <IMachineExtensionUpdatePropertiesProtectedSettings>]`: The extension can contain either protectedSettings or protectedSettingsFromKeyVault or no protected settings at all.</span></span>
  - <span data-ttu-id="35d71-188">`[Publisher <String>]`: O nome do fornecedor do manipulador de extensão.</span><span class="sxs-lookup"><span data-stu-id="35d71-188">`[Publisher <String>]`: The name of the extension handler publisher.</span></span>
  - <span data-ttu-id="35d71-189">`[Setting <IMachineExtensionUpdatePropertiesSettings>]`: Configurações públicas formatadas por JSON para a extensão.</span><span class="sxs-lookup"><span data-stu-id="35d71-189">`[Setting <IMachineExtensionUpdatePropertiesSettings>]`: Json formatted public settings for the extension.</span></span>
  - <span data-ttu-id="35d71-190">`[Type <String>]`: Especifica o tipo da extensão; um exemplo é "CustomScriptExtension".</span><span class="sxs-lookup"><span data-stu-id="35d71-190">`[Type <String>]`: Specifies the type of the extension; an example is "CustomScriptExtension".</span></span>
  - <span data-ttu-id="35d71-191">`[TypeHandlerVersion <String>]`: Especifica a versão do manipulador de script.</span><span class="sxs-lookup"><span data-stu-id="35d71-191">`[TypeHandlerVersion <String>]`: Specifies the version of the script handler.</span></span>

<span data-ttu-id="35d71-192">INPUTobject <IConnectedMachineIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="35d71-192">INPUTOBJECT <IConnectedMachineIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="35d71-193">`[ExtensionName <String>]`: O nome da extensão da máquina.</span><span class="sxs-lookup"><span data-stu-id="35d71-193">`[ExtensionName <String>]`: The name of the machine extension.</span></span>
  - <span data-ttu-id="35d71-194">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="35d71-194">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="35d71-195">`[Name <String>]`: O nome da máquina híbrida.</span><span class="sxs-lookup"><span data-stu-id="35d71-195">`[Name <String>]`: The name of the hybrid machine.</span></span>
  - <span data-ttu-id="35d71-196">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="35d71-196">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="35d71-197">`[SubscriptionId <String>]`: Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="35d71-197">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="35d71-198">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="35d71-198">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="35d71-199">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="35d71-199">RELATED LINKS</span></span>


---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedmachine/update-azconnectedmachineextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Update-AzConnectedMachineExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Update-AzConnectedMachineExtension.md
ms.openlocfilehash: 95334b4f67685183e499518b068f1003f5bb6547
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111064"
---
# <span data-ttu-id="808eb-101">Update-AzConnectedMachineExtension</span><span class="sxs-lookup"><span data-stu-id="808eb-101">Update-AzConnectedMachineExtension</span></span>

## <span data-ttu-id="808eb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="808eb-102">SYNOPSIS</span></span>
<span data-ttu-id="808eb-103">A operação para criar ou atualizar a extensão.</span><span class="sxs-lookup"><span data-stu-id="808eb-103">The operation to create or update the extension.</span></span>

## <span data-ttu-id="808eb-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="808eb-104">SYNTAX</span></span>

### <span data-ttu-id="808eb-105">UpdateExpanded (Padrão)</span><span class="sxs-lookup"><span data-stu-id="808eb-105">UpdateExpanded (Default)</span></span>
```
Update-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-AutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-ProtectedSetting <IMachineExtensionUpdatePropertiesProtectedSettings>] [-Publisher <String>]
 [-Setting <IMachineExtensionUpdatePropertiesSettings>] [-Tag <Hashtable>] [-Type <String>]
 [-TypeHandlerVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="808eb-106">Atualização</span><span class="sxs-lookup"><span data-stu-id="808eb-106">Update</span></span>
```
Update-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 -ExtensionParameter <IMachineExtensionUpdate> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="808eb-107">UpdateViaIdentity</span><span class="sxs-lookup"><span data-stu-id="808eb-107">UpdateViaIdentity</span></span>
```
Update-AzConnectedMachineExtension -InputObject <IConnectedMachineIdentity>
 -ExtensionParameter <IMachineExtensionUpdate> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="808eb-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="808eb-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzConnectedMachineExtension -InputObject <IConnectedMachineIdentity> [-AutoUpgradeMinorVersion]
 [-ForceRerun <String>] [-ProtectedSetting <IMachineExtensionUpdatePropertiesProtectedSettings>]
 [-Publisher <String>] [-Setting <IMachineExtensionUpdatePropertiesSettings>] [-Tag <Hashtable>]
 [-Type <String>] [-TypeHandlerVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="808eb-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="808eb-109">DESCRIPTION</span></span>
<span data-ttu-id="808eb-110">A operação para criar ou atualizar a extensão.</span><span class="sxs-lookup"><span data-stu-id="808eb-110">The operation to create or update the extension.</span></span>

## <span data-ttu-id="808eb-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="808eb-111">EXAMPLES</span></span>

### <span data-ttu-id="808eb-112">Exemplo 1: Atualizar uma extensão</span><span class="sxs-lookup"><span data-stu-id="808eb-112">Example 1: Update an extension</span></span>
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

<span data-ttu-id="808eb-113">Atualiza uma extensão em um computador específico.</span><span class="sxs-lookup"><span data-stu-id="808eb-113">Updates an extension on a specific machine.</span></span>

### <span data-ttu-id="808eb-114">Exemplo 2: Atualizar uma extensão com a localização especificada por meio do pipeline</span><span class="sxs-lookup"><span data-stu-id="808eb-114">Example 2: Update an extension with location specified via the pipeline</span></span>
```powershell
PS C:\> $extToUpdate = Get-AzConnectedMachineExtension -ResourceGroupName connectedMachines -MachineName linux-eastus1_1 -Name customScript
PS C:\> $extToUpdate | Update-AzConnectedMachineExtension -Settings @{
                commandToExecute = "ls -l"
            }

Name         Location ProvisioningState
----         -------- -----------------
customScript eastus   Succeeded
```

<span data-ttu-id="808eb-115">Atualiza uma extensão específica passada por meio do pipeline.</span><span class="sxs-lookup"><span data-stu-id="808eb-115">Updates a specific extension passed in via the pipeline.</span></span>
<span data-ttu-id="808eb-116">Aqui estamos usando a extensão passada por meio do pipeline para nos ajudar a identificar em qual extensão desejamos operar e estamos especificando o que desejamos alterar por meio dos parâmetros normais `-Settings` (como)</span><span class="sxs-lookup"><span data-stu-id="808eb-116">Here we are using the extension passed in via the pipeline to help us identify which extension we want to operate on and are specifying what we want to change via the normal parameters (like `-Settings`)</span></span>

### <span data-ttu-id="808eb-117">Exemplo 3: Atualizar uma extensão com parâmetros de extensão especificados por meio do pipeline</span><span class="sxs-lookup"><span data-stu-id="808eb-117">Example 3: Update an extension with extension parameters specified via the pipeline</span></span>
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

<span data-ttu-id="808eb-118">Atualiza uma extensão específica passada por meio do pipeline.</span><span class="sxs-lookup"><span data-stu-id="808eb-118">Updates a specific extension passed in via the pipeline.</span></span>
<span data-ttu-id="808eb-119">Aqui estamos usando a extensão passada por meio do pipeline para fornecer as alterações que desejamos fazer na extensão.</span><span class="sxs-lookup"><span data-stu-id="808eb-119">Here we are using the extension passed in via the pipeline to provide the changes we want to make on the extension.</span></span>
<span data-ttu-id="808eb-120">O local da extensão não é recuperado pelo pipeline, mas sim pelos parâmetros especificados normalmente (pelo parâmetro splat).</span><span class="sxs-lookup"><span data-stu-id="808eb-120">The location of the extension is not retrieved via the pipeline but rather via the parameters specified normally (by the splat parameter).</span></span>

### <span data-ttu-id="808eb-121">Exemplo 4: Usar um objeto de extensão como o local e os parâmetros para atualizar</span><span class="sxs-lookup"><span data-stu-id="808eb-121">Example 4: Using an extension object as both the location and parameters for updating</span></span>
```powershell
PS C:\> $extToUpdate = Get-AzConnectedMachineExtension -ResourceGroupName connectedMachines -MachineName linux-eastus1_1 -Name customScript
PS C:\> # Update the settings on the object that will be used via the pipeline
PS C:\> $extToUpdate.Setting.commandToExecute = "ls -l"
PS C:\> $extToUpdate | Update-AzConnectedMachineExtension -ExtensionParameter $extToUpdate

Name         Location ProvisioningState
----         -------- -----------------
customScript eastus   Succeeded
```

<span data-ttu-id="808eb-122">Atualiza uma extensão específica passada por meio do pipeline.</span><span class="sxs-lookup"><span data-stu-id="808eb-122">Updates a specific extension passed in via the pipeline.</span></span>
<span data-ttu-id="808eb-123">Aqui estamos usando a extensão passada por meio do pipeline para nos ajudar a identificar em qual extensão desejamos operar.</span><span class="sxs-lookup"><span data-stu-id="808eb-123">Here we are using the extension passed in via the pipeline to help us identify which extension we want to operate on.</span></span>
<span data-ttu-id="808eb-124">Além disso, estamos usando os parâmetros do objeto de extensão para especificar o que atualizar.</span><span class="sxs-lookup"><span data-stu-id="808eb-124">In addition to that, we are using the parameters of the extension object to specify what to update.</span></span>

## <span data-ttu-id="808eb-125">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="808eb-125">PARAMETERS</span></span>

### <span data-ttu-id="808eb-126">-AsJob</span><span class="sxs-lookup"><span data-stu-id="808eb-126">-AsJob</span></span>
<span data-ttu-id="808eb-127">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="808eb-127">Run the command as a job</span></span>

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

### <span data-ttu-id="808eb-128">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="808eb-128">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="808eb-129">Indica se a extensão deve usar uma versão secundária mais recente, se estiver disponível no momento da implantação.</span><span class="sxs-lookup"><span data-stu-id="808eb-129">Indicates whether the extension should use a newer minor version if one is available at deployment time.</span></span>
<span data-ttu-id="808eb-130">Uma vez implantada, no entanto, a extensão não atualizará as versões secundárias, a menos que seja reimplantada, mesmo com essa propriedade definida como verdadeira.</span><span class="sxs-lookup"><span data-stu-id="808eb-130">Once deployed, however, the extension will not upgrade minor versions unless redeployed, even with this property set to true.</span></span>

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

### <span data-ttu-id="808eb-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="808eb-131">-DefaultProfile</span></span>
<span data-ttu-id="808eb-132">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="808eb-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="808eb-133">-ExtensionParameter</span><span class="sxs-lookup"><span data-stu-id="808eb-133">-ExtensionParameter</span></span>
<span data-ttu-id="808eb-134">Descreve uma Atualização de Extensão de Máquina.</span><span class="sxs-lookup"><span data-stu-id="808eb-134">Describes a Machine Extension Update.</span></span>
<span data-ttu-id="808eb-135">Para construir, confira a seção ANOTAÇÕES para propriedades EXTENSIONPARAMETER e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="808eb-135">To construct, see NOTES section for EXTENSIONPARAMETER properties and create a hash table.</span></span>

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

### <span data-ttu-id="808eb-136">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="808eb-136">-ForceRerun</span></span>
<span data-ttu-id="808eb-137">Como o manipulador de extensão deve ser obrigado a atualizar mesmo que a configuração de extensão não tenha sido alterada.</span><span class="sxs-lookup"><span data-stu-id="808eb-137">How the extension handler should be forced to update even if the extension configuration has not changed.</span></span>

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

### <span data-ttu-id="808eb-138">-InputObject</span><span class="sxs-lookup"><span data-stu-id="808eb-138">-InputObject</span></span>
<span data-ttu-id="808eb-139">Parâmetro de Identidade Para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="808eb-139">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="808eb-140">-MachineName</span><span class="sxs-lookup"><span data-stu-id="808eb-140">-MachineName</span></span>
<span data-ttu-id="808eb-141">O nome do computador onde a extensão deve ser criada ou atualizada.</span><span class="sxs-lookup"><span data-stu-id="808eb-141">The name of the machine where the extension should be created or updated.</span></span>

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

### <span data-ttu-id="808eb-142">-Nome</span><span class="sxs-lookup"><span data-stu-id="808eb-142">-Name</span></span>
<span data-ttu-id="808eb-143">O nome da extensão do computador.</span><span class="sxs-lookup"><span data-stu-id="808eb-143">The name of the machine extension.</span></span>

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

### <span data-ttu-id="808eb-144">-NoWait</span><span class="sxs-lookup"><span data-stu-id="808eb-144">-NoWait</span></span>
<span data-ttu-id="808eb-145">Executar o comando assíncrona</span><span class="sxs-lookup"><span data-stu-id="808eb-145">Run the command asynchronously</span></span>

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

### <span data-ttu-id="808eb-146">-ProtectedSetting</span><span class="sxs-lookup"><span data-stu-id="808eb-146">-ProtectedSetting</span></span>
<span data-ttu-id="808eb-147">A extensão pode conterSettings protegidos ou protectedSettingsFromKeyVault ou nenhuma configuração protegida.</span><span class="sxs-lookup"><span data-stu-id="808eb-147">The extension can contain either protectedSettings or protectedSettingsFromKeyVault or no protected settings at all.</span></span>

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

### <span data-ttu-id="808eb-148">-Publisher</span><span class="sxs-lookup"><span data-stu-id="808eb-148">-Publisher</span></span>
<span data-ttu-id="808eb-149">O nome do editor do manipulador de extensão.</span><span class="sxs-lookup"><span data-stu-id="808eb-149">The name of the extension handler publisher.</span></span>

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

### <span data-ttu-id="808eb-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="808eb-150">-ResourceGroupName</span></span>
<span data-ttu-id="808eb-151">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="808eb-151">The name of the resource group.</span></span>

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

### <span data-ttu-id="808eb-152">-Configuração</span><span class="sxs-lookup"><span data-stu-id="808eb-152">-Setting</span></span>
<span data-ttu-id="808eb-153">Json formatado configurações públicas para a extensão.</span><span class="sxs-lookup"><span data-stu-id="808eb-153">Json formatted public settings for the extension.</span></span>

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

### <span data-ttu-id="808eb-154">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="808eb-154">-SubscriptionId</span></span>
<span data-ttu-id="808eb-155">Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="808eb-155">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="808eb-156">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="808eb-156">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="808eb-157">-Tag</span><span class="sxs-lookup"><span data-stu-id="808eb-157">-Tag</span></span>
<span data-ttu-id="808eb-158">Marcas de recurso</span><span class="sxs-lookup"><span data-stu-id="808eb-158">Resource tags</span></span>

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

### <span data-ttu-id="808eb-159">-Tipo</span><span class="sxs-lookup"><span data-stu-id="808eb-159">-Type</span></span>
<span data-ttu-id="808eb-160">Especifica o tipo da extensão; um exemplo é "CustomScriptExtension".</span><span class="sxs-lookup"><span data-stu-id="808eb-160">Specifies the type of the extension; an example is "CustomScriptExtension".</span></span>

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

### <span data-ttu-id="808eb-161">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="808eb-161">-TypeHandlerVersion</span></span>
<span data-ttu-id="808eb-162">Especifica a versão do manipulador de script.</span><span class="sxs-lookup"><span data-stu-id="808eb-162">Specifies the version of the script handler.</span></span>

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

### <span data-ttu-id="808eb-163">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="808eb-163">-Confirm</span></span>
<span data-ttu-id="808eb-164">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="808eb-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="808eb-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="808eb-165">-WhatIf</span></span>
<span data-ttu-id="808eb-166">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="808eb-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="808eb-167">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="808eb-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="808eb-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="808eb-168">CommonParameters</span></span>
<span data-ttu-id="808eb-169">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="808eb-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="808eb-170">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="808eb-170">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="808eb-171">Entradas</span><span class="sxs-lookup"><span data-stu-id="808eb-171">INPUTS</span></span>

### <span data-ttu-id="808eb-172">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtensionUpdate</span><span class="sxs-lookup"><span data-stu-id="808eb-172">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtensionUpdate</span></span>

### <span data-ttu-id="808eb-173">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.IConnectedMachineIdentity</span><span class="sxs-lookup"><span data-stu-id="808eb-173">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.IConnectedMachineIdentity</span></span>

## <span data-ttu-id="808eb-174">Saídas</span><span class="sxs-lookup"><span data-stu-id="808eb-174">OUTPUTS</span></span>

### <span data-ttu-id="808eb-175">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span><span class="sxs-lookup"><span data-stu-id="808eb-175">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span></span>

## <span data-ttu-id="808eb-176">Notas</span><span class="sxs-lookup"><span data-stu-id="808eb-176">NOTES</span></span>

<span data-ttu-id="808eb-177">Aliases</span><span class="sxs-lookup"><span data-stu-id="808eb-177">ALIASES</span></span>

<span data-ttu-id="808eb-178">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="808eb-178">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="808eb-179">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="808eb-179">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="808eb-180">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="808eb-180">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="808eb-181">EXTENSIONPARAMETER <IMachineExtensionUpdate> : descreve uma Atualização de Extensão de Máquina.</span><span class="sxs-lookup"><span data-stu-id="808eb-181">EXTENSIONPARAMETER <IMachineExtensionUpdate>: Describes a Machine Extension Update.</span></span>
  - <span data-ttu-id="808eb-182">`[Tag <IUpdateResourceTags>]`: Marcas de recurso</span><span class="sxs-lookup"><span data-stu-id="808eb-182">`[Tag <IUpdateResourceTags>]`: Resource tags</span></span>
    - <span data-ttu-id="808eb-183">`[(Any) <String>]`: indica que qualquer propriedade pode ser adicionada a este objeto.</span><span class="sxs-lookup"><span data-stu-id="808eb-183">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="808eb-184">`[AutoUpgradeMinorVersion <Boolean?>]`: indica se a extensão deve usar uma versão secundária mais recente, se estiver disponível no momento da implantação.</span><span class="sxs-lookup"><span data-stu-id="808eb-184">`[AutoUpgradeMinorVersion <Boolean?>]`: Indicates whether the extension should use a newer minor version if one is available at deployment time.</span></span> <span data-ttu-id="808eb-185">Uma vez implantada, no entanto, a extensão não atualizará as versões secundárias, a menos que seja reimplantada, mesmo com essa propriedade definida como verdadeira.</span><span class="sxs-lookup"><span data-stu-id="808eb-185">Once deployed, however, the extension will not upgrade minor versions unless redeployed, even with this property set to true.</span></span>
  - <span data-ttu-id="808eb-186">`[ForceUpdateTag <String>]`: como o manipulador de extensão deve ser obrigado a atualizar mesmo que a configuração de extensão não tenha sido alterada.</span><span class="sxs-lookup"><span data-stu-id="808eb-186">`[ForceUpdateTag <String>]`: How the extension handler should be forced to update even if the extension configuration has not changed.</span></span>
  - <span data-ttu-id="808eb-187">`[ProtectedSetting <IMachineExtensionUpdatePropertiesProtectedSettings>]`: A extensão pode conterSettings protegidos ou protectedSettingsFromKeyVault ou nenhuma configuração protegida.</span><span class="sxs-lookup"><span data-stu-id="808eb-187">`[ProtectedSetting <IMachineExtensionUpdatePropertiesProtectedSettings>]`: The extension can contain either protectedSettings or protectedSettingsFromKeyVault or no protected settings at all.</span></span>
  - <span data-ttu-id="808eb-188">`[Publisher <String>]`: o nome do editor do manipulador de extensão.</span><span class="sxs-lookup"><span data-stu-id="808eb-188">`[Publisher <String>]`: The name of the extension handler publisher.</span></span>
  - <span data-ttu-id="808eb-189">`[Setting <IMachineExtensionUpdatePropertiesSettings>]`: Json formatou as configurações públicas para a extensão.</span><span class="sxs-lookup"><span data-stu-id="808eb-189">`[Setting <IMachineExtensionUpdatePropertiesSettings>]`: Json formatted public settings for the extension.</span></span>
  - <span data-ttu-id="808eb-190">`[Type <String>]`: especifica o tipo da extensão; um exemplo é "CustomScriptExtension".</span><span class="sxs-lookup"><span data-stu-id="808eb-190">`[Type <String>]`: Specifies the type of the extension; an example is "CustomScriptExtension".</span></span>
  - <span data-ttu-id="808eb-191">`[TypeHandlerVersion <String>]`: especifica a versão do manipulador de script.</span><span class="sxs-lookup"><span data-stu-id="808eb-191">`[TypeHandlerVersion <String>]`: Specifies the version of the script handler.</span></span>

<span data-ttu-id="808eb-192">INPUTOBJECT: <IConnectedMachineIdentity> Parâmetro de Identidade</span><span class="sxs-lookup"><span data-stu-id="808eb-192">INPUTOBJECT <IConnectedMachineIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="808eb-193">`[ExtensionName <String>]`: o nome da extensão do computador.</span><span class="sxs-lookup"><span data-stu-id="808eb-193">`[ExtensionName <String>]`: The name of the machine extension.</span></span>
  - <span data-ttu-id="808eb-194">`[Id <String>]`: Caminho de identidade de recursos</span><span class="sxs-lookup"><span data-stu-id="808eb-194">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="808eb-195">`[Name <String>]`: o nome da máquina híbrida.</span><span class="sxs-lookup"><span data-stu-id="808eb-195">`[Name <String>]`: The name of the hybrid machine.</span></span>
  - <span data-ttu-id="808eb-196">`[ResourceGroupName <String>]`: o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="808eb-196">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="808eb-197">`[SubscriptionId <String>]`: Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="808eb-197">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="808eb-198">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="808eb-198">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="808eb-199">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="808eb-199">RELATED LINKS</span></span>


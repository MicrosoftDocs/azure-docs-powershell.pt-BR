---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/powershell/module/az.connectedmachine/new-azconnectedmachineextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/New-AzConnectedMachineExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/New-AzConnectedMachineExtension.md
ms.openlocfilehash: df2e1de102143f227178b45ea14264f9e61d86a5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101893201"
---
# <span data-ttu-id="8f401-101">New-AzConnectedMachineExtension</span><span class="sxs-lookup"><span data-stu-id="8f401-101">New-AzConnectedMachineExtension</span></span>

## <span data-ttu-id="8f401-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8f401-102">SYNOPSIS</span></span>
<span data-ttu-id="8f401-103">A operação para criar ou atualizar a extensão.</span><span class="sxs-lookup"><span data-stu-id="8f401-103">The operation to create or update the extension.</span></span>

## <span data-ttu-id="8f401-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="8f401-104">SYNTAX</span></span>

### <span data-ttu-id="8f401-105">CreateExpanded (Default)</span><span class="sxs-lookup"><span data-stu-id="8f401-105">CreateExpanded (Default)</span></span>
```
New-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 -Location <String> [-SubscriptionId <String>] [-AutoUpgradeMinorVersion] [-ExtensionType <String>]
 [-ForceRerun <String>] [-ProtectedSetting <IMachineExtensionPropertiesProtectedSettings>]
 [-Publisher <String>] [-Setting <IMachineExtensionPropertiesSettings>] [-Tag <Hashtable>]
 [-TypeHandlerVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="8f401-106">Criar</span><span class="sxs-lookup"><span data-stu-id="8f401-106">Create</span></span>
```
New-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 -ExtensionParameter <IMachineExtension> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="8f401-107">CreateViaIdentity</span><span class="sxs-lookup"><span data-stu-id="8f401-107">CreateViaIdentity</span></span>
```
New-AzConnectedMachineExtension -InputObject <IConnectedMachineIdentity>
 -ExtensionParameter <IMachineExtension> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="8f401-108">CreateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="8f401-108">CreateViaIdentityExpanded</span></span>
```
New-AzConnectedMachineExtension -InputObject <IConnectedMachineIdentity> -Location <String>
 [-AutoUpgradeMinorVersion] [-ExtensionType <String>] [-ForceRerun <String>]
 [-ProtectedSetting <IMachineExtensionPropertiesProtectedSettings>] [-Publisher <String>]
 [-Setting <IMachineExtensionPropertiesSettings>] [-Tag <Hashtable>] [-TypeHandlerVersion <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="8f401-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="8f401-109">DESCRIPTION</span></span>
<span data-ttu-id="8f401-110">A operação para criar ou atualizar a extensão.</span><span class="sxs-lookup"><span data-stu-id="8f401-110">The operation to create or update the extension.</span></span>

## <span data-ttu-id="8f401-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8f401-111">EXAMPLES</span></span>

### <span data-ttu-id="8f401-112">Exemplo 1: Adicionar uma nova extensão a um computador</span><span class="sxs-lookup"><span data-stu-id="8f401-112">Example 1: Add a new extension to a machine</span></span>
```powershell
PS C:\> $Settings = @{ "commandToExecute" = "powershell.exe -c Get-Process" }
PS C:\> New-AzConnectedMachineExtension -Name custom -ResourceGroupName ContosoTest -MachineName win-eastus1 -Location eastus -Publisher "Microsoft.Compute" -TypeHandlerVersion 1.10 -Settings $Settings -ExtensionType CustomScriptExtension

Name   Location ProvisioningState
----   -------- -----------------
custom eastus   Succeeded
```

<span data-ttu-id="8f401-113">Define uma extensão em um computador.</span><span class="sxs-lookup"><span data-stu-id="8f401-113">Sets an extension on a machine.</span></span>

### <span data-ttu-id="8f401-114">Exemplo 2: Adicionar uma nova extensão com parâmetros de extensão especificados por meio do pipeline</span><span class="sxs-lookup"><span data-stu-id="8f401-114">Example 2: Add a new extension with extension parameters specified via the pipeline</span></span>
```powershell
PS C:\> $otherExtension = Get-AzConnectedMachineExtension -Name custom -ResourceGroupName ContosoTest -MachineName other
PS C:\> $otherExtension | New-AzConnectedMachineExtension -Name custom -ResourceGroupName ContosoTest -MachineName important

Name   Location ProvisioningState
----   -------- -----------------
custom eastus   Succeeded
```

<span data-ttu-id="8f401-115">Isso cria uma nova extensão com os parâmetros de extensão fornecidos pelo objeto passado por meio do pipeline.</span><span class="sxs-lookup"><span data-stu-id="8f401-115">This creates a new extension with the extension parameters provided by the object passed in via the pipeline.</span></span>
<span data-ttu-id="8f401-116">Isso é ótimo se você quiser pegar os parâmetros de uma máquina e aplicá-los a outro computador.</span><span class="sxs-lookup"><span data-stu-id="8f401-116">This is great if you want to grab the parameters of one machine and apply it to another machine.</span></span>

### <span data-ttu-id="8f401-117">Exemplo 3: Adicionar uma nova extensão com o local especificado por meio do pipeline</span><span class="sxs-lookup"><span data-stu-id="8f401-117">Example 3: Add a new extension with location specified via the pipeline</span></span>
```powershell
PS C:\> $identity = [Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.ConnectedMachineIdentity]@{
    Id = "/subscriptions/$($SubscriptionId)/resourceGroups/$($ResourceGroupName)/providers/Microsoft.HybridCompute/machines/$MachineName/extensions/$ExtensionName"
}
PS C:\> $Settings = @{ "commandToExecute" = "powershell.exe -c Get-Process" }
PS C:\> $identity | New-AzConnectedMachineExtension -Location eastus -Publisher "Microsoft.Compute" -TypeHandlerVersion 1.10 -Settings $Settings -ExtensionType CustomScriptExtension

Name   Location ProvisioningState
----   -------- -----------------
custom eastus   Succeeded
```

<span data-ttu-id="8f401-118">Isso cria uma nova extensão de máquina usando a identidade fornecida por meio do pipeline.</span><span class="sxs-lookup"><span data-stu-id="8f401-118">This creates a new machine extension using the identity provided via the pipeline.</span></span>
<span data-ttu-id="8f401-119">Você provavelmente não fará isso, mas é possível.</span><span class="sxs-lookup"><span data-stu-id="8f401-119">You likely won't do this, but it's possible.</span></span>

### <span data-ttu-id="8f401-120">Exemplo 4: Adicionar uma nova extensão usando um objeto extension como o local e os parâmetros para atualização</span><span class="sxs-lookup"><span data-stu-id="8f401-120">Example 4: Add a new extension using an extension object as both the location and parameters for updating</span></span>
```powershell
PS C:\> $ext = Get-AzConnectedMachineExtension -Name custom -ResourceGroupName ContosoTest -MachineName other
PS C:\> $ext | New-AzConnectedMachineExtension -ExtensionParameter $ext
```

<span data-ttu-id="8f401-121">Isso cria uma nova extensão de máquina usando a identidade fornecida por meio do pipeline e os detalhes de extensão fornecidos pelo objeto de extensão passado.</span><span class="sxs-lookup"><span data-stu-id="8f401-121">This creates a new machine extension using the identity provided via the pipeline and the extension details provided by the passed in extension object.</span></span>
<span data-ttu-id="8f401-122">Você provavelmente não fará isso, mas é possível.</span><span class="sxs-lookup"><span data-stu-id="8f401-122">You likely won't do this, but it's possible.</span></span>

## <span data-ttu-id="8f401-123">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="8f401-123">PARAMETERS</span></span>

### <span data-ttu-id="8f401-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8f401-124">-AsJob</span></span>
<span data-ttu-id="8f401-125">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="8f401-125">Run the command as a job</span></span>

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

### <span data-ttu-id="8f401-126">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="8f401-126">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="8f401-127">Indica se a extensão deve usar uma versão secundária mais recente se uma estiver disponível no momento da implantação.</span><span class="sxs-lookup"><span data-stu-id="8f401-127">Indicates whether the extension should use a newer minor version if one is available at deployment time.</span></span>
<span data-ttu-id="8f401-128">No entanto, uma vez implantado, a extensão não atualizará versões secundárias, a menos que seja reimplantada, mesmo com essa propriedade definida como true.</span><span class="sxs-lookup"><span data-stu-id="8f401-128">Once deployed, however, the extension will not upgrade minor versions unless redeployed, even with this property set to true.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f401-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f401-129">-DefaultProfile</span></span>
<span data-ttu-id="8f401-130">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8f401-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8f401-131">-ExtensionParameter</span><span class="sxs-lookup"><span data-stu-id="8f401-131">-ExtensionParameter</span></span>
<span data-ttu-id="8f401-132">Descreve uma extensão de máquina.</span><span class="sxs-lookup"><span data-stu-id="8f401-132">Describes a Machine Extension.</span></span>
<span data-ttu-id="8f401-133">Para construir, consulte a seção NOTES para propriedades EXTENSIONPARAMETER e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="8f401-133">To construct, see NOTES section for EXTENSIONPARAMETER properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension
Parameter Sets: Create, CreateViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8f401-134">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="8f401-134">-ExtensionType</span></span>
<span data-ttu-id="8f401-135">Especifica o tipo da extensão; um exemplo é "CustomScriptExtension".</span><span class="sxs-lookup"><span data-stu-id="8f401-135">Specifies the type of the extension; an example is "CustomScriptExtension".</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f401-136">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="8f401-136">-ForceRerun</span></span>
<span data-ttu-id="8f401-137">Como o manipulador de extensão deve ser forçado a atualizar mesmo que a configuração da extensão não tenha sido alterada.</span><span class="sxs-lookup"><span data-stu-id="8f401-137">How the extension handler should be forced to update even if the extension configuration has not changed.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f401-138">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8f401-138">-InputObject</span></span>
<span data-ttu-id="8f401-139">Parâmetro Identity Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="8f401-139">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.IConnectedMachineIdentity
Parameter Sets: CreateViaIdentity, CreateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8f401-140">-Location</span><span class="sxs-lookup"><span data-stu-id="8f401-140">-Location</span></span>
<span data-ttu-id="8f401-141">A localização geográfica onde o recurso mora</span><span class="sxs-lookup"><span data-stu-id="8f401-141">The geo-location where the resource lives</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f401-142">-MachineName</span><span class="sxs-lookup"><span data-stu-id="8f401-142">-MachineName</span></span>
<span data-ttu-id="8f401-143">O nome do computador onde a extensão deve ser criada ou atualizada.</span><span class="sxs-lookup"><span data-stu-id="8f401-143">The name of the machine where the extension should be created or updated.</span></span>

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f401-144">-Name</span><span class="sxs-lookup"><span data-stu-id="8f401-144">-Name</span></span>
<span data-ttu-id="8f401-145">O nome da extensão do computador.</span><span class="sxs-lookup"><span data-stu-id="8f401-145">The name of the machine extension.</span></span>

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f401-146">-NoWait</span><span class="sxs-lookup"><span data-stu-id="8f401-146">-NoWait</span></span>
<span data-ttu-id="8f401-147">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="8f401-147">Run the command asynchronously</span></span>

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

### <span data-ttu-id="8f401-148">-ProtectedSetting</span><span class="sxs-lookup"><span data-stu-id="8f401-148">-ProtectedSetting</span></span>
<span data-ttu-id="8f401-149">A extensão pode conter protectedSettings ou protectedSettingsFromKeyVault ou nenhuma configuração protegida.</span><span class="sxs-lookup"><span data-stu-id="8f401-149">The extension can contain either protectedSettings or protectedSettingsFromKeyVault or no protected settings at all.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtensionPropertiesProtectedSettings
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases: ProtectedSettings

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f401-150">-Publisher</span><span class="sxs-lookup"><span data-stu-id="8f401-150">-Publisher</span></span>
<span data-ttu-id="8f401-151">O nome do editor do manipulador de extensão.</span><span class="sxs-lookup"><span data-stu-id="8f401-151">The name of the extension handler publisher.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f401-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f401-152">-ResourceGroupName</span></span>
<span data-ttu-id="8f401-153">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="8f401-153">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f401-154">-Setting</span><span class="sxs-lookup"><span data-stu-id="8f401-154">-Setting</span></span>
<span data-ttu-id="8f401-155">Configurações públicas formatadas Json para a extensão.</span><span class="sxs-lookup"><span data-stu-id="8f401-155">Json formatted public settings for the extension.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtensionPropertiesSettings
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases: Settings

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f401-156">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8f401-156">-SubscriptionId</span></span>
<span data-ttu-id="8f401-157">Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="8f401-157">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="8f401-158">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="8f401-158">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f401-159">-Tag</span><span class="sxs-lookup"><span data-stu-id="8f401-159">-Tag</span></span>
<span data-ttu-id="8f401-160">Marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="8f401-160">Resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f401-161">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="8f401-161">-TypeHandlerVersion</span></span>
<span data-ttu-id="8f401-162">Especifica a versão do manipulador de scripts.</span><span class="sxs-lookup"><span data-stu-id="8f401-162">Specifies the version of the script handler.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f401-163">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8f401-163">-Confirm</span></span>
<span data-ttu-id="8f401-164">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8f401-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8f401-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f401-165">-WhatIf</span></span>
<span data-ttu-id="8f401-166">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8f401-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8f401-167">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8f401-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8f401-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f401-168">CommonParameters</span></span>
<span data-ttu-id="8f401-169">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f401-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f401-170">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8f401-170">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f401-171">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8f401-171">INPUTS</span></span>

### <span data-ttu-id="8f401-172">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span><span class="sxs-lookup"><span data-stu-id="8f401-172">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span></span>

### <span data-ttu-id="8f401-173">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.IConnectedMachineIdentity</span><span class="sxs-lookup"><span data-stu-id="8f401-173">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.IConnectedMachineIdentity</span></span>

## <span data-ttu-id="8f401-174">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="8f401-174">OUTPUTS</span></span>

### <span data-ttu-id="8f401-175">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span><span class="sxs-lookup"><span data-stu-id="8f401-175">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span></span>

## <span data-ttu-id="8f401-176">NOTES</span><span class="sxs-lookup"><span data-stu-id="8f401-176">NOTES</span></span>

<span data-ttu-id="8f401-177">ALIASES</span><span class="sxs-lookup"><span data-stu-id="8f401-177">ALIASES</span></span>

<span data-ttu-id="8f401-178">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="8f401-178">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="8f401-179">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="8f401-179">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8f401-180">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="8f401-180">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="8f401-181">EXTENSIONPARAMETER <IMachineExtension> : descreve uma extensão de máquina.</span><span class="sxs-lookup"><span data-stu-id="8f401-181">EXTENSIONPARAMETER <IMachineExtension>: Describes a Machine Extension.</span></span>
  - <span data-ttu-id="8f401-182">`Location <String>`: A localização geográfica onde o recurso mora</span><span class="sxs-lookup"><span data-stu-id="8f401-182">`Location <String>`: The geo-location where the resource lives</span></span>
  - <span data-ttu-id="8f401-183">`[Tag <ITrackedResourceTags>]`: Marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="8f401-183">`[Tag <ITrackedResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="8f401-184">`[(Any) <String>]`: Isso indica que qualquer propriedade pode ser adicionada a esse objeto.</span><span class="sxs-lookup"><span data-stu-id="8f401-184">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="8f401-185">`[AutoUpgradeMinorVersion <Boolean?>]`: Indica se a extensão deve usar uma versão secundária mais recente se uma estiver disponível no momento da implantação.</span><span class="sxs-lookup"><span data-stu-id="8f401-185">`[AutoUpgradeMinorVersion <Boolean?>]`: Indicates whether the extension should use a newer minor version if one is available at deployment time.</span></span> <span data-ttu-id="8f401-186">No entanto, uma vez implantado, a extensão não atualizará versões secundárias, a menos que seja reimplantada, mesmo com essa propriedade definida como true.</span><span class="sxs-lookup"><span data-stu-id="8f401-186">Once deployed, however, the extension will not upgrade minor versions unless redeployed, even with this property set to true.</span></span>
  - <span data-ttu-id="8f401-187">`[ForceUpdateTag <String>]`: Como o manipulador de extensão deve ser forçado a atualizar mesmo que a configuração da extensão não tenha sido alterada.</span><span class="sxs-lookup"><span data-stu-id="8f401-187">`[ForceUpdateTag <String>]`: How the extension handler should be forced to update even if the extension configuration has not changed.</span></span>
  - <span data-ttu-id="8f401-188">`[MachineExtensionType <String>]`: Especifica o tipo da extensão; um exemplo é "CustomScriptExtension".</span><span class="sxs-lookup"><span data-stu-id="8f401-188">`[MachineExtensionType <String>]`: Specifies the type of the extension; an example is "CustomScriptExtension".</span></span>
  - <span data-ttu-id="8f401-189">`[ProtectedSetting <IMachineExtensionPropertiesProtectedSettings>]`: A extensão pode conter protectedSettings ou protectedSettingsFromKeyVault ou nenhuma configuração protegida.</span><span class="sxs-lookup"><span data-stu-id="8f401-189">`[ProtectedSetting <IMachineExtensionPropertiesProtectedSettings>]`: The extension can contain either protectedSettings or protectedSettingsFromKeyVault or no protected settings at all.</span></span>
  - <span data-ttu-id="8f401-190">`[Publisher <String>]`: O nome do editor do manipulador de extensão.</span><span class="sxs-lookup"><span data-stu-id="8f401-190">`[Publisher <String>]`: The name of the extension handler publisher.</span></span>
  - <span data-ttu-id="8f401-191">`[Setting <IMachineExtensionPropertiesSettings>]`: Configurações públicas formatadas Json para a extensão.</span><span class="sxs-lookup"><span data-stu-id="8f401-191">`[Setting <IMachineExtensionPropertiesSettings>]`: Json formatted public settings for the extension.</span></span>
  - <span data-ttu-id="8f401-192">`[TypeHandlerVersion <String>]`: Especifica a versão do manipulador de scripts.</span><span class="sxs-lookup"><span data-stu-id="8f401-192">`[TypeHandlerVersion <String>]`: Specifies the version of the script handler.</span></span>

<span data-ttu-id="8f401-193">INPUTOBJECT <IConnectedMachineIdentity> : Parâmetro Identity</span><span class="sxs-lookup"><span data-stu-id="8f401-193">INPUTOBJECT <IConnectedMachineIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="8f401-194">`[ExtensionName <String>]`: O nome da extensão do computador.</span><span class="sxs-lookup"><span data-stu-id="8f401-194">`[ExtensionName <String>]`: The name of the machine extension.</span></span>
  - <span data-ttu-id="8f401-195">`[Id <String>]`: Caminho da identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="8f401-195">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="8f401-196">`[Name <String>]`: O nome da máquina híbrida.</span><span class="sxs-lookup"><span data-stu-id="8f401-196">`[Name <String>]`: The name of the hybrid machine.</span></span>
  - <span data-ttu-id="8f401-197">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="8f401-197">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="8f401-198">`[SubscriptionId <String>]`: Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="8f401-198">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="8f401-199">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="8f401-199">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="8f401-200">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8f401-200">RELATED LINKS</span></span>


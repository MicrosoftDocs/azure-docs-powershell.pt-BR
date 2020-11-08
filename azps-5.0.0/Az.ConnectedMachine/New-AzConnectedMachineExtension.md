---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedmachine/new-azconnectedmachineextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/New-AzConnectedMachineExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/New-AzConnectedMachineExtension.md
ms.openlocfilehash: 13095d24bd095e27bac788d0d578bdcdf3e1a0f7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94124681"
---
# <span data-ttu-id="6cfc9-101">New-AzConnectedMachineExtension</span><span class="sxs-lookup"><span data-stu-id="6cfc9-101">New-AzConnectedMachineExtension</span></span>

## <span data-ttu-id="6cfc9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6cfc9-102">SYNOPSIS</span></span>
<span data-ttu-id="6cfc9-103">A operação para criar ou atualizar a extensão.</span><span class="sxs-lookup"><span data-stu-id="6cfc9-103">The operation to create or update the extension.</span></span>

## <span data-ttu-id="6cfc9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6cfc9-104">SYNTAX</span></span>

### <span data-ttu-id="6cfc9-105">Createexpanded (padrão)</span><span class="sxs-lookup"><span data-stu-id="6cfc9-105">CreateExpanded (Default)</span></span>
```
New-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 -Location <String> [-SubscriptionId <String>] [-AutoUpgradeMinorVersion] [-ExtensionType <String>]
 [-ForceRerun <String>] [-ProtectedSetting <IMachineExtensionPropertiesProtectedSettings>]
 [-Publisher <String>] [-Setting <IMachineExtensionPropertiesSettings>] [-Tag <Hashtable>]
 [-TypeHandlerVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="6cfc9-106">Criados</span><span class="sxs-lookup"><span data-stu-id="6cfc9-106">Create</span></span>
```
New-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 -ExtensionParameter <IMachineExtension> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="6cfc9-107">CreateViaIdentity</span><span class="sxs-lookup"><span data-stu-id="6cfc9-107">CreateViaIdentity</span></span>
```
New-AzConnectedMachineExtension -InputObject <IConnectedMachineIdentity>
 -ExtensionParameter <IMachineExtension> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="6cfc9-108">CreateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="6cfc9-108">CreateViaIdentityExpanded</span></span>
```
New-AzConnectedMachineExtension -InputObject <IConnectedMachineIdentity> -Location <String>
 [-AutoUpgradeMinorVersion] [-ExtensionType <String>] [-ForceRerun <String>]
 [-ProtectedSetting <IMachineExtensionPropertiesProtectedSettings>] [-Publisher <String>]
 [-Setting <IMachineExtensionPropertiesSettings>] [-Tag <Hashtable>] [-TypeHandlerVersion <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="6cfc9-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6cfc9-109">DESCRIPTION</span></span>
<span data-ttu-id="6cfc9-110">A operação para criar ou atualizar a extensão.</span><span class="sxs-lookup"><span data-stu-id="6cfc9-110">The operation to create or update the extension.</span></span>

## <span data-ttu-id="6cfc9-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6cfc9-111">EXAMPLES</span></span>

### <span data-ttu-id="6cfc9-112">Exemplo 1: adicionar uma nova extensão a um computador</span><span class="sxs-lookup"><span data-stu-id="6cfc9-112">Example 1: Add a new extension to a machine</span></span>
```powershell
PS C:\> $Settings = @{ "commandToExecute" = "powershell.exe -c Get-Process" }
PS C:\> New-AzConnectedMachineExtension -Name custom -ResourceGroupName ContosoTest -MachineName win-eastus1 -Location eastus -Publisher "Microsoft.Compute" -TypeHandlerVersion 1.10 -Settings $Settings -ExtensionType CustomScriptExtension

Name   Location ProvisioningState
----   -------- -----------------
custom eastus   Succeeded
```

<span data-ttu-id="6cfc9-113">Define uma extensão em um computador.</span><span class="sxs-lookup"><span data-stu-id="6cfc9-113">Sets an extension on a machine.</span></span>

### <span data-ttu-id="6cfc9-114">Exemplo 2: adicionar uma nova extensão com parâmetros de extensão especificados via pipeline</span><span class="sxs-lookup"><span data-stu-id="6cfc9-114">Example 2: Add a new extension with extension parameters specified via the pipeline</span></span>
```powershell
PS C:\> $otherExtension = Get-AzConnectedMachineExtension -Name custom -ResourceGroupName ContosoTest -MachineName other
PS C:\> $otherExtension | New-AzConnectedMachineExtension -Name custom -ResourceGroupName ContosoTest -MachineName important

Name   Location ProvisioningState
----   -------- -----------------
custom eastus   Succeeded
```

<span data-ttu-id="6cfc9-115">Isso cria uma nova extensão com os parâmetros de extensão fornecidos pelo objeto passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="6cfc9-115">This creates a new extension with the extension parameters provided by the object passed in via the pipeline.</span></span>
<span data-ttu-id="6cfc9-116">Isso é ótimo se você quiser pegar os parâmetros de uma máquina e aplicá-la a outro computador.</span><span class="sxs-lookup"><span data-stu-id="6cfc9-116">This is great if you want to grab the parameters of one machine and apply it to another machine.</span></span>

### <span data-ttu-id="6cfc9-117">Exemplo 3: adicionar uma nova extensão com local especificado via pipeline</span><span class="sxs-lookup"><span data-stu-id="6cfc9-117">Example 3: Add a new extension with location specified via the pipeline</span></span>
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

<span data-ttu-id="6cfc9-118">Isso cria uma nova extensão de máquina usando a identidade fornecida pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="6cfc9-118">This creates a new machine extension using the identity provided via the pipeline.</span></span>
<span data-ttu-id="6cfc9-119">Você provavelmente não vai fazer isso, mas é possível.</span><span class="sxs-lookup"><span data-stu-id="6cfc9-119">You likely won't do this, but it's possible.</span></span>

### <span data-ttu-id="6cfc9-120">Exemplo 4: adicionar uma nova extensão usando um objeto de extensão como o local e os parâmetros para atualização</span><span class="sxs-lookup"><span data-stu-id="6cfc9-120">Example 4: Add a new extension using an extension object as both the location and parameters for updating</span></span>
```powershell
PS C:\> $ext = Get-AzConnectedMachineExtension -Name custom -ResourceGroupName ContosoTest -MachineName other
PS C:\> $ext | New-AzConnectedMachineExtension -ExtensionParameter $ext
```

<span data-ttu-id="6cfc9-121">Isso cria uma nova extensão de máquina usando a identidade fornecida pelo pipeline e os detalhes de extensão fornecidos pelo objeto de extensão passado.</span><span class="sxs-lookup"><span data-stu-id="6cfc9-121">This creates a new machine extension using the identity provided via the pipeline and the extension details provided by the passed in extension object.</span></span>
<span data-ttu-id="6cfc9-122">Você provavelmente não vai fazer isso, mas é possível.</span><span class="sxs-lookup"><span data-stu-id="6cfc9-122">You likely won't do this, but it's possible.</span></span>

## <span data-ttu-id="6cfc9-123">OS</span><span class="sxs-lookup"><span data-stu-id="6cfc9-123">PARAMETERS</span></span>

### <span data-ttu-id="6cfc9-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6cfc9-124">-AsJob</span></span>
<span data-ttu-id="6cfc9-125">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="6cfc9-125">Run the command as a job</span></span>

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

### <span data-ttu-id="6cfc9-126">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="6cfc9-126">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="6cfc9-127">Indica se a extensão deve usar uma versão secundária mais recente, se disponível no momento da implantação.</span><span class="sxs-lookup"><span data-stu-id="6cfc9-127">Indicates whether the extension should use a newer minor version if one is available at deployment time.</span></span>
<span data-ttu-id="6cfc9-128">Depois de implantada, no entanto, a extensão não atualizará versões secundárias, a menos que reimplantada, mesmo com essa propriedade definida como true.</span><span class="sxs-lookup"><span data-stu-id="6cfc9-128">Once deployed, however, the extension will not upgrade minor versions unless redeployed, even with this property set to true.</span></span>

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

### <span data-ttu-id="6cfc9-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6cfc9-129">-DefaultProfile</span></span>
<span data-ttu-id="6cfc9-130">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6cfc9-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6cfc9-131">-ExtensionParameter</span><span class="sxs-lookup"><span data-stu-id="6cfc9-131">-ExtensionParameter</span></span>
<span data-ttu-id="6cfc9-132">Descreve uma extensão de máquina.</span><span class="sxs-lookup"><span data-stu-id="6cfc9-132">Describes a Machine Extension.</span></span>
<span data-ttu-id="6cfc9-133">Para construir, consulte a seção notas para propriedades EXTENSIONPARAMETER e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="6cfc9-133">To construct, see NOTES section for EXTENSIONPARAMETER properties and create a hash table.</span></span>

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

### <span data-ttu-id="6cfc9-134">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="6cfc9-134">-ExtensionType</span></span>
<span data-ttu-id="6cfc9-135">Especifica o tipo da extensão; um exemplo é "CustomScriptExtension".</span><span class="sxs-lookup"><span data-stu-id="6cfc9-135">Specifies the type of the extension; an example is "CustomScriptExtension".</span></span>

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

### <span data-ttu-id="6cfc9-136">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="6cfc9-136">-ForceRerun</span></span>
<span data-ttu-id="6cfc9-137">Como o manipulador de extensão deve ser forçado a atualizar mesmo que a configuração de extensão não tenha sido alterada.</span><span class="sxs-lookup"><span data-stu-id="6cfc9-137">How the extension handler should be forced to update even if the extension configuration has not changed.</span></span>

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

### <span data-ttu-id="6cfc9-138">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6cfc9-138">-InputObject</span></span>
<span data-ttu-id="6cfc9-139">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="6cfc9-139">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="6cfc9-140">-Local</span><span class="sxs-lookup"><span data-stu-id="6cfc9-140">-Location</span></span>
<span data-ttu-id="6cfc9-141">A localização geográfica onde reside o recurso</span><span class="sxs-lookup"><span data-stu-id="6cfc9-141">The geo-location where the resource lives</span></span>

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

### <span data-ttu-id="6cfc9-142">-MachineName</span><span class="sxs-lookup"><span data-stu-id="6cfc9-142">-MachineName</span></span>
<span data-ttu-id="6cfc9-143">O nome da máquina na qual a extensão deve ser criada ou atualizada.</span><span class="sxs-lookup"><span data-stu-id="6cfc9-143">The name of the machine where the extension should be created or updated.</span></span>

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

### <span data-ttu-id="6cfc9-144">-Nome</span><span class="sxs-lookup"><span data-stu-id="6cfc9-144">-Name</span></span>
<span data-ttu-id="6cfc9-145">O nome da extensão da máquina.</span><span class="sxs-lookup"><span data-stu-id="6cfc9-145">The name of the machine extension.</span></span>

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

### <span data-ttu-id="6cfc9-146">-Nowait</span><span class="sxs-lookup"><span data-stu-id="6cfc9-146">-NoWait</span></span>
<span data-ttu-id="6cfc9-147">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="6cfc9-147">Run the command asynchronously</span></span>

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

### <span data-ttu-id="6cfc9-148">-ProtectedSetting</span><span class="sxs-lookup"><span data-stu-id="6cfc9-148">-ProtectedSetting</span></span>
<span data-ttu-id="6cfc9-149">A extensão pode conter o protectedSettings ou o protectedSettingsFromKeyVault ou nenhuma configuração protegida.</span><span class="sxs-lookup"><span data-stu-id="6cfc9-149">The extension can contain either protectedSettings or protectedSettingsFromKeyVault or no protected settings at all.</span></span>

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

### <span data-ttu-id="6cfc9-150">-Publisher</span><span class="sxs-lookup"><span data-stu-id="6cfc9-150">-Publisher</span></span>
<span data-ttu-id="6cfc9-151">O nome do fornecedor do manipulador de extensão.</span><span class="sxs-lookup"><span data-stu-id="6cfc9-151">The name of the extension handler publisher.</span></span>

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

### <span data-ttu-id="6cfc9-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6cfc9-152">-ResourceGroupName</span></span>
<span data-ttu-id="6cfc9-153">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="6cfc9-153">The name of the resource group.</span></span>

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

### <span data-ttu-id="6cfc9-154">-Configuração</span><span class="sxs-lookup"><span data-stu-id="6cfc9-154">-Setting</span></span>
<span data-ttu-id="6cfc9-155">Configurações públicas formatadas como JSON para a extensão.</span><span class="sxs-lookup"><span data-stu-id="6cfc9-155">Json formatted public settings for the extension.</span></span>

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

### <span data-ttu-id="6cfc9-156">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6cfc9-156">-SubscriptionId</span></span>
<span data-ttu-id="6cfc9-157">Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="6cfc9-157">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="6cfc9-158">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="6cfc9-158">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="6cfc9-159">-Marca</span><span class="sxs-lookup"><span data-stu-id="6cfc9-159">-Tag</span></span>
<span data-ttu-id="6cfc9-160">Marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="6cfc9-160">Resource tags.</span></span>

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

### <span data-ttu-id="6cfc9-161">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="6cfc9-161">-TypeHandlerVersion</span></span>
<span data-ttu-id="6cfc9-162">Especifica a versão do manipulador de script.</span><span class="sxs-lookup"><span data-stu-id="6cfc9-162">Specifies the version of the script handler.</span></span>

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

### <span data-ttu-id="6cfc9-163">-Confirme</span><span class="sxs-lookup"><span data-stu-id="6cfc9-163">-Confirm</span></span>
<span data-ttu-id="6cfc9-164">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6cfc9-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6cfc9-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6cfc9-165">-WhatIf</span></span>
<span data-ttu-id="6cfc9-166">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6cfc9-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6cfc9-167">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6cfc9-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6cfc9-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6cfc9-168">CommonParameters</span></span>
<span data-ttu-id="6cfc9-169">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6cfc9-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6cfc9-170">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6cfc9-170">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6cfc9-171">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6cfc9-171">INPUTS</span></span>

### <span data-ttu-id="6cfc9-172">Microsoft. Azure. PowerShell. cmdlets. ConnectedMachine. Models. Api20200802. IMachineExtension</span><span class="sxs-lookup"><span data-stu-id="6cfc9-172">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span></span>

### <span data-ttu-id="6cfc9-173">Microsoft. Azure. PowerShell. cmdlets. ConnectedMachine. Models. IConnectedMachineIdentity</span><span class="sxs-lookup"><span data-stu-id="6cfc9-173">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.IConnectedMachineIdentity</span></span>

## <span data-ttu-id="6cfc9-174">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6cfc9-174">OUTPUTS</span></span>

### <span data-ttu-id="6cfc9-175">Microsoft. Azure. PowerShell. cmdlets. ConnectedMachine. Models. Api20200802. IMachineExtension</span><span class="sxs-lookup"><span data-stu-id="6cfc9-175">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span></span>

## <span data-ttu-id="6cfc9-176">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6cfc9-176">NOTES</span></span>

<span data-ttu-id="6cfc9-177">ALIASES</span><span class="sxs-lookup"><span data-stu-id="6cfc9-177">ALIASES</span></span>

<span data-ttu-id="6cfc9-178">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="6cfc9-178">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="6cfc9-179">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="6cfc9-179">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6cfc9-180">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="6cfc9-180">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="6cfc9-181">EXTENSIONPARAMETER <IMachineExtension> : descreve uma extensão de máquina.</span><span class="sxs-lookup"><span data-stu-id="6cfc9-181">EXTENSIONPARAMETER <IMachineExtension>: Describes a Machine Extension.</span></span>
  - <span data-ttu-id="6cfc9-182">`Location <String>`: A localização geográfica onde reside o recurso</span><span class="sxs-lookup"><span data-stu-id="6cfc9-182">`Location <String>`: The geo-location where the resource lives</span></span>
  - <span data-ttu-id="6cfc9-183">`[Tag <ITrackedResourceTags>]`: Marcas do recurso.</span><span class="sxs-lookup"><span data-stu-id="6cfc9-183">`[Tag <ITrackedResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="6cfc9-184">`[(Any) <String>]`: Isso indica que qualquer propriedade pode ser adicionada a esse objeto.</span><span class="sxs-lookup"><span data-stu-id="6cfc9-184">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="6cfc9-185">`[AutoUpgradeMinorVersion <Boolean?>]`: Indica se a extensão deve usar uma versão secundária mais recente, se disponível no momento da implantação.</span><span class="sxs-lookup"><span data-stu-id="6cfc9-185">`[AutoUpgradeMinorVersion <Boolean?>]`: Indicates whether the extension should use a newer minor version if one is available at deployment time.</span></span> <span data-ttu-id="6cfc9-186">Depois de implantada, no entanto, a extensão não atualizará versões secundárias, a menos que reimplantada, mesmo com essa propriedade definida como true.</span><span class="sxs-lookup"><span data-stu-id="6cfc9-186">Once deployed, however, the extension will not upgrade minor versions unless redeployed, even with this property set to true.</span></span>
  - <span data-ttu-id="6cfc9-187">`[ForceUpdateTag <String>]`: Como o manipulador de extensão deve ser forçado a atualizar mesmo que a configuração de extensão não tenha sido alterada.</span><span class="sxs-lookup"><span data-stu-id="6cfc9-187">`[ForceUpdateTag <String>]`: How the extension handler should be forced to update even if the extension configuration has not changed.</span></span>
  - <span data-ttu-id="6cfc9-188">`[MachineExtensionType <String>]`: Especifica o tipo da extensão; um exemplo é "CustomScriptExtension".</span><span class="sxs-lookup"><span data-stu-id="6cfc9-188">`[MachineExtensionType <String>]`: Specifies the type of the extension; an example is "CustomScriptExtension".</span></span>
  - <span data-ttu-id="6cfc9-189">`[ProtectedSetting <IMachineExtensionPropertiesProtectedSettings>]`: A extensão pode conter o protectedSettings ou o protectedSettingsFromKeyVault ou nenhuma configuração protegida.</span><span class="sxs-lookup"><span data-stu-id="6cfc9-189">`[ProtectedSetting <IMachineExtensionPropertiesProtectedSettings>]`: The extension can contain either protectedSettings or protectedSettingsFromKeyVault or no protected settings at all.</span></span>
  - <span data-ttu-id="6cfc9-190">`[Publisher <String>]`: O nome do fornecedor do manipulador de extensão.</span><span class="sxs-lookup"><span data-stu-id="6cfc9-190">`[Publisher <String>]`: The name of the extension handler publisher.</span></span>
  - <span data-ttu-id="6cfc9-191">`[Setting <IMachineExtensionPropertiesSettings>]`: Configurações públicas formatadas por JSON para a extensão.</span><span class="sxs-lookup"><span data-stu-id="6cfc9-191">`[Setting <IMachineExtensionPropertiesSettings>]`: Json formatted public settings for the extension.</span></span>
  - <span data-ttu-id="6cfc9-192">`[TypeHandlerVersion <String>]`: Especifica a versão do manipulador de script.</span><span class="sxs-lookup"><span data-stu-id="6cfc9-192">`[TypeHandlerVersion <String>]`: Specifies the version of the script handler.</span></span>

<span data-ttu-id="6cfc9-193">INPUTobject <IConnectedMachineIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="6cfc9-193">INPUTOBJECT <IConnectedMachineIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="6cfc9-194">`[ExtensionName <String>]`: O nome da extensão da máquina.</span><span class="sxs-lookup"><span data-stu-id="6cfc9-194">`[ExtensionName <String>]`: The name of the machine extension.</span></span>
  - <span data-ttu-id="6cfc9-195">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="6cfc9-195">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="6cfc9-196">`[Name <String>]`: O nome da máquina híbrida.</span><span class="sxs-lookup"><span data-stu-id="6cfc9-196">`[Name <String>]`: The name of the hybrid machine.</span></span>
  - <span data-ttu-id="6cfc9-197">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="6cfc9-197">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="6cfc9-198">`[SubscriptionId <String>]`: Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="6cfc9-198">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="6cfc9-199">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="6cfc9-199">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="6cfc9-200">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6cfc9-200">RELATED LINKS</span></span>


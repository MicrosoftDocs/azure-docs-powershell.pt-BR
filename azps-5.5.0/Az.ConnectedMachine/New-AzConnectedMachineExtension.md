---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedmachine/new-azconnectedmachineextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/New-AzConnectedMachineExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/New-AzConnectedMachineExtension.md
ms.openlocfilehash: 13095d24bd095e27bac788d0d578bdcdf3e1a0f7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100127061"
---
# <span data-ttu-id="9f212-101">New-AzConnectedMachineExtension</span><span class="sxs-lookup"><span data-stu-id="9f212-101">New-AzConnectedMachineExtension</span></span>

## <span data-ttu-id="9f212-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9f212-102">SYNOPSIS</span></span>
<span data-ttu-id="9f212-103">A operação para criar ou atualizar a extensão.</span><span class="sxs-lookup"><span data-stu-id="9f212-103">The operation to create or update the extension.</span></span>

## <span data-ttu-id="9f212-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9f212-104">SYNTAX</span></span>

### <span data-ttu-id="9f212-105">CreateExpanded (Default)</span><span class="sxs-lookup"><span data-stu-id="9f212-105">CreateExpanded (Default)</span></span>
```
New-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 -Location <String> [-SubscriptionId <String>] [-AutoUpgradeMinorVersion] [-ExtensionType <String>]
 [-ForceRerun <String>] [-ProtectedSetting <IMachineExtensionPropertiesProtectedSettings>]
 [-Publisher <String>] [-Setting <IMachineExtensionPropertiesSettings>] [-Tag <Hashtable>]
 [-TypeHandlerVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="9f212-106">Criar</span><span class="sxs-lookup"><span data-stu-id="9f212-106">Create</span></span>
```
New-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 -ExtensionParameter <IMachineExtension> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="9f212-107">CreateViaIdentity</span><span class="sxs-lookup"><span data-stu-id="9f212-107">CreateViaIdentity</span></span>
```
New-AzConnectedMachineExtension -InputObject <IConnectedMachineIdentity>
 -ExtensionParameter <IMachineExtension> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="9f212-108">CreateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="9f212-108">CreateViaIdentityExpanded</span></span>
```
New-AzConnectedMachineExtension -InputObject <IConnectedMachineIdentity> -Location <String>
 [-AutoUpgradeMinorVersion] [-ExtensionType <String>] [-ForceRerun <String>]
 [-ProtectedSetting <IMachineExtensionPropertiesProtectedSettings>] [-Publisher <String>]
 [-Setting <IMachineExtensionPropertiesSettings>] [-Tag <Hashtable>] [-TypeHandlerVersion <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="9f212-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="9f212-109">DESCRIPTION</span></span>
<span data-ttu-id="9f212-110">A operação para criar ou atualizar a extensão.</span><span class="sxs-lookup"><span data-stu-id="9f212-110">The operation to create or update the extension.</span></span>

## <span data-ttu-id="9f212-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="9f212-111">EXAMPLES</span></span>

### <span data-ttu-id="9f212-112">Exemplo 1: Adicionar uma nova extensão a um computador</span><span class="sxs-lookup"><span data-stu-id="9f212-112">Example 1: Add a new extension to a machine</span></span>
```powershell
PS C:\> $Settings = @{ "commandToExecute" = "powershell.exe -c Get-Process" }
PS C:\> New-AzConnectedMachineExtension -Name custom -ResourceGroupName ContosoTest -MachineName win-eastus1 -Location eastus -Publisher "Microsoft.Compute" -TypeHandlerVersion 1.10 -Settings $Settings -ExtensionType CustomScriptExtension

Name   Location ProvisioningState
----   -------- -----------------
custom eastus   Succeeded
```

<span data-ttu-id="9f212-113">Define uma extensão em uma máquina.</span><span class="sxs-lookup"><span data-stu-id="9f212-113">Sets an extension on a machine.</span></span>

### <span data-ttu-id="9f212-114">Exemplo 2: Adicionar uma nova extensão com parâmetros de extensão especificados por meio do pipeline</span><span class="sxs-lookup"><span data-stu-id="9f212-114">Example 2: Add a new extension with extension parameters specified via the pipeline</span></span>
```powershell
PS C:\> $otherExtension = Get-AzConnectedMachineExtension -Name custom -ResourceGroupName ContosoTest -MachineName other
PS C:\> $otherExtension | New-AzConnectedMachineExtension -Name custom -ResourceGroupName ContosoTest -MachineName important

Name   Location ProvisioningState
----   -------- -----------------
custom eastus   Succeeded
```

<span data-ttu-id="9f212-115">Isso cria uma nova extensão com os parâmetros de extensão fornecidos pelo objeto passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="9f212-115">This creates a new extension with the extension parameters provided by the object passed in via the pipeline.</span></span>
<span data-ttu-id="9f212-116">Isso é ótimo se você quiser pegar os parâmetros de uma máquina e aplicá-los a outro computador.</span><span class="sxs-lookup"><span data-stu-id="9f212-116">This is great if you want to grab the parameters of one machine and apply it to another machine.</span></span>

### <span data-ttu-id="9f212-117">Exemplo 3: Adicionar uma nova extensão com a localização especificada por meio do pipeline</span><span class="sxs-lookup"><span data-stu-id="9f212-117">Example 3: Add a new extension with location specified via the pipeline</span></span>
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

<span data-ttu-id="9f212-118">Isso cria uma nova extensão de máquina usando a identidade fornecida por meio do pipeline.</span><span class="sxs-lookup"><span data-stu-id="9f212-118">This creates a new machine extension using the identity provided via the pipeline.</span></span>
<span data-ttu-id="9f212-119">Você provavelmente não fará isso, mas é possível.</span><span class="sxs-lookup"><span data-stu-id="9f212-119">You likely won't do this, but it's possible.</span></span>

### <span data-ttu-id="9f212-120">Exemplo 4: Adicionar uma nova extensão usando um objeto de extensão como o local e os parâmetros para atualizar</span><span class="sxs-lookup"><span data-stu-id="9f212-120">Example 4: Add a new extension using an extension object as both the location and parameters for updating</span></span>
```powershell
PS C:\> $ext = Get-AzConnectedMachineExtension -Name custom -ResourceGroupName ContosoTest -MachineName other
PS C:\> $ext | New-AzConnectedMachineExtension -ExtensionParameter $ext
```

<span data-ttu-id="9f212-121">Isso cria uma nova extensão de máquina usando a identidade fornecida por meio do pipeline e os detalhes de extensão fornecidos pelo objeto de extensão passado.</span><span class="sxs-lookup"><span data-stu-id="9f212-121">This creates a new machine extension using the identity provided via the pipeline and the extension details provided by the passed in extension object.</span></span>
<span data-ttu-id="9f212-122">Você provavelmente não fará isso, mas é possível.</span><span class="sxs-lookup"><span data-stu-id="9f212-122">You likely won't do this, but it's possible.</span></span>

## <span data-ttu-id="9f212-123">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9f212-123">PARAMETERS</span></span>

### <span data-ttu-id="9f212-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9f212-124">-AsJob</span></span>
<span data-ttu-id="9f212-125">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="9f212-125">Run the command as a job</span></span>

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

### <span data-ttu-id="9f212-126">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="9f212-126">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="9f212-127">Indica se a extensão deve usar uma versão secundária mais recente, se estiver disponível no momento da implantação.</span><span class="sxs-lookup"><span data-stu-id="9f212-127">Indicates whether the extension should use a newer minor version if one is available at deployment time.</span></span>
<span data-ttu-id="9f212-128">Uma vez implantada, no entanto, a extensão não atualizará as versões secundárias, a menos que seja reimplantada, mesmo com essa propriedade definida como verdadeira.</span><span class="sxs-lookup"><span data-stu-id="9f212-128">Once deployed, however, the extension will not upgrade minor versions unless redeployed, even with this property set to true.</span></span>

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

### <span data-ttu-id="9f212-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f212-129">-DefaultProfile</span></span>
<span data-ttu-id="9f212-130">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9f212-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9f212-131">-ExtensionParameter</span><span class="sxs-lookup"><span data-stu-id="9f212-131">-ExtensionParameter</span></span>
<span data-ttu-id="9f212-132">Descreve uma Extensão de Máquina.</span><span class="sxs-lookup"><span data-stu-id="9f212-132">Describes a Machine Extension.</span></span>
<span data-ttu-id="9f212-133">Para construir, confira a seção ANOTAÇÕES para propriedades EXTENSIONPARAMETER e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="9f212-133">To construct, see NOTES section for EXTENSIONPARAMETER properties and create a hash table.</span></span>

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

### <span data-ttu-id="9f212-134">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="9f212-134">-ExtensionType</span></span>
<span data-ttu-id="9f212-135">Especifica o tipo da extensão; um exemplo é "CustomScriptExtension".</span><span class="sxs-lookup"><span data-stu-id="9f212-135">Specifies the type of the extension; an example is "CustomScriptExtension".</span></span>

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

### <span data-ttu-id="9f212-136">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="9f212-136">-ForceRerun</span></span>
<span data-ttu-id="9f212-137">Como o manipulador de extensão deve ser obrigado a atualizar mesmo que a configuração de extensão não tenha sido alterada.</span><span class="sxs-lookup"><span data-stu-id="9f212-137">How the extension handler should be forced to update even if the extension configuration has not changed.</span></span>

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

### <span data-ttu-id="9f212-138">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9f212-138">-InputObject</span></span>
<span data-ttu-id="9f212-139">Parâmetro de Identidade para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="9f212-139">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="9f212-140">-Local</span><span class="sxs-lookup"><span data-stu-id="9f212-140">-Location</span></span>
<span data-ttu-id="9f212-141">A localização geográfica onde o recurso reside</span><span class="sxs-lookup"><span data-stu-id="9f212-141">The geo-location where the resource lives</span></span>

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

### <span data-ttu-id="9f212-142">-MachineName</span><span class="sxs-lookup"><span data-stu-id="9f212-142">-MachineName</span></span>
<span data-ttu-id="9f212-143">O nome do computador onde a extensão deve ser criada ou atualizada.</span><span class="sxs-lookup"><span data-stu-id="9f212-143">The name of the machine where the extension should be created or updated.</span></span>

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

### <span data-ttu-id="9f212-144">-Nome</span><span class="sxs-lookup"><span data-stu-id="9f212-144">-Name</span></span>
<span data-ttu-id="9f212-145">O nome da extensão do computador.</span><span class="sxs-lookup"><span data-stu-id="9f212-145">The name of the machine extension.</span></span>

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

### <span data-ttu-id="9f212-146">-NoWait</span><span class="sxs-lookup"><span data-stu-id="9f212-146">-NoWait</span></span>
<span data-ttu-id="9f212-147">Executar o comando assíncrona</span><span class="sxs-lookup"><span data-stu-id="9f212-147">Run the command asynchronously</span></span>

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

### <span data-ttu-id="9f212-148">-ProtectedSetting</span><span class="sxs-lookup"><span data-stu-id="9f212-148">-ProtectedSetting</span></span>
<span data-ttu-id="9f212-149">A extensão pode conterSettings protegidos ou protectedSettingsFromKeyVault ou nenhuma configuração protegida.</span><span class="sxs-lookup"><span data-stu-id="9f212-149">The extension can contain either protectedSettings or protectedSettingsFromKeyVault or no protected settings at all.</span></span>

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

### <span data-ttu-id="9f212-150">-Publisher</span><span class="sxs-lookup"><span data-stu-id="9f212-150">-Publisher</span></span>
<span data-ttu-id="9f212-151">O nome do editor do manipulador de extensão.</span><span class="sxs-lookup"><span data-stu-id="9f212-151">The name of the extension handler publisher.</span></span>

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

### <span data-ttu-id="9f212-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f212-152">-ResourceGroupName</span></span>
<span data-ttu-id="9f212-153">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="9f212-153">The name of the resource group.</span></span>

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

### <span data-ttu-id="9f212-154">-Configuração</span><span class="sxs-lookup"><span data-stu-id="9f212-154">-Setting</span></span>
<span data-ttu-id="9f212-155">Json formatado configurações públicas para a extensão.</span><span class="sxs-lookup"><span data-stu-id="9f212-155">Json formatted public settings for the extension.</span></span>

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

### <span data-ttu-id="9f212-156">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9f212-156">-SubscriptionId</span></span>
<span data-ttu-id="9f212-157">Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="9f212-157">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="9f212-158">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="9f212-158">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="9f212-159">-Tag</span><span class="sxs-lookup"><span data-stu-id="9f212-159">-Tag</span></span>
<span data-ttu-id="9f212-160">Marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="9f212-160">Resource tags.</span></span>

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

### <span data-ttu-id="9f212-161">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="9f212-161">-TypeHandlerVersion</span></span>
<span data-ttu-id="9f212-162">Especifica a versão do manipulador de script.</span><span class="sxs-lookup"><span data-stu-id="9f212-162">Specifies the version of the script handler.</span></span>

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

### <span data-ttu-id="9f212-163">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="9f212-163">-Confirm</span></span>
<span data-ttu-id="9f212-164">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9f212-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9f212-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9f212-165">-WhatIf</span></span>
<span data-ttu-id="9f212-166">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="9f212-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9f212-167">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9f212-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9f212-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f212-168">CommonParameters</span></span>
<span data-ttu-id="9f212-169">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f212-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f212-170">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9f212-170">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f212-171">Entradas</span><span class="sxs-lookup"><span data-stu-id="9f212-171">INPUTS</span></span>

### <span data-ttu-id="9f212-172">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span><span class="sxs-lookup"><span data-stu-id="9f212-172">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span></span>

### <span data-ttu-id="9f212-173">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.IConnectedMachineIdentity</span><span class="sxs-lookup"><span data-stu-id="9f212-173">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.IConnectedMachineIdentity</span></span>

## <span data-ttu-id="9f212-174">Saídas</span><span class="sxs-lookup"><span data-stu-id="9f212-174">OUTPUTS</span></span>

### <span data-ttu-id="9f212-175">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span><span class="sxs-lookup"><span data-stu-id="9f212-175">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span></span>

## <span data-ttu-id="9f212-176">Notas</span><span class="sxs-lookup"><span data-stu-id="9f212-176">NOTES</span></span>

<span data-ttu-id="9f212-177">Aliases</span><span class="sxs-lookup"><span data-stu-id="9f212-177">ALIASES</span></span>

<span data-ttu-id="9f212-178">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="9f212-178">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="9f212-179">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="9f212-179">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="9f212-180">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="9f212-180">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="9f212-181">EXTENSIONPARAMETER <IMachineExtension> : descreve uma Extensão de Máquina.</span><span class="sxs-lookup"><span data-stu-id="9f212-181">EXTENSIONPARAMETER <IMachineExtension>: Describes a Machine Extension.</span></span>
  - <span data-ttu-id="9f212-182">`Location <String>`: a localização geográfica onde o recurso reside</span><span class="sxs-lookup"><span data-stu-id="9f212-182">`Location <String>`: The geo-location where the resource lives</span></span>
  - <span data-ttu-id="9f212-183">`[Tag <ITrackedResourceTags>]`: Marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="9f212-183">`[Tag <ITrackedResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="9f212-184">`[(Any) <String>]`: indica que qualquer propriedade pode ser adicionada a este objeto.</span><span class="sxs-lookup"><span data-stu-id="9f212-184">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="9f212-185">`[AutoUpgradeMinorVersion <Boolean?>]`: indica se a extensão deve usar uma versão secundária mais recente, se estiver disponível no momento da implantação.</span><span class="sxs-lookup"><span data-stu-id="9f212-185">`[AutoUpgradeMinorVersion <Boolean?>]`: Indicates whether the extension should use a newer minor version if one is available at deployment time.</span></span> <span data-ttu-id="9f212-186">Uma vez implantada, no entanto, a extensão não atualizará as versões secundárias, a menos que seja reimplantada, mesmo com essa propriedade definida como verdadeira.</span><span class="sxs-lookup"><span data-stu-id="9f212-186">Once deployed, however, the extension will not upgrade minor versions unless redeployed, even with this property set to true.</span></span>
  - <span data-ttu-id="9f212-187">`[ForceUpdateTag <String>]`: como o manipulador de extensão deve ser obrigado a atualizar mesmo que a configuração de extensão não tenha sido alterada.</span><span class="sxs-lookup"><span data-stu-id="9f212-187">`[ForceUpdateTag <String>]`: How the extension handler should be forced to update even if the extension configuration has not changed.</span></span>
  - <span data-ttu-id="9f212-188">`[MachineExtensionType <String>]`: especifica o tipo da extensão; um exemplo é "CustomScriptExtension".</span><span class="sxs-lookup"><span data-stu-id="9f212-188">`[MachineExtensionType <String>]`: Specifies the type of the extension; an example is "CustomScriptExtension".</span></span>
  - <span data-ttu-id="9f212-189">`[ProtectedSetting <IMachineExtensionPropertiesProtectedSettings>]`: A extensão pode conterSettings protegidos ou protectedSettingsFromKeyVault ou nenhuma configuração protegida.</span><span class="sxs-lookup"><span data-stu-id="9f212-189">`[ProtectedSetting <IMachineExtensionPropertiesProtectedSettings>]`: The extension can contain either protectedSettings or protectedSettingsFromKeyVault or no protected settings at all.</span></span>
  - <span data-ttu-id="9f212-190">`[Publisher <String>]`: o nome do editor do manipulador de extensão.</span><span class="sxs-lookup"><span data-stu-id="9f212-190">`[Publisher <String>]`: The name of the extension handler publisher.</span></span>
  - <span data-ttu-id="9f212-191">`[Setting <IMachineExtensionPropertiesSettings>]`: Json formatou as configurações públicas para a extensão.</span><span class="sxs-lookup"><span data-stu-id="9f212-191">`[Setting <IMachineExtensionPropertiesSettings>]`: Json formatted public settings for the extension.</span></span>
  - <span data-ttu-id="9f212-192">`[TypeHandlerVersion <String>]`: especifica a versão do manipulador de script.</span><span class="sxs-lookup"><span data-stu-id="9f212-192">`[TypeHandlerVersion <String>]`: Specifies the version of the script handler.</span></span>

<span data-ttu-id="9f212-193">INPUTOBJECT: <IConnectedMachineIdentity> Parâmetro de Identidade</span><span class="sxs-lookup"><span data-stu-id="9f212-193">INPUTOBJECT <IConnectedMachineIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="9f212-194">`[ExtensionName <String>]`: o nome da extensão do computador.</span><span class="sxs-lookup"><span data-stu-id="9f212-194">`[ExtensionName <String>]`: The name of the machine extension.</span></span>
  - <span data-ttu-id="9f212-195">`[Id <String>]`: Caminho de identidade de recursos</span><span class="sxs-lookup"><span data-stu-id="9f212-195">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="9f212-196">`[Name <String>]`: o nome da máquina híbrida.</span><span class="sxs-lookup"><span data-stu-id="9f212-196">`[Name <String>]`: The name of the hybrid machine.</span></span>
  - <span data-ttu-id="9f212-197">`[ResourceGroupName <String>]`: o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="9f212-197">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="9f212-198">`[SubscriptionId <String>]`: Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="9f212-198">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="9f212-199">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="9f212-199">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="9f212-200">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9f212-200">RELATED LINKS</span></span>


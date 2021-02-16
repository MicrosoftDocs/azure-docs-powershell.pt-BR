---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedmachine/set-azconnectedmachineextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Set-AzConnectedMachineExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Set-AzConnectedMachineExtension.md
ms.openlocfilehash: b136f5194bdc7e0f4b4dfc969564d7ef8476d9bf
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100127057"
---
# <span data-ttu-id="85c83-101">Set-AzConnectedMachineExtension</span><span class="sxs-lookup"><span data-stu-id="85c83-101">Set-AzConnectedMachineExtension</span></span>

## <span data-ttu-id="85c83-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="85c83-102">SYNOPSIS</span></span>
<span data-ttu-id="85c83-103">A operação para criar ou atualizar a extensão.</span><span class="sxs-lookup"><span data-stu-id="85c83-103">The operation to create or update the extension.</span></span>

## <span data-ttu-id="85c83-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="85c83-104">SYNTAX</span></span>

### <span data-ttu-id="85c83-105">UpdateExpanded (Padrão)</span><span class="sxs-lookup"><span data-stu-id="85c83-105">UpdateExpanded (Default)</span></span>
```
Set-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 -Location <String> [-SubscriptionId <String>] [-AutoUpgradeMinorVersion] [-ExtensionType <String>]
 [-ForceRerun <String>] [-ProtectedSetting <IMachineExtensionPropertiesProtectedSettings>]
 [-Publisher <String>] [-Setting <IMachineExtensionPropertiesSettings>] [-Tag <Hashtable>]
 [-TypeHandlerVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="85c83-106">Atualização</span><span class="sxs-lookup"><span data-stu-id="85c83-106">Update</span></span>
```
Set-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 -ExtensionParameter <IMachineExtension> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="85c83-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="85c83-107">DESCRIPTION</span></span>
<span data-ttu-id="85c83-108">A operação para criar ou atualizar a extensão.</span><span class="sxs-lookup"><span data-stu-id="85c83-108">The operation to create or update the extension.</span></span>

## <span data-ttu-id="85c83-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="85c83-109">EXAMPLES</span></span>

### <span data-ttu-id="85c83-110">Exemplo 1: Definir uma extensão em um computador</span><span class="sxs-lookup"><span data-stu-id="85c83-110">Example 1: Set an extension on a machine</span></span>
```powershell
PS C:\> $Settings = @{ "commandToExecute" = "powershell.exe -c Get-Process" }
PS C:\> Set-AzConnectedMachineExtension -Name custom -ResourceGroupName ContosoTest -MachineName win-eastus1 -Location eastus -Publisher "Microsoft.Compute" -TypeHandlerVersion 1.10 -Settings $Settings -ExtensionType CustomScriptExtension

Name   Location ProvisioningState
----   -------- -----------------
custom eastus   Succeeded
```

<span data-ttu-id="85c83-111">Define uma extensão em uma máquina.</span><span class="sxs-lookup"><span data-stu-id="85c83-111">Sets an extension on a machine.</span></span>

### <span data-ttu-id="85c83-112">Exemplo 2: Definir uma extensão com parâmetros de extensão especificados por meio do pipeline</span><span class="sxs-lookup"><span data-stu-id="85c83-112">Example 2: Set an extension with extension parameters specified via the pipeline</span></span>
```powershell
PS C:\> $otherExtension = Get-AzConnectedMachineExtension -Name custom -ResourceGroupName ContosoTest -MachineName other
PS C:\> $otherExtension | Set-AzConnectedMachineExtension -Name custom -ResourceGroupName ContosoTest -MachineName important

Name   Location ProvisioningState
----   -------- -----------------
custom eastus   Succeeded
```

<span data-ttu-id="85c83-113">Isso define uma extensão com os parâmetros de extensão fornecidos pelo objeto passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="85c83-113">This sets an extension with the extension parameters provided by the object passed in via the pipeline.</span></span>
<span data-ttu-id="85c83-114">Isso é ótimo se você quiser pegar os parâmetros de uma máquina e aplicá-los a outro computador.</span><span class="sxs-lookup"><span data-stu-id="85c83-114">This is great if you want to grab the parameters of one machine and apply it to another machine.</span></span>

## <span data-ttu-id="85c83-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="85c83-115">PARAMETERS</span></span>

### <span data-ttu-id="85c83-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="85c83-116">-AsJob</span></span>
<span data-ttu-id="85c83-117">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="85c83-117">Run the command as a job</span></span>

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

### <span data-ttu-id="85c83-118">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="85c83-118">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="85c83-119">Indica se a extensão deve usar uma versão secundária mais recente, se estiver disponível no momento da implantação.</span><span class="sxs-lookup"><span data-stu-id="85c83-119">Indicates whether the extension should use a newer minor version if one is available at deployment time.</span></span>
<span data-ttu-id="85c83-120">Uma vez implantada, no entanto, a extensão não atualizará as versões secundárias, a menos que seja reimplantada, mesmo com essa propriedade definida como verdadeira.</span><span class="sxs-lookup"><span data-stu-id="85c83-120">Once deployed, however, the extension will not upgrade minor versions unless redeployed, even with this property set to true.</span></span>

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

### <span data-ttu-id="85c83-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85c83-121">-DefaultProfile</span></span>
<span data-ttu-id="85c83-122">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="85c83-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="85c83-123">-ExtensionParameter</span><span class="sxs-lookup"><span data-stu-id="85c83-123">-ExtensionParameter</span></span>
<span data-ttu-id="85c83-124">Descreve uma Extensão de Máquina.</span><span class="sxs-lookup"><span data-stu-id="85c83-124">Describes a Machine Extension.</span></span>
<span data-ttu-id="85c83-125">Para construir, confira a seção ANOTAÇÕES para propriedades EXTENSIONPARAMETER e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="85c83-125">To construct, see NOTES section for EXTENSIONPARAMETER properties and create a hash table.</span></span>

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

### <span data-ttu-id="85c83-126">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="85c83-126">-ExtensionType</span></span>
<span data-ttu-id="85c83-127">Especifica o tipo da extensão; um exemplo é "CustomScriptExtension".</span><span class="sxs-lookup"><span data-stu-id="85c83-127">Specifies the type of the extension; an example is "CustomScriptExtension".</span></span>

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

### <span data-ttu-id="85c83-128">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="85c83-128">-ForceRerun</span></span>
<span data-ttu-id="85c83-129">Como o manipulador de extensão deve ser obrigado a atualizar mesmo que a configuração de extensão não tenha sido alterada.</span><span class="sxs-lookup"><span data-stu-id="85c83-129">How the extension handler should be forced to update even if the extension configuration has not changed.</span></span>

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

### <span data-ttu-id="85c83-130">-Local</span><span class="sxs-lookup"><span data-stu-id="85c83-130">-Location</span></span>
<span data-ttu-id="85c83-131">A localização geográfica onde o recurso reside</span><span class="sxs-lookup"><span data-stu-id="85c83-131">The geo-location where the resource lives</span></span>

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

### <span data-ttu-id="85c83-132">-MachineName</span><span class="sxs-lookup"><span data-stu-id="85c83-132">-MachineName</span></span>
<span data-ttu-id="85c83-133">O nome do computador onde a extensão deve ser criada ou atualizada.</span><span class="sxs-lookup"><span data-stu-id="85c83-133">The name of the machine where the extension should be created or updated.</span></span>

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

### <span data-ttu-id="85c83-134">-Nome</span><span class="sxs-lookup"><span data-stu-id="85c83-134">-Name</span></span>
<span data-ttu-id="85c83-135">O nome da extensão do computador.</span><span class="sxs-lookup"><span data-stu-id="85c83-135">The name of the machine extension.</span></span>

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

### <span data-ttu-id="85c83-136">-NoWait</span><span class="sxs-lookup"><span data-stu-id="85c83-136">-NoWait</span></span>
<span data-ttu-id="85c83-137">Executar o comando assíncrona</span><span class="sxs-lookup"><span data-stu-id="85c83-137">Run the command asynchronously</span></span>

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

### <span data-ttu-id="85c83-138">-ProtectedSetting</span><span class="sxs-lookup"><span data-stu-id="85c83-138">-ProtectedSetting</span></span>
<span data-ttu-id="85c83-139">A extensão pode conterSettings protegidos ou protectedSettingsFromKeyVault ou nenhuma configuração protegida.</span><span class="sxs-lookup"><span data-stu-id="85c83-139">The extension can contain either protectedSettings or protectedSettingsFromKeyVault or no protected settings at all.</span></span>

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

### <span data-ttu-id="85c83-140">-Publisher</span><span class="sxs-lookup"><span data-stu-id="85c83-140">-Publisher</span></span>
<span data-ttu-id="85c83-141">O nome do editor do manipulador de extensão.</span><span class="sxs-lookup"><span data-stu-id="85c83-141">The name of the extension handler publisher.</span></span>

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

### <span data-ttu-id="85c83-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="85c83-142">-ResourceGroupName</span></span>
<span data-ttu-id="85c83-143">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="85c83-143">The name of the resource group.</span></span>

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

### <span data-ttu-id="85c83-144">-Configuração</span><span class="sxs-lookup"><span data-stu-id="85c83-144">-Setting</span></span>
<span data-ttu-id="85c83-145">Json formatado configurações públicas para a extensão.</span><span class="sxs-lookup"><span data-stu-id="85c83-145">Json formatted public settings for the extension.</span></span>

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

### <span data-ttu-id="85c83-146">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="85c83-146">-SubscriptionId</span></span>
<span data-ttu-id="85c83-147">Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="85c83-147">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="85c83-148">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="85c83-148">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="85c83-149">-Tag</span><span class="sxs-lookup"><span data-stu-id="85c83-149">-Tag</span></span>
<span data-ttu-id="85c83-150">Marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="85c83-150">Resource tags.</span></span>

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

### <span data-ttu-id="85c83-151">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="85c83-151">-TypeHandlerVersion</span></span>
<span data-ttu-id="85c83-152">Especifica a versão do manipulador de script.</span><span class="sxs-lookup"><span data-stu-id="85c83-152">Specifies the version of the script handler.</span></span>

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

### <span data-ttu-id="85c83-153">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="85c83-153">-Confirm</span></span>
<span data-ttu-id="85c83-154">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="85c83-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="85c83-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="85c83-155">-WhatIf</span></span>
<span data-ttu-id="85c83-156">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="85c83-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="85c83-157">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="85c83-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="85c83-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85c83-158">CommonParameters</span></span>
<span data-ttu-id="85c83-159">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85c83-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85c83-160">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="85c83-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85c83-161">Entradas</span><span class="sxs-lookup"><span data-stu-id="85c83-161">INPUTS</span></span>

### <span data-ttu-id="85c83-162">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span><span class="sxs-lookup"><span data-stu-id="85c83-162">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span></span>

## <span data-ttu-id="85c83-163">Saídas</span><span class="sxs-lookup"><span data-stu-id="85c83-163">OUTPUTS</span></span>

### <span data-ttu-id="85c83-164">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span><span class="sxs-lookup"><span data-stu-id="85c83-164">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span></span>

## <span data-ttu-id="85c83-165">Notas</span><span class="sxs-lookup"><span data-stu-id="85c83-165">NOTES</span></span>

<span data-ttu-id="85c83-166">Aliases</span><span class="sxs-lookup"><span data-stu-id="85c83-166">ALIASES</span></span>

<span data-ttu-id="85c83-167">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="85c83-167">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="85c83-168">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="85c83-168">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="85c83-169">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="85c83-169">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="85c83-170">EXTENSIONPARAMETER <IMachineExtension> : descreve uma Extensão de Máquina.</span><span class="sxs-lookup"><span data-stu-id="85c83-170">EXTENSIONPARAMETER <IMachineExtension>: Describes a Machine Extension.</span></span>
  - <span data-ttu-id="85c83-171">`Location <String>`: a localização geográfica onde o recurso reside</span><span class="sxs-lookup"><span data-stu-id="85c83-171">`Location <String>`: The geo-location where the resource lives</span></span>
  - <span data-ttu-id="85c83-172">`[Tag <ITrackedResourceTags>]`: Marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="85c83-172">`[Tag <ITrackedResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="85c83-173">`[(Any) <String>]`: indica que qualquer propriedade pode ser adicionada a este objeto.</span><span class="sxs-lookup"><span data-stu-id="85c83-173">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="85c83-174">`[AutoUpgradeMinorVersion <Boolean?>]`: indica se a extensão deve usar uma versão secundária mais recente se estiver disponível no momento da implantação.</span><span class="sxs-lookup"><span data-stu-id="85c83-174">`[AutoUpgradeMinorVersion <Boolean?>]`: Indicates whether the extension should use a newer minor version if one is available at deployment time.</span></span> <span data-ttu-id="85c83-175">Uma vez implantada, no entanto, a extensão não atualizará as versões secundárias, a menos que seja reimplantada, mesmo com essa propriedade definida como verdadeira.</span><span class="sxs-lookup"><span data-stu-id="85c83-175">Once deployed, however, the extension will not upgrade minor versions unless redeployed, even with this property set to true.</span></span>
  - <span data-ttu-id="85c83-176">`[ForceUpdateTag <String>]`: como o manipulador de extensão deve ser obrigado a atualizar mesmo que a configuração da extensão não tenha sido alterada.</span><span class="sxs-lookup"><span data-stu-id="85c83-176">`[ForceUpdateTag <String>]`: How the extension handler should be forced to update even if the extension configuration has not changed.</span></span>
  - <span data-ttu-id="85c83-177">`[MachineExtensionType <String>]`: especifica o tipo da extensão; um exemplo é "CustomScriptExtension".</span><span class="sxs-lookup"><span data-stu-id="85c83-177">`[MachineExtensionType <String>]`: Specifies the type of the extension; an example is "CustomScriptExtension".</span></span>
  - <span data-ttu-id="85c83-178">`[ProtectedSetting <IMachineExtensionPropertiesProtectedSettings>]`: A extensão pode conterSettings protegidos ou protectedSettingsFromKeyVault ou nenhuma configuração protegida.</span><span class="sxs-lookup"><span data-stu-id="85c83-178">`[ProtectedSetting <IMachineExtensionPropertiesProtectedSettings>]`: The extension can contain either protectedSettings or protectedSettingsFromKeyVault or no protected settings at all.</span></span>
  - <span data-ttu-id="85c83-179">`[Publisher <String>]`: o nome do editor de manipuladores de extensão.</span><span class="sxs-lookup"><span data-stu-id="85c83-179">`[Publisher <String>]`: The name of the extension handler publisher.</span></span>
  - <span data-ttu-id="85c83-180">`[Setting <IMachineExtensionPropertiesSettings>]`: Json formatou as configurações públicas para a extensão.</span><span class="sxs-lookup"><span data-stu-id="85c83-180">`[Setting <IMachineExtensionPropertiesSettings>]`: Json formatted public settings for the extension.</span></span>
  - <span data-ttu-id="85c83-181">`[TypeHandlerVersion <String>]`: especifica a versão do manipulador de script.</span><span class="sxs-lookup"><span data-stu-id="85c83-181">`[TypeHandlerVersion <String>]`: Specifies the version of the script handler.</span></span>

## <span data-ttu-id="85c83-182">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="85c83-182">RELATED LINKS</span></span>


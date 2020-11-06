---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/set-azurermfrontdoorfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/Set-AzureRmFrontDoorFireWallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/Set-AzureRmFrontDoorFireWallPolicy.md
ms.openlocfilehash: a02510cc72b9e674f9d4fded1355ae5b2cadc807
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93601968"
---
# <span data-ttu-id="cfc5f-101">Set-AzureRmFrontDoorFireWallPolicy</span><span class="sxs-lookup"><span data-stu-id="cfc5f-101">Set-AzureRmFrontDoorFireWallPolicy</span></span>

## <span data-ttu-id="cfc5f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cfc5f-102">SYNOPSIS</span></span>
<span data-ttu-id="cfc5f-103">atualizar a política WAF</span><span class="sxs-lookup"><span data-stu-id="cfc5f-103">update WAF policy</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cfc5f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cfc5f-104">SYNTAX</span></span>

### <span data-ttu-id="cfc5f-105">ByFieldsParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="cfc5f-105">ByFieldsParameterSet (Default)</span></span>
```
Set-AzureRmFrontDoorFireWallPolicy -ResourceGroupName <String> -Name <String> [-EnabledState <PSEnabledState>]
 [-Mode <PSMode>] [-Customrule <PSCustomRule[]>] [-ManagedRule <PSManagedRule[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cfc5f-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cfc5f-106">ByObjectParameterSet</span></span>
```
Set-AzureRmFrontDoorFireWallPolicy -InputObject <PSPolicy> [-EnabledState <PSEnabledState>] [-Mode <PSMode>]
 [-Customrule <PSCustomRule[]>] [-ManagedRule <PSManagedRule[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cfc5f-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cfc5f-107">ResourceIdParameterSet</span></span>
```
Set-AzureRmFrontDoorFireWallPolicy -ResourceId <String> [-EnabledState <PSEnabledState>] [-Mode <PSMode>]
 [-Customrule <PSCustomRule[]>] [-ManagedRule <PSManagedRule[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cfc5f-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="cfc5f-108">DESCRIPTION</span></span>
<span data-ttu-id="cfc5f-109">O cmdlet **set-AzureRmFrontDoor** atualiza uma política WAF existente.</span><span class="sxs-lookup"><span data-stu-id="cfc5f-109">The **Set-AzureRmFrontDoor** cmdlet updates an existing WAF policy.</span></span> <span data-ttu-id="cfc5f-110">Se os parâmetros de entrada não forem fornecidos, os parâmetros antigos da política WAF existente serão usados.</span><span class="sxs-lookup"><span data-stu-id="cfc5f-110">If input parameters are not provided, old parameters from the existing WAF policy will be used.</span></span>

## <span data-ttu-id="cfc5f-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cfc5f-111">EXAMPLES</span></span>

### <span data-ttu-id="cfc5f-112">Exemplo 1: atualizar uma política de WAF existente</span><span class="sxs-lookup"><span data-stu-id="cfc5f-112">Example 1: update an existing WAF policy</span></span>
```powershell
PS C:\> Set-AzureRmFrontDoorFireWallPolicy -Name $name -ResourceGroupName $resourceGroup -Customrule $customRule -ManagedRule $managedRule -EnabledState $enabledState -Mode $node

PolicyMode         : Prevention
PolicyEnabledState : Enabled
CustomRules        : {Rule1}
ManagedRules       : {Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRule}
Etag               :
ProvisioningState  : Succeeded
Tags               :
Id                 : /subscriptions/{subid}/resourcegroups/{resourceGroupName}/providers/Micr
                     osoft.Network/frontdoorwebapplicationfirewallpolicies/{Name}
Name               : {Name}
Type               :
```

<span data-ttu-id="cfc5f-113">atualizar uma política existente do WAF</span><span class="sxs-lookup"><span data-stu-id="cfc5f-113">update an existing WAF policy</span></span>

### <span data-ttu-id="cfc5f-114">Exemplo 2: atualizar uma política existente do WAF</span><span class="sxs-lookup"><span data-stu-id="cfc5f-114">Example 2: update an existing WAF policy</span></span>
```powershell
PS C:\> Set-AzureRmFrontDoorFireWallPolicy -InputObject $policy1 -Customrule $customRule -ManagedRule $managedRule -EnabledState $enabledState -Mode $mode

PolicyMode         : Prevention
PolicyEnabledState : Enabled
CustomRules        : {Rule1}
ManagedRules       : {Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRule}
Etag               :
ProvisioningState  : Succeeded
Tags               :
Id                 : /subscriptions/{subid}/resourcegroups/{resourceGroupName}/providers/Micr
                     osoft.Network/frontdoorwebapplicationfirewallpolicies/{Name}
Name               : {Name}
Type               :
```

<span data-ttu-id="cfc5f-115">atualizar uma política existente do WAF</span><span class="sxs-lookup"><span data-stu-id="cfc5f-115">update an existing WAF policy</span></span>

### <span data-ttu-id="cfc5f-116">Exemplo 3: atualizar uma política de WAF existente</span><span class="sxs-lookup"><span data-stu-id="cfc5f-116">Example 3: update an existing WAF policy</span></span>
```powershell
PS C:\> Set-AzureRmFrontDoorFireWallPolicy -ResourceId $resourcdId -Customrule $customRule -ManagedRule $managedRule -EnabledState $enabledState -Mode $mode

PolicyMode         : Prevention
PolicyEnabledState : Enabled
CustomRules        : {Rule1}
ManagedRules       : {Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRule}
Etag               :
ProvisioningState  : Succeeded
Tags               :
Id                 : /subscriptions/{subid}/resourcegroups/{resourceGroupName}/providers/Micr
                     osoft.Network/frontdoorwebapplicationfirewallpolicies/{Name}
Name               : {Name}
Type               :
```

<span data-ttu-id="cfc5f-117">atualizar uma política existente do WAF</span><span class="sxs-lookup"><span data-stu-id="cfc5f-117">update an existing WAF policy</span></span>

### <span data-ttu-id="cfc5f-118">Exemplo 4: atualizar todas as políticas do WAF no $resourceGroup</span><span class="sxs-lookup"><span data-stu-id="cfc5f-118">Example 4: update all WAF policies in $resourceGroup</span></span>
```powershell
PS C:\> Get-AzureRmFrontDoorFireWallPolicy -ResourceGroupName $resourceGroup | Set-AzureRmFrontDoorFireWallPolicy -Customrule $customRule -ManagedRule $managedRule -EnabledState $enabledState -Mode $mode
```

<span data-ttu-id="cfc5f-119">atualizar todas as políticas do WAF no $resourceGroup</span><span class="sxs-lookup"><span data-stu-id="cfc5f-119">update all WAF policies in $resourceGroup</span></span>

## <span data-ttu-id="cfc5f-120">OS</span><span class="sxs-lookup"><span data-stu-id="cfc5f-120">PARAMETERS</span></span>

### <span data-ttu-id="cfc5f-121">-Customrule</span><span class="sxs-lookup"><span data-stu-id="cfc5f-121">-Customrule</span></span>
<span data-ttu-id="cfc5f-122">Regras personalizadas dentro da política</span><span class="sxs-lookup"><span data-stu-id="cfc5f-122">Custom rules inside the policy</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSCustomRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cfc5f-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cfc5f-123">-DefaultProfile</span></span>
<span data-ttu-id="cfc5f-124">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="cfc5f-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cfc5f-125">-Enabledstate</span><span class="sxs-lookup"><span data-stu-id="cfc5f-125">-EnabledState</span></span>
<span data-ttu-id="cfc5f-126">Se a política está no estado habilitado ou desabilitado.</span><span class="sxs-lookup"><span data-stu-id="cfc5f-126">Whether the policy is in enabled state or disabled state.</span></span>
<span data-ttu-id="cfc5f-127">Os valores possíveis incluem: ' disabled ', ' Enabled '</span><span class="sxs-lookup"><span data-stu-id="cfc5f-127">Possible values include: 'Disabled', 'Enabled'</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSEnabledState
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cfc5f-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cfc5f-128">-InputObject</span></span>
<span data-ttu-id="cfc5f-129">O objeto FireWallPolicy a ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="cfc5f-129">The FireWallPolicy object to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cfc5f-130">-ManagedRule</span><span class="sxs-lookup"><span data-stu-id="cfc5f-130">-ManagedRule</span></span>
<span data-ttu-id="cfc5f-131">Regras gerenciadas dentro da política</span><span class="sxs-lookup"><span data-stu-id="cfc5f-131">Managed rules inside the policy</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSManagedRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cfc5f-132">-Mode</span><span class="sxs-lookup"><span data-stu-id="cfc5f-132">-Mode</span></span>
<span data-ttu-id="cfc5f-133">Descreve se ele está no modo de detecção ou no modo de prevenção em nível de política.</span><span class="sxs-lookup"><span data-stu-id="cfc5f-133">Describes if it is in detection mode  or prevention mode at policy level.</span></span>
<span data-ttu-id="cfc5f-134">Os valores possíveis incluem: ' Prevention ', ' detecção '</span><span class="sxs-lookup"><span data-stu-id="cfc5f-134">Possible values include:'Prevention', 'Detection'</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSMode
Parameter Sets: (All)
Aliases:
Accepted values: Prevention, Detection

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cfc5f-135">-Nome</span><span class="sxs-lookup"><span data-stu-id="cfc5f-135">-Name</span></span>
<span data-ttu-id="cfc5f-136">O nome do FireWallPolicy a ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="cfc5f-136">The name of the FireWallPolicy to update.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cfc5f-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cfc5f-137">-ResourceGroupName</span></span>
<span data-ttu-id="cfc5f-138">O grupo de recursos ao qual o FireWallPolicy pertence.</span><span class="sxs-lookup"><span data-stu-id="cfc5f-138">The resource group to which the FireWallPolicy belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cfc5f-139">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cfc5f-139">-ResourceId</span></span>
<span data-ttu-id="cfc5f-140">ID do recurso do FireWallPolicy para atualizar</span><span class="sxs-lookup"><span data-stu-id="cfc5f-140">Resource Id of the FireWallPolicy to update</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cfc5f-141">-Confirme</span><span class="sxs-lookup"><span data-stu-id="cfc5f-141">-Confirm</span></span>
<span data-ttu-id="cfc5f-142">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cfc5f-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cfc5f-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cfc5f-143">-WhatIf</span></span>
<span data-ttu-id="cfc5f-144">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="cfc5f-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cfc5f-145">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="cfc5f-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cfc5f-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cfc5f-146">CommonParameters</span></span>
<span data-ttu-id="cfc5f-147">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cfc5f-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cfc5f-148">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cfc5f-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cfc5f-149">SENSORES</span><span class="sxs-lookup"><span data-stu-id="cfc5f-149">INPUTS</span></span>

### <span data-ttu-id="cfc5f-150">Microsoft. Azure. Commands. FrontDoor. Models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="cfc5f-150">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

### <span data-ttu-id="cfc5f-151">System. String</span><span class="sxs-lookup"><span data-stu-id="cfc5f-151">System.String</span></span>

## <span data-ttu-id="cfc5f-152">EXIBE</span><span class="sxs-lookup"><span data-stu-id="cfc5f-152">OUTPUTS</span></span>

### <span data-ttu-id="cfc5f-153">Microsoft. Azure. Commands. FrontDoor. Models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="cfc5f-153">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

## <span data-ttu-id="cfc5f-154">INFORMA</span><span class="sxs-lookup"><span data-stu-id="cfc5f-154">NOTES</span></span>

## <span data-ttu-id="cfc5f-155">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cfc5f-155">RELATED LINKS</span></span>

<span data-ttu-id="cfc5f-156">[New-AzureRmFrontDoorFireWallPolicy](./New-AzureRmFrontDoorFireWallPolicy.md) 
 [Get-AzureRmFrontDoorFireWallPolicy](./Get-AzureRmFrontDoorFireWallPolicy.md) 
 [New-AzureRmFrontDoorManagedRuleObject](./New-AzureRmFrontDoorManagedRuleObject.md) 
 [New-AzureRmFrontDoorCustomRuleObject](./New-AzureRmFrontDoorManagedRuleObject.md)</span><span class="sxs-lookup"><span data-stu-id="cfc5f-156">[New-AzureRmFrontDoorFireWallPolicy](./New-AzureRmFrontDoorFireWallPolicy.md)
[Get-AzureRmFrontDoorFireWallPolicy](./Get-AzureRmFrontDoorFireWallPolicy.md)
[New-AzureRmFrontDoorManagedRuleObject](./New-AzureRmFrontDoorManagedRuleObject.md)
[New-AzureRmFrontDoorCustomRuleObject](./New-AzureRmFrontDoorManagedRuleObject.md)</span></span>

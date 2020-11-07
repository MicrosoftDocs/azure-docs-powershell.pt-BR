---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/update-azfrontdoorwafpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Update-AzFrontDoorWafPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Update-AzFrontDoorWafPolicy.md
ms.openlocfilehash: cafb705ec5f2882eb239931b22ccfba610721100
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93941161"
---
# <span data-ttu-id="548e6-101">Update-AzFrontDoorWafPolicy</span><span class="sxs-lookup"><span data-stu-id="548e6-101">Update-AzFrontDoorWafPolicy</span></span>

## <span data-ttu-id="548e6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="548e6-102">SYNOPSIS</span></span>
<span data-ttu-id="548e6-103">Atualizar a política WAF</span><span class="sxs-lookup"><span data-stu-id="548e6-103">Update WAF policy</span></span>

## <span data-ttu-id="548e6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="548e6-104">SYNTAX</span></span>

### <span data-ttu-id="548e6-105">ByFieldsParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="548e6-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzFrontDoorWafPolicy -ResourceGroupName <String> -Name <String> [-EnabledState <PSEnabledState>]
 [-Mode <String>] [-Customrule <PSCustomRule[]>] [-ManagedRule <PSManagedRule[]>] [-RedirectUrl <String>]
 [-CustomBlockResponseStatusCode <Int32>] [-CustomBlockResponseBody <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="548e6-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="548e6-106">ByObjectParameterSet</span></span>
```
Update-AzFrontDoorWafPolicy -InputObject <PSPolicy> [-EnabledState <PSEnabledState>] [-Mode <String>]
 [-Customrule <PSCustomRule[]>] [-ManagedRule <PSManagedRule[]>] [-RedirectUrl <String>]
 [-CustomBlockResponseStatusCode <Int32>] [-CustomBlockResponseBody <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="548e6-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="548e6-107">ByResourceIdParameterSet</span></span>
```
Update-AzFrontDoorWafPolicy -ResourceId <String> [-EnabledState <PSEnabledState>] [-Mode <String>]
 [-Customrule <PSCustomRule[]>] [-ManagedRule <PSManagedRule[]>] [-RedirectUrl <String>]
 [-CustomBlockResponseStatusCode <Int32>] [-CustomBlockResponseBody <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="548e6-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="548e6-108">DESCRIPTION</span></span>
<span data-ttu-id="548e6-109">O cmdlet **Update-AzFrontDoorWafPolicy** atualiza uma política WAF existente.</span><span class="sxs-lookup"><span data-stu-id="548e6-109">The **Update-AzFrontDoorWafPolicy** cmdlet updates an existing WAF policy.</span></span> <span data-ttu-id="548e6-110">Se os parâmetros de entrada não forem fornecidos, os parâmetros antigos da política WAF existente serão usados.</span><span class="sxs-lookup"><span data-stu-id="548e6-110">If input parameters are not provided, old parameters from the existing WAF policy will be used.</span></span>

## <span data-ttu-id="548e6-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="548e6-111">EXAMPLES</span></span>

### <span data-ttu-id="548e6-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="548e6-112">Example 1</span></span>
```powershell
PS C:\> Update-AzFrontDoorWafPolicy -Name $policyName -ResourceGroupName $resourceGroupName -CustomBlockResponseStatusCode 403

Name         PolicyMode PolicyEnabledState CustomBlockResponseStatusCode RedirectUrl
----         ---------- ------------------ ----------------------------- -----------
{policyName} Prevention            Enabled                           403 https://www.bing.com/
```

<span data-ttu-id="548e6-113">Atualize um código de status personalizado de política de WAF existente.</span><span class="sxs-lookup"><span data-stu-id="548e6-113">Update an existing WAF policy custom status code.</span></span>

### <span data-ttu-id="548e6-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="548e6-114">Example 2</span></span>
```powershell
PS C:\> Update-AzFrontDoorWafPolicy -Name $policyName -ResourceGroupName $resourceGroupName -Mode Detection

Name         PolicyMode PolicyEnabledState CustomBlockResponseStatusCode RedirectUrl
----         ---------- ------------------ ----------------------------- -----------
{policyName} Detection            Enabled                           403 https://www.bing.com/
```

<span data-ttu-id="548e6-115">Atualizar um modo de política WAF existente.</span><span class="sxs-lookup"><span data-stu-id="548e6-115">Update an existing WAF policy mode.</span></span>

### <span data-ttu-id="548e6-116">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="548e6-116">Example 3</span></span>
```powershell
PS C:\> Update-AzFrontDoorWafPolicy -Name $policyName -ResourceGroupName $resourceGroupName -Mode Detection -EnabledState Disabled

Name          PolicyMode PolicyEnabledState CustomBlockResponseStatusCode RedirectUrl
----          ---------- ------------------ ----------------------------- -----------
{policyName}  Detection           Disabled                           403 https://www.bing.com/
```

<span data-ttu-id="548e6-117">Atualizar um estado e modo habilitados para política do WAF existente.</span><span class="sxs-lookup"><span data-stu-id="548e6-117">Update an existing WAF policy enabled state and mode.</span></span>

### <span data-ttu-id="548e6-118">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="548e6-118">Example 4</span></span>
```powershell
PS C:\> Get-AzFrontDoorWafPolicy -ResourceGroupName $resourceGroupName | Update-AzFrontDoorWafPolicy -Mode Detection -EnabledState Disabled
```

<span data-ttu-id="548e6-119">Atualizar todas as políticas do WAF no $resourceGroupName</span><span class="sxs-lookup"><span data-stu-id="548e6-119">Update all WAF policies in $resourceGroupName</span></span>

## <span data-ttu-id="548e6-120">OS</span><span class="sxs-lookup"><span data-stu-id="548e6-120">PARAMETERS</span></span>

### <span data-ttu-id="548e6-121">-CustomBlockResponseBody</span><span class="sxs-lookup"><span data-stu-id="548e6-121">-CustomBlockResponseBody</span></span>
<span data-ttu-id="548e6-122">Corpo de resposta personalizado</span><span class="sxs-lookup"><span data-stu-id="548e6-122">Custom Response Body</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="548e6-123">-CustomBlockResponseStatusCode</span><span class="sxs-lookup"><span data-stu-id="548e6-123">-CustomBlockResponseStatusCode</span></span>
<span data-ttu-id="548e6-124">Código de status de resposta personalizado</span><span class="sxs-lookup"><span data-stu-id="548e6-124">Custom Response Status Code</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="548e6-125">-Customrule</span><span class="sxs-lookup"><span data-stu-id="548e6-125">-Customrule</span></span>
<span data-ttu-id="548e6-126">Regras personalizadas dentro da política</span><span class="sxs-lookup"><span data-stu-id="548e6-126">Custom rules inside the policy</span></span>

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

### <span data-ttu-id="548e6-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="548e6-127">-DefaultProfile</span></span>
<span data-ttu-id="548e6-128">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="548e6-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="548e6-129">-Enabledstate</span><span class="sxs-lookup"><span data-stu-id="548e6-129">-EnabledState</span></span>
<span data-ttu-id="548e6-130">Se a política está no estado habilitado ou desabilitado.</span><span class="sxs-lookup"><span data-stu-id="548e6-130">Whether the policy is in enabled state or disabled state.</span></span>
<span data-ttu-id="548e6-131">Os valores possíveis incluem: ' disabled ', ' Enabled '</span><span class="sxs-lookup"><span data-stu-id="548e6-131">Possible values include: 'Disabled', 'Enabled'</span></span>

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

### <span data-ttu-id="548e6-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="548e6-132">-InputObject</span></span>
<span data-ttu-id="548e6-133">O objeto FireWallPolicy a ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="548e6-133">The FireWallPolicy object to update.</span></span>

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

### <span data-ttu-id="548e6-134">-ManagedRule</span><span class="sxs-lookup"><span data-stu-id="548e6-134">-ManagedRule</span></span>
<span data-ttu-id="548e6-135">Regras gerenciadas dentro da política</span><span class="sxs-lookup"><span data-stu-id="548e6-135">Managed rules inside the policy</span></span>

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

### <span data-ttu-id="548e6-136">-Mode</span><span class="sxs-lookup"><span data-stu-id="548e6-136">-Mode</span></span>
<span data-ttu-id="548e6-137">Descreve se ele está no modo de detecção ou no modo de prevenção em nível de política.</span><span class="sxs-lookup"><span data-stu-id="548e6-137">Describes if it is in detection mode  or prevention mode at policy level.</span></span>
<span data-ttu-id="548e6-138">Os valores possíveis incluem: ' Prevention ', ' detecção '</span><span class="sxs-lookup"><span data-stu-id="548e6-138">Possible values include:'Prevention', 'Detection'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="548e6-139">-Nome</span><span class="sxs-lookup"><span data-stu-id="548e6-139">-Name</span></span>
<span data-ttu-id="548e6-140">O nome do FireWallPolicy a ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="548e6-140">The name of the FireWallPolicy to update.</span></span>

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

### <span data-ttu-id="548e6-141">-RedirectUrl</span><span class="sxs-lookup"><span data-stu-id="548e6-141">-RedirectUrl</span></span>
<span data-ttu-id="548e6-142">Redirecionar URL</span><span class="sxs-lookup"><span data-stu-id="548e6-142">Redirect URL</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="548e6-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="548e6-143">-ResourceGroupName</span></span>
<span data-ttu-id="548e6-144">O grupo de recursos ao qual o FireWallPolicy pertence.</span><span class="sxs-lookup"><span data-stu-id="548e6-144">The resource group to which the FireWallPolicy belongs.</span></span>

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

### <span data-ttu-id="548e6-145">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="548e6-145">-ResourceId</span></span>
<span data-ttu-id="548e6-146">ID do recurso do FireWallPolicy para atualizar</span><span class="sxs-lookup"><span data-stu-id="548e6-146">Resource Id of the FireWallPolicy to update</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="548e6-147">-Confirme</span><span class="sxs-lookup"><span data-stu-id="548e6-147">-Confirm</span></span>
<span data-ttu-id="548e6-148">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="548e6-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="548e6-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="548e6-149">-WhatIf</span></span>
<span data-ttu-id="548e6-150">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="548e6-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="548e6-151">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="548e6-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="548e6-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="548e6-152">CommonParameters</span></span>
<span data-ttu-id="548e6-153">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="548e6-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="548e6-154">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="548e6-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="548e6-155">SENSORES</span><span class="sxs-lookup"><span data-stu-id="548e6-155">INPUTS</span></span>

### <span data-ttu-id="548e6-156">Microsoft. Azure. Commands. FrontDoor. Models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="548e6-156">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

### <span data-ttu-id="548e6-157">System. String</span><span class="sxs-lookup"><span data-stu-id="548e6-157">System.String</span></span>

## <span data-ttu-id="548e6-158">EXIBE</span><span class="sxs-lookup"><span data-stu-id="548e6-158">OUTPUTS</span></span>

### <span data-ttu-id="548e6-159">Microsoft. Azure. Commands. FrontDoor. Models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="548e6-159">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

## <span data-ttu-id="548e6-160">INFORMA</span><span class="sxs-lookup"><span data-stu-id="548e6-160">NOTES</span></span>

## <span data-ttu-id="548e6-161">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="548e6-161">RELATED LINKS</span></span>

<span data-ttu-id="548e6-162">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md) 
 [Get-AzFrontDoorWafPolicy](./Get-AzFrontDoorWafPolicy.md) 
 [New-AzFrontDoorWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md) 
 [New-AzFrontDoorWafCustomRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)</span><span class="sxs-lookup"><span data-stu-id="548e6-162">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md)
[Get-AzFrontDoorWafPolicy](./Get-AzFrontDoorWafPolicy.md)
[New-AzFrontDoorWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)
[New-AzFrontDoorWafCustomRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)</span></span>

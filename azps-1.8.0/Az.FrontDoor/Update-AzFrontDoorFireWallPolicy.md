---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/update-azfrontdoorfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Update-AzFrontDoorFireWallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Update-AzFrontDoorFireWallPolicy.md
ms.openlocfilehash: 3e0502d3503bdbf95fb81c779829b73e896b150f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93770833"
---
# <span data-ttu-id="c3122-101">Update-AzFrontDoorFireWallPolicy</span><span class="sxs-lookup"><span data-stu-id="c3122-101">Update-AzFrontDoorFireWallPolicy</span></span>

## <span data-ttu-id="c3122-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c3122-102">SYNOPSIS</span></span>
<span data-ttu-id="c3122-103">Atualizar a política WAF</span><span class="sxs-lookup"><span data-stu-id="c3122-103">Update WAF policy</span></span>

## <span data-ttu-id="c3122-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c3122-104">SYNTAX</span></span>

### <span data-ttu-id="c3122-105">ByFieldsParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="c3122-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzFrontDoorFireWallPolicy -ResourceGroupName <String> -Name <String> [-EnabledState <PSEnabledState>]
 [-Mode <PSMode>] [-Customrule <PSCustomRule[]>] [-ManagedRule <PSManagedRule[]>] [-RedirectUrl <String>]
 [-CustomBlockResponseStatusCode <Int32>] [-CustomBlockResponseBody <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c3122-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c3122-106">ByObjectParameterSet</span></span>
```
Update-AzFrontDoorFireWallPolicy -InputObject <PSPolicy> [-EnabledState <PSEnabledState>] [-Mode <PSMode>]
 [-Customrule <PSCustomRule[]>] [-ManagedRule <PSManagedRule[]>] [-RedirectUrl <String>]
 [-CustomBlockResponseStatusCode <Int32>] [-CustomBlockResponseBody <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c3122-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c3122-107">ByResourceIdParameterSet</span></span>
```
Update-AzFrontDoorFireWallPolicy -ResourceId <String> [-EnabledState <PSEnabledState>] [-Mode <PSMode>]
 [-Customrule <PSCustomRule[]>] [-ManagedRule <PSManagedRule[]>] [-RedirectUrl <String>]
 [-CustomBlockResponseStatusCode <Int32>] [-CustomBlockResponseBody <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c3122-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c3122-108">DESCRIPTION</span></span>
<span data-ttu-id="c3122-109">O cmdlet **Update-AzFrontDoorFireWallPolicy** atualiza uma política WAF existente.</span><span class="sxs-lookup"><span data-stu-id="c3122-109">The **Update-AzFrontDoorFireWallPolicy** cmdlet updates an existing WAF policy.</span></span> <span data-ttu-id="c3122-110">Se os parâmetros de entrada não forem fornecidos, os parâmetros antigos da política WAF existente serão usados.</span><span class="sxs-lookup"><span data-stu-id="c3122-110">If input parameters are not provided, old parameters from the existing WAF policy will be used.</span></span>

## <span data-ttu-id="c3122-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c3122-111">EXAMPLES</span></span>

### <span data-ttu-id="c3122-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c3122-112">Example 1</span></span>
```powershell
PS C:\> Update-AzFrontDoorFireWallPolicy -Name $policyName -ResourceGroupName $resourceGroupName -CustomBlockResponseStatusCode 403

Name         PolicyMode PolicyEnabledState CustomBlockResponseStatusCode RedirectUrl
----         ---------- ------------------ ----------------------------- -----------
{policyName} Prevention            Enabled                           403 https://www.bing.com/
```

<span data-ttu-id="c3122-113">Atualize um código de status personalizado de política de WAF existente.</span><span class="sxs-lookup"><span data-stu-id="c3122-113">Update an existing WAF policy custom status code.</span></span>

### <span data-ttu-id="c3122-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="c3122-114">Example 2</span></span>
```powershell
PS C:\> Update-AzFrontDoorFireWallPolicy -Name $policyName -ResourceGroupName $resourceGroupName -Mode Detection

Name         PolicyMode PolicyEnabledState CustomBlockResponseStatusCode RedirectUrl
----         ---------- ------------------ ----------------------------- -----------
{policyName} Detection            Enabled                           403 https://www.bing.com/
```

<span data-ttu-id="c3122-115">Atualizar um modo de política WAF existente.</span><span class="sxs-lookup"><span data-stu-id="c3122-115">Update an existing WAF policy mode.</span></span>

### <span data-ttu-id="c3122-116">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="c3122-116">Example 3</span></span>
```powershell
PS C:\> Update-AzFrontDoorFireWallPolicy -Name $policyName -ResourceGroupName $resourceGroupName -Mode Detection -EnabledState Disabled

Name          PolicyMode PolicyEnabledState CustomBlockResponseStatusCode RedirectUrl
----          ---------- ------------------ ----------------------------- -----------
{policyName}  Detection           Disabled                           403 https://www.bing.com/
```

<span data-ttu-id="c3122-117">Atualizar um estado e modo habilitados para política do WAF existente.</span><span class="sxs-lookup"><span data-stu-id="c3122-117">Update an existing WAF policy enabled state and mode.</span></span>

### <span data-ttu-id="c3122-118">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="c3122-118">Example 4</span></span>
```powershell
PS C:\> Get-AzFrontDoorFireWallPolicy -ResourceGroupName $resourceGroupName | Update-AzFrontDoorFireWallPolicy -Mode Detection -EnabledState Disabled
```

<span data-ttu-id="c3122-119">Atualizar todas as políticas do WAF no $resourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3122-119">Update all WAF policies in $resourceGroupName</span></span>

## <span data-ttu-id="c3122-120">OS</span><span class="sxs-lookup"><span data-stu-id="c3122-120">PARAMETERS</span></span>

### <span data-ttu-id="c3122-121">-CustomBlockResponseBody</span><span class="sxs-lookup"><span data-stu-id="c3122-121">-CustomBlockResponseBody</span></span>
<span data-ttu-id="c3122-122">Corpo de resposta personalizado</span><span class="sxs-lookup"><span data-stu-id="c3122-122">Custom Response Body</span></span>

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

### <span data-ttu-id="c3122-123">-CustomBlockResponseStatusCode</span><span class="sxs-lookup"><span data-stu-id="c3122-123">-CustomBlockResponseStatusCode</span></span>
<span data-ttu-id="c3122-124">Código de status de resposta personalizado</span><span class="sxs-lookup"><span data-stu-id="c3122-124">Custom Response Status Code</span></span>

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

### <span data-ttu-id="c3122-125">-Customrule</span><span class="sxs-lookup"><span data-stu-id="c3122-125">-Customrule</span></span>
<span data-ttu-id="c3122-126">Regras personalizadas dentro da política</span><span class="sxs-lookup"><span data-stu-id="c3122-126">Custom rules inside the policy</span></span>

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

### <span data-ttu-id="c3122-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3122-127">-DefaultProfile</span></span>
<span data-ttu-id="c3122-128">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c3122-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c3122-129">-Enabledstate</span><span class="sxs-lookup"><span data-stu-id="c3122-129">-EnabledState</span></span>
<span data-ttu-id="c3122-130">Se a política está no estado habilitado ou desabilitado.</span><span class="sxs-lookup"><span data-stu-id="c3122-130">Whether the policy is in enabled state or disabled state.</span></span>
<span data-ttu-id="c3122-131">Os valores possíveis incluem: ' disabled ', ' Enabled '</span><span class="sxs-lookup"><span data-stu-id="c3122-131">Possible values include: 'Disabled', 'Enabled'</span></span>

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

### <span data-ttu-id="c3122-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c3122-132">-InputObject</span></span>
<span data-ttu-id="c3122-133">O objeto FireWallPolicy a ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="c3122-133">The FireWallPolicy object to update.</span></span>

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

### <span data-ttu-id="c3122-134">-ManagedRule</span><span class="sxs-lookup"><span data-stu-id="c3122-134">-ManagedRule</span></span>
<span data-ttu-id="c3122-135">Regras gerenciadas dentro da política</span><span class="sxs-lookup"><span data-stu-id="c3122-135">Managed rules inside the policy</span></span>

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

### <span data-ttu-id="c3122-136">-Mode</span><span class="sxs-lookup"><span data-stu-id="c3122-136">-Mode</span></span>
<span data-ttu-id="c3122-137">Descreve se ele está no modo de detecção ou no modo de prevenção em nível de política.</span><span class="sxs-lookup"><span data-stu-id="c3122-137">Describes if it is in detection mode  or prevention mode at policy level.</span></span>
<span data-ttu-id="c3122-138">Os valores possíveis incluem: ' Prevention ', ' detecção '</span><span class="sxs-lookup"><span data-stu-id="c3122-138">Possible values include:'Prevention', 'Detection'</span></span>

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

### <span data-ttu-id="c3122-139">-Nome</span><span class="sxs-lookup"><span data-stu-id="c3122-139">-Name</span></span>
<span data-ttu-id="c3122-140">O nome do FireWallPolicy a ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="c3122-140">The name of the FireWallPolicy to update.</span></span>

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

### <span data-ttu-id="c3122-141">-RedirectUrl</span><span class="sxs-lookup"><span data-stu-id="c3122-141">-RedirectUrl</span></span>
<span data-ttu-id="c3122-142">Redirecionar URL</span><span class="sxs-lookup"><span data-stu-id="c3122-142">Redirect URL</span></span>

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

### <span data-ttu-id="c3122-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3122-143">-ResourceGroupName</span></span>
<span data-ttu-id="c3122-144">O grupo de recursos ao qual o FireWallPolicy pertence.</span><span class="sxs-lookup"><span data-stu-id="c3122-144">The resource group to which the FireWallPolicy belongs.</span></span>

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

### <span data-ttu-id="c3122-145">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c3122-145">-ResourceId</span></span>
<span data-ttu-id="c3122-146">ID do recurso do FireWallPolicy para atualizar</span><span class="sxs-lookup"><span data-stu-id="c3122-146">Resource Id of the FireWallPolicy to update</span></span>

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

### <span data-ttu-id="c3122-147">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c3122-147">-Confirm</span></span>
<span data-ttu-id="c3122-148">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c3122-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c3122-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c3122-149">-WhatIf</span></span>
<span data-ttu-id="c3122-150">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c3122-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c3122-151">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c3122-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c3122-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3122-152">CommonParameters</span></span>
<span data-ttu-id="c3122-153">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3122-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3122-154">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c3122-154">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3122-155">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c3122-155">INPUTS</span></span>

### <span data-ttu-id="c3122-156">Microsoft. Azure. Commands. FrontDoor. Models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="c3122-156">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

### <span data-ttu-id="c3122-157">System. String</span><span class="sxs-lookup"><span data-stu-id="c3122-157">System.String</span></span>

## <span data-ttu-id="c3122-158">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c3122-158">OUTPUTS</span></span>

### <span data-ttu-id="c3122-159">Microsoft. Azure. Commands. FrontDoor. Models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="c3122-159">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

## <span data-ttu-id="c3122-160">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c3122-160">NOTES</span></span>

## <span data-ttu-id="c3122-161">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c3122-161">RELATED LINKS</span></span>

<span data-ttu-id="c3122-162">[New-AzFrontDoorFireWallPolicy](./New-AzFrontDoorFireWallPolicy.md) 
 [Get-AzFrontDoorFireWallPolicy](./Get-AzFrontDoorFireWallPolicy.md) 
 [New-AzFrontDoorManagedRuleObject](./New-AzFrontDoorManagedRuleObject.md) 
 [New-AzFrontDoorCustomRuleObject](./New-AzFrontDoorManagedRuleObject.md)</span><span class="sxs-lookup"><span data-stu-id="c3122-162">[New-AzFrontDoorFireWallPolicy](./New-AzFrontDoorFireWallPolicy.md)
[Get-AzFrontDoorFireWallPolicy](./Get-AzFrontDoorFireWallPolicy.md)
[New-AzFrontDoorManagedRuleObject](./New-AzFrontDoorManagedRuleObject.md)
[New-AzFrontDoorCustomRuleObject](./New-AzFrontDoorManagedRuleObject.md)</span></span>

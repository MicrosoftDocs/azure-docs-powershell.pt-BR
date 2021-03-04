---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/powershell/module/az.policyinsights/remove-azpolicyremediation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Remove-AzPolicyRemediation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Remove-AzPolicyRemediation.md
ms.openlocfilehash: 44e6be7e7f112d0c6e4e657aca5670211aff6006
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890105"
---
# <span data-ttu-id="fa52d-101">Remove-AzPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="fa52d-101">Remove-AzPolicyRemediation</span></span>

## <span data-ttu-id="fa52d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fa52d-102">SYNOPSIS</span></span>
<span data-ttu-id="fa52d-103">Exclui uma correção de política.</span><span class="sxs-lookup"><span data-stu-id="fa52d-103">Deletes a policy remediation.</span></span>

## <span data-ttu-id="fa52d-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="fa52d-104">SYNTAX</span></span>

### <span data-ttu-id="fa52d-105">ByName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="fa52d-105">ByName (Default)</span></span>
```
Remove-AzPolicyRemediation -Name <String> [-Scope <String>] [-ManagementGroupName <String>]
 [-ResourceGroupName <String>] [-AllowStop] [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fa52d-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="fa52d-106">ByResourceId</span></span>
```
Remove-AzPolicyRemediation -ResourceId <String> [-AllowStop] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fa52d-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="fa52d-107">ByInputObject</span></span>
```
Remove-AzPolicyRemediation -InputObject <PSRemediation> [-AllowStop] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fa52d-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="fa52d-108">DESCRIPTION</span></span>
<span data-ttu-id="fa52d-109">O cmdlet **Remove-AzPolicyRemediation** exclui uma correção de política.</span><span class="sxs-lookup"><span data-stu-id="fa52d-109">The **Remove-AzPolicyRemediation** cmdlet deletes a policy remediation.</span></span>

## <span data-ttu-id="fa52d-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fa52d-110">EXAMPLES</span></span>

### <span data-ttu-id="fa52d-111">Exemplo 1: Excluir uma correção de política no escopo do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="fa52d-111">Example 1: Delete a policy remediation at resource group scope</span></span>
```
PS C:\> Remove-AzPolicyRemediation -ResourceGroupName "myRG" -Name "remediation1"
```

<span data-ttu-id="fa52d-112">Este comando exclui a correção chamada 'correção1' no grupo de recursos 'myRG'.</span><span class="sxs-lookup"><span data-stu-id="fa52d-112">This command deletes the remediation named 'remediation1' in resource group 'myRG'.</span></span>

### <span data-ttu-id="fa52d-113">Exemplo 2: Excluir uma correção de grupo de gerenciamento por meio de canalização</span><span class="sxs-lookup"><span data-stu-id="fa52d-113">Example 2: Delete a management group remediation via piping</span></span>
```
PS C:\> $remediation = Get-AzPolicyRemediation -ManagementGroupName "mg1" -Name "remediation1"
PS C:\> $remediation | Remove-AzPolicyRemediation -Confirm
```

<span data-ttu-id="fa52d-114">Este comando exclui a correção denominada 'correção1' do grupo de gerenciamento 'mg1'.</span><span class="sxs-lookup"><span data-stu-id="fa52d-114">This command deletes the remediation named 'remediation1' from management group 'mg1'.</span></span> <span data-ttu-id="fa52d-115">Um prompt de confirmação será apresentado antes de excluir o recurso.</span><span class="sxs-lookup"><span data-stu-id="fa52d-115">A confirmation prompt will be presented before deleting the resource.</span></span>

### <span data-ttu-id="fa52d-116">Exemplo 3: Cancelar e excluir uma correção de política</span><span class="sxs-lookup"><span data-stu-id="fa52d-116">Example 3: Cancel and delete a policy remediation</span></span>
```
PS C:\> Remove-AzPolicyRemediation -ResourceGroupName "myRG" -Name "remediation1" -AllowStop
```

<span data-ttu-id="fa52d-117">Este comando exclui a correção chamada 'correção1' no grupo de recursos 'myRG'.</span><span class="sxs-lookup"><span data-stu-id="fa52d-117">This command deletes the remediation named 'remediation1' in resource group 'myRG'.</span></span> <span data-ttu-id="fa52d-118">Se a correção estiver em andamento, ela será cancelada antes de ser excluída.</span><span class="sxs-lookup"><span data-stu-id="fa52d-118">If the remediation is in-progress it will be canceled before being deleted.</span></span>

## <span data-ttu-id="fa52d-119">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="fa52d-119">PARAMETERS</span></span>

### <span data-ttu-id="fa52d-120">-AllowStop</span><span class="sxs-lookup"><span data-stu-id="fa52d-120">-AllowStop</span></span>
<span data-ttu-id="fa52d-121">Permitir que a correção seja cancelada se ela estiver em andamento.</span><span class="sxs-lookup"><span data-stu-id="fa52d-121">Allow the remediation to be canceled if it is in-progress.</span></span>

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

### <span data-ttu-id="fa52d-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fa52d-122">-AsJob</span></span>
<span data-ttu-id="fa52d-123">Execute o cmdlet em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="fa52d-123">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="fa52d-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa52d-124">-DefaultProfile</span></span>
<span data-ttu-id="fa52d-125">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fa52d-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fa52d-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fa52d-126">-InputObject</span></span>
<span data-ttu-id="fa52d-127">O objeto Remediation.</span><span class="sxs-lookup"><span data-stu-id="fa52d-127">The Remediation object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.PolicyInsights.Models.Remediation.PSRemediation
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fa52d-128">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="fa52d-128">-ManagementGroupName</span></span>
<span data-ttu-id="fa52d-129">ID do grupo de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="fa52d-129">Management group ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa52d-130">-Name</span><span class="sxs-lookup"><span data-stu-id="fa52d-130">-Name</span></span>
<span data-ttu-id="fa52d-131">Nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="fa52d-131">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa52d-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fa52d-132">-PassThru</span></span>
<span data-ttu-id="fa52d-133">Retornar True se o comando for concluído com êxito.</span><span class="sxs-lookup"><span data-stu-id="fa52d-133">Return True if the command completes successfully.</span></span>

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

### <span data-ttu-id="fa52d-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa52d-134">-ResourceGroupName</span></span>
<span data-ttu-id="fa52d-135">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="fa52d-135">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa52d-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fa52d-136">-ResourceId</span></span>
<span data-ttu-id="fa52d-137">ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="fa52d-137">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa52d-138">-Scope</span><span class="sxs-lookup"><span data-stu-id="fa52d-138">-Scope</span></span>
<span data-ttu-id="fa52d-139">Escopo do recurso.</span><span class="sxs-lookup"><span data-stu-id="fa52d-139">Scope of the resource.</span></span>
<span data-ttu-id="fa52d-140">Por exemplo,</span><span class="sxs-lookup"><span data-stu-id="fa52d-140">E.g.</span></span>
<span data-ttu-id="fa52d-141">'/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span><span class="sxs-lookup"><span data-stu-id="fa52d-141">'/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa52d-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fa52d-142">-Confirm</span></span>
<span data-ttu-id="fa52d-143">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fa52d-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fa52d-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fa52d-144">-WhatIf</span></span>
<span data-ttu-id="fa52d-145">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="fa52d-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fa52d-146">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="fa52d-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fa52d-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa52d-147">CommonParameters</span></span>
<span data-ttu-id="fa52d-148">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa52d-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa52d-149">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fa52d-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa52d-150">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fa52d-150">INPUTS</span></span>

### <span data-ttu-id="fa52d-151">System.String</span><span class="sxs-lookup"><span data-stu-id="fa52d-151">System.String</span></span>

### <span data-ttu-id="fa52d-152">Microsoft.Azure.Commands.PolicyInsights.Models.Remediation.PSRemediation</span><span class="sxs-lookup"><span data-stu-id="fa52d-152">Microsoft.Azure.Commands.PolicyInsights.Models.Remediation.PSRemediation</span></span>

## <span data-ttu-id="fa52d-153">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="fa52d-153">OUTPUTS</span></span>

### <span data-ttu-id="fa52d-154">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="fa52d-154">System.Boolean</span></span>

## <span data-ttu-id="fa52d-155">NOTES</span><span class="sxs-lookup"><span data-stu-id="fa52d-155">NOTES</span></span>

## <span data-ttu-id="fa52d-156">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fa52d-156">RELATED LINKS</span></span>

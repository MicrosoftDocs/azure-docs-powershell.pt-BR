---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/remove-azpolicyremediation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Remove-AzPolicyRemediation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Remove-AzPolicyRemediation.md
ms.openlocfilehash: 969b764be302231f33dda00b32afb79ec04a324e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94114714"
---
# <span data-ttu-id="92eca-101">Remove-AzPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="92eca-101">Remove-AzPolicyRemediation</span></span>

## <span data-ttu-id="92eca-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="92eca-102">SYNOPSIS</span></span>
<span data-ttu-id="92eca-103">Exclui uma correção de política.</span><span class="sxs-lookup"><span data-stu-id="92eca-103">Deletes a policy remediation.</span></span>

## <span data-ttu-id="92eca-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="92eca-104">SYNTAX</span></span>

### <span data-ttu-id="92eca-105">ByName (padrão)</span><span class="sxs-lookup"><span data-stu-id="92eca-105">ByName (Default)</span></span>
```
Remove-AzPolicyRemediation -Name <String> [-Scope <String>] [-ManagementGroupName <String>]
 [-ResourceGroupName <String>] [-AllowStop] [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="92eca-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="92eca-106">ByResourceId</span></span>
```
Remove-AzPolicyRemediation -ResourceId <String> [-AllowStop] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="92eca-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="92eca-107">ByInputObject</span></span>
```
Remove-AzPolicyRemediation -InputObject <PSRemediation> [-AllowStop] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="92eca-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="92eca-108">DESCRIPTION</span></span>
<span data-ttu-id="92eca-109">O cmdlet **Remove-AzPolicyRemediation** exclui uma correção de política.</span><span class="sxs-lookup"><span data-stu-id="92eca-109">The **Remove-AzPolicyRemediation** cmdlet deletes a policy remediation.</span></span>

## <span data-ttu-id="92eca-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="92eca-110">EXAMPLES</span></span>

### <span data-ttu-id="92eca-111">Exemplo 1: excluir uma correção de política no escopo do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="92eca-111">Example 1: Delete a policy remediation at resource group scope</span></span>
```
PS C:\> Remove-AzPolicyRemediation -ResourceGroupName "myRG" -Name "remediation1"
```

<span data-ttu-id="92eca-112">Este comando exclui a correção chamada "remediation1" no grupo de recursos "myRG".</span><span class="sxs-lookup"><span data-stu-id="92eca-112">This command deletes the remediation named 'remediation1' in resource group 'myRG'.</span></span>

### <span data-ttu-id="92eca-113">Exemplo 2: excluir uma correção de grupo de gerenciamento via tubulação</span><span class="sxs-lookup"><span data-stu-id="92eca-113">Example 2: Delete a management group remediation via piping</span></span>
```
PS C:\> $remediation = Get-AzPolicyRemediation -ManagementGroupName "mg1" -Name "remediation1"
PS C:\> $remediation | Remove-AzPolicyRemediation -Confirm
```

<span data-ttu-id="92eca-114">Este comando exclui a correção chamada "remediation1" do grupo de gerenciamento "MG1".</span><span class="sxs-lookup"><span data-stu-id="92eca-114">This command deletes the remediation named 'remediation1' from management group 'mg1'.</span></span> <span data-ttu-id="92eca-115">Um prompt de confirmação será apresentado antes da exclusão do recurso.</span><span class="sxs-lookup"><span data-stu-id="92eca-115">A confirmation prompt will be presented before deleting the resource.</span></span>

### <span data-ttu-id="92eca-116">Exemplo 3: cancelar e excluir uma remediação de política</span><span class="sxs-lookup"><span data-stu-id="92eca-116">Example 3: Cancel and delete a policy remediation</span></span>
```
PS C:\> Remove-AzPolicyRemediation -ResourceGroupName "myRG" -Name "remediation1" -AllowStop
```

<span data-ttu-id="92eca-117">Este comando exclui a correção chamada "remediation1" no grupo de recursos "myRG".</span><span class="sxs-lookup"><span data-stu-id="92eca-117">This command deletes the remediation named 'remediation1' in resource group 'myRG'.</span></span> <span data-ttu-id="92eca-118">Se a correção estiver em andamento, ela será cancelada antes de ser excluída.</span><span class="sxs-lookup"><span data-stu-id="92eca-118">If the remediation is in-progress it will be canceled before being deleted.</span></span>

## <span data-ttu-id="92eca-119">OS</span><span class="sxs-lookup"><span data-stu-id="92eca-119">PARAMETERS</span></span>

### <span data-ttu-id="92eca-120">-AllowStop</span><span class="sxs-lookup"><span data-stu-id="92eca-120">-AllowStop</span></span>
<span data-ttu-id="92eca-121">Permita que a correção seja cancelada se estiver em andamento.</span><span class="sxs-lookup"><span data-stu-id="92eca-121">Allow the remediation to be canceled if it is in-progress.</span></span>

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

### <span data-ttu-id="92eca-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="92eca-122">-AsJob</span></span>
<span data-ttu-id="92eca-123">Execute o cmdlet em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="92eca-123">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="92eca-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92eca-124">-DefaultProfile</span></span>
<span data-ttu-id="92eca-125">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="92eca-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="92eca-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="92eca-126">-InputObject</span></span>
<span data-ttu-id="92eca-127">O objeto remediate.</span><span class="sxs-lookup"><span data-stu-id="92eca-127">The Remediation object.</span></span>

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

### <span data-ttu-id="92eca-128">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="92eca-128">-ManagementGroupName</span></span>
<span data-ttu-id="92eca-129">ID do grupo de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="92eca-129">Management group ID.</span></span>

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

### <span data-ttu-id="92eca-130">-Nome</span><span class="sxs-lookup"><span data-stu-id="92eca-130">-Name</span></span>
<span data-ttu-id="92eca-131">Nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="92eca-131">Resource name.</span></span>

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

### <span data-ttu-id="92eca-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="92eca-132">-PassThru</span></span>
<span data-ttu-id="92eca-133">Retorne true se o comando for concluído com êxito.</span><span class="sxs-lookup"><span data-stu-id="92eca-133">Return True if the command completes successfully.</span></span>

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

### <span data-ttu-id="92eca-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92eca-134">-ResourceGroupName</span></span>
<span data-ttu-id="92eca-135">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="92eca-135">Resource group name.</span></span>

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

### <span data-ttu-id="92eca-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="92eca-136">-ResourceId</span></span>
<span data-ttu-id="92eca-137">ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="92eca-137">Resource ID.</span></span>

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

### <span data-ttu-id="92eca-138">-Escopo</span><span class="sxs-lookup"><span data-stu-id="92eca-138">-Scope</span></span>
<span data-ttu-id="92eca-139">Escopo do recurso.</span><span class="sxs-lookup"><span data-stu-id="92eca-139">Scope of the resource.</span></span>
<span data-ttu-id="92eca-140">:.</span><span class="sxs-lookup"><span data-stu-id="92eca-140">E.g.</span></span>
<span data-ttu-id="92eca-141">'/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span><span class="sxs-lookup"><span data-stu-id="92eca-141">'/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span></span>

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

### <span data-ttu-id="92eca-142">-Confirme</span><span class="sxs-lookup"><span data-stu-id="92eca-142">-Confirm</span></span>
<span data-ttu-id="92eca-143">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="92eca-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="92eca-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="92eca-144">-WhatIf</span></span>
<span data-ttu-id="92eca-145">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="92eca-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="92eca-146">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="92eca-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="92eca-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92eca-147">CommonParameters</span></span>
<span data-ttu-id="92eca-148">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92eca-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92eca-149">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="92eca-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92eca-150">SENSORES</span><span class="sxs-lookup"><span data-stu-id="92eca-150">INPUTS</span></span>

### <span data-ttu-id="92eca-151">System. String</span><span class="sxs-lookup"><span data-stu-id="92eca-151">System.String</span></span>

### <span data-ttu-id="92eca-152">Microsoft. Azure. Commands. PolicyInsights. Models. remediation. PSRemediation</span><span class="sxs-lookup"><span data-stu-id="92eca-152">Microsoft.Azure.Commands.PolicyInsights.Models.Remediation.PSRemediation</span></span>

## <span data-ttu-id="92eca-153">EXIBE</span><span class="sxs-lookup"><span data-stu-id="92eca-153">OUTPUTS</span></span>

### <span data-ttu-id="92eca-154">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="92eca-154">System.Boolean</span></span>

## <span data-ttu-id="92eca-155">INFORMA</span><span class="sxs-lookup"><span data-stu-id="92eca-155">NOTES</span></span>

## <span data-ttu-id="92eca-156">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="92eca-156">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/remove-azpolicyremediation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Remove-AzPolicyRemediation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Remove-AzPolicyRemediation.md
ms.openlocfilehash: 969b764be302231f33dda00b32afb79ec04a324e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118199"
---
# <span data-ttu-id="1344e-101">Remove-AzPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="1344e-101">Remove-AzPolicyRemediation</span></span>

## <span data-ttu-id="1344e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1344e-102">SYNOPSIS</span></span>
<span data-ttu-id="1344e-103">Exclui uma correção de política.</span><span class="sxs-lookup"><span data-stu-id="1344e-103">Deletes a policy remediation.</span></span>

## <span data-ttu-id="1344e-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1344e-104">SYNTAX</span></span>

### <span data-ttu-id="1344e-105">ByName (Default)</span><span class="sxs-lookup"><span data-stu-id="1344e-105">ByName (Default)</span></span>
```
Remove-AzPolicyRemediation -Name <String> [-Scope <String>] [-ManagementGroupName <String>]
 [-ResourceGroupName <String>] [-AllowStop] [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1344e-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="1344e-106">ByResourceId</span></span>
```
Remove-AzPolicyRemediation -ResourceId <String> [-AllowStop] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1344e-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="1344e-107">ByInputObject</span></span>
```
Remove-AzPolicyRemediation -InputObject <PSRemediation> [-AllowStop] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1344e-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="1344e-108">DESCRIPTION</span></span>
<span data-ttu-id="1344e-109">O **cmdlet Remove-AzPolicyRemediation** exclui uma correção de política.</span><span class="sxs-lookup"><span data-stu-id="1344e-109">The **Remove-AzPolicyRemediation** cmdlet deletes a policy remediation.</span></span>

## <span data-ttu-id="1344e-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="1344e-110">EXAMPLES</span></span>

### <span data-ttu-id="1344e-111">Exemplo 1: Excluir uma correção de política no escopo do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="1344e-111">Example 1: Delete a policy remediation at resource group scope</span></span>
```
PS C:\> Remove-AzPolicyRemediation -ResourceGroupName "myRG" -Name "remediation1"
```

<span data-ttu-id="1344e-112">Esse comando exclui a correção chamada "correção1" no grupo de recursos "meuRG".</span><span class="sxs-lookup"><span data-stu-id="1344e-112">This command deletes the remediation named 'remediation1' in resource group 'myRG'.</span></span>

### <span data-ttu-id="1344e-113">Exemplo 2: Excluir uma correção de grupo de gerenciamento por meio de uma canalização</span><span class="sxs-lookup"><span data-stu-id="1344e-113">Example 2: Delete a management group remediation via piping</span></span>
```
PS C:\> $remediation = Get-AzPolicyRemediation -ManagementGroupName "mg1" -Name "remediation1"
PS C:\> $remediation | Remove-AzPolicyRemediation -Confirm
```

<span data-ttu-id="1344e-114">Esse comando exclui a correção denominada 'correção1' do grupo de gerenciamento 'mg1'.</span><span class="sxs-lookup"><span data-stu-id="1344e-114">This command deletes the remediation named 'remediation1' from management group 'mg1'.</span></span> <span data-ttu-id="1344e-115">Um prompt de confirmação será apresentado antes de excluir o recurso.</span><span class="sxs-lookup"><span data-stu-id="1344e-115">A confirmation prompt will be presented before deleting the resource.</span></span>

### <span data-ttu-id="1344e-116">Exemplo 3: Cancelar e excluir uma correção de política</span><span class="sxs-lookup"><span data-stu-id="1344e-116">Example 3: Cancel and delete a policy remediation</span></span>
```
PS C:\> Remove-AzPolicyRemediation -ResourceGroupName "myRG" -Name "remediation1" -AllowStop
```

<span data-ttu-id="1344e-117">Esse comando exclui a correção chamada "correção1" no grupo de recursos "meuRG".</span><span class="sxs-lookup"><span data-stu-id="1344e-117">This command deletes the remediation named 'remediation1' in resource group 'myRG'.</span></span> <span data-ttu-id="1344e-118">Se a correção estiver em andamento, ela será cancelada antes de ser excluída.</span><span class="sxs-lookup"><span data-stu-id="1344e-118">If the remediation is in-progress it will be canceled before being deleted.</span></span>

## <span data-ttu-id="1344e-119">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1344e-119">PARAMETERS</span></span>

### <span data-ttu-id="1344e-120">-AllowStop</span><span class="sxs-lookup"><span data-stu-id="1344e-120">-AllowStop</span></span>
<span data-ttu-id="1344e-121">Permita que a correção seja cancelada se ela estiver em andamento.</span><span class="sxs-lookup"><span data-stu-id="1344e-121">Allow the remediation to be canceled if it is in-progress.</span></span>

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

### <span data-ttu-id="1344e-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1344e-122">-AsJob</span></span>
<span data-ttu-id="1344e-123">Executar cmdlet em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="1344e-123">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="1344e-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1344e-124">-DefaultProfile</span></span>
<span data-ttu-id="1344e-125">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1344e-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1344e-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1344e-126">-InputObject</span></span>
<span data-ttu-id="1344e-127">O objeto De correção.</span><span class="sxs-lookup"><span data-stu-id="1344e-127">The Remediation object.</span></span>

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

### <span data-ttu-id="1344e-128">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="1344e-128">-ManagementGroupName</span></span>
<span data-ttu-id="1344e-129">ID do grupo de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="1344e-129">Management group ID.</span></span>

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

### <span data-ttu-id="1344e-130">-Nome</span><span class="sxs-lookup"><span data-stu-id="1344e-130">-Name</span></span>
<span data-ttu-id="1344e-131">Nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="1344e-131">Resource name.</span></span>

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

### <span data-ttu-id="1344e-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1344e-132">-PassThru</span></span>
<span data-ttu-id="1344e-133">Retornar True se o comando for concluído com êxito.</span><span class="sxs-lookup"><span data-stu-id="1344e-133">Return True if the command completes successfully.</span></span>

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

### <span data-ttu-id="1344e-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1344e-134">-ResourceGroupName</span></span>
<span data-ttu-id="1344e-135">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="1344e-135">Resource group name.</span></span>

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

### <span data-ttu-id="1344e-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1344e-136">-ResourceId</span></span>
<span data-ttu-id="1344e-137">ID do Recurso.</span><span class="sxs-lookup"><span data-stu-id="1344e-137">Resource ID.</span></span>

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

### <span data-ttu-id="1344e-138">-Escopo</span><span class="sxs-lookup"><span data-stu-id="1344e-138">-Scope</span></span>
<span data-ttu-id="1344e-139">Escopo do recurso.</span><span class="sxs-lookup"><span data-stu-id="1344e-139">Scope of the resource.</span></span>
<span data-ttu-id="1344e-140">E.g.</span><span class="sxs-lookup"><span data-stu-id="1344e-140">E.g.</span></span>
<span data-ttu-id="1344e-141">'/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span><span class="sxs-lookup"><span data-stu-id="1344e-141">'/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span></span>

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

### <span data-ttu-id="1344e-142">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="1344e-142">-Confirm</span></span>
<span data-ttu-id="1344e-143">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1344e-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1344e-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1344e-144">-WhatIf</span></span>
<span data-ttu-id="1344e-145">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="1344e-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1344e-146">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1344e-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1344e-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1344e-147">CommonParameters</span></span>
<span data-ttu-id="1344e-148">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1344e-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1344e-149">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1344e-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1344e-150">Entradas</span><span class="sxs-lookup"><span data-stu-id="1344e-150">INPUTS</span></span>

### <span data-ttu-id="1344e-151">System.String</span><span class="sxs-lookup"><span data-stu-id="1344e-151">System.String</span></span>

### <span data-ttu-id="1344e-152">Microsoft.Azure.Commands.PolicyInsights.Models.Remediation.PSRemediation</span><span class="sxs-lookup"><span data-stu-id="1344e-152">Microsoft.Azure.Commands.PolicyInsights.Models.Remediation.PSRemediation</span></span>

## <span data-ttu-id="1344e-153">Saídas</span><span class="sxs-lookup"><span data-stu-id="1344e-153">OUTPUTS</span></span>

### <span data-ttu-id="1344e-154">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="1344e-154">System.Boolean</span></span>

## <span data-ttu-id="1344e-155">Notas</span><span class="sxs-lookup"><span data-stu-id="1344e-155">NOTES</span></span>

## <span data-ttu-id="1344e-156">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1344e-156">RELATED LINKS</span></span>

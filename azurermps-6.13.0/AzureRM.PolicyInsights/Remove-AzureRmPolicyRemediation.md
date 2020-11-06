---
external help file: Microsoft.Azure.Commands.PolicyInsights.dll-Help.xml
Module Name: AzureRM.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.policyinsights/remove-azurermpolicyremediation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PolicyInsights/Commands.PolicyInsights/help/Remove-AzureRmPolicyRemediation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PolicyInsights/Commands.PolicyInsights/help/Remove-AzureRmPolicyRemediation.md
ms.openlocfilehash: ec5becd714b034789aeeb8449a63012232c99d5e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602301"
---
# <span data-ttu-id="377fd-101">Remove-AzureRmPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="377fd-101">Remove-AzureRmPolicyRemediation</span></span>

## <span data-ttu-id="377fd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="377fd-102">SYNOPSIS</span></span>
<span data-ttu-id="377fd-103">Exclui uma correção de política.</span><span class="sxs-lookup"><span data-stu-id="377fd-103">Deletes a policy remediation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="377fd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="377fd-104">SYNTAX</span></span>

### <span data-ttu-id="377fd-105">ByName (padrão)</span><span class="sxs-lookup"><span data-stu-id="377fd-105">ByName (Default)</span></span>
```
Remove-AzureRmPolicyRemediation -Name <String> [-Scope <String>] [-ManagementGroupName <String>]
 [-ResourceGroupName <String>] [-AllowStop] [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="377fd-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="377fd-106">ByResourceId</span></span>
```
Remove-AzureRmPolicyRemediation -ResourceId <String> [-AllowStop] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="377fd-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="377fd-107">ByInputObject</span></span>
```
Remove-AzureRmPolicyRemediation -InputObject <PSRemediation> [-AllowStop] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="377fd-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="377fd-108">DESCRIPTION</span></span>
<span data-ttu-id="377fd-109">O cmdlet **Remove-AzureRmPolicyRemediation** exclui uma correção de política.</span><span class="sxs-lookup"><span data-stu-id="377fd-109">The **Remove-AzureRmPolicyRemediation** cmdlet deletes a policy remediation.</span></span>

## <span data-ttu-id="377fd-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="377fd-110">EXAMPLES</span></span>

### <span data-ttu-id="377fd-111">Exemplo 1: excluir uma correção de política no escopo do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="377fd-111">Example 1: Delete a policy remediation at resource group scope</span></span>
```
PS C:\> Remove-AzureRmPolicyRemediation -ResourceGroupName "myRG" -Name "remediation1"
```

<span data-ttu-id="377fd-112">Este comando exclui a correção chamada "remediation1" no grupo de recursos "myRG".</span><span class="sxs-lookup"><span data-stu-id="377fd-112">This command deletes the remediation named 'remediation1' in resource group 'myRG'.</span></span>

### <span data-ttu-id="377fd-113">Exemplo 2: excluir uma correção de grupo de gerenciamento via tubulação</span><span class="sxs-lookup"><span data-stu-id="377fd-113">Example 2: Delete a management group remediation via piping</span></span>
```
PS C:\> $remediation = Get-AzureRmPolicyRemediation -ManagementGroupName "mg1" -Name "remediation1"
PS C:\> $remediation | Remove-AzureRmPolicyRemediation -Confirm
```

<span data-ttu-id="377fd-114">Este comando exclui a correção chamada "remediation1" do grupo de gerenciamento "MG1".</span><span class="sxs-lookup"><span data-stu-id="377fd-114">This command deletes the remediation named 'remediation1' from management group 'mg1'.</span></span> <span data-ttu-id="377fd-115">Um prompt de confirmação será apresentado antes da exclusão do recurso.</span><span class="sxs-lookup"><span data-stu-id="377fd-115">A confirmation prompt will be presented before deleting the resource.</span></span>

### <span data-ttu-id="377fd-116">Exemplo 3: cancelar e excluir uma remediação de política</span><span class="sxs-lookup"><span data-stu-id="377fd-116">Example 3: Cancel and delete a policy remediation</span></span>
```
PS C:\> Remove-AzureRmPolicyRemediation -ResourceGroupName "myRG" -Name "remediation1" -AllowStop
```

<span data-ttu-id="377fd-117">Este comando exclui a correção chamada "remediation1" no grupo de recursos "myRG".</span><span class="sxs-lookup"><span data-stu-id="377fd-117">This command deletes the remediation named 'remediation1' in resource group 'myRG'.</span></span> <span data-ttu-id="377fd-118">Se a correção estiver em andamento, ela será cancelada antes de ser excluída.</span><span class="sxs-lookup"><span data-stu-id="377fd-118">If the remediation is in-progress it will be canceled before being deleted.</span></span>

## <span data-ttu-id="377fd-119">OS</span><span class="sxs-lookup"><span data-stu-id="377fd-119">PARAMETERS</span></span>

### <span data-ttu-id="377fd-120">-AllowStop</span><span class="sxs-lookup"><span data-stu-id="377fd-120">-AllowStop</span></span>
<span data-ttu-id="377fd-121">Permita que a correção seja cancelada se estiver em andamento.</span><span class="sxs-lookup"><span data-stu-id="377fd-121">Allow the remediation to be canceled if it is in-progress.</span></span>

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

### <span data-ttu-id="377fd-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="377fd-122">-AsJob</span></span>
<span data-ttu-id="377fd-123">Execute o cmdlet em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="377fd-123">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="377fd-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="377fd-124">-DefaultProfile</span></span>
<span data-ttu-id="377fd-125">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="377fd-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="377fd-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="377fd-126">-InputObject</span></span>
<span data-ttu-id="377fd-127">O objeto remediate.</span><span class="sxs-lookup"><span data-stu-id="377fd-127">The Remediation object.</span></span>

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

### <span data-ttu-id="377fd-128">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="377fd-128">-ManagementGroupName</span></span>
<span data-ttu-id="377fd-129">ID do grupo de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="377fd-129">Management group ID.</span></span>

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

### <span data-ttu-id="377fd-130">-Nome</span><span class="sxs-lookup"><span data-stu-id="377fd-130">-Name</span></span>
<span data-ttu-id="377fd-131">Nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="377fd-131">Resource name.</span></span>

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

### <span data-ttu-id="377fd-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="377fd-132">-PassThru</span></span>
<span data-ttu-id="377fd-133">Retorne true se o comando for concluído com êxito.</span><span class="sxs-lookup"><span data-stu-id="377fd-133">Return True if the command completes successfully.</span></span>

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

### <span data-ttu-id="377fd-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="377fd-134">-ResourceGroupName</span></span>
<span data-ttu-id="377fd-135">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="377fd-135">Resource group name.</span></span>

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

### <span data-ttu-id="377fd-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="377fd-136">-ResourceId</span></span>
<span data-ttu-id="377fd-137">ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="377fd-137">Resource ID.</span></span>

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

### <span data-ttu-id="377fd-138">-Escopo</span><span class="sxs-lookup"><span data-stu-id="377fd-138">-Scope</span></span>
<span data-ttu-id="377fd-139">Escopo do recurso.</span><span class="sxs-lookup"><span data-stu-id="377fd-139">Scope of the resource.</span></span>
<span data-ttu-id="377fd-140">:.</span><span class="sxs-lookup"><span data-stu-id="377fd-140">E.g.</span></span>
<span data-ttu-id="377fd-141">'/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span><span class="sxs-lookup"><span data-stu-id="377fd-141">'/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span></span>

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

### <span data-ttu-id="377fd-142">-Confirme</span><span class="sxs-lookup"><span data-stu-id="377fd-142">-Confirm</span></span>
<span data-ttu-id="377fd-143">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="377fd-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="377fd-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="377fd-144">-WhatIf</span></span>
<span data-ttu-id="377fd-145">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="377fd-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="377fd-146">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="377fd-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="377fd-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="377fd-147">CommonParameters</span></span>
<span data-ttu-id="377fd-148">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="377fd-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="377fd-149">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="377fd-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="377fd-150">SENSORES</span><span class="sxs-lookup"><span data-stu-id="377fd-150">INPUTS</span></span>

### <span data-ttu-id="377fd-151">System. String</span><span class="sxs-lookup"><span data-stu-id="377fd-151">System.String</span></span>

### <span data-ttu-id="377fd-152">Microsoft. Azure. Commands. PolicyInsights. Models. remediation. PSRemediation</span><span class="sxs-lookup"><span data-stu-id="377fd-152">Microsoft.Azure.Commands.PolicyInsights.Models.Remediation.PSRemediation</span></span>

## <span data-ttu-id="377fd-153">EXIBE</span><span class="sxs-lookup"><span data-stu-id="377fd-153">OUTPUTS</span></span>

### <span data-ttu-id="377fd-154">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="377fd-154">System.Boolean</span></span>

## <span data-ttu-id="377fd-155">INFORMA</span><span class="sxs-lookup"><span data-stu-id="377fd-155">NOTES</span></span>

## <span data-ttu-id="377fd-156">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="377fd-156">RELATED LINKS</span></span>

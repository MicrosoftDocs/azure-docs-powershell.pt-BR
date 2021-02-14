---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 0C35E679-B991-49A8-890F-C8DAB68A8240
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/remove-azoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsWorkspace.md
ms.openlocfilehash: d02338c34584a68ece2ad3a90887a765f8142347
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117296"
---
# <span data-ttu-id="824c8-101">Remove-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="824c8-101">Remove-AzOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="824c8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="824c8-102">SYNOPSIS</span></span>
<span data-ttu-id="824c8-103">Remove um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="824c8-103">Removes a workspace.</span></span>

## <span data-ttu-id="824c8-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="824c8-104">SYNTAX</span></span>

```
Remove-AzOperationalInsightsWorkspace [-ResourceGroupName] <String> [-Name] <String> [-ForceDelete] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="824c8-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="824c8-105">DESCRIPTION</span></span>
<span data-ttu-id="824c8-106">O cmdlet **Remove-AzOperationalInsightsWorkspace** exclui um espaço de trabalho existente.</span><span class="sxs-lookup"><span data-stu-id="824c8-106">The **Remove-AzOperationalInsightsWorkspace** cmdlet deletes an existing workspace.</span></span>
<span data-ttu-id="824c8-107">Se esse espaço de trabalho foi vinculado a uma conta existente por meio do parâmetro *CustomerId* no momento da criação, a conta original não será excluída no portal de Insights Operacionais.</span><span class="sxs-lookup"><span data-stu-id="824c8-107">If this workspace was linked to an existing account via the *CustomerId* parameter at creation time the original account is not deleted in the Operational Insights portal.</span></span>

## <span data-ttu-id="824c8-108">Exemplos</span><span class="sxs-lookup"><span data-stu-id="824c8-108">EXAMPLES</span></span>

### <span data-ttu-id="824c8-109">Exemplo 1: Remover um espaço de trabalho por nome</span><span class="sxs-lookup"><span data-stu-id="824c8-109">Example 1: Remove a workspace by name</span></span>
```
PS C:\>Remove-AzOperationalInsightsWorkspace -ResourceGroupName "ContosResourceGroup" -Name "MyWorkspace"
```

<span data-ttu-id="824c8-110">Esse comando remove o espaço de trabalho chamado MyWorkspace do grupo de recursos chamado ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="824c8-110">This command removes the workspace named MyWorkspace from the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="824c8-111">Exemplo 2: Remover um espaço de trabalho usando o pipeline e sem confirmação</span><span class="sxs-lookup"><span data-stu-id="824c8-111">Example 2: Remove a workspace by using the pipeline and without confirmation</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosResourceGroup" -Name "MyWorkspace" | Remove-AzOperationalInsightsWorkspace -Force
```

<span data-ttu-id="824c8-112">Esse comando usa o cmdlet Get-AzOperationalInsightsWorkspace para obter o espaço de trabalho chamado MyWorkspace e passa-o para o cmdlet **Remove-AzOperationalInsightsWorkspace** usando o operador de pipeline para removê-lo.</span><span class="sxs-lookup"><span data-stu-id="824c8-112">This command uses the Get-AzOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkspace, and then passes it to the **Remove-AzOperationalInsightsWorkspace** cmdlet by using the pipeline operator to remove it.</span></span>
<span data-ttu-id="824c8-113">Como o *parâmetro Forçar* é especificado, o comando não solicita antes de remover o espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="824c8-113">Since the *Force* parameter is specified, the command does not prompt you before removing the workspace.</span></span>

### <span data-ttu-id="824c8-114">Exemplo 3: forçar a exclusão de espaço de trabalho (não pode ser recuperado)</span><span class="sxs-lookup"><span data-stu-id="824c8-114">Example 3: Force delete workspace (cannot be recovered)</span></span>
```
PS C:\> $workspace = New-AzOperationalInsightsWorkspace -ResourceGroupName $rgname -Name $wsname -Location $wslocation
PS C:\> $workspace | Remove-AzOperationalInsightsWorkspace -ForceDelete
```

<span data-ttu-id="824c8-115">Forçar a exclusão de um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="824c8-115">Force delete a workspace.</span></span>

## <span data-ttu-id="824c8-116">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="824c8-116">PARAMETERS</span></span>

### <span data-ttu-id="824c8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="824c8-117">-DefaultProfile</span></span>
<span data-ttu-id="824c8-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="824c8-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="824c8-119">-Forçar</span><span class="sxs-lookup"><span data-stu-id="824c8-119">-Force</span></span>
<span data-ttu-id="824c8-120">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="824c8-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="824c8-121">-ForceDelete</span><span class="sxs-lookup"><span data-stu-id="824c8-121">-ForceDelete</span></span>
<span data-ttu-id="824c8-122">Forçar a exclusão do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="824c8-122">Force delete workspace.</span></span>

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

### <span data-ttu-id="824c8-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="824c8-123">-Name</span></span>
<span data-ttu-id="824c8-124">Especifica o nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="824c8-124">Specifies the name of the workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="824c8-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="824c8-125">-ResourceGroupName</span></span>
<span data-ttu-id="824c8-126">Especifica o nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="824c8-126">Specifies the name of an Azure resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="824c8-127">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="824c8-127">-Confirm</span></span>
<span data-ttu-id="824c8-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="824c8-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="824c8-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="824c8-129">-WhatIf</span></span>
<span data-ttu-id="824c8-130">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="824c8-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="824c8-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="824c8-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="824c8-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="824c8-132">CommonParameters</span></span>
<span data-ttu-id="824c8-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="824c8-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="824c8-134">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="824c8-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="824c8-135">Entradas</span><span class="sxs-lookup"><span data-stu-id="824c8-135">INPUTS</span></span>

### <span data-ttu-id="824c8-136">System.String</span><span class="sxs-lookup"><span data-stu-id="824c8-136">System.String</span></span>

## <span data-ttu-id="824c8-137">Saídas</span><span class="sxs-lookup"><span data-stu-id="824c8-137">OUTPUTS</span></span>

### <span data-ttu-id="824c8-138">System.Void</span><span class="sxs-lookup"><span data-stu-id="824c8-138">System.Void</span></span>

## <span data-ttu-id="824c8-139">Notas</span><span class="sxs-lookup"><span data-stu-id="824c8-139">NOTES</span></span>

## <span data-ttu-id="824c8-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="824c8-140">RELATED LINKS</span></span>

[<span data-ttu-id="824c8-141">Cmdlets de Insights Operacionais do Azure</span><span class="sxs-lookup"><span data-stu-id="824c8-141">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)

[<span data-ttu-id="824c8-142">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="824c8-142">Get-AzOperationalInsightsWorkspace</span></span>](./Get-AzOperationalInsightsWorkspace.md)



---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 92261663-CF50-4EBD-85D2-C2E254F39B41
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/remove-azoperationalinsightsstorageinsight
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsStorageInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsStorageInsight.md
ms.openlocfilehash: 7eece12130095889c5da574a4d0a3ec8d0b0bed2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890203"
---
# <span data-ttu-id="65733-101">Remove-AzOperationalInsightsStorageInsight</span><span class="sxs-lookup"><span data-stu-id="65733-101">Remove-AzOperationalInsightsStorageInsight</span></span>

## <span data-ttu-id="65733-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="65733-102">SYNOPSIS</span></span>
<span data-ttu-id="65733-103">Remove um Storage Insight.</span><span class="sxs-lookup"><span data-stu-id="65733-103">Removes a Storage Insight.</span></span>

## <span data-ttu-id="65733-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="65733-104">SYNTAX</span></span>

### <span data-ttu-id="65733-105">ByWorkspaceName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="65733-105">ByWorkspaceName (Default)</span></span>
```
Remove-AzOperationalInsightsStorageInsight [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65733-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="65733-106">ByWorkspaceObject</span></span>
```
Remove-AzOperationalInsightsStorageInsight [-Workspace] <PSWorkspace> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="65733-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="65733-107">DESCRIPTION</span></span>
<span data-ttu-id="65733-108">O cmdlet **Remove-AzOperationalInsightsStorageInsight** exclui um Storage Insight de um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="65733-108">The **Remove-AzOperationalInsightsStorageInsight** cmdlet deletes a Storage Insight from a workspace.</span></span>

## <span data-ttu-id="65733-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="65733-109">EXAMPLES</span></span>

### <span data-ttu-id="65733-110">Exemplo 1: Remover um Insight de Armazenamento pelo nome</span><span class="sxs-lookup"><span data-stu-id="65733-110">Example 1: Remove a Storage Insight by name</span></span>
```
PS C:\>Remove-AzOperationalInsightsStorageInsight -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "MyWorkspace" -Name "MyStorageInsight"
```

<span data-ttu-id="65733-111">Este comando remove o Storage Insight chamado MyStorageInsight do espaço de trabalho chamado MyWorkspace no grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="65733-111">This command removes the Storage Insight named MyStorageInsight from the workspace named MyWorkspace in the specified resource group.</span></span>
<span data-ttu-id="65733-112">O comando não especifica o parâmetro *Force,* portanto, solicita a confirmação antes de remover o Storage Insight.</span><span class="sxs-lookup"><span data-stu-id="65733-112">The command does not specify the *Force* parameter, so it prompts you for confirmation before removing the Storage Insight.</span></span>

### <span data-ttu-id="65733-113">Exemplo 2: Remover um Insight de Armazenamento sem confirmação</span><span class="sxs-lookup"><span data-stu-id="65733-113">Example 2: Remove a Storage Insight without confirmation</span></span>
```
PS C:\>$Workspace = Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"

PS C:\>Remove-AzOperationalInsightsStorageInsight -Workspace $Workspace -Name "MyStorageInsight" -Force
```

<span data-ttu-id="65733-114">O primeiro comando usa o cmdlet Get-AzOperationalInsightsWorkspace para obter o espaço de trabalho chamado MyWorkspace e, em seguida, o armazena na variável $Workspace. O segundo comando remove o insight de armazenamento chamado MyStorageInsight $Workspace sem solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="65733-114">The first command uses the Get-AzOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkspace, and then stores it in the $Workspace variable.The second command removes the storage insight named MyStorageInsight from $Workspace without prompting you for confirmation.</span></span>

## <span data-ttu-id="65733-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="65733-115">PARAMETERS</span></span>

### <span data-ttu-id="65733-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65733-116">-DefaultProfile</span></span>
<span data-ttu-id="65733-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="65733-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="65733-118">-Force</span><span class="sxs-lookup"><span data-stu-id="65733-118">-Force</span></span>
<span data-ttu-id="65733-119">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="65733-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="65733-120">-Name</span><span class="sxs-lookup"><span data-stu-id="65733-120">-Name</span></span>
<span data-ttu-id="65733-121">Especifica o nome do Storage Insight.</span><span class="sxs-lookup"><span data-stu-id="65733-121">Specifies the name of the Storage Insight.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65733-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65733-122">-ResourceGroupName</span></span>
<span data-ttu-id="65733-123">Especifica o nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="65733-123">Specifies the name of an Azure resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65733-124">-Workspace</span><span class="sxs-lookup"><span data-stu-id="65733-124">-Workspace</span></span>
<span data-ttu-id="65733-125">Especifica o espaço de trabalho que contém o Storage Insight.</span><span class="sxs-lookup"><span data-stu-id="65733-125">Specifies the workspace that contains the Storage Insight.</span></span>

```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace
Parameter Sets: ByWorkspaceObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="65733-126">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="65733-126">-WorkspaceName</span></span>
<span data-ttu-id="65733-127">Especifica o nome do espaço de trabalho que contém o Storage Insight.</span><span class="sxs-lookup"><span data-stu-id="65733-127">Specifies the name of the workspace that contains the Storage Insight.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65733-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="65733-128">-Confirm</span></span>
<span data-ttu-id="65733-129">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="65733-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="65733-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65733-130">-WhatIf</span></span>
<span data-ttu-id="65733-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="65733-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="65733-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="65733-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="65733-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65733-133">CommonParameters</span></span>
<span data-ttu-id="65733-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65733-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65733-135">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="65733-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65733-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="65733-136">INPUTS</span></span>

### <span data-ttu-id="65733-137">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="65733-137">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="65733-138">System.String</span><span class="sxs-lookup"><span data-stu-id="65733-138">System.String</span></span>

## <span data-ttu-id="65733-139">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="65733-139">OUTPUTS</span></span>

### <span data-ttu-id="65733-140">System.Void</span><span class="sxs-lookup"><span data-stu-id="65733-140">System.Void</span></span>

## <span data-ttu-id="65733-141">NOTES</span><span class="sxs-lookup"><span data-stu-id="65733-141">NOTES</span></span>

## <span data-ttu-id="65733-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="65733-142">RELATED LINKS</span></span>

[<span data-ttu-id="65733-143">Cmdlets do Insights Operacionais do Azure</span><span class="sxs-lookup"><span data-stu-id="65733-143">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)

[<span data-ttu-id="65733-144">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="65733-144">Get-AzOperationalInsightsWorkspace</span></span>](./Get-AzOperationalInsightsWorkspace.md)



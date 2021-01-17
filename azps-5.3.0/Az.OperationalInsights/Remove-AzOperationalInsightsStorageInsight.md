---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 92261663-CF50-4EBD-85D2-C2E254F39B41
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/remove-azoperationalinsightsstorageinsight
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsStorageInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsStorageInsight.md
ms.openlocfilehash: ac9e061fea8c6d7737eb268feec225dff0b0924d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98434530"
---
# <span data-ttu-id="ce8e7-101">Remove-AzOperationalInsightsStorageInsight</span><span class="sxs-lookup"><span data-stu-id="ce8e7-101">Remove-AzOperationalInsightsStorageInsight</span></span>

## <span data-ttu-id="ce8e7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ce8e7-102">SYNOPSIS</span></span>
<span data-ttu-id="ce8e7-103">Remove uma percepção do armazenamento.</span><span class="sxs-lookup"><span data-stu-id="ce8e7-103">Removes a Storage Insight.</span></span>

## <span data-ttu-id="ce8e7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ce8e7-104">SYNTAX</span></span>

### <span data-ttu-id="ce8e7-105">ByWorkspaceName (padrão)</span><span class="sxs-lookup"><span data-stu-id="ce8e7-105">ByWorkspaceName (Default)</span></span>
```
Remove-AzOperationalInsightsStorageInsight [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ce8e7-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="ce8e7-106">ByWorkspaceObject</span></span>
```
Remove-AzOperationalInsightsStorageInsight [-Workspace] <PSWorkspace> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ce8e7-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ce8e7-107">DESCRIPTION</span></span>
<span data-ttu-id="ce8e7-108">O cmdlet **Remove-AzOperationalInsightsStorageInsight** exclui uma percepção do armazenamento de um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="ce8e7-108">The **Remove-AzOperationalInsightsStorageInsight** cmdlet deletes a Storage Insight from a workspace.</span></span>

## <span data-ttu-id="ce8e7-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ce8e7-109">EXAMPLES</span></span>

### <span data-ttu-id="ce8e7-110">Exemplo 1: remover uma visão de armazenamento por nome</span><span class="sxs-lookup"><span data-stu-id="ce8e7-110">Example 1: Remove a Storage Insight by name</span></span>
```
PS C:\>Remove-AzOperationalInsightsStorageInsight -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "MyWorkspace" -Name "MyStorageInsight"
```

<span data-ttu-id="ce8e7-111">Esse comando Remove a percepção do armazenamento chamada MyStorageInsight do espaço de trabalho chamado MyWorkspace no grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="ce8e7-111">This command removes the Storage Insight named MyStorageInsight from the workspace named MyWorkspace in the specified resource group.</span></span>
<span data-ttu-id="ce8e7-112">O comando não especifica o parâmetro *Force* ; portanto, ele solicita confirmação antes de remover a percepção do armazenamento.</span><span class="sxs-lookup"><span data-stu-id="ce8e7-112">The command does not specify the *Force* parameter, so it prompts you for confirmation before removing the Storage Insight.</span></span>

### <span data-ttu-id="ce8e7-113">Exemplo 2: remover uma visão de armazenamento sem confirmação</span><span class="sxs-lookup"><span data-stu-id="ce8e7-113">Example 2: Remove a Storage Insight without confirmation</span></span>
```
PS C:\>$Workspace = Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"

PS C:\>Remove-AzOperationalInsightsStorageInsight -Workspace $Workspace -Name "MyStorageInsight" -Force
```

<span data-ttu-id="ce8e7-114">O primeiro comando usa o cmdlet Get-AzOperationalInsightsWorkspace para obter o espaço de trabalho chamado MyWorkspace e, em seguida, armazena-o na variável $Workspace. O segundo comando Remove a percepção do armazenamento chamada MyStorageInsight de $Workspace sem solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="ce8e7-114">The first command uses the Get-AzOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkspace, and then stores it in the $Workspace variable.The second command removes the storage insight named MyStorageInsight from $Workspace without prompting you for confirmation.</span></span>

## <span data-ttu-id="ce8e7-115">OS</span><span class="sxs-lookup"><span data-stu-id="ce8e7-115">PARAMETERS</span></span>

### <span data-ttu-id="ce8e7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce8e7-116">-DefaultProfile</span></span>
<span data-ttu-id="ce8e7-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="ce8e7-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ce8e7-118">-Force</span><span class="sxs-lookup"><span data-stu-id="ce8e7-118">-Force</span></span>
<span data-ttu-id="ce8e7-119">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="ce8e7-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ce8e7-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="ce8e7-120">-Name</span></span>
<span data-ttu-id="ce8e7-121">Especifica o nome da informação sobre o armazenamento.</span><span class="sxs-lookup"><span data-stu-id="ce8e7-121">Specifies the name of the Storage Insight.</span></span>

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

### <span data-ttu-id="ce8e7-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce8e7-122">-ResourceGroupName</span></span>
<span data-ttu-id="ce8e7-123">Especifica o nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="ce8e7-123">Specifies the name of an Azure resource group.</span></span>

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

### <span data-ttu-id="ce8e7-124">-Espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="ce8e7-124">-Workspace</span></span>
<span data-ttu-id="ce8e7-125">Especifica o espaço de trabalho que contém a percepção do armazenamento.</span><span class="sxs-lookup"><span data-stu-id="ce8e7-125">Specifies the workspace that contains the Storage Insight.</span></span>

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

### <span data-ttu-id="ce8e7-126">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="ce8e7-126">-WorkspaceName</span></span>
<span data-ttu-id="ce8e7-127">Especifica o nome do espaço de trabalho que contém a percepção do armazenamento.</span><span class="sxs-lookup"><span data-stu-id="ce8e7-127">Specifies the name of the workspace that contains the Storage Insight.</span></span>

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

### <span data-ttu-id="ce8e7-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="ce8e7-128">-Confirm</span></span>
<span data-ttu-id="ce8e7-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ce8e7-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ce8e7-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ce8e7-130">-WhatIf</span></span>
<span data-ttu-id="ce8e7-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ce8e7-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ce8e7-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ce8e7-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ce8e7-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce8e7-133">CommonParameters</span></span>
<span data-ttu-id="ce8e7-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ce8e7-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce8e7-135">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ce8e7-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce8e7-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ce8e7-136">INPUTS</span></span>

### <span data-ttu-id="ce8e7-137">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="ce8e7-137">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="ce8e7-138">System. String</span><span class="sxs-lookup"><span data-stu-id="ce8e7-138">System.String</span></span>

## <span data-ttu-id="ce8e7-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ce8e7-139">OUTPUTS</span></span>

### <span data-ttu-id="ce8e7-140">System. void</span><span class="sxs-lookup"><span data-stu-id="ce8e7-140">System.Void</span></span>

## <span data-ttu-id="ce8e7-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ce8e7-141">NOTES</span></span>

## <span data-ttu-id="ce8e7-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ce8e7-142">RELATED LINKS</span></span>

[<span data-ttu-id="ce8e7-143">Cmdlets do Azure Operational insights</span><span class="sxs-lookup"><span data-stu-id="ce8e7-143">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)

[<span data-ttu-id="ce8e7-144">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="ce8e7-144">Get-AzOperationalInsightsWorkspace</span></span>](./Get-AzOperationalInsightsWorkspace.md)



---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 92261663-CF50-4EBD-85D2-C2E254F39B41
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/remove-azoperationalinsightsstorageinsight
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsStorageInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsStorageInsight.md
ms.openlocfilehash: ac9e061fea8c6d7737eb268feec225dff0b0924d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114069"
---
# <span data-ttu-id="77159-101">Remove-AzOperationalInsightsStorageInsight</span><span class="sxs-lookup"><span data-stu-id="77159-101">Remove-AzOperationalInsightsStorageInsight</span></span>

## <span data-ttu-id="77159-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="77159-102">SYNOPSIS</span></span>
<span data-ttu-id="77159-103">Remove uma Visão de Armazenamento.</span><span class="sxs-lookup"><span data-stu-id="77159-103">Removes a Storage Insight.</span></span>

## <span data-ttu-id="77159-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="77159-104">SYNTAX</span></span>

### <span data-ttu-id="77159-105">ByWorkspaceName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="77159-105">ByWorkspaceName (Default)</span></span>
```
Remove-AzOperationalInsightsStorageInsight [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="77159-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="77159-106">ByWorkspaceObject</span></span>
```
Remove-AzOperationalInsightsStorageInsight [-Workspace] <PSWorkspace> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="77159-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="77159-107">DESCRIPTION</span></span>
<span data-ttu-id="77159-108">O cmdlet **Remove-AzOperationalInsightsStorageInsight** exclui uma Visão de Armazenamento de um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="77159-108">The **Remove-AzOperationalInsightsStorageInsight** cmdlet deletes a Storage Insight from a workspace.</span></span>

## <span data-ttu-id="77159-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="77159-109">EXAMPLES</span></span>

### <span data-ttu-id="77159-110">Exemplo 1: Remover uma Visão de Armazenamento por nome</span><span class="sxs-lookup"><span data-stu-id="77159-110">Example 1: Remove a Storage Insight by name</span></span>
```
PS C:\>Remove-AzOperationalInsightsStorageInsight -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "MyWorkspace" -Name "MyStorageInsight"
```

<span data-ttu-id="77159-111">Esse comando remove o Insight de Armazenamento chamado MyStorageInsight do espaço de trabalho chamado MyWorkspace no grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="77159-111">This command removes the Storage Insight named MyStorageInsight from the workspace named MyWorkspace in the specified resource group.</span></span>
<span data-ttu-id="77159-112">O comando não especifica o parâmetro *Forçar,* portanto, ele solicita que você confirme antes de remover o Insight de Armazenamento.</span><span class="sxs-lookup"><span data-stu-id="77159-112">The command does not specify the *Force* parameter, so it prompts you for confirmation before removing the Storage Insight.</span></span>

### <span data-ttu-id="77159-113">Exemplo 2: Remover uma Visão de Armazenamento sem confirmação</span><span class="sxs-lookup"><span data-stu-id="77159-113">Example 2: Remove a Storage Insight without confirmation</span></span>
```
PS C:\>$Workspace = Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"

PS C:\>Remove-AzOperationalInsightsStorageInsight -Workspace $Workspace -Name "MyStorageInsight" -Force
```

<span data-ttu-id="77159-114">O primeiro comando usa o cmdlet Get-AzOperationalInsightsWorkspace para obter o espaço de trabalho chamado MyWorkspace e, em seguida, armazena-o na variável $Workspace dados. O segundo comando remove as informações de armazenamento chamadas MyStorageInsight $Workspace sem solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="77159-114">The first command uses the Get-AzOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkspace, and then stores it in the $Workspace variable.The second command removes the storage insight named MyStorageInsight from $Workspace without prompting you for confirmation.</span></span>

## <span data-ttu-id="77159-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="77159-115">PARAMETERS</span></span>

### <span data-ttu-id="77159-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77159-116">-DefaultProfile</span></span>
<span data-ttu-id="77159-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="77159-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="77159-118">-Forçar</span><span class="sxs-lookup"><span data-stu-id="77159-118">-Force</span></span>
<span data-ttu-id="77159-119">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="77159-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="77159-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="77159-120">-Name</span></span>
<span data-ttu-id="77159-121">Especifica o nome do Insights de Armazenamento.</span><span class="sxs-lookup"><span data-stu-id="77159-121">Specifies the name of the Storage Insight.</span></span>

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

### <span data-ttu-id="77159-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77159-122">-ResourceGroupName</span></span>
<span data-ttu-id="77159-123">Especifica o nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="77159-123">Specifies the name of an Azure resource group.</span></span>

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

### <span data-ttu-id="77159-124">-Espaço de Trabalho</span><span class="sxs-lookup"><span data-stu-id="77159-124">-Workspace</span></span>
<span data-ttu-id="77159-125">Especifica o espaço de trabalho que contém o Insights de Armazenamento.</span><span class="sxs-lookup"><span data-stu-id="77159-125">Specifies the workspace that contains the Storage Insight.</span></span>

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

### <span data-ttu-id="77159-126">-NomedoEspacial de Trabalho</span><span class="sxs-lookup"><span data-stu-id="77159-126">-WorkspaceName</span></span>
<span data-ttu-id="77159-127">Especifica o nome do espaço de trabalho que contém o Insights de Armazenamento.</span><span class="sxs-lookup"><span data-stu-id="77159-127">Specifies the name of the workspace that contains the Storage Insight.</span></span>

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

### <span data-ttu-id="77159-128">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="77159-128">-Confirm</span></span>
<span data-ttu-id="77159-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="77159-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="77159-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="77159-130">-WhatIf</span></span>
<span data-ttu-id="77159-131">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="77159-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="77159-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="77159-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="77159-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77159-133">CommonParameters</span></span>
<span data-ttu-id="77159-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77159-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77159-135">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="77159-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77159-136">Entradas</span><span class="sxs-lookup"><span data-stu-id="77159-136">INPUTS</span></span>

### <span data-ttu-id="77159-137">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="77159-137">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="77159-138">System.String</span><span class="sxs-lookup"><span data-stu-id="77159-138">System.String</span></span>

## <span data-ttu-id="77159-139">Saídas</span><span class="sxs-lookup"><span data-stu-id="77159-139">OUTPUTS</span></span>

### <span data-ttu-id="77159-140">System.Void</span><span class="sxs-lookup"><span data-stu-id="77159-140">System.Void</span></span>

## <span data-ttu-id="77159-141">Notas</span><span class="sxs-lookup"><span data-stu-id="77159-141">NOTES</span></span>

## <span data-ttu-id="77159-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="77159-142">RELATED LINKS</span></span>

[<span data-ttu-id="77159-143">Cmdlets de Insights Operacionais do Azure</span><span class="sxs-lookup"><span data-stu-id="77159-143">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)

[<span data-ttu-id="77159-144">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="77159-144">Get-AzOperationalInsightsWorkspace</span></span>](./Get-AzOperationalInsightsWorkspace.md)



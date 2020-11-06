---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 92261663-CF50-4EBD-85D2-C2E254F39B41
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/remove-azurermoperationalinsightsstorageinsight
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Remove-AzureRmOperationalInsightsStorageInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Remove-AzureRmOperationalInsightsStorageInsight.md
ms.openlocfilehash: 726386fb4a455b3daab314e5f61d33122592dcf8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430106"
---
# <span data-ttu-id="b91a6-101">Remove-AzureRmOperationalInsightsStorageInsight</span><span class="sxs-lookup"><span data-stu-id="b91a6-101">Remove-AzureRmOperationalInsightsStorageInsight</span></span>

## <span data-ttu-id="b91a6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b91a6-102">SYNOPSIS</span></span>
<span data-ttu-id="b91a6-103">Remove uma percepção do armazenamento.</span><span class="sxs-lookup"><span data-stu-id="b91a6-103">Removes a Storage Insight.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b91a6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b91a6-104">SYNTAX</span></span>

### <span data-ttu-id="b91a6-105">ByWorkspaceName (padrão)</span><span class="sxs-lookup"><span data-stu-id="b91a6-105">ByWorkspaceName (Default)</span></span>
```
Remove-AzureRmOperationalInsightsStorageInsight [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b91a6-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="b91a6-106">ByWorkspaceObject</span></span>
```
Remove-AzureRmOperationalInsightsStorageInsight [-Workspace] <PSWorkspace> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b91a6-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b91a6-107">DESCRIPTION</span></span>
<span data-ttu-id="b91a6-108">O cmdlet **Remove-AzureRmOperationalInsightsStorageInsight** exclui uma percepção do armazenamento de um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="b91a6-108">The **Remove-AzureRmOperationalInsightsStorageInsight** cmdlet deletes a Storage Insight from a workspace.</span></span>

## <span data-ttu-id="b91a6-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b91a6-109">EXAMPLES</span></span>

### <span data-ttu-id="b91a6-110">Exemplo 1: remover uma visão de armazenamento por nome</span><span class="sxs-lookup"><span data-stu-id="b91a6-110">Example 1: Remove a Storage Insight by name</span></span>
```
PS C:\>Remove-AzureRmOperationalInsightsStorageInsight -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "MyWorkspace" -Name "MyStorageInsight"
```

<span data-ttu-id="b91a6-111">Esse comando Remove a percepção do armazenamento chamada MyStorageInsight do espaço de trabalho chamado MyWorkspace no grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="b91a6-111">This command removes the Storage Insight named MyStorageInsight from the workspace named MyWorkspace in the specified resource group.</span></span>
<span data-ttu-id="b91a6-112">O comando não especifica o parâmetro *Force* ; portanto, ele solicita confirmação antes de remover a percepção do armazenamento.</span><span class="sxs-lookup"><span data-stu-id="b91a6-112">The command does not specify the *Force* parameter, so it prompts you for confirmation before removing the Storage Insight.</span></span>

### <span data-ttu-id="b91a6-113">Exemplo 2: remover uma visão de armazenamento sem confirmação</span><span class="sxs-lookup"><span data-stu-id="b91a6-113">Example 2: Remove a Storage Insight without confirmation</span></span>
```
PS C:\>$Workspace = Get-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"

PS C:\>Remove-AzureRmOperationalInsightsStorageInsight -Workspace $Workspace -Name "MyStorageInsight" -Force
```

<span data-ttu-id="b91a6-114">O primeiro comando usa o cmdlet Get-AzureRmOperationalInsightsWorkspace para obter o espaço de trabalho chamado MyWorkspace e, em seguida, armazena-o na variável $Workspace. O segundo comando Remove a percepção do armazenamento chamada MyStorageInsight de $Workspace sem solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="b91a6-114">The first command uses the Get-AzureRmOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkspace, and then stores it in the $Workspace variable.The second command removes the storage insight named MyStorageInsight from $Workspace without prompting you for confirmation.</span></span>

## <span data-ttu-id="b91a6-115">OS</span><span class="sxs-lookup"><span data-stu-id="b91a6-115">PARAMETERS</span></span>

### <span data-ttu-id="b91a6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b91a6-116">-DefaultProfile</span></span>
<span data-ttu-id="b91a6-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="b91a6-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b91a6-118">-Force</span><span class="sxs-lookup"><span data-stu-id="b91a6-118">-Force</span></span>
<span data-ttu-id="b91a6-119">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="b91a6-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b91a6-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="b91a6-120">-Name</span></span>
<span data-ttu-id="b91a6-121">Especifica o nome da informação sobre o armazenamento.</span><span class="sxs-lookup"><span data-stu-id="b91a6-121">Specifies the name of the Storage Insight.</span></span>

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

### <span data-ttu-id="b91a6-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b91a6-122">-ResourceGroupName</span></span>
<span data-ttu-id="b91a6-123">Especifica o nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="b91a6-123">Specifies the name of an Azure resource group.</span></span>

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

### <span data-ttu-id="b91a6-124">-Espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="b91a6-124">-Workspace</span></span>
<span data-ttu-id="b91a6-125">Especifica o espaço de trabalho que contém a percepção do armazenamento.</span><span class="sxs-lookup"><span data-stu-id="b91a6-125">Specifies the workspace that contains the Storage Insight.</span></span>

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

### <span data-ttu-id="b91a6-126">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="b91a6-126">-WorkspaceName</span></span>
<span data-ttu-id="b91a6-127">Especifica o nome do espaço de trabalho que contém a percepção do armazenamento.</span><span class="sxs-lookup"><span data-stu-id="b91a6-127">Specifies the name of the workspace that contains the Storage Insight.</span></span>

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

### <span data-ttu-id="b91a6-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b91a6-128">-Confirm</span></span>
<span data-ttu-id="b91a6-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b91a6-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b91a6-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b91a6-130">-WhatIf</span></span>
<span data-ttu-id="b91a6-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b91a6-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b91a6-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b91a6-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b91a6-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b91a6-133">CommonParameters</span></span>
<span data-ttu-id="b91a6-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b91a6-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b91a6-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b91a6-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b91a6-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b91a6-136">INPUTS</span></span>

### <span data-ttu-id="b91a6-137">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="b91a6-137">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>
<span data-ttu-id="b91a6-138">Parâmetros: espaço de trabalho (ByValue)</span><span class="sxs-lookup"><span data-stu-id="b91a6-138">Parameters: Workspace (ByValue)</span></span>

### <span data-ttu-id="b91a6-139">System. String</span><span class="sxs-lookup"><span data-stu-id="b91a6-139">System.String</span></span>

## <span data-ttu-id="b91a6-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b91a6-140">OUTPUTS</span></span>

### <span data-ttu-id="b91a6-141">System. void</span><span class="sxs-lookup"><span data-stu-id="b91a6-141">System.Void</span></span>

## <span data-ttu-id="b91a6-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b91a6-142">NOTES</span></span>

## <span data-ttu-id="b91a6-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b91a6-143">RELATED LINKS</span></span>

[<span data-ttu-id="b91a6-144">Cmdlets do Azure Operational insights</span><span class="sxs-lookup"><span data-stu-id="b91a6-144">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)

[<span data-ttu-id="b91a6-145">Get-AzureRmOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="b91a6-145">Get-AzureRmOperationalInsightsWorkspace</span></span>](./Get-AzureRmOperationalInsightsWorkspace.md)



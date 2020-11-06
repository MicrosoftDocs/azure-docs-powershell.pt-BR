---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 92261663-CF50-4EBD-85D2-C2E254F39B41
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/remove-azurermoperationalinsightsstorageinsight
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Remove-AzureRmOperationalInsightsStorageInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Remove-AzureRmOperationalInsightsStorageInsight.md
ms.openlocfilehash: 5de334e5e9ac5c954770508a941a0c6fb951940d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441284"
---
# <span data-ttu-id="5904e-101">Remove-AzureRmOperationalInsightsStorageInsight</span><span class="sxs-lookup"><span data-stu-id="5904e-101">Remove-AzureRmOperationalInsightsStorageInsight</span></span>

## <span data-ttu-id="5904e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5904e-102">SYNOPSIS</span></span>
<span data-ttu-id="5904e-103">Remove uma percepção do armazenamento.</span><span class="sxs-lookup"><span data-stu-id="5904e-103">Removes a Storage Insight.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5904e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5904e-104">SYNTAX</span></span>

### <span data-ttu-id="5904e-105">ByWorkspaceName (padrão)</span><span class="sxs-lookup"><span data-stu-id="5904e-105">ByWorkspaceName (Default)</span></span>
```
Remove-AzureRmOperationalInsightsStorageInsight [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5904e-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="5904e-106">ByWorkspaceObject</span></span>
```
Remove-AzureRmOperationalInsightsStorageInsight [-Workspace] <PSWorkspace> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5904e-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5904e-107">DESCRIPTION</span></span>
<span data-ttu-id="5904e-108">O cmdlet **Remove-AzureRmOperationalInsightsStorageInsight** exclui uma percepção do armazenamento de um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="5904e-108">The **Remove-AzureRmOperationalInsightsStorageInsight** cmdlet deletes a Storage Insight from a workspace.</span></span>

## <span data-ttu-id="5904e-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5904e-109">EXAMPLES</span></span>

### <span data-ttu-id="5904e-110">Exemplo 1: remover uma visão de armazenamento por nome</span><span class="sxs-lookup"><span data-stu-id="5904e-110">Example 1: Remove a Storage Insight by name</span></span>
```
PS C:\>Remove-AzureRmOperationalInsightsStorageInsight -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "MyWorkspace" -Name "MyStorageInsight"
```

<span data-ttu-id="5904e-111">Esse comando Remove a percepção do armazenamento chamada MyStorageInsight do espaço de trabalho chamado MyWorkspace no grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="5904e-111">This command removes the Storage Insight named MyStorageInsight from the workspace named MyWorkspace in the specified resource group.</span></span>
<span data-ttu-id="5904e-112">O comando não especifica o parâmetro *Force* ; portanto, ele solicita confirmação antes de remover a percepção do armazenamento.</span><span class="sxs-lookup"><span data-stu-id="5904e-112">The command does not specify the *Force* parameter, so it prompts you for confirmation before removing the Storage Insight.</span></span>

### <span data-ttu-id="5904e-113">Exemplo 2: remover uma visão de armazenamento sem confirmação</span><span class="sxs-lookup"><span data-stu-id="5904e-113">Example 2: Remove a Storage Insight without confirmation</span></span>
```
PS C:\>$Workspace = Get-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"

PS C:\>Remove-AzureRmOperationalInsightsStorageInsight -Workspace $Workspace -Name "MyStorageInsight" -Force
```

<span data-ttu-id="5904e-114">O primeiro comando usa o cmdlet Get-AzureRmOperationalInsightsWorkspace para obter o espaço de trabalho chamado MyWorkspace e, em seguida, armazena-o na variável $Workspace. O segundo comando Remove a percepção do armazenamento chamada MyStorageInsight de $Workspace sem solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="5904e-114">The first command uses the Get-AzureRmOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkspace, and then stores it in the $Workspace variable.The second command removes the storage insight named MyStorageInsight from $Workspace without prompting you for confirmation.</span></span>

## <span data-ttu-id="5904e-115">OS</span><span class="sxs-lookup"><span data-stu-id="5904e-115">PARAMETERS</span></span>

### <span data-ttu-id="5904e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5904e-116">-DefaultProfile</span></span>
<span data-ttu-id="5904e-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="5904e-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5904e-118">-Force</span><span class="sxs-lookup"><span data-stu-id="5904e-118">-Force</span></span>
<span data-ttu-id="5904e-119">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="5904e-119">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5904e-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="5904e-120">-Name</span></span>
<span data-ttu-id="5904e-121">Especifica o nome da informação sobre o armazenamento.</span><span class="sxs-lookup"><span data-stu-id="5904e-121">Specifies the name of the Storage Insight.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5904e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5904e-122">-ResourceGroupName</span></span>
<span data-ttu-id="5904e-123">Especifica o nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="5904e-123">Specifies the name of an Azure resource group.</span></span>

```yaml
Type: String
Parameter Sets: ByWorkspaceName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5904e-124">-Espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="5904e-124">-Workspace</span></span>
<span data-ttu-id="5904e-125">Especifica o espaço de trabalho que contém a percepção do armazenamento.</span><span class="sxs-lookup"><span data-stu-id="5904e-125">Specifies the workspace that contains the Storage Insight.</span></span>

```yaml
Type: PSWorkspace
Parameter Sets: ByWorkspaceObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5904e-126">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="5904e-126">-WorkspaceName</span></span>
<span data-ttu-id="5904e-127">Especifica o nome do espaço de trabalho que contém a percepção do armazenamento.</span><span class="sxs-lookup"><span data-stu-id="5904e-127">Specifies the name of the workspace that contains the Storage Insight.</span></span>

```yaml
Type: String
Parameter Sets: ByWorkspaceName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5904e-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="5904e-128">-Confirm</span></span>
<span data-ttu-id="5904e-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5904e-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5904e-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5904e-130">-WhatIf</span></span>
<span data-ttu-id="5904e-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5904e-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5904e-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5904e-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5904e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5904e-133">CommonParameters</span></span>
<span data-ttu-id="5904e-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5904e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5904e-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5904e-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5904e-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5904e-136">INPUTS</span></span>

### <span data-ttu-id="5904e-137">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="5904e-137">PSWorkspace</span></span>
<span data-ttu-id="5904e-138">O parâmetro ' Workspace ' aceita o valor do tipo ' PSWorkspace ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="5904e-138">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

## <span data-ttu-id="5904e-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5904e-139">OUTPUTS</span></span>

## <span data-ttu-id="5904e-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5904e-140">NOTES</span></span>

## <span data-ttu-id="5904e-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5904e-141">RELATED LINKS</span></span>

[<span data-ttu-id="5904e-142">Cmdlets do Azure Operational insights</span><span class="sxs-lookup"><span data-stu-id="5904e-142">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)

[<span data-ttu-id="5904e-143">Get-AzureRmOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="5904e-143">Get-AzureRmOperationalInsightsWorkspace</span></span>](./Get-AzureRmOperationalInsightsWorkspace.md)



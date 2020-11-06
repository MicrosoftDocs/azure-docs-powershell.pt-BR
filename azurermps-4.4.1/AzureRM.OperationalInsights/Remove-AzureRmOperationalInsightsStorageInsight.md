---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 92261663-CF50-4EBD-85D2-C2E254F39B41
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Remove-AzureRmOperationalInsightsStorageInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Remove-AzureRmOperationalInsightsStorageInsight.md
ms.openlocfilehash: cbbbd23a42f2922273811a7925cbae6f6fd867f4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429174"
---
# <span data-ttu-id="bff4e-101">Remove-AzureRmOperationalInsightsStorageInsight</span><span class="sxs-lookup"><span data-stu-id="bff4e-101">Remove-AzureRmOperationalInsightsStorageInsight</span></span>

## <span data-ttu-id="bff4e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bff4e-102">SYNOPSIS</span></span>
<span data-ttu-id="bff4e-103">Remove uma percepção do armazenamento.</span><span class="sxs-lookup"><span data-stu-id="bff4e-103">Removes a Storage Insight.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bff4e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bff4e-104">SYNTAX</span></span>

### <span data-ttu-id="bff4e-105">ByWorkspaceName (padrão)</span><span class="sxs-lookup"><span data-stu-id="bff4e-105">ByWorkspaceName (Default)</span></span>
```
Remove-AzureRmOperationalInsightsStorageInsight [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bff4e-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="bff4e-106">ByWorkspaceObject</span></span>
```
Remove-AzureRmOperationalInsightsStorageInsight [-Workspace] <PSWorkspace> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bff4e-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="bff4e-107">DESCRIPTION</span></span>
<span data-ttu-id="bff4e-108">O cmdlet **Remove-AzureRmOperationalInsightsStorageInsight** exclui uma percepção do armazenamento de um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="bff4e-108">The **Remove-AzureRmOperationalInsightsStorageInsight** cmdlet deletes a Storage Insight from a workspace.</span></span>

## <span data-ttu-id="bff4e-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bff4e-109">EXAMPLES</span></span>

### <span data-ttu-id="bff4e-110">Exemplo 1: remover uma visão de armazenamento por nome</span><span class="sxs-lookup"><span data-stu-id="bff4e-110">Example 1: Remove a Storage Insight by name</span></span>
```
PS C:\>Remove-AzureRmOperationalInsightsStorageInsight -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "MyWorkspace" -Name "MyStorageInsight"
```

<span data-ttu-id="bff4e-111">Esse comando Remove a percepção do armazenamento chamada MyStorageInsight do espaço de trabalho chamado MyWorkspace no grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="bff4e-111">This command removes the Storage Insight named MyStorageInsight from the workspace named MyWorkspace in the specified resource group.</span></span>
<span data-ttu-id="bff4e-112">O comando não especifica o parâmetro *Force* ; portanto, ele solicita confirmação antes de remover a percepção do armazenamento.</span><span class="sxs-lookup"><span data-stu-id="bff4e-112">The command does not specify the *Force* parameter, so it prompts you for confirmation before removing the Storage Insight.</span></span>

### <span data-ttu-id="bff4e-113">Exemplo 2: remover uma visão de armazenamento sem confirmação</span><span class="sxs-lookup"><span data-stu-id="bff4e-113">Example 2: Remove a Storage Insight without confirmation</span></span>
```
PS C:\>$Workspace = Get-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"

PS C:\>Remove-AzureRmOperationalInsightsStorageInsight -Workspace $Workspace -Name "MyStorageInsight" -Force
```

<span data-ttu-id="bff4e-114">O primeiro comando usa o cmdlet Get-AzureRmOperationalInsightsWorkspace para obter o espaço de trabalho chamado MyWorkspace e, em seguida, armazena-o na variável $Workspace. O segundo comando Remove a percepção do armazenamento chamada MyStorageInsight de $Workspace sem solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="bff4e-114">The first command uses the Get-AzureRmOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkspace, and then stores it in the $Workspace variable.The second command removes the storage insight named MyStorageInsight from $Workspace without prompting you for confirmation.</span></span>

## <span data-ttu-id="bff4e-115">OS</span><span class="sxs-lookup"><span data-stu-id="bff4e-115">PARAMETERS</span></span>

### <span data-ttu-id="bff4e-116">-Force</span><span class="sxs-lookup"><span data-stu-id="bff4e-116">-Force</span></span>
<span data-ttu-id="bff4e-117">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="bff4e-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="bff4e-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="bff4e-118">-Name</span></span>
<span data-ttu-id="bff4e-119">Especifica o nome da informação sobre o armazenamento.</span><span class="sxs-lookup"><span data-stu-id="bff4e-119">Specifies the name of the Storage Insight.</span></span>

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

### <span data-ttu-id="bff4e-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bff4e-120">-ResourceGroupName</span></span>
<span data-ttu-id="bff4e-121">Especifica o nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="bff4e-121">Specifies the name of an Azure resource group.</span></span>

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

### <span data-ttu-id="bff4e-122">-Espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="bff4e-122">-Workspace</span></span>
<span data-ttu-id="bff4e-123">Especifica o espaço de trabalho que contém a percepção do armazenamento.</span><span class="sxs-lookup"><span data-stu-id="bff4e-123">Specifies the workspace that contains the Storage Insight.</span></span>

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

### <span data-ttu-id="bff4e-124">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="bff4e-124">-WorkspaceName</span></span>
<span data-ttu-id="bff4e-125">Especifica o nome do espaço de trabalho que contém a percepção do armazenamento.</span><span class="sxs-lookup"><span data-stu-id="bff4e-125">Specifies the name of the workspace that contains the Storage Insight.</span></span>

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

### <span data-ttu-id="bff4e-126">-Confirme</span><span class="sxs-lookup"><span data-stu-id="bff4e-126">-Confirm</span></span>
<span data-ttu-id="bff4e-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bff4e-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bff4e-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bff4e-128">-WhatIf</span></span>
<span data-ttu-id="bff4e-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="bff4e-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bff4e-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="bff4e-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bff4e-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bff4e-131">-DefaultProfile</span></span>
<span data-ttu-id="bff4e-132">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bff4e-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bff4e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bff4e-133">CommonParameters</span></span>
<span data-ttu-id="bff4e-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bff4e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bff4e-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bff4e-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bff4e-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="bff4e-136">INPUTS</span></span>

### <span data-ttu-id="bff4e-137">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="bff4e-137">PSWorkspace</span></span>
<span data-ttu-id="bff4e-138">O parâmetro ' Workspace ' aceita o valor do tipo ' PSWorkspace ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="bff4e-138">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

## <span data-ttu-id="bff4e-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="bff4e-139">OUTPUTS</span></span>

## <span data-ttu-id="bff4e-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="bff4e-140">NOTES</span></span>

## <span data-ttu-id="bff4e-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bff4e-141">RELATED LINKS</span></span>

[<span data-ttu-id="bff4e-142">Cmdlets do Azure Operational insights</span><span class="sxs-lookup"><span data-stu-id="bff4e-142">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)

[<span data-ttu-id="bff4e-143">Get-AzureRmOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="bff4e-143">Get-AzureRmOperationalInsightsWorkspace</span></span>](./Get-AzureRmOperationalInsightsWorkspace.md)



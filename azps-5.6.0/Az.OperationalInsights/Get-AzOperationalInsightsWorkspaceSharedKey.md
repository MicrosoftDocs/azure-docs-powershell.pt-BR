---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 112D5C69-3F4F-4BB6-9DA4-52757146B0EF
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/get-azoperationalinsightsworkspacesharedkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspaceSharedKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspaceSharedKey.md
ms.openlocfilehash: 2cf7f548db74a7c7393fcd52bb7183c54f5f4e60
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891777"
---
# <span data-ttu-id="cf418-101">Get-AzOperationalInsightsWorkspaceSharedKey</span><span class="sxs-lookup"><span data-stu-id="cf418-101">Get-AzOperationalInsightsWorkspaceSharedKey</span></span>

## <span data-ttu-id="cf418-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cf418-102">SYNOPSIS</span></span>
<span data-ttu-id="cf418-103">Obtém as chaves compartilhadas de um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="cf418-103">Gets the shared keys for a workspace.</span></span>

## <span data-ttu-id="cf418-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="cf418-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsWorkspaceSharedKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cf418-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="cf418-105">DESCRIPTION</span></span>
<span data-ttu-id="cf418-106">O cmdlet **Get-AzOperationalInsightsWorkspaceSharedKey** lista as chaves compartilhadas de um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="cf418-106">The **Get-AzOperationalInsightsWorkspaceSharedKey** cmdlet lists the shared keys for a workspace.</span></span>
<span data-ttu-id="cf418-107">As chaves são usadas para conectar agentes do Insights Operacionais ao espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="cf418-107">The keys are used to connect Operational Insights agents to the workspace.</span></span>

## <span data-ttu-id="cf418-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cf418-108">EXAMPLES</span></span>

### <span data-ttu-id="cf418-109">Exemplo 1: Obter chaves compartilhadas pelo nome do espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="cf418-109">Example 1: Get shared keys by workspace name</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspaceSharedKey -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"
```

<span data-ttu-id="cf418-110">Este comando obtém as chaves compartilhadas do espaço de trabalho chamado MyWorkspace no grupo de recursos chamado ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="cf418-110">This command gets the shared keys for the workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="cf418-111">Exemplo 2: Obter chaves compartilhadas usando o pipeline</span><span class="sxs-lookup"><span data-stu-id="cf418-111">Example 2: Get shared keys by using the pipeline</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" | Get-AzOperationalInsightsWorkspaceSharedKey
```

<span data-ttu-id="cf418-112">Este comando obtém o espaço de trabalho chamado MyWorkspace usando o cmdlet Get-AzOperationalInsightsWorkspace e passa o espaço de trabalho para o cmdlet **Get-AzOperationalInsightsWorkspaceSharedKey.**</span><span class="sxs-lookup"><span data-stu-id="cf418-112">This command gets the workspace named MyWorkspace using the Get-AzOperationalInsightsWorkspace cmdlet, and then passes the workspace to the **Get-AzOperationalInsightsWorkspaceSharedKey** cmdlet.</span></span>
<span data-ttu-id="cf418-113">O comando obtém as chaves compartilhadas para esse espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="cf418-113">The command gets the shared keys for that workspace.</span></span>

## <span data-ttu-id="cf418-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="cf418-114">PARAMETERS</span></span>

### <span data-ttu-id="cf418-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf418-115">-DefaultProfile</span></span>
<span data-ttu-id="cf418-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="cf418-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cf418-117">-Name</span><span class="sxs-lookup"><span data-stu-id="cf418-117">-Name</span></span>
<span data-ttu-id="cf418-118">Especifica o nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="cf418-118">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="cf418-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf418-119">-ResourceGroupName</span></span>
<span data-ttu-id="cf418-120">Especifica o nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="cf418-120">Specifies the name of an Azure resource group.</span></span>

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

### <span data-ttu-id="cf418-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf418-121">CommonParameters</span></span>
<span data-ttu-id="cf418-122">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cf418-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf418-123">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cf418-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf418-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cf418-124">INPUTS</span></span>

### <span data-ttu-id="cf418-125">System.String</span><span class="sxs-lookup"><span data-stu-id="cf418-125">System.String</span></span>

## <span data-ttu-id="cf418-126">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="cf418-126">OUTPUTS</span></span>

### <span data-ttu-id="cf418-127">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspaceKeys</span><span class="sxs-lookup"><span data-stu-id="cf418-127">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspaceKeys</span></span>

## <span data-ttu-id="cf418-128">NOTES</span><span class="sxs-lookup"><span data-stu-id="cf418-128">NOTES</span></span>

## <span data-ttu-id="cf418-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cf418-129">RELATED LINKS</span></span>

[<span data-ttu-id="cf418-130">Cmdlets do Insights Operacionais do Azure</span><span class="sxs-lookup"><span data-stu-id="cf418-130">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)

[<span data-ttu-id="cf418-131">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="cf418-131">Get-AzOperationalInsightsWorkspace</span></span>](./Get-AzOperationalInsightsWorkspace.md)



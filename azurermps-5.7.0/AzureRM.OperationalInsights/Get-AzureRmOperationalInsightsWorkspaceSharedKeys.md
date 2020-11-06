---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 112D5C69-3F4F-4BB6-9DA4-52757146B0EF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/get-azurermoperationalinsightsworkspacesharedkeys
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsWorkspaceSharedKeys.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsWorkspaceSharedKeys.md
ms.openlocfilehash: 5fab6a3a0419047fef32f5bf32f52e1f7ee57d3c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428145"
---
# <span data-ttu-id="e8d69-101">Get-AzureRmOperationalInsightsWorkspaceSharedKeys</span><span class="sxs-lookup"><span data-stu-id="e8d69-101">Get-AzureRmOperationalInsightsWorkspaceSharedKeys</span></span>

## <span data-ttu-id="e8d69-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e8d69-102">SYNOPSIS</span></span>
<span data-ttu-id="e8d69-103">Obtém as chaves compartilhadas para um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="e8d69-103">Gets the shared keys for a workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e8d69-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e8d69-104">SYNTAX</span></span>

```
Get-AzureRmOperationalInsightsWorkspaceSharedKeys [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e8d69-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e8d69-105">DESCRIPTION</span></span>
<span data-ttu-id="e8d69-106">O cmdlet **Get-AzureRmOperationalInsightsWorkspaceSharedKeys** lista as chaves compartilhadas de um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="e8d69-106">The **Get-AzureRmOperationalInsightsWorkspaceSharedKeys** cmdlet lists the shared keys for a workspace.</span></span>
<span data-ttu-id="e8d69-107">As chaves são usadas para conectar agentes do insights operacionais ao espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="e8d69-107">The keys are used to connect Operational Insights agents to the workspace.</span></span>

## <span data-ttu-id="e8d69-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e8d69-108">EXAMPLES</span></span>

### <span data-ttu-id="e8d69-109">Exemplo 1: obter chaves compartilhadas por nome do espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="e8d69-109">Example 1: Get shared keys by workspace name</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsWorkspaceSharedKeys -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"
```

<span data-ttu-id="e8d69-110">Esse comando obtém as chaves compartilhadas para o espaço de trabalho chamado MyWorkspace no grupo de recursos chamado ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="e8d69-110">This command gets the shared keys for the workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="e8d69-111">Exemplo 2: obter chaves compartilhadas usando o pipeline</span><span class="sxs-lookup"><span data-stu-id="e8d69-111">Example 2: Get shared keys by using the pipeline</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" | Get-AzureRmOperationalInsightsWorkspaceSharedKeys
```

<span data-ttu-id="e8d69-112">Esse comando obtém o espaço de trabalho chamado MyWorkspace usando o cmdlet Get-AzureRmOperationalInsightsWorkspace e, em seguida, passa o espaço de trabalho para o cmdlet **Get-AzureRmOperationalInsightsWorkspaceSharedKeys** .</span><span class="sxs-lookup"><span data-stu-id="e8d69-112">This command gets the workspace named MyWorkspace using the Get-AzureRmOperationalInsightsWorkspace cmdlet, and then passes the workspace to the **Get-AzureRmOperationalInsightsWorkspaceSharedKeys** cmdlet.</span></span>
<span data-ttu-id="e8d69-113">O comando obtém as chaves compartilhadas para esse espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="e8d69-113">The command gets the shared keys for that workspace.</span></span>

## <span data-ttu-id="e8d69-114">OS</span><span class="sxs-lookup"><span data-stu-id="e8d69-114">PARAMETERS</span></span>

### <span data-ttu-id="e8d69-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8d69-115">-DefaultProfile</span></span>
<span data-ttu-id="e8d69-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="e8d69-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e8d69-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="e8d69-117">-Name</span></span>
<span data-ttu-id="e8d69-118">Especifica o nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="e8d69-118">Specifies the workspace name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8d69-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8d69-119">-ResourceGroupName</span></span>
<span data-ttu-id="e8d69-120">Especifica o nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="e8d69-120">Specifies the name of an Azure resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8d69-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8d69-121">CommonParameters</span></span>
<span data-ttu-id="e8d69-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8d69-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8d69-123">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e8d69-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8d69-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e8d69-124">INPUTS</span></span>

### <span data-ttu-id="e8d69-125">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="e8d69-125">None</span></span>
<span data-ttu-id="e8d69-126">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="e8d69-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e8d69-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e8d69-127">OUTPUTS</span></span>

### <span data-ttu-id="e8d69-128">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspaceKeys</span><span class="sxs-lookup"><span data-stu-id="e8d69-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspaceKeys</span></span>

## <span data-ttu-id="e8d69-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e8d69-129">NOTES</span></span>

## <span data-ttu-id="e8d69-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e8d69-130">RELATED LINKS</span></span>

[<span data-ttu-id="e8d69-131">Cmdlets do Azure Operational insights</span><span class="sxs-lookup"><span data-stu-id="e8d69-131">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)

[<span data-ttu-id="e8d69-132">Get-AzureRmOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="e8d69-132">Get-AzureRmOperationalInsightsWorkspace</span></span>](./Get-AzureRmOperationalInsightsWorkspace.md)



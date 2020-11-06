---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearning/get-azurermmlcommitmentplanusagehistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlCommitmentPlanUsageHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlCommitmentPlanUsageHistory.md
ms.openlocfilehash: e92f32dab72a4a96be03f800297194711f275d70
ms.sourcegitcommit: e0947ba0606618a565d8a99fa0e4bef7d028d7e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "93611151"
---
# <span data-ttu-id="f7975-101">Get-AzureRmMlCommitmentPlanUsageHistory</span><span class="sxs-lookup"><span data-stu-id="f7975-101">Get-AzureRmMlCommitmentPlanUsageHistory</span></span>

## <span data-ttu-id="f7975-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f7975-102">SYNOPSIS</span></span>
<span data-ttu-id="f7975-103">Recupera as informações do histórico de uso para um plano de compromisso especificado.</span><span class="sxs-lookup"><span data-stu-id="f7975-103">Retrieves usage history information for a specified commitment plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f7975-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f7975-104">SYNTAX</span></span>

```
Get-AzureRmMlCommitmentPlanUsageHistory -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f7975-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f7975-105">DESCRIPTION</span></span>
<span data-ttu-id="f7975-106">Recupera as informações do histórico de uso para um plano de compromisso especificado, incluindo recursos usados e recursos restantes no plano.</span><span class="sxs-lookup"><span data-stu-id="f7975-106">Retrieves usage history information for a specified commitment plan, including resources used and resources remaining within the plan.</span></span>

## <span data-ttu-id="f7975-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f7975-107">EXAMPLES</span></span>

### <span data-ttu-id="f7975-108">--------------------------Exemplo 1: obter histórico de uso de um plano de compromisso específico--------------------------</span><span class="sxs-lookup"><span data-stu-id="f7975-108">--------------------------  Example 1: Get usage history for a specific commitment plan  --------------------------</span></span>
```
Get-AzureRmMlCommitmentPlanUsageHistory -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName"
```

## <span data-ttu-id="f7975-109">OS</span><span class="sxs-lookup"><span data-stu-id="f7975-109">PARAMETERS</span></span>

### <span data-ttu-id="f7975-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7975-110">-DefaultProfile</span></span>
<span data-ttu-id="f7975-111">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="f7975-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f7975-112">-Nome</span><span class="sxs-lookup"><span data-stu-id="f7975-112">-Name</span></span>
<span data-ttu-id="f7975-113">O nome do plano de compromisso do Azure ML.</span><span class="sxs-lookup"><span data-stu-id="f7975-113">The name of the Azure ML commitment plan.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7975-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7975-114">-ResourceGroupName</span></span>
<span data-ttu-id="f7975-115">O nome do grupo de recursos para o plano de compromisso do Azure ML.</span><span class="sxs-lookup"><span data-stu-id="f7975-115">The name of the resource group for the Azure ML commitment plan.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7975-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7975-116">CommonParameters</span></span>
<span data-ttu-id="f7975-117">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7975-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7975-118">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f7975-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7975-119">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f7975-119">INPUTS</span></span>

### <span data-ttu-id="f7975-120">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="f7975-120">None</span></span>
<span data-ttu-id="f7975-121">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="f7975-121">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f7975-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f7975-122">OUTPUTS</span></span>

### <span data-ttu-id="f7975-123">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. Models. PlanUsageHistory []</span><span class="sxs-lookup"><span data-stu-id="f7975-123">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.PlanUsageHistory[]</span></span>

## <span data-ttu-id="f7975-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f7975-124">NOTES</span></span>
<span data-ttu-id="f7975-125">Palavras-chave: Azure, azurerm, ARM, Resource, Management, Manager, Machine, Machine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="f7975-125">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="f7975-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f7975-126">RELATED LINKS</span></span>


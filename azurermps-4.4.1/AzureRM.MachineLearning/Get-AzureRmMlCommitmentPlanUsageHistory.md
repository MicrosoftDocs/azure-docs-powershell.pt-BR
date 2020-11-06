---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlCommitmentPlanUsageHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlCommitmentPlanUsageHistory.md
ms.openlocfilehash: c80278e460368ca6ec78efb4f5e74e456816df47
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610767"
---
# <span data-ttu-id="ece56-101">Get-AzureRmMlCommitmentPlanUsageHistory</span><span class="sxs-lookup"><span data-stu-id="ece56-101">Get-AzureRmMlCommitmentPlanUsageHistory</span></span>

## <span data-ttu-id="ece56-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ece56-102">SYNOPSIS</span></span>
<span data-ttu-id="ece56-103">Recupera as informações do histórico de uso para um plano de compromisso especificado.</span><span class="sxs-lookup"><span data-stu-id="ece56-103">Retrieves usage history information for a specified commitment plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ece56-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ece56-104">SYNTAX</span></span>

```
Get-AzureRmMlCommitmentPlanUsageHistory -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ece56-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ece56-105">DESCRIPTION</span></span>
<span data-ttu-id="ece56-106">Recupera as informações do histórico de uso para um plano de compromisso especificado, incluindo recursos usados e recursos restantes no plano.</span><span class="sxs-lookup"><span data-stu-id="ece56-106">Retrieves usage history information for a specified commitment plan, including resources used and resources remaining within the plan.</span></span>

## <span data-ttu-id="ece56-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ece56-107">EXAMPLES</span></span>

### <span data-ttu-id="ece56-108">--------------------------Exemplo 1: obter histórico de uso de um plano de compromisso específico--------------------------</span><span class="sxs-lookup"><span data-stu-id="ece56-108">--------------------------  Example 1: Get usage history for a specific commitment plan  --------------------------</span></span>
<span data-ttu-id="ece56-109">@ {Paragraph = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="ece56-109">@{paragraph=PS C:\\\>}</span></span>





```
Get-AzureRmMlCommitmentPlanUsageHistory -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName"
```

## <span data-ttu-id="ece56-110">OS</span><span class="sxs-lookup"><span data-stu-id="ece56-110">PARAMETERS</span></span>

### <span data-ttu-id="ece56-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="ece56-111">-Name</span></span>
<span data-ttu-id="ece56-112">O nome do plano de compromisso do Azure ML.</span><span class="sxs-lookup"><span data-stu-id="ece56-112">The name of the Azure ML commitment plan.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ece56-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ece56-113">-ResourceGroupName</span></span>
<span data-ttu-id="ece56-114">O nome do grupo de recursos para o plano de compromisso do Azure ML.</span><span class="sxs-lookup"><span data-stu-id="ece56-114">The name of the resource group for the Azure ML commitment plan.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ece56-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ece56-115">-DefaultProfile</span></span>
<span data-ttu-id="ece56-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ece56-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ece56-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ece56-117">CommonParameters</span></span>
<span data-ttu-id="ece56-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ece56-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ece56-119">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ece56-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ece56-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ece56-120">INPUTS</span></span>

## <span data-ttu-id="ece56-121">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ece56-121">OUTPUTS</span></span>

### <span data-ttu-id="ece56-122">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. Models. PlanUsageHistory []</span><span class="sxs-lookup"><span data-stu-id="ece56-122">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.PlanUsageHistory[]</span></span>

## <span data-ttu-id="ece56-123">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ece56-123">NOTES</span></span>
<span data-ttu-id="ece56-124">Palavras-chave: Azure, azurerm, ARM, Resource, Management, Manager, Machine, Machine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="ece56-124">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="ece56-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ece56-125">RELATED LINKS</span></span>


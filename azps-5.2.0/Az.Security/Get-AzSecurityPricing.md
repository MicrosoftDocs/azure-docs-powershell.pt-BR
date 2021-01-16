---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityPricing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityPricing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityPricing.md
ms.openlocfilehash: 59d1c7fa5d546652d8976dc42739c2e483164999
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98258572"
---
# <span data-ttu-id="03cb9-101">Get-AzSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="03cb9-101">Get-AzSecurityPricing</span></span>

## <span data-ttu-id="03cb9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="03cb9-102">SYNOPSIS</span></span>

<span data-ttu-id="03cb9-103">Obtém os planos do Azure defender para uma assinatura na central de segurança do Azure.</span><span class="sxs-lookup"><span data-stu-id="03cb9-103">Gets the Azure Defender plans for a subscription in Azure Security Center.</span></span>

## <span data-ttu-id="03cb9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="03cb9-104">SYNTAX</span></span>

### <span data-ttu-id="03cb9-105">SubscriptionScope (padrão)</span><span class="sxs-lookup"><span data-stu-id="03cb9-105">SubscriptionScope (Default)</span></span>

```powershell
Get-AzSecurityPricing [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="03cb9-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="03cb9-106">SubscriptionLevelResource</span></span>

```powershell
Get-AzSecurityPricing -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="03cb9-107">Identificação</span><span class="sxs-lookup"><span data-stu-id="03cb9-107">ResourceId</span></span>

```powershell
Get-AzSecurityPricing -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="03cb9-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="03cb9-108">DESCRIPTION</span></span>

<span data-ttu-id="03cb9-109">Você pode exibir cada plano do Azure defender, por assinatura, usando este cmdlet.</span><span class="sxs-lookup"><span data-stu-id="03cb9-109">You can view each Azure Defender plan, per subscription, using this cmdlet.</span></span>

<span data-ttu-id="03cb9-110">Para obter detalhes sobre o Azure defender e os planos disponíveis, consulte [introdução ao Azure defender](https://docs.microsoft.com/azure/security-center/azure-defender).</span><span class="sxs-lookup"><span data-stu-id="03cb9-110">For details about Azure Defender and the available plans, see [Introduction to Azure Defender](https://docs.microsoft.com/azure/security-center/azure-defender).</span></span>

## <span data-ttu-id="03cb9-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="03cb9-111">EXAMPLES</span></span>

### <span data-ttu-id="03cb9-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="03cb9-112">Example 1</span></span>

```powershell
PS C:\> Get-AzSecurityPricing
Id                                                                                                                   Name                      PricingTier    FreeTrialRemainingTime
--                                                                                                                   ----                      -----------    ----------------------
/subscriptions/fbaa2b23-e9dd-4bed-93c1-9e2a44f64bc0/providers/Microsoft.Security/pricings/VirtualMachines            VirtualMachines           Free           00:00:00
/subscriptions/fbaa2b23-e9dd-4bed-93c1-9e2a44f64bc0/providers/Microsoft.Security/pricings/Sqlservers                 SqlServers                Standard       00:00:00
/subscriptions/fbaa2b23-e9dd-4bed-93c1-9e2a44f64bc0/providers/Microsoft.Security/pricings/AppServices                AppServices               Free           00:00:00
/subscriptions/fbaa2b23-e9dd-4bed-93c1-9e2a44f64bc0/providers/Microsoft.Security/pricings/StorageAccounts            StorageAccounts           Free           00:00:00
/subscriptions/fbaa2b23-e9dd-4bed-93c1-9e2a44f64bc0/providers/Microsoft.Security/pricings/SqlserverVirtualMachines   SqlservervirtualMachines  Free           00:00:00
/subscriptions/fbaa2b23-e9dd-4bed-93c1-9e2a44f64bc0/providers/Microsoft.Security/pricings/KubernetesService          KubernetesService         Free           00:00:00
/subscriptions/fbaa2b23-e9dd-4bed-93c1-9e2a44f64bc0/providers/Microsoft.Security/pricings/ContainerRegistry          ContainerRegistry         Free           00:00:00
/subscriptions/fbaa2b23-e9dd-4bed-93c1-9e2a44f64bc0/providers/Microsoft.Security/pricings/KeyVaults                  KeyVaults                 Free           00:00:00
```

<span data-ttu-id="03cb9-113">Obtém o status de cada plano do Azure defender para a assinatura.</span><span class="sxs-lookup"><span data-stu-id="03cb9-113">Gets the status of each Azure Defender plan for the subscription.</span></span>



### <span data-ttu-id="03cb9-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="03cb9-114">Example 2</span></span>

```powershell
PS C:\> Get-AzSecurityPricing -ResourceId
```

<span data-ttu-id="03cb9-115">Obtém detalhes de preço da ID de recurso específica.</span><span class="sxs-lookup"><span data-stu-id="03cb9-115">Gets pricing details of the specific resource ID.</span></span> <span data-ttu-id="03cb9-116">Onde ResourceId é uma das IDs retornadas por `Get-AzSecurityPricing` .</span><span class="sxs-lookup"><span data-stu-id="03cb9-116">Where ResourceId is one of the IDs returned by `Get-AzSecurityPricing`.</span></span>

### <span data-ttu-id="03cb9-117">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="03cb9-117">Example 3</span></span>

```powershell
PS C:\> Get-AzSecurityPricing -Name
```

<span data-ttu-id="03cb9-118">Obtém detalhes de preço do plano nomeado do Azure defender.</span><span class="sxs-lookup"><span data-stu-id="03cb9-118">Gets pricing details of the named Azure Defender plan.</span></span> <span data-ttu-id="03cb9-119">Onde `name` é um dos nomes retornados por `Get-AzSecurityPricing` .</span><span class="sxs-lookup"><span data-stu-id="03cb9-119">Where `name` is one of the names returned by `Get-AzSecurityPricing`.</span></span>


## <span data-ttu-id="03cb9-120">OS</span><span class="sxs-lookup"><span data-stu-id="03cb9-120">PARAMETERS</span></span>

### <span data-ttu-id="03cb9-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03cb9-121">-DefaultProfile</span></span>

<span data-ttu-id="03cb9-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="03cb9-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="03cb9-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="03cb9-123">-Name</span></span>

<span data-ttu-id="03cb9-124">Nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="03cb9-124">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03cb9-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="03cb9-125">-ResourceId</span></span>

<span data-ttu-id="03cb9-126">ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="03cb9-126">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03cb9-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03cb9-127">CommonParameters</span></span>

<span data-ttu-id="03cb9-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03cb9-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03cb9-129">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03cb9-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03cb9-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="03cb9-130">INPUTS</span></span>

### <span data-ttu-id="03cb9-131">System. String</span><span class="sxs-lookup"><span data-stu-id="03cb9-131">System.String</span></span>

## <span data-ttu-id="03cb9-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="03cb9-132">OUTPUTS</span></span>

### <span data-ttu-id="03cb9-133">Microsoft. Azure. Commands. Security. Models. pricings. PSSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="03cb9-133">Microsoft.Azure.Commands.Security.Models.Pricings.PSSecurityPricing</span></span>

## <span data-ttu-id="03cb9-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="03cb9-134">NOTES</span></span>

## <span data-ttu-id="03cb9-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="03cb9-135">RELATED LINKS</span></span>

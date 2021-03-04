---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Get-AzSecurityPricing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityPricing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityPricing.md
ms.openlocfilehash: 588f9a057767e1e78b43664c35a61f26e6edf972
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901576"
---
# <span data-ttu-id="dadfd-101">Get-AzSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="dadfd-101">Get-AzSecurityPricing</span></span>

## <span data-ttu-id="dadfd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dadfd-102">SYNOPSIS</span></span>

<span data-ttu-id="dadfd-103">Obtém os planos do Azure Defender para uma assinatura no Centro de Segurança do Azure.</span><span class="sxs-lookup"><span data-stu-id="dadfd-103">Gets the Azure Defender plans for a subscription in Azure Security Center.</span></span>

## <span data-ttu-id="dadfd-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="dadfd-104">SYNTAX</span></span>

### <span data-ttu-id="dadfd-105">SubscriptionScope (Padrão)</span><span class="sxs-lookup"><span data-stu-id="dadfd-105">SubscriptionScope (Default)</span></span>

```powershell
Get-AzSecurityPricing [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dadfd-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="dadfd-106">SubscriptionLevelResource</span></span>

```powershell
Get-AzSecurityPricing -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dadfd-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="dadfd-107">ResourceId</span></span>

```powershell
Get-AzSecurityPricing -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dadfd-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="dadfd-108">DESCRIPTION</span></span>

<span data-ttu-id="dadfd-109">Você pode exibir cada plano do Azure Defender, por assinatura, usando este cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dadfd-109">You can view each Azure Defender plan, per subscription, using this cmdlet.</span></span>

<span data-ttu-id="dadfd-110">Para obter detalhes sobre o Azure Defender e os planos disponíveis, consulte [Introdução ao Azure Defender](https://docs.microsoft.com/azure/security-center/azure-defender).</span><span class="sxs-lookup"><span data-stu-id="dadfd-110">For details about Azure Defender and the available plans, see [Introduction to Azure Defender](https://docs.microsoft.com/azure/security-center/azure-defender).</span></span>

## <span data-ttu-id="dadfd-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="dadfd-111">EXAMPLES</span></span>

### <span data-ttu-id="dadfd-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="dadfd-112">Example 1</span></span>

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

<span data-ttu-id="dadfd-113">Obtém o status de cada plano do Azure Defender para a assinatura.</span><span class="sxs-lookup"><span data-stu-id="dadfd-113">Gets the status of each Azure Defender plan for the subscription.</span></span>



### <span data-ttu-id="dadfd-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="dadfd-114">Example 2</span></span>

```powershell
PS C:\> Get-AzSecurityPricing -ResourceId
```

<span data-ttu-id="dadfd-115">Obtém detalhes de preços da ID de recurso específica.</span><span class="sxs-lookup"><span data-stu-id="dadfd-115">Gets pricing details of the specific resource ID.</span></span> <span data-ttu-id="dadfd-116">Onde ResourceId é uma das IDs retornadas por `Get-AzSecurityPricing` .</span><span class="sxs-lookup"><span data-stu-id="dadfd-116">Where ResourceId is one of the IDs returned by `Get-AzSecurityPricing`.</span></span>

### <span data-ttu-id="dadfd-117">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="dadfd-117">Example 3</span></span>

```powershell
PS C:\> Get-AzSecurityPricing -Name
```

<span data-ttu-id="dadfd-118">Obtém detalhes de preços do plano chamado Azure Defender.</span><span class="sxs-lookup"><span data-stu-id="dadfd-118">Gets pricing details of the named Azure Defender plan.</span></span> <span data-ttu-id="dadfd-119">Onde `name` está um dos nomes retornados por `Get-AzSecurityPricing` .</span><span class="sxs-lookup"><span data-stu-id="dadfd-119">Where `name` is one of the names returned by `Get-AzSecurityPricing`.</span></span>


## <span data-ttu-id="dadfd-120">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="dadfd-120">PARAMETERS</span></span>

### <span data-ttu-id="dadfd-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dadfd-121">-DefaultProfile</span></span>

<span data-ttu-id="dadfd-122">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="dadfd-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dadfd-123">-Name</span><span class="sxs-lookup"><span data-stu-id="dadfd-123">-Name</span></span>

<span data-ttu-id="dadfd-124">Nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="dadfd-124">Resource name.</span></span>

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

### <span data-ttu-id="dadfd-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dadfd-125">-ResourceId</span></span>

<span data-ttu-id="dadfd-126">ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="dadfd-126">Resource ID.</span></span>

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

### <span data-ttu-id="dadfd-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dadfd-127">CommonParameters</span></span>

<span data-ttu-id="dadfd-128">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dadfd-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dadfd-129">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dadfd-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dadfd-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="dadfd-130">INPUTS</span></span>

### <span data-ttu-id="dadfd-131">System.String</span><span class="sxs-lookup"><span data-stu-id="dadfd-131">System.String</span></span>

## <span data-ttu-id="dadfd-132">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="dadfd-132">OUTPUTS</span></span>

### <span data-ttu-id="dadfd-133">Microsoft.Azure.Commands.Security.Models.Pricings.PSSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="dadfd-133">Microsoft.Azure.Commands.Security.Models.Pricings.PSSecurityPricing</span></span>

## <span data-ttu-id="dadfd-134">NOTES</span><span class="sxs-lookup"><span data-stu-id="dadfd-134">NOTES</span></span>

## <span data-ttu-id="dadfd-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="dadfd-135">RELATED LINKS</span></span>

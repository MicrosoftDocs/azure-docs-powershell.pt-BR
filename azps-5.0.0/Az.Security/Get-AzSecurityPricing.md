---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityPricing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityPricing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityPricing.md
ms.openlocfilehash: a1b07c5fb76d912ec117d42497f0d0b14bfb298c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94116552"
---
# <span data-ttu-id="a578c-101">Get-AzSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="a578c-101">Get-AzSecurityPricing</span></span>

## <span data-ttu-id="a578c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a578c-102">SYNOPSIS</span></span>
<span data-ttu-id="a578c-103">Obtém os dados da camada de preços do Azure Security Center para um escopo.</span><span class="sxs-lookup"><span data-stu-id="a578c-103">Gets the pricing tier data for Azure Security Center for a scope.</span></span>

## <span data-ttu-id="a578c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a578c-104">SYNTAX</span></span>

### <span data-ttu-id="a578c-105">SubscriptionScope (padrão)</span><span class="sxs-lookup"><span data-stu-id="a578c-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityPricing [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a578c-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="a578c-106">SubscriptionLevelResource</span></span>
```
Get-AzSecurityPricing -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a578c-107">Identificação</span><span class="sxs-lookup"><span data-stu-id="a578c-107">ResourceId</span></span>
```
Get-AzSecurityPricing -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a578c-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a578c-108">DESCRIPTION</span></span>
<span data-ttu-id="a578c-109">O tipo de preço da central de segurança do Azure é decidido por escopo, com esse cmdlet você pode obter os tipos de preços configurados.</span><span class="sxs-lookup"><span data-stu-id="a578c-109">Azure Security Center pricing tier is decided per scope, with this cmdlet you can get the configured pricing tiers.</span></span>
<span data-ttu-id="a578c-110">O tipo de preço da assinatura inclui todos os grupos de recursos abaixo dele.</span><span class="sxs-lookup"><span data-stu-id="a578c-110">Subscription pricing tier include all the resource groups under it.</span></span>
<span data-ttu-id="a578c-111">O tipo de preço do grupo de recursos substituirá o tipo de preço da assinatura.</span><span class="sxs-lookup"><span data-stu-id="a578c-111">Resource Group pricing tier will override the subscription pricing tier.</span></span>

## <span data-ttu-id="a578c-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a578c-112">EXAMPLES</span></span>

### <span data-ttu-id="a578c-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a578c-113">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityPricing
Id                                                                                                                             Name       PricingTier
--                                                                                                                             ----       -----------
Id--/subscriptions/fbaa2b23-e9dd-4bed-93c1-9e2a44f64bc0/providers/Microsoft.Security/pricings/VirtualMachines
--                                                                                                                             ----       -----------
/subscriptions/fbaa2b23-e9dd-4bed-93c1-9e2a44f64bc0/providers/Microsoft.Security/pricings/SqlServers
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/pricings/default                              default    Standard
/subscriptions/fbaa2b23-e9dd-4bed-93c1-9e2a44f64bc0/providers/Microsoft.Security/pricings/AppServices
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/pricings/myService1 myService1 Standard
/subscriptions/fbaa2b23-e9dd-4bed-93c1-9e2a44f64bc0/providers/Microsoft.Security/pricings/StorageAccounts
/subscriptions/fbaa2b23-e9dd-4bed-93c1-9e2a44f64bc0/providers/Microsoft.Security/pricings/SqlServerVirtualMachin…
/subscriptions/fbaa2b23-e9dd-4bed-93c1-9e2a44f64bc0/providers/Microsoft.Security/pricings/KubernetesService
/subscriptions/fbaa2b23-e9dd-4bed-93c1-9e2a44f64bc0/providers/Microsoft.Security/pricings/ContainerRegistry
/subscriptions/fbaa2b23-e9dd-4bed-93c1-9e2a44f64bc0/providers/Microsoft.Security/pricings/KeyVaults
```

<span data-ttu-id="a578c-114">Obtém todas as faixas de preços configuradas para a assinatura e os grupos de recursos abaixo dela.</span><span class="sxs-lookup"><span data-stu-id="a578c-114">Gets all the configured pricing tiers for the subscription and the resource groups under it.</span></span>

### <span data-ttu-id="a578c-115">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="a578c-115">Example 2</span></span>
```powershell
PS C:\> Get-AzSecurityPricing -ResourceGroupName "myService1"
Id                                                                                                                             Name       PricingTier
--                                                                                                                             ----       -----------
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/pricings/myService1 myService1 Standard
```

<span data-ttu-id="a578c-116">Obtém a camada de preços configurada para o grupo de recursos "myService1".</span><span class="sxs-lookup"><span data-stu-id="a578c-116">Gets the configured pricing tier for the "myService1" resource group.</span></span>

## <span data-ttu-id="a578c-117">OS</span><span class="sxs-lookup"><span data-stu-id="a578c-117">PARAMETERS</span></span>

### <span data-ttu-id="a578c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a578c-118">-DefaultProfile</span></span>
<span data-ttu-id="a578c-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a578c-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a578c-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="a578c-120">-Name</span></span>
<span data-ttu-id="a578c-121">Nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="a578c-121">Resource name.</span></span>

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

### <span data-ttu-id="a578c-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a578c-122">-ResourceId</span></span>
<span data-ttu-id="a578c-123">ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="a578c-123">Resource ID.</span></span>

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

### <span data-ttu-id="a578c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a578c-124">CommonParameters</span></span>
<span data-ttu-id="a578c-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a578c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a578c-126">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a578c-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a578c-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a578c-127">INPUTS</span></span>

### <span data-ttu-id="a578c-128">System. String</span><span class="sxs-lookup"><span data-stu-id="a578c-128">System.String</span></span>

## <span data-ttu-id="a578c-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a578c-129">OUTPUTS</span></span>

### <span data-ttu-id="a578c-130">Microsoft. Azure. Commands. Security. Models. pricings. PSSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="a578c-130">Microsoft.Azure.Commands.Security.Models.Pricings.PSSecurityPricing</span></span>

## <span data-ttu-id="a578c-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a578c-131">NOTES</span></span>

## <span data-ttu-id="a578c-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a578c-132">RELATED LINKS</span></span>

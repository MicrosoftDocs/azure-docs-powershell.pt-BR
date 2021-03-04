---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Get-AzSecurityAdaptiveNetworkHardening
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdaptiveNetworkHardening.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdaptiveNetworkHardening.md
ms.openlocfilehash: 87b53048ede0a5b2484da18ccd0a2f6a531aa92b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892723"
---
# <span data-ttu-id="06640-101">Get-AzSecurityAdaptiveNetworkHardening</span><span class="sxs-lookup"><span data-stu-id="06640-101">Get-AzSecurityAdaptiveNetworkHardening</span></span>

## <span data-ttu-id="06640-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="06640-102">SYNOPSIS</span></span>
<span data-ttu-id="06640-103">Obtém uma lista de recursos de Proteção de Rede Adaptável no escopo de um recurso estendido.</span><span class="sxs-lookup"><span data-stu-id="06640-103">Gets a list of Adaptive Network Hardenings resources in scope of an extended resource.</span></span>

## <span data-ttu-id="06640-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="06640-104">SYNTAX</span></span>

### <span data-ttu-id="06640-105">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="06640-105">ResourceGroupLevelResource</span></span>
```
Get-AzSecurityAdaptiveNetworkHardening [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```
## <span data-ttu-id="06640-106">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="06640-106">DESCRIPTION</span></span>
<span data-ttu-id="06640-107">Os Hardenings adaptáveis de rede são calculados automaticamente pelo Centro de Segurança do Azure, use este cmdlet para obter uma lista de recursos de Proteção de Rede Adaptável no escopo de um recurso estendido.</span><span class="sxs-lookup"><span data-stu-id="06640-107">Adaptive Network Hardenings are automatically calculated by Azure Security Center, use this cmdlet to get a list of Adaptive Network Hardenings resources in scope of an extended resource.</span></span>

## <span data-ttu-id="06640-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="06640-108">EXAMPLES</span></span>

### <span data-ttu-id="06640-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="06640-109">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityAdaptiveNetworkHardening -ResourceGroupName myService1 -ResourceName myResource1 -ResourceNamespace Microsoft.Compute -ResourceType virtualMachines -SubscriptionId 3eeab341-f466-499c-a8be-85427e154baf7612f869

Id                                                                                                                                                                                                                      Name    Type                                         Properties
--                                                                                                                                                                                                                      ----    ----                                         ----------
/subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/myResource1/providers/Microsoft.Security/adaptiveNetworkHardenings/default default Microsoft.Security/adaptiveNetworkHardenings Microsoft.Azure.Commands.SecurityCenter.Models…
```

<span data-ttu-id="06640-110">Obtém uma lista de recursos de Proteção de Rede Adaptável no escopo de um recurso estendido.</span><span class="sxs-lookup"><span data-stu-id="06640-110">Gets a list of Adaptive Network Hardenings resources in scope of an extended resource.</span></span>

### <span data-ttu-id="06640-111">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="06640-111">Example 2</span></span>
```powershell
PS C:\> Get-AzSecurityAdaptiveNetworkHardening -AdaptiveNetworkHardeningResourceName default -ResourceGroupName myService1 -ResourceName myResource1 -ResourceNamespace Microsoft.Compute -ResourceType virtualMachines -SubscriptionId 3eeab341-f466-499c-a8be-85427e154baf7612f869

Id                                                                                                                                                                                                                      Name    Type                                         Properties
--                                                                                                                                                                                                                      ----    ----                                         ----------
/subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/myResource1/providers/Microsoft.Security/adaptiveNetworkHardenings/default default Microsoft.Security/adaptiveNetworkHardenings Microsoft.Azure.Commands.SecurityCenter.Models…
```
<span data-ttu-id="06640-112">Obter um único recurso Adaptive Network Hardenings</span><span class="sxs-lookup"><span data-stu-id="06640-112">Get  a single Adaptive Network Hardenings resource</span></span>

## <span data-ttu-id="06640-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="06640-113">PARAMETERS</span></span>

### <span data-ttu-id="06640-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06640-114">-DefaultProfile</span></span>
<span data-ttu-id="06640-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="06640-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="06640-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06640-116">-ResourceGroupName</span></span>
<span data-ttu-id="06640-117">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="06640-117">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06640-118">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="06640-118">-ResourceName</span></span>
<span data-ttu-id="06640-119">Nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="06640-119">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06640-120">-ResourceNamespace</span><span class="sxs-lookup"><span data-stu-id="06640-120">-ResourceNamespace</span></span>
<span data-ttu-id="06640-121">O Namespace do recurso.</span><span class="sxs-lookup"><span data-stu-id="06640-121">The Namespace of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNamespace
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06640-122">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="06640-122">-ResourceType</span></span>
<span data-ttu-id="06640-123">O tipo do recurso.</span><span class="sxs-lookup"><span data-stu-id="06640-123">The type of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceType
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06640-124">-AdaptiveNetworkHardeningResourceName</span><span class="sxs-lookup"><span data-stu-id="06640-124">-AdaptiveNetworkHardeningResourceName</span></span>
<span data-ttu-id="06640-125">O nome do recurso de Proteção de Rede Adaptável.</span><span class="sxs-lookup"><span data-stu-id="06640-125">The name of the Adaptive Network Hardening resource.</span></span>

```yaml
Type: System.String
Parameter Sets: AdaptiveNetworkHardeningResourceName
Aliases:

Required: false
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06640-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="06640-126">-SubscriptionId</span></span>
<span data-ttu-id="06640-127">ID da assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="06640-127">Azure subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionId
Aliases:

Required: false
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```
### <span data-ttu-id="06640-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06640-128">CommonParameters</span></span>
<span data-ttu-id="06640-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06640-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06640-130">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06640-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06640-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="06640-131">INPUTS</span></span>

### <span data-ttu-id="06640-132">System.String</span><span class="sxs-lookup"><span data-stu-id="06640-132">System.String</span></span>

## <span data-ttu-id="06640-133">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="06640-133">OUTPUTS</span></span>

### <span data-ttu-id="06640-134">Microsoft.Azure.Commands.Security.Models.AdaptiveNetworkHardenings.PSSecurityAdaptiveNetworkHardenings</span><span class="sxs-lookup"><span data-stu-id="06640-134">Microsoft.Azure.Commands.Security.Models.AdaptiveNetworkHardenings.PSSecurityAdaptiveNetworkHardenings</span></span>

## <span data-ttu-id="06640-135">NOTES</span><span class="sxs-lookup"><span data-stu-id="06640-135">NOTES</span></span>

## <span data-ttu-id="06640-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="06640-136">RELATED LINKS</span></span>
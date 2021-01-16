---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityAdaptiveNetworkHardening
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdaptiveNetworkHardening.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdaptiveNetworkHardening.md
ms.openlocfilehash: cd28e66466239bf7fb0478774c1914180d2ede42
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98271557"
---
# <span data-ttu-id="b9084-101">Get-AzSecurityAdaptiveNetworkHardening</span><span class="sxs-lookup"><span data-stu-id="b9084-101">Get-AzSecurityAdaptiveNetworkHardening</span></span>

## <span data-ttu-id="b9084-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b9084-102">SYNOPSIS</span></span>
<span data-ttu-id="b9084-103">Obtém uma lista de recursos de proteção de rede adaptável no escopo de um recurso estendido.</span><span class="sxs-lookup"><span data-stu-id="b9084-103">Gets a list of Adaptive Network Hardenings resources in scope of an extended resource.</span></span>

## <span data-ttu-id="b9084-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b9084-104">SYNTAX</span></span>

### <span data-ttu-id="b9084-105">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="b9084-105">ResourceGroupLevelResource</span></span>
```
Get-AzSecurityAdaptiveNetworkHardening [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```
## <span data-ttu-id="b9084-106">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b9084-106">DESCRIPTION</span></span>
<span data-ttu-id="b9084-107">As otimizações de rede adaptáveis são calculadas automaticamente pela central de segurança do Azure, use esse cmdlet para obter uma lista de recursos de proteção de rede adaptável no escopo de um recurso estendido.</span><span class="sxs-lookup"><span data-stu-id="b9084-107">Adaptive Network Hardenings are automatically calculated by Azure Security Center, use this cmdlet to get a list of Adaptive Network Hardenings resources in scope of an extended resource.</span></span>

## <span data-ttu-id="b9084-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b9084-108">EXAMPLES</span></span>

### <span data-ttu-id="b9084-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b9084-109">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityAdaptiveNetworkHardening -ResourceGroupName myService1 -ResourceName myResource1 -ResourceNamespace Microsoft.Compute -ResourceType virtualMachines -SubscriptionId 3eeab341-f466-499c-a8be-85427e154baf7612f869

Id                                                                                                                                                                                                                      Name    Type                                         Properties
--                                                                                                                                                                                                                      ----    ----                                         ----------
/subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/myResource1/providers/Microsoft.Security/adaptiveNetworkHardenings/default default Microsoft.Security/adaptiveNetworkHardenings Microsoft.Azure.Commands.SecurityCenter.Models…
```

<span data-ttu-id="b9084-110">Obtém uma lista de recursos de proteção de rede adaptável no escopo de um recurso estendido.</span><span class="sxs-lookup"><span data-stu-id="b9084-110">Gets a list of Adaptive Network Hardenings resources in scope of an extended resource.</span></span>

### <span data-ttu-id="b9084-111">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="b9084-111">Example 2</span></span>
```powershell
PS C:\> Get-AzSecurityAdaptiveNetworkHardening -AdaptiveNetworkHardeningResourceName default -ResourceGroupName myService1 -ResourceName myResource1 -ResourceNamespace Microsoft.Compute -ResourceType virtualMachines -SubscriptionId 3eeab341-f466-499c-a8be-85427e154baf7612f869

Id                                                                                                                                                                                                                      Name    Type                                         Properties
--                                                                                                                                                                                                                      ----    ----                                         ----------
/subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/myResource1/providers/Microsoft.Security/adaptiveNetworkHardenings/default default Microsoft.Security/adaptiveNetworkHardenings Microsoft.Azure.Commands.SecurityCenter.Models…
```
<span data-ttu-id="b9084-112">Obter um único recurso de proteção de rede adaptável</span><span class="sxs-lookup"><span data-stu-id="b9084-112">Get  a single Adaptive Network Hardenings resource</span></span>

## <span data-ttu-id="b9084-113">OS</span><span class="sxs-lookup"><span data-stu-id="b9084-113">PARAMETERS</span></span>

### <span data-ttu-id="b9084-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9084-114">-DefaultProfile</span></span>
<span data-ttu-id="b9084-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b9084-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b9084-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9084-116">-ResourceGroupName</span></span>
<span data-ttu-id="b9084-117">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b9084-117">Resource group name.</span></span>

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

### <span data-ttu-id="b9084-118">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="b9084-118">-ResourceName</span></span>
<span data-ttu-id="b9084-119">Nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="b9084-119">Resource name.</span></span>

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

### <span data-ttu-id="b9084-120">-ResourceNamespace</span><span class="sxs-lookup"><span data-stu-id="b9084-120">-ResourceNamespace</span></span>
<span data-ttu-id="b9084-121">O namespace do recurso.</span><span class="sxs-lookup"><span data-stu-id="b9084-121">The Namespace of the resource.</span></span>

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

### <span data-ttu-id="b9084-122">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="b9084-122">-ResourceType</span></span>
<span data-ttu-id="b9084-123">O tipo do recurso.</span><span class="sxs-lookup"><span data-stu-id="b9084-123">The type of the resource.</span></span>

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

### <span data-ttu-id="b9084-124">-AdaptiveNetworkHardeningResourceName</span><span class="sxs-lookup"><span data-stu-id="b9084-124">-AdaptiveNetworkHardeningResourceName</span></span>
<span data-ttu-id="b9084-125">O nome do recurso de proteção de rede adaptável.</span><span class="sxs-lookup"><span data-stu-id="b9084-125">The name of the Adaptive Network Hardening resource.</span></span>

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

### <span data-ttu-id="b9084-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b9084-126">-SubscriptionId</span></span>
<span data-ttu-id="b9084-127">ID da assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="b9084-127">Azure subscription ID.</span></span>

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
### <span data-ttu-id="b9084-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9084-128">CommonParameters</span></span>
<span data-ttu-id="b9084-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9084-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9084-130">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9084-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9084-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b9084-131">INPUTS</span></span>

### <span data-ttu-id="b9084-132">System. String</span><span class="sxs-lookup"><span data-stu-id="b9084-132">System.String</span></span>

## <span data-ttu-id="b9084-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b9084-133">OUTPUTS</span></span>

### <span data-ttu-id="b9084-134">Microsoft. Azure. Commands. Security. Models. AdaptiveNetworkHardenings. PSSecurityAdaptiveNetworkHardenings</span><span class="sxs-lookup"><span data-stu-id="b9084-134">Microsoft.Azure.Commands.Security.Models.AdaptiveNetworkHardenings.PSSecurityAdaptiveNetworkHardenings</span></span>

## <span data-ttu-id="b9084-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b9084-135">NOTES</span></span>

## <span data-ttu-id="b9084-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b9084-136">RELATED LINKS</span></span>
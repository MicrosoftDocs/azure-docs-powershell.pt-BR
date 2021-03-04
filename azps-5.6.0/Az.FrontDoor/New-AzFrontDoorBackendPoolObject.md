---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/powershell/module/az.frontdoor/new-azfrontdoorbackendpoolobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorBackendPoolObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorBackendPoolObject.md
ms.openlocfilehash: 5cfe83c48950fff7f300b07cf43ba32ff9739606
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887124"
---
# <span data-ttu-id="e0dbd-101">New-AzFrontDoorBackendPoolObject</span><span class="sxs-lookup"><span data-stu-id="e0dbd-101">New-AzFrontDoorBackendPoolObject</span></span>

## <span data-ttu-id="e0dbd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e0dbd-102">SYNOPSIS</span></span>
<span data-ttu-id="e0dbd-103">Criar um objeto PSBackendPool para criação do Front Door</span><span class="sxs-lookup"><span data-stu-id="e0dbd-103">Create a PSBackendPool object for Front Door creation</span></span>

## <span data-ttu-id="e0dbd-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="e0dbd-104">SYNTAX</span></span>

```
New-AzFrontDoorBackendPoolObject -ResourceGroupName <String> -Name <String> -FrontDoorName <String>
 -Backend <PSBackend[]> -LoadBalancingSettingsName <String> -HealthProbeSettingsName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e0dbd-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="e0dbd-105">DESCRIPTION</span></span>
<span data-ttu-id="e0dbd-106">Criar um objeto PSBackendPool para criação do Front Door</span><span class="sxs-lookup"><span data-stu-id="e0dbd-106">Create a PSBackendPool object for Front Door creation</span></span>

## <span data-ttu-id="e0dbd-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e0dbd-107">EXAMPLES</span></span>

### <span data-ttu-id="e0dbd-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e0dbd-108">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorBackendPoolObject -Name "backendpool1" -FrontDoorName $Name -ResourceGroupName $resourceGroupName -Backend $backend1 -He
althProbeSettingsName "healthProbeSetting1" -LoadBalancingSettingsName "loadBalancingSetting1"


Backends                : {Microsoft.Azure.Commands.FrontDoor.Models.PSBackend}
LoadBalancingSettingRef : /subscriptions/{subid}/resourceGroups/{resourceGroupName}/providers
                          /Microsoft.Network/frontDoors/frontdoor5/LoadBalancingSettings/loadBalancingSetting1
HealthProbeSettingRef   : /subscriptions/{subid}/resourceGroups/{resourceGroupName}/providers
                          /Microsoft.Network/frontDoors/frontdoor5/HealthProbeSettings/healthProbeSetting1
EnabledState            : Enabled
ResourceState           :
Id                      :
Name                    : backendpool1
Type                    :
```

<span data-ttu-id="e0dbd-109">Criar um objeto PSBackendPool para criação do Front Door</span><span class="sxs-lookup"><span data-stu-id="e0dbd-109">Create a PSBackendPool object for Front Door creation</span></span>

## <span data-ttu-id="e0dbd-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="e0dbd-110">PARAMETERS</span></span>

### <span data-ttu-id="e0dbd-111">-Backend</span><span class="sxs-lookup"><span data-stu-id="e0dbd-111">-Backend</span></span>
<span data-ttu-id="e0dbd-112">O conjunto de back-ends para esse pool.</span><span class="sxs-lookup"><span data-stu-id="e0dbd-112">The set of backends for this pool.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSBackend[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0dbd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0dbd-113">-DefaultProfile</span></span>
<span data-ttu-id="e0dbd-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e0dbd-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e0dbd-115">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="e0dbd-115">-FrontDoorName</span></span>
<span data-ttu-id="e0dbd-116">O nome da Porta da Frente à qual essa regra de roteamento pertence.</span><span class="sxs-lookup"><span data-stu-id="e0dbd-116">The name of the Front Door to which this routing rule belongs.</span></span>

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

### <span data-ttu-id="e0dbd-117">-HealthProbeSettingsName</span><span class="sxs-lookup"><span data-stu-id="e0dbd-117">-HealthProbeSettingsName</span></span>
<span data-ttu-id="e0dbd-118">O nome das configurações da sonda de saúde para este pool de back-end</span><span class="sxs-lookup"><span data-stu-id="e0dbd-118">The name of the health probe settings for this backend pool</span></span>

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

### <span data-ttu-id="e0dbd-119">-LoadBalancingSettingsName</span><span class="sxs-lookup"><span data-stu-id="e0dbd-119">-LoadBalancingSettingsName</span></span>
<span data-ttu-id="e0dbd-120">O nome das configurações de balanceamento de carga para este pool de back-end</span><span class="sxs-lookup"><span data-stu-id="e0dbd-120">The name of the load balancing settings for this backend pool</span></span>

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

### <span data-ttu-id="e0dbd-121">-Name</span><span class="sxs-lookup"><span data-stu-id="e0dbd-121">-Name</span></span>
<span data-ttu-id="e0dbd-122">Nome do BackendPool.</span><span class="sxs-lookup"><span data-stu-id="e0dbd-122">BackendPool name.</span></span>

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

### <span data-ttu-id="e0dbd-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0dbd-123">-ResourceGroupName</span></span>
<span data-ttu-id="e0dbd-124">O nome do grupo de recursos em que RoutingRule será criado.</span><span class="sxs-lookup"><span data-stu-id="e0dbd-124">The resource group name that the RoutingRule will be created in.</span></span>

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

### <span data-ttu-id="e0dbd-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0dbd-125">CommonParameters</span></span>
<span data-ttu-id="e0dbd-126">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0dbd-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0dbd-127">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e0dbd-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0dbd-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e0dbd-128">INPUTS</span></span>

### <span data-ttu-id="e0dbd-129">Nenhum</span><span class="sxs-lookup"><span data-stu-id="e0dbd-129">None</span></span>

## <span data-ttu-id="e0dbd-130">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="e0dbd-130">OUTPUTS</span></span>

### <span data-ttu-id="e0dbd-131">Microsoft.Azure.Commands.FrontDoor.Models.PSBackendPool</span><span class="sxs-lookup"><span data-stu-id="e0dbd-131">Microsoft.Azure.Commands.FrontDoor.Models.PSBackendPool</span></span>

## <span data-ttu-id="e0dbd-132">NOTES</span><span class="sxs-lookup"><span data-stu-id="e0dbd-132">NOTES</span></span>

## <span data-ttu-id="e0dbd-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e0dbd-133">RELATED LINKS</span></span>

<span data-ttu-id="e0dbd-134">[New-AzFrontDoor](./New-AzFrontDoor.md) 
 [Set-AzFrontDoor](./Set-AzFrontDoor.md) 
 [New-AzFrontDoorBackendObject](./New-AzFrontDoorBackendObject.md)</span><span class="sxs-lookup"><span data-stu-id="e0dbd-134">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)
[New-AzFrontDoorBackendObject](./New-AzFrontDoorBackendObject.md)</span></span>

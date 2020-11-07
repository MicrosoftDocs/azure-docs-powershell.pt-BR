---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorbackendpoolobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorBackendPoolObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorBackendPoolObject.md
ms.openlocfilehash: 6dba24ae79d051668e88a718402c5e01e81a7461
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93947763"
---
# <span data-ttu-id="d68f5-101">New-AzFrontDoorBackendPoolObject</span><span class="sxs-lookup"><span data-stu-id="d68f5-101">New-AzFrontDoorBackendPoolObject</span></span>

## <span data-ttu-id="d68f5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d68f5-102">SYNOPSIS</span></span>
<span data-ttu-id="d68f5-103">Criar um objeto PSBackendPool para a criação da porta frontal</span><span class="sxs-lookup"><span data-stu-id="d68f5-103">Create a PSBackendPool object for Front Door creation</span></span>

## <span data-ttu-id="d68f5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d68f5-104">SYNTAX</span></span>

```
New-AzFrontDoorBackendPoolObject -ResourceGroupName <String> -Name <String> -FrontDoorName <String>
 -Backend <PSBackend[]> -LoadBalancingSettingsName <String> -HealthProbeSettingsName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d68f5-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d68f5-105">DESCRIPTION</span></span>
<span data-ttu-id="d68f5-106">Criar um objeto PSBackendPool para a criação da porta frontal</span><span class="sxs-lookup"><span data-stu-id="d68f5-106">Create a PSBackendPool object for Front Door creation</span></span>

## <span data-ttu-id="d68f5-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d68f5-107">EXAMPLES</span></span>

### <span data-ttu-id="d68f5-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d68f5-108">Example 1</span></span>
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

<span data-ttu-id="d68f5-109">Criar um objeto PSBackendPool para a criação da porta frontal</span><span class="sxs-lookup"><span data-stu-id="d68f5-109">Create a PSBackendPool object for Front Door creation</span></span>

## <span data-ttu-id="d68f5-110">OS</span><span class="sxs-lookup"><span data-stu-id="d68f5-110">PARAMETERS</span></span>

### <span data-ttu-id="d68f5-111">-Back-end</span><span class="sxs-lookup"><span data-stu-id="d68f5-111">-Backend</span></span>
<span data-ttu-id="d68f5-112">O conjunto de back-ends para este pool.</span><span class="sxs-lookup"><span data-stu-id="d68f5-112">The set of backends for this pool.</span></span>

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

### <span data-ttu-id="d68f5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d68f5-113">-DefaultProfile</span></span>
<span data-ttu-id="d68f5-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d68f5-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d68f5-115">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="d68f5-115">-FrontDoorName</span></span>
<span data-ttu-id="d68f5-116">O nome da porta frontal à qual esta regra de roteamento pertence.</span><span class="sxs-lookup"><span data-stu-id="d68f5-116">The name of the Front Door to which this routing rule belongs.</span></span>

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

### <span data-ttu-id="d68f5-117">-HealthProbeSettingsName</span><span class="sxs-lookup"><span data-stu-id="d68f5-117">-HealthProbeSettingsName</span></span>
<span data-ttu-id="d68f5-118">O nome das configurações de investigação de integridade para este pool de back-end</span><span class="sxs-lookup"><span data-stu-id="d68f5-118">The name of the health probe settings for this backend pool</span></span>

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

### <span data-ttu-id="d68f5-119">-LoadBalancingSettingsName</span><span class="sxs-lookup"><span data-stu-id="d68f5-119">-LoadBalancingSettingsName</span></span>
<span data-ttu-id="d68f5-120">O nome das configurações de balanceamento de carga para este pool de back-end</span><span class="sxs-lookup"><span data-stu-id="d68f5-120">The name of the load balancing settings for this backend pool</span></span>

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

### <span data-ttu-id="d68f5-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="d68f5-121">-Name</span></span>
<span data-ttu-id="d68f5-122">Nome do BackendPool.</span><span class="sxs-lookup"><span data-stu-id="d68f5-122">BackendPool name.</span></span>

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

### <span data-ttu-id="d68f5-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d68f5-123">-ResourceGroupName</span></span>
<span data-ttu-id="d68f5-124">O nome do grupo de recursos no qual o RoutingRule será criado.</span><span class="sxs-lookup"><span data-stu-id="d68f5-124">The resource group name that the RoutingRule will be created in.</span></span>

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

### <span data-ttu-id="d68f5-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d68f5-125">CommonParameters</span></span>
<span data-ttu-id="d68f5-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d68f5-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d68f5-127">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d68f5-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d68f5-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d68f5-128">INPUTS</span></span>

### <span data-ttu-id="d68f5-129">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="d68f5-129">None</span></span>

## <span data-ttu-id="d68f5-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d68f5-130">OUTPUTS</span></span>

### <span data-ttu-id="d68f5-131">Microsoft. Azure. Commands. FrontDoor. Models. PSBackendPool</span><span class="sxs-lookup"><span data-stu-id="d68f5-131">Microsoft.Azure.Commands.FrontDoor.Models.PSBackendPool</span></span>

## <span data-ttu-id="d68f5-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d68f5-132">NOTES</span></span>

## <span data-ttu-id="d68f5-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d68f5-133">RELATED LINKS</span></span>

<span data-ttu-id="d68f5-134">[New-AzFrontDoor](./New-AzFrontDoor.md) 
 [Set-AzFrontDoor](./Set-AzFrontDoor.md) 
 [New-AzFrontDoorBackendObject](./New-AzFrontDoorBackendObject.md)</span><span class="sxs-lookup"><span data-stu-id="d68f5-134">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)
[New-AzFrontDoorBackendObject](./New-AzFrontDoorBackendObject.md)</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherconnectionmonitorendpointobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorEndpointObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorEndpointObject.md
ms.openlocfilehash: 58e26de74abb46234f6985c3973b5bbe494bd0ad
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93941029"
---
# <span data-ttu-id="bd43f-101">New-AzNetworkWatcherConnectionMonitorEndpointObject</span><span class="sxs-lookup"><span data-stu-id="bd43f-101">New-AzNetworkWatcherConnectionMonitorEndpointObject</span></span>

## <span data-ttu-id="bd43f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bd43f-102">SYNOPSIS</span></span>
<span data-ttu-id="bd43f-103">Cria um ponto de extremidade do monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="bd43f-103">Creates connection monitor endpoint.</span></span>

## <span data-ttu-id="bd43f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bd43f-104">SYNTAX</span></span>

### <span data-ttu-id="bd43f-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="bd43f-105">SetByResourceId</span></span>
```
New-AzNetworkWatcherConnectionMonitorEndpointObject [-Name <String>] -ResourceId <String>
 [-FilterType <String>]
 [-FilterItem <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorEndpointFilterItem]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bd43f-106">SetByAddress</span><span class="sxs-lookup"><span data-stu-id="bd43f-106">SetByAddress</span></span>
```
New-AzNetworkWatcherConnectionMonitorEndpointObject [-Name <String>] [-Address <String>] [-FilterType <String>]
 [-FilterItem <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorEndpointFilterItem]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bd43f-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="bd43f-107">DESCRIPTION</span></span>
<span data-ttu-id="bd43f-108">New-AzNetworkWatcherConnectionMonitorEndpointObject cmdlet cria um ponto de extremidade de monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="bd43f-108">New-AzNetworkWatcherConnectionMonitorEndpointObject cmdlet creates connection monitor endpoint.</span></span>

## <span data-ttu-id="bd43f-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bd43f-109">EXAMPLES</span></span>

### <span data-ttu-id="bd43f-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="bd43f-110">Example 1</span></span>
```powershell
PS C:\>$MySrcResourceId1 = "/subscriptions/00000000-0000-0000-0000-000000000000/resourcegroups/myresourceGroup/providers/Microsoft.OperationalInsights/workspaces/myworkspace"
PS C:\>$SrcEndpointFilterItem1 =New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject -Type "AgentAddress" -Address "WIN-P0HGNDO2S1B"
PS C:\>$SourceEndpointObject1 = New-AzNetworkWatcherConnectionMonitorEndPointObject -Name "workspaceEndpoint" -ResourceId $MySrcResourceId1 -FilterType Include -FilterItem $SrcEndpointFilterItem1
```

<span data-ttu-id="bd43f-111">Nome: workspaceEndpoint ResourceId:/subscriptions/00000000-0000-0000-0000-000000000000/resourcegroups/myresourceGroup/providers/Microsoft.OperationalInsights/workspaces/myworkspace endereço: filtro: {"tipo": "endereço": "WIN-P0HGNDO2S1B"}]}, "endereço": "WIN-"}]}</span><span class="sxs-lookup"><span data-stu-id="bd43f-111">Name       : workspaceEndpoint ResourceId : /subscriptions/00000000-0000-0000-0000-000000000000/resourcegroups/myresourceGroup/providers/Microsoft.OperationalInsights/workspaces/myworkspace Address    : Filter     : { "Type": "Include", "Items": [ { "Type": "AgentAddress", "Address": "WIN-P0HGNDO2S1B" } ] }</span></span>

## <span data-ttu-id="bd43f-112">OS</span><span class="sxs-lookup"><span data-stu-id="bd43f-112">PARAMETERS</span></span>

### <span data-ttu-id="bd43f-113">-Endereço</span><span class="sxs-lookup"><span data-stu-id="bd43f-113">-Address</span></span>
<span data-ttu-id="bd43f-114">Endereço do ponto de extremidade do monitor de conexão (IP ou nome do domínio).</span><span class="sxs-lookup"><span data-stu-id="bd43f-114">Address of the connection monitor endpoint (IP or domain name).</span></span>

```yaml
Type: System.String
Parameter Sets: SetByAddress
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd43f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd43f-115">-DefaultProfile</span></span>
<span data-ttu-id="bd43f-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bd43f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bd43f-117">-FilterItem</span><span class="sxs-lookup"><span data-stu-id="bd43f-117">-FilterItem</span></span>
<span data-ttu-id="bd43f-118">Lista de itens no filtro.</span><span class="sxs-lookup"><span data-stu-id="bd43f-118">List of items in the filter.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorEndpointFilterItem]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd43f-119">-FilterType</span><span class="sxs-lookup"><span data-stu-id="bd43f-119">-FilterType</span></span>
<span data-ttu-id="bd43f-120">O comportamento do filtro de ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="bd43f-120">The behavior of the endpoint filter.</span></span> <span data-ttu-id="bd43f-121">Atualmente há suporte para ' include ' apenas.</span><span class="sxs-lookup"><span data-stu-id="bd43f-121">Currently only 'Include' is supported.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd43f-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="bd43f-122">-Name</span></span>
<span data-ttu-id="bd43f-123">O nome do ponto de extremidade do monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="bd43f-123">The name of the connection monitor endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd43f-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bd43f-124">-ResourceId</span></span>
<span data-ttu-id="bd43f-125">ID do recurso do ponto de extremidade do monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="bd43f-125">Resource ID of the connection monitor endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd43f-126">-Confirme</span><span class="sxs-lookup"><span data-stu-id="bd43f-126">-Confirm</span></span>
<span data-ttu-id="bd43f-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bd43f-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd43f-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bd43f-128">-WhatIf</span></span>
<span data-ttu-id="bd43f-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="bd43f-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bd43f-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="bd43f-130">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd43f-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd43f-131">CommonParameters</span></span>
<span data-ttu-id="bd43f-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd43f-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd43f-133">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bd43f-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd43f-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="bd43f-134">INPUTS</span></span>

### <span data-ttu-id="bd43f-135">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="bd43f-135">None</span></span>

## <span data-ttu-id="bd43f-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="bd43f-136">OUTPUTS</span></span>

### <span data-ttu-id="bd43f-137">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcherConnectionMonitorEndpointObject</span><span class="sxs-lookup"><span data-stu-id="bd43f-137">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorEndpointObject</span></span>

## <span data-ttu-id="bd43f-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="bd43f-138">NOTES</span></span>

## <span data-ttu-id="bd43f-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bd43f-139">RELATED LINKS</span></span>

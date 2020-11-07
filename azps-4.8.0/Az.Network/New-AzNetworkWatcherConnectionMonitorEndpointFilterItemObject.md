---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherconnectionmonitorendpointfilteritemobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject.md
ms.openlocfilehash: c06052ee28d849c5d07a941366efd15cbfeefe25
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93954843"
---
# <span data-ttu-id="b30f5-101">New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject</span><span class="sxs-lookup"><span data-stu-id="b30f5-101">New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject</span></span>

## <span data-ttu-id="b30f5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b30f5-102">SYNOPSIS</span></span>
<span data-ttu-id="b30f5-103">Cria um item de filtro de ponto de extremidade de monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="b30f5-103">Creates a connection monitor endpoint filter item.</span></span>

## <span data-ttu-id="b30f5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b30f5-104">SYNTAX</span></span>

```
New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject [-Type <String>]
 [-DefaultProfile <IAzureContextContainer>] -Address <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b30f5-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b30f5-105">DESCRIPTION</span></span>
<span data-ttu-id="b30f5-106">O cmdlet New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject cria um item de filtro de ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="b30f5-106">The New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject cmdlet creates endpoint filter item.</span></span>

## <span data-ttu-id="b30f5-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b30f5-107">EXAMPLES</span></span>

### <span data-ttu-id="b30f5-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b30f5-108">Example 1</span></span>
```powershell
PS C:\> New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject -Type "AgentAddress" -Address "10.0.0.1"
```

<span data-ttu-id="b30f5-109">Tipo: endereço AgentAddress: 10.0.0.1</span><span class="sxs-lookup"><span data-stu-id="b30f5-109">Type    : AgentAddress Address : 10.0.0.1</span></span>

## <span data-ttu-id="b30f5-110">OS</span><span class="sxs-lookup"><span data-stu-id="b30f5-110">PARAMETERS</span></span>

### <span data-ttu-id="b30f5-111">-Endereço</span><span class="sxs-lookup"><span data-stu-id="b30f5-111">-Address</span></span>
<span data-ttu-id="b30f5-112">O endereço do item de filtro.</span><span class="sxs-lookup"><span data-stu-id="b30f5-112">The address of the filter item.</span></span>

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

### <span data-ttu-id="b30f5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b30f5-113">-DefaultProfile</span></span>
<span data-ttu-id="b30f5-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b30f5-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b30f5-115">-Digite</span><span class="sxs-lookup"><span data-stu-id="b30f5-115">-Type</span></span>
<span data-ttu-id="b30f5-116">O tipo de item incluído no filtro.</span><span class="sxs-lookup"><span data-stu-id="b30f5-116">The type of item included in the filter.</span></span> <span data-ttu-id="b30f5-117">No momento, só há suporte para "AgentAddress".</span><span class="sxs-lookup"><span data-stu-id="b30f5-117">Currently only 'AgentAddress' is supported.</span></span>

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

### <span data-ttu-id="b30f5-118">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b30f5-118">-Confirm</span></span>
<span data-ttu-id="b30f5-119">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b30f5-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b30f5-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b30f5-120">-WhatIf</span></span>
<span data-ttu-id="b30f5-121">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b30f5-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b30f5-122">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b30f5-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b30f5-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b30f5-123">CommonParameters</span></span>
<span data-ttu-id="b30f5-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b30f5-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b30f5-125">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b30f5-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b30f5-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b30f5-126">INPUTS</span></span>

### <span data-ttu-id="b30f5-127">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="b30f5-127">None</span></span>

## <span data-ttu-id="b30f5-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b30f5-128">OUTPUTS</span></span>

### <span data-ttu-id="b30f5-129">Microsoft. Azure. Commands. Network. Models. PSConnectionMonitorEndpointFilterItem</span><span class="sxs-lookup"><span data-stu-id="b30f5-129">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorEndpointFilterItem</span></span>

## <span data-ttu-id="b30f5-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b30f5-130">NOTES</span></span>

## <span data-ttu-id="b30f5-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b30f5-131">RELATED LINKS</span></span>

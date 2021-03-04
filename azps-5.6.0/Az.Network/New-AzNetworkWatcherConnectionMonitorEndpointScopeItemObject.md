---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-aznetworkwatcherconnectionmonitorendpointscopeitemobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject.md
ms.openlocfilehash: 298586f11bba29ce44e78bc3c19d4d9fc6be21f2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886201"
---
# <span data-ttu-id="93825-101">New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject</span><span class="sxs-lookup"><span data-stu-id="93825-101">New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject</span></span>

## <span data-ttu-id="93825-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="93825-102">SYNOPSIS</span></span>
<span data-ttu-id="93825-103">Cria um item de escopo do ponto de extremidade do monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="93825-103">Creates a connection monitor endpoint scope item.</span></span>

## <span data-ttu-id="93825-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="93825-104">SYNTAX</span></span>

```
New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject [-DefaultProfile <IAzureContextContainer>]
 -Address <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="93825-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="93825-105">DESCRIPTION</span></span>
<span data-ttu-id="93825-106">O New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject cmdlet cria o item de escopo do ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="93825-106">The New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject cmdlet creates endpoint scope item.</span></span>

## <span data-ttu-id="93825-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="93825-107">EXAMPLES</span></span>

### <span data-ttu-id="93825-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="93825-108">Example 1</span></span>
```powershell
PS C:\> New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject -Address "10.0.1.0/24"
```


## <span data-ttu-id="93825-109">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="93825-109">PARAMETERS</span></span>

### <span data-ttu-id="93825-110">-Address</span><span class="sxs-lookup"><span data-stu-id="93825-110">-Address</span></span>
<span data-ttu-id="93825-111">O endereço do item de escopo.</span><span class="sxs-lookup"><span data-stu-id="93825-111">The address of the scope item.</span></span>

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

### <span data-ttu-id="93825-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93825-112">-DefaultProfile</span></span>
<span data-ttu-id="93825-113">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="93825-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="93825-114">-Confirm</span><span class="sxs-lookup"><span data-stu-id="93825-114">-Confirm</span></span>
<span data-ttu-id="93825-115">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="93825-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="93825-116">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="93825-116">-WhatIf</span></span>
<span data-ttu-id="93825-117">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="93825-117">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="93825-118">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="93825-118">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="93825-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93825-119">CommonParameters</span></span>
<span data-ttu-id="93825-120">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93825-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93825-121">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="93825-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93825-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="93825-122">INPUTS</span></span>

### <span data-ttu-id="93825-123">Nenhum</span><span class="sxs-lookup"><span data-stu-id="93825-123">None</span></span>

## <span data-ttu-id="93825-124">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="93825-124">OUTPUTS</span></span>

### <span data-ttu-id="93825-125">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorEndpointScopeItem</span><span class="sxs-lookup"><span data-stu-id="93825-125">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorEndpointScopeItem</span></span>

## <span data-ttu-id="93825-126">NOTES</span><span class="sxs-lookup"><span data-stu-id="93825-126">NOTES</span></span>

## <span data-ttu-id="93825-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="93825-127">RELATED LINKS</span></span>

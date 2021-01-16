---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherconnectionmonitorendpointscopeitemobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject.md
ms.openlocfilehash: c0ca9e257c0686aa0f4589ef4166fec150f41967
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98258459"
---
# <span data-ttu-id="4e4d5-101">New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject</span><span class="sxs-lookup"><span data-stu-id="4e4d5-101">New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject</span></span>

## <span data-ttu-id="4e4d5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4e4d5-102">SYNOPSIS</span></span>
<span data-ttu-id="4e4d5-103">Cria um item de escopo de ponto de extremidade de monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="4e4d5-103">Creates a connection monitor endpoint scope item.</span></span>

## <span data-ttu-id="4e4d5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4e4d5-104">SYNTAX</span></span>

```
New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject [-DefaultProfile <IAzureContextContainer>]
 -Address <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4e4d5-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4e4d5-105">DESCRIPTION</span></span>
<span data-ttu-id="4e4d5-106">O cmdlet New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject cria um item de escopo de ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="4e4d5-106">The New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject cmdlet creates endpoint scope item.</span></span>

## <span data-ttu-id="4e4d5-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4e4d5-107">EXAMPLES</span></span>

### <span data-ttu-id="4e4d5-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="4e4d5-108">Example 1</span></span>
```powershell
PS C:\> New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject -Address "10.0.1.0/24"
```


## <span data-ttu-id="4e4d5-109">OS</span><span class="sxs-lookup"><span data-stu-id="4e4d5-109">PARAMETERS</span></span>

### <span data-ttu-id="4e4d5-110">-Endereço</span><span class="sxs-lookup"><span data-stu-id="4e4d5-110">-Address</span></span>
<span data-ttu-id="4e4d5-111">O endereço do item de escopo.</span><span class="sxs-lookup"><span data-stu-id="4e4d5-111">The address of the scope item.</span></span>

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

### <span data-ttu-id="4e4d5-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e4d5-112">-DefaultProfile</span></span>
<span data-ttu-id="4e4d5-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4e4d5-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4e4d5-114">-Confirme</span><span class="sxs-lookup"><span data-stu-id="4e4d5-114">-Confirm</span></span>
<span data-ttu-id="4e4d5-115">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4e4d5-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4e4d5-116">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4e4d5-116">-WhatIf</span></span>
<span data-ttu-id="4e4d5-117">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4e4d5-117">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4e4d5-118">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4e4d5-118">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4e4d5-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e4d5-119">CommonParameters</span></span>
<span data-ttu-id="4e4d5-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e4d5-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e4d5-121">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4e4d5-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e4d5-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4e4d5-122">INPUTS</span></span>

### <span data-ttu-id="4e4d5-123">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="4e4d5-123">None</span></span>

## <span data-ttu-id="4e4d5-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4e4d5-124">OUTPUTS</span></span>

### <span data-ttu-id="4e4d5-125">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcherConnectionMonitorEndpointScopeItem</span><span class="sxs-lookup"><span data-stu-id="4e4d5-125">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorEndpointScopeItem</span></span>

## <span data-ttu-id="4e4d5-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4e4d5-126">NOTES</span></span>

## <span data-ttu-id="4e4d5-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4e4d5-127">RELATED LINKS</span></span>

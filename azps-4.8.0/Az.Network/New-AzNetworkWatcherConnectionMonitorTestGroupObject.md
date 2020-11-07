---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherconnectionmonitortestgroupobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorTestGroupObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorTestGroupObject.md
ms.openlocfilehash: af924210c8f1fb465881f054815f874ff5d99429
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93955414"
---
# <span data-ttu-id="3890a-101">New-AzNetworkWatcherConnectionMonitorTestGroupObject</span><span class="sxs-lookup"><span data-stu-id="3890a-101">New-AzNetworkWatcherConnectionMonitorTestGroupObject</span></span>

## <span data-ttu-id="3890a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3890a-102">SYNOPSIS</span></span>
<span data-ttu-id="3890a-103">Crie um grupo de teste do monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="3890a-103">Create a connection monitor test group.</span></span>

## <span data-ttu-id="3890a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3890a-104">SYNTAX</span></span>

```
New-AzNetworkWatcherConnectionMonitorTestGroupObject -Name <String>
 -TestConfiguration <PSNetworkWatcherConnectionMonitorTestConfigurationObject[]>
 -Source <PSNetworkWatcherConnectionMonitorEndpointObject[]>
 -Destination <PSNetworkWatcherConnectionMonitorEndpointObject[]> [-Disable]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3890a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3890a-105">DESCRIPTION</span></span>
<span data-ttu-id="3890a-106">O cmdlet New-AzNetworkWatcherConnectionMonitorTestGroupObject cria um grupo de teste de monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="3890a-106">The New-AzNetworkWatcherConnectionMonitorTestGroupObject cmdlet creates a connection monitor test group.</span></span>

## <span data-ttu-id="3890a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3890a-107">EXAMPLES</span></span>

### <span data-ttu-id="3890a-108">Exemplo 1: criar um grupo de teste com dois pontos de extremidade de 2 testConfigurations, w Source e 2 destinos</span><span class="sxs-lookup"><span data-stu-id="3890a-108">Example 1: Create a test group with 2 testConfigurations, w source and 2 destination endpoints</span></span>

```
$testGroup1 = New-AzNetworkWatcherConnectionMonitorTestGroupObject -Name testGroup1 -TestConfiguration $tcpTestConfiguration, $icmpTestConfiguration -Source $vmEndpoint, $workspaceEndpoint -Destination $bingEndpoint, $googleEndpoint
```

## <span data-ttu-id="3890a-109">OS</span><span class="sxs-lookup"><span data-stu-id="3890a-109">PARAMETERS</span></span>

### <span data-ttu-id="3890a-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3890a-110">-DefaultProfile</span></span>
<span data-ttu-id="3890a-111">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3890a-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3890a-112">-Destino</span><span class="sxs-lookup"><span data-stu-id="3890a-112">-Destination</span></span>
<span data-ttu-id="3890a-113">Lista de pontos de extremidade de destino.</span><span class="sxs-lookup"><span data-stu-id="3890a-113">List of destination endpoints.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorEndpointObject[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3890a-114">-Disable</span><span class="sxs-lookup"><span data-stu-id="3890a-114">-Disable</span></span>
<span data-ttu-id="3890a-115">Sinalizador que indica se o grupo de teste está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="3890a-115">Flag indicating whether test group is disabled.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3890a-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="3890a-116">-Name</span></span>
<span data-ttu-id="3890a-117">O nome do grupo de teste.</span><span class="sxs-lookup"><span data-stu-id="3890a-117">The test group name.</span></span>

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

### <span data-ttu-id="3890a-118">-Fonte</span><span class="sxs-lookup"><span data-stu-id="3890a-118">-Source</span></span>
<span data-ttu-id="3890a-119">Lista de pontos de extremidade de origem.</span><span class="sxs-lookup"><span data-stu-id="3890a-119">List of source endpoints.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorEndpointObject[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3890a-120">-TestConfiguration</span><span class="sxs-lookup"><span data-stu-id="3890a-120">-TestConfiguration</span></span>
<span data-ttu-id="3890a-121">Lista de configurações de teste.</span><span class="sxs-lookup"><span data-stu-id="3890a-121">List of test configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorTestConfigurationObject[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3890a-122">-Confirme</span><span class="sxs-lookup"><span data-stu-id="3890a-122">-Confirm</span></span>
<span data-ttu-id="3890a-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3890a-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3890a-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3890a-124">-WhatIf</span></span>
<span data-ttu-id="3890a-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3890a-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3890a-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3890a-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3890a-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3890a-127">CommonParameters</span></span>
<span data-ttu-id="3890a-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3890a-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3890a-129">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3890a-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3890a-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3890a-130">INPUTS</span></span>

### <span data-ttu-id="3890a-131">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="3890a-131">None</span></span>

## <span data-ttu-id="3890a-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3890a-132">OUTPUTS</span></span>

### <span data-ttu-id="3890a-133">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcherConnectionMonitorTestGroupObject</span><span class="sxs-lookup"><span data-stu-id="3890a-133">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorTestGroupObject</span></span>

## <span data-ttu-id="3890a-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3890a-134">NOTES</span></span>

## <span data-ttu-id="3890a-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3890a-135">RELATED LINKS</span></span>

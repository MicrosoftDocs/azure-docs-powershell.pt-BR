---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherconnectionmonitortestgroupobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorTestGroupObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorTestGroupObject.md
ms.openlocfilehash: af924210c8f1fb465881f054815f874ff5d99429
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118303"
---
# <span data-ttu-id="20b0e-101">New-AzNetworkWatcherConnectionMonitorTestGroupObject</span><span class="sxs-lookup"><span data-stu-id="20b0e-101">New-AzNetworkWatcherConnectionMonitorTestGroupObject</span></span>

## <span data-ttu-id="20b0e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="20b0e-102">SYNOPSIS</span></span>
<span data-ttu-id="20b0e-103">Criar um grupo de teste do monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="20b0e-103">Create a connection monitor test group.</span></span>

## <span data-ttu-id="20b0e-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="20b0e-104">SYNTAX</span></span>

```
New-AzNetworkWatcherConnectionMonitorTestGroupObject -Name <String>
 -TestConfiguration <PSNetworkWatcherConnectionMonitorTestConfigurationObject[]>
 -Source <PSNetworkWatcherConnectionMonitorEndpointObject[]>
 -Destination <PSNetworkWatcherConnectionMonitorEndpointObject[]> [-Disable]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="20b0e-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="20b0e-105">DESCRIPTION</span></span>
<span data-ttu-id="20b0e-106">O New-AzNetworkWatcherConnectionMonitorTestGroupObject cmdlet cria um grupo de teste do monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="20b0e-106">The New-AzNetworkWatcherConnectionMonitorTestGroupObject cmdlet creates a connection monitor test group.</span></span>

## <span data-ttu-id="20b0e-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="20b0e-107">EXAMPLES</span></span>

### <span data-ttu-id="20b0e-108">Exemplo 1: Criar um grupo de teste com 2 testConfigurações, w source e 2 pontos de extremidade de destino</span><span class="sxs-lookup"><span data-stu-id="20b0e-108">Example 1: Create a test group with 2 testConfigurations, w source and 2 destination endpoints</span></span>

```
$testGroup1 = New-AzNetworkWatcherConnectionMonitorTestGroupObject -Name testGroup1 -TestConfiguration $tcpTestConfiguration, $icmpTestConfiguration -Source $vmEndpoint, $workspaceEndpoint -Destination $bingEndpoint, $googleEndpoint
```

## <span data-ttu-id="20b0e-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="20b0e-109">PARAMETERS</span></span>

### <span data-ttu-id="20b0e-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20b0e-110">-DefaultProfile</span></span>
<span data-ttu-id="20b0e-111">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="20b0e-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="20b0e-112">-Destino</span><span class="sxs-lookup"><span data-stu-id="20b0e-112">-Destination</span></span>
<span data-ttu-id="20b0e-113">Lista de pontos de extremidade de destino.</span><span class="sxs-lookup"><span data-stu-id="20b0e-113">List of destination endpoints.</span></span>

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

### <span data-ttu-id="20b0e-114">-Desabilitar</span><span class="sxs-lookup"><span data-stu-id="20b0e-114">-Disable</span></span>
<span data-ttu-id="20b0e-115">Sinalizador indicando se o grupo de teste está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="20b0e-115">Flag indicating whether test group is disabled.</span></span>

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

### <span data-ttu-id="20b0e-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="20b0e-116">-Name</span></span>
<span data-ttu-id="20b0e-117">O nome do grupo de teste.</span><span class="sxs-lookup"><span data-stu-id="20b0e-117">The test group name.</span></span>

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

### <span data-ttu-id="20b0e-118">-Origem</span><span class="sxs-lookup"><span data-stu-id="20b0e-118">-Source</span></span>
<span data-ttu-id="20b0e-119">Lista de pontos de extremidade de origem.</span><span class="sxs-lookup"><span data-stu-id="20b0e-119">List of source endpoints.</span></span>

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

### <span data-ttu-id="20b0e-120">-TestConfiguration</span><span class="sxs-lookup"><span data-stu-id="20b0e-120">-TestConfiguration</span></span>
<span data-ttu-id="20b0e-121">Lista de configurações de teste.</span><span class="sxs-lookup"><span data-stu-id="20b0e-121">List of test configuration.</span></span>

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

### <span data-ttu-id="20b0e-122">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="20b0e-122">-Confirm</span></span>
<span data-ttu-id="20b0e-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="20b0e-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="20b0e-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="20b0e-124">-WhatIf</span></span>
<span data-ttu-id="20b0e-125">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="20b0e-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="20b0e-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="20b0e-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="20b0e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20b0e-127">CommonParameters</span></span>
<span data-ttu-id="20b0e-128">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20b0e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20b0e-129">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="20b0e-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20b0e-130">Entradas</span><span class="sxs-lookup"><span data-stu-id="20b0e-130">INPUTS</span></span>

### <span data-ttu-id="20b0e-131">Nenhum</span><span class="sxs-lookup"><span data-stu-id="20b0e-131">None</span></span>

## <span data-ttu-id="20b0e-132">Saídas</span><span class="sxs-lookup"><span data-stu-id="20b0e-132">OUTPUTS</span></span>

### <span data-ttu-id="20b0e-133">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorTestGroupObject</span><span class="sxs-lookup"><span data-stu-id="20b0e-133">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorTestGroupObject</span></span>

## <span data-ttu-id="20b0e-134">Notas</span><span class="sxs-lookup"><span data-stu-id="20b0e-134">NOTES</span></span>

## <span data-ttu-id="20b0e-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="20b0e-135">RELATED LINKS</span></span>

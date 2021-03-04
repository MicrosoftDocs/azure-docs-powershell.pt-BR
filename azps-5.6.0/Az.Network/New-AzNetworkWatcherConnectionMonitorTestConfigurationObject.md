---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-aznetworkwatcherconnectionmonitortestconfigurationobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorTestConfigurationObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorTestConfigurationObject.md
ms.openlocfilehash: 542a207e60e451d97ba5edcbdccc45b84b14f760
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886190"
---
# <span data-ttu-id="a5e32-101">New-AzNetworkWatcherConnectionMonitorTestConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="a5e32-101">New-AzNetworkWatcherConnectionMonitorTestConfigurationObject</span></span>

## <span data-ttu-id="a5e32-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a5e32-102">SYNOPSIS</span></span>
<span data-ttu-id="a5e32-103">Crie uma configuração de teste do monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="a5e32-103">Create a connection monitor test configuration.</span></span>

## <span data-ttu-id="a5e32-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="a5e32-104">SYNTAX</span></span>

```
New-AzNetworkWatcherConnectionMonitorTestConfigurationObject -Name <String> -TestFrequencySec <Int32>
 -ProtocolConfiguration <PSNetworkWatcherConnectionMonitorProtocolConfiguration>
 [-SuccessThresholdChecksFailedPercent <Int32>] [-SuccessThresholdRoundTripTimeMs <Double>]
 [-PreferredIPVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a5e32-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="a5e32-105">DESCRIPTION</span></span>
<span data-ttu-id="a5e32-106">O cmdlet New-AzNetworkWatcherConnectionMonitorTestConfigurationObject cria uma configuração de teste do monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="a5e32-106">The New-AzNetworkWatcherConnectionMonitorTestConfigurationObject cmdlet creates a connection monitor test configuration.</span></span>

## <span data-ttu-id="a5e32-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a5e32-107">EXAMPLES</span></span>

### <span data-ttu-id="a5e32-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a5e32-108">Example 1</span></span>
```powershell
PS C:\>$httpProtocolConfiguration = New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject -HttpProtocol -Port 443 -Method GET -RequestHeader @{"Allow" = "GET"} -ValidStatusCodeRange 2xx, 300-308 -PreferHTTPS
PS C:\>$httpTestConfiguration = New-AzNetworkWatcherConnectionMonitorTestConfigurationObject -Name httpTC -TestFrequencySec 120 -ProtocolConfiguration $httpProtocolConfiguration -SuccessThresholdChecksFailedPercent 20 -SuccessThresholdRoundTripTimeMs 30
```

<span data-ttu-id="a5e32-109">Nome : httpTC TestFrequencySec : 120 PreferredIPVersion : ProtocolConfiguration : { "Porta": 443, "Método": "GET", "RequestHeaders": [ { "Name": "Allow", "Value": "GET" } ], "ValidStatusCodeRanges": [ "2xx", "300-308" ], "PreferHTTPS": true } SuccessThreshold : { "ChecksFailedPercent": 20, "RoundTripTimeMs": 30 }</span><span class="sxs-lookup"><span data-stu-id="a5e32-109">Name                  : httpTC TestFrequencySec      : 120 PreferredIPVersion    : ProtocolConfiguration : { "Port": 443, "Method": "GET", "RequestHeaders": [ { "Name": "Allow", "Value": "GET" } ], "ValidStatusCodeRanges": [ "2xx", "300-308" ], "PreferHTTPS": true } SuccessThreshold      : { "ChecksFailedPercent": 20, "RoundTripTimeMs": 30 }</span></span> 

## <span data-ttu-id="a5e32-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="a5e32-110">PARAMETERS</span></span>

### <span data-ttu-id="a5e32-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5e32-111">-DefaultProfile</span></span>
<span data-ttu-id="a5e32-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a5e32-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a5e32-113">-Name</span><span class="sxs-lookup"><span data-stu-id="a5e32-113">-Name</span></span>
<span data-ttu-id="a5e32-114">O nome da configuração de teste do monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="a5e32-114">The name of the connection monitor test configuration.</span></span>

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

### <span data-ttu-id="a5e32-115">-PreferredIPVersion</span><span class="sxs-lookup"><span data-stu-id="a5e32-115">-PreferredIPVersion</span></span>
<span data-ttu-id="a5e32-116">A versão IP preferida a ser usada na avaliação de teste.</span><span class="sxs-lookup"><span data-stu-id="a5e32-116">The preferred IP version to use in test evaluation.</span></span> <span data-ttu-id="a5e32-117">O monitor de conexão pode optar por usar uma versão diferente, dependendo de outros parâmetros.</span><span class="sxs-lookup"><span data-stu-id="a5e32-117">The connection monitor may choose to use a different version depending on other parameters.</span></span>

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

### <span data-ttu-id="a5e32-118">-ProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="a5e32-118">-ProtocolConfiguration</span></span>
<span data-ttu-id="a5e32-119">Os parâmetros usados para executar a avaliação de teste em relação a algum protocolo.</span><span class="sxs-lookup"><span data-stu-id="a5e32-119">The parameters used to perform test evaluation over some protocol.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorProtocolConfiguration
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5e32-120">-SuccessThresholdChecksFailedPercent</span><span class="sxs-lookup"><span data-stu-id="a5e32-120">-SuccessThresholdChecksFailedPercent</span></span>
<span data-ttu-id="a5e32-121">A porcentagem máxima de verificações com falha permitida para um teste ser avaliada como bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="a5e32-121">The maximum percentage of failed checks permitted for a test to evaluate as successful.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5e32-122">-SuccessThresholdRoundTripTimeMs</span><span class="sxs-lookup"><span data-stu-id="a5e32-122">-SuccessThresholdRoundTripTimeMs</span></span>
<span data-ttu-id="a5e32-123">O tempo máximo de ida e volta em milissegundos permitidos para um teste ser avaliada como bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="a5e32-123">The maximum round-trip time in milliseconds permitted for a test to evaluate as successful.</span></span>

```yaml
Type: System.Nullable`1[System.Double]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5e32-124">-TestFrequencySec</span><span class="sxs-lookup"><span data-stu-id="a5e32-124">-TestFrequencySec</span></span>
<span data-ttu-id="a5e32-125">A frequência da avaliação de teste, em segundos.</span><span class="sxs-lookup"><span data-stu-id="a5e32-125">The frequency of test evaluation, in seconds.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: TestFrequency

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5e32-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a5e32-126">-Confirm</span></span>
<span data-ttu-id="a5e32-127">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a5e32-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5e32-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5e32-128">-WhatIf</span></span>
<span data-ttu-id="a5e32-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a5e32-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a5e32-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a5e32-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5e32-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5e32-131">CommonParameters</span></span>
<span data-ttu-id="a5e32-132">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5e32-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5e32-133">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a5e32-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5e32-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a5e32-134">INPUTS</span></span>

### <span data-ttu-id="a5e32-135">Nenhum</span><span class="sxs-lookup"><span data-stu-id="a5e32-135">None</span></span>

## <span data-ttu-id="a5e32-136">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="a5e32-136">OUTPUTS</span></span>

### <span data-ttu-id="a5e32-137">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorTestConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="a5e32-137">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorTestConfigurationObject</span></span>

## <span data-ttu-id="a5e32-138">NOTES</span><span class="sxs-lookup"><span data-stu-id="a5e32-138">NOTES</span></span>

## <span data-ttu-id="a5e32-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a5e32-139">RELATED LINKS</span></span>

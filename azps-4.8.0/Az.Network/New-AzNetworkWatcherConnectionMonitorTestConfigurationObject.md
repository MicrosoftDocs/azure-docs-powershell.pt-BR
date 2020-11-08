---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherconnectionmonitortestconfigurationobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorTestConfigurationObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorTestConfigurationObject.md
ms.openlocfilehash: d46cba5a939a2054bc8cc40975647a198808ca09
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94112990"
---
# <span data-ttu-id="8d972-101">New-AzNetworkWatcherConnectionMonitorTestConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="8d972-101">New-AzNetworkWatcherConnectionMonitorTestConfigurationObject</span></span>

## <span data-ttu-id="8d972-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8d972-102">SYNOPSIS</span></span>
<span data-ttu-id="8d972-103">Criar uma configuração de teste de monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="8d972-103">Create a connection monitor test configuration.</span></span>

## <span data-ttu-id="8d972-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8d972-104">SYNTAX</span></span>

```
New-AzNetworkWatcherConnectionMonitorTestConfigurationObject -Name <String> -TestFrequencySec <Int32>
 -ProtocolConfiguration <PSNetworkWatcherConnectionMonitorProtocolConfiguration>
 [-SuccessThresholdChecksFailedPercent <Int32>] [-SuccessThresholdRoundTripTimeMs <Double>]
 [-PreferredIPVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8d972-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8d972-105">DESCRIPTION</span></span>
<span data-ttu-id="8d972-106">O cmdlet New-AzNetworkWatcherConnectionMonitorTestConfigurationObject cria uma configuração de teste de monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="8d972-106">The New-AzNetworkWatcherConnectionMonitorTestConfigurationObject cmdlet creates a connection monitor test configuration.</span></span>

## <span data-ttu-id="8d972-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8d972-107">EXAMPLES</span></span>

### <span data-ttu-id="8d972-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="8d972-108">Example 1</span></span>
```powershell
PS C:\>$httpProtocolConfiguration = New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject -HttpProtocol -Port 443 -Method GET -RequestHeader @{"Allow" = "GET"} -ValidStatusCodeRange 2xx, 300-308 -PreferHTTPS
PS C:\>$httpTestConfiguration = New-AzNetworkWatcherConnectionMonitorTestConfigurationObject -Name httpTC -TestFrequencySec 120 -ProtocolConfiguration $httpProtocolConfiguration -SuccessThresholdChecksFailedPercent 20 -SuccessThresholdRoundTripTimeMs 30
```

<span data-ttu-id="8d972-109">Nome: httpTC TestFrequencySec: 120 PreferredIPVersion: ProtocolConfiguration: {"porta": 443, "método": "GET", "GET", [{"Name": "Allow", "value": "GET"}], "ValidStatusCodeRanges": ["2xx", "300-308"], "PreferHTTPS": verdadeiro} SuccessThreshold: {"ChecksFailedPercent": 20, "RoundTripTimeMs": 30}</span><span class="sxs-lookup"><span data-stu-id="8d972-109">Name                  : httpTC TestFrequencySec      : 120 PreferredIPVersion    : ProtocolConfiguration : { "Port": 443, "Method": "GET", "RequestHeaders": [ { "Name": "Allow", "Value": "GET" } ], "ValidStatusCodeRanges": [ "2xx", "300-308" ], "PreferHTTPS": true } SuccessThreshold      : { "ChecksFailedPercent": 20, "RoundTripTimeMs": 30 }</span></span> 

## <span data-ttu-id="8d972-110">OS</span><span class="sxs-lookup"><span data-stu-id="8d972-110">PARAMETERS</span></span>

### <span data-ttu-id="8d972-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d972-111">-DefaultProfile</span></span>
<span data-ttu-id="8d972-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8d972-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8d972-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="8d972-113">-Name</span></span>
<span data-ttu-id="8d972-114">O nome da configuração de teste do monitor de conexão.</span><span class="sxs-lookup"><span data-stu-id="8d972-114">The name of the connection monitor test configuration.</span></span>

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

### <span data-ttu-id="8d972-115">-PreferredIPVersion</span><span class="sxs-lookup"><span data-stu-id="8d972-115">-PreferredIPVersion</span></span>
<span data-ttu-id="8d972-116">A versão de IP preferencial a ser usada na avaliação de teste.</span><span class="sxs-lookup"><span data-stu-id="8d972-116">The preferred IP version to use in test evaluation.</span></span> <span data-ttu-id="8d972-117">O monitor de conexão pode optar por usar uma versão diferente, dependendo dos outros parâmetros.</span><span class="sxs-lookup"><span data-stu-id="8d972-117">The connection monitor may choose to use a different version depending on other parameters.</span></span>

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

### <span data-ttu-id="8d972-118">-ProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="8d972-118">-ProtocolConfiguration</span></span>
<span data-ttu-id="8d972-119">Os parâmetros usados para executar a avaliação de teste em um protocolo.</span><span class="sxs-lookup"><span data-stu-id="8d972-119">The parameters used to perform test evaluation over some protocol.</span></span>

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

### <span data-ttu-id="8d972-120">-SuccessThresholdChecksFailedPercent</span><span class="sxs-lookup"><span data-stu-id="8d972-120">-SuccessThresholdChecksFailedPercent</span></span>
<span data-ttu-id="8d972-121">A porcentagem máxima de verificações com falha permitidas para um teste ser avaliada como bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="8d972-121">The maximum percentage of failed checks permitted for a test to evaluate as successful.</span></span>

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

### <span data-ttu-id="8d972-122">-SuccessThresholdRoundTripTimeMs</span><span class="sxs-lookup"><span data-stu-id="8d972-122">-SuccessThresholdRoundTripTimeMs</span></span>
<span data-ttu-id="8d972-123">O tempo máximo de ida e volta em milissegundos permitido para um teste avaliar como bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="8d972-123">The maximum round-trip time in milliseconds permitted for a test to evaluate as successful.</span></span>

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

### <span data-ttu-id="8d972-124">-TestFrequencySec</span><span class="sxs-lookup"><span data-stu-id="8d972-124">-TestFrequencySec</span></span>
<span data-ttu-id="8d972-125">A frequência da avaliação do teste, em segundos.</span><span class="sxs-lookup"><span data-stu-id="8d972-125">The frequency of test evaluation, in seconds.</span></span>

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

### <span data-ttu-id="8d972-126">-Confirme</span><span class="sxs-lookup"><span data-stu-id="8d972-126">-Confirm</span></span>
<span data-ttu-id="8d972-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8d972-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8d972-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8d972-128">-WhatIf</span></span>
<span data-ttu-id="8d972-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8d972-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8d972-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8d972-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8d972-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d972-131">CommonParameters</span></span>
<span data-ttu-id="8d972-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d972-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d972-133">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8d972-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d972-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8d972-134">INPUTS</span></span>

### <span data-ttu-id="8d972-135">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="8d972-135">None</span></span>

## <span data-ttu-id="8d972-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8d972-136">OUTPUTS</span></span>

### <span data-ttu-id="8d972-137">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcherConnectionMonitorTestConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="8d972-137">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorTestConfigurationObject</span></span>

## <span data-ttu-id="8d972-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8d972-138">NOTES</span></span>

## <span data-ttu-id="8d972-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8d972-139">RELATED LINKS</span></span>

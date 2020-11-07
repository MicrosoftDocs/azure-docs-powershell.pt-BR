---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherconnectionmonitorprotocolconfigurationobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject.md
ms.openlocfilehash: 5a0994a5328390a928fd60cda8e8004deaaab162
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93941018"
---
# <span data-ttu-id="10da0-101">New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="10da0-101">New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject</span></span>

## <span data-ttu-id="10da0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="10da0-102">SYNOPSIS</span></span>
<span data-ttu-id="10da0-103">Criar configuração de protocolo usada para executar a avaliação de teste sobre TCP, HTTP ou ICMP.</span><span class="sxs-lookup"><span data-stu-id="10da0-103">Create protocol configuration used to perform test evaluation over TCP, HTTP or ICMP.</span></span>

## <span data-ttu-id="10da0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="10da0-104">SYNTAX</span></span>

### <span data-ttu-id="10da0-105">Protocol</span><span class="sxs-lookup"><span data-stu-id="10da0-105">TCP</span></span>
```
New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject [-TcpProtocol] -Port <Int32>
 [-DisableTraceRoute] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="10da0-106">HTTP</span><span class="sxs-lookup"><span data-stu-id="10da0-106">HTTP</span></span>
```
New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject [-HttpProtocol] [-Port <Int32>]
 [-Method <String>] [-Path <String>] [-RequestHeader <Hashtable>] [-ValidStatusCodeRange <String[]>]
 [-PreferHTTPS] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="10da0-107">ICMP</span><span class="sxs-lookup"><span data-stu-id="10da0-107">ICMP</span></span>
```
New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject [-IcmpProtocol] [-DisableTraceRoute]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="10da0-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="10da0-108">DESCRIPTION</span></span>
<span data-ttu-id="10da0-109">O cmdlet New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject cria a configuração de protocolo usada para executar a avaliação de teste sobre TCP, HTTP ou ICMP.</span><span class="sxs-lookup"><span data-stu-id="10da0-109">The New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject cmdlet creates protocol configuration used to perform test evaluation over TCP, HTTP or ICMP.</span></span>

## <span data-ttu-id="10da0-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="10da0-110">EXAMPLES</span></span>

### <span data-ttu-id="10da0-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="10da0-111">Example 1</span></span>
```powershell
PS C:\>$TcpProtocolConfiguration = New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject -TcpProtocol -Port 80 -DisableTraceRoute $false
```

<span data-ttu-id="10da0-112">Porta: 80 DisableTraceRoute: false</span><span class="sxs-lookup"><span data-stu-id="10da0-112">Port              : 80 DisableTraceRoute : False</span></span>

## <span data-ttu-id="10da0-113">OS</span><span class="sxs-lookup"><span data-stu-id="10da0-113">PARAMETERS</span></span>

### <span data-ttu-id="10da0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10da0-114">-DefaultProfile</span></span>
<span data-ttu-id="10da0-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="10da0-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="10da0-116">-DisableTraceRoute</span><span class="sxs-lookup"><span data-stu-id="10da0-116">-DisableTraceRoute</span></span>
<span data-ttu-id="10da0-117">Valor que indica se a avaliação de caminho com a rota de rastreamento deve ser desabilitada.</span><span class="sxs-lookup"><span data-stu-id="10da0-117">Value indicating whether path evaluation with trace route should be disabled.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: TCP, ICMP
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10da0-118">-HttpProtocol</span><span class="sxs-lookup"><span data-stu-id="10da0-118">-HttpProtocol</span></span>
<span data-ttu-id="10da0-119">Opção de protocolo HTTP</span><span class="sxs-lookup"><span data-stu-id="10da0-119">HTTP protocol switch</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: HTTP
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10da0-120">-IcmpProtocol</span><span class="sxs-lookup"><span data-stu-id="10da0-120">-IcmpProtocol</span></span>
<span data-ttu-id="10da0-121">Opção de protocolo ICMP.</span><span class="sxs-lookup"><span data-stu-id="10da0-121">ICMP protocol switch.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ICMP
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10da0-122">-Método</span><span class="sxs-lookup"><span data-stu-id="10da0-122">-Method</span></span>
<span data-ttu-id="10da0-123">O método HTTP a ser usado.</span><span class="sxs-lookup"><span data-stu-id="10da0-123">The HTTP method to use.</span></span>

```yaml
Type: System.String
Parameter Sets: HTTP
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10da0-124">-Caminho</span><span class="sxs-lookup"><span data-stu-id="10da0-124">-Path</span></span>
<span data-ttu-id="10da0-125">O componente Path do URI.</span><span class="sxs-lookup"><span data-stu-id="10da0-125">The path component of the URI.</span></span> <span data-ttu-id="10da0-126">Por exemplo, \" /dir1/dir2 \" .</span><span class="sxs-lookup"><span data-stu-id="10da0-126">For instance, \"/dir1/dir2\".</span></span>

```yaml
Type: System.String
Parameter Sets: HTTP
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10da0-127">-Porta</span><span class="sxs-lookup"><span data-stu-id="10da0-127">-Port</span></span>
<span data-ttu-id="10da0-128">A porta à qual se conectar.</span><span class="sxs-lookup"><span data-stu-id="10da0-128">The port to connect to.</span></span>

```yaml
Type: System.Nullable`1[System.UInt16]
Parameter Sets: TCP
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Nullable`1[System.UInt16]
Parameter Sets: HTTP
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10da0-129">-PreferHTTPS</span><span class="sxs-lookup"><span data-stu-id="10da0-129">-PreferHTTPS</span></span>
<span data-ttu-id="10da0-130">Valor que indica se HTTPS tem preferência sobre HTTP em casos em que a opção não é explícita.</span><span class="sxs-lookup"><span data-stu-id="10da0-130">Value indicating whether HTTPS is preferred over HTTP in cases where the choice is not explicit.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: HTTP
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10da0-131">-RequestHeader</span><span class="sxs-lookup"><span data-stu-id="10da0-131">-RequestHeader</span></span>
<span data-ttu-id="10da0-132">Os cabeçalhos HTTP a serem transmitidos com a solicitação.</span><span class="sxs-lookup"><span data-stu-id="10da0-132">The HTTP headers to transmit with the request.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: HTTP
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10da0-133">-TcpProtocol</span><span class="sxs-lookup"><span data-stu-id="10da0-133">-TcpProtocol</span></span>
<span data-ttu-id="10da0-134">Parâmetro de protocolo TCP.</span><span class="sxs-lookup"><span data-stu-id="10da0-134">TCP protocol switch.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: TCP
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10da0-135">-ValidStatusCodeRange</span><span class="sxs-lookup"><span data-stu-id="10da0-135">-ValidStatusCodeRange</span></span>
<span data-ttu-id="10da0-136">Códigos de status HTTP a serem considerados com êxito.</span><span class="sxs-lookup"><span data-stu-id="10da0-136">HTTP status codes to consider successful.</span></span> <span data-ttu-id="10da0-137">Por exemplo, \" 2xx, 301-304418 \" .</span><span class="sxs-lookup"><span data-stu-id="10da0-137">For instance, \"2xx,301-304,418\".</span></span>

```yaml
Type: System.String[]
Parameter Sets: HTTP
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10da0-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10da0-138">CommonParameters</span></span>
<span data-ttu-id="10da0-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10da0-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10da0-140">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="10da0-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10da0-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="10da0-141">INPUTS</span></span>

### <span data-ttu-id="10da0-142">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="10da0-142">None</span></span>

## <span data-ttu-id="10da0-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="10da0-143">OUTPUTS</span></span>

### <span data-ttu-id="10da0-144">Microsoft. Azure. Commands. Network. Models. PSConnectionMonitorTcpConfiguration</span><span class="sxs-lookup"><span data-stu-id="10da0-144">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorTcpConfiguration</span></span>

### <span data-ttu-id="10da0-145">Microsoft. Azure. Commands. Network. Models. PSConnectionMonitorHttpConfiguration</span><span class="sxs-lookup"><span data-stu-id="10da0-145">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorHttpConfiguration</span></span>

### <span data-ttu-id="10da0-146">Microsoft. Azure. Commands. Network. Models. PSConnectionMonitorIcmpConfiguration</span><span class="sxs-lookup"><span data-stu-id="10da0-146">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorIcmpConfiguration</span></span>

## <span data-ttu-id="10da0-147">INFORMA</span><span class="sxs-lookup"><span data-stu-id="10da0-147">NOTES</span></span>

## <span data-ttu-id="10da0-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="10da0-148">RELATED LINKS</span></span>

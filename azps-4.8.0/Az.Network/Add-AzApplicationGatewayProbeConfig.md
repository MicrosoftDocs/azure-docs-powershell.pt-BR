---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayProbeConfig.md
ms.openlocfilehash: cea6f92ba15e43d5977af03dfee1054240f5ecad
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93947714"
---
# <span data-ttu-id="dbed6-101">Add-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="dbed6-101">Add-AzApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="dbed6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="dbed6-102">SYNOPSIS</span></span>
<span data-ttu-id="dbed6-103">Adiciona um teste de integridade a um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="dbed6-103">Adds a health probe to an Application Gateway.</span></span>

## <span data-ttu-id="dbed6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dbed6-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayProbeConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -Protocol <String> [-HostName <String>] -Path <String> -Interval <Int32> -Timeout <Int32>
 -UnhealthyThreshold <Int32> [-PickHostNameFromBackendHttpSettings] [-MinServers <Int32>]
 [-Match <PSApplicationGatewayProbeHealthResponseMatch>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="dbed6-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="dbed6-105">DESCRIPTION</span></span>
<span data-ttu-id="dbed6-106">O cmdlet Add-AzApplicationGatewayProbeConfig adiciona um teste de integridade a um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="dbed6-106">The Add-AzApplicationGatewayProbeConfig cmdlet adds a health probe to an Application Gateway.</span></span>

## <span data-ttu-id="dbed6-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="dbed6-107">EXAMPLES</span></span>

### <span data-ttu-id="dbed6-108">Exemplo 1: adicionar um teste de integridade a um gateway de aplicativo</span><span class="sxs-lookup"><span data-stu-id="dbed6-108">Example 1: Add a health probe to an application gateway</span></span>
```
PS C:\>$Probe = Add-AzApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe01" -Protocol Http -HostName "contoso.com" -Path "/path/custompath.htm" -Interval 30 -Timeout 120 -UnhealthyThreshold 8
```

<span data-ttu-id="dbed6-109">Esse comando adiciona um teste de integridade chamado Probe01 para o gateway do aplicativo chamado gateway.</span><span class="sxs-lookup"><span data-stu-id="dbed6-109">This command adds a health probe named Probe01 for the application gateway named Gateway.</span></span>
<span data-ttu-id="dbed6-110">O comando também define o limiar não íntegro para 8 tentativas e o tempo limite após 120 segundos.</span><span class="sxs-lookup"><span data-stu-id="dbed6-110">The command also sets the unhealthy threshold to 8 retries and times out after 120 seconds.</span></span>

## <span data-ttu-id="dbed6-111">OS</span><span class="sxs-lookup"><span data-stu-id="dbed6-111">PARAMETERS</span></span>

### <span data-ttu-id="dbed6-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="dbed6-112">-ApplicationGateway</span></span>
<span data-ttu-id="dbed6-113">Especifica o gateway do aplicativo para o qual esse cmdlet adiciona um teste.</span><span class="sxs-lookup"><span data-stu-id="dbed6-113">Specifies the application gateway to which this cmdlet adds a probe.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dbed6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbed6-114">-DefaultProfile</span></span>
<span data-ttu-id="dbed6-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="dbed6-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dbed6-116">-HostName</span><span class="sxs-lookup"><span data-stu-id="dbed6-116">-HostName</span></span>
<span data-ttu-id="dbed6-117">Especifica o nome do host para o qual esse cmdlet envia o teste.</span><span class="sxs-lookup"><span data-stu-id="dbed6-117">Specifies the host name that this cmdlet sends the probe to.</span></span>

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

### <span data-ttu-id="dbed6-118">-Intervalo</span><span class="sxs-lookup"><span data-stu-id="dbed6-118">-Interval</span></span>
<span data-ttu-id="dbed6-119">Especifica o intervalo de sondagem em segundos.</span><span class="sxs-lookup"><span data-stu-id="dbed6-119">Specifies the probe interval in seconds.</span></span>
<span data-ttu-id="dbed6-120">Esse é o intervalo de tempo entre dois testes consecutivos.</span><span class="sxs-lookup"><span data-stu-id="dbed6-120">This is the time interval between two consecutive probes.</span></span>
<span data-ttu-id="dbed6-121">Esse valor é entre 1 segundo e 86400 segundos.</span><span class="sxs-lookup"><span data-stu-id="dbed6-121">This value is between 1 second and 86400 seconds.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dbed6-122">-Match</span><span class="sxs-lookup"><span data-stu-id="dbed6-122">-Match</span></span>
<span data-ttu-id="dbed6-123">Corpo que deve estar contido na resposta de integridade.</span><span class="sxs-lookup"><span data-stu-id="dbed6-123">Body that must be contained in the health response.</span></span>
<span data-ttu-id="dbed6-124">O valor padrão está vazio</span><span class="sxs-lookup"><span data-stu-id="dbed6-124">Default value is empty</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbeHealthResponseMatch
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dbed6-125">-MinServers</span><span class="sxs-lookup"><span data-stu-id="dbed6-125">-MinServers</span></span>
<span data-ttu-id="dbed6-126">Número mínimo de servidores que sempre estão marcados como íntegros.</span><span class="sxs-lookup"><span data-stu-id="dbed6-126">Minimum number of servers that are always marked healthy.</span></span>
<span data-ttu-id="dbed6-127">O valor padrão é 0</span><span class="sxs-lookup"><span data-stu-id="dbed6-127">Default value is 0</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dbed6-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="dbed6-128">-Name</span></span>
<span data-ttu-id="dbed6-129">Especifica o nome do teste.</span><span class="sxs-lookup"><span data-stu-id="dbed6-129">Specifies the name of the probe.</span></span>

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

### <span data-ttu-id="dbed6-130">-Caminho</span><span class="sxs-lookup"><span data-stu-id="dbed6-130">-Path</span></span>
<span data-ttu-id="dbed6-131">Especifica o caminho relativo do teste.</span><span class="sxs-lookup"><span data-stu-id="dbed6-131">Specifies the relative path of probe.</span></span>
<span data-ttu-id="dbed6-132">Caminho válido comece com o caractere de barra (/).</span><span class="sxs-lookup"><span data-stu-id="dbed6-132">Valid path start with the slash character (/).</span></span>
<span data-ttu-id="dbed6-133">O teste é enviado para \<Protocol\> :// \<host\> : \<port\> \<path\> .</span><span class="sxs-lookup"><span data-stu-id="dbed6-133">The probe is sent to \<Protocol\>://\<host\>:\<port\>\<path\>.</span></span>

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

### <span data-ttu-id="dbed6-134">-PickHostNameFromBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="dbed6-134">-PickHostNameFromBackendHttpSettings</span></span>
<span data-ttu-id="dbed6-135">Se o cabeçalho do host deve ser selecionado nas configurações http de back-end.</span><span class="sxs-lookup"><span data-stu-id="dbed6-135">Whether the host header should be picked from the backend http settings.</span></span>
<span data-ttu-id="dbed6-136">O valor padrão é falso</span><span class="sxs-lookup"><span data-stu-id="dbed6-136">Default value is false</span></span>

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

### <span data-ttu-id="dbed6-137">-Protocolo</span><span class="sxs-lookup"><span data-stu-id="dbed6-137">-Protocol</span></span>
<span data-ttu-id="dbed6-138">Especifica o protocolo usado para enviar o teste.</span><span class="sxs-lookup"><span data-stu-id="dbed6-138">Specifies the protocol used to send probe.</span></span>
<span data-ttu-id="dbed6-139">Esse cmdlet dá suporte somente para HTTP.</span><span class="sxs-lookup"><span data-stu-id="dbed6-139">This cmdlet supports HTTP only.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Http, Https

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dbed6-140">-Timeout</span><span class="sxs-lookup"><span data-stu-id="dbed6-140">-Timeout</span></span>
<span data-ttu-id="dbed6-141">Especifica o tempo limite do teste em segundos.</span><span class="sxs-lookup"><span data-stu-id="dbed6-141">Specifies the probe timeout in seconds.</span></span>
<span data-ttu-id="dbed6-142">Esse cmdlet marca o teste como Failed se uma resposta válida não for recebida com esse período de tempo limite.</span><span class="sxs-lookup"><span data-stu-id="dbed6-142">This cmdlet marks the probe as failed if a valid response is not received with this timeout period.</span></span>
<span data-ttu-id="dbed6-143">Os valores válidos estão entre 1 segundo e 86400 segundos.</span><span class="sxs-lookup"><span data-stu-id="dbed6-143">Valid values are between 1 second and 86400 seconds.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dbed6-144">-UnhealthyThreshold</span><span class="sxs-lookup"><span data-stu-id="dbed6-144">-UnhealthyThreshold</span></span>
<span data-ttu-id="dbed6-145">Especifica a contagem de repetição de teste.</span><span class="sxs-lookup"><span data-stu-id="dbed6-145">Specifies the probe retry count.</span></span>
<span data-ttu-id="dbed6-146">O servidor back-end está marcado para baixo após a contagem de falhas de investigação consecutiva alcançar o limite não íntegro.</span><span class="sxs-lookup"><span data-stu-id="dbed6-146">The backend server is marked down after consecutive probe failure count reaches the unhealthy threshold.</span></span>
<span data-ttu-id="dbed6-147">Os valores válidos estão entre 1 segundo e 20 segundos.</span><span class="sxs-lookup"><span data-stu-id="dbed6-147">Valid values are between 1 second and 20 seconds.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dbed6-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbed6-148">CommonParameters</span></span>
<span data-ttu-id="dbed6-149">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dbed6-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbed6-150">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dbed6-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbed6-151">SENSORES</span><span class="sxs-lookup"><span data-stu-id="dbed6-151">INPUTS</span></span>

### <span data-ttu-id="dbed6-152">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="dbed6-152">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="dbed6-153">EXIBE</span><span class="sxs-lookup"><span data-stu-id="dbed6-153">OUTPUTS</span></span>

### <span data-ttu-id="dbed6-154">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="dbed6-154">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="dbed6-155">INFORMA</span><span class="sxs-lookup"><span data-stu-id="dbed6-155">NOTES</span></span>

## <span data-ttu-id="dbed6-156">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="dbed6-156">RELATED LINKS</span></span>

[<span data-ttu-id="dbed6-157">Adicionar um teste a um gateway de aplicativo existente</span><span class="sxs-lookup"><span data-stu-id="dbed6-157">Add a probe to an existing application gateway</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#add-a-probe-to-an-existing-application-gateway)

[<span data-ttu-id="dbed6-158">Get-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="dbed6-158">Get-AzApplicationGatewayProbeConfig</span></span>](./Get-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="dbed6-159">New-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="dbed6-159">New-AzApplicationGatewayProbeConfig</span></span>](./New-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="dbed6-160">Remove-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="dbed6-160">Remove-AzApplicationGatewayProbeConfig</span></span>](./Remove-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="dbed6-161">Set-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="dbed6-161">Set-AzApplicationGatewayProbeConfig</span></span>](./Set-AzApplicationGatewayProbeConfig.md)


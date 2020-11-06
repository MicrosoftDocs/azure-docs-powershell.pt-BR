---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#add-a-probe-to-an-existing-application-gateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayProbeConfig.md
ms.openlocfilehash: 169a63248ebc499f577a635821131e0153e64433
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93433084"
---
# <span data-ttu-id="fb69a-101">Add-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="fb69a-101">Add-AzureRmApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="fb69a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fb69a-102">SYNOPSIS</span></span>
<span data-ttu-id="fb69a-103">Adiciona um teste de integridade a um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="fb69a-103">Adds a health probe to an Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fb69a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fb69a-104">SYNTAX</span></span>

```
Add-AzureRmApplicationGatewayProbeConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -Protocol <String> [-HostName <String>] -Path <String> -Interval <Int32> -Timeout <Int32>
 -UnhealthyThreshold <Int32> [-PickHostNameFromBackendHttpSettings] [-MinServers <Int32>]
 [-Match <PSApplicationGatewayProbeHealthResponseMatch>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fb69a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fb69a-105">DESCRIPTION</span></span>
<span data-ttu-id="fb69a-106">O cmdlet Add-AzureRmApplicationGatewayProbeConfig adiciona um teste de integridade a um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="fb69a-106">The Add-AzureRmApplicationGatewayProbeConfig cmdlet adds a health probe to an Application Gateway.</span></span>

## <span data-ttu-id="fb69a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fb69a-107">EXAMPLES</span></span>

### <span data-ttu-id="fb69a-108">Exemplo 1: adicionar um teste de integridade a um gateway de aplicativo</span><span class="sxs-lookup"><span data-stu-id="fb69a-108">Example 1: Add a health probe to an application gateway</span></span>
```
PS C:\>$Probe = Add-AzureRmApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe01" -Protocol Http -HostName "contoso.com" -Path "/path/custompath.htm" -Interval 30 -Timeout 120 -UnhealthyThreshold 8
```

<span data-ttu-id="fb69a-109">Esse comando adiciona um teste de integridade chamado Probe01 para o gateway do aplicativo chamado gateway.</span><span class="sxs-lookup"><span data-stu-id="fb69a-109">This command adds a health probe named Probe01 for the application gateway named Gateway.</span></span>
<span data-ttu-id="fb69a-110">O comando também define o limiar não íntegro para 8 tentativas e o tempo limite após 120 segundos.</span><span class="sxs-lookup"><span data-stu-id="fb69a-110">The command also sets the unhealthy threshold to 8 retries and times out after 120 seconds.</span></span>

## <span data-ttu-id="fb69a-111">OS</span><span class="sxs-lookup"><span data-stu-id="fb69a-111">PARAMETERS</span></span>

### <span data-ttu-id="fb69a-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fb69a-112">-ApplicationGateway</span></span>
<span data-ttu-id="fb69a-113">Especifica o gateway do aplicativo para o qual esse cmdlet adiciona um teste.</span><span class="sxs-lookup"><span data-stu-id="fb69a-113">Specifies the application gateway to which this cmdlet adds a probe.</span></span>

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

### <span data-ttu-id="fb69a-114">-HostName</span><span class="sxs-lookup"><span data-stu-id="fb69a-114">-HostName</span></span>
<span data-ttu-id="fb69a-115">Especifica o nome do host para o qual esse cmdlet envia o teste.</span><span class="sxs-lookup"><span data-stu-id="fb69a-115">Specifies the host name that this cmdlet sends the probe to.</span></span>

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

### <span data-ttu-id="fb69a-116">-Intervalo</span><span class="sxs-lookup"><span data-stu-id="fb69a-116">-Interval</span></span>
<span data-ttu-id="fb69a-117">Especifica o intervalo de sondagem em segundos.</span><span class="sxs-lookup"><span data-stu-id="fb69a-117">Specifies the probe interval in seconds.</span></span>
<span data-ttu-id="fb69a-118">Esse é o intervalo de tempo entre dois testes consecutivos.</span><span class="sxs-lookup"><span data-stu-id="fb69a-118">This is the time interval between two consecutive probes.</span></span>
<span data-ttu-id="fb69a-119">Esse valor é entre 1 segundo e 86400 segundos.</span><span class="sxs-lookup"><span data-stu-id="fb69a-119">This value is between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="fb69a-120">-Match</span><span class="sxs-lookup"><span data-stu-id="fb69a-120">-Match</span></span>
<span data-ttu-id="fb69a-121">Corpo que deve estar contido na resposta de integridade.</span><span class="sxs-lookup"><span data-stu-id="fb69a-121">Body that must be contained in the health response.</span></span>
<span data-ttu-id="fb69a-122">O valor padrão está vazio</span><span class="sxs-lookup"><span data-stu-id="fb69a-122">Default value is empty</span></span>

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

### <span data-ttu-id="fb69a-123">-MinServers</span><span class="sxs-lookup"><span data-stu-id="fb69a-123">-MinServers</span></span>
<span data-ttu-id="fb69a-124">Número mínimo de servidores que sempre estão marcados como íntegros.</span><span class="sxs-lookup"><span data-stu-id="fb69a-124">Minimum number of servers that are always marked healthy.</span></span>
<span data-ttu-id="fb69a-125">O valor padrão é 0</span><span class="sxs-lookup"><span data-stu-id="fb69a-125">Default value is 0</span></span>

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

### <span data-ttu-id="fb69a-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="fb69a-126">-Name</span></span>
<span data-ttu-id="fb69a-127">Especifica o nome do teste.</span><span class="sxs-lookup"><span data-stu-id="fb69a-127">Specifies the name of the probe.</span></span>

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

### <span data-ttu-id="fb69a-128">-Caminho</span><span class="sxs-lookup"><span data-stu-id="fb69a-128">-Path</span></span>
<span data-ttu-id="fb69a-129">Especifica o caminho relativo do teste.</span><span class="sxs-lookup"><span data-stu-id="fb69a-129">Specifies the relative path of probe.</span></span>
<span data-ttu-id="fb69a-130">Caminho válido comece com o caractere de barra (/).</span><span class="sxs-lookup"><span data-stu-id="fb69a-130">Valid path start with the slash character (/).</span></span>
<span data-ttu-id="fb69a-131">O teste é enviado para \<Protocol\> :// \<host\> : \<port\> \<path\> .</span><span class="sxs-lookup"><span data-stu-id="fb69a-131">The probe is sent to \<Protocol\>://\<host\>:\<port\>\<path\>.</span></span>

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

### <span data-ttu-id="fb69a-132">-PickHostNameFromBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="fb69a-132">-PickHostNameFromBackendHttpSettings</span></span>
<span data-ttu-id="fb69a-133">Se o cabeçalho do host deve ser selecionado nas configurações http de back-end.</span><span class="sxs-lookup"><span data-stu-id="fb69a-133">Whether the host header should be picked from the backend http settings.</span></span>
<span data-ttu-id="fb69a-134">O valor padrão é falso</span><span class="sxs-lookup"><span data-stu-id="fb69a-134">Default value is false</span></span>

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

### <span data-ttu-id="fb69a-135">-Protocolo</span><span class="sxs-lookup"><span data-stu-id="fb69a-135">-Protocol</span></span>
<span data-ttu-id="fb69a-136">Especifica o protocolo usado para enviar o teste.</span><span class="sxs-lookup"><span data-stu-id="fb69a-136">Specifies the protocol used to send probe.</span></span>
<span data-ttu-id="fb69a-137">Esse cmdlet dá suporte somente para HTTP.</span><span class="sxs-lookup"><span data-stu-id="fb69a-137">This cmdlet supports HTTP only.</span></span>

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

### <span data-ttu-id="fb69a-138">-Timeout</span><span class="sxs-lookup"><span data-stu-id="fb69a-138">-Timeout</span></span>
<span data-ttu-id="fb69a-139">Especifica o tempo limite do teste em segundos.</span><span class="sxs-lookup"><span data-stu-id="fb69a-139">Specifies the probe timeout in seconds.</span></span>
<span data-ttu-id="fb69a-140">Esse cmdlet marca o teste como Failed se uma resposta válida não for recebida com esse período de tempo limite.</span><span class="sxs-lookup"><span data-stu-id="fb69a-140">This cmdlet marks the probe as failed if a valid response is not received with this timeout period.</span></span>
<span data-ttu-id="fb69a-141">Os valores válidos estão entre 1 segundo e 86400 segundos.</span><span class="sxs-lookup"><span data-stu-id="fb69a-141">Valid values are between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="fb69a-142">-UnhealthyThreshold</span><span class="sxs-lookup"><span data-stu-id="fb69a-142">-UnhealthyThreshold</span></span>
<span data-ttu-id="fb69a-143">Especifica a contagem de repetição de teste.</span><span class="sxs-lookup"><span data-stu-id="fb69a-143">Specifies the probe retry count.</span></span>
<span data-ttu-id="fb69a-144">O servidor back-end está marcado para baixo após a contagem de falhas de investigação consecutiva alcançar o limite não íntegro.</span><span class="sxs-lookup"><span data-stu-id="fb69a-144">The backend server is marked down after consecutive probe failure count reaches the unhealthy threshold.</span></span>
<span data-ttu-id="fb69a-145">Os valores válidos estão entre 1 segundo e 20 segundos.</span><span class="sxs-lookup"><span data-stu-id="fb69a-145">Valid values are between 1 second and 20 seconds.</span></span>

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

### <span data-ttu-id="fb69a-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb69a-146">-DefaultProfile</span></span>
<span data-ttu-id="fb69a-147">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fb69a-147">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb69a-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb69a-148">CommonParameters</span></span>
<span data-ttu-id="fb69a-149">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb69a-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb69a-150">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb69a-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb69a-151">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fb69a-151">INPUTS</span></span>

### <span data-ttu-id="fb69a-152">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fb69a-152">PSApplicationGateway</span></span>
<span data-ttu-id="fb69a-153">O parâmetro ' ApplicationGateway ' aceita o valor do tipo ' PSApplicationGateway ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="fb69a-153">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="fb69a-154">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fb69a-154">OUTPUTS</span></span>

### <span data-ttu-id="fb69a-155">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fb69a-155">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="fb69a-156">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fb69a-156">NOTES</span></span>

## <span data-ttu-id="fb69a-157">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fb69a-157">RELATED LINKS</span></span>

[<span data-ttu-id="fb69a-158">Adicionar um teste a um gateway de aplicativo existente</span><span class="sxs-lookup"><span data-stu-id="fb69a-158">Add a probe to an existing application gateway</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#add-a-probe-to-an-existing-application-gateway)

[<span data-ttu-id="fb69a-159">Get-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="fb69a-159">Get-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="fb69a-160">New-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="fb69a-160">New-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="fb69a-161">Remove-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="fb69a-161">Remove-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="fb69a-162">Set-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="fb69a-162">Set-AzureRmApplicationGatewayProbeConfig</span></span>]()


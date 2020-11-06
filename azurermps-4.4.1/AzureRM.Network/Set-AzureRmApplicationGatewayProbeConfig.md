---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayProbeConfig.md
ms.openlocfilehash: 212e418c3fdaf8ba7f67ebdae0565d5d230daa0d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430722"
---
# <span data-ttu-id="022b1-101">Set-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="022b1-101">Set-AzureRmApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="022b1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="022b1-102">SYNOPSIS</span></span>
<span data-ttu-id="022b1-103">Define a configuração de investigação de integridade em um gateway de aplicativo existente.</span><span class="sxs-lookup"><span data-stu-id="022b1-103">Sets the health probe configuration on an existing Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="022b1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="022b1-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewayProbeConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -Protocol <String> [-HostName <String>] -Path <String> -Interval <Int32> -Timeout <Int32>
 -UnhealthyThreshold <Int32> [-PickHostNameFromBackendHttpSettings] [-MinServers <Int32>]
 [-Match <PSApplicationGatewayProbeHealthResponseMatch>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="022b1-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="022b1-105">DESCRIPTION</span></span>
<span data-ttu-id="022b1-106">O cmdlet Set-AzureRmApplicationGatewayProbeConfig define a configuração de investigação de integridade em um gateway de aplicativo existente.</span><span class="sxs-lookup"><span data-stu-id="022b1-106">The Set-AzureRmApplicationGatewayProbeConfig cmdlet sets the health probe configuration on an existing Application Gateway.</span></span>

## <span data-ttu-id="022b1-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="022b1-107">EXAMPLES</span></span>

### <span data-ttu-id="022b1-108">Exemplo 1: definir a configuração para um teste de integridade em um gateway de aplicativo</span><span class="sxs-lookup"><span data-stu-id="022b1-108">Example 1: Set the configuration for a health probe on an application gateway</span></span>
```
PS C:\>Set-AzureRmApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe05" -Protocol Http -HostName "contoso.com" -Path "/path/custompath.htm" -Interval 30 -Timeout 120 -UnhealthyThreshold 8
```

<span data-ttu-id="022b1-109">Este comando define a configuração de um teste de integridade chamado Probe05 para o gateway do aplicativo chamado gateway.</span><span class="sxs-lookup"><span data-stu-id="022b1-109">This command sets the configuration for a health probe named Probe05 for the application gateway named Gateway.</span></span>
<span data-ttu-id="022b1-110">O comando também define o limiar não íntegro para 8 tentativas e o tempo limite após 120 segundos.</span><span class="sxs-lookup"><span data-stu-id="022b1-110">The command also sets the unhealthy threshold to 8 retries and times out after 120 seconds.</span></span>

## <span data-ttu-id="022b1-111">OS</span><span class="sxs-lookup"><span data-stu-id="022b1-111">PARAMETERS</span></span>

### <span data-ttu-id="022b1-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="022b1-112">-ApplicationGateway</span></span>
<span data-ttu-id="022b1-113">Especifica o gateway do aplicativo para o qual esse cmdlet envia um teste.</span><span class="sxs-lookup"><span data-stu-id="022b1-113">Specifies the application gateway to which this cmdlet sends a probe.</span></span>

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

### <span data-ttu-id="022b1-114">-HostName</span><span class="sxs-lookup"><span data-stu-id="022b1-114">-HostName</span></span>
<span data-ttu-id="022b1-115">Especifica o nome do host para o qual esse cmdlet envia o teste.</span><span class="sxs-lookup"><span data-stu-id="022b1-115">Specifies the host name that this cmdlet sends the probe to.</span></span>

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

### <span data-ttu-id="022b1-116">-Intervalo</span><span class="sxs-lookup"><span data-stu-id="022b1-116">-Interval</span></span>
<span data-ttu-id="022b1-117">Especifica o intervalo de sondagem em segundos.</span><span class="sxs-lookup"><span data-stu-id="022b1-117">Specifies the probe interval in seconds.</span></span>
<span data-ttu-id="022b1-118">Esse é o intervalo de tempo entre dois testes consecutivos.</span><span class="sxs-lookup"><span data-stu-id="022b1-118">This is the time interval between two consecutive probes.</span></span>
<span data-ttu-id="022b1-119">Esse valor é entre 1 segundo e 86400 segundos.</span><span class="sxs-lookup"><span data-stu-id="022b1-119">This value is between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="022b1-120">-Match</span><span class="sxs-lookup"><span data-stu-id="022b1-120">-Match</span></span>
<span data-ttu-id="022b1-121">Corpo que deve estar contido na resposta de integridade.</span><span class="sxs-lookup"><span data-stu-id="022b1-121">Body that must be contained in the health response.</span></span>
<span data-ttu-id="022b1-122">O valor padrão está vazio</span><span class="sxs-lookup"><span data-stu-id="022b1-122">Default value is empty</span></span>

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

### <span data-ttu-id="022b1-123">-MinServers</span><span class="sxs-lookup"><span data-stu-id="022b1-123">-MinServers</span></span>
<span data-ttu-id="022b1-124">Número mínimo de servidores que sempre estão marcados como íntegros.</span><span class="sxs-lookup"><span data-stu-id="022b1-124">Minimum number of servers that are always marked healthy.</span></span>
<span data-ttu-id="022b1-125">O valor padrão é 0</span><span class="sxs-lookup"><span data-stu-id="022b1-125">Default value is 0</span></span>

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

### <span data-ttu-id="022b1-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="022b1-126">-Name</span></span>
<span data-ttu-id="022b1-127">Especifica o nome do teste.</span><span class="sxs-lookup"><span data-stu-id="022b1-127">Specifies the name of the probe.</span></span>

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

### <span data-ttu-id="022b1-128">-Caminho</span><span class="sxs-lookup"><span data-stu-id="022b1-128">-Path</span></span>
<span data-ttu-id="022b1-129">Especifica o caminho relativo do teste.</span><span class="sxs-lookup"><span data-stu-id="022b1-129">Specifies the relative path of probe.</span></span>
<span data-ttu-id="022b1-130">Caminhos válidos começam com o caractere de barra (/).</span><span class="sxs-lookup"><span data-stu-id="022b1-130">Valid paths start with the slash character (/).</span></span>
<span data-ttu-id="022b1-131">O teste é enviado para \<Protocol\> :// \<host\> : \<port\> \<path\> .</span><span class="sxs-lookup"><span data-stu-id="022b1-131">The probe is sent to \<Protocol\>://\<host\>:\<port\>\<path\>.</span></span>

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

### <span data-ttu-id="022b1-132">-PickHostNameFromBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="022b1-132">-PickHostNameFromBackendHttpSettings</span></span>
<span data-ttu-id="022b1-133">Se o cabeçalho do host deve ser selecionado nas configurações http de back-end.</span><span class="sxs-lookup"><span data-stu-id="022b1-133">Whether the host header should be picked from the backend http settings.</span></span>
<span data-ttu-id="022b1-134">O valor padrão é falso</span><span class="sxs-lookup"><span data-stu-id="022b1-134">Default value is false</span></span>

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

### <span data-ttu-id="022b1-135">-Protocolo</span><span class="sxs-lookup"><span data-stu-id="022b1-135">-Protocol</span></span>
<span data-ttu-id="022b1-136">Especifica o protocolo usado para enviar o teste.</span><span class="sxs-lookup"><span data-stu-id="022b1-136">Specifies the protocol used to send probe.</span></span>

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

### <span data-ttu-id="022b1-137">-Timeout</span><span class="sxs-lookup"><span data-stu-id="022b1-137">-Timeout</span></span>
<span data-ttu-id="022b1-138">Especifica o tempo limite do teste em segundos.</span><span class="sxs-lookup"><span data-stu-id="022b1-138">Specifies the probe timeout in seconds.</span></span>
<span data-ttu-id="022b1-139">Esse cmdlet marca o teste como Failed se uma resposta válida não for recebida com esse período de tempo limite.</span><span class="sxs-lookup"><span data-stu-id="022b1-139">This cmdlet marks the probe as failed if a valid response is not received with this timeout period.</span></span>
<span data-ttu-id="022b1-140">Os valores válidos estão entre 1 segundo e 86400 segundos.</span><span class="sxs-lookup"><span data-stu-id="022b1-140">Valid values are between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="022b1-141">-UnhealthyThreshold</span><span class="sxs-lookup"><span data-stu-id="022b1-141">-UnhealthyThreshold</span></span>
<span data-ttu-id="022b1-142">Especifica a contagem de repetição de teste.</span><span class="sxs-lookup"><span data-stu-id="022b1-142">Specifies the probe retry count.</span></span>
<span data-ttu-id="022b1-143">O servidor back-end está marcado para baixo após a contagem de falhas de investigação consecutiva alcançar o limite não íntegro.</span><span class="sxs-lookup"><span data-stu-id="022b1-143">The backend server is marked down after consecutive probe failure count reaches the unhealthy threshold.</span></span>
<span data-ttu-id="022b1-144">Os valores válidos estão entre 1 segundo e 20 segundos.</span><span class="sxs-lookup"><span data-stu-id="022b1-144">Valid values are between 1 second and 20 seconds.</span></span>

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

### <span data-ttu-id="022b1-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="022b1-145">-DefaultProfile</span></span>
<span data-ttu-id="022b1-146">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="022b1-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="022b1-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="022b1-147">CommonParameters</span></span>
<span data-ttu-id="022b1-148">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="022b1-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="022b1-149">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="022b1-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="022b1-150">SENSORES</span><span class="sxs-lookup"><span data-stu-id="022b1-150">INPUTS</span></span>

### <span data-ttu-id="022b1-151">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="022b1-151">PSApplicationGateway</span></span>
<span data-ttu-id="022b1-152">O parâmetro ' ApplicationGateway ' aceita o valor do tipo ' PSApplicationGateway ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="022b1-152">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="022b1-153">EXIBE</span><span class="sxs-lookup"><span data-stu-id="022b1-153">OUTPUTS</span></span>

### <span data-ttu-id="022b1-154">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="022b1-154">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="022b1-155">INFORMA</span><span class="sxs-lookup"><span data-stu-id="022b1-155">NOTES</span></span>

## <span data-ttu-id="022b1-156">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="022b1-156">RELATED LINKS</span></span>

[<span data-ttu-id="022b1-157">Add-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="022b1-157">Add-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="022b1-158">Get-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="022b1-158">Get-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="022b1-159">New-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="022b1-159">New-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="022b1-160">Remove-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="022b1-160">Remove-AzureRmApplicationGatewayProbeConfig</span></span>]()


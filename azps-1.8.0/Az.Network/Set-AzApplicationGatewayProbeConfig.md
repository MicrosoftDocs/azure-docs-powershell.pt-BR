---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayProbeConfig.md
ms.openlocfilehash: 7763dac119ba2a2144f2c7428dfd63aeedcd3b45
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93600046"
---
# <span data-ttu-id="9292f-101">Set-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="9292f-101">Set-AzApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="9292f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9292f-102">SYNOPSIS</span></span>
<span data-ttu-id="9292f-103">Define a configuração de investigação de integridade em um gateway de aplicativo existente.</span><span class="sxs-lookup"><span data-stu-id="9292f-103">Sets the health probe configuration on an existing Application Gateway.</span></span>

## <span data-ttu-id="9292f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9292f-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayProbeConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -Protocol <String> [-HostName <String>] -Path <String> -Interval <Int32> -Timeout <Int32>
 -UnhealthyThreshold <Int32> [-PickHostNameFromBackendHttpSettings] [-MinServers <Int32>]
 [-Match <PSApplicationGatewayProbeHealthResponseMatch>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9292f-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9292f-105">DESCRIPTION</span></span>
<span data-ttu-id="9292f-106">O cmdlet Set-AzApplicationGatewayProbeConfig define a configuração de investigação de integridade em um gateway de aplicativo existente.</span><span class="sxs-lookup"><span data-stu-id="9292f-106">The Set-AzApplicationGatewayProbeConfig cmdlet sets the health probe configuration on an existing Application Gateway.</span></span>

## <span data-ttu-id="9292f-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9292f-107">EXAMPLES</span></span>

### <span data-ttu-id="9292f-108">Exemplo 1: definir a configuração para um teste de integridade em um gateway de aplicativo</span><span class="sxs-lookup"><span data-stu-id="9292f-108">Example 1: Set the configuration for a health probe on an application gateway</span></span>
```
PS C:\>Set-AzApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe05" -Protocol Http -HostName "contoso.com" -Path "/path/custompath.htm" -Interval 30 -Timeout 120 -UnhealthyThreshold 8
```

<span data-ttu-id="9292f-109">Este comando define a configuração de um teste de integridade chamado Probe05 para o gateway do aplicativo chamado gateway.</span><span class="sxs-lookup"><span data-stu-id="9292f-109">This command sets the configuration for a health probe named Probe05 for the application gateway named Gateway.</span></span>
<span data-ttu-id="9292f-110">O comando também define o limiar não íntegro para 8 tentativas e o tempo limite após 120 segundos.</span><span class="sxs-lookup"><span data-stu-id="9292f-110">The command also sets the unhealthy threshold to 8 retries and times out after 120 seconds.</span></span>

## <span data-ttu-id="9292f-111">OS</span><span class="sxs-lookup"><span data-stu-id="9292f-111">PARAMETERS</span></span>

### <span data-ttu-id="9292f-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9292f-112">-ApplicationGateway</span></span>
<span data-ttu-id="9292f-113">Especifica o gateway do aplicativo para o qual esse cmdlet envia um teste.</span><span class="sxs-lookup"><span data-stu-id="9292f-113">Specifies the application gateway to which this cmdlet sends a probe.</span></span>

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

### <span data-ttu-id="9292f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9292f-114">-DefaultProfile</span></span>
<span data-ttu-id="9292f-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9292f-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9292f-116">-HostName</span><span class="sxs-lookup"><span data-stu-id="9292f-116">-HostName</span></span>
<span data-ttu-id="9292f-117">Especifica o nome do host para o qual esse cmdlet envia o teste.</span><span class="sxs-lookup"><span data-stu-id="9292f-117">Specifies the host name that this cmdlet sends the probe to.</span></span>

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

### <span data-ttu-id="9292f-118">-Intervalo</span><span class="sxs-lookup"><span data-stu-id="9292f-118">-Interval</span></span>
<span data-ttu-id="9292f-119">Especifica o intervalo de sondagem em segundos.</span><span class="sxs-lookup"><span data-stu-id="9292f-119">Specifies the probe interval in seconds.</span></span>
<span data-ttu-id="9292f-120">Esse é o intervalo de tempo entre dois testes consecutivos.</span><span class="sxs-lookup"><span data-stu-id="9292f-120">This is the time interval between two consecutive probes.</span></span>
<span data-ttu-id="9292f-121">Esse valor é entre 1 segundo e 86400 segundos.</span><span class="sxs-lookup"><span data-stu-id="9292f-121">This value is between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="9292f-122">-Match</span><span class="sxs-lookup"><span data-stu-id="9292f-122">-Match</span></span>
<span data-ttu-id="9292f-123">Corpo que deve estar contido na resposta de integridade.</span><span class="sxs-lookup"><span data-stu-id="9292f-123">Body that must be contained in the health response.</span></span>
<span data-ttu-id="9292f-124">O valor padrão está vazio</span><span class="sxs-lookup"><span data-stu-id="9292f-124">Default value is empty</span></span>

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

### <span data-ttu-id="9292f-125">-MinServers</span><span class="sxs-lookup"><span data-stu-id="9292f-125">-MinServers</span></span>
<span data-ttu-id="9292f-126">Número mínimo de servidores que sempre estão marcados como íntegros.</span><span class="sxs-lookup"><span data-stu-id="9292f-126">Minimum number of servers that are always marked healthy.</span></span>
<span data-ttu-id="9292f-127">O valor padrão é 0</span><span class="sxs-lookup"><span data-stu-id="9292f-127">Default value is 0</span></span>

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

### <span data-ttu-id="9292f-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="9292f-128">-Name</span></span>
<span data-ttu-id="9292f-129">Especifica o nome do teste.</span><span class="sxs-lookup"><span data-stu-id="9292f-129">Specifies the name of the probe.</span></span>

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

### <span data-ttu-id="9292f-130">-Caminho</span><span class="sxs-lookup"><span data-stu-id="9292f-130">-Path</span></span>
<span data-ttu-id="9292f-131">Especifica o caminho relativo do teste.</span><span class="sxs-lookup"><span data-stu-id="9292f-131">Specifies the relative path of probe.</span></span>
<span data-ttu-id="9292f-132">Caminhos válidos começam com o caractere de barra (/).</span><span class="sxs-lookup"><span data-stu-id="9292f-132">Valid paths start with the slash character (/).</span></span>
<span data-ttu-id="9292f-133">O teste é enviado para o \< caminho de porta do protocolo \> :// \< host \> : \< \> \< \> .</span><span class="sxs-lookup"><span data-stu-id="9292f-133">The probe is sent to \<Protocol\>://\<host\>:\<port\>\<path\>.</span></span>

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

### <span data-ttu-id="9292f-134">-PickHostNameFromBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="9292f-134">-PickHostNameFromBackendHttpSettings</span></span>
<span data-ttu-id="9292f-135">Se o cabeçalho do host deve ser selecionado nas configurações http de back-end.</span><span class="sxs-lookup"><span data-stu-id="9292f-135">Whether the host header should be picked from the backend http settings.</span></span>
<span data-ttu-id="9292f-136">O valor padrão é falso</span><span class="sxs-lookup"><span data-stu-id="9292f-136">Default value is false</span></span>

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

### <span data-ttu-id="9292f-137">-Protocolo</span><span class="sxs-lookup"><span data-stu-id="9292f-137">-Protocol</span></span>
<span data-ttu-id="9292f-138">Especifica o protocolo usado para enviar o teste.</span><span class="sxs-lookup"><span data-stu-id="9292f-138">Specifies the protocol used to send probe.</span></span>

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

### <span data-ttu-id="9292f-139">-Timeout</span><span class="sxs-lookup"><span data-stu-id="9292f-139">-Timeout</span></span>
<span data-ttu-id="9292f-140">Especifica o tempo limite do teste em segundos.</span><span class="sxs-lookup"><span data-stu-id="9292f-140">Specifies the probe timeout in seconds.</span></span>
<span data-ttu-id="9292f-141">Esse cmdlet marca o teste como Failed se uma resposta válida não for recebida com esse período de tempo limite.</span><span class="sxs-lookup"><span data-stu-id="9292f-141">This cmdlet marks the probe as failed if a valid response is not received with this timeout period.</span></span>
<span data-ttu-id="9292f-142">Os valores válidos estão entre 1 segundo e 86400 segundos.</span><span class="sxs-lookup"><span data-stu-id="9292f-142">Valid values are between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="9292f-143">-UnhealthyThreshold</span><span class="sxs-lookup"><span data-stu-id="9292f-143">-UnhealthyThreshold</span></span>
<span data-ttu-id="9292f-144">Especifica a contagem de repetição de teste.</span><span class="sxs-lookup"><span data-stu-id="9292f-144">Specifies the probe retry count.</span></span>
<span data-ttu-id="9292f-145">O servidor back-end está marcado para baixo após a contagem de falhas de investigação consecutiva alcançar o limite não íntegro.</span><span class="sxs-lookup"><span data-stu-id="9292f-145">The backend server is marked down after consecutive probe failure count reaches the unhealthy threshold.</span></span>
<span data-ttu-id="9292f-146">Os valores válidos estão entre 1 segundo e 20 segundos.</span><span class="sxs-lookup"><span data-stu-id="9292f-146">Valid values are between 1 second and 20 seconds.</span></span>

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

### <span data-ttu-id="9292f-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9292f-147">CommonParameters</span></span>
<span data-ttu-id="9292f-148">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9292f-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9292f-149">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9292f-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9292f-150">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9292f-150">INPUTS</span></span>

### <span data-ttu-id="9292f-151">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9292f-151">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="9292f-152">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9292f-152">OUTPUTS</span></span>

### <span data-ttu-id="9292f-153">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9292f-153">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="9292f-154">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9292f-154">NOTES</span></span>

## <span data-ttu-id="9292f-155">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9292f-155">RELATED LINKS</span></span>

[<span data-ttu-id="9292f-156">Add-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="9292f-156">Add-AzApplicationGatewayProbeConfig</span></span>](./Add-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="9292f-157">Get-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="9292f-157">Get-AzApplicationGatewayProbeConfig</span></span>](./Get-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="9292f-158">New-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="9292f-158">New-AzApplicationGatewayProbeConfig</span></span>](./New-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="9292f-159">Remove-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="9292f-159">Remove-AzApplicationGatewayProbeConfig</span></span>](./Remove-AzApplicationGatewayProbeConfig.md)


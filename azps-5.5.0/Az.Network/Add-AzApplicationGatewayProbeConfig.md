---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayProbeConfig.md
ms.openlocfilehash: cea6f92ba15e43d5977af03dfee1054240f5ecad
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114211"
---
# <span data-ttu-id="fc264-101">Add-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="fc264-101">Add-AzApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="fc264-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fc264-102">SYNOPSIS</span></span>
<span data-ttu-id="fc264-103">Adiciona um problema de saúde a um Gateway de Aplicativo.</span><span class="sxs-lookup"><span data-stu-id="fc264-103">Adds a health probe to an Application Gateway.</span></span>

## <span data-ttu-id="fc264-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fc264-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayProbeConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -Protocol <String> [-HostName <String>] -Path <String> -Interval <Int32> -Timeout <Int32>
 -UnhealthyThreshold <Int32> [-PickHostNameFromBackendHttpSettings] [-MinServers <Int32>]
 [-Match <PSApplicationGatewayProbeHealthResponseMatch>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fc264-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="fc264-105">DESCRIPTION</span></span>
<span data-ttu-id="fc264-106">O Add-AzApplicationGatewayProbeConfig cmdlet adiciona um problema de saúde a um Gateway de Aplicativos.</span><span class="sxs-lookup"><span data-stu-id="fc264-106">The Add-AzApplicationGatewayProbeConfig cmdlet adds a health probe to an Application Gateway.</span></span>

## <span data-ttu-id="fc264-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="fc264-107">EXAMPLES</span></span>

### <span data-ttu-id="fc264-108">Exemplo 1: Adicionar um problema de saúde a um gateway de aplicativo</span><span class="sxs-lookup"><span data-stu-id="fc264-108">Example 1: Add a health probe to an application gateway</span></span>
```
PS C:\>$Probe = Add-AzApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe01" -Protocol Http -HostName "contoso.com" -Path "/path/custompath.htm" -Interval 30 -Timeout 120 -UnhealthyThreshold 8
```

<span data-ttu-id="fc264-109">Este comando adiciona uma confirmação de saúde chamada " Sor01 " para o gateway de aplicativo chamado Gateway.</span><span class="sxs-lookup"><span data-stu-id="fc264-109">This command adds a health probe named Probe01 for the application gateway named Gateway.</span></span>
<span data-ttu-id="fc264-110">O comando também define o limite não saudável para 8 recuperações e horas após 120 segundos.</span><span class="sxs-lookup"><span data-stu-id="fc264-110">The command also sets the unhealthy threshold to 8 retries and times out after 120 seconds.</span></span>

## <span data-ttu-id="fc264-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fc264-111">PARAMETERS</span></span>

### <span data-ttu-id="fc264-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fc264-112">-ApplicationGateway</span></span>
<span data-ttu-id="fc264-113">Especifica o gateway do aplicativo ao qual este cmdlet adiciona uma pontuação.</span><span class="sxs-lookup"><span data-stu-id="fc264-113">Specifies the application gateway to which this cmdlet adds a probe.</span></span>

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

### <span data-ttu-id="fc264-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc264-114">-DefaultProfile</span></span>
<span data-ttu-id="fc264-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="fc264-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fc264-116">-Nomedo Host</span><span class="sxs-lookup"><span data-stu-id="fc264-116">-HostName</span></span>
<span data-ttu-id="fc264-117">Especifica o nome do host para o que este cmdlet envia a confirmação.</span><span class="sxs-lookup"><span data-stu-id="fc264-117">Specifies the host name that this cmdlet sends the probe to.</span></span>

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

### <span data-ttu-id="fc264-118">-Intervalo</span><span class="sxs-lookup"><span data-stu-id="fc264-118">-Interval</span></span>
<span data-ttu-id="fc264-119">Especifica o intervalo de intervalo de intervalo em segundos.</span><span class="sxs-lookup"><span data-stu-id="fc264-119">Specifies the probe interval in seconds.</span></span>
<span data-ttu-id="fc264-120">Este é o intervalo de tempo entre duas reações consecutivas.</span><span class="sxs-lookup"><span data-stu-id="fc264-120">This is the time interval between two consecutive probes.</span></span>
<span data-ttu-id="fc264-121">Esse valor está entre 1 segundo e 86400 segundos.</span><span class="sxs-lookup"><span data-stu-id="fc264-121">This value is between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="fc264-122">-Match</span><span class="sxs-lookup"><span data-stu-id="fc264-122">-Match</span></span>
<span data-ttu-id="fc264-123">Corpo que deve estar contido na resposta à saúde.</span><span class="sxs-lookup"><span data-stu-id="fc264-123">Body that must be contained in the health response.</span></span>
<span data-ttu-id="fc264-124">O valor padrão está vazio</span><span class="sxs-lookup"><span data-stu-id="fc264-124">Default value is empty</span></span>

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

### <span data-ttu-id="fc264-125">-MinServers</span><span class="sxs-lookup"><span data-stu-id="fc264-125">-MinServers</span></span>
<span data-ttu-id="fc264-126">Número mínimo de servidores que estão sempre marcados como saudáveis.</span><span class="sxs-lookup"><span data-stu-id="fc264-126">Minimum number of servers that are always marked healthy.</span></span>
<span data-ttu-id="fc264-127">O valor padrão é 0</span><span class="sxs-lookup"><span data-stu-id="fc264-127">Default value is 0</span></span>

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

### <span data-ttu-id="fc264-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="fc264-128">-Name</span></span>
<span data-ttu-id="fc264-129">Especifica o nome da sonda.</span><span class="sxs-lookup"><span data-stu-id="fc264-129">Specifies the name of the probe.</span></span>

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

### <span data-ttu-id="fc264-130">-Caminho</span><span class="sxs-lookup"><span data-stu-id="fc264-130">-Path</span></span>
<span data-ttu-id="fc264-131">Especifica o caminho relativo da investigação.</span><span class="sxs-lookup"><span data-stu-id="fc264-131">Specifies the relative path of probe.</span></span>
<span data-ttu-id="fc264-132">Início de caminho válido com o caractere de barra (/).</span><span class="sxs-lookup"><span data-stu-id="fc264-132">Valid path start with the slash character (/).</span></span>
<span data-ttu-id="fc264-133">A sonda é enviada para \<Protocol\> :// \<host\> : \<port\> \<path\> .</span><span class="sxs-lookup"><span data-stu-id="fc264-133">The probe is sent to \<Protocol\>://\<host\>:\<port\>\<path\>.</span></span>

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

### <span data-ttu-id="fc264-134">-PickHostNameFromBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="fc264-134">-PickHostNameFromBackendHttpSettings</span></span>
<span data-ttu-id="fc264-135">Se o cabeçalho do host deve ser escolhido nas configurações de http back-end.</span><span class="sxs-lookup"><span data-stu-id="fc264-135">Whether the host header should be picked from the backend http settings.</span></span>
<span data-ttu-id="fc264-136">O valor padrão é falso</span><span class="sxs-lookup"><span data-stu-id="fc264-136">Default value is false</span></span>

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

### <span data-ttu-id="fc264-137">-Protocolo</span><span class="sxs-lookup"><span data-stu-id="fc264-137">-Protocol</span></span>
<span data-ttu-id="fc264-138">Especifica o protocolo usado para enviar teste.</span><span class="sxs-lookup"><span data-stu-id="fc264-138">Specifies the protocol used to send probe.</span></span>
<span data-ttu-id="fc264-139">Este cmdlet é compatível apenas com HTTP.</span><span class="sxs-lookup"><span data-stu-id="fc264-139">This cmdlet supports HTTP only.</span></span>

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

### <span data-ttu-id="fc264-140">-Tempo de tempo</span><span class="sxs-lookup"><span data-stu-id="fc264-140">-Timeout</span></span>
<span data-ttu-id="fc264-141">Especifica o tempo de teste em segundos.</span><span class="sxs-lookup"><span data-stu-id="fc264-141">Specifies the probe timeout in seconds.</span></span>
<span data-ttu-id="fc264-142">Este cmdlet marcará a falha se uma resposta válida não for recebida com esse período de tempo.</span><span class="sxs-lookup"><span data-stu-id="fc264-142">This cmdlet marks the probe as failed if a valid response is not received with this timeout period.</span></span>
<span data-ttu-id="fc264-143">Os valores válidos estão entre 1 segundo e 86400 segundos.</span><span class="sxs-lookup"><span data-stu-id="fc264-143">Valid values are between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="fc264-144">-Insalubreshold</span><span class="sxs-lookup"><span data-stu-id="fc264-144">-UnhealthyThreshold</span></span>
<span data-ttu-id="fc264-145">Especifica a contagem de tentar novamente.</span><span class="sxs-lookup"><span data-stu-id="fc264-145">Specifies the probe retry count.</span></span>
<span data-ttu-id="fc264-146">O servidor back-end é marcado para baixo depois que a contagem consecutiva de falhas de falha na falha atinge o limite não saudável.</span><span class="sxs-lookup"><span data-stu-id="fc264-146">The backend server is marked down after consecutive probe failure count reaches the unhealthy threshold.</span></span>
<span data-ttu-id="fc264-147">Os valores válidos estão entre 1 segundo e 20 segundos.</span><span class="sxs-lookup"><span data-stu-id="fc264-147">Valid values are between 1 second and 20 seconds.</span></span>

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

### <span data-ttu-id="fc264-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc264-148">CommonParameters</span></span>
<span data-ttu-id="fc264-149">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc264-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc264-150">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc264-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc264-151">Entradas</span><span class="sxs-lookup"><span data-stu-id="fc264-151">INPUTS</span></span>

### <span data-ttu-id="fc264-152">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fc264-152">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="fc264-153">Saídas</span><span class="sxs-lookup"><span data-stu-id="fc264-153">OUTPUTS</span></span>

### <span data-ttu-id="fc264-154">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fc264-154">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="fc264-155">Notas</span><span class="sxs-lookup"><span data-stu-id="fc264-155">NOTES</span></span>

## <span data-ttu-id="fc264-156">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fc264-156">RELATED LINKS</span></span>

[<span data-ttu-id="fc264-157">Adicionar um problema a um gateway de aplicativo existente</span><span class="sxs-lookup"><span data-stu-id="fc264-157">Add a probe to an existing application gateway</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#add-a-probe-to-an-existing-application-gateway)

[<span data-ttu-id="fc264-158">Get-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="fc264-158">Get-AzApplicationGatewayProbeConfig</span></span>](./Get-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="fc264-159">New-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="fc264-159">New-AzApplicationGatewayProbeConfig</span></span>](./New-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="fc264-160">Remove-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="fc264-160">Remove-AzApplicationGatewayProbeConfig</span></span>](./Remove-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="fc264-161">Set-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="fc264-161">Set-AzApplicationGatewayProbeConfig</span></span>](./Set-AzApplicationGatewayProbeConfig.md)


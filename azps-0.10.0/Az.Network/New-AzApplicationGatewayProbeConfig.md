---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayProbeConfig.md
ms.openlocfilehash: 43c74d2edd2cfd07f65b7d5437bf1cf5c0dfca9f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775426"
---
# <span data-ttu-id="2e451-101">New-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="2e451-101">New-AzApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="2e451-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2e451-102">SYNOPSIS</span></span>
<span data-ttu-id="2e451-103">Cria uma sondagem de integridade.</span><span class="sxs-lookup"><span data-stu-id="2e451-103">Creates a health probe.</span></span>

## <span data-ttu-id="2e451-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2e451-104">SYNTAX</span></span>

```
New-AzApplicationGatewayProbeConfig -Name <String> -Protocol <String> [-HostName <String>] -Path <String>
 -Interval <Int32> -Timeout <Int32> -UnhealthyThreshold <Int32> [-PickHostNameFromBackendHttpSettings]
 [-MinServers <Int32>] [-Match <PSApplicationGatewayProbeHealthResponseMatch>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2e451-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2e451-105">DESCRIPTION</span></span>
<span data-ttu-id="2e451-106">O cmdlet New-AzApplicationGatewayProbeConfig cria uma sondagem de integridade.</span><span class="sxs-lookup"><span data-stu-id="2e451-106">The New-AzApplicationGatewayProbeConfig cmdlet creates a health probe.</span></span>

## <span data-ttu-id="2e451-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2e451-107">EXAMPLES</span></span>

### <span data-ttu-id="2e451-108">Example1: criar uma sondagem de integridade</span><span class="sxs-lookup"><span data-stu-id="2e451-108">Example1: Create a health probe</span></span>
```
PS C:\>New-AzApplicationGatewayProbeConfig -Name "Probe03" -Protocol Http -HostName "contoso.com" -Path "/path/custompath.htm" -Interval 30 -Timeout 120 -UnhealthyThreshold 8
```

<span data-ttu-id="2e451-109">Esse comando cria um teste de integridade chamado Probe03, com o protocolo HTTP, um intervalo de 30 segundos, o tempo limite de 120 segundos e um limiar não íntegro de 8 tentativas.</span><span class="sxs-lookup"><span data-stu-id="2e451-109">This command creates a health probe named Probe03, with HTTP protocol, a 30 second interval, timeout of 120 seconds, and an unhealthy threshold of 8 retries.</span></span>

## <span data-ttu-id="2e451-110">OS</span><span class="sxs-lookup"><span data-stu-id="2e451-110">PARAMETERS</span></span>

### <span data-ttu-id="2e451-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e451-111">-DefaultProfile</span></span>
<span data-ttu-id="2e451-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2e451-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e451-113">-HostName</span><span class="sxs-lookup"><span data-stu-id="2e451-113">-HostName</span></span>
<span data-ttu-id="2e451-114">Especifica o nome do host para o qual esse cmdlet envia o teste.</span><span class="sxs-lookup"><span data-stu-id="2e451-114">Specifies the host name that this cmdlet sends the probe.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e451-115">-Intervalo</span><span class="sxs-lookup"><span data-stu-id="2e451-115">-Interval</span></span>
<span data-ttu-id="2e451-116">Especifica o intervalo de sondagem em segundos.</span><span class="sxs-lookup"><span data-stu-id="2e451-116">Specifies the probe interval in seconds.</span></span>
<span data-ttu-id="2e451-117">Esse é o intervalo de tempo entre dois testes consecutivos.</span><span class="sxs-lookup"><span data-stu-id="2e451-117">This is the time interval between two consecutive probes.</span></span>
<span data-ttu-id="2e451-118">Esse valor é entre 1 segundo e 86400 segundos.</span><span class="sxs-lookup"><span data-stu-id="2e451-118">This value is between 1 second and 86400 seconds.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e451-119">-Match</span><span class="sxs-lookup"><span data-stu-id="2e451-119">-Match</span></span>
<span data-ttu-id="2e451-120">Corpo que deve estar contido na resposta de integridade.</span><span class="sxs-lookup"><span data-stu-id="2e451-120">Body that must be contained in the health response.</span></span>
<span data-ttu-id="2e451-121">O valor padrão está vazio</span><span class="sxs-lookup"><span data-stu-id="2e451-121">Default value is empty</span></span>

```yaml
Type: PSApplicationGatewayProbeHealthResponseMatch
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e451-122">-MinServers</span><span class="sxs-lookup"><span data-stu-id="2e451-122">-MinServers</span></span>
<span data-ttu-id="2e451-123">Número mínimo de servidores que sempre estão marcados como íntegros.</span><span class="sxs-lookup"><span data-stu-id="2e451-123">Minimum number of servers that are always marked healthy.</span></span>
<span data-ttu-id="2e451-124">O valor padrão é 0</span><span class="sxs-lookup"><span data-stu-id="2e451-124">Default value is 0</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e451-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="2e451-125">-Name</span></span>
<span data-ttu-id="2e451-126">Especifica o nome do teste.</span><span class="sxs-lookup"><span data-stu-id="2e451-126">Specifies the name of the probe.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e451-127">-Caminho</span><span class="sxs-lookup"><span data-stu-id="2e451-127">-Path</span></span>
<span data-ttu-id="2e451-128">Especifica o caminho relativo do teste.</span><span class="sxs-lookup"><span data-stu-id="2e451-128">Specifies the relative path of probe.</span></span>
<span data-ttu-id="2e451-129">Caminhos válidos começam com o caractere de barra (/).</span><span class="sxs-lookup"><span data-stu-id="2e451-129">Valid paths start with the slash character (/).</span></span>
<span data-ttu-id="2e451-130">O teste é enviado para o \< caminho de porta do protocolo \> :// \< host \> : \< \> \< \> .</span><span class="sxs-lookup"><span data-stu-id="2e451-130">The probe is sent to \<Protocol\>://\<host\>:\<port\>\<path\>.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e451-131">-PickHostNameFromBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="2e451-131">-PickHostNameFromBackendHttpSettings</span></span>
<span data-ttu-id="2e451-132">Se o cabeçalho do host deve ser selecionado nas configurações http de back-end.</span><span class="sxs-lookup"><span data-stu-id="2e451-132">Whether the host header should be picked from the backend http settings.</span></span>
<span data-ttu-id="2e451-133">O valor padrão é falso</span><span class="sxs-lookup"><span data-stu-id="2e451-133">Default value is false</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e451-134">-Protocolo</span><span class="sxs-lookup"><span data-stu-id="2e451-134">-Protocol</span></span>
<span data-ttu-id="2e451-135">Especifica o protocolo usado para enviar o teste.</span><span class="sxs-lookup"><span data-stu-id="2e451-135">Specifies the protocol used to send probe.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Http, Https

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e451-136">-Timeout</span><span class="sxs-lookup"><span data-stu-id="2e451-136">-Timeout</span></span>
<span data-ttu-id="2e451-137">Especifica o tempo limite do teste em segundos.</span><span class="sxs-lookup"><span data-stu-id="2e451-137">Specifies the probe timeout in seconds.</span></span>
<span data-ttu-id="2e451-138">Esse cmdlet marca o teste como Failed se uma resposta válida não for recebida com esse período de tempo limite.</span><span class="sxs-lookup"><span data-stu-id="2e451-138">This cmdlet marks the probe as failed if a valid response is not received with this timeout period.</span></span>
<span data-ttu-id="2e451-139">Os valores válidos estão entre 1 segundo e 86400 segundos.</span><span class="sxs-lookup"><span data-stu-id="2e451-139">Valid values are between 1 second and 86400 seconds.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e451-140">-UnhealthyThreshold</span><span class="sxs-lookup"><span data-stu-id="2e451-140">-UnhealthyThreshold</span></span>
<span data-ttu-id="2e451-141">Especifica a contagem de repetição de teste.</span><span class="sxs-lookup"><span data-stu-id="2e451-141">Specifies the probe retry count.</span></span>
<span data-ttu-id="2e451-142">O servidor back-end está marcado para baixo após a contagem de falhas de investigação consecutiva alcançar o limite não íntegro.</span><span class="sxs-lookup"><span data-stu-id="2e451-142">The backend server is marked down after consecutive probe failure count reaches the unhealthy threshold.</span></span>
<span data-ttu-id="2e451-143">Os valores válidos estão entre 1 segundo e 20 segundos.</span><span class="sxs-lookup"><span data-stu-id="2e451-143">Valid values are between 1 second and 20 seconds.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e451-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e451-144">CommonParameters</span></span>
<span data-ttu-id="2e451-145">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e451-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e451-146">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2e451-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e451-147">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2e451-147">INPUTS</span></span>

## <span data-ttu-id="2e451-148">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2e451-148">OUTPUTS</span></span>

### <span data-ttu-id="2e451-149">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayProbe</span><span class="sxs-lookup"><span data-stu-id="2e451-149">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe</span></span>

## <span data-ttu-id="2e451-150">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2e451-150">NOTES</span></span>

## <span data-ttu-id="2e451-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2e451-151">RELATED LINKS</span></span>

[<span data-ttu-id="2e451-152">Criar investigação personalizada do Application Gateway usando o PowerShell para Azure Resource Manager</span><span class="sxs-lookup"><span data-stu-id="2e451-152">Create custom probe for Application Gateway using PowerShell for Azure Resource Manager</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#)

[<span data-ttu-id="2e451-153">Add-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="2e451-153">Add-AzApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="2e451-154">Get-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="2e451-154">Get-AzApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="2e451-155">Remove-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="2e451-155">Remove-AzApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="2e451-156">Set-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="2e451-156">Set-AzApplicationGatewayProbeConfig</span></span>]()

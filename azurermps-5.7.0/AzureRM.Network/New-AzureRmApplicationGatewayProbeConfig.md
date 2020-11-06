---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewayprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayProbeConfig.md
ms.openlocfilehash: 955f5179340351dd662979385ca3d3dc2a39b9f7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432452"
---
# <span data-ttu-id="6b2fb-101">New-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="6b2fb-101">New-AzureRmApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="6b2fb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6b2fb-102">SYNOPSIS</span></span>
<span data-ttu-id="6b2fb-103">Cria uma sondagem de integridade.</span><span class="sxs-lookup"><span data-stu-id="6b2fb-103">Creates a health probe.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6b2fb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6b2fb-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayProbeConfig -Name <String> -Protocol <String> [-HostName <String>] -Path <String>
 -Interval <Int32> -Timeout <Int32> -UnhealthyThreshold <Int32> [-PickHostNameFromBackendHttpSettings]
 [-MinServers <Int32>] [-Match <PSApplicationGatewayProbeHealthResponseMatch>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6b2fb-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6b2fb-105">DESCRIPTION</span></span>
<span data-ttu-id="6b2fb-106">O cmdlet New-AzureRmApplicationGatewayProbeConfig cria uma sondagem de integridade.</span><span class="sxs-lookup"><span data-stu-id="6b2fb-106">The New-AzureRmApplicationGatewayProbeConfig cmdlet creates a health probe.</span></span>

## <span data-ttu-id="6b2fb-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6b2fb-107">EXAMPLES</span></span>

### <span data-ttu-id="6b2fb-108">Example1: criar uma sondagem de integridade</span><span class="sxs-lookup"><span data-stu-id="6b2fb-108">Example1: Create a health probe</span></span>
```
PS C:\>New-AzureRmApplicationGatewayProbeConfig -Name "Probe03" -Protocol Http -HostName "contoso.com" -Path "/path/custompath.htm" -Interval 30 -Timeout 120 -UnhealthyThreshold 8
```

<span data-ttu-id="6b2fb-109">Esse comando cria um teste de integridade chamado Probe03, com o protocolo HTTP, um intervalo de 30 segundos, o tempo limite de 120 segundos e um limiar não íntegro de 8 tentativas.</span><span class="sxs-lookup"><span data-stu-id="6b2fb-109">This command creates a health probe named Probe03, with HTTP protocol, a 30 second interval, timeout of 120 seconds, and an unhealthy threshold of 8 retries.</span></span>

## <span data-ttu-id="6b2fb-110">OS</span><span class="sxs-lookup"><span data-stu-id="6b2fb-110">PARAMETERS</span></span>

### <span data-ttu-id="6b2fb-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b2fb-111">-DefaultProfile</span></span>
<span data-ttu-id="6b2fb-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6b2fb-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6b2fb-113">-HostName</span><span class="sxs-lookup"><span data-stu-id="6b2fb-113">-HostName</span></span>
<span data-ttu-id="6b2fb-114">Especifica o nome do host para o qual esse cmdlet envia o teste.</span><span class="sxs-lookup"><span data-stu-id="6b2fb-114">Specifies the host name that this cmdlet sends the probe.</span></span>

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

### <span data-ttu-id="6b2fb-115">-Intervalo</span><span class="sxs-lookup"><span data-stu-id="6b2fb-115">-Interval</span></span>
<span data-ttu-id="6b2fb-116">Especifica o intervalo de sondagem em segundos.</span><span class="sxs-lookup"><span data-stu-id="6b2fb-116">Specifies the probe interval in seconds.</span></span>
<span data-ttu-id="6b2fb-117">Esse é o intervalo de tempo entre dois testes consecutivos.</span><span class="sxs-lookup"><span data-stu-id="6b2fb-117">This is the time interval between two consecutive probes.</span></span>
<span data-ttu-id="6b2fb-118">Esse valor é entre 1 segundo e 86400 segundos.</span><span class="sxs-lookup"><span data-stu-id="6b2fb-118">This value is between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="6b2fb-119">-Match</span><span class="sxs-lookup"><span data-stu-id="6b2fb-119">-Match</span></span>
<span data-ttu-id="6b2fb-120">Corpo que deve estar contido na resposta de integridade.</span><span class="sxs-lookup"><span data-stu-id="6b2fb-120">Body that must be contained in the health response.</span></span>
<span data-ttu-id="6b2fb-121">O valor padrão está vazio</span><span class="sxs-lookup"><span data-stu-id="6b2fb-121">Default value is empty</span></span>

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

### <span data-ttu-id="6b2fb-122">-MinServers</span><span class="sxs-lookup"><span data-stu-id="6b2fb-122">-MinServers</span></span>
<span data-ttu-id="6b2fb-123">Número mínimo de servidores que sempre estão marcados como íntegros.</span><span class="sxs-lookup"><span data-stu-id="6b2fb-123">Minimum number of servers that are always marked healthy.</span></span>
<span data-ttu-id="6b2fb-124">O valor padrão é 0</span><span class="sxs-lookup"><span data-stu-id="6b2fb-124">Default value is 0</span></span>

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

### <span data-ttu-id="6b2fb-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="6b2fb-125">-Name</span></span>
<span data-ttu-id="6b2fb-126">Especifica o nome do teste.</span><span class="sxs-lookup"><span data-stu-id="6b2fb-126">Specifies the name of the probe.</span></span>

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

### <span data-ttu-id="6b2fb-127">-Caminho</span><span class="sxs-lookup"><span data-stu-id="6b2fb-127">-Path</span></span>
<span data-ttu-id="6b2fb-128">Especifica o caminho relativo do teste.</span><span class="sxs-lookup"><span data-stu-id="6b2fb-128">Specifies the relative path of probe.</span></span>
<span data-ttu-id="6b2fb-129">Caminhos válidos começam com o caractere de barra (/).</span><span class="sxs-lookup"><span data-stu-id="6b2fb-129">Valid paths start with the slash character (/).</span></span>
<span data-ttu-id="6b2fb-130">O teste é enviado para \<Protocol\> :// \<host\> : \<port\> \<path\> .</span><span class="sxs-lookup"><span data-stu-id="6b2fb-130">The probe is sent to \<Protocol\>://\<host\>:\<port\>\<path\>.</span></span>

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

### <span data-ttu-id="6b2fb-131">-PickHostNameFromBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="6b2fb-131">-PickHostNameFromBackendHttpSettings</span></span>
<span data-ttu-id="6b2fb-132">Se o cabeçalho do host deve ser selecionado nas configurações http de back-end.</span><span class="sxs-lookup"><span data-stu-id="6b2fb-132">Whether the host header should be picked from the backend http settings.</span></span>
<span data-ttu-id="6b2fb-133">O valor padrão é falso</span><span class="sxs-lookup"><span data-stu-id="6b2fb-133">Default value is false</span></span>

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

### <span data-ttu-id="6b2fb-134">-Protocolo</span><span class="sxs-lookup"><span data-stu-id="6b2fb-134">-Protocol</span></span>
<span data-ttu-id="6b2fb-135">Especifica o protocolo usado para enviar o teste.</span><span class="sxs-lookup"><span data-stu-id="6b2fb-135">Specifies the protocol used to send probe.</span></span>

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

### <span data-ttu-id="6b2fb-136">-Timeout</span><span class="sxs-lookup"><span data-stu-id="6b2fb-136">-Timeout</span></span>
<span data-ttu-id="6b2fb-137">Especifica o tempo limite do teste em segundos.</span><span class="sxs-lookup"><span data-stu-id="6b2fb-137">Specifies the probe timeout in seconds.</span></span>
<span data-ttu-id="6b2fb-138">Esse cmdlet marca o teste como Failed se uma resposta válida não for recebida com esse período de tempo limite.</span><span class="sxs-lookup"><span data-stu-id="6b2fb-138">This cmdlet marks the probe as failed if a valid response is not received with this timeout period.</span></span>
<span data-ttu-id="6b2fb-139">Os valores válidos estão entre 1 segundo e 86400 segundos.</span><span class="sxs-lookup"><span data-stu-id="6b2fb-139">Valid values are between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="6b2fb-140">-UnhealthyThreshold</span><span class="sxs-lookup"><span data-stu-id="6b2fb-140">-UnhealthyThreshold</span></span>
<span data-ttu-id="6b2fb-141">Especifica a contagem de repetição de teste.</span><span class="sxs-lookup"><span data-stu-id="6b2fb-141">Specifies the probe retry count.</span></span>
<span data-ttu-id="6b2fb-142">O servidor back-end está marcado para baixo após a contagem de falhas de investigação consecutiva alcançar o limite não íntegro.</span><span class="sxs-lookup"><span data-stu-id="6b2fb-142">The backend server is marked down after consecutive probe failure count reaches the unhealthy threshold.</span></span>
<span data-ttu-id="6b2fb-143">Os valores válidos estão entre 1 segundo e 20 segundos.</span><span class="sxs-lookup"><span data-stu-id="6b2fb-143">Valid values are between 1 second and 20 seconds.</span></span>

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

### <span data-ttu-id="6b2fb-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b2fb-144">CommonParameters</span></span>
<span data-ttu-id="6b2fb-145">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b2fb-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b2fb-146">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6b2fb-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b2fb-147">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6b2fb-147">INPUTS</span></span>

### <span data-ttu-id="6b2fb-148">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="6b2fb-148">None</span></span>
<span data-ttu-id="6b2fb-149">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="6b2fb-149">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6b2fb-150">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6b2fb-150">OUTPUTS</span></span>

### <span data-ttu-id="6b2fb-151">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayProbe</span><span class="sxs-lookup"><span data-stu-id="6b2fb-151">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe</span></span>

## <span data-ttu-id="6b2fb-152">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6b2fb-152">NOTES</span></span>

## <span data-ttu-id="6b2fb-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6b2fb-153">RELATED LINKS</span></span>

[<span data-ttu-id="6b2fb-154">Criar investigação personalizada do Application Gateway usando o PowerShell para Azure Resource Manager</span><span class="sxs-lookup"><span data-stu-id="6b2fb-154">Create custom probe for Application Gateway using PowerShell for Azure Resource Manager</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#)

[<span data-ttu-id="6b2fb-155">Add-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="6b2fb-155">Add-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="6b2fb-156">Get-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="6b2fb-156">Get-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="6b2fb-157">Remove-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="6b2fb-157">Remove-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="6b2fb-158">Set-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="6b2fb-158">Set-AzureRmApplicationGatewayProbeConfig</span></span>]()


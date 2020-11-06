---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayProbeConfig.md
ms.openlocfilehash: a41daa12a126e768a4cc7842a72b031d4ca7a759
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93439915"
---
# <span data-ttu-id="2bfda-101">New-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="2bfda-101">New-AzureRmApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="2bfda-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2bfda-102">SYNOPSIS</span></span>
<span data-ttu-id="2bfda-103">Cria uma sondagem de integridade.</span><span class="sxs-lookup"><span data-stu-id="2bfda-103">Creates a health probe.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2bfda-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2bfda-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayProbeConfig -Name <String> -Protocol <String> [-HostName <String>] -Path <String>
 -Interval <Int32> -Timeout <Int32> -UnhealthyThreshold <Int32> [-PickHostNameFromBackendHttpSettings]
 [-MinServers <Int32>] [-Match <PSApplicationGatewayProbeHealthResponseMatch>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2bfda-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2bfda-105">DESCRIPTION</span></span>
<span data-ttu-id="2bfda-106">O cmdlet New-AzureRmApplicationGatewayProbeConfig cria uma sondagem de integridade.</span><span class="sxs-lookup"><span data-stu-id="2bfda-106">The New-AzureRmApplicationGatewayProbeConfig cmdlet creates a health probe.</span></span>

## <span data-ttu-id="2bfda-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2bfda-107">EXAMPLES</span></span>

### <span data-ttu-id="2bfda-108">Example1: criar uma sondagem de integridade</span><span class="sxs-lookup"><span data-stu-id="2bfda-108">Example1: Create a health probe</span></span>
```
PS C:\>New-AzureRmApplicationGatewayProbeConfig -Name "Probe03" -Protocol Http -HostName "contoso.com" -Path "/path/custompath.htm" -Interval 30 -Timeout 120 -UnhealthyThreshold 8
```

<span data-ttu-id="2bfda-109">Esse comando cria um teste de integridade chamado Probe03, com o protocolo HTTP, um intervalo de 30 segundos, o tempo limite de 120 segundos e um limiar não íntegro de 8 tentativas.</span><span class="sxs-lookup"><span data-stu-id="2bfda-109">This command creates a health probe named Probe03, with HTTP protocol, a 30 second interval, timeout of 120 seconds, and an unhealthy threshold of 8 retries.</span></span>

## <span data-ttu-id="2bfda-110">OS</span><span class="sxs-lookup"><span data-stu-id="2bfda-110">PARAMETERS</span></span>

### <span data-ttu-id="2bfda-111">-HostName</span><span class="sxs-lookup"><span data-stu-id="2bfda-111">-HostName</span></span>
<span data-ttu-id="2bfda-112">Especifica o nome do host para o qual esse cmdlet envia o teste.</span><span class="sxs-lookup"><span data-stu-id="2bfda-112">Specifies the host name that this cmdlet sends the probe.</span></span>

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

### <span data-ttu-id="2bfda-113">-Intervalo</span><span class="sxs-lookup"><span data-stu-id="2bfda-113">-Interval</span></span>
<span data-ttu-id="2bfda-114">Especifica o intervalo de sondagem em segundos.</span><span class="sxs-lookup"><span data-stu-id="2bfda-114">Specifies the probe interval in seconds.</span></span>
<span data-ttu-id="2bfda-115">Esse é o intervalo de tempo entre dois testes consecutivos.</span><span class="sxs-lookup"><span data-stu-id="2bfda-115">This is the time interval between two consecutive probes.</span></span>
<span data-ttu-id="2bfda-116">Esse valor é entre 1 segundo e 86400 segundos.</span><span class="sxs-lookup"><span data-stu-id="2bfda-116">This value is between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="2bfda-117">-Match</span><span class="sxs-lookup"><span data-stu-id="2bfda-117">-Match</span></span>
<span data-ttu-id="2bfda-118">Corpo que deve estar contido na resposta de integridade.</span><span class="sxs-lookup"><span data-stu-id="2bfda-118">Body that must be contained in the health response.</span></span>
<span data-ttu-id="2bfda-119">O valor padrão está vazio</span><span class="sxs-lookup"><span data-stu-id="2bfda-119">Default value is empty</span></span>

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

### <span data-ttu-id="2bfda-120">-MinServers</span><span class="sxs-lookup"><span data-stu-id="2bfda-120">-MinServers</span></span>
<span data-ttu-id="2bfda-121">Número mínimo de servidores que sempre estão marcados como íntegros.</span><span class="sxs-lookup"><span data-stu-id="2bfda-121">Minimum number of servers that are always marked healthy.</span></span>
<span data-ttu-id="2bfda-122">O valor padrão é 0</span><span class="sxs-lookup"><span data-stu-id="2bfda-122">Default value is 0</span></span>

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

### <span data-ttu-id="2bfda-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="2bfda-123">-Name</span></span>
<span data-ttu-id="2bfda-124">Especifica o nome do teste.</span><span class="sxs-lookup"><span data-stu-id="2bfda-124">Specifies the name of the probe.</span></span>

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

### <span data-ttu-id="2bfda-125">-Caminho</span><span class="sxs-lookup"><span data-stu-id="2bfda-125">-Path</span></span>
<span data-ttu-id="2bfda-126">Especifica o caminho relativo do teste.</span><span class="sxs-lookup"><span data-stu-id="2bfda-126">Specifies the relative path of probe.</span></span>
<span data-ttu-id="2bfda-127">Caminhos válidos começam com o caractere de barra (/).</span><span class="sxs-lookup"><span data-stu-id="2bfda-127">Valid paths start with the slash character (/).</span></span>
<span data-ttu-id="2bfda-128">O teste é enviado para \<Protocol\> :// \<host\> : \<port\> \<path\> .</span><span class="sxs-lookup"><span data-stu-id="2bfda-128">The probe is sent to \<Protocol\>://\<host\>:\<port\>\<path\>.</span></span>

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

### <span data-ttu-id="2bfda-129">-PickHostNameFromBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="2bfda-129">-PickHostNameFromBackendHttpSettings</span></span>
<span data-ttu-id="2bfda-130">Se o cabeçalho do host deve ser selecionado nas configurações http de back-end.</span><span class="sxs-lookup"><span data-stu-id="2bfda-130">Whether the host header should be picked from the backend http settings.</span></span>
<span data-ttu-id="2bfda-131">O valor padrão é falso</span><span class="sxs-lookup"><span data-stu-id="2bfda-131">Default value is false</span></span>

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

### <span data-ttu-id="2bfda-132">-Protocolo</span><span class="sxs-lookup"><span data-stu-id="2bfda-132">-Protocol</span></span>
<span data-ttu-id="2bfda-133">Especifica o protocolo usado para enviar o teste.</span><span class="sxs-lookup"><span data-stu-id="2bfda-133">Specifies the protocol used to send probe.</span></span>

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

### <span data-ttu-id="2bfda-134">-Timeout</span><span class="sxs-lookup"><span data-stu-id="2bfda-134">-Timeout</span></span>
<span data-ttu-id="2bfda-135">Especifica o tempo limite do teste em segundos.</span><span class="sxs-lookup"><span data-stu-id="2bfda-135">Specifies the probe timeout in seconds.</span></span>
<span data-ttu-id="2bfda-136">Esse cmdlet marca o teste como Failed se uma resposta válida não for recebida com esse período de tempo limite.</span><span class="sxs-lookup"><span data-stu-id="2bfda-136">This cmdlet marks the probe as failed if a valid response is not received with this timeout period.</span></span>
<span data-ttu-id="2bfda-137">Os valores válidos estão entre 1 segundo e 86400 segundos.</span><span class="sxs-lookup"><span data-stu-id="2bfda-137">Valid values are between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="2bfda-138">-UnhealthyThreshold</span><span class="sxs-lookup"><span data-stu-id="2bfda-138">-UnhealthyThreshold</span></span>
<span data-ttu-id="2bfda-139">Especifica a contagem de repetição de teste.</span><span class="sxs-lookup"><span data-stu-id="2bfda-139">Specifies the probe retry count.</span></span>
<span data-ttu-id="2bfda-140">O servidor back-end está marcado para baixo após a contagem de falhas de investigação consecutiva alcançar o limite não íntegro.</span><span class="sxs-lookup"><span data-stu-id="2bfda-140">The backend server is marked down after consecutive probe failure count reaches the unhealthy threshold.</span></span>
<span data-ttu-id="2bfda-141">Os valores válidos estão entre 1 segundo e 20 segundos.</span><span class="sxs-lookup"><span data-stu-id="2bfda-141">Valid values are between 1 second and 20 seconds.</span></span>

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

### <span data-ttu-id="2bfda-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2bfda-142">-DefaultProfile</span></span>
<span data-ttu-id="2bfda-143">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2bfda-143">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2bfda-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2bfda-144">CommonParameters</span></span>
<span data-ttu-id="2bfda-145">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2bfda-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2bfda-146">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2bfda-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2bfda-147">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2bfda-147">INPUTS</span></span>

## <span data-ttu-id="2bfda-148">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2bfda-148">OUTPUTS</span></span>

### <span data-ttu-id="2bfda-149">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayProbe</span><span class="sxs-lookup"><span data-stu-id="2bfda-149">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe</span></span>

## <span data-ttu-id="2bfda-150">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2bfda-150">NOTES</span></span>

## <span data-ttu-id="2bfda-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2bfda-151">RELATED LINKS</span></span>

[<span data-ttu-id="2bfda-152">Criar investigação personalizada do Application Gateway usando o PowerShell para Azure Resource Manager</span><span class="sxs-lookup"><span data-stu-id="2bfda-152">Create custom probe for Application Gateway using PowerShell for Azure Resource Manager</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#)

[<span data-ttu-id="2bfda-153">Add-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="2bfda-153">Add-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="2bfda-154">Get-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="2bfda-154">Get-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="2bfda-155">Remove-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="2bfda-155">Remove-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="2bfda-156">Set-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="2bfda-156">Set-AzureRmApplicationGatewayProbeConfig</span></span>]()


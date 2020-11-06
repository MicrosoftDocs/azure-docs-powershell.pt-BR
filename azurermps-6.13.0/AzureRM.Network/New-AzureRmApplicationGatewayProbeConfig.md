---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewayprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayProbeConfig.md
ms.openlocfilehash: 538020fa9ef55eedfdf7b181fca16f9499f46682
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93603159"
---
# <span data-ttu-id="cb8c1-101">New-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="cb8c1-101">New-AzureRmApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="cb8c1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cb8c1-102">SYNOPSIS</span></span>
<span data-ttu-id="cb8c1-103">Cria uma sondagem de integridade.</span><span class="sxs-lookup"><span data-stu-id="cb8c1-103">Creates a health probe.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cb8c1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cb8c1-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayProbeConfig -Name <String> -Protocol <String> [-HostName <String>] -Path <String>
 -Interval <Int32> -Timeout <Int32> -UnhealthyThreshold <Int32> [-PickHostNameFromBackendHttpSettings]
 [-MinServers <Int32>] [-Match <PSApplicationGatewayProbeHealthResponseMatch>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cb8c1-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="cb8c1-105">DESCRIPTION</span></span>
<span data-ttu-id="cb8c1-106">O cmdlet New-AzureRmApplicationGatewayProbeConfig cria uma sondagem de integridade.</span><span class="sxs-lookup"><span data-stu-id="cb8c1-106">The New-AzureRmApplicationGatewayProbeConfig cmdlet creates a health probe.</span></span>

## <span data-ttu-id="cb8c1-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cb8c1-107">EXAMPLES</span></span>

### <span data-ttu-id="cb8c1-108">Example1: criar uma sondagem de integridade</span><span class="sxs-lookup"><span data-stu-id="cb8c1-108">Example1: Create a health probe</span></span>
```
PS C:\>New-AzureRmApplicationGatewayProbeConfig -Name "Probe03" -Protocol Http -HostName "contoso.com" -Path "/path/custompath.htm" -Interval 30 -Timeout 120 -UnhealthyThreshold 8
```

<span data-ttu-id="cb8c1-109">Esse comando cria um teste de integridade chamado Probe03, com o protocolo HTTP, um intervalo de 30 segundos, o tempo limite de 120 segundos e um limiar não íntegro de 8 tentativas.</span><span class="sxs-lookup"><span data-stu-id="cb8c1-109">This command creates a health probe named Probe03, with HTTP protocol, a 30 second interval, timeout of 120 seconds, and an unhealthy threshold of 8 retries.</span></span>

## <span data-ttu-id="cb8c1-110">OS</span><span class="sxs-lookup"><span data-stu-id="cb8c1-110">PARAMETERS</span></span>

### <span data-ttu-id="cb8c1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb8c1-111">-DefaultProfile</span></span>
<span data-ttu-id="cb8c1-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="cb8c1-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cb8c1-113">-HostName</span><span class="sxs-lookup"><span data-stu-id="cb8c1-113">-HostName</span></span>
<span data-ttu-id="cb8c1-114">Especifica o nome do host para o qual esse cmdlet envia o teste.</span><span class="sxs-lookup"><span data-stu-id="cb8c1-114">Specifies the host name that this cmdlet sends the probe.</span></span>

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

### <span data-ttu-id="cb8c1-115">-Intervalo</span><span class="sxs-lookup"><span data-stu-id="cb8c1-115">-Interval</span></span>
<span data-ttu-id="cb8c1-116">Especifica o intervalo de sondagem em segundos.</span><span class="sxs-lookup"><span data-stu-id="cb8c1-116">Specifies the probe interval in seconds.</span></span>
<span data-ttu-id="cb8c1-117">Esse é o intervalo de tempo entre dois testes consecutivos.</span><span class="sxs-lookup"><span data-stu-id="cb8c1-117">This is the time interval between two consecutive probes.</span></span>
<span data-ttu-id="cb8c1-118">Esse valor é entre 1 segundo e 86400 segundos.</span><span class="sxs-lookup"><span data-stu-id="cb8c1-118">This value is between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="cb8c1-119">-Match</span><span class="sxs-lookup"><span data-stu-id="cb8c1-119">-Match</span></span>
<span data-ttu-id="cb8c1-120">Corpo que deve estar contido na resposta de integridade.</span><span class="sxs-lookup"><span data-stu-id="cb8c1-120">Body that must be contained in the health response.</span></span>
<span data-ttu-id="cb8c1-121">O valor padrão está vazio</span><span class="sxs-lookup"><span data-stu-id="cb8c1-121">Default value is empty</span></span>

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

### <span data-ttu-id="cb8c1-122">-MinServers</span><span class="sxs-lookup"><span data-stu-id="cb8c1-122">-MinServers</span></span>
<span data-ttu-id="cb8c1-123">Número mínimo de servidores que sempre estão marcados como íntegros.</span><span class="sxs-lookup"><span data-stu-id="cb8c1-123">Minimum number of servers that are always marked healthy.</span></span>
<span data-ttu-id="cb8c1-124">O valor padrão é 0</span><span class="sxs-lookup"><span data-stu-id="cb8c1-124">Default value is 0</span></span>

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

### <span data-ttu-id="cb8c1-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="cb8c1-125">-Name</span></span>
<span data-ttu-id="cb8c1-126">Especifica o nome do teste.</span><span class="sxs-lookup"><span data-stu-id="cb8c1-126">Specifies the name of the probe.</span></span>

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

### <span data-ttu-id="cb8c1-127">-Caminho</span><span class="sxs-lookup"><span data-stu-id="cb8c1-127">-Path</span></span>
<span data-ttu-id="cb8c1-128">Especifica o caminho relativo do teste.</span><span class="sxs-lookup"><span data-stu-id="cb8c1-128">Specifies the relative path of probe.</span></span>
<span data-ttu-id="cb8c1-129">Caminhos válidos começam com o caractere de barra (/).</span><span class="sxs-lookup"><span data-stu-id="cb8c1-129">Valid paths start with the slash character (/).</span></span>
<span data-ttu-id="cb8c1-130">O teste é enviado para \<Protocol\> :// \<host\> : \<port\> \<path\> .</span><span class="sxs-lookup"><span data-stu-id="cb8c1-130">The probe is sent to \<Protocol\>://\<host\>:\<port\>\<path\>.</span></span>

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

### <span data-ttu-id="cb8c1-131">-PickHostNameFromBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="cb8c1-131">-PickHostNameFromBackendHttpSettings</span></span>
<span data-ttu-id="cb8c1-132">Se o cabeçalho do host deve ser selecionado nas configurações http de back-end.</span><span class="sxs-lookup"><span data-stu-id="cb8c1-132">Whether the host header should be picked from the backend http settings.</span></span>
<span data-ttu-id="cb8c1-133">O valor padrão é falso</span><span class="sxs-lookup"><span data-stu-id="cb8c1-133">Default value is false</span></span>

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

### <span data-ttu-id="cb8c1-134">-Protocolo</span><span class="sxs-lookup"><span data-stu-id="cb8c1-134">-Protocol</span></span>
<span data-ttu-id="cb8c1-135">Especifica o protocolo usado para enviar o teste.</span><span class="sxs-lookup"><span data-stu-id="cb8c1-135">Specifies the protocol used to send probe.</span></span>

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

### <span data-ttu-id="cb8c1-136">-Timeout</span><span class="sxs-lookup"><span data-stu-id="cb8c1-136">-Timeout</span></span>
<span data-ttu-id="cb8c1-137">Especifica o tempo limite do teste em segundos.</span><span class="sxs-lookup"><span data-stu-id="cb8c1-137">Specifies the probe timeout in seconds.</span></span>
<span data-ttu-id="cb8c1-138">Esse cmdlet marca o teste como Failed se uma resposta válida não for recebida com esse período de tempo limite.</span><span class="sxs-lookup"><span data-stu-id="cb8c1-138">This cmdlet marks the probe as failed if a valid response is not received with this timeout period.</span></span>
<span data-ttu-id="cb8c1-139">Os valores válidos estão entre 1 segundo e 86400 segundos.</span><span class="sxs-lookup"><span data-stu-id="cb8c1-139">Valid values are between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="cb8c1-140">-UnhealthyThreshold</span><span class="sxs-lookup"><span data-stu-id="cb8c1-140">-UnhealthyThreshold</span></span>
<span data-ttu-id="cb8c1-141">Especifica a contagem de repetição de teste.</span><span class="sxs-lookup"><span data-stu-id="cb8c1-141">Specifies the probe retry count.</span></span>
<span data-ttu-id="cb8c1-142">O servidor back-end está marcado para baixo após a contagem de falhas de investigação consecutiva alcançar o limite não íntegro.</span><span class="sxs-lookup"><span data-stu-id="cb8c1-142">The backend server is marked down after consecutive probe failure count reaches the unhealthy threshold.</span></span>
<span data-ttu-id="cb8c1-143">Os valores válidos estão entre 1 segundo e 20 segundos.</span><span class="sxs-lookup"><span data-stu-id="cb8c1-143">Valid values are between 1 second and 20 seconds.</span></span>

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

### <span data-ttu-id="cb8c1-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb8c1-144">CommonParameters</span></span>
<span data-ttu-id="cb8c1-145">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cb8c1-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb8c1-146">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cb8c1-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb8c1-147">SENSORES</span><span class="sxs-lookup"><span data-stu-id="cb8c1-147">INPUTS</span></span>

### <span data-ttu-id="cb8c1-148">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="cb8c1-148">None</span></span>

## <span data-ttu-id="cb8c1-149">EXIBE</span><span class="sxs-lookup"><span data-stu-id="cb8c1-149">OUTPUTS</span></span>

### <span data-ttu-id="cb8c1-150">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayProbe</span><span class="sxs-lookup"><span data-stu-id="cb8c1-150">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe</span></span>

## <span data-ttu-id="cb8c1-151">INFORMA</span><span class="sxs-lookup"><span data-stu-id="cb8c1-151">NOTES</span></span>

## <span data-ttu-id="cb8c1-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cb8c1-152">RELATED LINKS</span></span>

[<span data-ttu-id="cb8c1-153">Criar investigação personalizada do Application Gateway usando o PowerShell para Azure Resource Manager</span><span class="sxs-lookup"><span data-stu-id="cb8c1-153">Create custom probe for Application Gateway using PowerShell for Azure Resource Manager</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#)

[<span data-ttu-id="cb8c1-154">Add-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="cb8c1-154">Add-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="cb8c1-155">Get-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="cb8c1-155">Get-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="cb8c1-156">Remove-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="cb8c1-156">Remove-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="cb8c1-157">Set-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="cb8c1-157">Set-AzureRmApplicationGatewayProbeConfig</span></span>]()


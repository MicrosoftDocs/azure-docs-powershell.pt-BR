---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermapplicationgatewaybackendhttpsettings
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayBackendHttpSettings.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayBackendHttpSettings.md
ms.openlocfilehash: e88614de1f61cb976937759b6962e682ee6bb0ea
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432109"
---
# <span data-ttu-id="e5dc0-101">Add-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="e5dc0-101">Add-AzureRmApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="e5dc0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e5dc0-102">SYNOPSIS</span></span>
<span data-ttu-id="e5dc0-103">Adiciona configurações HTTP back-end a um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e5dc0-103">Adds back-end HTTP settings to an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e5dc0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e5dc0-104">SYNTAX</span></span>

```
Add-AzureRmApplicationGatewayBackendHttpSettings -ApplicationGateway <PSApplicationGateway> -Name <String>
 -Port <Int32> -Protocol <String> -CookieBasedAffinity <String> [-RequestTimeout <Int32>]
 [-ConnectionDraining <PSApplicationGatewayConnectionDraining>] [-ProbeId <String>]
 [-Probe <PSApplicationGatewayProbe>]
 [-AuthenticationCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate]>]
 [-PickHostNameFromBackendAddress] [-HostName <String>] [-AffinityCookieName <String>] [-ProbeEnabled]
 [-Path <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e5dc0-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e5dc0-105">DESCRIPTION</span></span>
<span data-ttu-id="e5dc0-106">O cmdlet Add-AzureRmApplicationGatewayBackendHttpSettings adiciona configurações HTTP back-end a um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e5dc0-106">The Add-AzureRmApplicationGatewayBackendHttpSettings cmdlet adds back-end HTTP settings to an application gateway.</span></span>

<span data-ttu-id="e5dc0-107">As configurações HTTP de back-end são aplicadas a todos os servidores back-end do pool.</span><span class="sxs-lookup"><span data-stu-id="e5dc0-107">Back-end HTTP settings are applied to all back-end servers in the pool.</span></span>

## <span data-ttu-id="e5dc0-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e5dc0-108">EXAMPLES</span></span>

### <span data-ttu-id="e5dc0-109">Exemplo 1: adicionar configurações HTTP back-end a um gateway de aplicativo</span><span class="sxs-lookup"><span data-stu-id="e5dc0-109">Example 1: Add back-end HTTP settings to an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzureRmApplicationGatewayBackendHttpSettings -ApplicationGateway $AppGw -Name "Setting02" -Port 88 -Protocol "HTTP" -CookieBasedAffinity "Disabled"
```

<span data-ttu-id="e5dc0-110">O primeiro comando obtém o gateway do aplicativo chamado ApplicationGateway01 que pertence ao grupo de recursos chamado ResourceGroup01 e o armazena na variável $AppGw. O segundo comando adiciona configurações HTTP back-end ao gateway do aplicativo, definindo a porta como 88 e o protocolo para HTTP e nomeia as configurações Setting02.</span><span class="sxs-lookup"><span data-stu-id="e5dc0-110">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.The second command adds back-end HTTP settings to the application gateway, setting the port to 88 and the protocol to HTTP and names the settings Setting02.</span></span>

## <span data-ttu-id="e5dc0-111">OS</span><span class="sxs-lookup"><span data-stu-id="e5dc0-111">PARAMETERS</span></span>

### <span data-ttu-id="e5dc0-112">-AffinityCookieName</span><span class="sxs-lookup"><span data-stu-id="e5dc0-112">-AffinityCookieName</span></span>
<span data-ttu-id="e5dc0-113">Nome do cookie a ser usado para o cookie de afinidade</span><span class="sxs-lookup"><span data-stu-id="e5dc0-113">Cookie name to use for the affinity cookie</span></span>

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

### <span data-ttu-id="e5dc0-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e5dc0-114">-ApplicationGateway</span></span>
<span data-ttu-id="e5dc0-115">Especifica o nome do gateway do aplicativo para o qual esse cmdlet adiciona configurações.</span><span class="sxs-lookup"><span data-stu-id="e5dc0-115">Specifies the name of application gateway for which this cmdlet adds settings.</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e5dc0-116">-AuthenticationCertificates</span><span class="sxs-lookup"><span data-stu-id="e5dc0-116">-AuthenticationCertificates</span></span>
<span data-ttu-id="e5dc0-117">Especifica certificados de autenticação para o gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e5dc0-117">Specifies authentication certificates for the application gateway.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5dc0-118">-ConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="e5dc0-118">-ConnectionDraining</span></span>
<span data-ttu-id="e5dc0-119">Descarregamento de conexão do recurso de configurações http de back-end.</span><span class="sxs-lookup"><span data-stu-id="e5dc0-119">Connection draining of the backend http settings resource.</span></span>

```yaml
Type: PSApplicationGatewayConnectionDraining
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5dc0-120">-CookieBasedAffinity</span><span class="sxs-lookup"><span data-stu-id="e5dc0-120">-CookieBasedAffinity</span></span>
<span data-ttu-id="e5dc0-121">Especifica se a afinidade baseada em cookies deve ser habilitada ou desabilitada para o pool do servidor back-end.</span><span class="sxs-lookup"><span data-stu-id="e5dc0-121">Specifies whether cookie-based affinity should be enabled or disabled for the backend server pool.</span></span>
<span data-ttu-id="e5dc0-122">Os valores aceitáveis para esse parâmetro são: Disabled, Enabled.</span><span class="sxs-lookup"><span data-stu-id="e5dc0-122">The acceptable values for this parameter are: Disabled, Enabled.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Enabled, Disabled

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5dc0-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5dc0-123">-DefaultProfile</span></span>
<span data-ttu-id="e5dc0-124">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e5dc0-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e5dc0-125">-HostName</span><span class="sxs-lookup"><span data-stu-id="e5dc0-125">-HostName</span></span>
<span data-ttu-id="e5dc0-126">Define que o cabeçalho do host seja enviado para os servidores back-end.</span><span class="sxs-lookup"><span data-stu-id="e5dc0-126">Sets host header to be sent to the backend servers.</span></span>

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

### <span data-ttu-id="e5dc0-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="e5dc0-127">-Name</span></span>
<span data-ttu-id="e5dc0-128">Especifica o nome das configurações HTTP de back-end que esse cmdlet adiciona.</span><span class="sxs-lookup"><span data-stu-id="e5dc0-128">Specifies the name of the back-end HTTP settings which this cmdlet adds.</span></span>

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

### <span data-ttu-id="e5dc0-129">-Caminho</span><span class="sxs-lookup"><span data-stu-id="e5dc0-129">-Path</span></span>
<span data-ttu-id="e5dc0-130">Caminho que deve ser usado como um prefixo para todas as solicitações HTTP.</span><span class="sxs-lookup"><span data-stu-id="e5dc0-130">Path which should be used as a prefix for all HTTP requests.</span></span>
<span data-ttu-id="e5dc0-131">Se nenhum valor for fornecido para esse parâmetro, nenhum caminho será prefixado.</span><span class="sxs-lookup"><span data-stu-id="e5dc0-131">If no value is provided for this parameter, then no path will be prefixed.</span></span>

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

### <span data-ttu-id="e5dc0-132">-PickHostNameFromBackendAddress</span><span class="sxs-lookup"><span data-stu-id="e5dc0-132">-PickHostNameFromBackendAddress</span></span>
<span data-ttu-id="e5dc0-133">Sinalizar se o cabeçalho do host deve ser selecionado do nome do host do servidor back-end.</span><span class="sxs-lookup"><span data-stu-id="e5dc0-133">Flag if host header should be picked from the host name of the backend server.</span></span>

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

### <span data-ttu-id="e5dc0-134">-Porta</span><span class="sxs-lookup"><span data-stu-id="e5dc0-134">-Port</span></span>
<span data-ttu-id="e5dc0-135">Especifica a porta do pool de servidores back-end.</span><span class="sxs-lookup"><span data-stu-id="e5dc0-135">Specifies the port of the back-end server pool.</span></span>

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

### <span data-ttu-id="e5dc0-136">-Teste</span><span class="sxs-lookup"><span data-stu-id="e5dc0-136">-Probe</span></span>
<span data-ttu-id="e5dc0-137">Especifica um teste para associar a um servidor back-end.</span><span class="sxs-lookup"><span data-stu-id="e5dc0-137">Specifies a probe to associate with a back-end server.</span></span>

```yaml
Type: PSApplicationGatewayProbe
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5dc0-138">-ProbeEnabled</span><span class="sxs-lookup"><span data-stu-id="e5dc0-138">-ProbeEnabled</span></span>
<span data-ttu-id="e5dc0-139">Sinalizar se o teste deve ser habilitado.</span><span class="sxs-lookup"><span data-stu-id="e5dc0-139">Flag if probe should be enabled.</span></span>

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

### <span data-ttu-id="e5dc0-140">-Probeid</span><span class="sxs-lookup"><span data-stu-id="e5dc0-140">-ProbeId</span></span>
<span data-ttu-id="e5dc0-141">Especifica a ID do teste a ser associada ao servidor back-end.</span><span class="sxs-lookup"><span data-stu-id="e5dc0-141">Specifies the ID of the probe to associate with the back-end server.</span></span>

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

### <span data-ttu-id="e5dc0-142">-Protocolo</span><span class="sxs-lookup"><span data-stu-id="e5dc0-142">-Protocol</span></span>
<span data-ttu-id="e5dc0-143">Especifica o protocolo para comunicação entre os servidores de gateway e de back-end do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e5dc0-143">Specifies the protocol for communication between application gateway and back-end servers.</span></span>
<span data-ttu-id="e5dc0-144">Os valores aceitáveis para esse parâmetro são: http e HTTPS.</span><span class="sxs-lookup"><span data-stu-id="e5dc0-144">The acceptable values for this parameter are: Http and Https.</span></span>

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

### <span data-ttu-id="e5dc0-145">-RequestTimeout</span><span class="sxs-lookup"><span data-stu-id="e5dc0-145">-RequestTimeout</span></span>
<span data-ttu-id="e5dc0-146">Especifica o valor de tempo limite da solicitação.</span><span class="sxs-lookup"><span data-stu-id="e5dc0-146">Specifies the request time-out value.</span></span>

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

### <span data-ttu-id="e5dc0-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5dc0-147">CommonParameters</span></span>
<span data-ttu-id="e5dc0-148">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5dc0-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5dc0-149">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5dc0-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5dc0-150">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e5dc0-150">INPUTS</span></span>

### <span data-ttu-id="e5dc0-151">System. String</span><span class="sxs-lookup"><span data-stu-id="e5dc0-151">System.String</span></span>

## <span data-ttu-id="e5dc0-152">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e5dc0-152">OUTPUTS</span></span>

### <span data-ttu-id="e5dc0-153">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e5dc0-153">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e5dc0-154">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e5dc0-154">NOTES</span></span>

## <span data-ttu-id="e5dc0-155">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e5dc0-155">RELATED LINKS</span></span>

[<span data-ttu-id="e5dc0-156">Get-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="e5dc0-156">Get-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="e5dc0-157">New-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="e5dc0-157">New-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="e5dc0-158">Remove-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="e5dc0-158">Remove-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="e5dc0-159">Set-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="e5dc0-159">Set-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

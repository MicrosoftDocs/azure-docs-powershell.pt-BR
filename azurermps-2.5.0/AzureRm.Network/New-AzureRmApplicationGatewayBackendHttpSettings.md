---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewaybackendhttpsettings
schema: 2.0.0
ms.openlocfilehash: f4c4ccdce719b3593968f0429d5e02936d052cc4
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785906"
---
# <span data-ttu-id="13a1f-101">New-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="13a1f-101">New-AzureRmApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="13a1f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="13a1f-102">SYNOPSIS</span></span>
<span data-ttu-id="13a1f-103">Cria configurações HTTP de back-end para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="13a1f-103">Creates back-end HTTP settings for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="13a1f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="13a1f-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayBackendHttpSettings -Name <String> -Port <Int32> -Protocol <String>
 -CookieBasedAffinity <String> [-RequestTimeout <Int32>]
 [-ConnectionDraining <PSApplicationGatewayConnectionDraining>] [-ProbeId <String>]
 [-Probe <PSApplicationGatewayProbe>]
 [-AuthenticationCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate]>]
 [-PickHostNameFromBackendAddress] [-HostName <String>] [-AffinityCookieName <String>] [-ProbeEnabled]
 [-Path <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="13a1f-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="13a1f-105">DESCRIPTION</span></span>
<span data-ttu-id="13a1f-106">O cmdlet New-AzureRmApplicationGatewayBackendHttpSettings cria configurações HTTP back-end para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="13a1f-106">The New-AzureRmApplicationGatewayBackendHttpSettings cmdlet creates back-end HTTP settings for an application gateway.</span></span>
<span data-ttu-id="13a1f-107">As configurações HTTP de back-end são aplicadas a todos os servidores back-end em um pool.</span><span class="sxs-lookup"><span data-stu-id="13a1f-107">Back-end HTTP settings are applied to all back-end servers in a pool.</span></span>

## <span data-ttu-id="13a1f-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="13a1f-108">EXAMPLES</span></span>

### <span data-ttu-id="13a1f-109">Exemplo 1: criar configurações HTTP de back-end</span><span class="sxs-lookup"><span data-stu-id="13a1f-109">Example 1: Create back-end HTTP settings</span></span>
```
PS C:\>$Setting = New-AzureRmApplicationGatewayBackendHttpSettings -Name "Setting01" -Port 80 -Protocol Http -CookieBasedAffinity Disabled
```

<span data-ttu-id="13a1f-110">Este comando cria configurações HTTP de back-end chamadas Setting01 na porta 80, usando o protocolo HTTP, com afinidade baseada em cookies desabilitada.</span><span class="sxs-lookup"><span data-stu-id="13a1f-110">This command creates back-end HTTP settings named Setting01 on port 80, using the HTTP protocol, with cookie-based affinity disabled.</span></span>
<span data-ttu-id="13a1f-111">As configurações são armazenadas na variável $Setting.</span><span class="sxs-lookup"><span data-stu-id="13a1f-111">The settings are stored in the $Setting variable.</span></span>

## <span data-ttu-id="13a1f-112">OS</span><span class="sxs-lookup"><span data-stu-id="13a1f-112">PARAMETERS</span></span>

### <span data-ttu-id="13a1f-113">-AffinityCookieName</span><span class="sxs-lookup"><span data-stu-id="13a1f-113">-AffinityCookieName</span></span>
<span data-ttu-id="13a1f-114">Nome do cookie a ser usado para o cookie de afinidade</span><span class="sxs-lookup"><span data-stu-id="13a1f-114">Cookie name to use for the affinity cookie</span></span>

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

### <span data-ttu-id="13a1f-115">-AuthenticationCertificates</span><span class="sxs-lookup"><span data-stu-id="13a1f-115">-AuthenticationCertificates</span></span>
<span data-ttu-id="13a1f-116">Especifica certificados de autenticação para o gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="13a1f-116">Specifies authentication certificates for the application gateway.</span></span>

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

### <span data-ttu-id="13a1f-117">-ConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="13a1f-117">-ConnectionDraining</span></span>
<span data-ttu-id="13a1f-118">Descarregamento de conexão do recurso de configurações http de back-end.</span><span class="sxs-lookup"><span data-stu-id="13a1f-118">Connection draining of the backend http settings resource.</span></span>

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

### <span data-ttu-id="13a1f-119">-CookieBasedAffinity</span><span class="sxs-lookup"><span data-stu-id="13a1f-119">-CookieBasedAffinity</span></span>
<span data-ttu-id="13a1f-120">Especifica se a afinidade baseada em cookies deve ser habilitada ou desabilitada para o pool de servidores back-end.</span><span class="sxs-lookup"><span data-stu-id="13a1f-120">Specifies whether cookie-based affinity should be enabled or disabled for the back-end server pool.</span></span>

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

### <span data-ttu-id="13a1f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13a1f-121">-DefaultProfile</span></span>
<span data-ttu-id="13a1f-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="13a1f-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="13a1f-123">-HostName</span><span class="sxs-lookup"><span data-stu-id="13a1f-123">-HostName</span></span>
<span data-ttu-id="13a1f-124">Define que o cabeçalho do host seja enviado para os servidores back-end.</span><span class="sxs-lookup"><span data-stu-id="13a1f-124">Sets host header to be sent to the backend servers.</span></span>

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

### <span data-ttu-id="13a1f-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="13a1f-125">-Name</span></span>
<span data-ttu-id="13a1f-126">Especifica o nome das configurações HTTP de back-end que este cmdlet cria.</span><span class="sxs-lookup"><span data-stu-id="13a1f-126">Specifies the name of the back-end HTTP settings that this cmdlet creates.</span></span>

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

### <span data-ttu-id="13a1f-127">-Caminho</span><span class="sxs-lookup"><span data-stu-id="13a1f-127">-Path</span></span>
<span data-ttu-id="13a1f-128">Caminho que deve ser usado como um prefixo para todas as solicitações HTTP.</span><span class="sxs-lookup"><span data-stu-id="13a1f-128">Path which should be used as a prefix for all HTTP requests.</span></span>
<span data-ttu-id="13a1f-129">Se nenhum valor for fornecido para esse parâmetro, nenhum caminho será prefixado.</span><span class="sxs-lookup"><span data-stu-id="13a1f-129">If no value is provided for this parameter, then no path will be prefixed.</span></span>

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

### <span data-ttu-id="13a1f-130">-PickHostNameFromBackendAddress</span><span class="sxs-lookup"><span data-stu-id="13a1f-130">-PickHostNameFromBackendAddress</span></span>
<span data-ttu-id="13a1f-131">Sinalizar se o cabeçalho do host deve ser selecionado do nome do host do servidor back-end.</span><span class="sxs-lookup"><span data-stu-id="13a1f-131">Flag if host header should be picked from the host name of the backend server.</span></span>

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

### <span data-ttu-id="13a1f-132">-Porta</span><span class="sxs-lookup"><span data-stu-id="13a1f-132">-Port</span></span>
<span data-ttu-id="13a1f-133">Especifica a porta do pool de servidores back-end.</span><span class="sxs-lookup"><span data-stu-id="13a1f-133">Specifies the port of the back-end server pool.</span></span>

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

### <span data-ttu-id="13a1f-134">-Teste</span><span class="sxs-lookup"><span data-stu-id="13a1f-134">-Probe</span></span>
<span data-ttu-id="13a1f-135">Especifica um teste a ser associado ao pool do servidor back-end.</span><span class="sxs-lookup"><span data-stu-id="13a1f-135">Specifies a probe to associate with the back-end server pool.</span></span>

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

### <span data-ttu-id="13a1f-136">-ProbeEnabled</span><span class="sxs-lookup"><span data-stu-id="13a1f-136">-ProbeEnabled</span></span>
<span data-ttu-id="13a1f-137">Sinalizar se o teste deve ser habilitado.</span><span class="sxs-lookup"><span data-stu-id="13a1f-137">Flag if probe should be enabled.</span></span>

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

### <span data-ttu-id="13a1f-138">-Probeid</span><span class="sxs-lookup"><span data-stu-id="13a1f-138">-ProbeId</span></span>
<span data-ttu-id="13a1f-139">Especifica a ID do teste a ser associada ao pool de servidor back-end.</span><span class="sxs-lookup"><span data-stu-id="13a1f-139">Specifies the ID of the probe to associate with the back-end server pool.</span></span>

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

### <span data-ttu-id="13a1f-140">-Protocolo</span><span class="sxs-lookup"><span data-stu-id="13a1f-140">-Protocol</span></span>
<span data-ttu-id="13a1f-141">Especifica o protocolo a ser usado para comunicação entre o Application Gateway e os servidores back-end.</span><span class="sxs-lookup"><span data-stu-id="13a1f-141">Specifies the protocol to use for communication between the application gateway and the back-end servers.</span></span>
<span data-ttu-id="13a1f-142">Os valores aceitáveis para esse parâmetro são: http e HTTPS.</span><span class="sxs-lookup"><span data-stu-id="13a1f-142">The acceptable values for this parameter are: Http and Https.</span></span>

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

### <span data-ttu-id="13a1f-143">-RequestTimeout</span><span class="sxs-lookup"><span data-stu-id="13a1f-143">-RequestTimeout</span></span>
<span data-ttu-id="13a1f-144">Especifica um valor de tempo limite de solicitação.</span><span class="sxs-lookup"><span data-stu-id="13a1f-144">Specifies a request time-out value.</span></span>

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

### <span data-ttu-id="13a1f-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13a1f-145">CommonParameters</span></span>
<span data-ttu-id="13a1f-146">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13a1f-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13a1f-147">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="13a1f-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13a1f-148">SENSORES</span><span class="sxs-lookup"><span data-stu-id="13a1f-148">INPUTS</span></span>

### <span data-ttu-id="13a1f-149">System. String</span><span class="sxs-lookup"><span data-stu-id="13a1f-149">System.String</span></span>

## <span data-ttu-id="13a1f-150">EXIBE</span><span class="sxs-lookup"><span data-stu-id="13a1f-150">OUTPUTS</span></span>

### <span data-ttu-id="13a1f-151">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="13a1f-151">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="13a1f-152">INFORMA</span><span class="sxs-lookup"><span data-stu-id="13a1f-152">NOTES</span></span>

## <span data-ttu-id="13a1f-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="13a1f-153">RELATED LINKS</span></span>

[<span data-ttu-id="13a1f-154">Add-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="13a1f-154">Add-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="13a1f-155">Get-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="13a1f-155">Get-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="13a1f-156">Remove-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="13a1f-156">Remove-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="13a1f-157">Set-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="13a1f-157">Set-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()


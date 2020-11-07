---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaybackendhttpsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayBackendHttpSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayBackendHttpSetting.md
ms.openlocfilehash: 014309ceb54b1d16b2a55c97b03887deaf4ef281
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93771946"
---
# <span data-ttu-id="77c7a-101">New-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="77c7a-101">New-AzApplicationGatewayBackendHttpSetting</span></span>

## <span data-ttu-id="77c7a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="77c7a-102">SYNOPSIS</span></span>
<span data-ttu-id="77c7a-103">Cria uma configuração HTTP back-end para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="77c7a-103">Creates back-end HTTP setting for an application gateway.</span></span>

## <span data-ttu-id="77c7a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="77c7a-104">SYNTAX</span></span>

```
New-AzApplicationGatewayBackendHttpSetting -Name <String> -Port <Int32> -Protocol <String>
 -CookieBasedAffinity <String> [-RequestTimeout <Int32>]
 [-ConnectionDraining <PSApplicationGatewayConnectionDraining>] [-ProbeId <String>]
 [-Probe <PSApplicationGatewayProbe>]
 [-AuthenticationCertificates <PSApplicationGatewayAuthenticationCertificate[]>]
 [-TrustedRootCertificate <PSApplicationGatewayTrustedRootCertificate[]>] [-PickHostNameFromBackendAddress]
 [-HostName <String>] [-AffinityCookieName <String>] [-Path <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="77c7a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="77c7a-105">DESCRIPTION</span></span>
<span data-ttu-id="77c7a-106">O cmdlet New-AzApplicationGatewayBackendHttpSetting cria configurações HTTP back-end para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="77c7a-106">The New-AzApplicationGatewayBackendHttpSetting cmdlet creates back-end HTTP settings for an application gateway.</span></span>
<span data-ttu-id="77c7a-107">As configurações HTTP de back-end são aplicadas a todos os servidores back-end em um pool.</span><span class="sxs-lookup"><span data-stu-id="77c7a-107">Back-end HTTP settings are applied to all back-end servers in a pool.</span></span>

## <span data-ttu-id="77c7a-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="77c7a-108">EXAMPLES</span></span>

### <span data-ttu-id="77c7a-109">Exemplo 1: criar configurações HTTP de back-end</span><span class="sxs-lookup"><span data-stu-id="77c7a-109">Example 1: Create back-end HTTP settings</span></span>
```
PS C:\>$Setting = New-AzApplicationGatewayBackendHttpSetting -Name "Setting01" -Port 80 -Protocol Http -CookieBasedAffinity Disabled
```

<span data-ttu-id="77c7a-110">Este comando cria configurações HTTP de back-end chamadas Setting01 na porta 80, usando o protocolo HTTP, com afinidade baseada em cookies desabilitada.</span><span class="sxs-lookup"><span data-stu-id="77c7a-110">This command creates back-end HTTP settings named Setting01 on port 80, using the HTTP protocol, with cookie-based affinity disabled.</span></span>
<span data-ttu-id="77c7a-111">As configurações são armazenadas na variável $Setting.</span><span class="sxs-lookup"><span data-stu-id="77c7a-111">The settings are stored in the $Setting variable.</span></span>

## <span data-ttu-id="77c7a-112">OS</span><span class="sxs-lookup"><span data-stu-id="77c7a-112">PARAMETERS</span></span>

### <span data-ttu-id="77c7a-113">-AffinityCookieName</span><span class="sxs-lookup"><span data-stu-id="77c7a-113">-AffinityCookieName</span></span>
<span data-ttu-id="77c7a-114">Nome do cookie a ser usado para o cookie de afinidade</span><span class="sxs-lookup"><span data-stu-id="77c7a-114">Cookie name to use for the affinity cookie</span></span>

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

### <span data-ttu-id="77c7a-115">-AuthenticationCertificates</span><span class="sxs-lookup"><span data-stu-id="77c7a-115">-AuthenticationCertificates</span></span>
<span data-ttu-id="77c7a-116">Especifica certificados de autenticação para o gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="77c7a-116">Specifies authentication certificates for the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77c7a-117">-ConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="77c7a-117">-ConnectionDraining</span></span>
<span data-ttu-id="77c7a-118">Descarregamento de conexão do recurso de configurações http de back-end.</span><span class="sxs-lookup"><span data-stu-id="77c7a-118">Connection draining of the backend http settings resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayConnectionDraining
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77c7a-119">-CookieBasedAffinity</span><span class="sxs-lookup"><span data-stu-id="77c7a-119">-CookieBasedAffinity</span></span>
<span data-ttu-id="77c7a-120">Especifica se a afinidade baseada em cookies deve ser habilitada ou desabilitada para o pool de servidores back-end.</span><span class="sxs-lookup"><span data-stu-id="77c7a-120">Specifies whether cookie-based affinity should be enabled or disabled for the back-end server pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77c7a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77c7a-121">-DefaultProfile</span></span>
<span data-ttu-id="77c7a-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="77c7a-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="77c7a-123">-HostName</span><span class="sxs-lookup"><span data-stu-id="77c7a-123">-HostName</span></span>
<span data-ttu-id="77c7a-124">Define que o cabeçalho do host seja enviado para os servidores back-end.</span><span class="sxs-lookup"><span data-stu-id="77c7a-124">Sets host header to be sent to the backend servers.</span></span>

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

### <span data-ttu-id="77c7a-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="77c7a-125">-Name</span></span>
<span data-ttu-id="77c7a-126">Especifica o nome das configurações HTTP de back-end que este cmdlet cria.</span><span class="sxs-lookup"><span data-stu-id="77c7a-126">Specifies the name of the back-end HTTP settings that this cmdlet creates.</span></span>

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

### <span data-ttu-id="77c7a-127">-Caminho</span><span class="sxs-lookup"><span data-stu-id="77c7a-127">-Path</span></span>
<span data-ttu-id="77c7a-128">Caminho que deve ser usado como um prefixo para todas as solicitações HTTP.</span><span class="sxs-lookup"><span data-stu-id="77c7a-128">Path which should be used as a prefix for all HTTP requests.</span></span>
<span data-ttu-id="77c7a-129">Se nenhum valor for fornecido para esse parâmetro, nenhum caminho será prefixado.</span><span class="sxs-lookup"><span data-stu-id="77c7a-129">If no value is provided for this parameter, then no path will be prefixed.</span></span>

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

### <span data-ttu-id="77c7a-130">-PickHostNameFromBackendAddress</span><span class="sxs-lookup"><span data-stu-id="77c7a-130">-PickHostNameFromBackendAddress</span></span>
<span data-ttu-id="77c7a-131">Sinalizar se o cabeçalho do host deve ser selecionado do nome do host do servidor back-end.</span><span class="sxs-lookup"><span data-stu-id="77c7a-131">Flag if host header should be picked from the host name of the backend server.</span></span>

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

### <span data-ttu-id="77c7a-132">-Porta</span><span class="sxs-lookup"><span data-stu-id="77c7a-132">-Port</span></span>
<span data-ttu-id="77c7a-133">Especifica a porta do pool de servidores back-end.</span><span class="sxs-lookup"><span data-stu-id="77c7a-133">Specifies the port of the back-end server pool.</span></span>

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

### <span data-ttu-id="77c7a-134">-Teste</span><span class="sxs-lookup"><span data-stu-id="77c7a-134">-Probe</span></span>
<span data-ttu-id="77c7a-135">Especifica um teste a ser associado ao pool do servidor back-end.</span><span class="sxs-lookup"><span data-stu-id="77c7a-135">Specifies a probe to associate with the back-end server pool.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77c7a-136">-Probeid</span><span class="sxs-lookup"><span data-stu-id="77c7a-136">-ProbeId</span></span>
<span data-ttu-id="77c7a-137">Especifica a ID do teste a ser associada ao pool de servidor back-end.</span><span class="sxs-lookup"><span data-stu-id="77c7a-137">Specifies the ID of the probe to associate with the back-end server pool.</span></span>

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

### <span data-ttu-id="77c7a-138">-Protocolo</span><span class="sxs-lookup"><span data-stu-id="77c7a-138">-Protocol</span></span>
<span data-ttu-id="77c7a-139">Especifica o protocolo a ser usado para comunicação entre o Application Gateway e os servidores back-end.</span><span class="sxs-lookup"><span data-stu-id="77c7a-139">Specifies the protocol to use for communication between the application gateway and the back-end servers.</span></span>
<span data-ttu-id="77c7a-140">Os valores aceitáveis para esse parâmetro são: http e HTTPS.</span><span class="sxs-lookup"><span data-stu-id="77c7a-140">The acceptable values for this parameter are: Http and Https.</span></span>

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

### <span data-ttu-id="77c7a-141">-RequestTimeout</span><span class="sxs-lookup"><span data-stu-id="77c7a-141">-RequestTimeout</span></span>
<span data-ttu-id="77c7a-142">Especifica um valor de tempo limite de solicitação.</span><span class="sxs-lookup"><span data-stu-id="77c7a-142">Specifies a request time-out value.</span></span>

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

### <span data-ttu-id="77c7a-143">-TrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="77c7a-143">-TrustedRootCertificate</span></span>
<span data-ttu-id="77c7a-144">Certificados raiz confiáveis do Application Gateway</span><span class="sxs-lookup"><span data-stu-id="77c7a-144">Application gateway Trusted Root Certificates</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77c7a-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77c7a-145">CommonParameters</span></span>
<span data-ttu-id="77c7a-146">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77c7a-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77c7a-147">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="77c7a-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77c7a-148">SENSORES</span><span class="sxs-lookup"><span data-stu-id="77c7a-148">INPUTS</span></span>

### <span data-ttu-id="77c7a-149">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="77c7a-149">None</span></span>

## <span data-ttu-id="77c7a-150">EXIBE</span><span class="sxs-lookup"><span data-stu-id="77c7a-150">OUTPUTS</span></span>

### <span data-ttu-id="77c7a-151">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="77c7a-151">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="77c7a-152">INFORMA</span><span class="sxs-lookup"><span data-stu-id="77c7a-152">NOTES</span></span>

## <span data-ttu-id="77c7a-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="77c7a-153">RELATED LINKS</span></span>

[<span data-ttu-id="77c7a-154">Add-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="77c7a-154">Add-AzApplicationGatewayBackendHttpSetting</span></span>](./Add-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="77c7a-155">Get-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="77c7a-155">Get-AzApplicationGatewayBackendHttpSetting</span></span>](./Get-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="77c7a-156">Remove-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="77c7a-156">Remove-AzApplicationGatewayBackendHttpSetting</span></span>](./Remove-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="77c7a-157">Set-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="77c7a-157">Set-AzApplicationGatewayBackendHttpSetting</span></span>](./Set-AzApplicationGatewayBackendHttpSetting.md)


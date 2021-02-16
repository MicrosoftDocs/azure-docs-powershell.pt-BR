---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaybackendhttpsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayBackendHttpSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayBackendHttpSetting.md
ms.openlocfilehash: 35742a6dc65bd84359d08f4e30533a0a49488053
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118268"
---
# <span data-ttu-id="977f7-101">Set-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="977f7-101">Set-AzApplicationGatewayBackendHttpSetting</span></span>

## <span data-ttu-id="977f7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="977f7-102">SYNOPSIS</span></span>
<span data-ttu-id="977f7-103">Atualiza as configurações HTTP de back-end para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="977f7-103">Updates back-end HTTP settings for an application gateway.</span></span>

## <span data-ttu-id="977f7-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="977f7-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayBackendHttpSetting -ApplicationGateway <PSApplicationGateway> -Name <String>
 -Port <Int32> -Protocol <String> -CookieBasedAffinity <String> [-RequestTimeout <Int32>]
 [-ConnectionDraining <PSApplicationGatewayConnectionDraining>] [-ProbeId <String>]
 [-Probe <PSApplicationGatewayProbe>]
 [-AuthenticationCertificates <PSApplicationGatewayAuthenticationCertificate[]>]
 [-TrustedRootCertificate <PSApplicationGatewayTrustedRootCertificate[]>] [-PickHostNameFromBackendAddress]
 [-HostName <String>] [-AffinityCookieName <String>] [-Path <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="977f7-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="977f7-105">DESCRIPTION</span></span>
<span data-ttu-id="977f7-106">O Set-AzApplicationGatewayBackendHttpSetting cmdlet atualiza as configurações http de protocolo HTTP de back-end para um gateway de aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="977f7-106">The Set-AzApplicationGatewayBackendHttpSetting cmdlet updates the back-end Hypertext Transfer Protocol (HTTP) settings for an Azure application gateway.</span></span>
<span data-ttu-id="977f7-107">As configurações http de back-end são aplicadas a todos os servidores back-end em um pool.</span><span class="sxs-lookup"><span data-stu-id="977f7-107">Back-end HTTP settings are applied to all back-end servers in a pool.</span></span>

## <span data-ttu-id="977f7-108">Exemplos</span><span class="sxs-lookup"><span data-stu-id="977f7-108">EXAMPLES</span></span>

### <span data-ttu-id="977f7-109">Exemplo 1: Atualizar as configurações http de back-end para um gateway de aplicativo</span><span class="sxs-lookup"><span data-stu-id="977f7-109">Example 1: Update the back-end HTTP settings for an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayBackendHttpSetting -ApplicationGateway $AppGw -Name "Setting02" -Port 88 -Protocol "Http" -CookieBasedAffinity "Disabled"
```

<span data-ttu-id="977f7-110">O primeiro comando obtém o gateway de aplicativo chamado ApplicationGateway01 que pertence ao grupo de recursos chamado ResourceGroup01 e o armazena na variável $AppGw.</span><span class="sxs-lookup"><span data-stu-id="977f7-110">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="977f7-111">O segundo comando atualiza as configurações HTTP do gateway de aplicativo na variável $AppGw para usar a porta 88, o protocolo HTTP e habilita affinity baseada em cookies.</span><span class="sxs-lookup"><span data-stu-id="977f7-111">The second command updates the HTTP settings of the application gateway in the $AppGw variable to use port 88, the HTTP protocol and enables cookie-based affinity.</span></span>

## <span data-ttu-id="977f7-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="977f7-112">PARAMETERS</span></span>

### <span data-ttu-id="977f7-113">-AffinityCookieName</span><span class="sxs-lookup"><span data-stu-id="977f7-113">-AffinityCookieName</span></span>
<span data-ttu-id="977f7-114">Nome de cookie a ser usado para o cookie de affinity</span><span class="sxs-lookup"><span data-stu-id="977f7-114">Cookie name to use for the affinity cookie</span></span>

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

### <span data-ttu-id="977f7-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="977f7-115">-ApplicationGateway</span></span>
<span data-ttu-id="977f7-116">Especifica um objeto de gateway de aplicativo com o qual este cmdlet associa as configurações http de back-end.</span><span class="sxs-lookup"><span data-stu-id="977f7-116">Specifies an application gateway object with which this cmdlet associates back-end HTTP settings.</span></span>

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

### <span data-ttu-id="977f7-117">-AuthenticationCertificates</span><span class="sxs-lookup"><span data-stu-id="977f7-117">-AuthenticationCertificates</span></span>
<span data-ttu-id="977f7-118">Especifica certificados de autenticação para o gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="977f7-118">Specifies authentication certificates for the application gateway.</span></span>

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

### <span data-ttu-id="977f7-119">-ConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="977f7-119">-ConnectionDraining</span></span>
<span data-ttu-id="977f7-120">O esgotamento de conexão do recurso de configurações http back-end.</span><span class="sxs-lookup"><span data-stu-id="977f7-120">Connection draining of the backend http settings resource.</span></span>

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

### <span data-ttu-id="977f7-121">-CookieBasedAffinity</span><span class="sxs-lookup"><span data-stu-id="977f7-121">-CookieBasedAffinity</span></span>
<span data-ttu-id="977f7-122">Especifica se affinity baseada em cookies deve ser habilitada ou desabilitada para o pool de servidor de back-end.</span><span class="sxs-lookup"><span data-stu-id="977f7-122">Specifies whether cookie-based affinity should be enabled or disabled for the backend server pool.</span></span>
<span data-ttu-id="977f7-123">Os valores aceitáveis para este parâmetro são: Desabilitados ou Habilitados.</span><span class="sxs-lookup"><span data-stu-id="977f7-123">The acceptable values for this parameter are: Disabled or Enabled.</span></span>

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

### <span data-ttu-id="977f7-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="977f7-124">-DefaultProfile</span></span>
<span data-ttu-id="977f7-125">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="977f7-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="977f7-126">-Nomedo Host</span><span class="sxs-lookup"><span data-stu-id="977f7-126">-HostName</span></span>
<span data-ttu-id="977f7-127">Define o header do host a ser enviado para os servidores back-end.</span><span class="sxs-lookup"><span data-stu-id="977f7-127">Sets host header to be sent to the backend servers.</span></span>

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

### <span data-ttu-id="977f7-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="977f7-128">-Name</span></span>
<span data-ttu-id="977f7-129">Especifica o nome do objeto de configurações HTTP de back-end.</span><span class="sxs-lookup"><span data-stu-id="977f7-129">Specifies the name of the back-end HTTP settings object.</span></span>

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

### <span data-ttu-id="977f7-130">-Caminho</span><span class="sxs-lookup"><span data-stu-id="977f7-130">-Path</span></span>
<span data-ttu-id="977f7-131">Caminho que deve ser usado como prefixo para todas as solicitações HTTP.</span><span class="sxs-lookup"><span data-stu-id="977f7-131">Path which should be used as a prefix for all HTTP requests.</span></span>
<span data-ttu-id="977f7-132">Se nenhum valor for fornecido para esse parâmetro, nenhum caminho será prefixado.</span><span class="sxs-lookup"><span data-stu-id="977f7-132">If no value is provided for this parameter, then no path will be prefixed.</span></span>

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

### <span data-ttu-id="977f7-133">-PickHostNameFromBackendAddress</span><span class="sxs-lookup"><span data-stu-id="977f7-133">-PickHostNameFromBackendAddress</span></span>
<span data-ttu-id="977f7-134">Sinalizar se o header do host deve ser escolhido no nome do host do servidor back-end.</span><span class="sxs-lookup"><span data-stu-id="977f7-134">Flag if host header should be picked from the host name of the backend server.</span></span>

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

### <span data-ttu-id="977f7-135">-Porta</span><span class="sxs-lookup"><span data-stu-id="977f7-135">-Port</span></span>
<span data-ttu-id="977f7-136">Especifica a porta a ser usada para cada servidor no pool de servidores back-end.</span><span class="sxs-lookup"><span data-stu-id="977f7-136">Specifies the port to use for each server in the back-end server pool.</span></span>

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

### <span data-ttu-id="977f7-137">-Desmão</span><span class="sxs-lookup"><span data-stu-id="977f7-137">-Probe</span></span>
<span data-ttu-id="977f7-138">Especifica um problema para associar às configurações HTTP de back-end.</span><span class="sxs-lookup"><span data-stu-id="977f7-138">Specifies a probe to associate with the back-end HTTP settings.</span></span>

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

### <span data-ttu-id="977f7-139">-ElaId</span><span class="sxs-lookup"><span data-stu-id="977f7-139">-ProbeId</span></span>
<span data-ttu-id="977f7-140">Especifica a ID do teste para associar às configurações HTTP de back-end.</span><span class="sxs-lookup"><span data-stu-id="977f7-140">Specifies the ID of the probe to associate with the back-end HTTP settings.</span></span>

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

### <span data-ttu-id="977f7-141">-Protocolo</span><span class="sxs-lookup"><span data-stu-id="977f7-141">-Protocol</span></span>
<span data-ttu-id="977f7-142">Especifica o protocolo a ser usado para comunicação entre o gateway do aplicativo e os servidores back-end.</span><span class="sxs-lookup"><span data-stu-id="977f7-142">Specifies the protocol to use for communication between the application gateway and back-end servers.</span></span>
<span data-ttu-id="977f7-143">Os valores aceitáveis para este parâmetro são: Http e Https.</span><span class="sxs-lookup"><span data-stu-id="977f7-143">The acceptable values for this parameter are: Http and Https.</span></span>
<span data-ttu-id="977f7-144">Este parâmetro é sensível a minúsculas.</span><span class="sxs-lookup"><span data-stu-id="977f7-144">This parameter is case-sensitive.</span></span>

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

### <span data-ttu-id="977f7-145">-RequestTimeout</span><span class="sxs-lookup"><span data-stu-id="977f7-145">-RequestTimeout</span></span>
<span data-ttu-id="977f7-146">Especifica um valor de tempo de tempo de solicitação.</span><span class="sxs-lookup"><span data-stu-id="977f7-146">Specifies a request time-out value.</span></span>

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

### <span data-ttu-id="977f7-147">-TrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="977f7-147">-TrustedRootCertificate</span></span>
<span data-ttu-id="977f7-148">Certificados Raiz Confiáveis do Gateway de Aplicativos</span><span class="sxs-lookup"><span data-stu-id="977f7-148">Application gateway Trusted Root Certificates</span></span>

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

### <span data-ttu-id="977f7-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="977f7-149">CommonParameters</span></span>
<span data-ttu-id="977f7-150">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="977f7-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="977f7-151">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="977f7-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="977f7-152">Entradas</span><span class="sxs-lookup"><span data-stu-id="977f7-152">INPUTS</span></span>

### <span data-ttu-id="977f7-153">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="977f7-153">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="977f7-154">Saídas</span><span class="sxs-lookup"><span data-stu-id="977f7-154">OUTPUTS</span></span>

### <span data-ttu-id="977f7-155">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="977f7-155">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="977f7-156">Notas</span><span class="sxs-lookup"><span data-stu-id="977f7-156">NOTES</span></span>

## <span data-ttu-id="977f7-157">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="977f7-157">RELATED LINKS</span></span>

[<span data-ttu-id="977f7-158">Add-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="977f7-158">Add-AzApplicationGatewayBackendHttpSetting</span></span>](./Add-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="977f7-159">Get-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="977f7-159">Get-AzApplicationGatewayBackendHttpSetting</span></span>](./Get-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="977f7-160">New-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="977f7-160">New-AzApplicationGatewayBackendHttpSetting</span></span>](./New-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="977f7-161">Remove-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="977f7-161">Remove-AzApplicationGatewayBackendHttpSetting</span></span>](./Remove-AzApplicationGatewayBackendHttpSetting.md)


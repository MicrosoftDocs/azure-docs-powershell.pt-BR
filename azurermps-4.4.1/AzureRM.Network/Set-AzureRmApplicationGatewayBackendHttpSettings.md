---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayBackendHttpSettings.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayBackendHttpSettings.md
ms.openlocfilehash: 87d875881ce6086f033353dd4b37ba8a8098a96c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93611085"
---
# <span data-ttu-id="fd4d5-101">Set-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="fd4d5-101">Set-AzureRmApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="fd4d5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fd4d5-102">SYNOPSIS</span></span>
<span data-ttu-id="fd4d5-103">Atualiza as configurações de HTTP back-end para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="fd4d5-103">Updates back-end HTTP settings for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fd4d5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fd4d5-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewayBackendHttpSettings -ApplicationGateway <PSApplicationGateway> -Name <String>
 -Port <Int32> -Protocol <String> -CookieBasedAffinity <String> [-RequestTimeout <Int32>]
 [-ConnectionDraining <PSApplicationGatewayConnectionDraining>] [-ProbeId <String>]
 [-Probe <PSApplicationGatewayProbe>]
 [-AuthenticationCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate]>]
 [-PickHostNameFromBackendAddress] [-HostName <String>] [-AffinityCookieName <String>] [-ProbeEnabled]
 [-Path <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fd4d5-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fd4d5-105">DESCRIPTION</span></span>
<span data-ttu-id="fd4d5-106">O cmdlet Set-AzureRmApplicationGatewayBackendHttpSettings atualiza as configurações de protocolo de transferência de hipertexto (HTTP) back-end para um gateway do aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="fd4d5-106">The Set-AzureRmApplicationGatewayBackendHttpSettings cmdlet updates the back-end Hypertext Transfer Protocol (HTTP) settings for an Azure application gateway.</span></span>
<span data-ttu-id="fd4d5-107">As configurações HTTP de back-end são aplicadas a todos os servidores back-end em um pool.</span><span class="sxs-lookup"><span data-stu-id="fd4d5-107">Back-end HTTP settings are applied to all back-end servers in a pool.</span></span>

## <span data-ttu-id="fd4d5-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fd4d5-108">EXAMPLES</span></span>

### <span data-ttu-id="fd4d5-109">Exemplo 1: atualizar as configurações HTTP de back-end para um Application Gateway</span><span class="sxs-lookup"><span data-stu-id="fd4d5-109">Example 1: Update the back-end HTTP settings for an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewayBackendHttpSettings -ApplicationGateway $AppGw -Name "Setting02" -Port 88 -Protocol "Http" -CookieBasedAffinity "Disabled"
```

<span data-ttu-id="fd4d5-110">O primeiro comando obtém o gateway do aplicativo chamado ApplicationGateway01 que pertence ao grupo de recursos chamado ResourceGroup01 e o armazena na variável $AppGw.</span><span class="sxs-lookup"><span data-stu-id="fd4d5-110">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="fd4d5-111">O segundo comando atualiza as configurações de HTTP do gateway do aplicativo na variável $AppGw para usar a porta 88, o protocolo HTTP e habilita a afinidade baseada em cookies.</span><span class="sxs-lookup"><span data-stu-id="fd4d5-111">The second command updates the HTTP settings of the application gateway in the $AppGw variable to use port 88, the HTTP protocol and enables cookie-based affinity.</span></span>

## <span data-ttu-id="fd4d5-112">OS</span><span class="sxs-lookup"><span data-stu-id="fd4d5-112">PARAMETERS</span></span>

### <span data-ttu-id="fd4d5-113">-AffinityCookieName</span><span class="sxs-lookup"><span data-stu-id="fd4d5-113">-AffinityCookieName</span></span>
<span data-ttu-id="fd4d5-114">Nome do cookie a ser usado para o cookie de afinidade</span><span class="sxs-lookup"><span data-stu-id="fd4d5-114">Cookie name to use for the affinity cookie</span></span>

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

### <span data-ttu-id="fd4d5-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fd4d5-115">-ApplicationGateway</span></span>
<span data-ttu-id="fd4d5-116">Especifica um objeto do aplicativo gateway com o qual esse cmdlet associa as configurações de HTTP back-end.</span><span class="sxs-lookup"><span data-stu-id="fd4d5-116">Specifies an application gateway object with which this cmdlet associates back-end HTTP settings.</span></span>

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

### <span data-ttu-id="fd4d5-117">-AuthenticationCertificates</span><span class="sxs-lookup"><span data-stu-id="fd4d5-117">-AuthenticationCertificates</span></span>
<span data-ttu-id="fd4d5-118">Especifica certificados de autenticação para o gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="fd4d5-118">Specifies authentication certificates for the application gateway.</span></span>

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

### <span data-ttu-id="fd4d5-119">-ConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="fd4d5-119">-ConnectionDraining</span></span>
<span data-ttu-id="fd4d5-120">Descarregamento de conexão do recurso de configurações http de back-end.</span><span class="sxs-lookup"><span data-stu-id="fd4d5-120">Connection draining of the backend http settings resource.</span></span>

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

### <span data-ttu-id="fd4d5-121">-CookieBasedAffinity</span><span class="sxs-lookup"><span data-stu-id="fd4d5-121">-CookieBasedAffinity</span></span>
<span data-ttu-id="fd4d5-122">Especifica se a afinidade baseada em cookies deve ser habilitada ou desabilitada para o pool do servidor back-end.</span><span class="sxs-lookup"><span data-stu-id="fd4d5-122">Specifies whether cookie-based affinity should be enabled or disabled for the backend server pool.</span></span>
<span data-ttu-id="fd4d5-123">Os valores aceitáveis para esse parâmetro são: Disabled ou Enabled.</span><span class="sxs-lookup"><span data-stu-id="fd4d5-123">The acceptable values for this parameter are: Disabled or Enabled.</span></span>

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

### <span data-ttu-id="fd4d5-124">-HostName</span><span class="sxs-lookup"><span data-stu-id="fd4d5-124">-HostName</span></span>
<span data-ttu-id="fd4d5-125">Define que o cabeçalho do host seja enviado para os servidores back-end.</span><span class="sxs-lookup"><span data-stu-id="fd4d5-125">Sets host header to be sent to the backend servers.</span></span>

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

### <span data-ttu-id="fd4d5-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="fd4d5-126">-Name</span></span>
<span data-ttu-id="fd4d5-127">Especifica o nome do objeto de configurações HTTP back-end.</span><span class="sxs-lookup"><span data-stu-id="fd4d5-127">Specifies the name of the back-end HTTP settings object.</span></span>

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

### <span data-ttu-id="fd4d5-128">-Caminho</span><span class="sxs-lookup"><span data-stu-id="fd4d5-128">-Path</span></span>
<span data-ttu-id="fd4d5-129">Caminho que deve ser usado como um prefixo para todas as solicitações HTTP.</span><span class="sxs-lookup"><span data-stu-id="fd4d5-129">Path which should be used as a prefix for all HTTP requests.</span></span>
<span data-ttu-id="fd4d5-130">Se nenhum valor for fornecido para esse parâmetro, nenhum caminho será prefixado.</span><span class="sxs-lookup"><span data-stu-id="fd4d5-130">If no value is provided for this parameter, then no path will be prefixed.</span></span>

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

### <span data-ttu-id="fd4d5-131">-PickHostNameFromBackendAddress</span><span class="sxs-lookup"><span data-stu-id="fd4d5-131">-PickHostNameFromBackendAddress</span></span>
<span data-ttu-id="fd4d5-132">Sinalizar se o cabeçalho do host deve ser selecionado do nome do host do servidor back-end.</span><span class="sxs-lookup"><span data-stu-id="fd4d5-132">Flag if host header should be picked from the host name of the backend server.</span></span>

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

### <span data-ttu-id="fd4d5-133">-Porta</span><span class="sxs-lookup"><span data-stu-id="fd4d5-133">-Port</span></span>
<span data-ttu-id="fd4d5-134">Especifica a porta a ser usada para cada servidor no pool de servidores back-end.</span><span class="sxs-lookup"><span data-stu-id="fd4d5-134">Specifies the port to use for each server in the back-end server pool.</span></span>

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

### <span data-ttu-id="fd4d5-135">-Teste</span><span class="sxs-lookup"><span data-stu-id="fd4d5-135">-Probe</span></span>
<span data-ttu-id="fd4d5-136">Especifica um teste para associar às configurações HTTP back-end.</span><span class="sxs-lookup"><span data-stu-id="fd4d5-136">Specifies a probe to associate with the back-end HTTP settings.</span></span>

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

### <span data-ttu-id="fd4d5-137">-ProbeEnabled</span><span class="sxs-lookup"><span data-stu-id="fd4d5-137">-ProbeEnabled</span></span>
<span data-ttu-id="fd4d5-138">Sinalizar se o teste deve ser habilitado.</span><span class="sxs-lookup"><span data-stu-id="fd4d5-138">Flag if probe should be enabled.</span></span>

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

### <span data-ttu-id="fd4d5-139">-Probeid</span><span class="sxs-lookup"><span data-stu-id="fd4d5-139">-ProbeId</span></span>
<span data-ttu-id="fd4d5-140">Especifica a ID do teste a ser associada às configurações HTTP back-end.</span><span class="sxs-lookup"><span data-stu-id="fd4d5-140">Specifies the ID of the probe to associate with the back-end HTTP settings.</span></span>

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

### <span data-ttu-id="fd4d5-141">-Protocolo</span><span class="sxs-lookup"><span data-stu-id="fd4d5-141">-Protocol</span></span>
<span data-ttu-id="fd4d5-142">Especifica o protocolo a ser usado para comunicação entre os servidores de gateway e de back-end do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="fd4d5-142">Specifies the protocol to use for communication between the application gateway and back-end servers.</span></span>
<span data-ttu-id="fd4d5-143">Os valores aceitáveis para esse parâmetro são: http e HTTPS.</span><span class="sxs-lookup"><span data-stu-id="fd4d5-143">The acceptable values for this parameter are: Http and Https.</span></span>
<span data-ttu-id="fd4d5-144">Esse parâmetro diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="fd4d5-144">This parameter is case-sensitive.</span></span>

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

### <span data-ttu-id="fd4d5-145">-RequestTimeout</span><span class="sxs-lookup"><span data-stu-id="fd4d5-145">-RequestTimeout</span></span>
<span data-ttu-id="fd4d5-146">Especifica um valor de tempo limite de solicitação.</span><span class="sxs-lookup"><span data-stu-id="fd4d5-146">Specifies a request time-out value.</span></span>

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

### <span data-ttu-id="fd4d5-147">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd4d5-147">-DefaultProfile</span></span>
<span data-ttu-id="fd4d5-148">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fd4d5-148">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fd4d5-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd4d5-149">CommonParameters</span></span>
<span data-ttu-id="fd4d5-150">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd4d5-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd4d5-151">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd4d5-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd4d5-152">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fd4d5-152">INPUTS</span></span>

### <span data-ttu-id="fd4d5-153">System. String</span><span class="sxs-lookup"><span data-stu-id="fd4d5-153">System.String</span></span>

## <span data-ttu-id="fd4d5-154">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fd4d5-154">OUTPUTS</span></span>

### <span data-ttu-id="fd4d5-155">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fd4d5-155">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="fd4d5-156">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fd4d5-156">NOTES</span></span>

## <span data-ttu-id="fd4d5-157">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fd4d5-157">RELATED LINKS</span></span>

[<span data-ttu-id="fd4d5-158">Add-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="fd4d5-158">Add-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="fd4d5-159">Get-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="fd4d5-159">Get-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="fd4d5-160">New-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="fd4d5-160">New-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="fd4d5-161">Remove-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="fd4d5-161">Remove-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()


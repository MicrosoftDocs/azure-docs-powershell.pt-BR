---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: AF8CC409-2EA7-4EC1-86C9-E7A773DE9201
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayHttpListener.md
ms.openlocfilehash: 9505194ef562c7faf292d5bbf2fe3de20ac7995f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94125623"
---
# <span data-ttu-id="4038a-101">New-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="4038a-101">New-AzApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="4038a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4038a-102">SYNOPSIS</span></span>
<span data-ttu-id="4038a-103">Cria um ouvinte HTTP para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="4038a-103">Creates an HTTP listener for an application gateway.</span></span>

## <span data-ttu-id="4038a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4038a-104">SYNTAX</span></span>

### <span data-ttu-id="4038a-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="4038a-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayHttpListener -Name <String> [-FrontendIPConfigurationId <String>]
 [-FrontendPortId <String>] [-SslCertificateId <String>] [-FirewallPolicyId <String>] [-HostName <String>]
 [-HostNames <String[]>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4038a-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="4038a-106">SetByResource</span></span>
```
New-AzApplicationGatewayHttpListener -Name <String>
 [-FrontendIPConfiguration <PSApplicationGatewayFrontendIPConfiguration>]
 [-FrontendPort <PSApplicationGatewayFrontendPort>]
 [-FirewallPolicy <PSApplicationGatewayWebApplicationFirewallPolicy>]
 [-SslCertificate <PSApplicationGatewaySslCertificate>] [-HostName <String>] [-HostNames <String[]>]
 [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4038a-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4038a-107">DESCRIPTION</span></span>
<span data-ttu-id="4038a-108">O cmdlet **New-AzApplicationGatewayHttpListener** cria um ouvinte HTTP para um gateway do aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="4038a-108">The **New-AzApplicationGatewayHttpListener** cmdlet creates an HTTP listener for an Azure application gateway.</span></span>

## <span data-ttu-id="4038a-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4038a-109">EXAMPLES</span></span>

### <span data-ttu-id="4038a-110">Exemplo 1: criar um ouvinte HTTP</span><span class="sxs-lookup"><span data-stu-id="4038a-110">Example 1: Create an HTTP listener</span></span>
```
PS C:\>$Listener = New-AzApplicationGatewayHttpListener -Name "Listener01" -Protocol "Http" -FrontendIpConfiguration $FIp01 -FrontendPort $FP01
```

<span data-ttu-id="4038a-111">Esse comando cria um ouvinte HTTP chamado Listener01 e armazena o resultado na variável chamada $Listener.</span><span class="sxs-lookup"><span data-stu-id="4038a-111">This command creates an HTTP listener named Listener01 and stores the result in the variable named $Listener.</span></span>

### <span data-ttu-id="4038a-112">Exemplo 2: criar um ouvinte HTTP com SSL</span><span class="sxs-lookup"><span data-stu-id="4038a-112">Example 2: Create an HTTP listener with SSL</span></span>
```
PS C:\>$Listener = New-AzApplicationGatewayHttpListener -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIp01 -FrontendPort $FP01 -SslCertificate $SSLCert01
```

<span data-ttu-id="4038a-113">Esse comando cria um ouvinte HTTP que usa o Offload SSL e fornece o certificado SSL na variável $SSLCert 01.</span><span class="sxs-lookup"><span data-stu-id="4038a-113">This command creates an HTTP listener that uses SSL offload and provides the SSL certificate in the $SSLCert01 variable.</span></span>
<span data-ttu-id="4038a-114">O comando armazena o resultado na variável chamada $Listener.</span><span class="sxs-lookup"><span data-stu-id="4038a-114">The command stores the result in the variable named $Listener.</span></span>

### <span data-ttu-id="4038a-115">Exemplo 3: criar um ouvinte HTTP com firewall-política</span><span class="sxs-lookup"><span data-stu-id="4038a-115">Example 3: Create an HTTP listener with firewall-policy</span></span>
```
PS C:\>$Listener = New-AzApplicationGatewayHttpListener -Name "Listener01" -Protocol "Http" -FrontendIpConfiguration $FIp01 -FrontendPort $FP01 -FirewallPolicy $firewallPolicy
```

<span data-ttu-id="4038a-116">Esse comando cria um ouvinte HTTP chamado Listener01, FirewallPolicy como $firewallPolicy e armazena o resultado na variável chamada $Listener.</span><span class="sxs-lookup"><span data-stu-id="4038a-116">This command creates an HTTP listener named Listener01, FirewallPolicy as $firewallPolicy and stores the result in the variable named $Listener.</span></span>

### <span data-ttu-id="4038a-117">Exemplo 4: adicionar um ouvinte HTTPS com SSL e nomes de host</span><span class="sxs-lookup"><span data-stu-id="4038a-117">Example 4: Add a HTTPS listener with SSL and HostNames</span></span>
```
PS C:\> $Listener = New-AzApplicationGatewayHttpListener -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIp01 -FrontendPort $FP01 -SslCertificate $SSLCert01 -HostNames "*.contoso.com,www.microsoft.com"
```

<span data-ttu-id="4038a-118">Esse comando cria um ouvinte HTTP que usa o Offload SSL e fornece o certificado SSL na variável $SSLCert 01 juntamente com dois nomes de host.</span><span class="sxs-lookup"><span data-stu-id="4038a-118">This command creates an HTTP listener that uses SSL offload and provides the SSL certificate in the $SSLCert01 variable along with two HostNames.</span></span>
<span data-ttu-id="4038a-119">O comando armazena o resultado na variável chamada $Listener.</span><span class="sxs-lookup"><span data-stu-id="4038a-119">The command stores the result in the variable named $Listener.</span></span>

## <span data-ttu-id="4038a-120">OS</span><span class="sxs-lookup"><span data-stu-id="4038a-120">PARAMETERS</span></span>

### <span data-ttu-id="4038a-121">-CustomErrorConfiguration</span><span class="sxs-lookup"><span data-stu-id="4038a-121">-CustomErrorConfiguration</span></span>
<span data-ttu-id="4038a-122">Erro de cliente de um gateway de aplicativo</span><span class="sxs-lookup"><span data-stu-id="4038a-122">Customer error of an application gateway</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4038a-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4038a-123">-DefaultProfile</span></span>
<span data-ttu-id="4038a-124">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4038a-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4038a-125">-FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="4038a-125">-FirewallPolicy</span></span>
<span data-ttu-id="4038a-126">Especifica a referência de objeto a uma política de firewall de nível superior.</span><span class="sxs-lookup"><span data-stu-id="4038a-126">Specifies the object reference to a top-level firewall policy.</span></span> <span data-ttu-id="4038a-127">A referência do objeto pode ser criada usando-se New-AzApplicationGatewayWebApplicationFirewallPolicy cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4038a-127">The object reference can be created by using New-AzApplicationGatewayWebApplicationFirewallPolicy cmdlet.</span></span>
<span data-ttu-id="4038a-128">$firewallPolicy = New-AzApplicationGatewayFirewallPolicy-Name "wafPolicy1"-The Resource "rgName" uma política de firewall criada usando o commandlet acima pode ser referida em um nível de regra de caminho.</span><span class="sxs-lookup"><span data-stu-id="4038a-128">$firewallPolicy = New-AzApplicationGatewayFirewallPolicy -Name "wafPolicy1" -ResourceGroup "rgName" A firewall policy created using the above commandlet can be referred at a path-rule level.</span></span> <span data-ttu-id="4038a-129">o comando acima criaria as configurações de política padrão e as regras gerenciadas.</span><span class="sxs-lookup"><span data-stu-id="4038a-129">he above command would create a default policy settings and managed rules.</span></span>
<span data-ttu-id="4038a-130">Em vez dos valores padrão, os usuários podem especificar PolicySettings, ManagedRules usando New-AzApplicationGatewayFirewallPolicySettings e New-AzApplicationGatewayFirewallPolicyManagedRules, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="4038a-130">Instead of the default values, users can specify PolicySettings, ManagedRules by using New-AzApplicationGatewayFirewallPolicySettings and New-AzApplicationGatewayFirewallPolicyManagedRules respectively.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4038a-131">-FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="4038a-131">-FirewallPolicyId</span></span>
<span data-ttu-id="4038a-132">Especifica a ID de um recurso existente de firewall de aplicativo Web de nível superior.</span><span class="sxs-lookup"><span data-stu-id="4038a-132">Specifies the ID of an existing top-level web application firewall resource.</span></span>
<span data-ttu-id="4038a-133">IDs de política de firewall podem ser retornadas usando o cmdlet Get-AzApplicationGatewayWebApplicationFirewallPolicy.</span><span class="sxs-lookup"><span data-stu-id="4038a-133">Firewall policy IDs can be returned by using the Get-AzApplicationGatewayWebApplicationFirewallPolicy cmdlet.</span></span> <span data-ttu-id="4038a-134">Depois que tivermos a ID, você poderá usar o parâmetro *FirewallPolicyId* em vez do parâmetro *firewallpolicy* .</span><span class="sxs-lookup"><span data-stu-id="4038a-134">After we have the ID you can use *FirewallPolicyId* parameter instead of *FirewallPolicy* parameter.</span></span>
<span data-ttu-id="4038a-135">Por exemplo:-FirewallPolicyId/subscriptions/<assinatura-ID>/resourceGroups/<Resource-Group-ID>/providers/Microsoft.Network/ApplicationGatewayWebApplicationFirewallPolicies/ <firewallPolicyName></span><span class="sxs-lookup"><span data-stu-id="4038a-135">For instance: -FirewallPolicyId  �/subscriptions/<subscription-id>/resourceGroups/<resource-group-id>/providers/Microsoft.Network/ApplicationGatewayWebApplicationFirewallPolicies/<firewallPolicyName>�</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4038a-136">-FrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="4038a-136">-FrontendIPConfiguration</span></span>
<span data-ttu-id="4038a-137">Especifica o objeto de configuração de IP de front-end para o ouvinte HTTP.</span><span class="sxs-lookup"><span data-stu-id="4038a-137">Specifies front-end IP configuration object for the HTTP listener.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4038a-138">-FrontendIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="4038a-138">-FrontendIPConfigurationId</span></span>
<span data-ttu-id="4038a-139">Especifica a ID da configuração de IP de front-end para o ouvinte HTTP.</span><span class="sxs-lookup"><span data-stu-id="4038a-139">Specifies the ID of the front-end IP configuration for the HTTP listener.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4038a-140">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="4038a-140">-FrontendPort</span></span>
<span data-ttu-id="4038a-141">Especifica a porta de front-end do ouvinte HTTP.</span><span class="sxs-lookup"><span data-stu-id="4038a-141">Specifies the front-end port for the HTTP listener.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4038a-142">-FrontendPortId</span><span class="sxs-lookup"><span data-stu-id="4038a-142">-FrontendPortId</span></span>
<span data-ttu-id="4038a-143">Especifica a ID do objeto de porta de front-end para o ouvinte HTTP.</span><span class="sxs-lookup"><span data-stu-id="4038a-143">Specifies the ID of the front-end port object for the HTTP listener.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4038a-144">-HostName</span><span class="sxs-lookup"><span data-stu-id="4038a-144">-HostName</span></span>
<span data-ttu-id="4038a-145">Especifica o nome do host do ouvinte HTTP do Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="4038a-145">Specifies the host name of the application gateway HTTP listener.</span></span>

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

### <span data-ttu-id="4038a-146">-Nomes de host</span><span class="sxs-lookup"><span data-stu-id="4038a-146">-HostNames</span></span>
<span data-ttu-id="4038a-147">Nomes de host</span><span class="sxs-lookup"><span data-stu-id="4038a-147">Host names</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4038a-148">-Nome</span><span class="sxs-lookup"><span data-stu-id="4038a-148">-Name</span></span>
<span data-ttu-id="4038a-149">Especifica o nome da escuta HTTP que este cmdlet cria.</span><span class="sxs-lookup"><span data-stu-id="4038a-149">Specifies the name of the HTTP listener that this cmdlet creates.</span></span>

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

### <span data-ttu-id="4038a-150">-Protocolo</span><span class="sxs-lookup"><span data-stu-id="4038a-150">-Protocol</span></span>
<span data-ttu-id="4038a-151">Especifica o protocolo que a escuta HTTP usa.</span><span class="sxs-lookup"><span data-stu-id="4038a-151">Specifies the protocol that the HTTP listener uses.</span></span>

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

### <span data-ttu-id="4038a-152">-RequireServerNameIndication</span><span class="sxs-lookup"><span data-stu-id="4038a-152">-RequireServerNameIndication</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: true, false

Required: False
Position: Named
Default value: true
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4038a-153">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="4038a-153">-SslCertificate</span></span>
<span data-ttu-id="4038a-154">Especifica o objeto de certificado SSL para o ouvinte HTTP.</span><span class="sxs-lookup"><span data-stu-id="4038a-154">Specifies the SSL certificate object for the HTTP listener.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4038a-155">-SslCertificateId</span><span class="sxs-lookup"><span data-stu-id="4038a-155">-SslCertificateId</span></span>
<span data-ttu-id="4038a-156">Especifica a ID do certificado SSL para o ouvinte HTTP.</span><span class="sxs-lookup"><span data-stu-id="4038a-156">Specifies the ID of the SSL certificate for the HTTP listener.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4038a-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4038a-157">CommonParameters</span></span>
<span data-ttu-id="4038a-158">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4038a-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4038a-159">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4038a-159">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4038a-160">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4038a-160">INPUTS</span></span>

### <span data-ttu-id="4038a-161">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="4038a-161">None</span></span>

## <span data-ttu-id="4038a-162">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4038a-162">OUTPUTS</span></span>

### <span data-ttu-id="4038a-163">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="4038a-163">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="4038a-164">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4038a-164">NOTES</span></span>

## <span data-ttu-id="4038a-165">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4038a-165">RELATED LINKS</span></span>

[<span data-ttu-id="4038a-166">Add-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="4038a-166">Add-AzApplicationGatewayHttpListener</span></span>](./Add-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="4038a-167">Get-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="4038a-167">Get-AzApplicationGatewayHttpListener</span></span>](./Get-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="4038a-168">Remove-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="4038a-168">Remove-AzApplicationGatewayHttpListener</span></span>](./Remove-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="4038a-169">Set-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="4038a-169">Set-AzApplicationGatewayHttpListener</span></span>](./Set-AzApplicationGatewayHttpListener.md)



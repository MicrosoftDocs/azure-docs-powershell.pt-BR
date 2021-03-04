---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: AF8CC409-2EA7-4EC1-86C9-E7A773DE9201
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayHttpListener.md
ms.openlocfilehash: 1399dba141cb885e0ad184a588707e7c4f4efe7c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891271"
---
# <span data-ttu-id="de8d5-101">New-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="de8d5-101">New-AzApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="de8d5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="de8d5-102">SYNOPSIS</span></span>
<span data-ttu-id="de8d5-103">Cria um ouvinte HTTP para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="de8d5-103">Creates an HTTP listener for an application gateway.</span></span>

## <span data-ttu-id="de8d5-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="de8d5-104">SYNTAX</span></span>

### <span data-ttu-id="de8d5-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="de8d5-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayHttpListener -Name <String> [-FrontendIPConfigurationId <String>]
 [-FrontendPortId <String>] [-SslCertificateId <String>] [-FirewallPolicyId <String>] [-SslProfileId <String>]
 [-HostName <String>] [-HostNames <String[]>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="de8d5-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="de8d5-106">SetByResource</span></span>
```
New-AzApplicationGatewayHttpListener -Name <String>
 [-FrontendIPConfiguration <PSApplicationGatewayFrontendIPConfiguration>]
 [-FrontendPort <PSApplicationGatewayFrontendPort>]
 [-FirewallPolicy <PSApplicationGatewayWebApplicationFirewallPolicy>]
 [-SslCertificate <PSApplicationGatewaySslCertificate>] [-SslProfile <PSApplicationGatewaySslProfile>]
 [-HostName <String>] [-HostNames <String[]>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="de8d5-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="de8d5-107">DESCRIPTION</span></span>
<span data-ttu-id="de8d5-108">O cmdlet **New-AzApplicationGatewayHttpListener** cria um ouvinte HTTP para um gateway de aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="de8d5-108">The **New-AzApplicationGatewayHttpListener** cmdlet creates an HTTP listener for an Azure application gateway.</span></span>

## <span data-ttu-id="de8d5-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="de8d5-109">EXAMPLES</span></span>

### <span data-ttu-id="de8d5-110">Exemplo 1: Criar um ouvinte HTTP</span><span class="sxs-lookup"><span data-stu-id="de8d5-110">Example 1: Create an HTTP listener</span></span>
```
PS C:\>$Listener = New-AzApplicationGatewayHttpListener -Name "Listener01" -Protocol "Http" -FrontendIpConfiguration $FIp01 -FrontendPort $FP01
```

<span data-ttu-id="de8d5-111">Este comando cria um ouvinte HTTP chamado Listener01 e armazena o resultado na variável chamada $Listener.</span><span class="sxs-lookup"><span data-stu-id="de8d5-111">This command creates an HTTP listener named Listener01 and stores the result in the variable named $Listener.</span></span>

### <span data-ttu-id="de8d5-112">Exemplo 2: Criar um ouvinte HTTP com SSL</span><span class="sxs-lookup"><span data-stu-id="de8d5-112">Example 2: Create an HTTP listener with SSL</span></span>
```
PS C:\>$Listener = New-AzApplicationGatewayHttpListener -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIp01 -FrontendPort $FP01 -SslCertificate $SSLCert01
```

<span data-ttu-id="de8d5-113">Este comando cria um ouvinte HTTP que usa a carga SSL e fornece o certificado SSL na variável $SSLCert 01.</span><span class="sxs-lookup"><span data-stu-id="de8d5-113">This command creates an HTTP listener that uses SSL offload and provides the SSL certificate in the $SSLCert01 variable.</span></span>
<span data-ttu-id="de8d5-114">O comando armazena o resultado na variável chamada $Listener.</span><span class="sxs-lookup"><span data-stu-id="de8d5-114">The command stores the result in the variable named $Listener.</span></span>

### <span data-ttu-id="de8d5-115">Exemplo 3: Criar um ouvinte HTTP com política de firewall</span><span class="sxs-lookup"><span data-stu-id="de8d5-115">Example 3: Create an HTTP listener with firewall-policy</span></span>
```
PS C:\>$Listener = New-AzApplicationGatewayHttpListener -Name "Listener01" -Protocol "Http" -FrontendIpConfiguration $FIp01 -FrontendPort $FP01 -FirewallPolicy $firewallPolicy
```

<span data-ttu-id="de8d5-116">Este comando cria um ouvinte HTTP chamado Listener01, FirewallPolicy como $firewallPolicy e armazena o resultado na variável chamada $Listener.</span><span class="sxs-lookup"><span data-stu-id="de8d5-116">This command creates an HTTP listener named Listener01, FirewallPolicy as $firewallPolicy and stores the result in the variable named $Listener.</span></span>

### <span data-ttu-id="de8d5-117">Exemplo 4: Adicionar um ouvinte HTTPS com SSL e HostNames</span><span class="sxs-lookup"><span data-stu-id="de8d5-117">Example 4: Add a HTTPS listener with SSL and HostNames</span></span>
```
PS C:\> $Listener = New-AzApplicationGatewayHttpListener -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIp01 -FrontendPort $FP01 -SslCertificate $SSLCert01 -HostNames "*.contoso.com,www.microsoft.com"
```

<span data-ttu-id="de8d5-118">Este comando cria um ouvinte HTTP que usa a carga SSL e fornece o certificado SSL na variável $SSLCert 01 juntamente com dois HostNames.</span><span class="sxs-lookup"><span data-stu-id="de8d5-118">This command creates an HTTP listener that uses SSL offload and provides the SSL certificate in the $SSLCert01 variable along with two HostNames.</span></span>
<span data-ttu-id="de8d5-119">O comando armazena o resultado na variável chamada $Listener.</span><span class="sxs-lookup"><span data-stu-id="de8d5-119">The command stores the result in the variable named $Listener.</span></span>

## <span data-ttu-id="de8d5-120">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="de8d5-120">PARAMETERS</span></span>

### <span data-ttu-id="de8d5-121">-CustomErrorConfiguration</span><span class="sxs-lookup"><span data-stu-id="de8d5-121">-CustomErrorConfiguration</span></span>
<span data-ttu-id="de8d5-122">Erro do cliente de um gateway de aplicativo</span><span class="sxs-lookup"><span data-stu-id="de8d5-122">Customer error of an application gateway</span></span>

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

### <span data-ttu-id="de8d5-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de8d5-123">-DefaultProfile</span></span>
<span data-ttu-id="de8d5-124">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="de8d5-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="de8d5-125">-FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="de8d5-125">-FirewallPolicy</span></span>
<span data-ttu-id="de8d5-126">Especifica a referência de objeto a uma política de firewall de nível superior.</span><span class="sxs-lookup"><span data-stu-id="de8d5-126">Specifies the object reference to a top-level firewall policy.</span></span> <span data-ttu-id="de8d5-127">A referência de objeto pode ser criada usando New-AzApplicationGatewayWebApplicationFirewallPolicy cmdlet.</span><span class="sxs-lookup"><span data-stu-id="de8d5-127">The object reference can be created by using New-AzApplicationGatewayWebApplicationFirewallPolicy cmdlet.</span></span>
<span data-ttu-id="de8d5-128">$firewallPolicy = New-AzApplicationGatewayFirewallPolicy -Name "wafPolicy1" -ResourceGroup "rgName" Uma política de firewall criada usando o commandlet acima pode ser referenciada em um nível de regra de caminho.</span><span class="sxs-lookup"><span data-stu-id="de8d5-128">$firewallPolicy = New-AzApplicationGatewayFirewallPolicy -Name "wafPolicy1" -ResourceGroup "rgName" A firewall policy created using the above commandlet can be referred at a path-rule level.</span></span> <span data-ttu-id="de8d5-129">ele acima do comando criaria configurações de política padrão e regras gerenciadas.</span><span class="sxs-lookup"><span data-stu-id="de8d5-129">he above command would create a default policy settings and managed rules.</span></span>
<span data-ttu-id="de8d5-130">Em vez dos valores padrão, os usuários podem especificar PolicySettings, ManagedRules usando New-AzApplicationGatewayFirewallPolicySettings e New-AzApplicationGatewayFirewallPolicyManagedRules respectivamente.</span><span class="sxs-lookup"><span data-stu-id="de8d5-130">Instead of the default values, users can specify PolicySettings, ManagedRules by using New-AzApplicationGatewayFirewallPolicySettings and New-AzApplicationGatewayFirewallPolicyManagedRules respectively.</span></span>

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

### <span data-ttu-id="de8d5-131">-FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="de8d5-131">-FirewallPolicyId</span></span>
<span data-ttu-id="de8d5-132">Especifica a ID de um recurso de firewall de aplicativo Web de nível superior existente.</span><span class="sxs-lookup"><span data-stu-id="de8d5-132">Specifies the ID of an existing top-level web application firewall resource.</span></span>
<span data-ttu-id="de8d5-133">As IDs de política de firewall podem ser retornadas usando o cmdlet Get-AzApplicationGatewayWebApplicationFirewallPolicy firewall.</span><span class="sxs-lookup"><span data-stu-id="de8d5-133">Firewall policy IDs can be returned by using the Get-AzApplicationGatewayWebApplicationFirewallPolicy cmdlet.</span></span> <span data-ttu-id="de8d5-134">Depois de termos a ID, você pode usar *o parâmetro FirewallPolicyId* em vez do *parâmetro FirewallPolicy.*</span><span class="sxs-lookup"><span data-stu-id="de8d5-134">After we have the ID you can use *FirewallPolicyId* parameter instead of *FirewallPolicy* parameter.</span></span>
<span data-ttu-id="de8d5-135">Por exemplo: -FirewallPolicyId /subscriptions/<subscription-id>/resourceGroups/<resource-group-id>/providers/Microsoft.Network/ApplicationGatewayWebApplicationFirewallPolicies/ <firewallPolicyName></span><span class="sxs-lookup"><span data-stu-id="de8d5-135">For instance: -FirewallPolicyId  �/subscriptions/<subscription-id>/resourceGroups/<resource-group-id>/providers/Microsoft.Network/ApplicationGatewayWebApplicationFirewallPolicies/<firewallPolicyName>�</span></span>

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

### <span data-ttu-id="de8d5-136">-FrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="de8d5-136">-FrontendIPConfiguration</span></span>
<span data-ttu-id="de8d5-137">Especifica o objeto de configuração IP front-end para o ouvinte HTTP.</span><span class="sxs-lookup"><span data-stu-id="de8d5-137">Specifies front-end IP configuration object for the HTTP listener.</span></span>

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

### <span data-ttu-id="de8d5-138">-FrontendIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="de8d5-138">-FrontendIPConfigurationId</span></span>
<span data-ttu-id="de8d5-139">Especifica a ID da configuração de IP front-end para o ouvinte HTTP.</span><span class="sxs-lookup"><span data-stu-id="de8d5-139">Specifies the ID of the front-end IP configuration for the HTTP listener.</span></span>

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

### <span data-ttu-id="de8d5-140">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="de8d5-140">-FrontendPort</span></span>
<span data-ttu-id="de8d5-141">Especifica a porta front-end do ouvinte HTTP.</span><span class="sxs-lookup"><span data-stu-id="de8d5-141">Specifies the front-end port for the HTTP listener.</span></span>

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

### <span data-ttu-id="de8d5-142">-FrontendPortId</span><span class="sxs-lookup"><span data-stu-id="de8d5-142">-FrontendPortId</span></span>
<span data-ttu-id="de8d5-143">Especifica a ID do objeto de porta front-end para o ouvinte HTTP.</span><span class="sxs-lookup"><span data-stu-id="de8d5-143">Specifies the ID of the front-end port object for the HTTP listener.</span></span>

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

### <span data-ttu-id="de8d5-144">-HostName</span><span class="sxs-lookup"><span data-stu-id="de8d5-144">-HostName</span></span>
<span data-ttu-id="de8d5-145">Especifica o nome do host do ouvinte HTTP do gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="de8d5-145">Specifies the host name of the application gateway HTTP listener.</span></span>

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

### <span data-ttu-id="de8d5-146">-HostNames</span><span class="sxs-lookup"><span data-stu-id="de8d5-146">-HostNames</span></span>
<span data-ttu-id="de8d5-147">Nomes de host</span><span class="sxs-lookup"><span data-stu-id="de8d5-147">Host names</span></span>

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

### <span data-ttu-id="de8d5-148">-Name</span><span class="sxs-lookup"><span data-stu-id="de8d5-148">-Name</span></span>
<span data-ttu-id="de8d5-149">Especifica o nome do ouvinte HTTP que este cmdlet cria.</span><span class="sxs-lookup"><span data-stu-id="de8d5-149">Specifies the name of the HTTP listener that this cmdlet creates.</span></span>

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

### <span data-ttu-id="de8d5-150">-Protocol</span><span class="sxs-lookup"><span data-stu-id="de8d5-150">-Protocol</span></span>
<span data-ttu-id="de8d5-151">Especifica o protocolo que o ouvinte HTTP usa.</span><span class="sxs-lookup"><span data-stu-id="de8d5-151">Specifies the protocol that the HTTP listener uses.</span></span>

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

### <span data-ttu-id="de8d5-152">-RequireServerNameIndication</span><span class="sxs-lookup"><span data-stu-id="de8d5-152">-RequireServerNameIndication</span></span>
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

### <span data-ttu-id="de8d5-153">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="de8d5-153">-SslCertificate</span></span>
<span data-ttu-id="de8d5-154">Especifica o objeto de certificado SSL para o ouvinte HTTP.</span><span class="sxs-lookup"><span data-stu-id="de8d5-154">Specifies the SSL certificate object for the HTTP listener.</span></span>

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

### <span data-ttu-id="de8d5-155">-SslCertificateId</span><span class="sxs-lookup"><span data-stu-id="de8d5-155">-SslCertificateId</span></span>
<span data-ttu-id="de8d5-156">Especifica a ID do certificado SSL para o ouvinte HTTP.</span><span class="sxs-lookup"><span data-stu-id="de8d5-156">Specifies the ID of the SSL certificate for the HTTP listener.</span></span>

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

### <span data-ttu-id="de8d5-157">-SslProfile</span><span class="sxs-lookup"><span data-stu-id="de8d5-157">-SslProfile</span></span>
<span data-ttu-id="de8d5-158">SslProfile</span><span class="sxs-lookup"><span data-stu-id="de8d5-158">SslProfile</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de8d5-159">-SslProfileId</span><span class="sxs-lookup"><span data-stu-id="de8d5-159">-SslProfileId</span></span>
<span data-ttu-id="de8d5-160">SslProfileId</span><span class="sxs-lookup"><span data-stu-id="de8d5-160">SslProfileId</span></span>

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

### <span data-ttu-id="de8d5-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de8d5-161">CommonParameters</span></span>
<span data-ttu-id="de8d5-162">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de8d5-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de8d5-163">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="de8d5-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de8d5-164">INPUTS</span><span class="sxs-lookup"><span data-stu-id="de8d5-164">INPUTS</span></span>

### <span data-ttu-id="de8d5-165">Nenhum</span><span class="sxs-lookup"><span data-stu-id="de8d5-165">None</span></span>

## <span data-ttu-id="de8d5-166">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="de8d5-166">OUTPUTS</span></span>

### <span data-ttu-id="de8d5-167">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="de8d5-167">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="de8d5-168">NOTES</span><span class="sxs-lookup"><span data-stu-id="de8d5-168">NOTES</span></span>

## <span data-ttu-id="de8d5-169">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="de8d5-169">RELATED LINKS</span></span>

[<span data-ttu-id="de8d5-170">Add-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="de8d5-170">Add-AzApplicationGatewayHttpListener</span></span>](./Add-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="de8d5-171">Get-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="de8d5-171">Get-AzApplicationGatewayHttpListener</span></span>](./Get-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="de8d5-172">Remove-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="de8d5-172">Remove-AzApplicationGatewayHttpListener</span></span>](./Remove-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="de8d5-173">Set-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="de8d5-173">Set-AzApplicationGatewayHttpListener</span></span>](./Set-AzApplicationGatewayHttpListener.md)



---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: AF8CC409-2EA7-4EC1-86C9-E7A773DE9201
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayHttpListener.md
ms.openlocfilehash: a6fc3eb16cc82f7a0964e8cd0c1697a083771016
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117419"
---
# <span data-ttu-id="f72af-101">New-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="f72af-101">New-AzApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="f72af-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f72af-102">SYNOPSIS</span></span>
<span data-ttu-id="f72af-103">Cria um ouvinte HTTP para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f72af-103">Creates an HTTP listener for an application gateway.</span></span>

## <span data-ttu-id="f72af-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f72af-104">SYNTAX</span></span>

### <span data-ttu-id="f72af-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="f72af-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayHttpListener -Name <String> [-FrontendIPConfigurationId <String>]
 [-FrontendPortId <String>] [-SslCertificateId <String>] [-FirewallPolicyId <String>] [-SslProfileId <String>]
 [-HostName <String>] [-HostNames <String[]>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f72af-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="f72af-106">SetByResource</span></span>
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

## <span data-ttu-id="f72af-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="f72af-107">DESCRIPTION</span></span>
<span data-ttu-id="f72af-108">O **cmdlet New-AzApplicationGatewayHttpListener** cria um ouvinte HTTP para um gateway de aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="f72af-108">The **New-AzApplicationGatewayHttpListener** cmdlet creates an HTTP listener for an Azure application gateway.</span></span>

## <span data-ttu-id="f72af-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f72af-109">EXAMPLES</span></span>

### <span data-ttu-id="f72af-110">Exemplo 1: Criar um ouvinte HTTP</span><span class="sxs-lookup"><span data-stu-id="f72af-110">Example 1: Create an HTTP listener</span></span>
```
PS C:\>$Listener = New-AzApplicationGatewayHttpListener -Name "Listener01" -Protocol "Http" -FrontendIpConfiguration $FIp01 -FrontendPort $FP01
```

<span data-ttu-id="f72af-111">Esse comando cria um ouvinte HTTP chamado Ouvinte01 e armazena o resultado na variável chamada $Listener.</span><span class="sxs-lookup"><span data-stu-id="f72af-111">This command creates an HTTP listener named Listener01 and stores the result in the variable named $Listener.</span></span>

### <span data-ttu-id="f72af-112">Exemplo 2: Criar um ouvinte HTTP com SSL</span><span class="sxs-lookup"><span data-stu-id="f72af-112">Example 2: Create an HTTP listener with SSL</span></span>
```
PS C:\>$Listener = New-AzApplicationGatewayHttpListener -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIp01 -FrontendPort $FP01 -SslCertificate $SSLCert01
```

<span data-ttu-id="f72af-113">Esse comando cria um ouvinte HTTP que usa a recarga SSL e fornece o certificado SSL na variável $SSLCert 01.</span><span class="sxs-lookup"><span data-stu-id="f72af-113">This command creates an HTTP listener that uses SSL offload and provides the SSL certificate in the $SSLCert01 variable.</span></span>
<span data-ttu-id="f72af-114">O comando armazena o resultado na variável chamada $Listener.</span><span class="sxs-lookup"><span data-stu-id="f72af-114">The command stores the result in the variable named $Listener.</span></span>

### <span data-ttu-id="f72af-115">Exemplo 3: Criar um ouvinte HTTP com política de firewall</span><span class="sxs-lookup"><span data-stu-id="f72af-115">Example 3: Create an HTTP listener with firewall-policy</span></span>
```
PS C:\>$Listener = New-AzApplicationGatewayHttpListener -Name "Listener01" -Protocol "Http" -FrontendIpConfiguration $FIp01 -FrontendPort $FP01 -FirewallPolicy $firewallPolicy
```

<span data-ttu-id="f72af-116">Esse comando cria um ouvinte HTTP chamado Ouvinte01, FirewallPolicy como $firewallPolicy e armazena o resultado na variável chamada $Listener.</span><span class="sxs-lookup"><span data-stu-id="f72af-116">This command creates an HTTP listener named Listener01, FirewallPolicy as $firewallPolicy and stores the result in the variable named $Listener.</span></span>

### <span data-ttu-id="f72af-117">Exemplo 4: Adicionar um ouvinte HTTPS com SSL e Nomes de Host</span><span class="sxs-lookup"><span data-stu-id="f72af-117">Example 4: Add a HTTPS listener with SSL and HostNames</span></span>
```
PS C:\> $Listener = New-AzApplicationGatewayHttpListener -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIp01 -FrontendPort $FP01 -SslCertificate $SSLCert01 -HostNames "*.contoso.com,www.microsoft.com"
```

<span data-ttu-id="f72af-118">Esse comando cria um ouvinte HTTP que usa a recarga SSL e fornece o certificado SSL na variável $SSLCert 01 juntamente com dois Nomes de Host.</span><span class="sxs-lookup"><span data-stu-id="f72af-118">This command creates an HTTP listener that uses SSL offload and provides the SSL certificate in the $SSLCert01 variable along with two HostNames.</span></span>
<span data-ttu-id="f72af-119">O comando armazena o resultado na variável chamada $Listener.</span><span class="sxs-lookup"><span data-stu-id="f72af-119">The command stores the result in the variable named $Listener.</span></span>

## <span data-ttu-id="f72af-120">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f72af-120">PARAMETERS</span></span>

### <span data-ttu-id="f72af-121">-CustomErrorConfiguration</span><span class="sxs-lookup"><span data-stu-id="f72af-121">-CustomErrorConfiguration</span></span>
<span data-ttu-id="f72af-122">Erro do cliente de um gateway de aplicativo</span><span class="sxs-lookup"><span data-stu-id="f72af-122">Customer error of an application gateway</span></span>

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

### <span data-ttu-id="f72af-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f72af-123">-DefaultProfile</span></span>
<span data-ttu-id="f72af-124">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="f72af-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f72af-125">-FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="f72af-125">-FirewallPolicy</span></span>
<span data-ttu-id="f72af-126">Especifica a referência de objeto a uma política de firewall de nível superior.</span><span class="sxs-lookup"><span data-stu-id="f72af-126">Specifies the object reference to a top-level firewall policy.</span></span> <span data-ttu-id="f72af-127">A referência de objeto pode ser criada usando New-AzApplicationGatewayWebApplicationFirewallPolicy cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f72af-127">The object reference can be created by using New-AzApplicationGatewayWebApplicationFirewallPolicy cmdlet.</span></span>
<span data-ttu-id="f72af-128">$firewallPolicy = New-AzApplicationGatewayFirewallPolicy -Name "wafPolicy1" -ResourceGroup "rgName" Uma política de firewall criada usando o commandlet acima pode ser referenciada em um nível de regra de caminho.</span><span class="sxs-lookup"><span data-stu-id="f72af-128">$firewallPolicy = New-AzApplicationGatewayFirewallPolicy -Name "wafPolicy1" -ResourceGroup "rgName" A firewall policy created using the above commandlet can be referred at a path-rule level.</span></span> <span data-ttu-id="f72af-129">ele acima do comando criaria uma configuração de política padrão e regras gerenciadas.</span><span class="sxs-lookup"><span data-stu-id="f72af-129">he above command would create a default policy settings and managed rules.</span></span>
<span data-ttu-id="f72af-130">Em vez dos valores padrão, os usuários podem especificar PolicySettings, ManagedRules usando New-AzApplicationGatewayFirewallPolicySettings e New-AzApplicationGatewayFirewallPolicyManagedRules respectivamente.</span><span class="sxs-lookup"><span data-stu-id="f72af-130">Instead of the default values, users can specify PolicySettings, ManagedRules by using New-AzApplicationGatewayFirewallPolicySettings and New-AzApplicationGatewayFirewallPolicyManagedRules respectively.</span></span>

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

### <span data-ttu-id="f72af-131">-FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="f72af-131">-FirewallPolicyId</span></span>
<span data-ttu-id="f72af-132">Especifica a ID de um recurso de firewall de aplicativo Web de nível superior existente.</span><span class="sxs-lookup"><span data-stu-id="f72af-132">Specifies the ID of an existing top-level web application firewall resource.</span></span>
<span data-ttu-id="f72af-133">As IDs de política de firewall podem ser retornadas usando Get-AzApplicationGatewayWebApplicationFirewallPolicy cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f72af-133">Firewall policy IDs can be returned by using the Get-AzApplicationGatewayWebApplicationFirewallPolicy cmdlet.</span></span> <span data-ttu-id="f72af-134">Depois de termos a ID, você pode usar o *parâmetro FirewallPolicyId em* vez do *parâmetro FirewallPolicy.*</span><span class="sxs-lookup"><span data-stu-id="f72af-134">After we have the ID you can use *FirewallPolicyId* parameter instead of *FirewallPolicy* parameter.</span></span>
<span data-ttu-id="f72af-135">Por exemplo: -FirewallPolicyId /subscriptions/<subscription-id>/resourceGroups/<resource-group-id>/providers/Microsoft.Network/ApplicationGatewayWebApplicationFirewallPolicies/ <firewallPolicyName></span><span class="sxs-lookup"><span data-stu-id="f72af-135">For instance: -FirewallPolicyId  �/subscriptions/<subscription-id>/resourceGroups/<resource-group-id>/providers/Microsoft.Network/ApplicationGatewayWebApplicationFirewallPolicies/<firewallPolicyName>�</span></span>

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

### <span data-ttu-id="f72af-136">-FrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="f72af-136">-FrontendIPConfiguration</span></span>
<span data-ttu-id="f72af-137">Especifica o objeto de configuração IP front-end para o ouvinte HTTP.</span><span class="sxs-lookup"><span data-stu-id="f72af-137">Specifies front-end IP configuration object for the HTTP listener.</span></span>

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

### <span data-ttu-id="f72af-138">-FrontendIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="f72af-138">-FrontendIPConfigurationId</span></span>
<span data-ttu-id="f72af-139">Especifica a ID da configuração IP de front-end para o ouvinte HTTP.</span><span class="sxs-lookup"><span data-stu-id="f72af-139">Specifies the ID of the front-end IP configuration for the HTTP listener.</span></span>

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

### <span data-ttu-id="f72af-140">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="f72af-140">-FrontendPort</span></span>
<span data-ttu-id="f72af-141">Especifica a porta front-end para o ouvinte HTTP.</span><span class="sxs-lookup"><span data-stu-id="f72af-141">Specifies the front-end port for the HTTP listener.</span></span>

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

### <span data-ttu-id="f72af-142">-FrontendPortId</span><span class="sxs-lookup"><span data-stu-id="f72af-142">-FrontendPortId</span></span>
<span data-ttu-id="f72af-143">Especifica a ID do objeto de porta front-end para o ouvinte HTTP.</span><span class="sxs-lookup"><span data-stu-id="f72af-143">Specifies the ID of the front-end port object for the HTTP listener.</span></span>

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

### <span data-ttu-id="f72af-144">-Nomedo Host</span><span class="sxs-lookup"><span data-stu-id="f72af-144">-HostName</span></span>
<span data-ttu-id="f72af-145">Especifica o nome do host do ouvinte HTTP do gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f72af-145">Specifies the host name of the application gateway HTTP listener.</span></span>

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

### <span data-ttu-id="f72af-146">-Nomes de Host</span><span class="sxs-lookup"><span data-stu-id="f72af-146">-HostNames</span></span>
<span data-ttu-id="f72af-147">Nomes de host</span><span class="sxs-lookup"><span data-stu-id="f72af-147">Host names</span></span>

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

### <span data-ttu-id="f72af-148">-Nome</span><span class="sxs-lookup"><span data-stu-id="f72af-148">-Name</span></span>
<span data-ttu-id="f72af-149">Especifica o nome do ouvinte HTTP que este cmdlet cria.</span><span class="sxs-lookup"><span data-stu-id="f72af-149">Specifies the name of the HTTP listener that this cmdlet creates.</span></span>

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

### <span data-ttu-id="f72af-150">-Protocolo</span><span class="sxs-lookup"><span data-stu-id="f72af-150">-Protocol</span></span>
<span data-ttu-id="f72af-151">Especifica o protocolo que o ouvinte HTTP usa.</span><span class="sxs-lookup"><span data-stu-id="f72af-151">Specifies the protocol that the HTTP listener uses.</span></span>

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

### <span data-ttu-id="f72af-152">-RequireServerNameIndication</span><span class="sxs-lookup"><span data-stu-id="f72af-152">-RequireServerNameIndication</span></span>
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

### <span data-ttu-id="f72af-153">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="f72af-153">-SslCertificate</span></span>
<span data-ttu-id="f72af-154">Especifica o objeto de certificado SSL para o ouvinte HTTP.</span><span class="sxs-lookup"><span data-stu-id="f72af-154">Specifies the SSL certificate object for the HTTP listener.</span></span>

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

### <span data-ttu-id="f72af-155">-SslCertificateId</span><span class="sxs-lookup"><span data-stu-id="f72af-155">-SslCertificateId</span></span>
<span data-ttu-id="f72af-156">Especifica a ID do certificado SSL para o ouvinte HTTP.</span><span class="sxs-lookup"><span data-stu-id="f72af-156">Specifies the ID of the SSL certificate for the HTTP listener.</span></span>

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

### <span data-ttu-id="f72af-157">-SslProfile</span><span class="sxs-lookup"><span data-stu-id="f72af-157">-SslProfile</span></span>
<span data-ttu-id="f72af-158">SslProfile</span><span class="sxs-lookup"><span data-stu-id="f72af-158">SslProfile</span></span>

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

### <span data-ttu-id="f72af-159">-SslProfileId</span><span class="sxs-lookup"><span data-stu-id="f72af-159">-SslProfileId</span></span>
<span data-ttu-id="f72af-160">SslProfileId</span><span class="sxs-lookup"><span data-stu-id="f72af-160">SslProfileId</span></span>

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

### <span data-ttu-id="f72af-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f72af-161">CommonParameters</span></span>
<span data-ttu-id="f72af-162">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f72af-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f72af-163">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f72af-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f72af-164">Entradas</span><span class="sxs-lookup"><span data-stu-id="f72af-164">INPUTS</span></span>

### <span data-ttu-id="f72af-165">Nenhum</span><span class="sxs-lookup"><span data-stu-id="f72af-165">None</span></span>

## <span data-ttu-id="f72af-166">Saídas</span><span class="sxs-lookup"><span data-stu-id="f72af-166">OUTPUTS</span></span>

### <span data-ttu-id="f72af-167">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="f72af-167">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="f72af-168">Notas</span><span class="sxs-lookup"><span data-stu-id="f72af-168">NOTES</span></span>

## <span data-ttu-id="f72af-169">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f72af-169">RELATED LINKS</span></span>

[<span data-ttu-id="f72af-170">Add-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="f72af-170">Add-AzApplicationGatewayHttpListener</span></span>](./Add-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="f72af-171">Get-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="f72af-171">Get-AzApplicationGatewayHttpListener</span></span>](./Get-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="f72af-172">Remove-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="f72af-172">Remove-AzApplicationGatewayHttpListener</span></span>](./Remove-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="f72af-173">Set-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="f72af-173">Set-AzApplicationGatewayHttpListener</span></span>](./Set-AzApplicationGatewayHttpListener.md)



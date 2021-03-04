---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/powershell/module/az.frontdoor/enable-azfrontdoorcustomdomainhttps
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Enable-AzFrontDoorCustomDomainHttps.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Enable-AzFrontDoorCustomDomainHttps.md
ms.openlocfilehash: cb5986d7e8d467c76b64baddb5fd389eda1b5b8b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101893357"
---
# <span data-ttu-id="45fed-101">Enable-AzFrontDoorCustomDomainHttps</span><span class="sxs-lookup"><span data-stu-id="45fed-101">Enable-AzFrontDoorCustomDomainHttps</span></span>

## <span data-ttu-id="45fed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="45fed-102">SYNOPSIS</span></span>
<span data-ttu-id="45fed-103">Habilitar HTTPS para um domínio personalizado usando o certificado gerenciado porta da frente ou usando o próprio certificado do Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="45fed-103">Enable HTTPS for a custom domain using Front Door managed certificate or using own certificate from Azure Key Vault.</span></span>

## <span data-ttu-id="45fed-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="45fed-104">SYNTAX</span></span>

### <span data-ttu-id="45fed-105">ByFieldsParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="45fed-105">ByFieldsParameterSet (Default)</span></span>
```
Enable-AzFrontDoorCustomDomainHttps -ResourceGroupName <String> -FrontDoorName <String>
 -FrontendEndpointName <String> [-MinimumTlsVersion <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="45fed-106">ByFieldsWithVaultParameterSet</span><span class="sxs-lookup"><span data-stu-id="45fed-106">ByFieldsWithVaultParameterSet</span></span>
```
Enable-AzFrontDoorCustomDomainHttps -ResourceGroupName <String> -FrontDoorName <String>
 -FrontendEndpointName <String> -VaultId <String> -SecretName <String> -SecretVersion <String>
 [-MinimumTlsVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="45fed-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="45fed-107">ByResourceIdParameterSet</span></span>
```
Enable-AzFrontDoorCustomDomainHttps -ResourceId <String> [-MinimumTlsVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="45fed-108">ByResourceIdWithVaultParameterSet</span><span class="sxs-lookup"><span data-stu-id="45fed-108">ByResourceIdWithVaultParameterSet</span></span>
```
Enable-AzFrontDoorCustomDomainHttps -ResourceId <String> -VaultId <String> -SecretName <String>
 -SecretVersion <String> [-MinimumTlsVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="45fed-109">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="45fed-109">ByObjectParameterSet</span></span>
```
Enable-AzFrontDoorCustomDomainHttps -InputObject <PSFrontendEndpoint> [-MinimumTlsVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="45fed-110">ByObjectWithVaultParameterSet</span><span class="sxs-lookup"><span data-stu-id="45fed-110">ByObjectWithVaultParameterSet</span></span>
```
Enable-AzFrontDoorCustomDomainHttps -InputObject <PSFrontendEndpoint> -VaultId <String> -SecretName <String>
 -SecretVersion <String> [-MinimumTlsVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="45fed-111">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="45fed-111">DESCRIPTION</span></span>
<span data-ttu-id="45fed-112">**Enable-AzFrontDoorCustomDomainHttps** habilita HTTPS para um domínio personalizado.</span><span class="sxs-lookup"><span data-stu-id="45fed-112">The **Enable-AzFrontDoorCustomDomainHttps** enables HTTPS for a custom domain.</span></span>

## <span data-ttu-id="45fed-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="45fed-113">EXAMPLES</span></span>

### <span data-ttu-id="45fed-114">Exemplo 1: Habilitar HTTPS para um domínio personalizado com FrontDoorName e ResourceGroupName usando o certificado gerenciado porta da frente.</span><span class="sxs-lookup"><span data-stu-id="45fed-114">Example 1: Enable HTTPS for a custom domain with FrontDoorName and ResourceGroupName using Front Door managed certificate.</span></span>
```powershell
PS C:\> Enable-AzFrontDoorCustomDomainHttps -ResourceGroupName "resourcegroup1" -FrontDoorName "frontdoor1" -FrontendEndpointName "frontendpointname1-custom-xyz" -MinimumTlsVersion "1.2"


HostName                         : frontendpointname1.custom.xyz
SessionAffinityEnabledState      : Disabled
SessionAffinityTtlSeconds        : 0
WebApplicationFirewallPolicyLink :
Backends                         :
CustomHttpsProvisioningState     : Enabling
CustomHttpsProvisioningSubstate  : SubmittingDomainControlValidationRequest
CertificateSource                : FrontDoor
ProtocolType                     : ServerNameIndication
MinimumTlsVersion                : 1.2
Vault                            :
SecretName                       :
SecretVersion                    :
CertificateType                  :
ResourceState                    : Enabled
Id                               : /subscriptions/{guid}/resourcegroups/resourcegroup1
                                   /providers/Microsoft.Network/frontdoors/frontdoor1/frontendendpoints/frontendpointname1-custom-xyz
Name                             : frontendpointname1-custom-xyz
Type                             : Microsoft.Network/frontdoors/frontendendpoints
```

<span data-ttu-id="45fed-115">Habilitar HTTPS para um domínio personalizado "frontendpointname1-custom-xyz" que faz parte do "frontdoor1" da Porta da Frente no grupo de recursos "resourcegroup1" usando o certificado gerenciado porta da frente.</span><span class="sxs-lookup"><span data-stu-id="45fed-115">Enable HTTPS for a custom domain "frontendpointname1-custom-xyz" that is part of Front Door "frontdoor1" in resource group "resourcegroup1" using Front Door managed certificate.</span></span>

### <span data-ttu-id="45fed-116">Exemplo 2: Habilitar HTTPS para um domínio personalizado com FrontDoorName e ResourceGroupName usando o próprio certificado no Key Vault.</span><span class="sxs-lookup"><span data-stu-id="45fed-116">Example 2: Enable HTTPS for a custom domain with FrontDoorName and ResourceGroupName using own certificate in Key Vault.</span></span>
```powershell
PS C:\> $vaultId = (Get-AzKeyVault -VaultName $vaultName).ResourceId
PS C:\> Enable-AzFrontDoorCustomDomainHttps -ResourceGroupName "resourcegroup1" -FrontDoorName "frontdoor1" -FrontendEndpointName "frontendpointname1-custom-xyz" -Vault $vaultId -secretName $secretName -SecretVersion $secretVersion -MinimumTlsVersion "1.0"


HostName                         : frontendpointname1.custom.xyz
SessionAffinityEnabledState      : Disabled
SessionAffinityTtlSeconds        : 0
WebApplicationFirewallPolicyLink :
Backends                         :
CustomHttpsProvisioningState     : Enabling
CustomHttpsProvisioningSubstate  : SubmittingDomainControlValidationRequest
CertificateSource                : AzureKeyVault
ProtocolType                     : ServerNameIndication
MinimumTlsVersion                : 1.0
Vault                            :
SecretName                       :
SecretVersion                    :
CertificateType                  :
ResourceState                    : Enabled
Id                               : /subscriptions/{guid}/resourcegroups/resourcegroup1
                                   /providers/Microsoft.Network/frontdoors/frontdoor1/frontendendpoints/frontendpointname1-custom-xyz
Name                             : frontendpointname1-custom-xyz
Type                             : Microsoft.Network/frontdoors/frontendendpoints
```

<span data-ttu-id="45fed-117">Habilitar HTTPS para um domínio personalizado "frontendpointname1-custom-xyz" que faz parte do "frontdoor1" da Porta da Frente no grupo de recursos "resourcegroup1" usando o certificado gerenciado porta da frente.</span><span class="sxs-lookup"><span data-stu-id="45fed-117">Enable HTTPS for a custom domain "frontendpointname1-custom-xyz" that is part of Front Door "frontdoor1" in resource group "resourcegroup1" using Front Door managed certificate.</span></span>

### <span data-ttu-id="45fed-118">Exemplo 3: Habilitar HTTPS para um domínio personalizado com o objeto PSFrontendEndpoint usando o certificado gerenciado porta da frente.</span><span class="sxs-lookup"><span data-stu-id="45fed-118">Example 3: Enable HTTPS for a custom domain with PSFrontendEndpoint object using Front Door managed certificate.</span></span>
```powershell
PS C:\> Get-AzFrontDoorFrontendEndpoint -ResourceGroupName "resourcegroup1" -FrontDoorName "frontdoor1" -Name "frontendpointname1-custom-xyz" | Enable-AzFrontDoorCustomDomainHttps 


HostName                         : frontendpointname1.custom.xyz
SessionAffinityEnabledState      : Disabled
SessionAffinityTtlSeconds        : 0
WebApplicationFirewallPolicyLink :
Backends                         :
CustomHttpsProvisioningState     : Enabling
CustomHttpsProvisioningSubstate  : SubmittingDomainControlValidationRequest
CertificateSource                : FrontDoor
ProtocolType                     : ServerNameIndication
MinimumTlsVersion                : 1.2
Vault                            :
SecretName                       :
SecretVersion                    :
CertificateType                  :
ResourceState                    : Enabled
Id                               : /subscriptions/{guid}/resourcegroups/resourcegroup1
                                   /providers/Microsoft.Network/frontdoors/frontdoor1/frontendendpoints/frontendpointname1-custom-xyz
Name                             : frontendpointname1-custom-xyz
Type                             : Microsoft.Network/frontdoors/frontendendpoints
```

<span data-ttu-id="45fed-119">Habilitar HTTPS para um domínio personalizado com o objeto PSFrontendEndpoint usando o certificado gerenciado porta da frente.</span><span class="sxs-lookup"><span data-stu-id="45fed-119">Enable HTTPS for a custom domain with PSFrontendEndpoint object using Front Door managed certificate.</span></span>

### <span data-ttu-id="45fed-120">Exemplo 4: Habilitar HTTPS para um domínio personalizado com id de recurso usando o certificado gerenciado porta da frente.</span><span class="sxs-lookup"><span data-stu-id="45fed-120">Example 4: Enable HTTPS for a custom domain with resource id using Front Door managed certificate.</span></span>
```powershell
PS C:\> Enable-AzFrontDoorCustomDomainHttps -ResourceId $resourceId


HostName                         : frontendpointname1.custom.xyz
SessionAffinityEnabledState      : Disabled
SessionAffinityTtlSeconds        : 0
WebApplicationFirewallPolicyLink :
Backends                         :
CustomHttpsProvisioningState     : Enabling
CustomHttpsProvisioningSubstate  : SubmittingDomainControlValidationRequest
CertificateSource                : FrontDoor
ProtocolType                     : ServerNameIndication
MinimumTlsVersion                : 1.2
Vault                            :
SecretName                       :
SecretVersion                    :
CertificateType                  :
ResourceState                    : Enabled
Id                               : /subscriptions/{guid}/resourcegroups/resourcegroup1
                                   /providers/Microsoft.Network/frontdoors/frontdoor1/frontendendpoints/frontendpointname1-custom-xyz
Name                             : frontendpointname1-custom-xyz
Type                             : Microsoft.Network/frontdoors/frontendendpoints
```

<span data-ttu-id="45fed-121">Habilitar HTTPS para um domínio personalizado "frontendpointname1-custom-xyz" com id de recurso $resourceId usando o certificado gerenciado porta da frente.</span><span class="sxs-lookup"><span data-stu-id="45fed-121">Enable HTTPS for a custom domain "frontendpointname1-custom-xyz" with resource id $resourceId using Front Door managed certificate.</span></span>

## <span data-ttu-id="45fed-122">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="45fed-122">PARAMETERS</span></span>

### <span data-ttu-id="45fed-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45fed-123">-DefaultProfile</span></span>
<span data-ttu-id="45fed-124">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="45fed-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="45fed-125">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="45fed-125">-FrontDoorName</span></span>
<span data-ttu-id="45fed-126">O nome da Porta da Frente.</span><span class="sxs-lookup"><span data-stu-id="45fed-126">The name of the Front Door.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByFieldsWithVaultParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45fed-127">-FrontendEndpointName</span><span class="sxs-lookup"><span data-stu-id="45fed-127">-FrontendEndpointName</span></span>
<span data-ttu-id="45fed-128">Nome do ponto de extremidade front-end.</span><span class="sxs-lookup"><span data-stu-id="45fed-128">Frontend endpoint name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByFieldsWithVaultParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45fed-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="45fed-129">-InputObject</span></span>
<span data-ttu-id="45fed-130">O objeto de ponto de extremidade Frontend a ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="45fed-130">The Frontend endpoint object to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint
Parameter Sets: ByObjectParameterSet, ByObjectWithVaultParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="45fed-131">-MinimumTlsVersion</span><span class="sxs-lookup"><span data-stu-id="45fed-131">-MinimumTlsVersion</span></span>
<span data-ttu-id="45fed-132">A versão TLS mínima necessária dos clientes para estabelecer um handshake SSL com o Front Door.</span><span class="sxs-lookup"><span data-stu-id="45fed-132">The minimum TLS version required from the clients to establish an SSL handshake with Front Door.</span></span>

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

### <span data-ttu-id="45fed-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45fed-133">-ResourceGroupName</span></span>
<span data-ttu-id="45fed-134">O grupo de recursos ao qual a Porta da Frente pertence.</span><span class="sxs-lookup"><span data-stu-id="45fed-134">The resource group to which the Front Door belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByFieldsWithVaultParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45fed-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="45fed-135">-ResourceId</span></span>
<span data-ttu-id="45fed-136">ID do recurso do ponto de extremidade da Porta da Frente para habilitar https</span><span class="sxs-lookup"><span data-stu-id="45fed-136">Resource Id of the Front Door endpoint to enable https</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet, ByResourceIdWithVaultParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45fed-137">-SecretName</span><span class="sxs-lookup"><span data-stu-id="45fed-137">-SecretName</span></span>
<span data-ttu-id="45fed-138">O nome do segredo do Cofre de Chaves que representa o certificado completo PFX</span><span class="sxs-lookup"><span data-stu-id="45fed-138">The name of the Key Vault secret representing the full certificate PFX</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsWithVaultParameterSet, ByResourceIdWithVaultParameterSet, ByObjectWithVaultParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45fed-139">-SecretVersion</span><span class="sxs-lookup"><span data-stu-id="45fed-139">-SecretVersion</span></span>
<span data-ttu-id="45fed-140">A versão do segredo do Cofre de Chaves que representa o certificado completo PFX</span><span class="sxs-lookup"><span data-stu-id="45fed-140">The version of the Key Vault secret representing the full certificate PFX</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsWithVaultParameterSet, ByResourceIdWithVaultParameterSet, ByObjectWithVaultParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45fed-141">-VaultId</span><span class="sxs-lookup"><span data-stu-id="45fed-141">-VaultId</span></span>
<span data-ttu-id="45fed-142">A ID do Cofre de Chaves que contém o certificado SSL</span><span class="sxs-lookup"><span data-stu-id="45fed-142">The Key Vault id containing the SSL certificate</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsWithVaultParameterSet, ByResourceIdWithVaultParameterSet, ByObjectWithVaultParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45fed-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="45fed-143">-Confirm</span></span>
<span data-ttu-id="45fed-144">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="45fed-144">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45fed-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="45fed-145">-WhatIf</span></span>
<span data-ttu-id="45fed-146">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="45fed-146">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="45fed-147">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="45fed-147">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45fed-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45fed-148">CommonParameters</span></span>
<span data-ttu-id="45fed-149">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45fed-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45fed-150">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="45fed-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45fed-151">INPUTS</span><span class="sxs-lookup"><span data-stu-id="45fed-151">INPUTS</span></span>

### <span data-ttu-id="45fed-152">System.String</span><span class="sxs-lookup"><span data-stu-id="45fed-152">System.String</span></span>
## <span data-ttu-id="45fed-153">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="45fed-153">OUTPUTS</span></span>

### <span data-ttu-id="45fed-154">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="45fed-154">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint</span></span>
## <span data-ttu-id="45fed-155">NOTES</span><span class="sxs-lookup"><span data-stu-id="45fed-155">NOTES</span></span>

## <span data-ttu-id="45fed-156">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="45fed-156">RELATED LINKS</span></span>

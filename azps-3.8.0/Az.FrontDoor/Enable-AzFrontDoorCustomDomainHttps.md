---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/enable-azfrontdoorcustomdomainhttps
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Enable-AzFrontDoorCustomDomainHttps.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Enable-AzFrontDoorCustomDomainHttps.md
ms.openlocfilehash: 0e189e997ad0c2c468126bfe9c6c2d9a8c87f0a5
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93777495"
---
# <span data-ttu-id="63e3f-101">Enable-AzFrontDoorCustomDomainHttps</span><span class="sxs-lookup"><span data-stu-id="63e3f-101">Enable-AzFrontDoorCustomDomainHttps</span></span>

## <span data-ttu-id="63e3f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="63e3f-102">SYNOPSIS</span></span>
<span data-ttu-id="63e3f-103">Habilite o HTTPS para um domínio personalizado usando o certificado gerenciado de front door ou usando o próprio certificado do cofre de chaves do Azure.</span><span class="sxs-lookup"><span data-stu-id="63e3f-103">Enable HTTPS for a custom domain using Front Door managed certificate or using own certificate from Azure Key Vault.</span></span>

## <span data-ttu-id="63e3f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="63e3f-104">SYNTAX</span></span>

### <span data-ttu-id="63e3f-105">ByFieldsParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="63e3f-105">ByFieldsParameterSet (Default)</span></span>
```
Enable-AzFrontDoorCustomDomainHttps -ResourceGroupName <String> -FrontDoorName <String>
 -FrontendEndpointName <String> [-MinimumTlsVersion <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="63e3f-106">ByFieldsWithVaultParameterSet</span><span class="sxs-lookup"><span data-stu-id="63e3f-106">ByFieldsWithVaultParameterSet</span></span>
```
Enable-AzFrontDoorCustomDomainHttps -ResourceGroupName <String> -FrontDoorName <String>
 -FrontendEndpointName <String> -VaultId <String> -SecretName <String> -SecretVersion <String>
 [-MinimumTlsVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="63e3f-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="63e3f-107">ByResourceIdParameterSet</span></span>
```
Enable-AzFrontDoorCustomDomainHttps -ResourceId <String> [-MinimumTlsVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="63e3f-108">ByResourceIdWithVaultParameterSet</span><span class="sxs-lookup"><span data-stu-id="63e3f-108">ByResourceIdWithVaultParameterSet</span></span>
```
Enable-AzFrontDoorCustomDomainHttps -ResourceId <String> -VaultId <String> -SecretName <String>
 -SecretVersion <String> [-MinimumTlsVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="63e3f-109">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="63e3f-109">ByObjectParameterSet</span></span>
```
Enable-AzFrontDoorCustomDomainHttps -InputObject <PSFrontendEndpoint> [-MinimumTlsVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="63e3f-110">ByObjectWithVaultParameterSet</span><span class="sxs-lookup"><span data-stu-id="63e3f-110">ByObjectWithVaultParameterSet</span></span>
```
Enable-AzFrontDoorCustomDomainHttps -InputObject <PSFrontendEndpoint> -VaultId <String> -SecretName <String>
 -SecretVersion <String> [-MinimumTlsVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="63e3f-111">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="63e3f-111">DESCRIPTION</span></span>
<span data-ttu-id="63e3f-112">O **Enable-AzFrontDoorCustomDomainHttps** habilita HTTPS para um domínio personalizado.</span><span class="sxs-lookup"><span data-stu-id="63e3f-112">The **Enable-AzFrontDoorCustomDomainHttps** enables HTTPS for a custom domain.</span></span>

## <span data-ttu-id="63e3f-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="63e3f-113">EXAMPLES</span></span>

### <span data-ttu-id="63e3f-114">Exemplo 1: habilitar HTTPS para um domínio personalizado com FrontDoorName e ResourceGroupName usando o certificado gerenciado de front door.</span><span class="sxs-lookup"><span data-stu-id="63e3f-114">Example 1: Enable HTTPS for a custom domain with FrontDoorName and ResourceGroupName using Front Door managed certificate.</span></span>
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

<span data-ttu-id="63e3f-115">Habilite o HTTPS para um domínio personalizado "frontendpointname1-Custom-XYZ" que faz parte da porta frontal "frontdoor1" no grupo de recursos "resourcegroup1" usando o certificado gerenciado pela porta frontal.</span><span class="sxs-lookup"><span data-stu-id="63e3f-115">Enable HTTPS for a custom domain "frontendpointname1-custom-xyz" that is part of Front Door "frontdoor1" in resource group "resourcegroup1" using Front Door managed certificate.</span></span>

### <span data-ttu-id="63e3f-116">Exemplo 2: habilitar HTTPS para um domínio personalizado com FrontDoorName e ResourceGroupName usando o próprio certificado no cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="63e3f-116">Example 2: Enable HTTPS for a custom domain with FrontDoorName and ResourceGroupName using own certificate in Key Vault.</span></span>
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

<span data-ttu-id="63e3f-117">Habilite o HTTPS para um domínio personalizado "frontendpointname1-Custom-XYZ" que faz parte da porta frontal "frontdoor1" no grupo de recursos "resourcegroup1" usando o certificado gerenciado pela porta frontal.</span><span class="sxs-lookup"><span data-stu-id="63e3f-117">Enable HTTPS for a custom domain "frontendpointname1-custom-xyz" that is part of Front Door "frontdoor1" in resource group "resourcegroup1" using Front Door managed certificate.</span></span>

### <span data-ttu-id="63e3f-118">Exemplo 3: habilitar HTTPS para um domínio personalizado com objeto PSFrontendEndpoint usando o certificado gerenciado pela porta frontal.</span><span class="sxs-lookup"><span data-stu-id="63e3f-118">Example 3: Enable HTTPS for a custom domain with PSFrontendEndpoint object using Front Door managed certificate.</span></span>
```powershell
PS C:\> Get-AzFrontDoorFrontendEndpoint -ResourceGroupName "resourcegroup1" -FrontDoorName "frontdoor1" -FrontendEndpointName "frontendpointname1-custom-xyz" | Enable-AzFrontDoorCustomDomainHttps 


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

<span data-ttu-id="63e3f-119">Habilite HTTPS para um domínio personalizado com objeto PSFrontendEndpoint usando o certificado gerenciado de front door.</span><span class="sxs-lookup"><span data-stu-id="63e3f-119">Enable HTTPS for a custom domain with PSFrontendEndpoint object using Front Door managed certificate.</span></span>

### <span data-ttu-id="63e3f-120">Exemplo 4: habilitar HTTPS para um domínio personalizado com ID de recurso usando o certificado gerenciado pela porta frontal.</span><span class="sxs-lookup"><span data-stu-id="63e3f-120">Example 4: Enable HTTPS for a custom domain with resource id using Front Door managed certificate.</span></span>
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

<span data-ttu-id="63e3f-121">Habilite o HTTPS para um domínio personalizado "frontendpointname1-Custom-XYZ" com a ID do recurso $resourceId usando o certificado gerenciado de front door.</span><span class="sxs-lookup"><span data-stu-id="63e3f-121">Enable HTTPS for a custom domain "frontendpointname1-custom-xyz" with resource id $resourceId using Front Door managed certificate.</span></span>

## <span data-ttu-id="63e3f-122">OS</span><span class="sxs-lookup"><span data-stu-id="63e3f-122">PARAMETERS</span></span>

### <span data-ttu-id="63e3f-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63e3f-123">-DefaultProfile</span></span>
<span data-ttu-id="63e3f-124">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="63e3f-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="63e3f-125">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="63e3f-125">-FrontDoorName</span></span>
<span data-ttu-id="63e3f-126">O nome da porta frontal.</span><span class="sxs-lookup"><span data-stu-id="63e3f-126">The name of the Front Door.</span></span>

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

### <span data-ttu-id="63e3f-127">-FrontendEndpointName</span><span class="sxs-lookup"><span data-stu-id="63e3f-127">-FrontendEndpointName</span></span>
<span data-ttu-id="63e3f-128">Nome do ponto de extremidade front-end.</span><span class="sxs-lookup"><span data-stu-id="63e3f-128">Frontend endpoint name.</span></span>

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

### <span data-ttu-id="63e3f-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="63e3f-129">-InputObject</span></span>
<span data-ttu-id="63e3f-130">O objeto de ponto de extremidade de front-end a ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="63e3f-130">The Frontend endpoint object to update.</span></span>

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

### <span data-ttu-id="63e3f-131">-MinimumTlsVersion</span><span class="sxs-lookup"><span data-stu-id="63e3f-131">-MinimumTlsVersion</span></span>
<span data-ttu-id="63e3f-132">A versão mínima do TLS necessária dos clientes para estabelecer um handshake SSL com a porta frontal.</span><span class="sxs-lookup"><span data-stu-id="63e3f-132">The minimum TLS version required from the clients to establish an SSL handshake with Front Door.</span></span>

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

### <span data-ttu-id="63e3f-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63e3f-133">-ResourceGroupName</span></span>
<span data-ttu-id="63e3f-134">O grupo de recursos ao qual a porta frontal pertence.</span><span class="sxs-lookup"><span data-stu-id="63e3f-134">The resource group to which the Front Door belongs.</span></span>

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

### <span data-ttu-id="63e3f-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="63e3f-135">-ResourceId</span></span>
<span data-ttu-id="63e3f-136">ID do recurso do ponto de extremidade da porta frontal para habilitar https</span><span class="sxs-lookup"><span data-stu-id="63e3f-136">Resource Id of the Front Door endpoint to enable https</span></span>

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

### <span data-ttu-id="63e3f-137">-Secretname</span><span class="sxs-lookup"><span data-stu-id="63e3f-137">-SecretName</span></span>
<span data-ttu-id="63e3f-138">O nome do segredo do cofre de chaves que representa o PFX de certificado completo</span><span class="sxs-lookup"><span data-stu-id="63e3f-138">The name of the Key Vault secret representing the full certificate PFX</span></span>

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

### <span data-ttu-id="63e3f-139">-SecretVersion</span><span class="sxs-lookup"><span data-stu-id="63e3f-139">-SecretVersion</span></span>
<span data-ttu-id="63e3f-140">A versão do segredo do cofre de chaves que representa o PFX de certificado completo</span><span class="sxs-lookup"><span data-stu-id="63e3f-140">The version of the Key Vault secret representing the full certificate PFX</span></span>

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

### <span data-ttu-id="63e3f-141">-Cofreid</span><span class="sxs-lookup"><span data-stu-id="63e3f-141">-VaultId</span></span>
<span data-ttu-id="63e3f-142">A ID do cofre de chaves que contém o certificado SSL</span><span class="sxs-lookup"><span data-stu-id="63e3f-142">The Key Vault id containing the SSL certificate</span></span>

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

### <span data-ttu-id="63e3f-143">-Confirme</span><span class="sxs-lookup"><span data-stu-id="63e3f-143">-Confirm</span></span>
<span data-ttu-id="63e3f-144">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="63e3f-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="63e3f-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="63e3f-145">-WhatIf</span></span>
<span data-ttu-id="63e3f-146">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="63e3f-146">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="63e3f-147">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="63e3f-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="63e3f-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63e3f-148">CommonParameters</span></span>
<span data-ttu-id="63e3f-149">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="63e3f-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63e3f-150">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="63e3f-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63e3f-151">SENSORES</span><span class="sxs-lookup"><span data-stu-id="63e3f-151">INPUTS</span></span>

### <span data-ttu-id="63e3f-152">System. String</span><span class="sxs-lookup"><span data-stu-id="63e3f-152">System.String</span></span>
## <span data-ttu-id="63e3f-153">EXIBE</span><span class="sxs-lookup"><span data-stu-id="63e3f-153">OUTPUTS</span></span>

### <span data-ttu-id="63e3f-154">Microsoft. Azure. Commands. FrontDoor. Models. PSFrontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="63e3f-154">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint</span></span>
## <span data-ttu-id="63e3f-155">INFORMA</span><span class="sxs-lookup"><span data-stu-id="63e3f-155">NOTES</span></span>

## <span data-ttu-id="63e3f-156">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="63e3f-156">RELATED LINKS</span></span>

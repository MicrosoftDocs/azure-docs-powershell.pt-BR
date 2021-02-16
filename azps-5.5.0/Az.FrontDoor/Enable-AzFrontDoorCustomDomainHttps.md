---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/enable-azfrontdoorcustomdomainhttps
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Enable-AzFrontDoorCustomDomainHttps.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Enable-AzFrontDoorCustomDomainHttps.md
ms.openlocfilehash: 6d3eb8d4cbeb2a8c40e3fc6fbf0f54e8973e8f79
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100126965"
---
# <span data-ttu-id="bdefe-101">Enable-AzFrontDoorCustomDomainHttps</span><span class="sxs-lookup"><span data-stu-id="bdefe-101">Enable-AzFrontDoorCustomDomainHttps</span></span>

## <span data-ttu-id="bdefe-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bdefe-102">SYNOPSIS</span></span>
<span data-ttu-id="bdefe-103">Habilita o HTTPS para um domínio personalizado usando certificado gerenciado pelo Front Door ou usando o próprio certificado do Cofre de Teclas do Azure.</span><span class="sxs-lookup"><span data-stu-id="bdefe-103">Enable HTTPS for a custom domain using Front Door managed certificate or using own certificate from Azure Key Vault.</span></span>

## <span data-ttu-id="bdefe-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bdefe-104">SYNTAX</span></span>

### <span data-ttu-id="bdefe-105">ByFieldsParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="bdefe-105">ByFieldsParameterSet (Default)</span></span>
```
Enable-AzFrontDoorCustomDomainHttps -ResourceGroupName <String> -FrontDoorName <String>
 -FrontendEndpointName <String> [-MinimumTlsVersion <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bdefe-106">ByFieldsWithVaultParameterSet</span><span class="sxs-lookup"><span data-stu-id="bdefe-106">ByFieldsWithVaultParameterSet</span></span>
```
Enable-AzFrontDoorCustomDomainHttps -ResourceGroupName <String> -FrontDoorName <String>
 -FrontendEndpointName <String> -VaultId <String> -SecretName <String> -SecretVersion <String>
 [-MinimumTlsVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bdefe-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bdefe-107">ByResourceIdParameterSet</span></span>
```
Enable-AzFrontDoorCustomDomainHttps -ResourceId <String> [-MinimumTlsVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bdefe-108">ByResourceIdWithVaultParameterSet</span><span class="sxs-lookup"><span data-stu-id="bdefe-108">ByResourceIdWithVaultParameterSet</span></span>
```
Enable-AzFrontDoorCustomDomainHttps -ResourceId <String> -VaultId <String> -SecretName <String>
 -SecretVersion <String> [-MinimumTlsVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bdefe-109">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bdefe-109">ByObjectParameterSet</span></span>
```
Enable-AzFrontDoorCustomDomainHttps -InputObject <PSFrontendEndpoint> [-MinimumTlsVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bdefe-110">ByObjectWithVaultParameterSet</span><span class="sxs-lookup"><span data-stu-id="bdefe-110">ByObjectWithVaultParameterSet</span></span>
```
Enable-AzFrontDoorCustomDomainHttps -InputObject <PSFrontendEndpoint> -VaultId <String> -SecretName <String>
 -SecretVersion <String> [-MinimumTlsVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bdefe-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="bdefe-111">DESCRIPTION</span></span>
<span data-ttu-id="bdefe-112">O **Enable-AzFrontDoorCustomDomainHttps** habilita HTTPS para um domínio personalizado.</span><span class="sxs-lookup"><span data-stu-id="bdefe-112">The **Enable-AzFrontDoorCustomDomainHttps** enables HTTPS for a custom domain.</span></span>

## <span data-ttu-id="bdefe-113">Exemplos</span><span class="sxs-lookup"><span data-stu-id="bdefe-113">EXAMPLES</span></span>

### <span data-ttu-id="bdefe-114">Exemplo 1: Habilitar HTTPS para um domínio personalizado com o FrontDoorName e o ResourceGroupName usando certificado gerenciado pelo Front Door.</span><span class="sxs-lookup"><span data-stu-id="bdefe-114">Example 1: Enable HTTPS for a custom domain with FrontDoorName and ResourceGroupName using Front Door managed certificate.</span></span>
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

<span data-ttu-id="bdefe-115">Habilita o HTTPS para um domínio personalizado "frontendpointname1-custom-xyz" que faz parte da "frontdoor1" do grupo de recursos "resourcegroup1" usando o certificado gerenciado pela Front Door.</span><span class="sxs-lookup"><span data-stu-id="bdefe-115">Enable HTTPS for a custom domain "frontendpointname1-custom-xyz" that is part of Front Door "frontdoor1" in resource group "resourcegroup1" using Front Door managed certificate.</span></span>

### <span data-ttu-id="bdefe-116">Exemplo 2: Habilitar HTTPS para um domínio personalizado com o FrontDoorName e o ResourceGroupName usando o próprio certificado no Cofre de Teclas.</span><span class="sxs-lookup"><span data-stu-id="bdefe-116">Example 2: Enable HTTPS for a custom domain with FrontDoorName and ResourceGroupName using own certificate in Key Vault.</span></span>
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

<span data-ttu-id="bdefe-117">Habilita o HTTPS para um domínio personalizado "frontendpointname1-custom-xyz" que faz parte do "frontdoor1" do grupo de recursos "resourcegroup1" usando o certificado gerenciado pela Front Door.</span><span class="sxs-lookup"><span data-stu-id="bdefe-117">Enable HTTPS for a custom domain "frontendpointname1-custom-xyz" that is part of Front Door "frontdoor1" in resource group "resourcegroup1" using Front Door managed certificate.</span></span>

### <span data-ttu-id="bdefe-118">Exemplo 3: Habilitar HTTPS para um domínio personalizado com objeto PSFrontendEndpoint usando certificado gerenciado pela Front Door.</span><span class="sxs-lookup"><span data-stu-id="bdefe-118">Example 3: Enable HTTPS for a custom domain with PSFrontendEndpoint object using Front Door managed certificate.</span></span>
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

<span data-ttu-id="bdefe-119">Habilita o HTTPS para um domínio personalizado com o objeto PSFrontendEndpoint usando certificado gerenciado pelo Front Door.</span><span class="sxs-lookup"><span data-stu-id="bdefe-119">Enable HTTPS for a custom domain with PSFrontendEndpoint object using Front Door managed certificate.</span></span>

### <span data-ttu-id="bdefe-120">Exemplo 4: Habilitar HTTPS para um domínio personalizado com id de recurso usando certificado gerenciado pelo Front Door.</span><span class="sxs-lookup"><span data-stu-id="bdefe-120">Example 4: Enable HTTPS for a custom domain with resource id using Front Door managed certificate.</span></span>
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

<span data-ttu-id="bdefe-121">Habilita o HTTPS para um domínio personalizado "nomedo frontendpoint1-custom-xyz" com a ID do recurso $resourceId usando certificado gerenciado pelo Front Door.</span><span class="sxs-lookup"><span data-stu-id="bdefe-121">Enable HTTPS for a custom domain "frontendpointname1-custom-xyz" with resource id $resourceId using Front Door managed certificate.</span></span>

## <span data-ttu-id="bdefe-122">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bdefe-122">PARAMETERS</span></span>

### <span data-ttu-id="bdefe-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bdefe-123">-DefaultProfile</span></span>
<span data-ttu-id="bdefe-124">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bdefe-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bdefe-125">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="bdefe-125">-FrontDoorName</span></span>
<span data-ttu-id="bdefe-126">O nome da porta da frente.</span><span class="sxs-lookup"><span data-stu-id="bdefe-126">The name of the Front Door.</span></span>

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

### <span data-ttu-id="bdefe-127">-FrontendEndpointName</span><span class="sxs-lookup"><span data-stu-id="bdefe-127">-FrontendEndpointName</span></span>
<span data-ttu-id="bdefe-128">Nome do ponto de extremidade frontend.</span><span class="sxs-lookup"><span data-stu-id="bdefe-128">Frontend endpoint name.</span></span>

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

### <span data-ttu-id="bdefe-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bdefe-129">-InputObject</span></span>
<span data-ttu-id="bdefe-130">O objeto do ponto de extremidade Frontend a ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="bdefe-130">The Frontend endpoint object to update.</span></span>

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

### <span data-ttu-id="bdefe-131">-MinimumTlsVersion</span><span class="sxs-lookup"><span data-stu-id="bdefe-131">-MinimumTlsVersion</span></span>
<span data-ttu-id="bdefe-132">A versão TLS mínima necessária para os clientes estabelecerem um handshake SSL com o Front Door.</span><span class="sxs-lookup"><span data-stu-id="bdefe-132">The minimum TLS version required from the clients to establish an SSL handshake with Front Door.</span></span>

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

### <span data-ttu-id="bdefe-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bdefe-133">-ResourceGroupName</span></span>
<span data-ttu-id="bdefe-134">O grupo de recursos ao qual a Porta da Frente pertence.</span><span class="sxs-lookup"><span data-stu-id="bdefe-134">The resource group to which the Front Door belongs.</span></span>

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

### <span data-ttu-id="bdefe-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bdefe-135">-ResourceId</span></span>
<span data-ttu-id="bdefe-136">ID do Recurso do ponto de extremidade Porta da Frente para habilitar https</span><span class="sxs-lookup"><span data-stu-id="bdefe-136">Resource Id of the Front Door endpoint to enable https</span></span>

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

### <span data-ttu-id="bdefe-137">-SecretName</span><span class="sxs-lookup"><span data-stu-id="bdefe-137">-SecretName</span></span>
<span data-ttu-id="bdefe-138">O nome do segredo do Cofre de Chaves representando o certificado PFX completo</span><span class="sxs-lookup"><span data-stu-id="bdefe-138">The name of the Key Vault secret representing the full certificate PFX</span></span>

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

### <span data-ttu-id="bdefe-139">-SecretVersion</span><span class="sxs-lookup"><span data-stu-id="bdefe-139">-SecretVersion</span></span>
<span data-ttu-id="bdefe-140">A versão do segredo do Cofre de Chaves que representa o certificado PFX completo</span><span class="sxs-lookup"><span data-stu-id="bdefe-140">The version of the Key Vault secret representing the full certificate PFX</span></span>

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

### <span data-ttu-id="bdefe-141">-VaultId</span><span class="sxs-lookup"><span data-stu-id="bdefe-141">-VaultId</span></span>
<span data-ttu-id="bdefe-142">A ID do Cofre de Teclas que contém o certificado SSL</span><span class="sxs-lookup"><span data-stu-id="bdefe-142">The Key Vault id containing the SSL certificate</span></span>

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

### <span data-ttu-id="bdefe-143">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="bdefe-143">-Confirm</span></span>
<span data-ttu-id="bdefe-144">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bdefe-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bdefe-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bdefe-145">-WhatIf</span></span>
<span data-ttu-id="bdefe-146">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="bdefe-146">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bdefe-147">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="bdefe-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bdefe-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bdefe-148">CommonParameters</span></span>
<span data-ttu-id="bdefe-149">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bdefe-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bdefe-150">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bdefe-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bdefe-151">Entradas</span><span class="sxs-lookup"><span data-stu-id="bdefe-151">INPUTS</span></span>

### <span data-ttu-id="bdefe-152">System.String</span><span class="sxs-lookup"><span data-stu-id="bdefe-152">System.String</span></span>
## <span data-ttu-id="bdefe-153">Saídas</span><span class="sxs-lookup"><span data-stu-id="bdefe-153">OUTPUTS</span></span>

### <span data-ttu-id="bdefe-154">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="bdefe-154">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint</span></span>
## <span data-ttu-id="bdefe-155">Notas</span><span class="sxs-lookup"><span data-stu-id="bdefe-155">NOTES</span></span>

## <span data-ttu-id="bdefe-156">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bdefe-156">RELATED LINKS</span></span>

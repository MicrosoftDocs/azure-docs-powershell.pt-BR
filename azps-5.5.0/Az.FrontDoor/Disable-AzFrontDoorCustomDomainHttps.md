---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/disable-azfrontdoorcustomdomainhttps
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Disable-AzFrontDoorCustomDomainHttps.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Disable-AzFrontDoorCustomDomainHttps.md
ms.openlocfilehash: 65c9bca6eb678ff3f3cb0a61d815f8415c715e43
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116804"
---
# <span data-ttu-id="fdad9-101">Disable-AzFrontDoorCustomDomainHttps</span><span class="sxs-lookup"><span data-stu-id="fdad9-101">Disable-AzFrontDoorCustomDomainHttps</span></span>

## <span data-ttu-id="fdad9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fdad9-102">SYNOPSIS</span></span>
<span data-ttu-id="fdad9-103">Desabilitar HTTPS para um domínio personalizado</span><span class="sxs-lookup"><span data-stu-id="fdad9-103">Disable HTTPS for a custom domain</span></span>

## <span data-ttu-id="fdad9-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fdad9-104">SYNTAX</span></span>

### <span data-ttu-id="fdad9-105">ByFieldsParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="fdad9-105">ByFieldsParameterSet (Default)</span></span>
```
Disable-AzFrontDoorCustomDomainHttps -ResourceGroupName <String> -FrontDoorName <String>
 -FrontendEndpointName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fdad9-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fdad9-106">ByResourceIdParameterSet</span></span>
```
Disable-AzFrontDoorCustomDomainHttps -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fdad9-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fdad9-107">ByObjectParameterSet</span></span>
```
Disable-AzFrontDoorCustomDomainHttps -InputObject <PSFrontendEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fdad9-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="fdad9-108">DESCRIPTION</span></span>
<span data-ttu-id="fdad9-109">O **Disable-AzFrontDoorCustomDomainHttps** desabilita HTTPS para um domínio personalizado.</span><span class="sxs-lookup"><span data-stu-id="fdad9-109">The **Disable-AzFrontDoorCustomDomainHttps** disables HTTPS for a custom domain.</span></span>

## <span data-ttu-id="fdad9-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="fdad9-110">EXAMPLES</span></span>

### <span data-ttu-id="fdad9-111">Exemplo 1: Desabilitar HTTPS para um domínio personalizado com o FrontDoorName e o ResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="fdad9-111">Example 1: Disable HTTPS for a custom domain with FrontDoorName and ResourceGroupName.</span></span>
```powershell
PS C:\> Disable-AzFrontDoorCustomDomainHttps -ResourceGroupName "resourcegroup1" -FrontDoorName "frontdoor1" -FrontendEndpointName "frontendpointname1-custom-xyz"

HostName                         : frontendpointname1.custom.xyz
SessionAffinityEnabledState      : Disabled
SessionAffinityTtlSeconds        : 0
WebApplicationFirewallPolicyLink :
Backends                         :
CustomHttpsProvisioningState     : Disabling
CustomHttpsProvisioningSubstate  : DeletingCertificate
CertificateSource                : FrontDoor
ProtocolType                     : ServerNameIndication
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

<span data-ttu-id="fdad9-112">Desabilite HTTPS para um domínio personalizado "frontendpointname1-custom-xyz" com o FrontDoorName como "frontdoor1" e ResourceGroupName como "resourcegroup1".</span><span class="sxs-lookup"><span data-stu-id="fdad9-112">Disable HTTPS for a custom domain "frontendpointname1-custom-xyz" with FrontDoorName as "frontdoor1" and ResourceGroupName as "resourcegroup1".</span></span>

### <span data-ttu-id="fdad9-113">Exemplo 2: Desabilitar HTTPS para um domínio personalizado com objeto PSFrontendEndpoint.</span><span class="sxs-lookup"><span data-stu-id="fdad9-113">Example 2: Disable HTTPS for a custom domain with PSFrontendEndpoint object.</span></span>
```powershell
PS C:\> Get-AzFrontDoorFrontendEndpoint -ResourceGroupName "resourcegroup1" -FrontDoorName "frontdoor1" -FrontendEndpointName "frontendpointname1-custom-xyz" | Disable-AzFrontDoorCustomDomainHttps -InputObject $frontendEndpointObj 

HostName                         : frontendpointname1.custom.xyz
SessionAffinityEnabledState      : Disabled
SessionAffinityTtlSeconds        : 0
WebApplicationFirewallPolicyLink :
Backends                         :
CustomHttpsProvisioningState     : Disabling
CustomHttpsProvisioningSubstate  : DeletingCertificate
CertificateSource                : FrontDoor
ProtocolType                     : ServerNameIndication
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

<span data-ttu-id="fdad9-114">Desabilitar HTTPS para um domínio personalizado com o objeto PSFrontendEndpoint.</span><span class="sxs-lookup"><span data-stu-id="fdad9-114">Disable HTTPS for a custom domain with PSFrontendEndpoint object.</span></span>

### <span data-ttu-id="fdad9-115">Exemplo 3: Desabilitar HTTPS para um domínio personalizado com ResourceId.</span><span class="sxs-lookup"><span data-stu-id="fdad9-115">Example 3: Disable HTTPS for a custom domain with ResourceId.</span></span>
```powershell
PS C:\> Disable-AzFrontDoorCustomDomainHttps -ResourceId $resourceId 

HostName                         : frontendpointname1.custom.xyz
SessionAffinityEnabledState      : Disabled
SessionAffinityTtlSeconds        : 0
WebApplicationFirewallPolicyLink :
Backends                         :
CustomHttpsProvisioningState     : Disabling
CustomHttpsProvisioningSubstate  : DeletingCertificate
CertificateSource                : FrontDoor
ProtocolType                     : ServerNameIndication
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

<span data-ttu-id="fdad9-116">Desabilite HTTPS para um domínio personalizado "frontendpointname1-custom-xyz" com ResourceId como $resourceId.</span><span class="sxs-lookup"><span data-stu-id="fdad9-116">Disable HTTPS for a custom domain "frontendpointname1-custom-xyz" with ResourceId as $resourceId.</span></span>

## <span data-ttu-id="fdad9-117">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fdad9-117">PARAMETERS</span></span>

### <span data-ttu-id="fdad9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fdad9-118">-DefaultProfile</span></span>
<span data-ttu-id="fdad9-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fdad9-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fdad9-120">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="fdad9-120">-FrontDoorName</span></span>
<span data-ttu-id="fdad9-121">O nome da porta da frente.</span><span class="sxs-lookup"><span data-stu-id="fdad9-121">The name of the Front Door.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fdad9-122">-FrontendEndpointName</span><span class="sxs-lookup"><span data-stu-id="fdad9-122">-FrontendEndpointName</span></span>
<span data-ttu-id="fdad9-123">Nome do ponto de extremidade frontend.</span><span class="sxs-lookup"><span data-stu-id="fdad9-123">Frontend endpoint name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fdad9-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fdad9-124">-InputObject</span></span>
<span data-ttu-id="fdad9-125">O objeto do ponto de extremidade Frontend a ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="fdad9-125">The Frontend endpoint object to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fdad9-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fdad9-126">-ResourceGroupName</span></span>
<span data-ttu-id="fdad9-127">O grupo de recursos ao qual a Porta da Frente pertence.</span><span class="sxs-lookup"><span data-stu-id="fdad9-127">The resource group to which the Front Door belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fdad9-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fdad9-128">-ResourceId</span></span>
<span data-ttu-id="fdad9-129">ID do recurso do ponto de extremidade Porta da Frente para desabilitar https</span><span class="sxs-lookup"><span data-stu-id="fdad9-129">Resource Id of the Front Door endpoint to disable https</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fdad9-130">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="fdad9-130">-Confirm</span></span>
<span data-ttu-id="fdad9-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fdad9-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fdad9-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fdad9-132">-WhatIf</span></span>
<span data-ttu-id="fdad9-133">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="fdad9-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fdad9-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="fdad9-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fdad9-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fdad9-135">CommonParameters</span></span>
<span data-ttu-id="fdad9-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fdad9-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fdad9-137">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fdad9-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fdad9-138">Entradas</span><span class="sxs-lookup"><span data-stu-id="fdad9-138">INPUTS</span></span>

### <span data-ttu-id="fdad9-139">System.String</span><span class="sxs-lookup"><span data-stu-id="fdad9-139">System.String</span></span>

## <span data-ttu-id="fdad9-140">Saídas</span><span class="sxs-lookup"><span data-stu-id="fdad9-140">OUTPUTS</span></span>

### <span data-ttu-id="fdad9-141">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="fdad9-141">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint</span></span>

## <span data-ttu-id="fdad9-142">Notas</span><span class="sxs-lookup"><span data-stu-id="fdad9-142">NOTES</span></span>

## <span data-ttu-id="fdad9-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fdad9-143">RELATED LINKS</span></span>

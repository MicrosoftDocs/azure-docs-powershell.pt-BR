---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6AB09621-488B-4A16-92D9-9C47EB87DA95
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azresourceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceProvider.md
ms.openlocfilehash: 0f7a05cd0cd711388973c3f823b1aee6aa9f6902
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94110974"
---
# <span data-ttu-id="91cd7-101">Get-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="91cd7-101">Get-AzResourceProvider</span></span>

## <span data-ttu-id="91cd7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="91cd7-102">SYNOPSIS</span></span>
<span data-ttu-id="91cd7-103">Obtém um provedor de recursos.</span><span class="sxs-lookup"><span data-stu-id="91cd7-103">Gets a resource provider.</span></span>

## <span data-ttu-id="91cd7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="91cd7-104">SYNTAX</span></span>

### <span data-ttu-id="91cd7-105">ListAvailable (padrão)</span><span class="sxs-lookup"><span data-stu-id="91cd7-105">ListAvailable (Default)</span></span>
```
Get-AzResourceProvider [-Location <String>] [-ListAvailable] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="91cd7-106">Indivíduo</span><span class="sxs-lookup"><span data-stu-id="91cd7-106">IndividualProvider</span></span>
```
Get-AzResourceProvider -ProviderNamespace <String[]> [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="91cd7-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="91cd7-107">DESCRIPTION</span></span>
<span data-ttu-id="91cd7-108">O cmdlet **Get-AzResourceProvider** Obtém um provedor de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="91cd7-108">The **Get-AzResourceProvider** cmdlet gets an Azure resource provider.</span></span>

## <span data-ttu-id="91cd7-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="91cd7-109">EXAMPLES</span></span>

### <span data-ttu-id="91cd7-110">Exemplo 1: obter todos os provedores de recursos registrados com a assinatura atual</span><span class="sxs-lookup"><span data-stu-id="91cd7-110">Example 1: Get all resource providers registered with the current subscription</span></span>

```powershell
PS C:\>Get-AzResourceProvider

ProviderNamespace : Microsoft.AppConfiguration
RegistrationState : Registered
ResourceTypes     : {configurationStores, configurationStores/eventGridFilters, checkNameAvailability, locations…}
Locations         : {West Central US, Central US, West US, East US…}

ProviderNamespace : Microsoft.KeyVault
RegistrationState : Registered
ResourceTypes     : {vaults, vaults/secrets, vaults/accessPolicies, operations…}
Locations         : {North Central US, East US, North Europe, West Europe…}

ProviderNamespace : Microsoft.Network
RegistrationState : Registered
ResourceTypes     : {virtualNetworks, publicIPAddresses, networkInterfaces, privateEndpoints…}
Locations         : {West US, East US, North Europe, West Europe…}

ProviderNamespace : Microsoft.Compute
RegistrationState : Registered
ResourceTypes     : {availabilitySets, virtualMachines, virtualMachines/extensions, virtualMachineScaleSets…}
Locations         : {East US, East US 2, West US, Central US…}

ProviderNamespace : Microsoft.Security
RegistrationState : Registered
ResourceTypes     : {operations, securityStatuses, tasks, regulatoryComplianceStandards…}
Locations         : {Central US, East US, West Europe, West Central US…}

ProviderNamespace : Microsoft.ResourceHealth
RegistrationState : Registered
ResourceTypes     : {availabilityStatuses, childAvailabilityStatuses, childResources, events…}
Locations         : {Australia Southeast}

ProviderNamespace : Microsoft.PolicyInsights
RegistrationState : Registered
ResourceTypes     : {policyEvents, policyStates, operations, asyncOperationResults…}
Locations         : {}

ProviderNamespace : Microsoft.Storage
RegistrationState : Registered
ResourceTypes     : {storageAccounts, operations, locations/asyncoperations, storageAccounts/listAccountSas…}
Locations         : {East US, East US 2, West US, West Europe…}

ProviderNamespace : Microsoft.Web
RegistrationState : Registered
ResourceTypes     : {publishingUsers, ishostnameavailable, validate, isusernameavailable…}
Locations         : {Central US, North Europe, West Europe, Southeast Asia…}

ProviderNamespace : Sendgrid.Email
RegistrationState : Registered
ResourceTypes     : {accounts, operations}
Locations         : {Australia East, Australia Southeast, Brazil South, Canada Central…}

ProviderNamespace : Microsoft.Authorization
RegistrationState : Registered
ResourceTypes     : {roleAssignments, roleDefinitions, classicAdministrators, permissions…}
Locations         : {}
...
```

<span data-ttu-id="91cd7-111">Esse comando obtém todos os provedores de recursos da assinatura.</span><span class="sxs-lookup"><span data-stu-id="91cd7-111">This command gets all the resource providers from the subscription.</span></span>

### <span data-ttu-id="91cd7-112">Exemplo 2: obter todos os detalhes do provedor de recursos de um determinado ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="91cd7-112">Example 2: Get all resource provider details from the given ProviderNamespace</span></span>

```powershell
PS C:\>Get-AzResourceProvider -ProviderNamespace Microsoft.Compute
ProviderNamespace : Microsoft.Compute
RegistrationState : Registered
ResourceTypes     : {availabilitySets}
Locations         : {East US, East US 2, West US, Central US…}

ProviderNamespace : Microsoft.Compute
RegistrationState : Registered
ResourceTypes     : {virtualMachines}
Locations         : {East US, East US 2, West US, Central US…}

ProviderNamespace : Microsoft.Compute
RegistrationState : Registered
ResourceTypes     : {virtualMachines/extensions}
Locations         : {East US, East US 2, West US, Central US…}

ProviderNamespace : Microsoft.Compute
RegistrationState : Registered
ResourceTypes     : {virtualMachineScaleSets}
Locations         : {East US, East US 2, West US, Central US…}

ProviderNamespace : Microsoft.Compute
RegistrationState : Registered
ResourceTypes     : {virtualMachineScaleSets/extensions}
Locations         : {East US, East US 2, West US, Central US…}

ProviderNamespace : Microsoft.Compute
RegistrationState : Registered
ResourceTypes     : {virtualMachineScaleSets/virtualMachines}
Locations         : {East US, East US 2, West US, Central US…}

ProviderNamespace : Microsoft.Compute
RegistrationState : Registered
ResourceTypes     : {virtualMachineScaleSets/networkInterfaces}
Locations         : {East US, East US 2, West US, Central US…}
...
```

<span data-ttu-id="91cd7-113">Esse comando obtém todos os provedores de recursos em "Microsoft. Compute".</span><span class="sxs-lookup"><span data-stu-id="91cd7-113">This command Gets all the resource providers under "Microsoft.Compute".</span></span>

### <span data-ttu-id="91cd7-114">Exemplo 3: obter todos os detalhes do provedor de recursos da matriz ProviderNamespace determinada</span><span class="sxs-lookup"><span data-stu-id="91cd7-114">Example 3: Get all resource provider details from the given ProviderNamespace array</span></span>

```powershell
PS C:\>Get-AzResourceProvider -ProviderNamespace Microsoft.Compute,Microsoft.Network
ProviderNamespace : Microsoft.Compute
RegistrationState : Registered
ResourceTypes     : {availabilitySets}
Locations         : {East US, East US 2, West US, Central US…}

ProviderNamespace : Microsoft.Compute
RegistrationState : Registered
ResourceTypes     : {virtualMachines}
Locations         : {East US, East US 2, West US, Central US…}

ProviderNamespace : Microsoft.Compute
RegistrationState : Registered
ResourceTypes     : {virtualMachines/extensions}
Locations         : {East US, East US 2, West US, Central US…}

ProviderNamespace : Microsoft.Compute
RegistrationState : Registered
ResourceTypes     : {virtualMachineScaleSets}
Locations         : {East US, East US 2, West US, Central US…}

ProviderNamespace : Microsoft.Compute
RegistrationState : Registered
ResourceTypes     : {virtualMachineScaleSets/extensions}
Locations         : {East US, East US 2, West US, Central US…}
...

ProviderNamespace : Microsoft.Network
RegistrationState : Registered
ResourceTypes     : {virtualNetworks}
Locations         : {West US, East US, North Europe, West Europe…}

ProviderNamespace : Microsoft.Network
RegistrationState : Registered
ResourceTypes     : {publicIPAddresses}
Locations         : {West US, East US, North Europe, West Europe…}

ProviderNamespace : Microsoft.Network
RegistrationState : Registered
ResourceTypes     : {networkInterfaces}
Locations         : {West US, East US, North Europe, West Europe…}

ProviderNamespace : Microsoft.Network
RegistrationState : Registered
ResourceTypes     : {privateEndpoints}
Locations         : {West US, East US, North Europe, West Europe…}

ProviderNamespace : Microsoft.Network
RegistrationState : Registered
ResourceTypes     : {privateEndpointRedirectMaps}
Locations         : {West US, East US, North Europe, West Europe…}

ProviderNamespace : Microsoft.Network
RegistrationState : Registered
ResourceTypes     : {loadBalancers}
Locations         : {West US, East US, North Europe, West Europe…}

ProviderNamespace : Microsoft.Network
RegistrationState : Registered
ResourceTypes     : {networkSecurityGroups}
Locations         : {West US, East US, North Europe, West Europe…}
...
```

<span data-ttu-id="91cd7-115">Esse comando obtém todos os provedores de recursos em "Microsoft. Compute" e "Microsoft. Network".</span><span class="sxs-lookup"><span data-stu-id="91cd7-115">This command Gets all the resource providers under "Microsoft.Compute" and "Microsoft.Network".</span></span>

## <span data-ttu-id="91cd7-116">OS</span><span class="sxs-lookup"><span data-stu-id="91cd7-116">PARAMETERS</span></span>

### <span data-ttu-id="91cd7-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="91cd7-117">-ApiVersion</span></span>
<span data-ttu-id="91cd7-118">Especifica a versão da API que é suportada pelo provedor de recursos.</span><span class="sxs-lookup"><span data-stu-id="91cd7-118">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="91cd7-119">Você pode especificar uma versão diferente da versão padrão.</span><span class="sxs-lookup"><span data-stu-id="91cd7-119">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="91cd7-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91cd7-120">-DefaultProfile</span></span>
<span data-ttu-id="91cd7-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="91cd7-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="91cd7-122">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="91cd7-122">-ListAvailable</span></span>
<span data-ttu-id="91cd7-123">Indica que essa operação obtém todos os provedores de recursos disponíveis.</span><span class="sxs-lookup"><span data-stu-id="91cd7-123">Indicates that this operation gets all available resource providers.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ListAvailable
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91cd7-124">-Local</span><span class="sxs-lookup"><span data-stu-id="91cd7-124">-Location</span></span>
<span data-ttu-id="91cd7-125">Especifica o local do provedor de recursos.</span><span class="sxs-lookup"><span data-stu-id="91cd7-125">Specifies the location of the resource provider.</span></span>

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

### <span data-ttu-id="91cd7-126">-Pre</span><span class="sxs-lookup"><span data-stu-id="91cd7-126">-Pre</span></span>
<span data-ttu-id="91cd7-127">Indica que esse cmdlet considera versões de API de pré-lançamento quando determina automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="91cd7-127">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="91cd7-128">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="91cd7-128">-ProviderNamespace</span></span>
<span data-ttu-id="91cd7-129">Especifica o namespace do provedor de recursos.</span><span class="sxs-lookup"><span data-stu-id="91cd7-129">Specifies the namespace of the resource provider.</span></span>

```yaml
Type: System.String[]
Parameter Sets: IndividualProvider
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91cd7-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91cd7-130">CommonParameters</span></span>
<span data-ttu-id="91cd7-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91cd7-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91cd7-132">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="91cd7-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91cd7-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="91cd7-133">INPUTS</span></span>

### <span data-ttu-id="91cd7-134">System. String []</span><span class="sxs-lookup"><span data-stu-id="91cd7-134">System.String[]</span></span>

## <span data-ttu-id="91cd7-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="91cd7-135">OUTPUTS</span></span>

### <span data-ttu-id="91cd7-136">Microsoft. Azure. Commands. ResourceManager. cmdlets. SdkModels. PSResourceProvider</span><span class="sxs-lookup"><span data-stu-id="91cd7-136">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceProvider</span></span>

## <span data-ttu-id="91cd7-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="91cd7-137">NOTES</span></span>

## <span data-ttu-id="91cd7-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="91cd7-138">RELATED LINKS</span></span>

[<span data-ttu-id="91cd7-139">Register-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="91cd7-139">Register-AzResourceProvider</span></span>](./Register-AzResourceProvider.md)

[<span data-ttu-id="91cd7-140">Cancelar registro-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="91cd7-140">Unregister-AzResourceProvider</span></span>](./Unregister-AzResourceProvider.md)



---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/get-azspringcloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Get-AzSpringCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Get-AzSpringCloud.md
ms.openlocfilehash: 39324dc0f85ca4d6f9c3498fae92c340e2113dad
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94115241"
---
# <span data-ttu-id="7bc5b-101">Get-AzSpringCloud</span><span class="sxs-lookup"><span data-stu-id="7bc5b-101">Get-AzSpringCloud</span></span>

## <span data-ttu-id="7bc5b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7bc5b-102">SYNOPSIS</span></span>
<span data-ttu-id="7bc5b-103">Obter um serviço e suas propriedades.</span><span class="sxs-lookup"><span data-stu-id="7bc5b-103">Get a Service and its properties.</span></span>

## <span data-ttu-id="7bc5b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7bc5b-104">SYNTAX</span></span>

### <span data-ttu-id="7bc5b-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="7bc5b-105">List (Default)</span></span>
```
Get-AzSpringCloud [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="7bc5b-106">Obter</span><span class="sxs-lookup"><span data-stu-id="7bc5b-106">Get</span></span>
```
Get-AzSpringCloud -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="7bc5b-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="7bc5b-107">GetViaIdentity</span></span>
```
Get-AzSpringCloud -InputObject <ISpringCloudIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="7bc5b-108">List1</span><span class="sxs-lookup"><span data-stu-id="7bc5b-108">List1</span></span>
```
Get-AzSpringCloud -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="7bc5b-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7bc5b-109">DESCRIPTION</span></span>
<span data-ttu-id="7bc5b-110">Obter um serviço e suas propriedades.</span><span class="sxs-lookup"><span data-stu-id="7bc5b-110">Get a Service and its properties.</span></span>

## <span data-ttu-id="7bc5b-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7bc5b-111">EXAMPLES</span></span>

### <span data-ttu-id="7bc5b-112">Exemplo 1: obter o serviço de nuvem Spring por nome</span><span class="sxs-lookup"><span data-stu-id="7bc5b-112">Example 1: Get Spring Cloud Service by name</span></span>
```powershell
PS C:\> Get-AzSpringCloud -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service
ConfigServerPropertiesErrorCode                  :
ConfigServerPropertiesErrorMessage               :
ConfigServerPropertyState                        : Succeeded
GitPropertyHostKey                               :
GitPropertyHostKeyAlgorithm                      :
GitPropertyLabel                                 :
GitPropertyPassword                              :
GitPropertyPrivateKey                            :
GitPropertyRepository                            :
GitPropertySearchPath                            :
GitPropertyStrictHostKeyChecking                 :
GitPropertyUri                                   :
GitPropertyUsername                              :
Id                                               : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/spring-cloud-rg/providers/Microsoft.AppPlatform/Spring/spring-cloud-service
Location                                         : eastus
Name                                             : spring-cloud-service
NetworkProfileAppNetworkResourceGroup            :
NetworkProfileAppSubnetId                        :
NetworkProfileServiceCidr                        :
NetworkProfileServiceRuntimeNetworkResourceGroup :
NetworkProfileServiceRuntimeSubnetId             :
ProvisioningState                                : Succeeded
ServiceId                                        : e5e964885b4146b1a91e9bfc17971ee5
SkuCapacity                                      :
SkuName                                          : S0
SkuTier                                          : Standard
Tag                                              : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.TrackedResourceTags
TraceAppInsightInstrumentationKey                :
TraceEnabled                                     : False
TraceErrorCode                                   :
TraceErrorMessage                                :
TraceState                                       : Succeeded
Type                                             : Microsoft.AppPlatform/Spring
Version                                          : 2
ConfigServerGitProperty                          : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.ConfigServerGitProperty
ConfigServerProperty                             : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.ConfigServerProperties
ConfigServerPropertyConfigServer                 : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.ConfigServerSettings
ConfigServerPropertyError                        : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.Error
NetworkProfile                                   : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.NetworkProfile
Property                                         : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.ClusterResourceProperties
Sku                                              : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.Sku
Trace                                            : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.TraceProperties
TraceError                                       : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.Error
```

<span data-ttu-id="7bc5b-113">Obter serviço de nuvem Spring por nome</span><span class="sxs-lookup"><span data-stu-id="7bc5b-113">Get Spring Cloud Service by name</span></span>

### <span data-ttu-id="7bc5b-114">Exemplo 2: listar todos os serviços de nuvem Spring sob o grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="7bc5b-114">Example 2: List all the spring cloud service under the resource group.</span></span>
```powershell
PS C:\> Get-AzSpringCloud -ResourceGroupName spring-cloud-rg
Location Name                Type
-------- ----                ----
eastus   spring-cloud-rg Microsoft.AppPlatform/Spring
```

<span data-ttu-id="7bc5b-115">Liste todos os serviços de nuvem da mola sob o grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="7bc5b-115">List all the spring cloud service under the resource group.</span></span>

## <span data-ttu-id="7bc5b-116">OS</span><span class="sxs-lookup"><span data-stu-id="7bc5b-116">PARAMETERS</span></span>

### <span data-ttu-id="7bc5b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7bc5b-117">-DefaultProfile</span></span>
<span data-ttu-id="7bc5b-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7bc5b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bc5b-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7bc5b-119">-InputObject</span></span>
<span data-ttu-id="7bc5b-120">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="7bc5b-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7bc5b-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="7bc5b-121">-Name</span></span>
<span data-ttu-id="7bc5b-122">O nome do recurso de serviço.</span><span class="sxs-lookup"><span data-stu-id="7bc5b-122">The name of the Service resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bc5b-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7bc5b-123">-ResourceGroupName</span></span>
<span data-ttu-id="7bc5b-124">O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="7bc5b-124">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="7bc5b-125">Você pode obter esse valor da API do Azure Resource Manager ou do Portal.</span><span class="sxs-lookup"><span data-stu-id="7bc5b-125">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bc5b-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7bc5b-126">-SubscriptionId</span></span>
<span data-ttu-id="7bc5b-127">Obtém a ID da assinatura que identifica exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="7bc5b-127">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="7bc5b-128">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="7bc5b-128">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bc5b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7bc5b-129">CommonParameters</span></span>
<span data-ttu-id="7bc5b-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7bc5b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7bc5b-131">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7bc5b-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7bc5b-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7bc5b-132">INPUTS</span></span>

### <span data-ttu-id="7bc5b-133">Microsoft. Azure. PowerShell. cmdlets. SpringCloud. Models. ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="7bc5b-133">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="7bc5b-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7bc5b-134">OUTPUTS</span></span>

### <span data-ttu-id="7bc5b-135">Microsoft. Azure. PowerShell. cmdlets. SpringCloud. Models. Api20200701. IServiceResource</span><span class="sxs-lookup"><span data-stu-id="7bc5b-135">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IServiceResource</span></span>

## <span data-ttu-id="7bc5b-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7bc5b-136">NOTES</span></span>

<span data-ttu-id="7bc5b-137">ALIASES</span><span class="sxs-lookup"><span data-stu-id="7bc5b-137">ALIASES</span></span>

<span data-ttu-id="7bc5b-138">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="7bc5b-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="7bc5b-139">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="7bc5b-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="7bc5b-140">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="7bc5b-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="7bc5b-141">INPUTobject <ISpringCloudIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="7bc5b-141">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="7bc5b-142">`[AppName <String>]`: O nome do recurso de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="7bc5b-142">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="7bc5b-143">`[BindingName <String>]`: O nome do recurso de associação.</span><span class="sxs-lookup"><span data-stu-id="7bc5b-143">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="7bc5b-144">`[CertificateName <String>]`: O nome do recurso de certificado.</span><span class="sxs-lookup"><span data-stu-id="7bc5b-144">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="7bc5b-145">`[DeploymentName <String>]`: O nome do recurso de implantação.</span><span class="sxs-lookup"><span data-stu-id="7bc5b-145">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="7bc5b-146">`[DomainName <String>]`: O nome do recurso de domínio personalizado.</span><span class="sxs-lookup"><span data-stu-id="7bc5b-146">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="7bc5b-147">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="7bc5b-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="7bc5b-148">`[Location <String>]`: a região</span><span class="sxs-lookup"><span data-stu-id="7bc5b-148">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="7bc5b-149">`[ResourceGroupName <String>]`: O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="7bc5b-149">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="7bc5b-150">Você pode obter esse valor da API do Azure Resource Manager ou do Portal.</span><span class="sxs-lookup"><span data-stu-id="7bc5b-150">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="7bc5b-151">`[ServiceName <String>]`: O nome do recurso de serviço.</span><span class="sxs-lookup"><span data-stu-id="7bc5b-151">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="7bc5b-152">`[SubscriptionId <String>]`: Obtém a ID de assinatura que identifica exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="7bc5b-152">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="7bc5b-153">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="7bc5b-153">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="7bc5b-154">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7bc5b-154">RELATED LINKS</span></span>


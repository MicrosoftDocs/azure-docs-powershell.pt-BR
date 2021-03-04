---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/powershell/module/az.springcloud/get-azspringcloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Get-AzSpringCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Get-AzSpringCloud.md
ms.openlocfilehash: 186b93c23de78bddcfb88946fbd19becee8ae938
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885801"
---
# <span data-ttu-id="a06d1-101">Get-AzSpringCloud</span><span class="sxs-lookup"><span data-stu-id="a06d1-101">Get-AzSpringCloud</span></span>

## <span data-ttu-id="a06d1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a06d1-102">SYNOPSIS</span></span>
<span data-ttu-id="a06d1-103">Obter um Serviço e suas propriedades.</span><span class="sxs-lookup"><span data-stu-id="a06d1-103">Get a Service and its properties.</span></span>

## <span data-ttu-id="a06d1-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="a06d1-104">SYNTAX</span></span>

### <span data-ttu-id="a06d1-105">Lista (Padrão)</span><span class="sxs-lookup"><span data-stu-id="a06d1-105">List (Default)</span></span>
```
Get-AzSpringCloud [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a06d1-106">Obter</span><span class="sxs-lookup"><span data-stu-id="a06d1-106">Get</span></span>
```
Get-AzSpringCloud -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a06d1-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="a06d1-107">GetViaIdentity</span></span>
```
Get-AzSpringCloud -InputObject <ISpringCloudIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a06d1-108">List1</span><span class="sxs-lookup"><span data-stu-id="a06d1-108">List1</span></span>
```
Get-AzSpringCloud -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="a06d1-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="a06d1-109">DESCRIPTION</span></span>
<span data-ttu-id="a06d1-110">Obter um Serviço e suas propriedades.</span><span class="sxs-lookup"><span data-stu-id="a06d1-110">Get a Service and its properties.</span></span>

## <span data-ttu-id="a06d1-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a06d1-111">EXAMPLES</span></span>

### <span data-ttu-id="a06d1-112">Exemplo 1: obter o nome do Serviço de Nuvem da Primavera</span><span class="sxs-lookup"><span data-stu-id="a06d1-112">Example 1: Get Spring Cloud Service by name</span></span>
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

<span data-ttu-id="a06d1-113">Obter o nome do Serviço de Nuvem de Primavera</span><span class="sxs-lookup"><span data-stu-id="a06d1-113">Get Spring Cloud Service by name</span></span>

### <span data-ttu-id="a06d1-114">Exemplo 2: listar todo o serviço de nuvem de mola no grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a06d1-114">Example 2: List all the spring cloud service under the resource group.</span></span>
```powershell
PS C:\> Get-AzSpringCloud -ResourceGroupName spring-cloud-rg
Location Name                Type
-------- ----                ----
eastus   spring-cloud-rg Microsoft.AppPlatform/Spring
```

<span data-ttu-id="a06d1-115">Listar todo o serviço de nuvem de primavera no grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a06d1-115">List all the spring cloud service under the resource group.</span></span>

## <span data-ttu-id="a06d1-116">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="a06d1-116">PARAMETERS</span></span>

### <span data-ttu-id="a06d1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a06d1-117">-DefaultProfile</span></span>
<span data-ttu-id="a06d1-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a06d1-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a06d1-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a06d1-119">-InputObject</span></span>
<span data-ttu-id="a06d1-120">Parâmetro Identity Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="a06d1-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="a06d1-121">-Name</span><span class="sxs-lookup"><span data-stu-id="a06d1-121">-Name</span></span>
<span data-ttu-id="a06d1-122">O nome do recurso Service.</span><span class="sxs-lookup"><span data-stu-id="a06d1-122">The name of the Service resource.</span></span>

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

### <span data-ttu-id="a06d1-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a06d1-123">-ResourceGroupName</span></span>
<span data-ttu-id="a06d1-124">O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="a06d1-124">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="a06d1-125">Você pode obter esse valor da API do Gerenciador de Recursos do Azure ou do portal.</span><span class="sxs-lookup"><span data-stu-id="a06d1-125">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="a06d1-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a06d1-126">-SubscriptionId</span></span>
<span data-ttu-id="a06d1-127">Obtém a ID da assinatura que identifica exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="a06d1-127">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="a06d1-128">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="a06d1-128">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="a06d1-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a06d1-129">CommonParameters</span></span>
<span data-ttu-id="a06d1-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a06d1-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a06d1-131">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a06d1-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a06d1-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a06d1-132">INPUTS</span></span>

### <span data-ttu-id="a06d1-133">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="a06d1-133">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="a06d1-134">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="a06d1-134">OUTPUTS</span></span>

### <span data-ttu-id="a06d1-135">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IServiceResource</span><span class="sxs-lookup"><span data-stu-id="a06d1-135">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IServiceResource</span></span>

## <span data-ttu-id="a06d1-136">NOTES</span><span class="sxs-lookup"><span data-stu-id="a06d1-136">NOTES</span></span>

<span data-ttu-id="a06d1-137">ALIASES</span><span class="sxs-lookup"><span data-stu-id="a06d1-137">ALIASES</span></span>

<span data-ttu-id="a06d1-138">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="a06d1-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a06d1-139">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="a06d1-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a06d1-140">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a06d1-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a06d1-141">INPUTOBJECT <ISpringCloudIdentity> : Parâmetro Identity</span><span class="sxs-lookup"><span data-stu-id="a06d1-141">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a06d1-142">`[AppName <String>]`: O nome do recurso App.</span><span class="sxs-lookup"><span data-stu-id="a06d1-142">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="a06d1-143">`[BindingName <String>]`: O nome do recurso Binding.</span><span class="sxs-lookup"><span data-stu-id="a06d1-143">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="a06d1-144">`[CertificateName <String>]`: O nome do recurso de certificado.</span><span class="sxs-lookup"><span data-stu-id="a06d1-144">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="a06d1-145">`[DeploymentName <String>]`: O nome do recurso Deployment.</span><span class="sxs-lookup"><span data-stu-id="a06d1-145">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="a06d1-146">`[DomainName <String>]`: O nome do recurso de domínio personalizado.</span><span class="sxs-lookup"><span data-stu-id="a06d1-146">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="a06d1-147">`[Id <String>]`: Caminho da identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="a06d1-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a06d1-148">`[Location <String>]`: a região</span><span class="sxs-lookup"><span data-stu-id="a06d1-148">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="a06d1-149">`[ResourceGroupName <String>]`: O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="a06d1-149">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="a06d1-150">Você pode obter esse valor da API do Gerenciador de Recursos do Azure ou do portal.</span><span class="sxs-lookup"><span data-stu-id="a06d1-150">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="a06d1-151">`[ServiceName <String>]`: O nome do recurso Service.</span><span class="sxs-lookup"><span data-stu-id="a06d1-151">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="a06d1-152">`[SubscriptionId <String>]`: Obtém a ID da assinatura que identifica exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="a06d1-152">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="a06d1-153">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="a06d1-153">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="a06d1-154">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a06d1-154">RELATED LINKS</span></span>


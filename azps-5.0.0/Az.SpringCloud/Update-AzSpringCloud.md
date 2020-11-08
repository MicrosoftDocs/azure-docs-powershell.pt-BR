---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/update-azspringcloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Update-AzSpringCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Update-AzSpringCloud.md
ms.openlocfilehash: 361ba47486d7cc506e918ea279129110306e415f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94115221"
---
# <span data-ttu-id="ec81e-101">Update-AzSpringCloud</span><span class="sxs-lookup"><span data-stu-id="ec81e-101">Update-AzSpringCloud</span></span>

## <span data-ttu-id="ec81e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ec81e-102">SYNOPSIS</span></span>
<span data-ttu-id="ec81e-103">Operação para atualizar um serviço de saída.</span><span class="sxs-lookup"><span data-stu-id="ec81e-103">Operation to update an exiting Service.</span></span>

## <span data-ttu-id="ec81e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ec81e-104">SYNTAX</span></span>

### <span data-ttu-id="ec81e-105">UpdateExpanded (padrão)</span><span class="sxs-lookup"><span data-stu-id="ec81e-105">UpdateExpanded (Default)</span></span>
```
Update-AzSpringCloud -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-GitPropertyUri <String>] [-Location <String>] [-SkuName <String>] [-SkuTier <String>] [-Tag <Hashtable>]
 [-TraceAppInsightInstrumentationKey <String>] [-TraceEnabled] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="ec81e-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="ec81e-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzSpringCloud -InputObject <ISpringCloudIdentity> [-GitPropertyUri <String>] [-Location <String>]
 [-SkuName <String>] [-SkuTier <String>] [-Tag <Hashtable>] [-TraceAppInsightInstrumentationKey <String>]
 [-TraceEnabled] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ec81e-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ec81e-107">DESCRIPTION</span></span>
<span data-ttu-id="ec81e-108">Operação para atualizar um serviço de saída.</span><span class="sxs-lookup"><span data-stu-id="ec81e-108">Operation to update an exiting Service.</span></span>

## <span data-ttu-id="ec81e-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ec81e-109">EXAMPLES</span></span>

### <span data-ttu-id="ec81e-110">Exemplo 1: Atualize o serviço de nuvem Spring por nome.</span><span class="sxs-lookup"><span data-stu-id="ec81e-110">Example 1: Update Spring Cloud Service by name.</span></span>
```powershell
PS C:\> Update-AzSpringCloud -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service
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

<span data-ttu-id="ec81e-111">Atualize o serviço de nuvem da mola por nome.</span><span class="sxs-lookup"><span data-stu-id="ec81e-111">Update Spring Cloud Service by name.</span></span>

### <span data-ttu-id="ec81e-112">Exemplo 2: Atualize o serviço de nuvem da mola do pipe.</span><span class="sxs-lookup"><span data-stu-id="ec81e-112">Example 2: Update Spring Cloud Service from pipe.</span></span>
```powershell
PS C:\> Get-AzSpringCloud -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service | Update-AzSpringCloud
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

<span data-ttu-id="ec81e-113">Atualize o serviço de nuvem da mola do pipe.</span><span class="sxs-lookup"><span data-stu-id="ec81e-113">Update Spring Cloud Service from pipe.</span></span>

## <span data-ttu-id="ec81e-114">OS</span><span class="sxs-lookup"><span data-stu-id="ec81e-114">PARAMETERS</span></span>

### <span data-ttu-id="ec81e-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ec81e-115">-AsJob</span></span>
<span data-ttu-id="ec81e-116">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="ec81e-116">Run the command as a job</span></span>

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

### <span data-ttu-id="ec81e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec81e-117">-DefaultProfile</span></span>
<span data-ttu-id="ec81e-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ec81e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ec81e-119">-GitPropertyUri</span><span class="sxs-lookup"><span data-stu-id="ec81e-119">-GitPropertyUri</span></span>
<span data-ttu-id="ec81e-120">URI do repositório</span><span class="sxs-lookup"><span data-stu-id="ec81e-120">URI of the repository</span></span>

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

### <span data-ttu-id="ec81e-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ec81e-121">-InputObject</span></span>
<span data-ttu-id="ec81e-122">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="ec81e-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ec81e-123">-Local</span><span class="sxs-lookup"><span data-stu-id="ec81e-123">-Location</span></span>
<span data-ttu-id="ec81e-124">A localização geográfica do recurso.</span><span class="sxs-lookup"><span data-stu-id="ec81e-124">The GEO location of the resource.</span></span>

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

### <span data-ttu-id="ec81e-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="ec81e-125">-Name</span></span>
<span data-ttu-id="ec81e-126">O nome do recurso de serviço.</span><span class="sxs-lookup"><span data-stu-id="ec81e-126">The name of the Service resource.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: ServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec81e-127">-Nowait</span><span class="sxs-lookup"><span data-stu-id="ec81e-127">-NoWait</span></span>
<span data-ttu-id="ec81e-128">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="ec81e-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="ec81e-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec81e-129">-ResourceGroupName</span></span>
<span data-ttu-id="ec81e-130">O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="ec81e-130">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="ec81e-131">Você pode obter esse valor da API do Azure Resource Manager ou do Portal.</span><span class="sxs-lookup"><span data-stu-id="ec81e-131">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec81e-132">-SkuName</span><span class="sxs-lookup"><span data-stu-id="ec81e-132">-SkuName</span></span>
<span data-ttu-id="ec81e-133">Nome da SKU</span><span class="sxs-lookup"><span data-stu-id="ec81e-133">Name of the Sku</span></span>

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

### <span data-ttu-id="ec81e-134">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="ec81e-134">-SkuTier</span></span>
<span data-ttu-id="ec81e-135">Camada da SKU</span><span class="sxs-lookup"><span data-stu-id="ec81e-135">Tier of the Sku</span></span>

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

### <span data-ttu-id="ec81e-136">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ec81e-136">-SubscriptionId</span></span>
<span data-ttu-id="ec81e-137">Obtém a ID da assinatura que identifica exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="ec81e-137">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="ec81e-138">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="ec81e-138">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec81e-139">-Marca</span><span class="sxs-lookup"><span data-stu-id="ec81e-139">-Tag</span></span>
<span data-ttu-id="ec81e-140">Marcas do serviço que é uma lista de pares de valores chave que descrevem o recurso.</span><span class="sxs-lookup"><span data-stu-id="ec81e-140">Tags of the service which is a list of key value pairs that describe the resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec81e-141">-TraceAppInsightInstrumentationKey</span><span class="sxs-lookup"><span data-stu-id="ec81e-141">-TraceAppInsightInstrumentationKey</span></span>
<span data-ttu-id="ec81e-142">Chave de instrumentação de percepção do aplicativo de destino</span><span class="sxs-lookup"><span data-stu-id="ec81e-142">Target application insight instrumentation key</span></span>

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

### <span data-ttu-id="ec81e-143">-TraceEnabled</span><span class="sxs-lookup"><span data-stu-id="ec81e-143">-TraceEnabled</span></span>
<span data-ttu-id="ec81e-144">Indica se a funcionalidade de rastreamento deve ser habilitada</span><span class="sxs-lookup"><span data-stu-id="ec81e-144">Indicates whether enable the tracing functionality</span></span>

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

### <span data-ttu-id="ec81e-145">-Confirme</span><span class="sxs-lookup"><span data-stu-id="ec81e-145">-Confirm</span></span>
<span data-ttu-id="ec81e-146">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ec81e-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ec81e-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ec81e-147">-WhatIf</span></span>
<span data-ttu-id="ec81e-148">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ec81e-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ec81e-149">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ec81e-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ec81e-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec81e-150">CommonParameters</span></span>
<span data-ttu-id="ec81e-151">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ec81e-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec81e-152">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ec81e-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec81e-153">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ec81e-153">INPUTS</span></span>

### <span data-ttu-id="ec81e-154">Microsoft. Azure. PowerShell. cmdlets. SpringCloud. Models. ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="ec81e-154">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="ec81e-155">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ec81e-155">OUTPUTS</span></span>

### <span data-ttu-id="ec81e-156">Microsoft. Azure. PowerShell. cmdlets. SpringCloud. Models. Api20200701. IServiceResource</span><span class="sxs-lookup"><span data-stu-id="ec81e-156">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IServiceResource</span></span>

## <span data-ttu-id="ec81e-157">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ec81e-157">NOTES</span></span>

<span data-ttu-id="ec81e-158">ALIASES</span><span class="sxs-lookup"><span data-stu-id="ec81e-158">ALIASES</span></span>

<span data-ttu-id="ec81e-159">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="ec81e-159">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ec81e-160">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="ec81e-160">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ec81e-161">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ec81e-161">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ec81e-162">INPUTobject <ISpringCloudIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="ec81e-162">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ec81e-163">`[AppName <String>]`: O nome do recurso de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="ec81e-163">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="ec81e-164">`[BindingName <String>]`: O nome do recurso de associação.</span><span class="sxs-lookup"><span data-stu-id="ec81e-164">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="ec81e-165">`[CertificateName <String>]`: O nome do recurso de certificado.</span><span class="sxs-lookup"><span data-stu-id="ec81e-165">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="ec81e-166">`[DeploymentName <String>]`: O nome do recurso de implantação.</span><span class="sxs-lookup"><span data-stu-id="ec81e-166">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="ec81e-167">`[DomainName <String>]`: O nome do recurso de domínio personalizado.</span><span class="sxs-lookup"><span data-stu-id="ec81e-167">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="ec81e-168">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="ec81e-168">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ec81e-169">`[Location <String>]`: a região</span><span class="sxs-lookup"><span data-stu-id="ec81e-169">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="ec81e-170">`[ResourceGroupName <String>]`: O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="ec81e-170">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="ec81e-171">Você pode obter esse valor da API do Azure Resource Manager ou do Portal.</span><span class="sxs-lookup"><span data-stu-id="ec81e-171">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="ec81e-172">`[ServiceName <String>]`: O nome do recurso de serviço.</span><span class="sxs-lookup"><span data-stu-id="ec81e-172">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="ec81e-173">`[SubscriptionId <String>]`: Obtém a ID de assinatura que identifica exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="ec81e-173">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="ec81e-174">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="ec81e-174">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="ec81e-175">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ec81e-175">RELATED LINKS</span></span>


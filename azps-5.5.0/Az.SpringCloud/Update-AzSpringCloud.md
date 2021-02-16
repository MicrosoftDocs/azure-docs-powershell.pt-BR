---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/update-azspringcloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Update-AzSpringCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Update-AzSpringCloud.md
ms.openlocfilehash: 361ba47486d7cc506e918ea279129110306e415f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113963"
---
# <span data-ttu-id="0786d-101">Update-AzSpringCloud</span><span class="sxs-lookup"><span data-stu-id="0786d-101">Update-AzSpringCloud</span></span>

## <span data-ttu-id="0786d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0786d-102">SYNOPSIS</span></span>
<span data-ttu-id="0786d-103">Operação para atualizar um Serviço de saída.</span><span class="sxs-lookup"><span data-stu-id="0786d-103">Operation to update an exiting Service.</span></span>

## <span data-ttu-id="0786d-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0786d-104">SYNTAX</span></span>

### <span data-ttu-id="0786d-105">UpdateExpanded (Padrão)</span><span class="sxs-lookup"><span data-stu-id="0786d-105">UpdateExpanded (Default)</span></span>
```
Update-AzSpringCloud -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-GitPropertyUri <String>] [-Location <String>] [-SkuName <String>] [-SkuTier <String>] [-Tag <Hashtable>]
 [-TraceAppInsightInstrumentationKey <String>] [-TraceEnabled] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="0786d-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="0786d-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzSpringCloud -InputObject <ISpringCloudIdentity> [-GitPropertyUri <String>] [-Location <String>]
 [-SkuName <String>] [-SkuTier <String>] [-Tag <Hashtable>] [-TraceAppInsightInstrumentationKey <String>]
 [-TraceEnabled] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="0786d-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="0786d-107">DESCRIPTION</span></span>
<span data-ttu-id="0786d-108">Operação para atualizar um Serviço de saída.</span><span class="sxs-lookup"><span data-stu-id="0786d-108">Operation to update an exiting Service.</span></span>

## <span data-ttu-id="0786d-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="0786d-109">EXAMPLES</span></span>

### <span data-ttu-id="0786d-110">Exemplo 1: Atualizar o Serviço de Nuvem da Primavera por nome.</span><span class="sxs-lookup"><span data-stu-id="0786d-110">Example 1: Update Spring Cloud Service by name.</span></span>
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

<span data-ttu-id="0786d-111">Atualize o Serviço de Nuvem de Primavera por nome.</span><span class="sxs-lookup"><span data-stu-id="0786d-111">Update Spring Cloud Service by name.</span></span>

### <span data-ttu-id="0786d-112">Exemplo 2: Atualizar o Serviço de Nuvem de Primavera do cano.</span><span class="sxs-lookup"><span data-stu-id="0786d-112">Example 2: Update Spring Cloud Service from pipe.</span></span>
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

<span data-ttu-id="0786d-113">Atualize o Serviço de Nuvem de Primavera do cano.</span><span class="sxs-lookup"><span data-stu-id="0786d-113">Update Spring Cloud Service from pipe.</span></span>

## <span data-ttu-id="0786d-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0786d-114">PARAMETERS</span></span>

### <span data-ttu-id="0786d-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0786d-115">-AsJob</span></span>
<span data-ttu-id="0786d-116">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="0786d-116">Run the command as a job</span></span>

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

### <span data-ttu-id="0786d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0786d-117">-DefaultProfile</span></span>
<span data-ttu-id="0786d-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0786d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0786d-119">-GitPropertyUri</span><span class="sxs-lookup"><span data-stu-id="0786d-119">-GitPropertyUri</span></span>
<span data-ttu-id="0786d-120">URI do repositório</span><span class="sxs-lookup"><span data-stu-id="0786d-120">URI of the repository</span></span>

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

### <span data-ttu-id="0786d-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0786d-121">-InputObject</span></span>
<span data-ttu-id="0786d-122">Parâmetro de Identidade para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="0786d-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="0786d-123">-Local</span><span class="sxs-lookup"><span data-stu-id="0786d-123">-Location</span></span>
<span data-ttu-id="0786d-124">A localização GEO do recurso.</span><span class="sxs-lookup"><span data-stu-id="0786d-124">The GEO location of the resource.</span></span>

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

### <span data-ttu-id="0786d-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="0786d-125">-Name</span></span>
<span data-ttu-id="0786d-126">O nome do recurso Serviço.</span><span class="sxs-lookup"><span data-stu-id="0786d-126">The name of the Service resource.</span></span>

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

### <span data-ttu-id="0786d-127">-NoWait</span><span class="sxs-lookup"><span data-stu-id="0786d-127">-NoWait</span></span>
<span data-ttu-id="0786d-128">Executar o comando assíncrona</span><span class="sxs-lookup"><span data-stu-id="0786d-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="0786d-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0786d-129">-ResourceGroupName</span></span>
<span data-ttu-id="0786d-130">O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="0786d-130">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="0786d-131">Você pode obter esse valor da API do Gerenciador de Recursos do Azure ou do portal.</span><span class="sxs-lookup"><span data-stu-id="0786d-131">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="0786d-132">-SkuName</span><span class="sxs-lookup"><span data-stu-id="0786d-132">-SkuName</span></span>
<span data-ttu-id="0786d-133">Nome da SKU</span><span class="sxs-lookup"><span data-stu-id="0786d-133">Name of the Sku</span></span>

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

### <span data-ttu-id="0786d-134">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="0786d-134">-SkuTier</span></span>
<span data-ttu-id="0786d-135">Camada da SKU</span><span class="sxs-lookup"><span data-stu-id="0786d-135">Tier of the Sku</span></span>

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

### <span data-ttu-id="0786d-136">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0786d-136">-SubscriptionId</span></span>
<span data-ttu-id="0786d-137">Obtém a ID da assinatura que identifica exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="0786d-137">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="0786d-138">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="0786d-138">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="0786d-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="0786d-139">-Tag</span></span>
<span data-ttu-id="0786d-140">Marcas do serviço, que é uma lista de pares de valores-chave que descrevem o recurso.</span><span class="sxs-lookup"><span data-stu-id="0786d-140">Tags of the service which is a list of key value pairs that describe the resource.</span></span>

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

### <span data-ttu-id="0786d-141">-TraceAppInsightInstrumentationKey</span><span class="sxs-lookup"><span data-stu-id="0786d-141">-TraceAppInsightInstrumentationKey</span></span>
<span data-ttu-id="0786d-142">Chave de instrumentação de informações do aplicativo de destino</span><span class="sxs-lookup"><span data-stu-id="0786d-142">Target application insight instrumentation key</span></span>

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

### <span data-ttu-id="0786d-143">-TraceEnabled</span><span class="sxs-lookup"><span data-stu-id="0786d-143">-TraceEnabled</span></span>
<span data-ttu-id="0786d-144">Indica se habilitar a funcionalidade de rastreamento</span><span class="sxs-lookup"><span data-stu-id="0786d-144">Indicates whether enable the tracing functionality</span></span>

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

### <span data-ttu-id="0786d-145">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="0786d-145">-Confirm</span></span>
<span data-ttu-id="0786d-146">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0786d-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0786d-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0786d-147">-WhatIf</span></span>
<span data-ttu-id="0786d-148">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="0786d-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0786d-149">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0786d-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0786d-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0786d-150">CommonParameters</span></span>
<span data-ttu-id="0786d-151">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0786d-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0786d-152">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0786d-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0786d-153">Entradas</span><span class="sxs-lookup"><span data-stu-id="0786d-153">INPUTS</span></span>

### <span data-ttu-id="0786d-154">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="0786d-154">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="0786d-155">Saídas</span><span class="sxs-lookup"><span data-stu-id="0786d-155">OUTPUTS</span></span>

### <span data-ttu-id="0786d-156">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IServiceResource</span><span class="sxs-lookup"><span data-stu-id="0786d-156">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IServiceResource</span></span>

## <span data-ttu-id="0786d-157">Notas</span><span class="sxs-lookup"><span data-stu-id="0786d-157">NOTES</span></span>

<span data-ttu-id="0786d-158">Aliases</span><span class="sxs-lookup"><span data-stu-id="0786d-158">ALIASES</span></span>

<span data-ttu-id="0786d-159">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="0786d-159">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="0786d-160">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="0786d-160">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0786d-161">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="0786d-161">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="0786d-162">INPUTOBJECT: <ISpringCloudIdentity> Parâmetro de Identidade</span><span class="sxs-lookup"><span data-stu-id="0786d-162">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="0786d-163">`[AppName <String>]`: o nome do recurso Aplicativo.</span><span class="sxs-lookup"><span data-stu-id="0786d-163">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="0786d-164">`[BindingName <String>]`: o nome do recurso Encadernação.</span><span class="sxs-lookup"><span data-stu-id="0786d-164">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="0786d-165">`[CertificateName <String>]`: o nome do recurso de certificado.</span><span class="sxs-lookup"><span data-stu-id="0786d-165">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="0786d-166">`[DeploymentName <String>]`: o nome do recurso implantação.</span><span class="sxs-lookup"><span data-stu-id="0786d-166">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="0786d-167">`[DomainName <String>]`: o nome do recurso de domínio personalizado.</span><span class="sxs-lookup"><span data-stu-id="0786d-167">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="0786d-168">`[Id <String>]`: Caminho de identidade de recursos</span><span class="sxs-lookup"><span data-stu-id="0786d-168">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="0786d-169">`[Location <String>]`: a região</span><span class="sxs-lookup"><span data-stu-id="0786d-169">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="0786d-170">`[ResourceGroupName <String>]`: o nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="0786d-170">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="0786d-171">Você pode obter esse valor da API do Gerenciador de Recursos do Azure ou do portal.</span><span class="sxs-lookup"><span data-stu-id="0786d-171">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="0786d-172">`[ServiceName <String>]`: o nome do recurso Serviço.</span><span class="sxs-lookup"><span data-stu-id="0786d-172">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="0786d-173">`[SubscriptionId <String>]`: obtém a ID da assinatura que identifica exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="0786d-173">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="0786d-174">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="0786d-174">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="0786d-175">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0786d-175">RELATED LINKS</span></span>


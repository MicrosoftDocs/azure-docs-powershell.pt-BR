---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/new-azspringcloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/New-AzSpringCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/New-AzSpringCloud.md
ms.openlocfilehash: d5b8d521c72b553143f75b0911cb9b933b0795e7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98257488"
---
# <span data-ttu-id="18a46-101">New-AzSpringCloud</span><span class="sxs-lookup"><span data-stu-id="18a46-101">New-AzSpringCloud</span></span>

## <span data-ttu-id="18a46-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="18a46-102">SYNOPSIS</span></span>
<span data-ttu-id="18a46-103">Crie um novo serviço ou atualize um serviço de saída.</span><span class="sxs-lookup"><span data-stu-id="18a46-103">Create a new Service or update an exiting Service.</span></span>

## <span data-ttu-id="18a46-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="18a46-104">SYNTAX</span></span>

```
New-AzSpringCloud -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-GitPropertyUri <String>] [-Location <String>] [-SkuName <String>] [-SkuTier <String>] [-Tag <Hashtable>]
 [-TraceAppInsightInstrumentationKey <String>] [-TraceEnabled] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="18a46-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="18a46-105">DESCRIPTION</span></span>
<span data-ttu-id="18a46-106">Crie um novo serviço ou atualize um serviço de saída.</span><span class="sxs-lookup"><span data-stu-id="18a46-106">Create a new Service or update an exiting Service.</span></span>

## <span data-ttu-id="18a46-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="18a46-107">EXAMPLES</span></span>

### <span data-ttu-id="18a46-108">Exemplo 1: criar um serviço de nuvem Spring.</span><span class="sxs-lookup"><span data-stu-id="18a46-108">Example 1: Create a spring cloud service.</span></span>
```powershell
PS C:\> New-AzSpringCloud -ResourceGroupName spring-cloud-rp -name spring-cloud-service -Location eastus

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

<span data-ttu-id="18a46-109">Criar um serviço de nuvem Spring.</span><span class="sxs-lookup"><span data-stu-id="18a46-109">Create a spring cloud service.</span></span>

## <span data-ttu-id="18a46-110">OS</span><span class="sxs-lookup"><span data-stu-id="18a46-110">PARAMETERS</span></span>

### <span data-ttu-id="18a46-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="18a46-111">-AsJob</span></span>
<span data-ttu-id="18a46-112">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="18a46-112">Run the command as a job</span></span>

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

### <span data-ttu-id="18a46-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18a46-113">-DefaultProfile</span></span>
<span data-ttu-id="18a46-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="18a46-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="18a46-115">-GitPropertyUri</span><span class="sxs-lookup"><span data-stu-id="18a46-115">-GitPropertyUri</span></span>
<span data-ttu-id="18a46-116">URI do repositório</span><span class="sxs-lookup"><span data-stu-id="18a46-116">URI of the repository</span></span>

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

### <span data-ttu-id="18a46-117">-Local</span><span class="sxs-lookup"><span data-stu-id="18a46-117">-Location</span></span>
<span data-ttu-id="18a46-118">A localização geográfica do recurso.</span><span class="sxs-lookup"><span data-stu-id="18a46-118">The GEO location of the resource.</span></span>

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

### <span data-ttu-id="18a46-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="18a46-119">-Name</span></span>
<span data-ttu-id="18a46-120">O nome do recurso de serviço.</span><span class="sxs-lookup"><span data-stu-id="18a46-120">The name of the Service resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18a46-121">-Nowait</span><span class="sxs-lookup"><span data-stu-id="18a46-121">-NoWait</span></span>
<span data-ttu-id="18a46-122">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="18a46-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="18a46-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18a46-123">-ResourceGroupName</span></span>
<span data-ttu-id="18a46-124">O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="18a46-124">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="18a46-125">Você pode obter esse valor da API do Azure Resource Manager ou do Portal.</span><span class="sxs-lookup"><span data-stu-id="18a46-125">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="18a46-126">-SkuName</span><span class="sxs-lookup"><span data-stu-id="18a46-126">-SkuName</span></span>
<span data-ttu-id="18a46-127">Nome da SKU</span><span class="sxs-lookup"><span data-stu-id="18a46-127">Name of the Sku</span></span>

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

### <span data-ttu-id="18a46-128">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="18a46-128">-SkuTier</span></span>
<span data-ttu-id="18a46-129">Camada da SKU</span><span class="sxs-lookup"><span data-stu-id="18a46-129">Tier of the Sku</span></span>

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

### <span data-ttu-id="18a46-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="18a46-130">-SubscriptionId</span></span>
<span data-ttu-id="18a46-131">Obtém a ID da assinatura que identifica exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="18a46-131">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="18a46-132">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="18a46-132">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18a46-133">-Marca</span><span class="sxs-lookup"><span data-stu-id="18a46-133">-Tag</span></span>
<span data-ttu-id="18a46-134">Marcas do serviço que é uma lista de pares de valores chave que descrevem o recurso.</span><span class="sxs-lookup"><span data-stu-id="18a46-134">Tags of the service which is a list of key value pairs that describe the resource.</span></span>

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

### <span data-ttu-id="18a46-135">-TraceAppInsightInstrumentationKey</span><span class="sxs-lookup"><span data-stu-id="18a46-135">-TraceAppInsightInstrumentationKey</span></span>
<span data-ttu-id="18a46-136">Chave de instrumentação de percepção do aplicativo de destino</span><span class="sxs-lookup"><span data-stu-id="18a46-136">Target application insight instrumentation key</span></span>

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

### <span data-ttu-id="18a46-137">-TraceEnabled</span><span class="sxs-lookup"><span data-stu-id="18a46-137">-TraceEnabled</span></span>
<span data-ttu-id="18a46-138">Indica se a funcionalidade de rastreamento deve ser habilitada</span><span class="sxs-lookup"><span data-stu-id="18a46-138">Indicates whether enable the tracing functionality</span></span>

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

### <span data-ttu-id="18a46-139">-Confirme</span><span class="sxs-lookup"><span data-stu-id="18a46-139">-Confirm</span></span>
<span data-ttu-id="18a46-140">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="18a46-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="18a46-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="18a46-141">-WhatIf</span></span>
<span data-ttu-id="18a46-142">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="18a46-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="18a46-143">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="18a46-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="18a46-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18a46-144">CommonParameters</span></span>
<span data-ttu-id="18a46-145">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18a46-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18a46-146">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="18a46-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18a46-147">SENSORES</span><span class="sxs-lookup"><span data-stu-id="18a46-147">INPUTS</span></span>

## <span data-ttu-id="18a46-148">EXIBE</span><span class="sxs-lookup"><span data-stu-id="18a46-148">OUTPUTS</span></span>

### <span data-ttu-id="18a46-149">Microsoft. Azure. PowerShell. cmdlets. SpringCloud. Models. Api20200701. IServiceResource</span><span class="sxs-lookup"><span data-stu-id="18a46-149">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IServiceResource</span></span>

## <span data-ttu-id="18a46-150">INFORMA</span><span class="sxs-lookup"><span data-stu-id="18a46-150">NOTES</span></span>

<span data-ttu-id="18a46-151">ALIASES</span><span class="sxs-lookup"><span data-stu-id="18a46-151">ALIASES</span></span>

## <span data-ttu-id="18a46-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="18a46-152">RELATED LINKS</span></span>


---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/update-azspringcloudapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Update-AzSpringCloudApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Update-AzSpringCloudApp.md
ms.openlocfilehash: e4d7d502d96245291fce001f4706ae44f21f5fed
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94113287"
---
# <span data-ttu-id="17ba1-101">Update-AzSpringCloudApp</span><span class="sxs-lookup"><span data-stu-id="17ba1-101">Update-AzSpringCloudApp</span></span>

## <span data-ttu-id="17ba1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="17ba1-102">SYNOPSIS</span></span>
<span data-ttu-id="17ba1-103">Operação para atualizar um aplicativo existente.</span><span class="sxs-lookup"><span data-stu-id="17ba1-103">Operation to update an exiting App.</span></span>

## <span data-ttu-id="17ba1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="17ba1-104">SYNTAX</span></span>

### <span data-ttu-id="17ba1-105">UpdateExpanded (padrão)</span><span class="sxs-lookup"><span data-stu-id="17ba1-105">UpdateExpanded (Default)</span></span>
```
Update-AzSpringCloudApp -Name <String> -ResourceGroupName <String> -ServiceName <String>
 [-SubscriptionId <String>] [-ActiveDeploymentName <String>] [-Fqdn <String>] [-HttpsOnly]
 [-Location <String>] [-PersistentDiskMountPath <String>] [-PersistentDiskSizeInGb <Int32>] [-Public]
 [-TemporaryDiskMountPath <String>] [-TemporaryDiskSizeInGb <Int32>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="17ba1-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="17ba1-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzSpringCloudApp -InputObject <ISpringCloudIdentity> [-ActiveDeploymentName <String>] [-Fqdn <String>]
 [-HttpsOnly] [-Location <String>] [-PersistentDiskMountPath <String>] [-PersistentDiskSizeInGb <Int32>]
 [-Public] [-TemporaryDiskMountPath <String>] [-TemporaryDiskSizeInGb <Int32>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="17ba1-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="17ba1-107">DESCRIPTION</span></span>
<span data-ttu-id="17ba1-108">Operação para atualizar um aplicativo existente.</span><span class="sxs-lookup"><span data-stu-id="17ba1-108">Operation to update an exiting App.</span></span>

## <span data-ttu-id="17ba1-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="17ba1-109">EXAMPLES</span></span>

### <span data-ttu-id="17ba1-110">Exemplo 1: atualizar o aplicativo de nuvem Spring por nome.</span><span class="sxs-lookup"><span data-stu-id="17ba1-110">Example 1: Update Spring Cloud App by name.</span></span>
```powershell
PS C:\> Update-AzSpringCloudApp -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway -ActiveDeploymentName default
ActiveDeploymentName    : default
CreatedTime             : 2020-08-08 15:37:43
Fqdn                    : spring-cloud-service.azuremicroservices.io
HttpsOnly               : False
Id                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/spring-cloud-rg/providers/Microsoft.AppPlatform/Spring/spring-cloud-service/apps/gateway
IdentityPrincipalId     :
IdentityTenantId        :
IdentityType            :
Location                : eastus
Name                    : gateway
PersistentDiskMountPath : /persistent
PersistentDiskSizeInGb  : 0
PersistentDiskUsedInGb  :
ProvisioningState       : Succeeded
Public                  : False
TemporaryDiskMountPath  : /tmp
TemporaryDiskSizeInGb   : 5
Type                    : Microsoft.AppPlatform/Spring/apps
Url                     :
Identity                : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.ManagedIdentityProperties
PersistentDisk          : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.PersistentDisk
Property                : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.AppResourceProperties
TemporaryDisk           : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.TemporaryDisk
```

<span data-ttu-id="17ba1-111">Atualize o aplicativo de nuvem da mola por nome.</span><span class="sxs-lookup"><span data-stu-id="17ba1-111">Update Spring Cloud App by name.</span></span>

### <span data-ttu-id="17ba1-112">Exemplo 2: atualizar o aplicativo de nuvem da mola do pipe.</span><span class="sxs-lookup"><span data-stu-id="17ba1-112">Example 2: Update Spring Cloud App from pipe.</span></span>
```powershell
PS C:\> Get-AzSpringCloudApp -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway | Update-AzSpringCloudApp -ActiveDeploymentName default
ActiveDeploymentName    : default
CreatedTime             : 2020-08-08 15:37:43
Fqdn                    : spring-cloud-service.azuremicroservices.io
HttpsOnly               : False
Id                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/spring-cloud-rg/providers/Microsoft.AppPlatform/Spring/spring-cloud-service/apps/gateway
IdentityPrincipalId     :
IdentityTenantId        :
IdentityType            :
Location                : eastus
Name                    : gateway
PersistentDiskMountPath : /persistent
PersistentDiskSizeInGb  : 0
PersistentDiskUsedInGb  :
ProvisioningState       : Succeeded
Public                  : False
TemporaryDiskMountPath  : /tmp
TemporaryDiskSizeInGb   : 5
Type                    : Microsoft.AppPlatform/Spring/apps
Url                     :
Identity                : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.ManagedIdentityProperties
PersistentDisk          : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.PersistentDisk
Property                : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.AppResourceProperties
TemporaryDisk           : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.TemporaryDisk
```

<span data-ttu-id="17ba1-113">Atualize o aplicativo de nuvem da mola do pipe.</span><span class="sxs-lookup"><span data-stu-id="17ba1-113">Update Spring Cloud App from pipe.</span></span>

## <span data-ttu-id="17ba1-114">OS</span><span class="sxs-lookup"><span data-stu-id="17ba1-114">PARAMETERS</span></span>

### <span data-ttu-id="17ba1-115">-ActiveDeploymentName</span><span class="sxs-lookup"><span data-stu-id="17ba1-115">-ActiveDeploymentName</span></span>
<span data-ttu-id="17ba1-116">Nome da implantação ativa do aplicativo</span><span class="sxs-lookup"><span data-stu-id="17ba1-116">Name of the active deployment of the App</span></span>

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

### <span data-ttu-id="17ba1-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="17ba1-117">-AsJob</span></span>
<span data-ttu-id="17ba1-118">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="17ba1-118">Run the command as a job</span></span>

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

### <span data-ttu-id="17ba1-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17ba1-119">-DefaultProfile</span></span>
<span data-ttu-id="17ba1-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="17ba1-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="17ba1-121">-FQDN</span><span class="sxs-lookup"><span data-stu-id="17ba1-121">-Fqdn</span></span>
<span data-ttu-id="17ba1-122">Nome DNS totalmente qualificado.</span><span class="sxs-lookup"><span data-stu-id="17ba1-122">Fully qualified dns Name.</span></span>

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

### <span data-ttu-id="17ba1-123">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="17ba1-123">-HttpsOnly</span></span>
<span data-ttu-id="17ba1-124">Indique se somente HTTPS é permitido.</span><span class="sxs-lookup"><span data-stu-id="17ba1-124">Indicate if only https is allowed.</span></span>

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

### <span data-ttu-id="17ba1-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="17ba1-125">-InputObject</span></span>
<span data-ttu-id="17ba1-126">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="17ba1-126">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="17ba1-127">-Local</span><span class="sxs-lookup"><span data-stu-id="17ba1-127">-Location</span></span>
<span data-ttu-id="17ba1-128">A localização geográfica do aplicativo, sempre a mesma com seu recurso pai</span><span class="sxs-lookup"><span data-stu-id="17ba1-128">The GEO location of the application, always the same with its parent resource</span></span>

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

### <span data-ttu-id="17ba1-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="17ba1-129">-Name</span></span>
<span data-ttu-id="17ba1-130">O nome do recurso de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="17ba1-130">The name of the App resource.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: AppName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17ba1-131">-Nowait</span><span class="sxs-lookup"><span data-stu-id="17ba1-131">-NoWait</span></span>
<span data-ttu-id="17ba1-132">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="17ba1-132">Run the command asynchronously</span></span>

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

### <span data-ttu-id="17ba1-133">-PersistentDiskMountPath</span><span class="sxs-lookup"><span data-stu-id="17ba1-133">-PersistentDiskMountPath</span></span>
<span data-ttu-id="17ba1-134">Caminho de montagem do disco persistente</span><span class="sxs-lookup"><span data-stu-id="17ba1-134">Mount path of the persistent disk</span></span>

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

### <span data-ttu-id="17ba1-135">-PersistentDiskSizeInGb</span><span class="sxs-lookup"><span data-stu-id="17ba1-135">-PersistentDiskSizeInGb</span></span>
<span data-ttu-id="17ba1-136">Tamanho do disco persistente em GB</span><span class="sxs-lookup"><span data-stu-id="17ba1-136">Size of the persistent disk in GB</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17ba1-137">-Público</span><span class="sxs-lookup"><span data-stu-id="17ba1-137">-Public</span></span>
<span data-ttu-id="17ba1-138">Indica se o aplicativo expõe um ponto de extremidade público</span><span class="sxs-lookup"><span data-stu-id="17ba1-138">Indicates whether the App exposes public endpoint</span></span>

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

### <span data-ttu-id="17ba1-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17ba1-139">-ResourceGroupName</span></span>
<span data-ttu-id="17ba1-140">O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="17ba1-140">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="17ba1-141">Você pode obter esse valor da API do Azure Resource Manager ou do Portal.</span><span class="sxs-lookup"><span data-stu-id="17ba1-141">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="17ba1-142">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="17ba1-142">-ServiceName</span></span>
<span data-ttu-id="17ba1-143">O nome do recurso de serviço.</span><span class="sxs-lookup"><span data-stu-id="17ba1-143">The name of the Service resource.</span></span>

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

### <span data-ttu-id="17ba1-144">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="17ba1-144">-SubscriptionId</span></span>
<span data-ttu-id="17ba1-145">Obtém a ID da assinatura que identifica exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="17ba1-145">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="17ba1-146">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="17ba1-146">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="17ba1-147">-TemporaryDiskMountPath</span><span class="sxs-lookup"><span data-stu-id="17ba1-147">-TemporaryDiskMountPath</span></span>
<span data-ttu-id="17ba1-148">Caminho de montagem do disco temporário</span><span class="sxs-lookup"><span data-stu-id="17ba1-148">Mount path of the temporary disk</span></span>

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

### <span data-ttu-id="17ba1-149">-TemporaryDiskSizeInGb</span><span class="sxs-lookup"><span data-stu-id="17ba1-149">-TemporaryDiskSizeInGb</span></span>
<span data-ttu-id="17ba1-150">Tamanho do disco temporário em GB</span><span class="sxs-lookup"><span data-stu-id="17ba1-150">Size of the temporary disk in GB</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17ba1-151">-Confirme</span><span class="sxs-lookup"><span data-stu-id="17ba1-151">-Confirm</span></span>
<span data-ttu-id="17ba1-152">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="17ba1-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="17ba1-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="17ba1-153">-WhatIf</span></span>
<span data-ttu-id="17ba1-154">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="17ba1-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="17ba1-155">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="17ba1-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="17ba1-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17ba1-156">CommonParameters</span></span>
<span data-ttu-id="17ba1-157">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="17ba1-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17ba1-158">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="17ba1-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17ba1-159">SENSORES</span><span class="sxs-lookup"><span data-stu-id="17ba1-159">INPUTS</span></span>

### <span data-ttu-id="17ba1-160">Microsoft. Azure. PowerShell. cmdlets. SpringCloud. Models. ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="17ba1-160">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="17ba1-161">EXIBE</span><span class="sxs-lookup"><span data-stu-id="17ba1-161">OUTPUTS</span></span>

### <span data-ttu-id="17ba1-162">Microsoft. Azure. PowerShell. cmdlets. SpringCloud. Models. Api20190501Preview. IAppResource</span><span class="sxs-lookup"><span data-stu-id="17ba1-162">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.IAppResource</span></span>

## <span data-ttu-id="17ba1-163">INFORMA</span><span class="sxs-lookup"><span data-stu-id="17ba1-163">NOTES</span></span>

<span data-ttu-id="17ba1-164">ALIASES</span><span class="sxs-lookup"><span data-stu-id="17ba1-164">ALIASES</span></span>

<span data-ttu-id="17ba1-165">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="17ba1-165">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="17ba1-166">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="17ba1-166">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="17ba1-167">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="17ba1-167">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="17ba1-168">INPUTobject <ISpringCloudIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="17ba1-168">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="17ba1-169">`[AppName <String>]`: O nome do recurso de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="17ba1-169">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="17ba1-170">`[BindingName <String>]`: O nome do recurso de associação.</span><span class="sxs-lookup"><span data-stu-id="17ba1-170">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="17ba1-171">`[CertificateName <String>]`: O nome do recurso de certificado.</span><span class="sxs-lookup"><span data-stu-id="17ba1-171">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="17ba1-172">`[DeploymentName <String>]`: O nome do recurso de implantação.</span><span class="sxs-lookup"><span data-stu-id="17ba1-172">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="17ba1-173">`[DomainName <String>]`: O nome do recurso de domínio personalizado.</span><span class="sxs-lookup"><span data-stu-id="17ba1-173">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="17ba1-174">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="17ba1-174">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="17ba1-175">`[Location <String>]`: a região</span><span class="sxs-lookup"><span data-stu-id="17ba1-175">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="17ba1-176">`[ResourceGroupName <String>]`: O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="17ba1-176">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="17ba1-177">Você pode obter esse valor da API do Azure Resource Manager ou do Portal.</span><span class="sxs-lookup"><span data-stu-id="17ba1-177">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="17ba1-178">`[ServiceName <String>]`: O nome do recurso de serviço.</span><span class="sxs-lookup"><span data-stu-id="17ba1-178">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="17ba1-179">`[SubscriptionId <String>]`: Obtém a ID de assinatura que identifica exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="17ba1-179">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="17ba1-180">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="17ba1-180">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="17ba1-181">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="17ba1-181">RELATED LINKS</span></span>


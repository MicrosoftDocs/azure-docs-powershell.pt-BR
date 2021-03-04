---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/powershell/module/az.springcloud/update-azspringcloudapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Update-AzSpringCloudApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Update-AzSpringCloudApp.md
ms.openlocfilehash: 2ea144ec36830286919f9cb512ccec01008428a0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892317"
---
# <span data-ttu-id="7f816-101">Update-AzSpringCloudApp</span><span class="sxs-lookup"><span data-stu-id="7f816-101">Update-AzSpringCloudApp</span></span>

## <span data-ttu-id="7f816-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7f816-102">SYNOPSIS</span></span>
<span data-ttu-id="7f816-103">Operação para atualizar um aplicativo que sai.</span><span class="sxs-lookup"><span data-stu-id="7f816-103">Operation to update an exiting App.</span></span>

## <span data-ttu-id="7f816-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="7f816-104">SYNTAX</span></span>

### <span data-ttu-id="7f816-105">UpdateExpanded (Padrão)</span><span class="sxs-lookup"><span data-stu-id="7f816-105">UpdateExpanded (Default)</span></span>
```
Update-AzSpringCloudApp -Name <String> -ResourceGroupName <String> -ServiceName <String>
 [-SubscriptionId <String>] [-ActiveDeploymentName <String>] [-Fqdn <String>] [-HttpsOnly]
 [-Location <String>] [-PersistentDiskMountPath <String>] [-PersistentDiskSizeInGb <Int32>] [-Public]
 [-TemporaryDiskMountPath <String>] [-TemporaryDiskSizeInGb <Int32>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="7f816-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="7f816-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzSpringCloudApp -InputObject <ISpringCloudIdentity> [-ActiveDeploymentName <String>] [-Fqdn <String>]
 [-HttpsOnly] [-Location <String>] [-PersistentDiskMountPath <String>] [-PersistentDiskSizeInGb <Int32>]
 [-Public] [-TemporaryDiskMountPath <String>] [-TemporaryDiskSizeInGb <Int32>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="7f816-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="7f816-107">DESCRIPTION</span></span>
<span data-ttu-id="7f816-108">Operação para atualizar um aplicativo que sai.</span><span class="sxs-lookup"><span data-stu-id="7f816-108">Operation to update an exiting App.</span></span>

## <span data-ttu-id="7f816-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7f816-109">EXAMPLES</span></span>

### <span data-ttu-id="7f816-110">Exemplo 1: Atualizar o Spring Cloud App pelo nome.</span><span class="sxs-lookup"><span data-stu-id="7f816-110">Example 1: Update Spring Cloud App by name.</span></span>
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

<span data-ttu-id="7f816-111">Atualizar o Spring Cloud App pelo nome.</span><span class="sxs-lookup"><span data-stu-id="7f816-111">Update Spring Cloud App by name.</span></span>

### <span data-ttu-id="7f816-112">Exemplo 2: Atualizar o Aplicativo de Nuvem de Primavera a partir do pipe.</span><span class="sxs-lookup"><span data-stu-id="7f816-112">Example 2: Update Spring Cloud App from pipe.</span></span>
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

<span data-ttu-id="7f816-113">Atualize o Aplicativo de Nuvem de Primavera do pipe.</span><span class="sxs-lookup"><span data-stu-id="7f816-113">Update Spring Cloud App from pipe.</span></span>

## <span data-ttu-id="7f816-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="7f816-114">PARAMETERS</span></span>

### <span data-ttu-id="7f816-115">-ActiveDeploymentName</span><span class="sxs-lookup"><span data-stu-id="7f816-115">-ActiveDeploymentName</span></span>
<span data-ttu-id="7f816-116">Nome da implantação ativa do aplicativo</span><span class="sxs-lookup"><span data-stu-id="7f816-116">Name of the active deployment of the App</span></span>

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

### <span data-ttu-id="7f816-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7f816-117">-AsJob</span></span>
<span data-ttu-id="7f816-118">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="7f816-118">Run the command as a job</span></span>

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

### <span data-ttu-id="7f816-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f816-119">-DefaultProfile</span></span>
<span data-ttu-id="7f816-120">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7f816-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7f816-121">-Fqdn</span><span class="sxs-lookup"><span data-stu-id="7f816-121">-Fqdn</span></span>
<span data-ttu-id="7f816-122">Nome dns totalmente qualificado.</span><span class="sxs-lookup"><span data-stu-id="7f816-122">Fully qualified dns Name.</span></span>

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

### <span data-ttu-id="7f816-123">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="7f816-123">-HttpsOnly</span></span>
<span data-ttu-id="7f816-124">Indique se apenas https é permitido.</span><span class="sxs-lookup"><span data-stu-id="7f816-124">Indicate if only https is allowed.</span></span>

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

### <span data-ttu-id="7f816-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7f816-125">-InputObject</span></span>
<span data-ttu-id="7f816-126">Parâmetro Identity Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="7f816-126">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="7f816-127">-Location</span><span class="sxs-lookup"><span data-stu-id="7f816-127">-Location</span></span>
<span data-ttu-id="7f816-128">O local GEO do aplicativo, sempre o mesmo com seu recurso pai</span><span class="sxs-lookup"><span data-stu-id="7f816-128">The GEO location of the application, always the same with its parent resource</span></span>

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

### <span data-ttu-id="7f816-129">-Name</span><span class="sxs-lookup"><span data-stu-id="7f816-129">-Name</span></span>
<span data-ttu-id="7f816-130">O nome do recurso App.</span><span class="sxs-lookup"><span data-stu-id="7f816-130">The name of the App resource.</span></span>

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

### <span data-ttu-id="7f816-131">-NoWait</span><span class="sxs-lookup"><span data-stu-id="7f816-131">-NoWait</span></span>
<span data-ttu-id="7f816-132">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="7f816-132">Run the command asynchronously</span></span>

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

### <span data-ttu-id="7f816-133">-PersistentDiskMountPath</span><span class="sxs-lookup"><span data-stu-id="7f816-133">-PersistentDiskMountPath</span></span>
<span data-ttu-id="7f816-134">Caminho de montagem do disco persistente</span><span class="sxs-lookup"><span data-stu-id="7f816-134">Mount path of the persistent disk</span></span>

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

### <span data-ttu-id="7f816-135">-PersistentDiskSizeInGb</span><span class="sxs-lookup"><span data-stu-id="7f816-135">-PersistentDiskSizeInGb</span></span>
<span data-ttu-id="7f816-136">Tamanho do disco persistente em GB</span><span class="sxs-lookup"><span data-stu-id="7f816-136">Size of the persistent disk in GB</span></span>

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

### <span data-ttu-id="7f816-137">-Public</span><span class="sxs-lookup"><span data-stu-id="7f816-137">-Public</span></span>
<span data-ttu-id="7f816-138">Indica se o aplicativo expõe o ponto de extremidade público</span><span class="sxs-lookup"><span data-stu-id="7f816-138">Indicates whether the App exposes public endpoint</span></span>

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

### <span data-ttu-id="7f816-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f816-139">-ResourceGroupName</span></span>
<span data-ttu-id="7f816-140">O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="7f816-140">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="7f816-141">Você pode obter esse valor da API do Gerenciador de Recursos do Azure ou do portal.</span><span class="sxs-lookup"><span data-stu-id="7f816-141">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="7f816-142">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="7f816-142">-ServiceName</span></span>
<span data-ttu-id="7f816-143">O nome do recurso Service.</span><span class="sxs-lookup"><span data-stu-id="7f816-143">The name of the Service resource.</span></span>

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

### <span data-ttu-id="7f816-144">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7f816-144">-SubscriptionId</span></span>
<span data-ttu-id="7f816-145">Obtém a ID da assinatura que identifica exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="7f816-145">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="7f816-146">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="7f816-146">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="7f816-147">-TemporaryDiskMountPath</span><span class="sxs-lookup"><span data-stu-id="7f816-147">-TemporaryDiskMountPath</span></span>
<span data-ttu-id="7f816-148">Caminho de montagem do disco temporário</span><span class="sxs-lookup"><span data-stu-id="7f816-148">Mount path of the temporary disk</span></span>

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

### <span data-ttu-id="7f816-149">-TemporaryDiskSizeInGb</span><span class="sxs-lookup"><span data-stu-id="7f816-149">-TemporaryDiskSizeInGb</span></span>
<span data-ttu-id="7f816-150">Tamanho do disco temporário em GB</span><span class="sxs-lookup"><span data-stu-id="7f816-150">Size of the temporary disk in GB</span></span>

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

### <span data-ttu-id="7f816-151">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7f816-151">-Confirm</span></span>
<span data-ttu-id="7f816-152">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7f816-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7f816-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7f816-153">-WhatIf</span></span>
<span data-ttu-id="7f816-154">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7f816-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7f816-155">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7f816-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7f816-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f816-156">CommonParameters</span></span>
<span data-ttu-id="7f816-157">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f816-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f816-158">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7f816-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f816-159">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7f816-159">INPUTS</span></span>

### <span data-ttu-id="7f816-160">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="7f816-160">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="7f816-161">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="7f816-161">OUTPUTS</span></span>

### <span data-ttu-id="7f816-162">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IAppResource</span><span class="sxs-lookup"><span data-stu-id="7f816-162">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IAppResource</span></span>

## <span data-ttu-id="7f816-163">NOTES</span><span class="sxs-lookup"><span data-stu-id="7f816-163">NOTES</span></span>

<span data-ttu-id="7f816-164">ALIASES</span><span class="sxs-lookup"><span data-stu-id="7f816-164">ALIASES</span></span>

<span data-ttu-id="7f816-165">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="7f816-165">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="7f816-166">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="7f816-166">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="7f816-167">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="7f816-167">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="7f816-168">INPUTOBJECT <ISpringCloudIdentity> : Parâmetro Identity</span><span class="sxs-lookup"><span data-stu-id="7f816-168">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="7f816-169">`[AppName <String>]`: O nome do recurso App.</span><span class="sxs-lookup"><span data-stu-id="7f816-169">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="7f816-170">`[BindingName <String>]`: O nome do recurso Binding.</span><span class="sxs-lookup"><span data-stu-id="7f816-170">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="7f816-171">`[CertificateName <String>]`: O nome do recurso de certificado.</span><span class="sxs-lookup"><span data-stu-id="7f816-171">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="7f816-172">`[DeploymentName <String>]`: O nome do recurso Deployment.</span><span class="sxs-lookup"><span data-stu-id="7f816-172">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="7f816-173">`[DomainName <String>]`: O nome do recurso de domínio personalizado.</span><span class="sxs-lookup"><span data-stu-id="7f816-173">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="7f816-174">`[Id <String>]`: Caminho da identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="7f816-174">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="7f816-175">`[Location <String>]`: a região</span><span class="sxs-lookup"><span data-stu-id="7f816-175">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="7f816-176">`[ResourceGroupName <String>]`: O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="7f816-176">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="7f816-177">Você pode obter esse valor da API do Gerenciador de Recursos do Azure ou do portal.</span><span class="sxs-lookup"><span data-stu-id="7f816-177">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="7f816-178">`[ServiceName <String>]`: O nome do recurso Service.</span><span class="sxs-lookup"><span data-stu-id="7f816-178">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="7f816-179">`[SubscriptionId <String>]`: Obtém a ID da assinatura que identifica exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="7f816-179">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="7f816-180">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="7f816-180">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="7f816-181">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7f816-181">RELATED LINKS</span></span>


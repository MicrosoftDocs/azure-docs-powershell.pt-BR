---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/get-azspringcloudappdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Get-AzSpringCloudAppDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Get-AzSpringCloudAppDeployment.md
ms.openlocfilehash: d33f649d71a8fb3f4a112ac77937f37d867a24c4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94113942"
---
# <span data-ttu-id="6ecfe-101">Get-AzSpringCloudAppDeployment</span><span class="sxs-lookup"><span data-stu-id="6ecfe-101">Get-AzSpringCloudAppDeployment</span></span>

## <span data-ttu-id="6ecfe-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6ecfe-102">SYNOPSIS</span></span>
<span data-ttu-id="6ecfe-103">Obter uma implantação e suas propriedades.</span><span class="sxs-lookup"><span data-stu-id="6ecfe-103">Get a Deployment and its properties.</span></span>

## <span data-ttu-id="6ecfe-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6ecfe-104">SYNTAX</span></span>

### <span data-ttu-id="6ecfe-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="6ecfe-105">List (Default)</span></span>
```
Get-AzSpringCloudAppDeployment -AppName <String> -ResourceGroupName <String> -ServiceName <String>
 [-SubscriptionId <String[]>] [-Version <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="6ecfe-106">Obter</span><span class="sxs-lookup"><span data-stu-id="6ecfe-106">Get</span></span>
```
Get-AzSpringCloudAppDeployment -AppName <String> -Name <String> -ResourceGroupName <String>
 -ServiceName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="6ecfe-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="6ecfe-107">GetViaIdentity</span></span>
```
Get-AzSpringCloudAppDeployment -InputObject <ISpringCloudIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="6ecfe-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6ecfe-108">DESCRIPTION</span></span>
<span data-ttu-id="6ecfe-109">Obter uma implantação e suas propriedades.</span><span class="sxs-lookup"><span data-stu-id="6ecfe-109">Get a Deployment and its properties.</span></span>

## <span data-ttu-id="6ecfe-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6ecfe-110">EXAMPLES</span></span>

### <span data-ttu-id="6ecfe-111">Exemplo 1: obter o aplicativo de nuvem Spring Deploymeng por nome.</span><span class="sxs-lookup"><span data-stu-id="6ecfe-111">Example 1: Get Spring Cloud App Deploymeng by name.</span></span>
```powershell
PS C:\> Get-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway -DeploymentName default
Active                               : False
AppName                              : gateway
CreatedTime                          :
DeploymentSettingCpu                 : 1
DeploymentSettingEnvironmentVariable : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.DeploymentSettingsEnvironmentVariables
DeploymentSettingInstanceCount       : 1
DeploymentSettingJvmOption           :
DeploymentSettingMemoryInGb          : 1
DeploymentSettingRuntimeVersion      : Java_8
Id                                   : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/spring-cloud-rg/providers/Microsoft.AppPlatform/Spring/spring-cloud-service/apps/gateway/deployments/default
Instance                             : {gateway-default-7-6bd6f87954-nl2wl}
Name                                 : default
ProvisioningState                    : Succeeded
SourceArtifactSelector               :
SourceRelativePath                   : <default>
SourceType                           : Jar
SourceVersion                        :
Status                               : Running
Type                                 : Microsoft.AppPlatform/Spring/apps/deployments
DeploymentSetting                    : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.DeploymentSettings
Property                             : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.DeploymentResourceProperties
Source                               : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.UserSourceInfo
```

<span data-ttu-id="6ecfe-112">Obtenha o aplicativo de nuvem Spring Deploymeng por nome.</span><span class="sxs-lookup"><span data-stu-id="6ecfe-112">Get Spring Cloud App Deploymeng by name.</span></span>

### <span data-ttu-id="6ecfe-113">Exemplo 2: listar toda a implantação em um determinado aplicativo de nuvem Spring.</span><span class="sxs-lookup"><span data-stu-id="6ecfe-113">Example 2: List all the deployment under a given spring cloud app.</span></span>
```powershell
PS C:\> Get-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway
Name    Type
----    ----
default Microsoft.AppPlatform/Spring/apps/deployments
prod    Microsoft.AppPlatform/Spring/apps/deployments
```

<span data-ttu-id="6ecfe-114">Listar toda a implantação em um determinado aplicativo de nuvem Spring.</span><span class="sxs-lookup"><span data-stu-id="6ecfe-114">List all the deployment under a given spring cloud app.</span></span>

## <span data-ttu-id="6ecfe-115">OS</span><span class="sxs-lookup"><span data-stu-id="6ecfe-115">PARAMETERS</span></span>

### <span data-ttu-id="6ecfe-116">-AppName</span><span class="sxs-lookup"><span data-stu-id="6ecfe-116">-AppName</span></span>
<span data-ttu-id="6ecfe-117">O nome do recurso de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6ecfe-117">The name of the App resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ecfe-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ecfe-118">-DefaultProfile</span></span>
<span data-ttu-id="6ecfe-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6ecfe-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6ecfe-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6ecfe-120">-InputObject</span></span>
<span data-ttu-id="6ecfe-121">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="6ecfe-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="6ecfe-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="6ecfe-122">-Name</span></span>
<span data-ttu-id="6ecfe-123">O nome do recurso de implantação.</span><span class="sxs-lookup"><span data-stu-id="6ecfe-123">The name of the Deployment resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: DeploymentName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ecfe-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ecfe-124">-ResourceGroupName</span></span>
<span data-ttu-id="6ecfe-125">O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="6ecfe-125">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="6ecfe-126">Você pode obter esse valor da API do Azure Resource Manager ou do Portal.</span><span class="sxs-lookup"><span data-stu-id="6ecfe-126">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ecfe-127">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="6ecfe-127">-ServiceName</span></span>
<span data-ttu-id="6ecfe-128">O nome do recurso de serviço.</span><span class="sxs-lookup"><span data-stu-id="6ecfe-128">The name of the Service resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ecfe-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6ecfe-129">-SubscriptionId</span></span>
<span data-ttu-id="6ecfe-130">Obtém a ID da assinatura que identifica exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="6ecfe-130">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="6ecfe-131">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="6ecfe-131">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ecfe-132">-Versão</span><span class="sxs-lookup"><span data-stu-id="6ecfe-132">-Version</span></span>
<span data-ttu-id="6ecfe-133">Versão das implantações a serem listadas</span><span class="sxs-lookup"><span data-stu-id="6ecfe-133">Version of the deployments to be listed</span></span>

```yaml
Type: System.String[]
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ecfe-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ecfe-134">CommonParameters</span></span>
<span data-ttu-id="6ecfe-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ecfe-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ecfe-136">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6ecfe-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ecfe-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6ecfe-137">INPUTS</span></span>

### <span data-ttu-id="6ecfe-138">Microsoft. Azure. PowerShell. cmdlets. SpringCloud. Models. ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="6ecfe-138">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="6ecfe-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6ecfe-139">OUTPUTS</span></span>

### <span data-ttu-id="6ecfe-140">Microsoft. Azure. PowerShell. cmdlets. SpringCloud. Models. Api20190501Preview. IDeploymentResource</span><span class="sxs-lookup"><span data-stu-id="6ecfe-140">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.IDeploymentResource</span></span>

## <span data-ttu-id="6ecfe-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6ecfe-141">NOTES</span></span>

<span data-ttu-id="6ecfe-142">ALIASES</span><span class="sxs-lookup"><span data-stu-id="6ecfe-142">ALIASES</span></span>

<span data-ttu-id="6ecfe-143">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="6ecfe-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="6ecfe-144">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="6ecfe-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6ecfe-145">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="6ecfe-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="6ecfe-146">INPUTobject <ISpringCloudIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="6ecfe-146">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="6ecfe-147">`[AppName <String>]`: O nome do recurso de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6ecfe-147">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="6ecfe-148">`[BindingName <String>]`: O nome do recurso de associação.</span><span class="sxs-lookup"><span data-stu-id="6ecfe-148">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="6ecfe-149">`[CertificateName <String>]`: O nome do recurso de certificado.</span><span class="sxs-lookup"><span data-stu-id="6ecfe-149">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="6ecfe-150">`[DeploymentName <String>]`: O nome do recurso de implantação.</span><span class="sxs-lookup"><span data-stu-id="6ecfe-150">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="6ecfe-151">`[DomainName <String>]`: O nome do recurso de domínio personalizado.</span><span class="sxs-lookup"><span data-stu-id="6ecfe-151">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="6ecfe-152">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="6ecfe-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="6ecfe-153">`[Location <String>]`: a região</span><span class="sxs-lookup"><span data-stu-id="6ecfe-153">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="6ecfe-154">`[ResourceGroupName <String>]`: O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="6ecfe-154">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="6ecfe-155">Você pode obter esse valor da API do Azure Resource Manager ou do Portal.</span><span class="sxs-lookup"><span data-stu-id="6ecfe-155">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="6ecfe-156">`[ServiceName <String>]`: O nome do recurso de serviço.</span><span class="sxs-lookup"><span data-stu-id="6ecfe-156">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="6ecfe-157">`[SubscriptionId <String>]`: Obtém a ID de assinatura que identifica exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="6ecfe-157">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="6ecfe-158">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="6ecfe-158">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="6ecfe-159">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6ecfe-159">RELATED LINKS</span></span>


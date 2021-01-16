---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/get-azspringcloudappdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Get-AzSpringCloudAppDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Get-AzSpringCloudAppDeployment.md
ms.openlocfilehash: 3accf4b622f77edb0e3d0cea6fe67bbc1db9ff6c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98263183"
---
# <span data-ttu-id="48403-101">Get-AzSpringCloudAppDeployment</span><span class="sxs-lookup"><span data-stu-id="48403-101">Get-AzSpringCloudAppDeployment</span></span>

## <span data-ttu-id="48403-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="48403-102">SYNOPSIS</span></span>
<span data-ttu-id="48403-103">Obter uma implantação e suas propriedades.</span><span class="sxs-lookup"><span data-stu-id="48403-103">Get a Deployment and its properties.</span></span>

## <span data-ttu-id="48403-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="48403-104">SYNTAX</span></span>

### <span data-ttu-id="48403-105">List1 (padrão)</span><span class="sxs-lookup"><span data-stu-id="48403-105">List1 (Default)</span></span>
```
Get-AzSpringCloudAppDeployment -ResourceGroupName <String> -ServiceName <String> [-SubscriptionId <String[]>]
 [-Version <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="48403-106">Obter</span><span class="sxs-lookup"><span data-stu-id="48403-106">Get</span></span>
```
Get-AzSpringCloudAppDeployment -AppName <String> -Name <String> -ResourceGroupName <String>
 -ServiceName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="48403-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="48403-107">GetViaIdentity</span></span>
```
Get-AzSpringCloudAppDeployment -InputObject <ISpringCloudIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="48403-108">Programação</span><span class="sxs-lookup"><span data-stu-id="48403-108">List</span></span>
```
Get-AzSpringCloudAppDeployment -AppName <String> -ResourceGroupName <String> -ServiceName <String>
 [-SubscriptionId <String[]>] [-Version <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="48403-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="48403-109">DESCRIPTION</span></span>
<span data-ttu-id="48403-110">Obter uma implantação e suas propriedades.</span><span class="sxs-lookup"><span data-stu-id="48403-110">Get a Deployment and its properties.</span></span>

## <span data-ttu-id="48403-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="48403-111">EXAMPLES</span></span>

### <span data-ttu-id="48403-112">Exemplo 1: obter o aplicativo de nuvem Spring Deploymeng por nome.</span><span class="sxs-lookup"><span data-stu-id="48403-112">Example 1: Get Spring Cloud App Deploymeng by name.</span></span>
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

<span data-ttu-id="48403-113">Obtenha o aplicativo de nuvem Spring Deploymeng por nome.</span><span class="sxs-lookup"><span data-stu-id="48403-113">Get Spring Cloud App Deploymeng by name.</span></span>

### <span data-ttu-id="48403-114">Exemplo 2: listar toda a implantação em um determinado aplicativo de nuvem Spring.</span><span class="sxs-lookup"><span data-stu-id="48403-114">Example 2: List all the deployment under a given spring cloud app.</span></span>
```powershell
PS C:\> Get-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway
Name    Type
----    ----
default Microsoft.AppPlatform/Spring/apps/deployments
prod    Microsoft.AppPlatform/Spring/apps/deployments
```

<span data-ttu-id="48403-115">Listar toda a implantação em um determinado aplicativo de nuvem Spring.</span><span class="sxs-lookup"><span data-stu-id="48403-115">List all the deployment under a given spring cloud app.</span></span>

## <span data-ttu-id="48403-116">OS</span><span class="sxs-lookup"><span data-stu-id="48403-116">PARAMETERS</span></span>

### <span data-ttu-id="48403-117">-AppName</span><span class="sxs-lookup"><span data-stu-id="48403-117">-AppName</span></span>
<span data-ttu-id="48403-118">O nome do recurso de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="48403-118">The name of the App resource.</span></span>

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

### <span data-ttu-id="48403-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48403-119">-DefaultProfile</span></span>
<span data-ttu-id="48403-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="48403-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="48403-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="48403-121">-InputObject</span></span>
<span data-ttu-id="48403-122">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="48403-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="48403-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="48403-123">-Name</span></span>
<span data-ttu-id="48403-124">O nome do recurso de implantação.</span><span class="sxs-lookup"><span data-stu-id="48403-124">The name of the Deployment resource.</span></span>

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

### <span data-ttu-id="48403-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48403-125">-ResourceGroupName</span></span>
<span data-ttu-id="48403-126">O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="48403-126">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="48403-127">Você pode obter esse valor da API do Azure Resource Manager ou do Portal.</span><span class="sxs-lookup"><span data-stu-id="48403-127">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List, List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48403-128">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="48403-128">-ServiceName</span></span>
<span data-ttu-id="48403-129">O nome do recurso de serviço.</span><span class="sxs-lookup"><span data-stu-id="48403-129">The name of the Service resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List, List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48403-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="48403-130">-SubscriptionId</span></span>
<span data-ttu-id="48403-131">Obtém a ID da assinatura que identifica exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="48403-131">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="48403-132">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="48403-132">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="48403-133">-Versão</span><span class="sxs-lookup"><span data-stu-id="48403-133">-Version</span></span>
<span data-ttu-id="48403-134">Versão das implantações a serem listadas</span><span class="sxs-lookup"><span data-stu-id="48403-134">Version of the deployments to be listed</span></span>

```yaml
Type: System.String[]
Parameter Sets: List, List1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48403-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48403-135">CommonParameters</span></span>
<span data-ttu-id="48403-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48403-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48403-137">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="48403-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48403-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="48403-138">INPUTS</span></span>

### <span data-ttu-id="48403-139">Microsoft. Azure. PowerShell. cmdlets. SpringCloud. Models. ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="48403-139">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="48403-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="48403-140">OUTPUTS</span></span>

### <span data-ttu-id="48403-141">Microsoft. Azure. PowerShell. cmdlets. SpringCloud. Models. Api20200701. IDeploymentResource</span><span class="sxs-lookup"><span data-stu-id="48403-141">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IDeploymentResource</span></span>

## <span data-ttu-id="48403-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="48403-142">NOTES</span></span>

<span data-ttu-id="48403-143">ALIASES</span><span class="sxs-lookup"><span data-stu-id="48403-143">ALIASES</span></span>

<span data-ttu-id="48403-144">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="48403-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="48403-145">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="48403-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="48403-146">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="48403-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="48403-147">INPUTobject <ISpringCloudIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="48403-147">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="48403-148">`[AppName <String>]`: O nome do recurso de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="48403-148">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="48403-149">`[BindingName <String>]`: O nome do recurso de associação.</span><span class="sxs-lookup"><span data-stu-id="48403-149">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="48403-150">`[CertificateName <String>]`: O nome do recurso de certificado.</span><span class="sxs-lookup"><span data-stu-id="48403-150">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="48403-151">`[DeploymentName <String>]`: O nome do recurso de implantação.</span><span class="sxs-lookup"><span data-stu-id="48403-151">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="48403-152">`[DomainName <String>]`: O nome do recurso de domínio personalizado.</span><span class="sxs-lookup"><span data-stu-id="48403-152">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="48403-153">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="48403-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="48403-154">`[Location <String>]`: a região</span><span class="sxs-lookup"><span data-stu-id="48403-154">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="48403-155">`[ResourceGroupName <String>]`: O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="48403-155">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="48403-156">Você pode obter esse valor da API do Azure Resource Manager ou do Portal.</span><span class="sxs-lookup"><span data-stu-id="48403-156">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="48403-157">`[ServiceName <String>]`: O nome do recurso de serviço.</span><span class="sxs-lookup"><span data-stu-id="48403-157">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="48403-158">`[SubscriptionId <String>]`: Obtém a ID de assinatura que identifica exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="48403-158">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="48403-159">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="48403-159">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="48403-160">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="48403-160">RELATED LINKS</span></span>


---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/get-azspringcloudapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Get-AzSpringCloudApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Get-AzSpringCloudApp.md
ms.openlocfilehash: 43001ca921344d334f91bfa7b594e733a3307d8d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98262405"
---
# <span data-ttu-id="2eac8-101">Get-AzSpringCloudApp</span><span class="sxs-lookup"><span data-stu-id="2eac8-101">Get-AzSpringCloudApp</span></span>

## <span data-ttu-id="2eac8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2eac8-102">SYNOPSIS</span></span>
<span data-ttu-id="2eac8-103">Obter um aplicativo e suas propriedades.</span><span class="sxs-lookup"><span data-stu-id="2eac8-103">Get an App and its properties.</span></span>

## <span data-ttu-id="2eac8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2eac8-104">SYNTAX</span></span>

### <span data-ttu-id="2eac8-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="2eac8-105">List (Default)</span></span>
```
Get-AzSpringCloudApp -ResourceGroupName <String> -ServiceName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="2eac8-106">Obter</span><span class="sxs-lookup"><span data-stu-id="2eac8-106">Get</span></span>
```
Get-AzSpringCloudApp -Name <String> -ResourceGroupName <String> -ServiceName <String>
 [-SubscriptionId <String[]>] [-SyncStatus <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="2eac8-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="2eac8-107">GetViaIdentity</span></span>
```
Get-AzSpringCloudApp -InputObject <ISpringCloudIdentity> [-SyncStatus <String>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="2eac8-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2eac8-108">DESCRIPTION</span></span>
<span data-ttu-id="2eac8-109">Obter um aplicativo e suas propriedades.</span><span class="sxs-lookup"><span data-stu-id="2eac8-109">Get an App and its properties.</span></span>

## <span data-ttu-id="2eac8-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2eac8-110">EXAMPLES</span></span>

### <span data-ttu-id="2eac8-111">Exemplo 1: obter o aplicativo de nuvem Spring por nome.</span><span class="sxs-lookup"><span data-stu-id="2eac8-111">Example 1: Get Spring Cloud App by name.</span></span>
```powershell
PS C:\> Get-AzSpringCloudApp -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway
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

<span data-ttu-id="2eac8-112">Obtenha o aplicativo de nuvem Spring por nome.</span><span class="sxs-lookup"><span data-stu-id="2eac8-112">Get Spring Cloud App by name.</span></span>

### <span data-ttu-id="2eac8-113">Exemplo 2: listar todos o aplicativo em um determinado serviço de nuvem Spring.</span><span class="sxs-lookup"><span data-stu-id="2eac8-113">Example 2: List all the app under a given spring cloud service.</span></span>
```powershell
PS C:\> Get-AzSpringCloudApp -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service
Name            Type                              Location
----            ----                              --------
account-service Microsoft.AppPlatform/Spring/apps eastus
auth-service    Microsoft.AppPlatform/Spring/apps eastus
gateway         Microsoft.AppPlatform/Spring/apps eastus
```

<span data-ttu-id="2eac8-114">Liste todos os aplicativos em um determinado serviço de nuvem Spring.</span><span class="sxs-lookup"><span data-stu-id="2eac8-114">List all the app under a given spring cloud service.</span></span>

## <span data-ttu-id="2eac8-115">OS</span><span class="sxs-lookup"><span data-stu-id="2eac8-115">PARAMETERS</span></span>

### <span data-ttu-id="2eac8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2eac8-116">-DefaultProfile</span></span>
<span data-ttu-id="2eac8-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2eac8-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2eac8-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2eac8-118">-InputObject</span></span>
<span data-ttu-id="2eac8-119">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="2eac8-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="2eac8-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="2eac8-120">-Name</span></span>
<span data-ttu-id="2eac8-121">O nome do recurso de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="2eac8-121">The name of the App resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: AppName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2eac8-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2eac8-122">-ResourceGroupName</span></span>
<span data-ttu-id="2eac8-123">O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="2eac8-123">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="2eac8-124">Você pode obter esse valor da API do Azure Resource Manager ou do Portal.</span><span class="sxs-lookup"><span data-stu-id="2eac8-124">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="2eac8-125">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="2eac8-125">-ServiceName</span></span>
<span data-ttu-id="2eac8-126">O nome do recurso de serviço.</span><span class="sxs-lookup"><span data-stu-id="2eac8-126">The name of the Service resource.</span></span>

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

### <span data-ttu-id="2eac8-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2eac8-127">-SubscriptionId</span></span>
<span data-ttu-id="2eac8-128">Obtém a ID da assinatura que identifica exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="2eac8-128">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="2eac8-129">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="2eac8-129">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="2eac8-130">-SyncStatus</span><span class="sxs-lookup"><span data-stu-id="2eac8-130">-SyncStatus</span></span>
<span data-ttu-id="2eac8-131">Indica se o status de sincronização</span><span class="sxs-lookup"><span data-stu-id="2eac8-131">Indicates whether sync status</span></span>

```yaml
Type: System.String
Parameter Sets: Get, GetViaIdentity
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2eac8-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2eac8-132">CommonParameters</span></span>
<span data-ttu-id="2eac8-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2eac8-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2eac8-134">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2eac8-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2eac8-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2eac8-135">INPUTS</span></span>

### <span data-ttu-id="2eac8-136">Microsoft. Azure. PowerShell. cmdlets. SpringCloud. Models. ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="2eac8-136">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="2eac8-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2eac8-137">OUTPUTS</span></span>

### <span data-ttu-id="2eac8-138">Microsoft. Azure. PowerShell. cmdlets. SpringCloud. Models. Api20200701. IAppResource</span><span class="sxs-lookup"><span data-stu-id="2eac8-138">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IAppResource</span></span>

## <span data-ttu-id="2eac8-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2eac8-139">NOTES</span></span>

<span data-ttu-id="2eac8-140">ALIASES</span><span class="sxs-lookup"><span data-stu-id="2eac8-140">ALIASES</span></span>

<span data-ttu-id="2eac8-141">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="2eac8-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="2eac8-142">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="2eac8-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="2eac8-143">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="2eac8-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="2eac8-144">INPUTobject <ISpringCloudIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="2eac8-144">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="2eac8-145">`[AppName <String>]`: O nome do recurso de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="2eac8-145">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="2eac8-146">`[BindingName <String>]`: O nome do recurso de associação.</span><span class="sxs-lookup"><span data-stu-id="2eac8-146">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="2eac8-147">`[CertificateName <String>]`: O nome do recurso de certificado.</span><span class="sxs-lookup"><span data-stu-id="2eac8-147">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="2eac8-148">`[DeploymentName <String>]`: O nome do recurso de implantação.</span><span class="sxs-lookup"><span data-stu-id="2eac8-148">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="2eac8-149">`[DomainName <String>]`: O nome do recurso de domínio personalizado.</span><span class="sxs-lookup"><span data-stu-id="2eac8-149">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="2eac8-150">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="2eac8-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="2eac8-151">`[Location <String>]`: a região</span><span class="sxs-lookup"><span data-stu-id="2eac8-151">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="2eac8-152">`[ResourceGroupName <String>]`: O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="2eac8-152">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="2eac8-153">Você pode obter esse valor da API do Azure Resource Manager ou do Portal.</span><span class="sxs-lookup"><span data-stu-id="2eac8-153">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="2eac8-154">`[ServiceName <String>]`: O nome do recurso de serviço.</span><span class="sxs-lookup"><span data-stu-id="2eac8-154">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="2eac8-155">`[SubscriptionId <String>]`: Obtém a ID de assinatura que identifica exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="2eac8-155">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="2eac8-156">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="2eac8-156">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="2eac8-157">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2eac8-157">RELATED LINKS</span></span>


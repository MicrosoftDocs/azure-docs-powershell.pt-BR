---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/powershell/module/az.springcloud/get-azspringcloudapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Get-AzSpringCloudApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Get-AzSpringCloudApp.md
ms.openlocfilehash: 62a0398ca117ac623d0b21cc89908b25a4e7e1e2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885800"
---
# <span data-ttu-id="90642-101">Get-AzSpringCloudApp</span><span class="sxs-lookup"><span data-stu-id="90642-101">Get-AzSpringCloudApp</span></span>

## <span data-ttu-id="90642-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="90642-102">SYNOPSIS</span></span>
<span data-ttu-id="90642-103">Obter um Aplicativo e suas propriedades.</span><span class="sxs-lookup"><span data-stu-id="90642-103">Get an App and its properties.</span></span>

## <span data-ttu-id="90642-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="90642-104">SYNTAX</span></span>

### <span data-ttu-id="90642-105">Lista (Padrão)</span><span class="sxs-lookup"><span data-stu-id="90642-105">List (Default)</span></span>
```
Get-AzSpringCloudApp -ResourceGroupName <String> -ServiceName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="90642-106">Obter</span><span class="sxs-lookup"><span data-stu-id="90642-106">Get</span></span>
```
Get-AzSpringCloudApp -Name <String> -ResourceGroupName <String> -ServiceName <String>
 [-SubscriptionId <String[]>] [-SyncStatus <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="90642-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="90642-107">GetViaIdentity</span></span>
```
Get-AzSpringCloudApp -InputObject <ISpringCloudIdentity> [-SyncStatus <String>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="90642-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="90642-108">DESCRIPTION</span></span>
<span data-ttu-id="90642-109">Obter um Aplicativo e suas propriedades.</span><span class="sxs-lookup"><span data-stu-id="90642-109">Get an App and its properties.</span></span>

## <span data-ttu-id="90642-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="90642-110">EXAMPLES</span></span>

### <span data-ttu-id="90642-111">Exemplo 1: Obter o Nome do Aplicativo na Nuvem da Primavera.</span><span class="sxs-lookup"><span data-stu-id="90642-111">Example 1: Get Spring Cloud App by name.</span></span>
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

<span data-ttu-id="90642-112">Obter Spring Cloud App pelo nome.</span><span class="sxs-lookup"><span data-stu-id="90642-112">Get Spring Cloud App by name.</span></span>

### <span data-ttu-id="90642-113">Exemplo 2: listar todo o aplicativo em um determinado serviço de nuvem de mola.</span><span class="sxs-lookup"><span data-stu-id="90642-113">Example 2: List all the app under a given spring cloud service.</span></span>
```powershell
PS C:\> Get-AzSpringCloudApp -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service
Name            Type                              Location
----            ----                              --------
account-service Microsoft.AppPlatform/Spring/apps eastus
auth-service    Microsoft.AppPlatform/Spring/apps eastus
gateway         Microsoft.AppPlatform/Spring/apps eastus
```

<span data-ttu-id="90642-114">Listar todo o aplicativo em um determinado serviço de nuvem de mola.</span><span class="sxs-lookup"><span data-stu-id="90642-114">List all the app under a given spring cloud service.</span></span>

## <span data-ttu-id="90642-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="90642-115">PARAMETERS</span></span>

### <span data-ttu-id="90642-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90642-116">-DefaultProfile</span></span>
<span data-ttu-id="90642-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="90642-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="90642-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="90642-118">-InputObject</span></span>
<span data-ttu-id="90642-119">Parâmetro Identity Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="90642-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="90642-120">-Name</span><span class="sxs-lookup"><span data-stu-id="90642-120">-Name</span></span>
<span data-ttu-id="90642-121">O nome do recurso App.</span><span class="sxs-lookup"><span data-stu-id="90642-121">The name of the App resource.</span></span>

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

### <span data-ttu-id="90642-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90642-122">-ResourceGroupName</span></span>
<span data-ttu-id="90642-123">O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="90642-123">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="90642-124">Você pode obter esse valor da API do Gerenciador de Recursos do Azure ou do portal.</span><span class="sxs-lookup"><span data-stu-id="90642-124">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="90642-125">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="90642-125">-ServiceName</span></span>
<span data-ttu-id="90642-126">O nome do recurso Service.</span><span class="sxs-lookup"><span data-stu-id="90642-126">The name of the Service resource.</span></span>

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

### <span data-ttu-id="90642-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="90642-127">-SubscriptionId</span></span>
<span data-ttu-id="90642-128">Obtém a ID da assinatura que identifica exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="90642-128">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="90642-129">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="90642-129">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="90642-130">-SyncStatus</span><span class="sxs-lookup"><span data-stu-id="90642-130">-SyncStatus</span></span>
<span data-ttu-id="90642-131">Indica se o status da sincronização</span><span class="sxs-lookup"><span data-stu-id="90642-131">Indicates whether sync status</span></span>

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

### <span data-ttu-id="90642-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90642-132">CommonParameters</span></span>
<span data-ttu-id="90642-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90642-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90642-134">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="90642-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90642-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="90642-135">INPUTS</span></span>

### <span data-ttu-id="90642-136">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="90642-136">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="90642-137">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="90642-137">OUTPUTS</span></span>

### <span data-ttu-id="90642-138">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IAppResource</span><span class="sxs-lookup"><span data-stu-id="90642-138">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IAppResource</span></span>

## <span data-ttu-id="90642-139">NOTES</span><span class="sxs-lookup"><span data-stu-id="90642-139">NOTES</span></span>

<span data-ttu-id="90642-140">ALIASES</span><span class="sxs-lookup"><span data-stu-id="90642-140">ALIASES</span></span>

<span data-ttu-id="90642-141">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="90642-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="90642-142">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="90642-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="90642-143">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="90642-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="90642-144">INPUTOBJECT <ISpringCloudIdentity> : Parâmetro Identity</span><span class="sxs-lookup"><span data-stu-id="90642-144">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="90642-145">`[AppName <String>]`: O nome do recurso App.</span><span class="sxs-lookup"><span data-stu-id="90642-145">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="90642-146">`[BindingName <String>]`: O nome do recurso Binding.</span><span class="sxs-lookup"><span data-stu-id="90642-146">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="90642-147">`[CertificateName <String>]`: O nome do recurso de certificado.</span><span class="sxs-lookup"><span data-stu-id="90642-147">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="90642-148">`[DeploymentName <String>]`: O nome do recurso Deployment.</span><span class="sxs-lookup"><span data-stu-id="90642-148">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="90642-149">`[DomainName <String>]`: O nome do recurso de domínio personalizado.</span><span class="sxs-lookup"><span data-stu-id="90642-149">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="90642-150">`[Id <String>]`: Caminho da identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="90642-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="90642-151">`[Location <String>]`: a região</span><span class="sxs-lookup"><span data-stu-id="90642-151">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="90642-152">`[ResourceGroupName <String>]`: O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="90642-152">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="90642-153">Você pode obter esse valor da API do Gerenciador de Recursos do Azure ou do portal.</span><span class="sxs-lookup"><span data-stu-id="90642-153">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="90642-154">`[ServiceName <String>]`: O nome do recurso Service.</span><span class="sxs-lookup"><span data-stu-id="90642-154">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="90642-155">`[SubscriptionId <String>]`: Obtém a ID da assinatura que identifica exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="90642-155">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="90642-156">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="90642-156">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="90642-157">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="90642-157">RELATED LINKS</span></span>


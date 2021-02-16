---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/en-us/powershell/module/az.cloudservice/get-azcloudservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Get-AzCloudService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Get-AzCloudService.md
ms.openlocfilehash: faab9e645f05b8b661b03911bcba517e770f4d78
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117906"
---
# <span data-ttu-id="f4d9f-101">Get-AzCloudService</span><span class="sxs-lookup"><span data-stu-id="f4d9f-101">Get-AzCloudService</span></span>

## <span data-ttu-id="f4d9f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f4d9f-102">SYNOPSIS</span></span>
<span data-ttu-id="f4d9f-103">Exibir informações sobre um serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="f4d9f-103">Display information about a cloud service.</span></span>

## <span data-ttu-id="f4d9f-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f4d9f-104">SYNTAX</span></span>

### <span data-ttu-id="f4d9f-105">Lista (Padrão)</span><span class="sxs-lookup"><span data-stu-id="f4d9f-105">List (Default)</span></span>
```
Get-AzCloudService [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="f4d9f-106">Obter</span><span class="sxs-lookup"><span data-stu-id="f4d9f-106">Get</span></span>
```
Get-AzCloudService -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="f4d9f-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="f4d9f-107">GetViaIdentity</span></span>
```
Get-AzCloudService -InputObject <ICloudServiceIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="f4d9f-108">Lista1</span><span class="sxs-lookup"><span data-stu-id="f4d9f-108">List1</span></span>
```
Get-AzCloudService -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="f4d9f-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="f4d9f-109">DESCRIPTION</span></span>
<span data-ttu-id="f4d9f-110">Exibir informações sobre um serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="f4d9f-110">Display information about a cloud service.</span></span>

## <span data-ttu-id="f4d9f-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f4d9f-111">EXAMPLES</span></span>

### <span data-ttu-id="f4d9f-112">Exemplo 1: Obter todos os serviços de nuvem em um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="f4d9f-112">Example 1: Get all cloud service under a resource group</span></span>
```powershell
PS C:\> Get-AzCloudService -ResourceGroupName "ContosOrg"

ResourceGroupName Name              Location    ProvisioningState
----------------- ----              --------    -----------------
ContosOrg         ContosoCS         eastus2euap Succeeded
ContosOrg         ContosoCSTest     eastus2euap Failed
```

<span data-ttu-id="f4d9f-113">Esse comando obtém todos os serviços de nuvem no grupo de recursos chamado ContosOrg</span><span class="sxs-lookup"><span data-stu-id="f4d9f-113">This command gets all cloud services in resource group named ContosOrg</span></span>

### <span data-ttu-id="f4d9f-114">Exemplo 2: Obter serviço de nuvem</span><span class="sxs-lookup"><span data-stu-id="f4d9f-114">Example 2: Get cloud service</span></span>
```powershell
PS C:\> Get-AzCloudService -ResourceGroupName "ContosOrg" -CloudServiceName "ContosoCS"

ResourceGroupName Name              Location    ProvisioningState
----------------- ----              --------    -----------------
ContosOrg         ContosoCS         eastus2euap Succeeded

PS C:\> $cloudService = Get-AzCloudService -ResourceGroupName "ContosOrg" -CloudServiceName "ContosoCS"
PS C:\> $cloudService | Format-List
ResourceGroupName : ContosOrg
Configuration     : xxxxxxxx
ConfigurationUrl  :
ExtensionProfile  : xxxxxxxx
Id                : xxxxxxxx
Location          : East US
Name              : ContosoCS
NetworkProfile    : xxxxxxxx
OSProfile         : xxxxxxxx
PackageUrl        : xxxxxxxx
ProvisioningState : Succeeded
RoleProfile       : xxxxxxxx
StartCloudService :
Tag               : {
                      "Owner": "Contos"
                    }
Type              : Microsoft.Compute/cloudServices
UniqueId          : xxxxxxxx
UpgradeMode       : Auto

```

<span data-ttu-id="f4d9f-115">Esse comando obtém um serviço de nuvem chamado ContosoCS que pertence ao grupo de recursos chamado ContosOrg.</span><span class="sxs-lookup"><span data-stu-id="f4d9f-115">This command gets cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

## <span data-ttu-id="f4d9f-116">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f4d9f-116">PARAMETERS</span></span>

### <span data-ttu-id="f4d9f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4d9f-117">-DefaultProfile</span></span>
<span data-ttu-id="f4d9f-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f4d9f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f4d9f-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f4d9f-119">-InputObject</span></span>
<span data-ttu-id="f4d9f-120">Parâmetro de Identidade Para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="f4d9f-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f4d9f-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="f4d9f-121">-Name</span></span>
<span data-ttu-id="f4d9f-122">Nome do serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="f4d9f-122">Name of the cloud service.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: CloudServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4d9f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4d9f-123">-ResourceGroupName</span></span>
<span data-ttu-id="f4d9f-124">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f4d9f-124">Name of the resource group.</span></span>

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

### <span data-ttu-id="f4d9f-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f4d9f-125">-SubscriptionId</span></span>
<span data-ttu-id="f4d9f-126">Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="f4d9f-126">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="f4d9f-127">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="f4d9f-127">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="f4d9f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4d9f-128">CommonParameters</span></span>
<span data-ttu-id="f4d9f-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4d9f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4d9f-130">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f4d9f-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4d9f-131">Entradas</span><span class="sxs-lookup"><span data-stu-id="f4d9f-131">INPUTS</span></span>

### <span data-ttu-id="f4d9f-132">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="f4d9f-132">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span></span>

## <span data-ttu-id="f4d9f-133">Saídas</span><span class="sxs-lookup"><span data-stu-id="f4d9f-133">OUTPUTS</span></span>

### <span data-ttu-id="f4d9f-134">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.ICloudService</span><span class="sxs-lookup"><span data-stu-id="f4d9f-134">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.ICloudService</span></span>

## <span data-ttu-id="f4d9f-135">Notas</span><span class="sxs-lookup"><span data-stu-id="f4d9f-135">NOTES</span></span>

<span data-ttu-id="f4d9f-136">Aliases</span><span class="sxs-lookup"><span data-stu-id="f4d9f-136">ALIASES</span></span>

<span data-ttu-id="f4d9f-137">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="f4d9f-137">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f4d9f-138">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="f4d9f-138">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f4d9f-139">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="f4d9f-139">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f4d9f-140">INPUTOBJECT: <ICloudServiceIdentity> Parâmetro de Identidade</span><span class="sxs-lookup"><span data-stu-id="f4d9f-140">INPUTOBJECT <ICloudServiceIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f4d9f-141">`[CloudServiceName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="f4d9f-141">`[CloudServiceName <String>]`:</span></span> 
  - <span data-ttu-id="f4d9f-142">`[Id <String>]`: Caminho de identidade de recursos</span><span class="sxs-lookup"><span data-stu-id="f4d9f-142">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f4d9f-143">`[ResourceGroupName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="f4d9f-143">`[ResourceGroupName <String>]`:</span></span> 
  - <span data-ttu-id="f4d9f-144">`[RoleInstanceName <String>]`: Nome da instância da função.</span><span class="sxs-lookup"><span data-stu-id="f4d9f-144">`[RoleInstanceName <String>]`: Name of the role instance.</span></span>
  - <span data-ttu-id="f4d9f-145">`[RoleName <String>]`: nome da função.</span><span class="sxs-lookup"><span data-stu-id="f4d9f-145">`[RoleName <String>]`: Name of the role.</span></span>
  - <span data-ttu-id="f4d9f-146">`[SubscriptionId <String>]`: Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="f4d9f-146">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="f4d9f-147">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="f4d9f-147">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="f4d9f-148">`[UpdateDomain <Int32?>]`: especifica um valor inteiro que identifica o domínio de atualização.</span><span class="sxs-lookup"><span data-stu-id="f4d9f-148">`[UpdateDomain <Int32?>]`: Specifies an integer value that identifies the update domain.</span></span> <span data-ttu-id="f4d9f-149">Os domínios de atualização são identificados com um índice baseado em zero: o primeiro domínio de atualização tem uma ID de 0, o segundo tem uma ID de 1 e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="f4d9f-149">Update domains are identified with a zero-based index: the first update domain has an ID of 0, the second has an ID of 1, and so on.</span></span>

## <span data-ttu-id="f4d9f-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f4d9f-150">RELATED LINKS</span></span>


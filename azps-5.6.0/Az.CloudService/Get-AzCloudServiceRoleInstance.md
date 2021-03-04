---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/powershell/module/az.cloudservice/get-azcloudserviceroleinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Get-AzCloudServiceRoleInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Get-AzCloudServiceRoleInstance.md
ms.openlocfilehash: 516bc63d7866ffd8a3c16fd224a49697c0cc972f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891877"
---
# <span data-ttu-id="19381-101">Get-AzCloudServiceRoleInstance</span><span class="sxs-lookup"><span data-stu-id="19381-101">Get-AzCloudServiceRoleInstance</span></span>

## <span data-ttu-id="19381-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="19381-102">SYNOPSIS</span></span>
<span data-ttu-id="19381-103">Obtém uma instância de função de um serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="19381-103">Gets a role instance from a cloud service.</span></span>

## <span data-ttu-id="19381-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="19381-104">SYNTAX</span></span>

### <span data-ttu-id="19381-105">Lista (Padrão)</span><span class="sxs-lookup"><span data-stu-id="19381-105">List (Default)</span></span>
```
Get-AzCloudServiceRoleInstance -CloudServiceName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-Expand <InstanceViewTypes>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="19381-106">Obter</span><span class="sxs-lookup"><span data-stu-id="19381-106">Get</span></span>
```
Get-AzCloudServiceRoleInstance -CloudServiceName <String> -ResourceGroupName <String>
 -RoleInstanceName <String> [-SubscriptionId <String[]>] [-Expand <InstanceViewTypes>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="19381-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="19381-107">GetViaIdentity</span></span>
```
Get-AzCloudServiceRoleInstance -InputObject <ICloudServiceIdentity> [-Expand <InstanceViewTypes>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="19381-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="19381-108">DESCRIPTION</span></span>
<span data-ttu-id="19381-109">Obtém uma instância de função de um serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="19381-109">Gets a role instance from a cloud service.</span></span>

## <span data-ttu-id="19381-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="19381-110">EXAMPLES</span></span>

### <span data-ttu-id="19381-111">Exemplo 1: Obter todas as instâncias de função</span><span class="sxs-lookup"><span data-stu-id="19381-111">Example 1: Get all role instances</span></span>
```powershell
PS C:\> Get-AzCloudServiceRoleInstance -ResourceGroupName "ContosOrg" -CloudServiceName "ContosoCS"

Name                    Location    SkuName        SkuTier
----                    --------    -------        -------
ContosoFrontEnd_IN_0    eastus2euap Standard_D1_v2 Standard
ContosoFrontEnd_IN_1    eastus2euap Standard_D1_v2 Standard
ContosoBackEnd_IN_1     eastus2euap Standard_D1_v2 Standard
ContosoBackEnd_IN_1     eastus2euap Standard_D1_v2 Standard

```

<span data-ttu-id="19381-112">Este comando obtém as propriedades de todas as instâncias de função do serviço de nuvem chamada ContosoCS que pertence ao grupo de recursos chamado ContosOrg.</span><span class="sxs-lookup"><span data-stu-id="19381-112">This command gets the properties of all role instances of cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

### <span data-ttu-id="19381-113">Exemplo 2: Obter propriedades para instância de função única</span><span class="sxs-lookup"><span data-stu-id="19381-113">Example 2: Get properties for single role instance</span></span>
```powershell
PS C:\> Get-AzCloudServiceRoleInstance -ResourceGroupName "ContosOrg" -CloudServiceName "ContosoCS" -RoleInstanceName "ContosoFrontEnd_IN_0"

Name                    Location    SkuName        SkuTier
----                    --------    -------        -------
ContosoFrontEnd_IN_0    eastus2euap Standard_D1_v2 Standard

```

<span data-ttu-id="19381-114">Este comando obtém as propriedades da instância de função chamada ContosoFrontEnd_IN_0 do serviço de nuvem chamado ContosoCS que pertence ao grupo de recursos chamado ContosOrg.</span><span class="sxs-lookup"><span data-stu-id="19381-114">This command gets the properties of the role instance named ContosoFrontEnd_IN_0 of cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

## <span data-ttu-id="19381-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="19381-115">PARAMETERS</span></span>

### <span data-ttu-id="19381-116">-CloudServiceName</span><span class="sxs-lookup"><span data-stu-id="19381-116">-CloudServiceName</span></span>
<span data-ttu-id="19381-117">.</span><span class="sxs-lookup"><span data-stu-id="19381-117">.</span></span>

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

### <span data-ttu-id="19381-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19381-118">-DefaultProfile</span></span>
<span data-ttu-id="19381-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="19381-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="19381-120">-Expand</span><span class="sxs-lookup"><span data-stu-id="19381-120">-Expand</span></span>
<span data-ttu-id="19381-121">A expressão expandir a ser aplicada à operação.</span><span class="sxs-lookup"><span data-stu-id="19381-121">The expand expression to apply to the operation.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Support.InstanceViewTypes
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19381-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="19381-122">-InputObject</span></span>
<span data-ttu-id="19381-123">Parâmetro Identity Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="19381-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="19381-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19381-124">-ResourceGroupName</span></span>
<span data-ttu-id="19381-125">.</span><span class="sxs-lookup"><span data-stu-id="19381-125">.</span></span>

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

### <span data-ttu-id="19381-126">-RoleInstanceName</span><span class="sxs-lookup"><span data-stu-id="19381-126">-RoleInstanceName</span></span>
<span data-ttu-id="19381-127">Nome da instância da função.</span><span class="sxs-lookup"><span data-stu-id="19381-127">Name of the role instance.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19381-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="19381-128">-SubscriptionId</span></span>
<span data-ttu-id="19381-129">Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="19381-129">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="19381-130">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="19381-130">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="19381-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19381-131">CommonParameters</span></span>
<span data-ttu-id="19381-132">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19381-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19381-133">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="19381-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19381-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="19381-134">INPUTS</span></span>

### <span data-ttu-id="19381-135">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="19381-135">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span></span>

## <span data-ttu-id="19381-136">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="19381-136">OUTPUTS</span></span>

### <span data-ttu-id="19381-137">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.IRoleInstance</span><span class="sxs-lookup"><span data-stu-id="19381-137">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.IRoleInstance</span></span>

## <span data-ttu-id="19381-138">NOTES</span><span class="sxs-lookup"><span data-stu-id="19381-138">NOTES</span></span>

<span data-ttu-id="19381-139">ALIASES</span><span class="sxs-lookup"><span data-stu-id="19381-139">ALIASES</span></span>

<span data-ttu-id="19381-140">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="19381-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="19381-141">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="19381-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="19381-142">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="19381-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="19381-143">INPUTOBJECT <ICloudServiceIdentity> : Parâmetro Identity</span><span class="sxs-lookup"><span data-stu-id="19381-143">INPUTOBJECT <ICloudServiceIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="19381-144">`[CloudServiceName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="19381-144">`[CloudServiceName <String>]`:</span></span> 
  - <span data-ttu-id="19381-145">`[Id <String>]`: Caminho da identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="19381-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="19381-146">`[ResourceGroupName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="19381-146">`[ResourceGroupName <String>]`:</span></span> 
  - <span data-ttu-id="19381-147">`[RoleInstanceName <String>]`: Nome da instância da função.</span><span class="sxs-lookup"><span data-stu-id="19381-147">`[RoleInstanceName <String>]`: Name of the role instance.</span></span>
  - <span data-ttu-id="19381-148">`[RoleName <String>]`: Nome da função.</span><span class="sxs-lookup"><span data-stu-id="19381-148">`[RoleName <String>]`: Name of the role.</span></span>
  - <span data-ttu-id="19381-149">`[SubscriptionId <String>]`: Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="19381-149">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="19381-150">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="19381-150">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="19381-151">`[UpdateDomain <Int32?>]`: Especifica um valor inteiro que identifica o domínio de atualização.</span><span class="sxs-lookup"><span data-stu-id="19381-151">`[UpdateDomain <Int32?>]`: Specifies an integer value that identifies the update domain.</span></span> <span data-ttu-id="19381-152">Os domínios de atualização são identificados com um índice baseado em zero: o primeiro domínio de atualização tem uma ID de 0, o segundo tem uma ID de 1 e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="19381-152">Update domains are identified with a zero-based index: the first update domain has an ID of 0, the second has an ID of 1, and so on.</span></span>

## <span data-ttu-id="19381-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="19381-153">RELATED LINKS</span></span>


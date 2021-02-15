---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/en-us/powershell/module/az.cloudservice/get-azcloudserviceroleinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Get-AzCloudServiceRoleInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Get-AzCloudServiceRoleInstance.md
ms.openlocfilehash: 55416adbd2ffbcb816e5652ad33e1777594fdcb6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112167"
---
# <span data-ttu-id="aff95-101">Get-AzCloudServiceRoleInstance</span><span class="sxs-lookup"><span data-stu-id="aff95-101">Get-AzCloudServiceRoleInstance</span></span>

## <span data-ttu-id="aff95-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="aff95-102">SYNOPSIS</span></span>
<span data-ttu-id="aff95-103">Obtém uma instância de função de um serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="aff95-103">Gets a role instance from a cloud service.</span></span>

## <span data-ttu-id="aff95-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="aff95-104">SYNTAX</span></span>

### <span data-ttu-id="aff95-105">Lista (Padrão)</span><span class="sxs-lookup"><span data-stu-id="aff95-105">List (Default)</span></span>
```
Get-AzCloudServiceRoleInstance -CloudServiceName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-Expand <InstanceViewTypes>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="aff95-106">Obter</span><span class="sxs-lookup"><span data-stu-id="aff95-106">Get</span></span>
```
Get-AzCloudServiceRoleInstance -CloudServiceName <String> -ResourceGroupName <String>
 -RoleInstanceName <String> [-SubscriptionId <String[]>] [-Expand <InstanceViewTypes>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="aff95-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="aff95-107">GetViaIdentity</span></span>
```
Get-AzCloudServiceRoleInstance -InputObject <ICloudServiceIdentity> [-Expand <InstanceViewTypes>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="aff95-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="aff95-108">DESCRIPTION</span></span>
<span data-ttu-id="aff95-109">Obtém uma instância de função de um serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="aff95-109">Gets a role instance from a cloud service.</span></span>

## <span data-ttu-id="aff95-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="aff95-110">EXAMPLES</span></span>

### <span data-ttu-id="aff95-111">Exemplo 1: Obter todas as instâncias de função</span><span class="sxs-lookup"><span data-stu-id="aff95-111">Example 1: Get all role instances</span></span>
```powershell
PS C:\> Get-AzCloudServiceRoleInstance -ResourceGroupName "ContosOrg" -CloudServiceName "ContosoCS"

Name                    Location    SkuName        SkuTier
----                    --------    -------        -------
ContosoFrontEnd_IN_0    eastus2euap Standard_D1_v2 Standard
ContosoFrontEnd_IN_1    eastus2euap Standard_D1_v2 Standard
ContosoBackEnd_IN_1     eastus2euap Standard_D1_v2 Standard
ContosoBackEnd_IN_1     eastus2euap Standard_D1_v2 Standard

```

<span data-ttu-id="aff95-112">Esse comando obtém as propriedades de todas as instâncias de função do serviço de nuvem chamada ContosoCS que pertencem ao grupo de recursos chamado ContosOrg.</span><span class="sxs-lookup"><span data-stu-id="aff95-112">This command gets the properties of all role instances of cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

### <span data-ttu-id="aff95-113">Exemplo 2: Obter propriedades para uma instância de função única</span><span class="sxs-lookup"><span data-stu-id="aff95-113">Example 2: Get properties for single role instance</span></span>
```powershell
PS C:\> Get-AzCloudServiceRoleInstance -ResourceGroupName "ContosOrg" -CloudServiceName "ContosoCS" -RoleInstanceName "ContosoFrontEnd_IN_0"

Name                    Location    SkuName        SkuTier
----                    --------    -------        -------
ContosoFrontEnd_IN_0    eastus2euap Standard_D1_v2 Standard

```

<span data-ttu-id="aff95-114">Esse comando obtém as propriedades da instância de função chamada ContosoFrontEnd_IN_0 do serviço de nuvem chamado ContosoCS que pertence ao grupo de recursos chamado ContosOrg.</span><span class="sxs-lookup"><span data-stu-id="aff95-114">This command gets the properties of the role instance named ContosoFrontEnd_IN_0 of cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

## <span data-ttu-id="aff95-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="aff95-115">PARAMETERS</span></span>

### <span data-ttu-id="aff95-116">-CloudServiceName</span><span class="sxs-lookup"><span data-stu-id="aff95-116">-CloudServiceName</span></span>
<span data-ttu-id="aff95-117">.</span><span class="sxs-lookup"><span data-stu-id="aff95-117">.</span></span>

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

### <span data-ttu-id="aff95-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aff95-118">-DefaultProfile</span></span>
<span data-ttu-id="aff95-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="aff95-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aff95-120">-Expandir</span><span class="sxs-lookup"><span data-stu-id="aff95-120">-Expand</span></span>
<span data-ttu-id="aff95-121">A expressão de expansão a ser aplicada à operação.</span><span class="sxs-lookup"><span data-stu-id="aff95-121">The expand expression to apply to the operation.</span></span>

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

### <span data-ttu-id="aff95-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="aff95-122">-InputObject</span></span>
<span data-ttu-id="aff95-123">Parâmetro de Identidade para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="aff95-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="aff95-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aff95-124">-ResourceGroupName</span></span>
<span data-ttu-id="aff95-125">.</span><span class="sxs-lookup"><span data-stu-id="aff95-125">.</span></span>

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

### <span data-ttu-id="aff95-126">-RoleInstanceName</span><span class="sxs-lookup"><span data-stu-id="aff95-126">-RoleInstanceName</span></span>
<span data-ttu-id="aff95-127">Nome da instância da função.</span><span class="sxs-lookup"><span data-stu-id="aff95-127">Name of the role instance.</span></span>

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

### <span data-ttu-id="aff95-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="aff95-128">-SubscriptionId</span></span>
<span data-ttu-id="aff95-129">Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="aff95-129">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="aff95-130">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="aff95-130">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="aff95-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aff95-131">CommonParameters</span></span>
<span data-ttu-id="aff95-132">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aff95-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aff95-133">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="aff95-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aff95-134">Entradas</span><span class="sxs-lookup"><span data-stu-id="aff95-134">INPUTS</span></span>

### <span data-ttu-id="aff95-135">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="aff95-135">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span></span>

## <span data-ttu-id="aff95-136">Saídas</span><span class="sxs-lookup"><span data-stu-id="aff95-136">OUTPUTS</span></span>

### <span data-ttu-id="aff95-137">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.IRoleInstance</span><span class="sxs-lookup"><span data-stu-id="aff95-137">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.IRoleInstance</span></span>

## <span data-ttu-id="aff95-138">Notas</span><span class="sxs-lookup"><span data-stu-id="aff95-138">NOTES</span></span>

<span data-ttu-id="aff95-139">Aliases</span><span class="sxs-lookup"><span data-stu-id="aff95-139">ALIASES</span></span>

<span data-ttu-id="aff95-140">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="aff95-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="aff95-141">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="aff95-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="aff95-142">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="aff95-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="aff95-143">INPUTOBJECT: <ICloudServiceIdentity> Parâmetro de Identidade</span><span class="sxs-lookup"><span data-stu-id="aff95-143">INPUTOBJECT <ICloudServiceIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="aff95-144">`[CloudServiceName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="aff95-144">`[CloudServiceName <String>]`:</span></span> 
  - <span data-ttu-id="aff95-145">`[Id <String>]`: Caminho de identidade de recursos</span><span class="sxs-lookup"><span data-stu-id="aff95-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="aff95-146">`[ResourceGroupName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="aff95-146">`[ResourceGroupName <String>]`:</span></span> 
  - <span data-ttu-id="aff95-147">`[RoleInstanceName <String>]`: Nome da instância da função.</span><span class="sxs-lookup"><span data-stu-id="aff95-147">`[RoleInstanceName <String>]`: Name of the role instance.</span></span>
  - <span data-ttu-id="aff95-148">`[RoleName <String>]`: nome da função.</span><span class="sxs-lookup"><span data-stu-id="aff95-148">`[RoleName <String>]`: Name of the role.</span></span>
  - <span data-ttu-id="aff95-149">`[SubscriptionId <String>]`: Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="aff95-149">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="aff95-150">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="aff95-150">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="aff95-151">`[UpdateDomain <Int32?>]`: especifica um valor inteiro que identifica o domínio de atualização.</span><span class="sxs-lookup"><span data-stu-id="aff95-151">`[UpdateDomain <Int32?>]`: Specifies an integer value that identifies the update domain.</span></span> <span data-ttu-id="aff95-152">Os domínios de atualização são identificados com um índice baseado em zero: o primeiro domínio de atualização tem uma ID de 0, o segundo tem uma ID de 1 e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="aff95-152">Update domains are identified with a zero-based index: the first update domain has an ID of 0, the second has an ID of 1, and so on.</span></span>

## <span data-ttu-id="aff95-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="aff95-153">RELATED LINKS</span></span>


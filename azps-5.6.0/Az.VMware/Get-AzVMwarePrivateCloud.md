---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/powershell/module/az.vmware/get-azvmwareprivatecloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Get-AzVMwarePrivateCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Get-AzVMwarePrivateCloud.md
ms.openlocfilehash: ae53ac56d60d61340e2592233901556a0e1d6b62
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890044"
---
# <span data-ttu-id="ff75a-101">Get-AzVMWarePrivateCloud</span><span class="sxs-lookup"><span data-stu-id="ff75a-101">Get-AzVMWarePrivateCloud</span></span>

## <span data-ttu-id="ff75a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ff75a-102">SYNOPSIS</span></span>
<span data-ttu-id="ff75a-103">Obter uma nuvem privada</span><span class="sxs-lookup"><span data-stu-id="ff75a-103">Get a private cloud</span></span>

## <span data-ttu-id="ff75a-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="ff75a-104">SYNTAX</span></span>

### <span data-ttu-id="ff75a-105">List1 (Padrão)</span><span class="sxs-lookup"><span data-stu-id="ff75a-105">List1 (Default)</span></span>
```
Get-AzVMWarePrivateCloud [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="ff75a-106">Obter</span><span class="sxs-lookup"><span data-stu-id="ff75a-106">Get</span></span>
```
Get-AzVMWarePrivateCloud -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="ff75a-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="ff75a-107">GetViaIdentity</span></span>
```
Get-AzVMWarePrivateCloud -InputObject <IVMWareIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="ff75a-108">Listar</span><span class="sxs-lookup"><span data-stu-id="ff75a-108">List</span></span>
```
Get-AzVMWarePrivateCloud -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="ff75a-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="ff75a-109">DESCRIPTION</span></span>
<span data-ttu-id="ff75a-110">Obter uma nuvem privada</span><span class="sxs-lookup"><span data-stu-id="ff75a-110">Get a private cloud</span></span>

## <span data-ttu-id="ff75a-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ff75a-111">EXAMPLES</span></span>

### <span data-ttu-id="ff75a-112">Exemplo 1: Listar nuvem privada sob assinatura</span><span class="sxs-lookup"><span data-stu-id="ff75a-112">Example 1: List private cloud under subscription</span></span>
```powershell
PS C:\> Get-AzVMWarePrivateCloud

Location      Name            Type
--------      ----            ----
australiaeast azps-test-cloud Microsoft.AVS/privateClouds
```

<span data-ttu-id="ff75a-113">Listar nuvem privada sob assinatura</span><span class="sxs-lookup"><span data-stu-id="ff75a-113">List private cloud under subscription</span></span>

### <span data-ttu-id="ff75a-114">Exemplo 2: Listar nuvem privada no grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="ff75a-114">Example 2: List private cloud under resource group</span></span>
```powershell
PS C:\> Get-AzVMWarePrivateCloud -ResourceGroupName azps-test-group

Location      Name            Type
--------      ----            ----
australiaeast azps-test-cloud Microsoft.AVS/privateClouds
```

<span data-ttu-id="ff75a-115">Listar nuvem privada em grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="ff75a-115">List private cloud under resource group</span></span>

### <span data-ttu-id="ff75a-116">Exemplo 3: Obter nuvem privada</span><span class="sxs-lookup"><span data-stu-id="ff75a-116">Example 3: Get private cloud</span></span>
```powershell
PS C:\> Get-AzVMWarePrivateCloud -ResourceGroupName azps-test-group -Name azps-test-cloud

Location      Name            Type
--------      ----            ----
australiaeast azps-test-cloud Microsoft.AVS/privateClouds
```

<span data-ttu-id="ff75a-117">Obter nuvem privada</span><span class="sxs-lookup"><span data-stu-id="ff75a-117">Get private cloud</span></span>

## <span data-ttu-id="ff75a-118">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="ff75a-118">PARAMETERS</span></span>

### <span data-ttu-id="ff75a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff75a-119">-DefaultProfile</span></span>
<span data-ttu-id="ff75a-120">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ff75a-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ff75a-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ff75a-121">-InputObject</span></span>
<span data-ttu-id="ff75a-122">Parâmetro Identity Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="ff75a-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ff75a-123">-Name</span><span class="sxs-lookup"><span data-stu-id="ff75a-123">-Name</span></span>
<span data-ttu-id="ff75a-124">Nome da nuvem privada</span><span class="sxs-lookup"><span data-stu-id="ff75a-124">Name of the private cloud</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: PrivateCloudName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff75a-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff75a-125">-ResourceGroupName</span></span>
<span data-ttu-id="ff75a-126">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ff75a-126">The name of the resource group.</span></span>
<span data-ttu-id="ff75a-127">O nome é insensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="ff75a-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="ff75a-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ff75a-128">-SubscriptionId</span></span>
<span data-ttu-id="ff75a-129">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="ff75a-129">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="ff75a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff75a-130">CommonParameters</span></span>
<span data-ttu-id="ff75a-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff75a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff75a-132">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ff75a-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff75a-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ff75a-133">INPUTS</span></span>

### <span data-ttu-id="ff75a-134">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span><span class="sxs-lookup"><span data-stu-id="ff75a-134">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span></span>

## <span data-ttu-id="ff75a-135">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="ff75a-135">OUTPUTS</span></span>

### <span data-ttu-id="ff75a-136">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IPrivateCloud</span><span class="sxs-lookup"><span data-stu-id="ff75a-136">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IPrivateCloud</span></span>

## <span data-ttu-id="ff75a-137">NOTES</span><span class="sxs-lookup"><span data-stu-id="ff75a-137">NOTES</span></span>

<span data-ttu-id="ff75a-138">ALIASES</span><span class="sxs-lookup"><span data-stu-id="ff75a-138">ALIASES</span></span>

<span data-ttu-id="ff75a-139">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="ff75a-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ff75a-140">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="ff75a-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ff75a-141">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ff75a-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ff75a-142">INPUTOBJECT <IVMWareIdentity> : Parâmetro Identity</span><span class="sxs-lookup"><span data-stu-id="ff75a-142">INPUTOBJECT <IVMWareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ff75a-143">`[AuthorizationName <String>]`: Nome da Autorização de Circuito Expresso na nuvem privada</span><span class="sxs-lookup"><span data-stu-id="ff75a-143">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="ff75a-144">`[ClusterName <String>]`: Nome do cluster na nuvem privada</span><span class="sxs-lookup"><span data-stu-id="ff75a-144">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="ff75a-145">`[HcxEnterpriseSiteName <String>]`: Nome do Site empresarial HCX na nuvem privada</span><span class="sxs-lookup"><span data-stu-id="ff75a-145">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="ff75a-146">`[Id <String>]`: Caminho da identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="ff75a-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ff75a-147">`[Location <String>]`: Região do Azure</span><span class="sxs-lookup"><span data-stu-id="ff75a-147">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="ff75a-148">`[PrivateCloudName <String>]`: Nome da nuvem privada</span><span class="sxs-lookup"><span data-stu-id="ff75a-148">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="ff75a-149">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ff75a-149">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="ff75a-150">O nome é insensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="ff75a-150">The name is case insensitive.</span></span>
  - <span data-ttu-id="ff75a-151">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="ff75a-151">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="ff75a-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ff75a-152">RELATED LINKS</span></span>


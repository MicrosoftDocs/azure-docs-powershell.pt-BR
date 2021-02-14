---
external help file: ''
Module Name: Az.VMware
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/get-azvmwareprivatecloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Get-AzVMwarePrivateCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Get-AzVMwarePrivateCloud.md
ms.openlocfilehash: 707e7e4e702912d4d838913cb7ca030fef914e58
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116031"
---
# <span data-ttu-id="281f2-101">Get-AzVMwarePrivateCloud</span><span class="sxs-lookup"><span data-stu-id="281f2-101">Get-AzVMwarePrivateCloud</span></span>

## <span data-ttu-id="281f2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="281f2-102">SYNOPSIS</span></span>
<span data-ttu-id="281f2-103">Obter uma nuvem privada</span><span class="sxs-lookup"><span data-stu-id="281f2-103">Get a private cloud</span></span>

## <span data-ttu-id="281f2-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="281f2-104">SYNTAX</span></span>

### <span data-ttu-id="281f2-105">Lista1 (Padrão)</span><span class="sxs-lookup"><span data-stu-id="281f2-105">List1 (Default)</span></span>
```
Get-AzVMwarePrivateCloud [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="281f2-106">Obter</span><span class="sxs-lookup"><span data-stu-id="281f2-106">Get</span></span>
```
Get-AzVMwarePrivateCloud -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="281f2-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="281f2-107">GetViaIdentity</span></span>
```
Get-AzVMwarePrivateCloud -InputObject <IVMwareIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="281f2-108">Lista</span><span class="sxs-lookup"><span data-stu-id="281f2-108">List</span></span>
```
Get-AzVMwarePrivateCloud -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="281f2-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="281f2-109">DESCRIPTION</span></span>
<span data-ttu-id="281f2-110">Obter uma nuvem privada</span><span class="sxs-lookup"><span data-stu-id="281f2-110">Get a private cloud</span></span>

## <span data-ttu-id="281f2-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="281f2-111">EXAMPLES</span></span>

### <span data-ttu-id="281f2-112">Exemplo 1: Listar nuvem privada sob assinatura</span><span class="sxs-lookup"><span data-stu-id="281f2-112">Example 1: List private cloud under subscription</span></span>
```powershell
PS C:\> Get-AzVMwarePrivateCloud

Location      Name            Type
--------      ----            ----
australiaeast azps-test-cloud Microsoft.AVS/privateClouds
```

<span data-ttu-id="281f2-113">Listar nuvem privada em assinatura</span><span class="sxs-lookup"><span data-stu-id="281f2-113">List private cloud under subscription</span></span>

### <span data-ttu-id="281f2-114">Exemplo 2: Listar nuvem privada no grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="281f2-114">Example 2: List private cloud under resource group</span></span>
```powershell
PS C:\> Get-AzVMwarePrivateCloud -ResourceGroupName azps-test-group

Location      Name            Type
--------      ----            ----
australiaeast azps-test-cloud Microsoft.AVS/privateClouds
```

<span data-ttu-id="281f2-115">Listar nuvem privada no grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="281f2-115">List private cloud under resource group</span></span>

### <span data-ttu-id="281f2-116">Exemplo 3: Obter nuvem privada</span><span class="sxs-lookup"><span data-stu-id="281f2-116">Example 3: Get private cloud</span></span>
```powershell
PS C:\> Get-AzVMwarePrivateCloud -ResourceGroupName azps-test-group -Name azps-test-cloud

Location      Name            Type
--------      ----            ----
australiaeast azps-test-cloud Microsoft.AVS/privateClouds
```

<span data-ttu-id="281f2-117">Obter nuvem privada</span><span class="sxs-lookup"><span data-stu-id="281f2-117">Get private cloud</span></span>

## <span data-ttu-id="281f2-118">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="281f2-118">PARAMETERS</span></span>

### <span data-ttu-id="281f2-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="281f2-119">-DefaultProfile</span></span>
<span data-ttu-id="281f2-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="281f2-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="281f2-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="281f2-121">-InputObject</span></span>
<span data-ttu-id="281f2-122">Parâmetro de Identidade para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="281f2-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.IVMwareIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="281f2-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="281f2-123">-Name</span></span>
<span data-ttu-id="281f2-124">Nome da nuvem privada</span><span class="sxs-lookup"><span data-stu-id="281f2-124">Name of the private cloud</span></span>

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

### <span data-ttu-id="281f2-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="281f2-125">-ResourceGroupName</span></span>
<span data-ttu-id="281f2-126">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="281f2-126">The name of the resource group.</span></span>
<span data-ttu-id="281f2-127">O nome não é sensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="281f2-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="281f2-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="281f2-128">-SubscriptionId</span></span>
<span data-ttu-id="281f2-129">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="281f2-129">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="281f2-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="281f2-130">CommonParameters</span></span>
<span data-ttu-id="281f2-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="281f2-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="281f2-132">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="281f2-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="281f2-133">Entradas</span><span class="sxs-lookup"><span data-stu-id="281f2-133">INPUTS</span></span>

### <span data-ttu-id="281f2-134">Microsoft.Azure.PowerShell.Cmdlets.V Ltd.Models.IV Ltd.</span><span class="sxs-lookup"><span data-stu-id="281f2-134">Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.IVMwareIdentity</span></span>

## <span data-ttu-id="281f2-135">Saídas</span><span class="sxs-lookup"><span data-stu-id="281f2-135">OUTPUTS</span></span>

### <span data-ttu-id="281f2-136">Microsoft.Azure.PowerShell.Cmdlets.VCloud.Models.Api20200320.IPrivateCloud</span><span class="sxs-lookup"><span data-stu-id="281f2-136">Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.Api20200320.IPrivateCloud</span></span>

## <span data-ttu-id="281f2-137">Notas</span><span class="sxs-lookup"><span data-stu-id="281f2-137">NOTES</span></span>

<span data-ttu-id="281f2-138">Aliases</span><span class="sxs-lookup"><span data-stu-id="281f2-138">ALIASES</span></span>

<span data-ttu-id="281f2-139">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="281f2-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="281f2-140">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="281f2-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="281f2-141">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="281f2-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="281f2-142">INPUTOBJECT: <IVMwareIdentity> Parâmetro de Identidade</span><span class="sxs-lookup"><span data-stu-id="281f2-142">INPUTOBJECT <IVMwareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="281f2-143">`[AuthorizationName <String>]`: Nome da Autorização de Circuito do ExpressRoute na nuvem privada</span><span class="sxs-lookup"><span data-stu-id="281f2-143">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="281f2-144">`[ClusterName <String>]`: Nome do cluster na nuvem privada</span><span class="sxs-lookup"><span data-stu-id="281f2-144">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="281f2-145">`[HcxEnterpriseSiteName <String>]`: Nome do Site Corporativo HCX na nuvem privada</span><span class="sxs-lookup"><span data-stu-id="281f2-145">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="281f2-146">`[Id <String>]`: Caminho de identidade de recursos</span><span class="sxs-lookup"><span data-stu-id="281f2-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="281f2-147">`[Location <String>]`: região do Azure</span><span class="sxs-lookup"><span data-stu-id="281f2-147">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="281f2-148">`[PrivateCloudName <String>]`: Nome da nuvem privada</span><span class="sxs-lookup"><span data-stu-id="281f2-148">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="281f2-149">`[ResourceGroupName <String>]`: o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="281f2-149">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="281f2-150">O nome não é sensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="281f2-150">The name is case insensitive.</span></span>
  - <span data-ttu-id="281f2-151">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="281f2-151">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="281f2-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="281f2-152">RELATED LINKS</span></span>


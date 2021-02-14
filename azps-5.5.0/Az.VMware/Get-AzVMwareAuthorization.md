---
external help file: ''
Module Name: Az.VMware
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/get-azvmwareauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Get-AzVMwareAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Get-AzVMwareAuthorization.md
ms.openlocfilehash: f4e4ea13f6e3fd46b1defa8dbf327024cb7557d6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116032"
---
# <span data-ttu-id="1aebd-101">Get-AzVMwareAuthorization</span><span class="sxs-lookup"><span data-stu-id="1aebd-101">Get-AzVMwareAuthorization</span></span>

## <span data-ttu-id="1aebd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1aebd-102">SYNOPSIS</span></span>
<span data-ttu-id="1aebd-103">Obter uma Autorização de Circuito do ExpressRoute por nome em uma nuvem privada</span><span class="sxs-lookup"><span data-stu-id="1aebd-103">Get an ExpressRoute Circuit Authorization by name in a private cloud</span></span>

## <span data-ttu-id="1aebd-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1aebd-104">SYNTAX</span></span>

### <span data-ttu-id="1aebd-105">Lista (Padrão)</span><span class="sxs-lookup"><span data-stu-id="1aebd-105">List (Default)</span></span>
```
Get-AzVMwareAuthorization -PrivateCloudName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="1aebd-106">Obter</span><span class="sxs-lookup"><span data-stu-id="1aebd-106">Get</span></span>
```
Get-AzVMwareAuthorization -Name <String> -PrivateCloudName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="1aebd-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="1aebd-107">GetViaIdentity</span></span>
```
Get-AzVMwareAuthorization -InputObject <IVMwareIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="1aebd-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="1aebd-108">DESCRIPTION</span></span>
<span data-ttu-id="1aebd-109">Obter uma Autorização de Circuito do ExpressRoute por nome em uma nuvem privada</span><span class="sxs-lookup"><span data-stu-id="1aebd-109">Get an ExpressRoute Circuit Authorization by name in a private cloud</span></span>

## <span data-ttu-id="1aebd-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="1aebd-110">EXAMPLES</span></span>

### <span data-ttu-id="1aebd-111">Exemplo 1: Obter autorização</span><span class="sxs-lookup"><span data-stu-id="1aebd-111">Example 1: Get authorization</span></span>
```powershell
PS C:\> Get-AzVMwareAuthorization -Name azps-test-auth -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group



Name           Type
----           ----
azps-test-auth Microsoft.AVS/privateClouds/authorizations
```

<span data-ttu-id="1aebd-112">Este cmdlet obtém autorização `azps-test-auth` em nuvem privada `azps-test-cloud`</span><span class="sxs-lookup"><span data-stu-id="1aebd-112">This cmdlet gets authorization `azps-test-auth` under private cloud `azps-test-cloud`</span></span>

### <span data-ttu-id="1aebd-113">Exemplo 2: Autorização de lista</span><span class="sxs-lookup"><span data-stu-id="1aebd-113">Example 2: List authorization</span></span>
```powershell
PS C:\> Get-AzVMwareAuthorization -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group



Name           Type
----           ----
azps-test-auth Microsoft.AVS/privateClouds/authorizations
```

<span data-ttu-id="1aebd-114">Este cmdlet lista autorização `azps-test-auth` em nuvem privada `azps-test-cloud`</span><span class="sxs-lookup"><span data-stu-id="1aebd-114">This cmdlet lists authorization `azps-test-auth` under private cloud `azps-test-cloud`</span></span>

## <span data-ttu-id="1aebd-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1aebd-115">PARAMETERS</span></span>

### <span data-ttu-id="1aebd-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1aebd-116">-DefaultProfile</span></span>
<span data-ttu-id="1aebd-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1aebd-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1aebd-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1aebd-118">-InputObject</span></span>
<span data-ttu-id="1aebd-119">Parâmetro de Identidade para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="1aebd-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="1aebd-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="1aebd-120">-Name</span></span>
<span data-ttu-id="1aebd-121">Nome da Autorização de Circuito do ExpressRoute na nuvem privada</span><span class="sxs-lookup"><span data-stu-id="1aebd-121">Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: AuthorizationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1aebd-122">-PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="1aebd-122">-PrivateCloudName</span></span>
<span data-ttu-id="1aebd-123">Nome da nuvem privada</span><span class="sxs-lookup"><span data-stu-id="1aebd-123">Name of the private cloud</span></span>

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

### <span data-ttu-id="1aebd-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1aebd-124">-ResourceGroupName</span></span>
<span data-ttu-id="1aebd-125">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="1aebd-125">The name of the resource group.</span></span>
<span data-ttu-id="1aebd-126">O nome não é sensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="1aebd-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="1aebd-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1aebd-127">-SubscriptionId</span></span>
<span data-ttu-id="1aebd-128">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="1aebd-128">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="1aebd-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1aebd-129">CommonParameters</span></span>
<span data-ttu-id="1aebd-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1aebd-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1aebd-131">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1aebd-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1aebd-132">Entradas</span><span class="sxs-lookup"><span data-stu-id="1aebd-132">INPUTS</span></span>

### <span data-ttu-id="1aebd-133">Microsoft.Azure.PowerShell.Cmdlets.V Ltd.Models.IV Ltd.</span><span class="sxs-lookup"><span data-stu-id="1aebd-133">Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.IVMwareIdentity</span></span>

## <span data-ttu-id="1aebd-134">Saídas</span><span class="sxs-lookup"><span data-stu-id="1aebd-134">OUTPUTS</span></span>

### <span data-ttu-id="1aebd-135">Microsoft.Azure.PowerShell.Cmdlets.V Ltd.Models.Api20200320.IExpressRouteAuthorization</span><span class="sxs-lookup"><span data-stu-id="1aebd-135">Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.Api20200320.IExpressRouteAuthorization</span></span>

## <span data-ttu-id="1aebd-136">Notas</span><span class="sxs-lookup"><span data-stu-id="1aebd-136">NOTES</span></span>

<span data-ttu-id="1aebd-137">Aliases</span><span class="sxs-lookup"><span data-stu-id="1aebd-137">ALIASES</span></span>

<span data-ttu-id="1aebd-138">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="1aebd-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="1aebd-139">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="1aebd-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="1aebd-140">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="1aebd-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="1aebd-141">INPUTOBJECT: <IVMwareIdentity> Parâmetro de Identidade</span><span class="sxs-lookup"><span data-stu-id="1aebd-141">INPUTOBJECT <IVMwareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="1aebd-142">`[AuthorizationName <String>]`: Nome da Autorização de Circuito do ExpressRoute na nuvem privada</span><span class="sxs-lookup"><span data-stu-id="1aebd-142">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="1aebd-143">`[ClusterName <String>]`: Nome do cluster na nuvem privada</span><span class="sxs-lookup"><span data-stu-id="1aebd-143">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="1aebd-144">`[HcxEnterpriseSiteName <String>]`: Nome do Site Corporativo HCX na nuvem privada</span><span class="sxs-lookup"><span data-stu-id="1aebd-144">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="1aebd-145">`[Id <String>]`: Caminho de identidade de recursos</span><span class="sxs-lookup"><span data-stu-id="1aebd-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="1aebd-146">`[Location <String>]`: região do Azure</span><span class="sxs-lookup"><span data-stu-id="1aebd-146">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="1aebd-147">`[PrivateCloudName <String>]`: Nome da nuvem privada</span><span class="sxs-lookup"><span data-stu-id="1aebd-147">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="1aebd-148">`[ResourceGroupName <String>]`: o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="1aebd-148">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="1aebd-149">O nome não é sensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="1aebd-149">The name is case insensitive.</span></span>
  - <span data-ttu-id="1aebd-150">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="1aebd-150">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="1aebd-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1aebd-151">RELATED LINKS</span></span>


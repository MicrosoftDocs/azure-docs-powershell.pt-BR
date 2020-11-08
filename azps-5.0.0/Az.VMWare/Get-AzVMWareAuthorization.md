---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/get-azvmwareauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Get-AzVMWareAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Get-AzVMWareAuthorization.md
ms.openlocfilehash: fc89f62711744ad1e6bd7182eeb61fffd0478eaf
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94116310"
---
# <span data-ttu-id="b17fd-101">Get-AzVMWareAuthorization</span><span class="sxs-lookup"><span data-stu-id="b17fd-101">Get-AzVMWareAuthorization</span></span>

## <span data-ttu-id="b17fd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b17fd-102">SYNOPSIS</span></span>
<span data-ttu-id="b17fd-103">Obter uma autorização de circuito do ExpressRoute por nome em uma nuvem privada</span><span class="sxs-lookup"><span data-stu-id="b17fd-103">Get an ExpressRoute Circuit Authorization by name in a private cloud</span></span>

## <span data-ttu-id="b17fd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b17fd-104">SYNTAX</span></span>

### <span data-ttu-id="b17fd-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="b17fd-105">List (Default)</span></span>
```
Get-AzVMWareAuthorization -PrivateCloudName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="b17fd-106">Obter</span><span class="sxs-lookup"><span data-stu-id="b17fd-106">Get</span></span>
```
Get-AzVMWareAuthorization -Name <String> -PrivateCloudName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="b17fd-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="b17fd-107">GetViaIdentity</span></span>
```
Get-AzVMWareAuthorization -InputObject <IVMWareIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="b17fd-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b17fd-108">DESCRIPTION</span></span>
<span data-ttu-id="b17fd-109">Obter uma autorização de circuito do ExpressRoute por nome em uma nuvem privada</span><span class="sxs-lookup"><span data-stu-id="b17fd-109">Get an ExpressRoute Circuit Authorization by name in a private cloud</span></span>

## <span data-ttu-id="b17fd-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b17fd-110">EXAMPLES</span></span>

### <span data-ttu-id="b17fd-111">Exemplo 1: obter autorização</span><span class="sxs-lookup"><span data-stu-id="b17fd-111">Example 1: Get authorization</span></span>
```powershell
PS C:\> Get-AzVMWareAuthorization -Name azps-test-auth -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group



Name           Type
----           ----
azps-test-auth Microsoft.AVS/privateClouds/authorizations
```

<span data-ttu-id="b17fd-112">Este cmdlet obtém autorização `azps-test-auth` em nuvem privada `azps-test-cloud`</span><span class="sxs-lookup"><span data-stu-id="b17fd-112">This cmdlet gets authorization `azps-test-auth` under private cloud `azps-test-cloud`</span></span>

### <span data-ttu-id="b17fd-113">Exemplo 2: listar a autorização</span><span class="sxs-lookup"><span data-stu-id="b17fd-113">Example 2: List authorization</span></span>
```powershell
PS C:\> Get-AzVMWareAuthorization -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group



Name           Type
----           ----
azps-test-auth Microsoft.AVS/privateClouds/authorizations
```

<span data-ttu-id="b17fd-114">Este cmdlet lista a autorização `azps-test-auth` em nuvem privada `azps-test-cloud`</span><span class="sxs-lookup"><span data-stu-id="b17fd-114">This cmdlet lists authorization `azps-test-auth` under private cloud `azps-test-cloud`</span></span>

## <span data-ttu-id="b17fd-115">OS</span><span class="sxs-lookup"><span data-stu-id="b17fd-115">PARAMETERS</span></span>

### <span data-ttu-id="b17fd-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b17fd-116">-DefaultProfile</span></span>
<span data-ttu-id="b17fd-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b17fd-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b17fd-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b17fd-118">-InputObject</span></span>
<span data-ttu-id="b17fd-119">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="b17fd-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="b17fd-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="b17fd-120">-Name</span></span>
<span data-ttu-id="b17fd-121">Nome da autorização de circuito do ExpressRoute na nuvem privada</span><span class="sxs-lookup"><span data-stu-id="b17fd-121">Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>

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

### <span data-ttu-id="b17fd-122">-PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="b17fd-122">-PrivateCloudName</span></span>
<span data-ttu-id="b17fd-123">Nome da nuvem privada</span><span class="sxs-lookup"><span data-stu-id="b17fd-123">Name of the private cloud</span></span>

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

### <span data-ttu-id="b17fd-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b17fd-124">-ResourceGroupName</span></span>
<span data-ttu-id="b17fd-125">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b17fd-125">The name of the resource group.</span></span>
<span data-ttu-id="b17fd-126">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="b17fd-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="b17fd-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b17fd-127">-SubscriptionId</span></span>
<span data-ttu-id="b17fd-128">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="b17fd-128">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="b17fd-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b17fd-129">CommonParameters</span></span>
<span data-ttu-id="b17fd-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b17fd-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b17fd-131">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b17fd-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b17fd-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b17fd-132">INPUTS</span></span>

### <span data-ttu-id="b17fd-133">Microsoft. Azure. PowerShell. cmdlets. VMWare. Models. IVMWareIdentity</span><span class="sxs-lookup"><span data-stu-id="b17fd-133">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span></span>

## <span data-ttu-id="b17fd-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b17fd-134">OUTPUTS</span></span>

### <span data-ttu-id="b17fd-135">Microsoft. Azure. PowerShell. cmdlets. VMWare. Models. Api20200320. IExpressRouteAuthorization</span><span class="sxs-lookup"><span data-stu-id="b17fd-135">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IExpressRouteAuthorization</span></span>

## <span data-ttu-id="b17fd-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b17fd-136">NOTES</span></span>

<span data-ttu-id="b17fd-137">ALIASES</span><span class="sxs-lookup"><span data-stu-id="b17fd-137">ALIASES</span></span>

<span data-ttu-id="b17fd-138">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="b17fd-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b17fd-139">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="b17fd-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b17fd-140">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b17fd-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b17fd-141">INPUTobject <IVMWareIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="b17fd-141">INPUTOBJECT <IVMWareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b17fd-142">`[AuthorizationName <String>]`: Nome da autorização de circuito do ExpressRoute na nuvem privada</span><span class="sxs-lookup"><span data-stu-id="b17fd-142">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="b17fd-143">`[ClusterName <String>]`: Nome do cluster na nuvem privada</span><span class="sxs-lookup"><span data-stu-id="b17fd-143">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="b17fd-144">`[HcxEnterpriseSiteName <String>]`: Nome do site da empresa HCX na nuvem privada</span><span class="sxs-lookup"><span data-stu-id="b17fd-144">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="b17fd-145">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="b17fd-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b17fd-146">`[Location <String>]`: Região do Azure</span><span class="sxs-lookup"><span data-stu-id="b17fd-146">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="b17fd-147">`[PrivateCloudName <String>]`: Nome da nuvem privada</span><span class="sxs-lookup"><span data-stu-id="b17fd-147">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="b17fd-148">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b17fd-148">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="b17fd-149">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="b17fd-149">The name is case insensitive.</span></span>
  - <span data-ttu-id="b17fd-150">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="b17fd-150">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="b17fd-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b17fd-151">RELATED LINKS</span></span>


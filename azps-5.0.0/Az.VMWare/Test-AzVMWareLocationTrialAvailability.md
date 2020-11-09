---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/test-azvmwarelocationtrialavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Test-AzVMWareLocationTrialAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Test-AzVMWareLocationTrialAvailability.md
ms.openlocfilehash: 942ac0b4a8bca964e88c7dfd327fe460f249a915
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94284143"
---
# <span data-ttu-id="ba82f-101">Test-AzVMWareLocationTrialAvailability</span><span class="sxs-lookup"><span data-stu-id="ba82f-101">Test-AzVMWareLocationTrialAvailability</span></span>

## <span data-ttu-id="ba82f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ba82f-102">SYNOPSIS</span></span>
<span data-ttu-id="ba82f-103">Retornar o status de avaliação da assinatura por região</span><span class="sxs-lookup"><span data-stu-id="ba82f-103">Return trial status for subscription by region</span></span>

## <span data-ttu-id="ba82f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ba82f-104">SYNTAX</span></span>

### <span data-ttu-id="ba82f-105">Verificar (padrão)</span><span class="sxs-lookup"><span data-stu-id="ba82f-105">Check (Default)</span></span>
```
Test-AzVMWareLocationTrialAvailability -Location <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="ba82f-106">CheckViaIdentity</span><span class="sxs-lookup"><span data-stu-id="ba82f-106">CheckViaIdentity</span></span>
```
Test-AzVMWareLocationTrialAvailability -InputObject <IVMWareIdentity> [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ba82f-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ba82f-107">DESCRIPTION</span></span>
<span data-ttu-id="ba82f-108">Retornar o status de avaliação da assinatura por região</span><span class="sxs-lookup"><span data-stu-id="ba82f-108">Return trial status for subscription by region</span></span>

## <span data-ttu-id="ba82f-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ba82f-109">EXAMPLES</span></span>

### <span data-ttu-id="ba82f-110">Exemplo 1: verificar a disponibilidade da avaliação</span><span class="sxs-lookup"><span data-stu-id="ba82f-110">Example 1: Check trial availability</span></span>
```powershell
PS C:\> Test-AzVMWareLocationTrialAvailability -Location australiaeast

AvailableHost Status
------------- ------
0             TrialDisabled
```

<span data-ttu-id="ba82f-111">Verificar a disponibilidade da avaliação</span><span class="sxs-lookup"><span data-stu-id="ba82f-111">Check trial availability</span></span>

## <span data-ttu-id="ba82f-112">OS</span><span class="sxs-lookup"><span data-stu-id="ba82f-112">PARAMETERS</span></span>

### <span data-ttu-id="ba82f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba82f-113">-DefaultProfile</span></span>
<span data-ttu-id="ba82f-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ba82f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ba82f-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ba82f-115">-InputObject</span></span>
<span data-ttu-id="ba82f-116">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="ba82f-116">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity
Parameter Sets: CheckViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ba82f-117">-Local</span><span class="sxs-lookup"><span data-stu-id="ba82f-117">-Location</span></span>
<span data-ttu-id="ba82f-118">Região do Azure</span><span class="sxs-lookup"><span data-stu-id="ba82f-118">Azure region</span></span>

```yaml
Type: System.String
Parameter Sets: Check
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba82f-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ba82f-119">-SubscriptionId</span></span>
<span data-ttu-id="ba82f-120">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="ba82f-120">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Check
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba82f-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="ba82f-121">-Confirm</span></span>
<span data-ttu-id="ba82f-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ba82f-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba82f-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba82f-123">-WhatIf</span></span>
<span data-ttu-id="ba82f-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ba82f-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ba82f-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ba82f-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba82f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba82f-126">CommonParameters</span></span>
<span data-ttu-id="ba82f-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba82f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba82f-128">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ba82f-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba82f-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ba82f-129">INPUTS</span></span>

### <span data-ttu-id="ba82f-130">Microsoft. Azure. PowerShell. cmdlets. VMWare. Models. IVMWareIdentity</span><span class="sxs-lookup"><span data-stu-id="ba82f-130">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span></span>

## <span data-ttu-id="ba82f-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ba82f-131">OUTPUTS</span></span>

### <span data-ttu-id="ba82f-132">Microsoft. Azure. PowerShell. cmdlets. VMWare. Models. Api20200320. ITrial</span><span class="sxs-lookup"><span data-stu-id="ba82f-132">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.ITrial</span></span>

## <span data-ttu-id="ba82f-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ba82f-133">NOTES</span></span>

<span data-ttu-id="ba82f-134">ALIASES</span><span class="sxs-lookup"><span data-stu-id="ba82f-134">ALIASES</span></span>

<span data-ttu-id="ba82f-135">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="ba82f-135">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ba82f-136">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="ba82f-136">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ba82f-137">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ba82f-137">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ba82f-138">INPUTobject <IVMWareIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="ba82f-138">INPUTOBJECT <IVMWareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ba82f-139">`[AuthorizationName <String>]`: Nome da autorização de circuito do ExpressRoute na nuvem privada</span><span class="sxs-lookup"><span data-stu-id="ba82f-139">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="ba82f-140">`[ClusterName <String>]`: Nome do cluster na nuvem privada</span><span class="sxs-lookup"><span data-stu-id="ba82f-140">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="ba82f-141">`[HcxEnterpriseSiteName <String>]`: Nome do site da empresa HCX na nuvem privada</span><span class="sxs-lookup"><span data-stu-id="ba82f-141">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="ba82f-142">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="ba82f-142">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ba82f-143">`[Location <String>]`: Região do Azure</span><span class="sxs-lookup"><span data-stu-id="ba82f-143">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="ba82f-144">`[PrivateCloudName <String>]`: Nome da nuvem privada</span><span class="sxs-lookup"><span data-stu-id="ba82f-144">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="ba82f-145">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ba82f-145">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="ba82f-146">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="ba82f-146">The name is case insensitive.</span></span>
  - <span data-ttu-id="ba82f-147">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="ba82f-147">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="ba82f-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ba82f-148">RELATED LINKS</span></span>


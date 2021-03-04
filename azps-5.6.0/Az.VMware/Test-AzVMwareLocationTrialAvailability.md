---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/powershell/module/az.vmware/test-azvmwarelocationtrialavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Test-AzVMwareLocationTrialAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Test-AzVMwareLocationTrialAvailability.md
ms.openlocfilehash: 133dc4dd259025556ab5f8dd3b848ae70a5101c7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890040"
---
# <span data-ttu-id="2fdba-101">Test-AzVMWareLocationTrialAvailability</span><span class="sxs-lookup"><span data-stu-id="2fdba-101">Test-AzVMWareLocationTrialAvailability</span></span>

## <span data-ttu-id="2fdba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2fdba-102">SYNOPSIS</span></span>
<span data-ttu-id="2fdba-103">Retornar o status de avaliação para assinatura por região</span><span class="sxs-lookup"><span data-stu-id="2fdba-103">Return trial status for subscription by region</span></span>

## <span data-ttu-id="2fdba-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="2fdba-104">SYNTAX</span></span>

### <span data-ttu-id="2fdba-105">Verificar (Padrão)</span><span class="sxs-lookup"><span data-stu-id="2fdba-105">Check (Default)</span></span>
```
Test-AzVMWareLocationTrialAvailability -Location <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="2fdba-106">CheckViaIdentity</span><span class="sxs-lookup"><span data-stu-id="2fdba-106">CheckViaIdentity</span></span>
```
Test-AzVMWareLocationTrialAvailability -InputObject <IVMWareIdentity> [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="2fdba-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="2fdba-107">DESCRIPTION</span></span>
<span data-ttu-id="2fdba-108">Retornar o status de avaliação para assinatura por região</span><span class="sxs-lookup"><span data-stu-id="2fdba-108">Return trial status for subscription by region</span></span>

## <span data-ttu-id="2fdba-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2fdba-109">EXAMPLES</span></span>

### <span data-ttu-id="2fdba-110">Exemplo 1: verificar a disponibilidade de avaliação</span><span class="sxs-lookup"><span data-stu-id="2fdba-110">Example 1: Check trial availability</span></span>
```powershell
PS C:\> Test-AzVMWareLocationTrialAvailability -Location australiaeast

AvailableHost Status
------------- ------
0             TrialDisabled
```

<span data-ttu-id="2fdba-111">Verificar a disponibilidade de avaliação</span><span class="sxs-lookup"><span data-stu-id="2fdba-111">Check trial availability</span></span>

## <span data-ttu-id="2fdba-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="2fdba-112">PARAMETERS</span></span>

### <span data-ttu-id="2fdba-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2fdba-113">-DefaultProfile</span></span>
<span data-ttu-id="2fdba-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2fdba-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2fdba-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2fdba-115">-InputObject</span></span>
<span data-ttu-id="2fdba-116">Parâmetro Identity Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="2fdba-116">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="2fdba-117">-Location</span><span class="sxs-lookup"><span data-stu-id="2fdba-117">-Location</span></span>
<span data-ttu-id="2fdba-118">Região do Azure</span><span class="sxs-lookup"><span data-stu-id="2fdba-118">Azure region</span></span>

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

### <span data-ttu-id="2fdba-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2fdba-119">-SubscriptionId</span></span>
<span data-ttu-id="2fdba-120">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="2fdba-120">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="2fdba-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2fdba-121">-Confirm</span></span>
<span data-ttu-id="2fdba-122">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2fdba-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2fdba-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2fdba-123">-WhatIf</span></span>
<span data-ttu-id="2fdba-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2fdba-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2fdba-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2fdba-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2fdba-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2fdba-126">CommonParameters</span></span>
<span data-ttu-id="2fdba-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2fdba-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2fdba-128">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2fdba-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2fdba-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2fdba-129">INPUTS</span></span>

### <span data-ttu-id="2fdba-130">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span><span class="sxs-lookup"><span data-stu-id="2fdba-130">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span></span>

## <span data-ttu-id="2fdba-131">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="2fdba-131">OUTPUTS</span></span>

### <span data-ttu-id="2fdba-132">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.ITrial</span><span class="sxs-lookup"><span data-stu-id="2fdba-132">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.ITrial</span></span>

## <span data-ttu-id="2fdba-133">NOTES</span><span class="sxs-lookup"><span data-stu-id="2fdba-133">NOTES</span></span>

<span data-ttu-id="2fdba-134">ALIASES</span><span class="sxs-lookup"><span data-stu-id="2fdba-134">ALIASES</span></span>

<span data-ttu-id="2fdba-135">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="2fdba-135">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="2fdba-136">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="2fdba-136">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="2fdba-137">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="2fdba-137">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="2fdba-138">INPUTOBJECT <IVMWareIdentity> : Parâmetro Identity</span><span class="sxs-lookup"><span data-stu-id="2fdba-138">INPUTOBJECT <IVMWareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="2fdba-139">`[AuthorizationName <String>]`: Nome da Autorização de Circuito Expresso na nuvem privada</span><span class="sxs-lookup"><span data-stu-id="2fdba-139">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="2fdba-140">`[ClusterName <String>]`: Nome do cluster na nuvem privada</span><span class="sxs-lookup"><span data-stu-id="2fdba-140">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="2fdba-141">`[HcxEnterpriseSiteName <String>]`: Nome do Site empresarial HCX na nuvem privada</span><span class="sxs-lookup"><span data-stu-id="2fdba-141">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="2fdba-142">`[Id <String>]`: Caminho da identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="2fdba-142">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="2fdba-143">`[Location <String>]`: Região do Azure</span><span class="sxs-lookup"><span data-stu-id="2fdba-143">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="2fdba-144">`[PrivateCloudName <String>]`: Nome da nuvem privada</span><span class="sxs-lookup"><span data-stu-id="2fdba-144">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="2fdba-145">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="2fdba-145">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="2fdba-146">O nome é insensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="2fdba-146">The name is case insensitive.</span></span>
  - <span data-ttu-id="2fdba-147">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="2fdba-147">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="2fdba-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2fdba-148">RELATED LINKS</span></span>


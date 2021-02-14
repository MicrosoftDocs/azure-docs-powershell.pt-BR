---
external help file: ''
Module Name: Az.VMware
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/test-azvmwarelocationtrialavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Test-AzVMwareLocationTrialAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Test-AzVMwareLocationTrialAvailability.md
ms.openlocfilehash: f667e5f2c6f85e06e1d16a35b1279d88af5e2ed7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115591"
---
# <span data-ttu-id="b00e3-101">Test-AzVMwareLocationTrialAvailability</span><span class="sxs-lookup"><span data-stu-id="b00e3-101">Test-AzVMwareLocationTrialAvailability</span></span>

## <span data-ttu-id="b00e3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b00e3-102">SYNOPSIS</span></span>
<span data-ttu-id="b00e3-103">Status de avaliação do retorno da assinatura por região</span><span class="sxs-lookup"><span data-stu-id="b00e3-103">Return trial status for subscription by region</span></span>

## <span data-ttu-id="b00e3-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b00e3-104">SYNTAX</span></span>

### <span data-ttu-id="b00e3-105">Verificar (Padrão)</span><span class="sxs-lookup"><span data-stu-id="b00e3-105">Check (Default)</span></span>
```
Test-AzVMwareLocationTrialAvailability -Location <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="b00e3-106">CheckViaIdentity</span><span class="sxs-lookup"><span data-stu-id="b00e3-106">CheckViaIdentity</span></span>
```
Test-AzVMwareLocationTrialAvailability -InputObject <IVMwareIdentity> [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b00e3-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="b00e3-107">DESCRIPTION</span></span>
<span data-ttu-id="b00e3-108">Status de avaliação do retorno da assinatura por região</span><span class="sxs-lookup"><span data-stu-id="b00e3-108">Return trial status for subscription by region</span></span>

## <span data-ttu-id="b00e3-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="b00e3-109">EXAMPLES</span></span>

### <span data-ttu-id="b00e3-110">Exemplo 1: Verificar a disponibilidade da avaliação</span><span class="sxs-lookup"><span data-stu-id="b00e3-110">Example 1: Check trial availability</span></span>
```powershell
PS C:\> Test-AzVMwareLocationTrialAvailability -Location australiaeast

AvailableHost Status
------------- ------
0             TrialDisabled
```

<span data-ttu-id="b00e3-111">Verificar a disponibilidade da avaliação</span><span class="sxs-lookup"><span data-stu-id="b00e3-111">Check trial availability</span></span>

## <span data-ttu-id="b00e3-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b00e3-112">PARAMETERS</span></span>

### <span data-ttu-id="b00e3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b00e3-113">-DefaultProfile</span></span>
<span data-ttu-id="b00e3-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b00e3-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b00e3-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b00e3-115">-InputObject</span></span>
<span data-ttu-id="b00e3-116">Parâmetro de Identidade para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="b00e3-116">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.IVMwareIdentity
Parameter Sets: CheckViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b00e3-117">-Local</span><span class="sxs-lookup"><span data-stu-id="b00e3-117">-Location</span></span>
<span data-ttu-id="b00e3-118">Região do Azure</span><span class="sxs-lookup"><span data-stu-id="b00e3-118">Azure region</span></span>

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

### <span data-ttu-id="b00e3-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b00e3-119">-SubscriptionId</span></span>
<span data-ttu-id="b00e3-120">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="b00e3-120">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="b00e3-121">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="b00e3-121">-Confirm</span></span>
<span data-ttu-id="b00e3-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b00e3-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b00e3-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b00e3-123">-WhatIf</span></span>
<span data-ttu-id="b00e3-124">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="b00e3-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b00e3-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b00e3-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b00e3-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b00e3-126">CommonParameters</span></span>
<span data-ttu-id="b00e3-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b00e3-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b00e3-128">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b00e3-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b00e3-129">Entradas</span><span class="sxs-lookup"><span data-stu-id="b00e3-129">INPUTS</span></span>

### <span data-ttu-id="b00e3-130">Microsoft.Azure.PowerShell.Cmdlets.V Ltd.Models.IV Ltd.</span><span class="sxs-lookup"><span data-stu-id="b00e3-130">Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.IVMwareIdentity</span></span>

## <span data-ttu-id="b00e3-131">Saídas</span><span class="sxs-lookup"><span data-stu-id="b00e3-131">OUTPUTS</span></span>

### <span data-ttu-id="b00e3-132">Microsoft.Azure.PowerShell.Cmdlets.V Ltd.Models.Api20200320.ITrial</span><span class="sxs-lookup"><span data-stu-id="b00e3-132">Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.Api20200320.ITrial</span></span>

## <span data-ttu-id="b00e3-133">Notas</span><span class="sxs-lookup"><span data-stu-id="b00e3-133">NOTES</span></span>

<span data-ttu-id="b00e3-134">Aliases</span><span class="sxs-lookup"><span data-stu-id="b00e3-134">ALIASES</span></span>

<span data-ttu-id="b00e3-135">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="b00e3-135">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b00e3-136">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="b00e3-136">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b00e3-137">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b00e3-137">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b00e3-138">INPUTOBJECT: <IVMwareIdentity> Parâmetro de Identidade</span><span class="sxs-lookup"><span data-stu-id="b00e3-138">INPUTOBJECT <IVMwareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b00e3-139">`[AuthorizationName <String>]`: Nome da Autorização de Circuito do ExpressRoute na nuvem privada</span><span class="sxs-lookup"><span data-stu-id="b00e3-139">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="b00e3-140">`[ClusterName <String>]`: Nome do cluster na nuvem privada</span><span class="sxs-lookup"><span data-stu-id="b00e3-140">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="b00e3-141">`[HcxEnterpriseSiteName <String>]`: Nome do Site Corporativo HCX na nuvem privada</span><span class="sxs-lookup"><span data-stu-id="b00e3-141">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="b00e3-142">`[Id <String>]`: Caminho de identidade de recursos</span><span class="sxs-lookup"><span data-stu-id="b00e3-142">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b00e3-143">`[Location <String>]`: região do Azure</span><span class="sxs-lookup"><span data-stu-id="b00e3-143">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="b00e3-144">`[PrivateCloudName <String>]`: Nome da nuvem privada</span><span class="sxs-lookup"><span data-stu-id="b00e3-144">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="b00e3-145">`[ResourceGroupName <String>]`: o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b00e3-145">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="b00e3-146">O nome não é sensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="b00e3-146">The name is case insensitive.</span></span>
  - <span data-ttu-id="b00e3-147">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="b00e3-147">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="b00e3-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b00e3-148">RELATED LINKS</span></span>


---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/powershell/module/az.vmware/test-azvmwarelocationquotaavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Test-AzVMwareLocationQuotaAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Test-AzVMwareLocationQuotaAvailability.md
ms.openlocfilehash: 61ecab0a22df339af7c790fd51def5a880d9b607
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890041"
---
# <span data-ttu-id="1fff1-101">Test-AzVMWareLocationQuotaAvailability</span><span class="sxs-lookup"><span data-stu-id="1fff1-101">Test-AzVMWareLocationQuotaAvailability</span></span>

## <span data-ttu-id="1fff1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1fff1-102">SYNOPSIS</span></span>
<span data-ttu-id="1fff1-103">Cota de retorno para assinatura por região</span><span class="sxs-lookup"><span data-stu-id="1fff1-103">Return quota for subscription by region</span></span>

## <span data-ttu-id="1fff1-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="1fff1-104">SYNTAX</span></span>

### <span data-ttu-id="1fff1-105">Verificar (Padrão)</span><span class="sxs-lookup"><span data-stu-id="1fff1-105">Check (Default)</span></span>
```
Test-AzVMWareLocationQuotaAvailability -Location <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="1fff1-106">CheckViaIdentity</span><span class="sxs-lookup"><span data-stu-id="1fff1-106">CheckViaIdentity</span></span>
```
Test-AzVMWareLocationQuotaAvailability -InputObject <IVMWareIdentity> [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="1fff1-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="1fff1-107">DESCRIPTION</span></span>
<span data-ttu-id="1fff1-108">Cota de retorno para assinatura por região</span><span class="sxs-lookup"><span data-stu-id="1fff1-108">Return quota for subscription by region</span></span>

## <span data-ttu-id="1fff1-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1fff1-109">EXAMPLES</span></span>

### <span data-ttu-id="1fff1-110">Exemplo 1: Verificar disponibilidade de cota</span><span class="sxs-lookup"><span data-stu-id="1fff1-110">Example 1: Check quota availability</span></span>
```powershell
PS C:\> Test-AzVMWareLocationQuotaAvailability -Location eastus

Enabled
-------
Disabled
```

<span data-ttu-id="1fff1-111">Verificar disponibilidade de cota</span><span class="sxs-lookup"><span data-stu-id="1fff1-111">Check quota availability</span></span>

## <span data-ttu-id="1fff1-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="1fff1-112">PARAMETERS</span></span>

### <span data-ttu-id="1fff1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1fff1-113">-DefaultProfile</span></span>
<span data-ttu-id="1fff1-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1fff1-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1fff1-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1fff1-115">-InputObject</span></span>
<span data-ttu-id="1fff1-116">Parâmetro Identity Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="1fff1-116">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="1fff1-117">-Location</span><span class="sxs-lookup"><span data-stu-id="1fff1-117">-Location</span></span>
<span data-ttu-id="1fff1-118">Região do Azure</span><span class="sxs-lookup"><span data-stu-id="1fff1-118">Azure region</span></span>

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

### <span data-ttu-id="1fff1-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1fff1-119">-SubscriptionId</span></span>
<span data-ttu-id="1fff1-120">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="1fff1-120">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="1fff1-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1fff1-121">-Confirm</span></span>
<span data-ttu-id="1fff1-122">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1fff1-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1fff1-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1fff1-123">-WhatIf</span></span>
<span data-ttu-id="1fff1-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1fff1-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1fff1-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1fff1-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1fff1-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1fff1-126">CommonParameters</span></span>
<span data-ttu-id="1fff1-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1fff1-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1fff1-128">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1fff1-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1fff1-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1fff1-129">INPUTS</span></span>

### <span data-ttu-id="1fff1-130">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span><span class="sxs-lookup"><span data-stu-id="1fff1-130">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span></span>

## <span data-ttu-id="1fff1-131">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="1fff1-131">OUTPUTS</span></span>

### <span data-ttu-id="1fff1-132">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IQuota</span><span class="sxs-lookup"><span data-stu-id="1fff1-132">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IQuota</span></span>

## <span data-ttu-id="1fff1-133">NOTES</span><span class="sxs-lookup"><span data-stu-id="1fff1-133">NOTES</span></span>

<span data-ttu-id="1fff1-134">ALIASES</span><span class="sxs-lookup"><span data-stu-id="1fff1-134">ALIASES</span></span>

<span data-ttu-id="1fff1-135">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="1fff1-135">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="1fff1-136">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="1fff1-136">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="1fff1-137">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="1fff1-137">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="1fff1-138">INPUTOBJECT <IVMWareIdentity> : Parâmetro Identity</span><span class="sxs-lookup"><span data-stu-id="1fff1-138">INPUTOBJECT <IVMWareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="1fff1-139">`[AuthorizationName <String>]`: Nome da Autorização de Circuito Expresso na nuvem privada</span><span class="sxs-lookup"><span data-stu-id="1fff1-139">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="1fff1-140">`[ClusterName <String>]`: Nome do cluster na nuvem privada</span><span class="sxs-lookup"><span data-stu-id="1fff1-140">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="1fff1-141">`[HcxEnterpriseSiteName <String>]`: Nome do Site empresarial HCX na nuvem privada</span><span class="sxs-lookup"><span data-stu-id="1fff1-141">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="1fff1-142">`[Id <String>]`: Caminho da identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="1fff1-142">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="1fff1-143">`[Location <String>]`: Região do Azure</span><span class="sxs-lookup"><span data-stu-id="1fff1-143">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="1fff1-144">`[PrivateCloudName <String>]`: Nome da nuvem privada</span><span class="sxs-lookup"><span data-stu-id="1fff1-144">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="1fff1-145">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="1fff1-145">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="1fff1-146">O nome é insensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="1fff1-146">The name is case insensitive.</span></span>
  - <span data-ttu-id="1fff1-147">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="1fff1-147">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="1fff1-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1fff1-148">RELATED LINKS</span></span>


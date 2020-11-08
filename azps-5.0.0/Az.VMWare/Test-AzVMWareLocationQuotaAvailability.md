---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/test-azvmwarelocationquotaavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Test-AzVMWareLocationQuotaAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Test-AzVMWareLocationQuotaAvailability.md
ms.openlocfilehash: 9cb677ff172c986f18c7c11c00e0f8d7e0bbf5bf
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94125205"
---
# <span data-ttu-id="b7213-101">Test-AzVMWareLocationQuotaAvailability</span><span class="sxs-lookup"><span data-stu-id="b7213-101">Test-AzVMWareLocationQuotaAvailability</span></span>

## <span data-ttu-id="b7213-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b7213-102">SYNOPSIS</span></span>
<span data-ttu-id="b7213-103">Devolver a cota de assinatura por região</span><span class="sxs-lookup"><span data-stu-id="b7213-103">Return quota for subscription by region</span></span>

## <span data-ttu-id="b7213-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b7213-104">SYNTAX</span></span>

### <span data-ttu-id="b7213-105">Verificar (padrão)</span><span class="sxs-lookup"><span data-stu-id="b7213-105">Check (Default)</span></span>
```
Test-AzVMWareLocationQuotaAvailability -Location <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="b7213-106">CheckViaIdentity</span><span class="sxs-lookup"><span data-stu-id="b7213-106">CheckViaIdentity</span></span>
```
Test-AzVMWareLocationQuotaAvailability -InputObject <IVMWareIdentity> [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b7213-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b7213-107">DESCRIPTION</span></span>
<span data-ttu-id="b7213-108">Devolver a cota de assinatura por região</span><span class="sxs-lookup"><span data-stu-id="b7213-108">Return quota for subscription by region</span></span>

## <span data-ttu-id="b7213-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b7213-109">EXAMPLES</span></span>

### <span data-ttu-id="b7213-110">Exemplo 1: verificar a disponibilidade da cota</span><span class="sxs-lookup"><span data-stu-id="b7213-110">Example 1: Check quota availability</span></span>
```powershell
PS C:\> Test-AzVMWareLocationQuotaAvailability -Location eastus

Enabled
-------
Disabled
```

<span data-ttu-id="b7213-111">Verificar a disponibilidade da cota</span><span class="sxs-lookup"><span data-stu-id="b7213-111">Check quota availability</span></span>

## <span data-ttu-id="b7213-112">OS</span><span class="sxs-lookup"><span data-stu-id="b7213-112">PARAMETERS</span></span>

### <span data-ttu-id="b7213-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7213-113">-DefaultProfile</span></span>
<span data-ttu-id="b7213-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b7213-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b7213-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b7213-115">-InputObject</span></span>
<span data-ttu-id="b7213-116">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="b7213-116">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="b7213-117">-Local</span><span class="sxs-lookup"><span data-stu-id="b7213-117">-Location</span></span>
<span data-ttu-id="b7213-118">Região do Azure</span><span class="sxs-lookup"><span data-stu-id="b7213-118">Azure region</span></span>

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

### <span data-ttu-id="b7213-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b7213-119">-SubscriptionId</span></span>
<span data-ttu-id="b7213-120">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="b7213-120">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="b7213-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b7213-121">-Confirm</span></span>
<span data-ttu-id="b7213-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b7213-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b7213-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7213-123">-WhatIf</span></span>
<span data-ttu-id="b7213-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b7213-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b7213-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b7213-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b7213-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7213-126">CommonParameters</span></span>
<span data-ttu-id="b7213-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7213-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7213-128">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b7213-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7213-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b7213-129">INPUTS</span></span>

### <span data-ttu-id="b7213-130">Microsoft. Azure. PowerShell. cmdlets. VMWare. Models. IVMWareIdentity</span><span class="sxs-lookup"><span data-stu-id="b7213-130">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span></span>

## <span data-ttu-id="b7213-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b7213-131">OUTPUTS</span></span>

### <span data-ttu-id="b7213-132">Microsoft. Azure. PowerShell. cmdlets. VMWare. Models. Api20200320. IQuota</span><span class="sxs-lookup"><span data-stu-id="b7213-132">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IQuota</span></span>

## <span data-ttu-id="b7213-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b7213-133">NOTES</span></span>

<span data-ttu-id="b7213-134">ALIASES</span><span class="sxs-lookup"><span data-stu-id="b7213-134">ALIASES</span></span>

<span data-ttu-id="b7213-135">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="b7213-135">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b7213-136">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="b7213-136">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b7213-137">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b7213-137">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b7213-138">INPUTobject <IVMWareIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="b7213-138">INPUTOBJECT <IVMWareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b7213-139">`[AuthorizationName <String>]`: Nome da autorização de circuito do ExpressRoute na nuvem privada</span><span class="sxs-lookup"><span data-stu-id="b7213-139">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="b7213-140">`[ClusterName <String>]`: Nome do cluster na nuvem privada</span><span class="sxs-lookup"><span data-stu-id="b7213-140">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="b7213-141">`[HcxEnterpriseSiteName <String>]`: Nome do site da empresa HCX na nuvem privada</span><span class="sxs-lookup"><span data-stu-id="b7213-141">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="b7213-142">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="b7213-142">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b7213-143">`[Location <String>]`: Região do Azure</span><span class="sxs-lookup"><span data-stu-id="b7213-143">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="b7213-144">`[PrivateCloudName <String>]`: Nome da nuvem privada</span><span class="sxs-lookup"><span data-stu-id="b7213-144">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="b7213-145">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b7213-145">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="b7213-146">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="b7213-146">The name is case insensitive.</span></span>
  - <span data-ttu-id="b7213-147">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="b7213-147">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="b7213-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b7213-148">RELATED LINKS</span></span>


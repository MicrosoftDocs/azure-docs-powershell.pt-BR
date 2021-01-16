---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/test-azvmwarelocationquotaavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Test-AzVMWareLocationQuotaAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Test-AzVMWareLocationQuotaAvailability.md
ms.openlocfilehash: 9cb677ff172c986f18c7c11c00e0f8d7e0bbf5bf
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98263232"
---
# <span data-ttu-id="ef0de-101">Test-AzVMWareLocationQuotaAvailability</span><span class="sxs-lookup"><span data-stu-id="ef0de-101">Test-AzVMWareLocationQuotaAvailability</span></span>

## <span data-ttu-id="ef0de-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ef0de-102">SYNOPSIS</span></span>
<span data-ttu-id="ef0de-103">Devolver a cota de assinatura por região</span><span class="sxs-lookup"><span data-stu-id="ef0de-103">Return quota for subscription by region</span></span>

## <span data-ttu-id="ef0de-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ef0de-104">SYNTAX</span></span>

### <span data-ttu-id="ef0de-105">Verificar (padrão)</span><span class="sxs-lookup"><span data-stu-id="ef0de-105">Check (Default)</span></span>
```
Test-AzVMWareLocationQuotaAvailability -Location <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="ef0de-106">CheckViaIdentity</span><span class="sxs-lookup"><span data-stu-id="ef0de-106">CheckViaIdentity</span></span>
```
Test-AzVMWareLocationQuotaAvailability -InputObject <IVMWareIdentity> [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ef0de-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ef0de-107">DESCRIPTION</span></span>
<span data-ttu-id="ef0de-108">Devolver a cota de assinatura por região</span><span class="sxs-lookup"><span data-stu-id="ef0de-108">Return quota for subscription by region</span></span>

## <span data-ttu-id="ef0de-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ef0de-109">EXAMPLES</span></span>

### <span data-ttu-id="ef0de-110">Exemplo 1: verificar a disponibilidade da cota</span><span class="sxs-lookup"><span data-stu-id="ef0de-110">Example 1: Check quota availability</span></span>
```powershell
PS C:\> Test-AzVMWareLocationQuotaAvailability -Location eastus

Enabled
-------
Disabled
```

<span data-ttu-id="ef0de-111">Verificar a disponibilidade da cota</span><span class="sxs-lookup"><span data-stu-id="ef0de-111">Check quota availability</span></span>

## <span data-ttu-id="ef0de-112">OS</span><span class="sxs-lookup"><span data-stu-id="ef0de-112">PARAMETERS</span></span>

### <span data-ttu-id="ef0de-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef0de-113">-DefaultProfile</span></span>
<span data-ttu-id="ef0de-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ef0de-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ef0de-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ef0de-115">-InputObject</span></span>
<span data-ttu-id="ef0de-116">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="ef0de-116">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="ef0de-117">-Local</span><span class="sxs-lookup"><span data-stu-id="ef0de-117">-Location</span></span>
<span data-ttu-id="ef0de-118">Região do Azure</span><span class="sxs-lookup"><span data-stu-id="ef0de-118">Azure region</span></span>

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

### <span data-ttu-id="ef0de-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ef0de-119">-SubscriptionId</span></span>
<span data-ttu-id="ef0de-120">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="ef0de-120">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="ef0de-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="ef0de-121">-Confirm</span></span>
<span data-ttu-id="ef0de-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ef0de-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ef0de-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef0de-123">-WhatIf</span></span>
<span data-ttu-id="ef0de-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ef0de-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ef0de-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ef0de-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ef0de-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef0de-126">CommonParameters</span></span>
<span data-ttu-id="ef0de-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef0de-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef0de-128">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ef0de-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef0de-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ef0de-129">INPUTS</span></span>

### <span data-ttu-id="ef0de-130">Microsoft. Azure. PowerShell. cmdlets. VMWare. Models. IVMWareIdentity</span><span class="sxs-lookup"><span data-stu-id="ef0de-130">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span></span>

## <span data-ttu-id="ef0de-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ef0de-131">OUTPUTS</span></span>

### <span data-ttu-id="ef0de-132">Microsoft. Azure. PowerShell. cmdlets. VMWare. Models. Api20200320. IQuota</span><span class="sxs-lookup"><span data-stu-id="ef0de-132">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IQuota</span></span>

## <span data-ttu-id="ef0de-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ef0de-133">NOTES</span></span>

<span data-ttu-id="ef0de-134">ALIASES</span><span class="sxs-lookup"><span data-stu-id="ef0de-134">ALIASES</span></span>

<span data-ttu-id="ef0de-135">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="ef0de-135">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ef0de-136">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="ef0de-136">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ef0de-137">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ef0de-137">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ef0de-138">INPUTobject <IVMWareIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="ef0de-138">INPUTOBJECT <IVMWareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ef0de-139">`[AuthorizationName <String>]`: Nome da autorização de circuito do ExpressRoute na nuvem privada</span><span class="sxs-lookup"><span data-stu-id="ef0de-139">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="ef0de-140">`[ClusterName <String>]`: Nome do cluster na nuvem privada</span><span class="sxs-lookup"><span data-stu-id="ef0de-140">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="ef0de-141">`[HcxEnterpriseSiteName <String>]`: Nome do site da empresa HCX na nuvem privada</span><span class="sxs-lookup"><span data-stu-id="ef0de-141">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="ef0de-142">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="ef0de-142">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ef0de-143">`[Location <String>]`: Região do Azure</span><span class="sxs-lookup"><span data-stu-id="ef0de-143">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="ef0de-144">`[PrivateCloudName <String>]`: Nome da nuvem privada</span><span class="sxs-lookup"><span data-stu-id="ef0de-144">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="ef0de-145">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ef0de-145">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="ef0de-146">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="ef0de-146">The name is case insensitive.</span></span>
  - <span data-ttu-id="ef0de-147">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="ef0de-147">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="ef0de-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ef0de-148">RELATED LINKS</span></span>


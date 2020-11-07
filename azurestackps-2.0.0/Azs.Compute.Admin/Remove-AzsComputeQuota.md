---
external help file: ''
Module Name: Azs.Compute.Admin
online version: https://docs.microsoft.com/powershell/module/azs.compute.admin/remove-azscomputequota
schema: 2.0.0
ms.openlocfilehash: 715234586df8383a2983b4f0459ae91ca457d684
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93777150"
---
# <span data-ttu-id="6a70c-101">Remove-AzsComputeQuota</span><span class="sxs-lookup"><span data-stu-id="6a70c-101">Remove-AzsComputeQuota</span></span>

## <span data-ttu-id="6a70c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6a70c-102">SYNOPSIS</span></span>
<span data-ttu-id="6a70c-103">Excluir uma cota de computação existente.</span><span class="sxs-lookup"><span data-stu-id="6a70c-103">Delete an existing Compute quota.</span></span>

## <span data-ttu-id="6a70c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6a70c-104">SYNTAX</span></span>

### <span data-ttu-id="6a70c-105">Excluir (padrão)</span><span class="sxs-lookup"><span data-stu-id="6a70c-105">Delete (Default)</span></span>
```
Remove-AzsComputeQuota -Name <String> [-Location <String>] [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="6a70c-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="6a70c-106">DeleteViaIdentity</span></span>
```
Remove-AzsComputeQuota -InputObject <IComputeAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="6a70c-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6a70c-107">DESCRIPTION</span></span>
<span data-ttu-id="6a70c-108">Excluir uma cota de computação existente.</span><span class="sxs-lookup"><span data-stu-id="6a70c-108">Delete an existing Compute quota.</span></span>

## <span data-ttu-id="6a70c-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6a70c-109">EXAMPLES</span></span>

### <span data-ttu-id="6a70c-110">Exemplo 1: remover uma cota de computação</span><span class="sxs-lookup"><span data-stu-id="6a70c-110">Example 1: Remove a Compute Quota</span></span>
```powershell
PS C:\> Remove-AzsComputeQuota -Name "AComputeQuota"
```

<span data-ttu-id="6a70c-111">Uma chamada bem-sucedida para remover uma cota de computação não retornará nenhuma saída</span><span class="sxs-lookup"><span data-stu-id="6a70c-111">A successful call to remove a compute quota will not return any output</span></span>

## <span data-ttu-id="6a70c-112">OS</span><span class="sxs-lookup"><span data-stu-id="6a70c-112">PARAMETERS</span></span>

### <span data-ttu-id="6a70c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a70c-113">-DefaultProfile</span></span>
<span data-ttu-id="6a70c-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6a70c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6a70c-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6a70c-115">-InputObject</span></span>
<span data-ttu-id="6a70c-116">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="6a70c-116">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.IComputeAdminIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="6a70c-117">-Local</span><span class="sxs-lookup"><span data-stu-id="6a70c-117">-Location</span></span>
<span data-ttu-id="6a70c-118">Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="6a70c-118">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="6a70c-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="6a70c-119">-Name</span></span>
<span data-ttu-id="6a70c-120">Nome da cota.</span><span class="sxs-lookup"><span data-stu-id="6a70c-120">Name of the quota.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: QuotaName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="6a70c-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6a70c-121">-PassThru</span></span>
<span data-ttu-id="6a70c-122">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="6a70c-122">Returns true when the command succeeds</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="6a70c-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6a70c-123">-SubscriptionId</span></span>
<span data-ttu-id="6a70c-124">Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="6a70c-124">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="6a70c-125">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="6a70c-125">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="6a70c-126">-Confirme</span><span class="sxs-lookup"><span data-stu-id="6a70c-126">-Confirm</span></span>
<span data-ttu-id="6a70c-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6a70c-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6a70c-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6a70c-128">-WhatIf</span></span>
<span data-ttu-id="6a70c-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6a70c-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6a70c-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6a70c-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6a70c-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a70c-131">CommonParameters</span></span>
<span data-ttu-id="6a70c-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a70c-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a70c-133">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6a70c-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a70c-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6a70c-134">INPUTS</span></span>

### <span data-ttu-id="6a70c-135">Microsoft. Azure. PowerShell. cmdlets. ComputeAdmin. Models. IComputeAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="6a70c-135">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.IComputeAdminIdentity</span></span>

## <span data-ttu-id="6a70c-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6a70c-136">OUTPUTS</span></span>

### <span data-ttu-id="6a70c-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6a70c-137">System.Boolean</span></span>



## <span data-ttu-id="6a70c-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6a70c-138">NOTES</span></span>

<span data-ttu-id="6a70c-139">Propriedades de parâmetros complexas para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="6a70c-139">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6a70c-140">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="6a70c-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="6a70c-141">INPUTobject <IComputeAdminIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="6a70c-141">INPUTOBJECT <IComputeAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="6a70c-142">`[DiskId <String>]`: O GUID de disco como identidade.</span><span class="sxs-lookup"><span data-stu-id="6a70c-142">`[DiskId <String>]`: The disk guid as identity.</span></span>
  - <span data-ttu-id="6a70c-143">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="6a70c-143">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="6a70c-144">`[Location <String>]`: Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="6a70c-144">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="6a70c-145">`[MigrationId <String>]`: O nome do GUID do trabalho de migração.</span><span class="sxs-lookup"><span data-stu-id="6a70c-145">`[MigrationId <String>]`: The migration job guid name.</span></span>
  - <span data-ttu-id="6a70c-146">`[Offer <String>]`: Nome da oferta.</span><span class="sxs-lookup"><span data-stu-id="6a70c-146">`[Offer <String>]`: Name of the offer.</span></span>
  - <span data-ttu-id="6a70c-147">`[Publisher <String>]`: Nome do fornecedor.</span><span class="sxs-lookup"><span data-stu-id="6a70c-147">`[Publisher <String>]`: Name of the publisher.</span></span>
  - <span data-ttu-id="6a70c-148">`[QuotaName <String>]`: Nome da cota.</span><span class="sxs-lookup"><span data-stu-id="6a70c-148">`[QuotaName <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="6a70c-149">`[Sku <String>]`: Nome da SKU.</span><span class="sxs-lookup"><span data-stu-id="6a70c-149">`[Sku <String>]`: Name of the SKU.</span></span>
  - <span data-ttu-id="6a70c-150">`[SubscriptionId <String>]`: Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="6a70c-150">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="6a70c-151">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="6a70c-151">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="6a70c-152">`[Type <String>]`: Tipo de extensão.</span><span class="sxs-lookup"><span data-stu-id="6a70c-152">`[Type <String>]`: Type of extension.</span></span>
  - <span data-ttu-id="6a70c-153">`[Version <String>]`: A versão do recurso.</span><span class="sxs-lookup"><span data-stu-id="6a70c-153">`[Version <String>]`: The version of the resource.</span></span>

## <span data-ttu-id="6a70c-154">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6a70c-154">RELATED LINKS</span></span>


---
external help file: ''
Module Name: Azs.Compute.Admin
online version: https://docs.microsoft.com/powershell/module/azs.compute.admin/remove-azscomputequota
schema: 2.0.0
ms.openlocfilehash: 715234586df8383a2983b4f0459ae91ca457d684
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/24/2020
ms.locfileid: "93945368"
---
# <span data-ttu-id="16e66-101">Remove-AzsComputeQuota</span><span class="sxs-lookup"><span data-stu-id="16e66-101">Remove-AzsComputeQuota</span></span>

## <span data-ttu-id="16e66-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="16e66-102">SYNOPSIS</span></span>
<span data-ttu-id="16e66-103">Excluir uma cota de computação existente.</span><span class="sxs-lookup"><span data-stu-id="16e66-103">Delete an existing Compute quota.</span></span>

## <span data-ttu-id="16e66-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="16e66-104">SYNTAX</span></span>

### <span data-ttu-id="16e66-105">Excluir (padrão)</span><span class="sxs-lookup"><span data-stu-id="16e66-105">Delete (Default)</span></span>
```
Remove-AzsComputeQuota -Name <String> [-Location <String>] [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="16e66-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="16e66-106">DeleteViaIdentity</span></span>
```
Remove-AzsComputeQuota -InputObject <IComputeAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="16e66-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="16e66-107">DESCRIPTION</span></span>
<span data-ttu-id="16e66-108">Excluir uma cota de computação existente.</span><span class="sxs-lookup"><span data-stu-id="16e66-108">Delete an existing Compute quota.</span></span>

## <span data-ttu-id="16e66-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="16e66-109">EXAMPLES</span></span>

### <span data-ttu-id="16e66-110">Exemplo 1: remover uma cota de computação</span><span class="sxs-lookup"><span data-stu-id="16e66-110">Example 1: Remove a Compute Quota</span></span>
```powershell
PS C:\> Remove-AzsComputeQuota -Name "AComputeQuota"
```

<span data-ttu-id="16e66-111">Uma chamada bem-sucedida para remover uma cota de computação não retornará nenhuma saída</span><span class="sxs-lookup"><span data-stu-id="16e66-111">A successful call to remove a compute quota will not return any output</span></span>

## <span data-ttu-id="16e66-112">OS</span><span class="sxs-lookup"><span data-stu-id="16e66-112">PARAMETERS</span></span>

### <span data-ttu-id="16e66-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16e66-113">-DefaultProfile</span></span>
<span data-ttu-id="16e66-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="16e66-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="16e66-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="16e66-115">-InputObject</span></span>
<span data-ttu-id="16e66-116">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="16e66-116">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="16e66-117">-Local</span><span class="sxs-lookup"><span data-stu-id="16e66-117">-Location</span></span>
<span data-ttu-id="16e66-118">Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="16e66-118">Location of the resource.</span></span>

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

### <span data-ttu-id="16e66-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="16e66-119">-Name</span></span>
<span data-ttu-id="16e66-120">Nome da cota.</span><span class="sxs-lookup"><span data-stu-id="16e66-120">Name of the quota.</span></span>

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

### <span data-ttu-id="16e66-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="16e66-121">-PassThru</span></span>
<span data-ttu-id="16e66-122">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="16e66-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="16e66-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="16e66-123">-SubscriptionId</span></span>
<span data-ttu-id="16e66-124">Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="16e66-124">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="16e66-125">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="16e66-125">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="16e66-126">-Confirme</span><span class="sxs-lookup"><span data-stu-id="16e66-126">-Confirm</span></span>
<span data-ttu-id="16e66-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="16e66-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="16e66-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="16e66-128">-WhatIf</span></span>
<span data-ttu-id="16e66-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="16e66-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="16e66-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="16e66-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="16e66-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16e66-131">CommonParameters</span></span>
<span data-ttu-id="16e66-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16e66-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16e66-133">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="16e66-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16e66-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="16e66-134">INPUTS</span></span>

### <span data-ttu-id="16e66-135">Microsoft. Azure. PowerShell. cmdlets. ComputeAdmin. Models. IComputeAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="16e66-135">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.IComputeAdminIdentity</span></span>

## <span data-ttu-id="16e66-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="16e66-136">OUTPUTS</span></span>

### <span data-ttu-id="16e66-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="16e66-137">System.Boolean</span></span>



## <span data-ttu-id="16e66-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="16e66-138">NOTES</span></span>

<span data-ttu-id="16e66-139">Propriedades de parâmetros complexas para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="16e66-139">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="16e66-140">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="16e66-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="16e66-141">INPUTobject <IComputeAdminIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="16e66-141">INPUTOBJECT <IComputeAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="16e66-142">`[DiskId <String>]`: O GUID de disco como identidade.</span><span class="sxs-lookup"><span data-stu-id="16e66-142">`[DiskId <String>]`: The disk guid as identity.</span></span>
  - <span data-ttu-id="16e66-143">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="16e66-143">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="16e66-144">`[Location <String>]`: Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="16e66-144">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="16e66-145">`[MigrationId <String>]`: O nome do GUID do trabalho de migração.</span><span class="sxs-lookup"><span data-stu-id="16e66-145">`[MigrationId <String>]`: The migration job guid name.</span></span>
  - <span data-ttu-id="16e66-146">`[Offer <String>]`: Nome da oferta.</span><span class="sxs-lookup"><span data-stu-id="16e66-146">`[Offer <String>]`: Name of the offer.</span></span>
  - <span data-ttu-id="16e66-147">`[Publisher <String>]`: Nome do fornecedor.</span><span class="sxs-lookup"><span data-stu-id="16e66-147">`[Publisher <String>]`: Name of the publisher.</span></span>
  - <span data-ttu-id="16e66-148">`[QuotaName <String>]`: Nome da cota.</span><span class="sxs-lookup"><span data-stu-id="16e66-148">`[QuotaName <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="16e66-149">`[Sku <String>]`: Nome da SKU.</span><span class="sxs-lookup"><span data-stu-id="16e66-149">`[Sku <String>]`: Name of the SKU.</span></span>
  - <span data-ttu-id="16e66-150">`[SubscriptionId <String>]`: Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="16e66-150">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="16e66-151">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="16e66-151">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="16e66-152">`[Type <String>]`: Tipo de extensão.</span><span class="sxs-lookup"><span data-stu-id="16e66-152">`[Type <String>]`: Type of extension.</span></span>
  - <span data-ttu-id="16e66-153">`[Version <String>]`: A versão do recurso.</span><span class="sxs-lookup"><span data-stu-id="16e66-153">`[Version <String>]`: The version of the resource.</span></span>

## <span data-ttu-id="16e66-154">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="16e66-154">RELATED LINKS</span></span>


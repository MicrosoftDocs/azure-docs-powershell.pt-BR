---
external help file: ''
Module Name: Azs.Compute.Admin
online version: https://docs.microsoft.com/powershell/module/azs.compute.admin/remove-azsvmextension
schema: 2.0.0
ms.openlocfilehash: 0b2bca9555b14a391df69acc4abdb2fc8c95017c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93777149"
---
# <span data-ttu-id="9781d-101">Remove-AzsVMExtension</span><span class="sxs-lookup"><span data-stu-id="9781d-101">Remove-AzsVMExtension</span></span>

## <span data-ttu-id="9781d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9781d-102">SYNOPSIS</span></span>
<span data-ttu-id="9781d-103">Exclui a imagem de extensão da máquina virtual especificada.</span><span class="sxs-lookup"><span data-stu-id="9781d-103">Deletes specified Virtual Machine Extension Image.</span></span>

## <span data-ttu-id="9781d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9781d-104">SYNTAX</span></span>

### <span data-ttu-id="9781d-105">Excluir (padrão)</span><span class="sxs-lookup"><span data-stu-id="9781d-105">Delete (Default)</span></span>
```
Remove-AzsVMExtension -Publisher <String> -Type <String> -Version <String> [-Location <String>]
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="9781d-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="9781d-106">DeleteViaIdentity</span></span>
```
Remove-AzsVMExtension -InputObject <IComputeAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="9781d-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9781d-107">DESCRIPTION</span></span>
<span data-ttu-id="9781d-108">Exclui a imagem de extensão da máquina virtual especificada.</span><span class="sxs-lookup"><span data-stu-id="9781d-108">Deletes specified Virtual Machine Extension Image.</span></span>

## <span data-ttu-id="9781d-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9781d-109">EXAMPLES</span></span>

### <span data-ttu-id="9781d-110">Exemplo 1: remover uma extensão de VM existente</span><span class="sxs-lookup"><span data-stu-id="9781d-110">Example 1: Remove a VM Extension that Exists</span></span> 
```powershell
PS C:\> Remove-AzsVMExtension -Location local -Publisher Microsoft -Type MicroExtension -Version 0.1.0
```

<span data-ttu-id="9781d-111">Uma chamada bem-sucedida para remover uma cota de computação não retornará nenhuma saída</span><span class="sxs-lookup"><span data-stu-id="9781d-111">A successful call to remove a compute quota will not return any output</span></span>

### <span data-ttu-id="9781d-112">Exemplo 2: remover uma extensão de VM que não existe</span><span class="sxs-lookup"><span data-stu-id="9781d-112">Example 2: Remove a VM Extension that Does Not Exist</span></span>
```powershell
PS C:\> Remove-AzsVMExtension -Location local -Publisher Microsoft -Type DoesntExist -Version 9.8.7
```

<span data-ttu-id="9781d-113">Uma chamada bem-sucedida para remover uma imagem de plataforma que não existe não retornará nenhuma saída</span><span class="sxs-lookup"><span data-stu-id="9781d-113">A successful call to remove a platform image that doesn't exist will not return any output</span></span>

## <span data-ttu-id="9781d-114">OS</span><span class="sxs-lookup"><span data-stu-id="9781d-114">PARAMETERS</span></span>

### <span data-ttu-id="9781d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9781d-115">-DefaultProfile</span></span>
<span data-ttu-id="9781d-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9781d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9781d-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9781d-117">-InputObject</span></span>
<span data-ttu-id="9781d-118">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="9781d-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="9781d-119">-Local</span><span class="sxs-lookup"><span data-stu-id="9781d-119">-Location</span></span>
<span data-ttu-id="9781d-120">Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="9781d-120">Location of the resource.</span></span>

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

### <span data-ttu-id="9781d-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9781d-121">-PassThru</span></span>
<span data-ttu-id="9781d-122">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="9781d-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="9781d-123">-Publisher</span><span class="sxs-lookup"><span data-stu-id="9781d-123">-Publisher</span></span>
<span data-ttu-id="9781d-124">Nome do fornecedor.</span><span class="sxs-lookup"><span data-stu-id="9781d-124">Name of the publisher.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="9781d-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9781d-125">-SubscriptionId</span></span>
<span data-ttu-id="9781d-126">Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="9781d-126">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="9781d-127">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="9781d-127">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="9781d-128">-Digite</span><span class="sxs-lookup"><span data-stu-id="9781d-128">-Type</span></span>
<span data-ttu-id="9781d-129">Tipo de extensão.</span><span class="sxs-lookup"><span data-stu-id="9781d-129">Type of extension.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="9781d-130">-Versão</span><span class="sxs-lookup"><span data-stu-id="9781d-130">-Version</span></span>
<span data-ttu-id="9781d-131">A versão do recurso.</span><span class="sxs-lookup"><span data-stu-id="9781d-131">The version of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="9781d-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="9781d-132">-Confirm</span></span>
<span data-ttu-id="9781d-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9781d-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9781d-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9781d-134">-WhatIf</span></span>
<span data-ttu-id="9781d-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9781d-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9781d-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9781d-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9781d-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9781d-137">CommonParameters</span></span>
<span data-ttu-id="9781d-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9781d-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9781d-139">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9781d-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9781d-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9781d-140">INPUTS</span></span>

### <span data-ttu-id="9781d-141">Microsoft. Azure. PowerShell. cmdlets. ComputeAdmin. Models. IComputeAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="9781d-141">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.IComputeAdminIdentity</span></span>

## <span data-ttu-id="9781d-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9781d-142">OUTPUTS</span></span>

### <span data-ttu-id="9781d-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9781d-143">System.Boolean</span></span>



## <span data-ttu-id="9781d-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9781d-144">NOTES</span></span>

<span data-ttu-id="9781d-145">Propriedades de parâmetros complexas para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="9781d-145">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="9781d-146">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="9781d-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="9781d-147">INPUTobject <IComputeAdminIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="9781d-147">INPUTOBJECT <IComputeAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="9781d-148">`[DiskId <String>]`: O GUID de disco como identidade.</span><span class="sxs-lookup"><span data-stu-id="9781d-148">`[DiskId <String>]`: The disk guid as identity.</span></span>
  - <span data-ttu-id="9781d-149">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="9781d-149">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="9781d-150">`[Location <String>]`: Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="9781d-150">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="9781d-151">`[MigrationId <String>]`: O nome do GUID do trabalho de migração.</span><span class="sxs-lookup"><span data-stu-id="9781d-151">`[MigrationId <String>]`: The migration job guid name.</span></span>
  - <span data-ttu-id="9781d-152">`[Offer <String>]`: Nome da oferta.</span><span class="sxs-lookup"><span data-stu-id="9781d-152">`[Offer <String>]`: Name of the offer.</span></span>
  - <span data-ttu-id="9781d-153">`[Publisher <String>]`: Nome do fornecedor.</span><span class="sxs-lookup"><span data-stu-id="9781d-153">`[Publisher <String>]`: Name of the publisher.</span></span>
  - <span data-ttu-id="9781d-154">`[QuotaName <String>]`: Nome da cota.</span><span class="sxs-lookup"><span data-stu-id="9781d-154">`[QuotaName <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="9781d-155">`[Sku <String>]`: Nome da SKU.</span><span class="sxs-lookup"><span data-stu-id="9781d-155">`[Sku <String>]`: Name of the SKU.</span></span>
  - <span data-ttu-id="9781d-156">`[SubscriptionId <String>]`: Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="9781d-156">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="9781d-157">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="9781d-157">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="9781d-158">`[Type <String>]`: Tipo de extensão.</span><span class="sxs-lookup"><span data-stu-id="9781d-158">`[Type <String>]`: Type of extension.</span></span>
  - <span data-ttu-id="9781d-159">`[Version <String>]`: A versão do recurso.</span><span class="sxs-lookup"><span data-stu-id="9781d-159">`[Version <String>]`: The version of the resource.</span></span>

## <span data-ttu-id="9781d-160">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9781d-160">RELATED LINKS</span></span>


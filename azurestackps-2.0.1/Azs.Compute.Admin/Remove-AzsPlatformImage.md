---
external help file: ''
Module Name: Azs.Compute.Admin
online version: https://docs.microsoft.com/powershell/module/azs.compute.admin/remove-azsplatformimage
schema: 2.0.0
ms.openlocfilehash: ae4fc80c54aedf7f35ebfc6c0c5f16bb2e5028ee
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/24/2020
ms.locfileid: "93945367"
---
# <span data-ttu-id="7fb23-101">Remove-AzsPlatformImage</span><span class="sxs-lookup"><span data-stu-id="7fb23-101">Remove-AzsPlatformImage</span></span>

## <span data-ttu-id="7fb23-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7fb23-102">SYNOPSIS</span></span>
<span data-ttu-id="7fb23-103">Excluir uma imagem de plataforma</span><span class="sxs-lookup"><span data-stu-id="7fb23-103">Delete a platform image</span></span>

## <span data-ttu-id="7fb23-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7fb23-104">SYNTAX</span></span>

### <span data-ttu-id="7fb23-105">Excluir (padrão)</span><span class="sxs-lookup"><span data-stu-id="7fb23-105">Delete (Default)</span></span>
```
Remove-AzsPlatformImage -Offer <String> -Publisher <String> -Sku <String> -Version <String>
 [-Location <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="7fb23-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="7fb23-106">DeleteViaIdentity</span></span>
```
Remove-AzsPlatformImage -InputObject <IComputeAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="7fb23-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7fb23-107">DESCRIPTION</span></span>
<span data-ttu-id="7fb23-108">Excluir uma imagem de plataforma</span><span class="sxs-lookup"><span data-stu-id="7fb23-108">Delete a platform image</span></span>

## <span data-ttu-id="7fb23-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7fb23-109">EXAMPLES</span></span>

### <span data-ttu-id="7fb23-110">Exemplo 1: remover uma imagem de plataforma</span><span class="sxs-lookup"><span data-stu-id="7fb23-110">Example 1: Remove a Platform Image</span></span>
```powershell
PS C:\>Remove-AzsPlatformImage -Location northwest -Offer UbuntuServer -Publisher Microsoft -Sku 16.04-LTS -Version 1.0.0
```

<span data-ttu-id="7fb23-111">Uma chamada bem-sucedida para remover uma plataforma de plataforma não retornará nenhuma saída</span><span class="sxs-lookup"><span data-stu-id="7fb23-111">A successful call to remove a platform image will not return any output</span></span>

### <span data-ttu-id="7fb23-112">Exemplo 2: remover uma imagem de plataforma que não existe</span><span class="sxs-lookup"><span data-stu-id="7fb23-112">Example 2: Remove a Platform Image the Does Not Exist</span></span>
```powershell
PS C:\>  Remove-AzsPlatformImage -Location northwest -Offer UbuntuServer -Publisher Microsoft -Sku 16.04-LTS -Version 1.1.6

```

<span data-ttu-id="7fb23-113">Uma chamada bem-sucedida para remover uma imagem de plataforma que não existe não retornará nenhuma saída</span><span class="sxs-lookup"><span data-stu-id="7fb23-113">A successful call to remove a platform image that doesn't exist will not return any output</span></span>

## <span data-ttu-id="7fb23-114">OS</span><span class="sxs-lookup"><span data-stu-id="7fb23-114">PARAMETERS</span></span>

### <span data-ttu-id="7fb23-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7fb23-115">-DefaultProfile</span></span>
<span data-ttu-id="7fb23-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7fb23-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7fb23-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7fb23-117">-InputObject</span></span>
<span data-ttu-id="7fb23-118">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="7fb23-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="7fb23-119">-Local</span><span class="sxs-lookup"><span data-stu-id="7fb23-119">-Location</span></span>
<span data-ttu-id="7fb23-120">Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="7fb23-120">Location of the resource.</span></span>

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

### <span data-ttu-id="7fb23-121">-Oferta</span><span class="sxs-lookup"><span data-stu-id="7fb23-121">-Offer</span></span>
<span data-ttu-id="7fb23-122">Nome da oferta.</span><span class="sxs-lookup"><span data-stu-id="7fb23-122">Name of the offer.</span></span>

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

### <span data-ttu-id="7fb23-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7fb23-123">-PassThru</span></span>
<span data-ttu-id="7fb23-124">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="7fb23-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="7fb23-125">-Publisher</span><span class="sxs-lookup"><span data-stu-id="7fb23-125">-Publisher</span></span>
<span data-ttu-id="7fb23-126">Nome do fornecedor.</span><span class="sxs-lookup"><span data-stu-id="7fb23-126">Name of the publisher.</span></span>

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

### <span data-ttu-id="7fb23-127">-SKU</span><span class="sxs-lookup"><span data-stu-id="7fb23-127">-Sku</span></span>
<span data-ttu-id="7fb23-128">Nome da SKU.</span><span class="sxs-lookup"><span data-stu-id="7fb23-128">Name of the SKU.</span></span>

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

### <span data-ttu-id="7fb23-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7fb23-129">-SubscriptionId</span></span>
<span data-ttu-id="7fb23-130">Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="7fb23-130">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="7fb23-131">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="7fb23-131">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="7fb23-132">-Versão</span><span class="sxs-lookup"><span data-stu-id="7fb23-132">-Version</span></span>
<span data-ttu-id="7fb23-133">A versão do recurso.</span><span class="sxs-lookup"><span data-stu-id="7fb23-133">The version of the resource.</span></span>

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

### <span data-ttu-id="7fb23-134">-Confirme</span><span class="sxs-lookup"><span data-stu-id="7fb23-134">-Confirm</span></span>
<span data-ttu-id="7fb23-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7fb23-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7fb23-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7fb23-136">-WhatIf</span></span>
<span data-ttu-id="7fb23-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7fb23-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7fb23-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7fb23-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7fb23-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7fb23-139">CommonParameters</span></span>
<span data-ttu-id="7fb23-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7fb23-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7fb23-141">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7fb23-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7fb23-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7fb23-142">INPUTS</span></span>

### <span data-ttu-id="7fb23-143">Microsoft. Azure. PowerShell. cmdlets. ComputeAdmin. Models. IComputeAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="7fb23-143">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.IComputeAdminIdentity</span></span>

## <span data-ttu-id="7fb23-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7fb23-144">OUTPUTS</span></span>

### <span data-ttu-id="7fb23-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7fb23-145">System.Boolean</span></span>



## <span data-ttu-id="7fb23-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7fb23-146">NOTES</span></span>

<span data-ttu-id="7fb23-147">Propriedades de parâmetros complexas para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="7fb23-147">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="7fb23-148">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="7fb23-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="7fb23-149">INPUTobject <IComputeAdminIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="7fb23-149">INPUTOBJECT <IComputeAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="7fb23-150">`[DiskId <String>]`: O GUID de disco como identidade.</span><span class="sxs-lookup"><span data-stu-id="7fb23-150">`[DiskId <String>]`: The disk guid as identity.</span></span>
  - <span data-ttu-id="7fb23-151">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="7fb23-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="7fb23-152">`[Location <String>]`: Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="7fb23-152">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="7fb23-153">`[MigrationId <String>]`: O nome do GUID do trabalho de migração.</span><span class="sxs-lookup"><span data-stu-id="7fb23-153">`[MigrationId <String>]`: The migration job guid name.</span></span>
  - <span data-ttu-id="7fb23-154">`[Offer <String>]`: Nome da oferta.</span><span class="sxs-lookup"><span data-stu-id="7fb23-154">`[Offer <String>]`: Name of the offer.</span></span>
  - <span data-ttu-id="7fb23-155">`[Publisher <String>]`: Nome do fornecedor.</span><span class="sxs-lookup"><span data-stu-id="7fb23-155">`[Publisher <String>]`: Name of the publisher.</span></span>
  - <span data-ttu-id="7fb23-156">`[QuotaName <String>]`: Nome da cota.</span><span class="sxs-lookup"><span data-stu-id="7fb23-156">`[QuotaName <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="7fb23-157">`[Sku <String>]`: Nome da SKU.</span><span class="sxs-lookup"><span data-stu-id="7fb23-157">`[Sku <String>]`: Name of the SKU.</span></span>
  - <span data-ttu-id="7fb23-158">`[SubscriptionId <String>]`: Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="7fb23-158">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="7fb23-159">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="7fb23-159">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="7fb23-160">`[Type <String>]`: Tipo de extensão.</span><span class="sxs-lookup"><span data-stu-id="7fb23-160">`[Type <String>]`: Type of extension.</span></span>
  - <span data-ttu-id="7fb23-161">`[Version <String>]`: A versão do recurso.</span><span class="sxs-lookup"><span data-stu-id="7fb23-161">`[Version <String>]`: The version of the resource.</span></span>

## <span data-ttu-id="7fb23-162">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7fb23-162">RELATED LINKS</span></span>


---
external help file: ''
Module Name: Az.DedicatedHsm
online version: https://docs.microsoft.com/en-us/powershell/module/az.dedicatedhsm/remove-azdedicatedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DedicatedHsm/help/Remove-AzDedicatedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DedicatedHsm/help/Remove-AzDedicatedHsm.md
ms.openlocfilehash: aeb8eddcc094e951c78cfe778182cece70448111
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94114553"
---
# <span data-ttu-id="06ccc-101">Remove-AzDedicatedHsm</span><span class="sxs-lookup"><span data-stu-id="06ccc-101">Remove-AzDedicatedHsm</span></span>

## <span data-ttu-id="06ccc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="06ccc-102">SYNOPSIS</span></span>
<span data-ttu-id="06ccc-103">Exclui o HSM dedicado do Azure especificado.</span><span class="sxs-lookup"><span data-stu-id="06ccc-103">Deletes the specified Azure Dedicated HSM.</span></span>

## <span data-ttu-id="06ccc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="06ccc-104">SYNTAX</span></span>

### <span data-ttu-id="06ccc-105">Excluir (padrão)</span><span class="sxs-lookup"><span data-stu-id="06ccc-105">Delete (Default)</span></span>
```
Remove-AzDedicatedHsm -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="06ccc-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="06ccc-106">DeleteViaIdentity</span></span>
```
Remove-AzDedicatedHsm -InputObject <IDedicatedHsmIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="06ccc-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="06ccc-107">DESCRIPTION</span></span>
<span data-ttu-id="06ccc-108">Exclui o HSM dedicado do Azure especificado.</span><span class="sxs-lookup"><span data-stu-id="06ccc-108">Deletes the specified Azure Dedicated HSM.</span></span>

## <span data-ttu-id="06ccc-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="06ccc-109">EXAMPLES</span></span>

### <span data-ttu-id="06ccc-110">Exemplo 1: remover um HSM dedicado por nome</span><span class="sxs-lookup"><span data-stu-id="06ccc-110">Example 1: Remove a Dedicated HSM by name</span></span>
```powershell
PS C:\> Remove-AzDedicatedHsm -Name hsm-7t2xaf -ResourceGroupName lucas-manual-test

```

<span data-ttu-id="06ccc-111">Este commnad remove um HSM (módulo de segurança de hardware) por nome.</span><span class="sxs-lookup"><span data-stu-id="06ccc-111">This commnad removes a hardware security module(HSM) by name.</span></span>

### <span data-ttu-id="06ccc-112">Exemplo 2: remover um HSM dedicado por objeto</span><span class="sxs-lookup"><span data-stu-id="06ccc-112">Example 2: Remove a Dedicated HSM  by object</span></span>
```powershell
PS C:\> $hsm = Get-AzDedicatedHsm -Name hsm-7t2xaf -ResourceGroupName dedicatedhsm-rg-n359cz
PS C:\> Remove-AzDedicatedHsm -InputObject  $hsm

```

<span data-ttu-id="06ccc-113">Isso commnad remove um HSM dedicado por objeto.</span><span class="sxs-lookup"><span data-stu-id="06ccc-113">This commnad removes a Dedicated HSM by object.</span></span>

## <span data-ttu-id="06ccc-114">OS</span><span class="sxs-lookup"><span data-stu-id="06ccc-114">PARAMETERS</span></span>

### <span data-ttu-id="06ccc-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="06ccc-115">-AsJob</span></span>
<span data-ttu-id="06ccc-116">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="06ccc-116">Run the command as a job</span></span>

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

### <span data-ttu-id="06ccc-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06ccc-117">-DefaultProfile</span></span>
<span data-ttu-id="06ccc-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="06ccc-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="06ccc-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="06ccc-119">-InputObject</span></span>
<span data-ttu-id="06ccc-120">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="06ccc-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.IDedicatedHsmIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="06ccc-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="06ccc-121">-Name</span></span>
<span data-ttu-id="06ccc-122">O nome do HSM dedicado a ser excluído</span><span class="sxs-lookup"><span data-stu-id="06ccc-122">The name of the dedicated HSM to delete</span></span>

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

### <span data-ttu-id="06ccc-123">-Nowait</span><span class="sxs-lookup"><span data-stu-id="06ccc-123">-NoWait</span></span>
<span data-ttu-id="06ccc-124">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="06ccc-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="06ccc-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="06ccc-125">-PassThru</span></span>
<span data-ttu-id="06ccc-126">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="06ccc-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="06ccc-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06ccc-127">-ResourceGroupName</span></span>
<span data-ttu-id="06ccc-128">O nome do grupo de recursos ao qual o HSM dedicado pertence.</span><span class="sxs-lookup"><span data-stu-id="06ccc-128">The name of the Resource Group to which the dedicated HSM belongs.</span></span>

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

### <span data-ttu-id="06ccc-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="06ccc-129">-SubscriptionId</span></span>
<span data-ttu-id="06ccc-130">Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="06ccc-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="06ccc-131">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="06ccc-131">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="06ccc-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="06ccc-132">-Confirm</span></span>
<span data-ttu-id="06ccc-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="06ccc-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="06ccc-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06ccc-134">-WhatIf</span></span>
<span data-ttu-id="06ccc-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="06ccc-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="06ccc-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="06ccc-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="06ccc-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06ccc-137">CommonParameters</span></span>
<span data-ttu-id="06ccc-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06ccc-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06ccc-139">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="06ccc-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06ccc-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="06ccc-140">INPUTS</span></span>

### <span data-ttu-id="06ccc-141">Microsoft. Azure. PowerShell. cmdlets. DedicatedHsm. Models. IDedicatedHsmIdentity</span><span class="sxs-lookup"><span data-stu-id="06ccc-141">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.IDedicatedHsmIdentity</span></span>

## <span data-ttu-id="06ccc-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="06ccc-142">OUTPUTS</span></span>

### <span data-ttu-id="06ccc-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="06ccc-143">System.Boolean</span></span>

## <span data-ttu-id="06ccc-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="06ccc-144">NOTES</span></span>

<span data-ttu-id="06ccc-145">ALIASES</span><span class="sxs-lookup"><span data-stu-id="06ccc-145">ALIASES</span></span>

<span data-ttu-id="06ccc-146">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="06ccc-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="06ccc-147">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="06ccc-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="06ccc-148">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="06ccc-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="06ccc-149">INPUTobject <IDedicatedHsmIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="06ccc-149">INPUTOBJECT <IDedicatedHsmIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="06ccc-150">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="06ccc-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="06ccc-151">`[Name <String>]`: Nome do HSM dedicado</span><span class="sxs-lookup"><span data-stu-id="06ccc-151">`[Name <String>]`: Name of the dedicated Hsm</span></span>
  - <span data-ttu-id="06ccc-152">`[ResourceGroupName <String>]`: O nome do grupo de recursos ao qual o recurso pertence.</span><span class="sxs-lookup"><span data-stu-id="06ccc-152">`[ResourceGroupName <String>]`: The name of the Resource Group to which the resource belongs.</span></span>
  - <span data-ttu-id="06ccc-153">`[SubscriptionId <String>]`: Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="06ccc-153">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="06ccc-154">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="06ccc-154">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="06ccc-155">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="06ccc-155">RELATED LINKS</span></span>


---
external help file: ''
Module Name: Az.DedicatedHsm
online version: https://docs.microsoft.com/powershell/module/az.dedicatedhsm/remove-azdedicatedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DedicatedHsm/help/Remove-AzDedicatedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DedicatedHsm/help/Remove-AzDedicatedHsm.md
ms.openlocfilehash: 0f9369e3ad2427fc633239b9775f485db01e87b1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886658"
---
# <span data-ttu-id="7152a-101">Remove-AzDedicatedHsm</span><span class="sxs-lookup"><span data-stu-id="7152a-101">Remove-AzDedicatedHsm</span></span>

## <span data-ttu-id="7152a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7152a-102">SYNOPSIS</span></span>
<span data-ttu-id="7152a-103">Exclui o HSM dedicado especificado do Azure.</span><span class="sxs-lookup"><span data-stu-id="7152a-103">Deletes the specified Azure Dedicated HSM.</span></span>

## <span data-ttu-id="7152a-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="7152a-104">SYNTAX</span></span>

### <span data-ttu-id="7152a-105">Excluir (Padrão)</span><span class="sxs-lookup"><span data-stu-id="7152a-105">Delete (Default)</span></span>
```
Remove-AzDedicatedHsm -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="7152a-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="7152a-106">DeleteViaIdentity</span></span>
```
Remove-AzDedicatedHsm -InputObject <IDedicatedHsmIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="7152a-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="7152a-107">DESCRIPTION</span></span>
<span data-ttu-id="7152a-108">Exclui o HSM dedicado especificado do Azure.</span><span class="sxs-lookup"><span data-stu-id="7152a-108">Deletes the specified Azure Dedicated HSM.</span></span>

## <span data-ttu-id="7152a-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7152a-109">EXAMPLES</span></span>

### <span data-ttu-id="7152a-110">Exemplo 1: Remover um HSM dedicado pelo nome</span><span class="sxs-lookup"><span data-stu-id="7152a-110">Example 1: Remove a Dedicated HSM by name</span></span>
```powershell
PS C:\> Remove-AzDedicatedHsm -Name hsm-7t2xaf -ResourceGroupName lucas-manual-test

```

<span data-ttu-id="7152a-111">Essa vírgula remove um HSM (módulo de segurança de hardware) pelo nome.</span><span class="sxs-lookup"><span data-stu-id="7152a-111">This commnad removes a hardware security module(HSM) by name.</span></span>

### <span data-ttu-id="7152a-112">Exemplo 2: Remover um HSM dedicado por objeto</span><span class="sxs-lookup"><span data-stu-id="7152a-112">Example 2: Remove a Dedicated HSM  by object</span></span>
```powershell
PS C:\> $hsm = Get-AzDedicatedHsm -Name hsm-7t2xaf -ResourceGroupName dedicatedhsm-rg-n359cz
PS C:\> Remove-AzDedicatedHsm -InputObject  $hsm

```

<span data-ttu-id="7152a-113">Essa vírgula remove um HSM dedicado por objeto.</span><span class="sxs-lookup"><span data-stu-id="7152a-113">This commnad removes a Dedicated HSM by object.</span></span>

## <span data-ttu-id="7152a-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="7152a-114">PARAMETERS</span></span>

### <span data-ttu-id="7152a-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7152a-115">-AsJob</span></span>
<span data-ttu-id="7152a-116">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="7152a-116">Run the command as a job</span></span>

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

### <span data-ttu-id="7152a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7152a-117">-DefaultProfile</span></span>
<span data-ttu-id="7152a-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7152a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7152a-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7152a-119">-InputObject</span></span>
<span data-ttu-id="7152a-120">Parâmetro Identity Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="7152a-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="7152a-121">-Name</span><span class="sxs-lookup"><span data-stu-id="7152a-121">-Name</span></span>
<span data-ttu-id="7152a-122">O nome do HSM dedicado a ser excluído</span><span class="sxs-lookup"><span data-stu-id="7152a-122">The name of the dedicated HSM to delete</span></span>

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

### <span data-ttu-id="7152a-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="7152a-123">-NoWait</span></span>
<span data-ttu-id="7152a-124">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="7152a-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="7152a-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7152a-125">-PassThru</span></span>
<span data-ttu-id="7152a-126">Retorna true quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="7152a-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="7152a-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7152a-127">-ResourceGroupName</span></span>
<span data-ttu-id="7152a-128">O nome do Grupo de Recursos ao qual o HSM dedicado pertence.</span><span class="sxs-lookup"><span data-stu-id="7152a-128">The name of the Resource Group to which the dedicated HSM belongs.</span></span>

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

### <span data-ttu-id="7152a-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7152a-129">-SubscriptionId</span></span>
<span data-ttu-id="7152a-130">Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="7152a-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="7152a-131">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="7152a-131">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="7152a-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7152a-132">-Confirm</span></span>
<span data-ttu-id="7152a-133">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7152a-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7152a-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7152a-134">-WhatIf</span></span>
<span data-ttu-id="7152a-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7152a-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7152a-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7152a-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7152a-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7152a-137">CommonParameters</span></span>
<span data-ttu-id="7152a-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7152a-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7152a-139">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7152a-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7152a-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7152a-140">INPUTS</span></span>

### <span data-ttu-id="7152a-141">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.IDedicatedHsmIdentity</span><span class="sxs-lookup"><span data-stu-id="7152a-141">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.IDedicatedHsmIdentity</span></span>

## <span data-ttu-id="7152a-142">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="7152a-142">OUTPUTS</span></span>

### <span data-ttu-id="7152a-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="7152a-143">System.Boolean</span></span>

## <span data-ttu-id="7152a-144">NOTES</span><span class="sxs-lookup"><span data-stu-id="7152a-144">NOTES</span></span>

<span data-ttu-id="7152a-145">ALIASES</span><span class="sxs-lookup"><span data-stu-id="7152a-145">ALIASES</span></span>

<span data-ttu-id="7152a-146">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="7152a-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="7152a-147">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="7152a-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="7152a-148">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="7152a-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="7152a-149">INPUTOBJECT <IDedicatedHsmIdentity> : Parâmetro Identity</span><span class="sxs-lookup"><span data-stu-id="7152a-149">INPUTOBJECT <IDedicatedHsmIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="7152a-150">`[Id <String>]`: Caminho da identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="7152a-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="7152a-151">`[Name <String>]`: Nome do Hsm dedicado</span><span class="sxs-lookup"><span data-stu-id="7152a-151">`[Name <String>]`: Name of the dedicated Hsm</span></span>
  - <span data-ttu-id="7152a-152">`[ResourceGroupName <String>]`: O nome do Grupo de Recursos ao qual o recurso pertence.</span><span class="sxs-lookup"><span data-stu-id="7152a-152">`[ResourceGroupName <String>]`: The name of the Resource Group to which the resource belongs.</span></span>
  - <span data-ttu-id="7152a-153">`[SubscriptionId <String>]`: Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="7152a-153">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="7152a-154">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="7152a-154">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="7152a-155">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7152a-155">RELATED LINKS</span></span>


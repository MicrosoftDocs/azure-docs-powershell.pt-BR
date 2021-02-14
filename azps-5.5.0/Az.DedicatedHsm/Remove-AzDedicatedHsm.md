---
external help file: ''
Module Name: Az.DedicatedHsm
online version: https://docs.microsoft.com/en-us/powershell/module/az.dedicatedhsm/remove-azdedicatedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DedicatedHsm/help/Remove-AzDedicatedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DedicatedHsm/help/Remove-AzDedicatedHsm.md
ms.openlocfilehash: aeb8eddcc094e951c78cfe778182cece70448111
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100110970"
---
# <span data-ttu-id="25688-101">Remove-AzDedicatedHsm</span><span class="sxs-lookup"><span data-stu-id="25688-101">Remove-AzDedicatedHsm</span></span>

## <span data-ttu-id="25688-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="25688-102">SYNOPSIS</span></span>
<span data-ttu-id="25688-103">Exclui o HSM dedicado do Azure especificado.</span><span class="sxs-lookup"><span data-stu-id="25688-103">Deletes the specified Azure Dedicated HSM.</span></span>

## <span data-ttu-id="25688-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="25688-104">SYNTAX</span></span>

### <span data-ttu-id="25688-105">Excluir (Padrão)</span><span class="sxs-lookup"><span data-stu-id="25688-105">Delete (Default)</span></span>
```
Remove-AzDedicatedHsm -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="25688-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="25688-106">DeleteViaIdentity</span></span>
```
Remove-AzDedicatedHsm -InputObject <IDedicatedHsmIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="25688-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="25688-107">DESCRIPTION</span></span>
<span data-ttu-id="25688-108">Exclui o HSM dedicado do Azure especificado.</span><span class="sxs-lookup"><span data-stu-id="25688-108">Deletes the specified Azure Dedicated HSM.</span></span>

## <span data-ttu-id="25688-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="25688-109">EXAMPLES</span></span>

### <span data-ttu-id="25688-110">Exemplo 1: Remover um HSM Dedicado por nome</span><span class="sxs-lookup"><span data-stu-id="25688-110">Example 1: Remove a Dedicated HSM by name</span></span>
```powershell
PS C:\> Remove-AzDedicatedHsm -Name hsm-7t2xaf -ResourceGroupName lucas-manual-test

```

<span data-ttu-id="25688-111">Esta vírgula remove um HSM (módulo de segurança de hardware) por nome.</span><span class="sxs-lookup"><span data-stu-id="25688-111">This commnad removes a hardware security module(HSM) by name.</span></span>

### <span data-ttu-id="25688-112">Exemplo 2: Remover um HSM Dedicado por objeto</span><span class="sxs-lookup"><span data-stu-id="25688-112">Example 2: Remove a Dedicated HSM  by object</span></span>
```powershell
PS C:\> $hsm = Get-AzDedicatedHsm -Name hsm-7t2xaf -ResourceGroupName dedicatedhsm-rg-n359cz
PS C:\> Remove-AzDedicatedHsm -InputObject  $hsm

```

<span data-ttu-id="25688-113">Esta vírgula remove um HSM Dedicado por objeto.</span><span class="sxs-lookup"><span data-stu-id="25688-113">This commnad removes a Dedicated HSM by object.</span></span>

## <span data-ttu-id="25688-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="25688-114">PARAMETERS</span></span>

### <span data-ttu-id="25688-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="25688-115">-AsJob</span></span>
<span data-ttu-id="25688-116">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="25688-116">Run the command as a job</span></span>

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

### <span data-ttu-id="25688-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25688-117">-DefaultProfile</span></span>
<span data-ttu-id="25688-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="25688-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="25688-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="25688-119">-InputObject</span></span>
<span data-ttu-id="25688-120">Parâmetro de Identidade para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="25688-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="25688-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="25688-121">-Name</span></span>
<span data-ttu-id="25688-122">O nome do HSM dedicado a ser excluído</span><span class="sxs-lookup"><span data-stu-id="25688-122">The name of the dedicated HSM to delete</span></span>

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

### <span data-ttu-id="25688-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="25688-123">-NoWait</span></span>
<span data-ttu-id="25688-124">Executar o comando assíncrona</span><span class="sxs-lookup"><span data-stu-id="25688-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="25688-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="25688-125">-PassThru</span></span>
<span data-ttu-id="25688-126">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="25688-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="25688-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25688-127">-ResourceGroupName</span></span>
<span data-ttu-id="25688-128">O nome do Grupo de Recursos ao qual o HSM dedicado pertence.</span><span class="sxs-lookup"><span data-stu-id="25688-128">The name of the Resource Group to which the dedicated HSM belongs.</span></span>

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

### <span data-ttu-id="25688-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="25688-129">-SubscriptionId</span></span>
<span data-ttu-id="25688-130">Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="25688-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="25688-131">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="25688-131">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="25688-132">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="25688-132">-Confirm</span></span>
<span data-ttu-id="25688-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="25688-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="25688-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="25688-134">-WhatIf</span></span>
<span data-ttu-id="25688-135">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="25688-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="25688-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="25688-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="25688-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25688-137">CommonParameters</span></span>
<span data-ttu-id="25688-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25688-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25688-139">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="25688-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25688-140">Entradas</span><span class="sxs-lookup"><span data-stu-id="25688-140">INPUTS</span></span>

### <span data-ttu-id="25688-141">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.IDedicatedHsmIdentity</span><span class="sxs-lookup"><span data-stu-id="25688-141">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.IDedicatedHsmIdentity</span></span>

## <span data-ttu-id="25688-142">Saídas</span><span class="sxs-lookup"><span data-stu-id="25688-142">OUTPUTS</span></span>

### <span data-ttu-id="25688-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="25688-143">System.Boolean</span></span>

## <span data-ttu-id="25688-144">Notas</span><span class="sxs-lookup"><span data-stu-id="25688-144">NOTES</span></span>

<span data-ttu-id="25688-145">Aliases</span><span class="sxs-lookup"><span data-stu-id="25688-145">ALIASES</span></span>

<span data-ttu-id="25688-146">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="25688-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="25688-147">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="25688-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="25688-148">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="25688-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="25688-149">INPUTOBJECT: <IDedicatedHsmIdentity> Parâmetro de Identidade</span><span class="sxs-lookup"><span data-stu-id="25688-149">INPUTOBJECT <IDedicatedHsmIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="25688-150">`[Id <String>]`: Caminho de identidade de recursos</span><span class="sxs-lookup"><span data-stu-id="25688-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="25688-151">`[Name <String>]`: nome do Hsm dedicado</span><span class="sxs-lookup"><span data-stu-id="25688-151">`[Name <String>]`: Name of the dedicated Hsm</span></span>
  - <span data-ttu-id="25688-152">`[ResourceGroupName <String>]`: o nome do Grupo de Recursos ao qual o recurso pertence.</span><span class="sxs-lookup"><span data-stu-id="25688-152">`[ResourceGroupName <String>]`: The name of the Resource Group to which the resource belongs.</span></span>
  - <span data-ttu-id="25688-153">`[SubscriptionId <String>]`: Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="25688-153">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="25688-154">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="25688-154">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="25688-155">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="25688-155">RELATED LINKS</span></span>


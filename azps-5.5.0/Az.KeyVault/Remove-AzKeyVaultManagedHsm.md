---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvaultmanagedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultManagedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultManagedHsm.md
ms.openlocfilehash: 82521bd7d0ff4f34f68029cdb7faacdd198f2b02
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116713"
---
# <span data-ttu-id="f5ede-101">Remove-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="f5ede-101">Remove-AzKeyVaultManagedHsm</span></span>

## <span data-ttu-id="f5ede-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f5ede-102">SYNOPSIS</span></span>
<span data-ttu-id="f5ede-103">Exclui um HSM gerenciado.</span><span class="sxs-lookup"><span data-stu-id="f5ede-103">Deletes a managed HSM.</span></span>

## <span data-ttu-id="f5ede-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f5ede-104">SYNTAX</span></span>

### <span data-ttu-id="f5ede-105">RemoveManagedHsmByName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="f5ede-105">RemoveManagedHsmByName (Default)</span></span>
```
Remove-AzKeyVaultManagedHsm [-Name] <String> [[-ResourceGroupName] <String>] [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f5ede-106">RemoveManagedHsmByInputObject</span><span class="sxs-lookup"><span data-stu-id="f5ede-106">RemoveManagedHsmByInputObject</span></span>
```
Remove-AzKeyVaultManagedHsm [-InputObject] <PSManagedHsm> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f5ede-107">RemoveManagedHsmByResourceId</span><span class="sxs-lookup"><span data-stu-id="f5ede-107">RemoveManagedHsmByResourceId</span></span>
```
Remove-AzKeyVaultManagedHsm [-ResourceId] <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f5ede-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="f5ede-108">DESCRIPTION</span></span>
<span data-ttu-id="f5ede-109">O cmdlet **Remove-AzKeyVaultManagedHsm** exclui o HSM gerenciado especificado.</span><span class="sxs-lookup"><span data-stu-id="f5ede-109">The **Remove-AzKeyVaultManagedHsm** cmdlet deletes the specified managed HSM.</span></span>
<span data-ttu-id="f5ede-110">Ele também exclui todas as teclas contidas nessa instância.</span><span class="sxs-lookup"><span data-stu-id="f5ede-110">It also deletes all keys contained in that instance.</span></span>
<span data-ttu-id="f5ede-111">Observe que, embora especificar o grupo de recursos seja opcional para esse cmdlet, você deve ter um melhor desempenho.</span><span class="sxs-lookup"><span data-stu-id="f5ede-111">Note that although specifying the resource group is optional for this cmdlet, you should so for better performance.</span></span>

## <span data-ttu-id="f5ede-112">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f5ede-112">EXAMPLES</span></span>

### <span data-ttu-id="f5ede-113">Exemplo 1: Remover um HSM gerenciado</span><span class="sxs-lookup"><span data-stu-id="f5ede-113">Example 1: Remove a managed HSM</span></span>
```powershell
PS C:\> Remove-AzKeyVaultManagedHsm -HsmName 'myhsm' -Force

True
```

<span data-ttu-id="f5ede-114">Esse comando remove o hsm gerenciado chamado myhsm da sua assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="f5ede-114">This command removes the managed hsm named myhsm from your current subscription.</span></span>

### <span data-ttu-id="f5ede-115">Exemplo 2: Remover um hsm gerenciado de um grupo de recursos especificado</span><span class="sxs-lookup"><span data-stu-id="f5ede-115">Example 2: Remove a managed hsm from a specified resource group</span></span>
```powershell
PS C:\> Remove-AzKeyVaultManagedHsm -HsmName 'myhsm' -ResourceGroupName "myrg1" -PassThru

True
```

<span data-ttu-id="f5ede-116">Esse comando remove o hsm gerenciado chamado myhsm do grupo de recursos chamado myrg1.</span><span class="sxs-lookup"><span data-stu-id="f5ede-116">This command removes the managed hsm named myhsm from the resource group named myrg1.</span></span>
<span data-ttu-id="f5ede-117">Se você não especificar o nome do grupo de recursos, o cmdlet procurará o HSM gerenciado nomeado para excluir em sua assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="f5ede-117">If you do not specify the resource group name, the cmdlet searches for the named managed HSM to delete in your current subscription.</span></span>

## <span data-ttu-id="f5ede-118">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f5ede-118">PARAMETERS</span></span>

### <span data-ttu-id="f5ede-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f5ede-119">-AsJob</span></span>
<span data-ttu-id="f5ede-120">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="f5ede-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f5ede-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5ede-121">-DefaultProfile</span></span>
<span data-ttu-id="f5ede-122">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f5ede-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5ede-123">-Forçar</span><span class="sxs-lookup"><span data-stu-id="f5ede-123">-Force</span></span>
<span data-ttu-id="f5ede-124">Indica que o cmdlet não solicita confirmação.</span><span class="sxs-lookup"><span data-stu-id="f5ede-124">Indicates that the cmdlet does not prompt you for confirmation.</span></span>
<span data-ttu-id="f5ede-125">Por padrão, esse cmdlet solicita que você confirme que deseja excluir o HSM gerenciado.</span><span class="sxs-lookup"><span data-stu-id="f5ede-125">By default, this cmdlet prompts you to confirm that you want to delete the managed HSM.</span></span>

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

### <span data-ttu-id="f5ede-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f5ede-126">-InputObject</span></span>
<span data-ttu-id="f5ede-127">Objeto HSM gerenciado a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="f5ede-127">Managed HSM object to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm
Parameter Sets: RemoveManagedHsmByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f5ede-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="f5ede-128">-Name</span></span>
<span data-ttu-id="f5ede-129">Especifica o nome do HSM gerenciado a ser removido.</span><span class="sxs-lookup"><span data-stu-id="f5ede-129">Specifies the name of the managed HSM to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveManagedHsmByName
Aliases: HsmName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5ede-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f5ede-130">-PassThru</span></span>
<span data-ttu-id="f5ede-131">Este Cmdlet não retorna um objeto por padrão.</span><span class="sxs-lookup"><span data-stu-id="f5ede-131">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="f5ede-132">Se essa opção for especificada, ela retornará verdadeira se for bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="f5ede-132">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="f5ede-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5ede-133">-ResourceGroupName</span></span>
<span data-ttu-id="f5ede-134">Especifica o nome do grupo de recursos para que o HSM gerenciado pelo Azure seja removido.</span><span class="sxs-lookup"><span data-stu-id="f5ede-134">Specifies the name of resource group for Azure managed HSM to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveManagedHsmByName
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5ede-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f5ede-135">-ResourceId</span></span>
<span data-ttu-id="f5ede-136">ID do Recurso ManagedHsm.</span><span class="sxs-lookup"><span data-stu-id="f5ede-136">ManagedHsm Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveManagedHsmByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5ede-137">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="f5ede-137">-Confirm</span></span>
<span data-ttu-id="f5ede-138">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f5ede-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f5ede-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f5ede-139">-WhatIf</span></span>
<span data-ttu-id="f5ede-140">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="f5ede-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f5ede-141">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f5ede-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f5ede-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5ede-142">CommonParameters</span></span>
<span data-ttu-id="f5ede-143">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f5ede-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5ede-144">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f5ede-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5ede-145">Entradas</span><span class="sxs-lookup"><span data-stu-id="f5ede-145">INPUTS</span></span>

### <span data-ttu-id="f5ede-146">Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm</span><span class="sxs-lookup"><span data-stu-id="f5ede-146">Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm</span></span>

### <span data-ttu-id="f5ede-147">System.String</span><span class="sxs-lookup"><span data-stu-id="f5ede-147">System.String</span></span>

## <span data-ttu-id="f5ede-148">Saídas</span><span class="sxs-lookup"><span data-stu-id="f5ede-148">OUTPUTS</span></span>

### <span data-ttu-id="f5ede-149">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f5ede-149">System.Boolean</span></span>

## <span data-ttu-id="f5ede-150">Notas</span><span class="sxs-lookup"><span data-stu-id="f5ede-150">NOTES</span></span>

## <span data-ttu-id="f5ede-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f5ede-151">RELATED LINKS</span></span>

[<span data-ttu-id="f5ede-152">Get-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="f5ede-152">Get-AzKeyVaultManagedHsm</span></span>](./Get-AzKeyVaultManagedHsm.md)

[<span data-ttu-id="f5ede-153">New-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="f5ede-153">New-AzKeyVaultManagedHsm</span></span>](./New-AzKeyVaultManagedHsm.md)

[<span data-ttu-id="f5ede-154">Update-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="f5ede-154">Update-AzKeyVaultManagedHsm</span></span>](./Update-AzKeyVaultManagedHsm.md)
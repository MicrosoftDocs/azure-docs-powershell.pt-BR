---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvaultmanagedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultManagedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultManagedHsm.md
ms.openlocfilehash: 82521bd7d0ff4f34f68029cdb7faacdd198f2b02
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98426759"
---
# <span data-ttu-id="59c67-101">Remove-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="59c67-101">Remove-AzKeyVaultManagedHsm</span></span>

## <span data-ttu-id="59c67-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="59c67-102">SYNOPSIS</span></span>
<span data-ttu-id="59c67-103">Exclui um HSM gerenciado.</span><span class="sxs-lookup"><span data-stu-id="59c67-103">Deletes a managed HSM.</span></span>

## <span data-ttu-id="59c67-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="59c67-104">SYNTAX</span></span>

### <span data-ttu-id="59c67-105">RemoveManagedHsmByName (padrão)</span><span class="sxs-lookup"><span data-stu-id="59c67-105">RemoveManagedHsmByName (Default)</span></span>
```
Remove-AzKeyVaultManagedHsm [-Name] <String> [[-ResourceGroupName] <String>] [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="59c67-106">RemoveManagedHsmByInputObject</span><span class="sxs-lookup"><span data-stu-id="59c67-106">RemoveManagedHsmByInputObject</span></span>
```
Remove-AzKeyVaultManagedHsm [-InputObject] <PSManagedHsm> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="59c67-107">RemoveManagedHsmByResourceId</span><span class="sxs-lookup"><span data-stu-id="59c67-107">RemoveManagedHsmByResourceId</span></span>
```
Remove-AzKeyVaultManagedHsm [-ResourceId] <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="59c67-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="59c67-108">DESCRIPTION</span></span>
<span data-ttu-id="59c67-109">O cmdlet **Remove-AzKeyVaultManagedHsm** exclui o HSM gerenciado especificado.</span><span class="sxs-lookup"><span data-stu-id="59c67-109">The **Remove-AzKeyVaultManagedHsm** cmdlet deletes the specified managed HSM.</span></span>
<span data-ttu-id="59c67-110">Ele também exclui todas as chaves contidas nessa instância.</span><span class="sxs-lookup"><span data-stu-id="59c67-110">It also deletes all keys contained in that instance.</span></span>
<span data-ttu-id="59c67-111">Observe que, embora a especificação do grupo de recursos seja opcional para esse cmdlet, você deve fazê-lo para melhorar o desempenho.</span><span class="sxs-lookup"><span data-stu-id="59c67-111">Note that although specifying the resource group is optional for this cmdlet, you should so for better performance.</span></span>

## <span data-ttu-id="59c67-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="59c67-112">EXAMPLES</span></span>

### <span data-ttu-id="59c67-113">Exemplo 1: remover um HSM gerenciado</span><span class="sxs-lookup"><span data-stu-id="59c67-113">Example 1: Remove a managed HSM</span></span>
```powershell
PS C:\> Remove-AzKeyVaultManagedHsm -HsmName 'myhsm' -Force

True
```

<span data-ttu-id="59c67-114">Esse comando Remove o HSM gerenciado chamado myhsm da sua assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="59c67-114">This command removes the managed hsm named myhsm from your current subscription.</span></span>

### <span data-ttu-id="59c67-115">Exemplo 2: remover um HSM gerenciado de um grupo de recursos especificado</span><span class="sxs-lookup"><span data-stu-id="59c67-115">Example 2: Remove a managed hsm from a specified resource group</span></span>
```powershell
PS C:\> Remove-AzKeyVaultManagedHsm -HsmName 'myhsm' -ResourceGroupName "myrg1" -PassThru

True
```

<span data-ttu-id="59c67-116">Esse comando Remove o HSM gerenciado chamado myhsm do grupo de recursos chamado myrg1.</span><span class="sxs-lookup"><span data-stu-id="59c67-116">This command removes the managed hsm named myhsm from the resource group named myrg1.</span></span>
<span data-ttu-id="59c67-117">Se você não especificar o nome do grupo de recursos, o cmdlet pesquisará o HSM gerenciado identificado para excluir na sua assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="59c67-117">If you do not specify the resource group name, the cmdlet searches for the named managed HSM to delete in your current subscription.</span></span>

## <span data-ttu-id="59c67-118">OS</span><span class="sxs-lookup"><span data-stu-id="59c67-118">PARAMETERS</span></span>

### <span data-ttu-id="59c67-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="59c67-119">-AsJob</span></span>
<span data-ttu-id="59c67-120">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="59c67-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="59c67-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59c67-121">-DefaultProfile</span></span>
<span data-ttu-id="59c67-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="59c67-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="59c67-123">-Force</span><span class="sxs-lookup"><span data-stu-id="59c67-123">-Force</span></span>
<span data-ttu-id="59c67-124">Indica que o cmdlet não solicita confirmação.</span><span class="sxs-lookup"><span data-stu-id="59c67-124">Indicates that the cmdlet does not prompt you for confirmation.</span></span>
<span data-ttu-id="59c67-125">Por padrão, esse cmdlet solicita que você confirme se deseja excluir o HSM gerenciado.</span><span class="sxs-lookup"><span data-stu-id="59c67-125">By default, this cmdlet prompts you to confirm that you want to delete the managed HSM.</span></span>

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

### <span data-ttu-id="59c67-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="59c67-126">-InputObject</span></span>
<span data-ttu-id="59c67-127">Objeto HSM gerenciado a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="59c67-127">Managed HSM object to be deleted.</span></span>

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

### <span data-ttu-id="59c67-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="59c67-128">-Name</span></span>
<span data-ttu-id="59c67-129">Especifica o nome do HSM gerenciado a ser removido.</span><span class="sxs-lookup"><span data-stu-id="59c67-129">Specifies the name of the managed HSM to remove.</span></span>

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

### <span data-ttu-id="59c67-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="59c67-130">-PassThru</span></span>
<span data-ttu-id="59c67-131">Esse cmdlet não retorna um objeto por padrão.</span><span class="sxs-lookup"><span data-stu-id="59c67-131">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="59c67-132">Se essa opção for especificada, retornará true se for bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="59c67-132">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="59c67-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59c67-133">-ResourceGroupName</span></span>
<span data-ttu-id="59c67-134">Especifica o nome do grupo de recursos do Azure Managed HSM para remoção.</span><span class="sxs-lookup"><span data-stu-id="59c67-134">Specifies the name of resource group for Azure managed HSM to remove.</span></span>

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

### <span data-ttu-id="59c67-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="59c67-135">-ResourceId</span></span>
<span data-ttu-id="59c67-136">ManagedHsm ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="59c67-136">ManagedHsm Resource Id.</span></span>

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

### <span data-ttu-id="59c67-137">-Confirme</span><span class="sxs-lookup"><span data-stu-id="59c67-137">-Confirm</span></span>
<span data-ttu-id="59c67-138">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="59c67-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="59c67-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59c67-139">-WhatIf</span></span>
<span data-ttu-id="59c67-140">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="59c67-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="59c67-141">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="59c67-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="59c67-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59c67-142">CommonParameters</span></span>
<span data-ttu-id="59c67-143">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59c67-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59c67-144">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="59c67-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59c67-145">SENSORES</span><span class="sxs-lookup"><span data-stu-id="59c67-145">INPUTS</span></span>

### <span data-ttu-id="59c67-146">Microsoft. Azure. Commands. keyvault. Models. PSManagedHsm</span><span class="sxs-lookup"><span data-stu-id="59c67-146">Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm</span></span>

### <span data-ttu-id="59c67-147">System. String</span><span class="sxs-lookup"><span data-stu-id="59c67-147">System.String</span></span>

## <span data-ttu-id="59c67-148">EXIBE</span><span class="sxs-lookup"><span data-stu-id="59c67-148">OUTPUTS</span></span>

### <span data-ttu-id="59c67-149">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="59c67-149">System.Boolean</span></span>

## <span data-ttu-id="59c67-150">INFORMA</span><span class="sxs-lookup"><span data-stu-id="59c67-150">NOTES</span></span>

## <span data-ttu-id="59c67-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="59c67-151">RELATED LINKS</span></span>

[<span data-ttu-id="59c67-152">Get-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="59c67-152">Get-AzKeyVaultManagedHsm</span></span>](./Get-AzKeyVaultManagedHsm.md)

[<span data-ttu-id="59c67-153">New-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="59c67-153">New-AzKeyVaultManagedHsm</span></span>](./New-AzKeyVaultManagedHsm.md)

[<span data-ttu-id="59c67-154">Update-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="59c67-154">Update-AzKeyVaultManagedHsm</span></span>](./Update-AzKeyVaultManagedHsm.md)
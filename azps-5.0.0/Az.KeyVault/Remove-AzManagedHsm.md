---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azmanagedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzManagedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzManagedHsm.md
ms.openlocfilehash: 6555299726d8dcf443382f72c2aba6324b6b377d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94115294"
---
# <span data-ttu-id="9bcd0-101">Remove-AzManagedHsm</span><span class="sxs-lookup"><span data-stu-id="9bcd0-101">Remove-AzManagedHsm</span></span>

## <span data-ttu-id="9bcd0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9bcd0-102">SYNOPSIS</span></span>
<span data-ttu-id="9bcd0-103">Exclui um HSM gerenciado.</span><span class="sxs-lookup"><span data-stu-id="9bcd0-103">Deletes a managed HSM.</span></span>

## <span data-ttu-id="9bcd0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9bcd0-104">SYNTAX</span></span>

### <span data-ttu-id="9bcd0-105">RemoveManagedHsmByName (padrão)</span><span class="sxs-lookup"><span data-stu-id="9bcd0-105">RemoveManagedHsmByName (Default)</span></span>
```
Remove-AzManagedHsm [-Name] <String> [[-ResourceGroupName] <String>] [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9bcd0-106">RemoveManagedHsmByInputObject</span><span class="sxs-lookup"><span data-stu-id="9bcd0-106">RemoveManagedHsmByInputObject</span></span>
```
Remove-AzManagedHsm [-InputObject] <PSManagedHsm> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9bcd0-107">RemoveManagedHsmByResourceId</span><span class="sxs-lookup"><span data-stu-id="9bcd0-107">RemoveManagedHsmByResourceId</span></span>
```
Remove-AzManagedHsm [-ResourceId] <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9bcd0-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9bcd0-108">DESCRIPTION</span></span>
<span data-ttu-id="9bcd0-109">O cmdlet **Remove-AzManagedHsm** exclui o HSM gerenciado especificado.</span><span class="sxs-lookup"><span data-stu-id="9bcd0-109">The **Remove-AzManagedHsm** cmdlet deletes the specified managed HSM.</span></span>
<span data-ttu-id="9bcd0-110">Ele também exclui todas as chaves contidas nessa instância.</span><span class="sxs-lookup"><span data-stu-id="9bcd0-110">It also deletes all keys contained in that instance.</span></span>
<span data-ttu-id="9bcd0-111">Observe que, embora a especificação do grupo de recursos seja opcional para esse cmdlet, você deve fazê-lo para melhorar o desempenho.</span><span class="sxs-lookup"><span data-stu-id="9bcd0-111">Note that although specifying the resource group is optional for this cmdlet, you should so for better performance.</span></span>

## <span data-ttu-id="9bcd0-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9bcd0-112">EXAMPLES</span></span>

### <span data-ttu-id="9bcd0-113">Exemplo 1: remover um HSM gerenciado</span><span class="sxs-lookup"><span data-stu-id="9bcd0-113">Example 1: Remove a managed HSM</span></span>
```powershell
PS C:\> Remove-AzManagedHsm -HsmName 'myhsm' -Force

True
```

<span data-ttu-id="9bcd0-114">Esse comando Remove o HSM gerenciado chamado myhsm da sua assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="9bcd0-114">This command removes the managed hsm named myhsm from your current subscription.</span></span>

### <span data-ttu-id="9bcd0-115">Exemplo 2: remover um HSM gerenciado de um grupo de recursos especificado</span><span class="sxs-lookup"><span data-stu-id="9bcd0-115">Example 2: Remove a managed hsm from a specified resource group</span></span>
```powershell
PS C:\> Remove-AzManagedHsm -HsmName 'myhsm' -ResourceGroupName "myrg1" -PassThru

True
```

<span data-ttu-id="9bcd0-116">Esse comando Remove o HSM gerenciado chamado myhsm do grupo de recursos chamado myrg1.</span><span class="sxs-lookup"><span data-stu-id="9bcd0-116">This command removes the managed hsm named myhsm from the resource group named myrg1.</span></span>
<span data-ttu-id="9bcd0-117">Se você não especificar o nome do grupo de recursos, o cmdlet pesquisará o HSM gerenciado identificado para excluir na sua assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="9bcd0-117">If you do not specify the resource group name, the cmdlet searches for the named managed HSM to delete in your current subscription.</span></span>

## <span data-ttu-id="9bcd0-118">OS</span><span class="sxs-lookup"><span data-stu-id="9bcd0-118">PARAMETERS</span></span>

### <span data-ttu-id="9bcd0-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9bcd0-119">-AsJob</span></span>
<span data-ttu-id="9bcd0-120">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="9bcd0-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9bcd0-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9bcd0-121">-DefaultProfile</span></span>
<span data-ttu-id="9bcd0-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9bcd0-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9bcd0-123">-Force</span><span class="sxs-lookup"><span data-stu-id="9bcd0-123">-Force</span></span>
<span data-ttu-id="9bcd0-124">Indica que o cmdlet não solicita confirmação.</span><span class="sxs-lookup"><span data-stu-id="9bcd0-124">Indicates that the cmdlet does not prompt you for confirmation.</span></span>
<span data-ttu-id="9bcd0-125">Por padrão, esse cmdlet solicita que você confirme se deseja excluir o HSM gerenciado.</span><span class="sxs-lookup"><span data-stu-id="9bcd0-125">By default, this cmdlet prompts you to confirm that you want to delete the managed HSM.</span></span>

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

### <span data-ttu-id="9bcd0-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9bcd0-126">-InputObject</span></span>
<span data-ttu-id="9bcd0-127">Objeto HSM gerenciado a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="9bcd0-127">Managed HSM object to be deleted.</span></span>

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

### <span data-ttu-id="9bcd0-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="9bcd0-128">-Name</span></span>
<span data-ttu-id="9bcd0-129">Especifica o nome do HSM gerenciado a ser removido.</span><span class="sxs-lookup"><span data-stu-id="9bcd0-129">Specifies the name of the managed HSM to remove.</span></span>

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

### <span data-ttu-id="9bcd0-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9bcd0-130">-PassThru</span></span>
<span data-ttu-id="9bcd0-131">Esse cmdlet não retorna um objeto por padrão.</span><span class="sxs-lookup"><span data-stu-id="9bcd0-131">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="9bcd0-132">Se essa opção for especificada, retornará true se for bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="9bcd0-132">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="9bcd0-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9bcd0-133">-ResourceGroupName</span></span>
<span data-ttu-id="9bcd0-134">Especifica o nome do grupo de recursos do Azure Managed HSM para remoção.</span><span class="sxs-lookup"><span data-stu-id="9bcd0-134">Specifies the name of resource group for Azure managed HSM to remove.</span></span>

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

### <span data-ttu-id="9bcd0-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9bcd0-135">-ResourceId</span></span>
<span data-ttu-id="9bcd0-136">ManagedHsm ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="9bcd0-136">ManagedHsm Resource Id.</span></span>

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

### <span data-ttu-id="9bcd0-137">-Confirme</span><span class="sxs-lookup"><span data-stu-id="9bcd0-137">-Confirm</span></span>
<span data-ttu-id="9bcd0-138">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9bcd0-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9bcd0-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9bcd0-139">-WhatIf</span></span>
<span data-ttu-id="9bcd0-140">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9bcd0-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9bcd0-141">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9bcd0-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9bcd0-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9bcd0-142">CommonParameters</span></span>
<span data-ttu-id="9bcd0-143">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9bcd0-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9bcd0-144">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9bcd0-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9bcd0-145">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9bcd0-145">INPUTS</span></span>

### <span data-ttu-id="9bcd0-146">Microsoft. Azure. Commands. keyvault. Models. PSManagedHsm</span><span class="sxs-lookup"><span data-stu-id="9bcd0-146">Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm</span></span>

### <span data-ttu-id="9bcd0-147">System. String</span><span class="sxs-lookup"><span data-stu-id="9bcd0-147">System.String</span></span>

## <span data-ttu-id="9bcd0-148">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9bcd0-148">OUTPUTS</span></span>

### <span data-ttu-id="9bcd0-149">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9bcd0-149">System.Boolean</span></span>

## <span data-ttu-id="9bcd0-150">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9bcd0-150">NOTES</span></span>

## <span data-ttu-id="9bcd0-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9bcd0-151">RELATED LINKS</span></span>

[<span data-ttu-id="9bcd0-152">Get-AzManagedHsm</span><span class="sxs-lookup"><span data-stu-id="9bcd0-152">Get-AzManagedHsm</span></span>](./Get-AzManagedHsm.md)

[<span data-ttu-id="9bcd0-153">New-AzManagedHsm</span><span class="sxs-lookup"><span data-stu-id="9bcd0-153">New-AzManagedHsm</span></span>](./New-AzManagedHsm.md)

[<span data-ttu-id="9bcd0-154">Update-AzManagedHsm</span><span class="sxs-lookup"><span data-stu-id="9bcd0-154">Update-AzManagedHsm</span></span>](./Update-AzManagedHsm.md)
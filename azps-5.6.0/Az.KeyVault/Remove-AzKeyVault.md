---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 7A929BA8-02D9-4BBE-AFF3-B8781F8DDAD9
online version: https://docs.microsoft.com/powershell/module/az.keyvault/remove-azkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVault.md
ms.openlocfilehash: 04b4f6be3393eae0fba2f98c477b4174612d2b79
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891810"
---
# <span data-ttu-id="01f6b-101">Remove-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="01f6b-101">Remove-AzKeyVault</span></span>

## <span data-ttu-id="01f6b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="01f6b-102">SYNOPSIS</span></span>
<span data-ttu-id="01f6b-103">Exclui um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="01f6b-103">Deletes a key vault.</span></span>

## <span data-ttu-id="01f6b-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="01f6b-104">SYNTAX</span></span>

### <span data-ttu-id="01f6b-105">ByAvailableVault (Padrão)</span><span class="sxs-lookup"><span data-stu-id="01f6b-105">ByAvailableVault (Default)</span></span>
```
Remove-AzKeyVault [-VaultName] <String> [[-ResourceGroupName] <String>] [[-Location] <String>] [-Force]
 [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="01f6b-106">ByDeletedVault</span><span class="sxs-lookup"><span data-stu-id="01f6b-106">ByDeletedVault</span></span>
```
Remove-AzKeyVault [-VaultName] <String> [-Location] <String> [-InRemovedState] [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="01f6b-107">InputObjectByAvailableVault</span><span class="sxs-lookup"><span data-stu-id="01f6b-107">InputObjectByAvailableVault</span></span>
```
Remove-AzKeyVault [-InputObject] <PSKeyVault> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="01f6b-108">InputObjectByDeletedVault</span><span class="sxs-lookup"><span data-stu-id="01f6b-108">InputObjectByDeletedVault</span></span>
```
Remove-AzKeyVault [-InputObject] <PSKeyVault> [-InRemovedState] [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="01f6b-109">ResourceIdByAvailableVault</span><span class="sxs-lookup"><span data-stu-id="01f6b-109">ResourceIdByAvailableVault</span></span>
```
Remove-AzKeyVault [-ResourceId] <String> [[-Location] <String>] [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="01f6b-110">ResourceIdByDeletedVault</span><span class="sxs-lookup"><span data-stu-id="01f6b-110">ResourceIdByDeletedVault</span></span>
```
Remove-AzKeyVault [-ResourceId] <String> [-Location] <String> [-InRemovedState] [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="01f6b-111">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="01f6b-111">DESCRIPTION</span></span>
<span data-ttu-id="01f6b-112">O cmdlet **Remove-AzKeyVault** exclui o cofre de chaves especificado.</span><span class="sxs-lookup"><span data-stu-id="01f6b-112">The **Remove-AzKeyVault** cmdlet deletes the specified key vault.</span></span>
<span data-ttu-id="01f6b-113">Ele também exclui todas as chaves e segredos contidos nessa instância.</span><span class="sxs-lookup"><span data-stu-id="01f6b-113">It also deletes all keys and secrets contained in that instance.</span></span>
<span data-ttu-id="01f6b-114">Observe que, embora a especificação do grupo de recursos seja opcional para este cmdlet, você deve fazer isso para melhorar o desempenho.</span><span class="sxs-lookup"><span data-stu-id="01f6b-114">Note that although specifying the resource group is optional for this cmdlet, you should so for better performance.</span></span>

## <span data-ttu-id="01f6b-115">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="01f6b-115">EXAMPLES</span></span>

### <span data-ttu-id="01f6b-116">Exemplo 1: Remover um cofre de chaves</span><span class="sxs-lookup"><span data-stu-id="01f6b-116">Example 1: Remove a key vault</span></span>
```powershell
PS C:\> Remove-AzKeyVault -VaultName "Contoso03Vault" -PassThru

True
```

<span data-ttu-id="01f6b-117">Este comando remove o cofre de chaves chamado Contoso03Vault da sua assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="01f6b-117">This command removes the key vault named Contoso03Vault from your current subscription.</span></span>

### <span data-ttu-id="01f6b-118">Exemplo 2: Remover um cofre de chaves de um grupo de recursos especificado</span><span class="sxs-lookup"><span data-stu-id="01f6b-118">Example 2: Remove a key vault from a specified resource group</span></span>
```powershell
PS C:\> Remove-AzKeyVault -Name "Contoso03Vault" -ResourceGroupName "Group14" -PassThru

True
```

<span data-ttu-id="01f6b-119">Este comando remove o cofre de chaves chamado Contoso03Vault do grupo de recursos nomeado.</span><span class="sxs-lookup"><span data-stu-id="01f6b-119">This command removes the key vault named Contoso03Vault from the named resource group.</span></span>
<span data-ttu-id="01f6b-120">Se você não especificar o nome do grupo de recursos, o cmdlet procurará o cofre de chaves nomeado para excluir em sua assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="01f6b-120">If you do not specify the resource group name, the cmdlet searches for the named key vault to delete in your current subscription.</span></span>

### <span data-ttu-id="01f6b-121">Exemplo 3: Remover um hsm gerenciado</span><span class="sxs-lookup"><span data-stu-id="01f6b-121">Example 3: Remove a managed hsm</span></span>
```powershell
PS C:\>  Remove-AzKeyVault -Name "testManagedHsm" -Hsm -PassThru

True
```

<span data-ttu-id="01f6b-122">Este comando remove o hsm gerenciado chamado testManagedHsm da sua assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="01f6b-122">This command removes the managed hsm named testManagedHsm from your current subscription.</span></span>

## <span data-ttu-id="01f6b-123">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="01f6b-123">PARAMETERS</span></span>

### <span data-ttu-id="01f6b-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="01f6b-124">-AsJob</span></span>
<span data-ttu-id="01f6b-125">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="01f6b-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="01f6b-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01f6b-126">-DefaultProfile</span></span>
<span data-ttu-id="01f6b-127">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="01f6b-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="01f6b-128">-Force</span><span class="sxs-lookup"><span data-stu-id="01f6b-128">-Force</span></span>
<span data-ttu-id="01f6b-129">Indica que o cmdlet não solicita a confirmação.</span><span class="sxs-lookup"><span data-stu-id="01f6b-129">Indicates that the cmdlet does not prompt you for confirmation.</span></span>
<span data-ttu-id="01f6b-130">Por padrão, este cmdlet solicita que você confirme se deseja excluir o cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="01f6b-130">By default, this cmdlet prompts you to confirm that you want to delete the key vault.</span></span>

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

### <span data-ttu-id="01f6b-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="01f6b-131">-InputObject</span></span>
<span data-ttu-id="01f6b-132">Objeto Key Vault a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="01f6b-132">Key Vault object to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: InputObjectByAvailableVault, InputObjectByDeletedVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="01f6b-133">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="01f6b-133">-InRemovedState</span></span>
<span data-ttu-id="01f6b-134">Remova o cofre excluído anteriormente permanentemente.</span><span class="sxs-lookup"><span data-stu-id="01f6b-134">Remove the previously deleted vault permanently.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByDeletedVault, InputObjectByDeletedVault, ResourceIdByDeletedVault
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01f6b-135">-Location</span><span class="sxs-lookup"><span data-stu-id="01f6b-135">-Location</span></span>
<span data-ttu-id="01f6b-136">O local do cofre excluído.</span><span class="sxs-lookup"><span data-stu-id="01f6b-136">The location of the deleted vault.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAvailableVault, ResourceIdByAvailableVault
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByDeletedVault, ResourceIdByDeletedVault
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01f6b-137">-PassThru</span><span class="sxs-lookup"><span data-stu-id="01f6b-137">-PassThru</span></span>
<span data-ttu-id="01f6b-138">Este Cmdlet não retorna um objeto por padrão.</span><span class="sxs-lookup"><span data-stu-id="01f6b-138">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="01f6b-139">Se essa opção for especificada, ela retornará true se tiver êxito.</span><span class="sxs-lookup"><span data-stu-id="01f6b-139">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="01f6b-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01f6b-140">-ResourceGroupName</span></span>
<span data-ttu-id="01f6b-141">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="01f6b-141">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAvailableVault
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01f6b-142">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="01f6b-142">-ResourceId</span></span>
<span data-ttu-id="01f6b-143">ID do Recurso KeyVault.</span><span class="sxs-lookup"><span data-stu-id="01f6b-143">KeyVault Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdByAvailableVault, ResourceIdByDeletedVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01f6b-144">-VaultName</span><span class="sxs-lookup"><span data-stu-id="01f6b-144">-VaultName</span></span>
<span data-ttu-id="01f6b-145">Especifica o nome do cofre de chaves a ser removido.</span><span class="sxs-lookup"><span data-stu-id="01f6b-145">Specifies the name of the key vault to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAvailableVault, ByDeletedVault
Aliases: Name

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01f6b-146">-Confirm</span><span class="sxs-lookup"><span data-stu-id="01f6b-146">-Confirm</span></span>
<span data-ttu-id="01f6b-147">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="01f6b-147">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01f6b-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="01f6b-148">-WhatIf</span></span>
<span data-ttu-id="01f6b-149">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="01f6b-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="01f6b-150">O cmdlet não é executado. Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="01f6b-150">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="01f6b-151">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="01f6b-151">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01f6b-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01f6b-152">CommonParameters</span></span>
<span data-ttu-id="01f6b-153">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01f6b-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01f6b-154">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="01f6b-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01f6b-155">INPUTS</span><span class="sxs-lookup"><span data-stu-id="01f6b-155">INPUTS</span></span>

### <span data-ttu-id="01f6b-156">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="01f6b-156">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="01f6b-157">System.String</span><span class="sxs-lookup"><span data-stu-id="01f6b-157">System.String</span></span>

## <span data-ttu-id="01f6b-158">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="01f6b-158">OUTPUTS</span></span>

### <span data-ttu-id="01f6b-159">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="01f6b-159">System.Boolean</span></span>

## <span data-ttu-id="01f6b-160">NOTES</span><span class="sxs-lookup"><span data-stu-id="01f6b-160">NOTES</span></span>

## <span data-ttu-id="01f6b-161">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="01f6b-161">RELATED LINKS</span></span>

[<span data-ttu-id="01f6b-162">Get-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="01f6b-162">Get-AzKeyVault</span></span>](./Get-AzKeyVault.md)

[<span data-ttu-id="01f6b-163">New-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="01f6b-163">New-AzKeyVault</span></span>](./New-AzKeyVault.md)

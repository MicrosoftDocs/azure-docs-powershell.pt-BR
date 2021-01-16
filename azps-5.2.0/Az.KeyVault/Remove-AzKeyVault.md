---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 7A929BA8-02D9-4BBE-AFF3-B8781F8DDAD9
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVault.md
ms.openlocfilehash: 69a1155b99d054699c41cc0b26cd78ef4445f931
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98259153"
---
# <span data-ttu-id="8b31b-101">Remove-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="8b31b-101">Remove-AzKeyVault</span></span>

## <span data-ttu-id="8b31b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8b31b-102">SYNOPSIS</span></span>
<span data-ttu-id="8b31b-103">Exclui um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="8b31b-103">Deletes a key vault.</span></span>

## <span data-ttu-id="8b31b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8b31b-104">SYNTAX</span></span>

### <span data-ttu-id="8b31b-105">ByAvailableVault (padrão)</span><span class="sxs-lookup"><span data-stu-id="8b31b-105">ByAvailableVault (Default)</span></span>
```
Remove-AzKeyVault [-VaultName] <String> [[-ResourceGroupName] <String>] [[-Location] <String>] [-Force]
 [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8b31b-106">ByDeletedVault</span><span class="sxs-lookup"><span data-stu-id="8b31b-106">ByDeletedVault</span></span>
```
Remove-AzKeyVault [-VaultName] <String> [-Location] <String> [-InRemovedState] [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8b31b-107">InputObjectByAvailableVault</span><span class="sxs-lookup"><span data-stu-id="8b31b-107">InputObjectByAvailableVault</span></span>
```
Remove-AzKeyVault [-InputObject] <PSKeyVault> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8b31b-108">InputObjectByDeletedVault</span><span class="sxs-lookup"><span data-stu-id="8b31b-108">InputObjectByDeletedVault</span></span>
```
Remove-AzKeyVault [-InputObject] <PSKeyVault> [-InRemovedState] [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8b31b-109">ResourceIdByAvailableVault</span><span class="sxs-lookup"><span data-stu-id="8b31b-109">ResourceIdByAvailableVault</span></span>
```
Remove-AzKeyVault [-ResourceId] <String> [[-Location] <String>] [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8b31b-110">ResourceIdByDeletedVault</span><span class="sxs-lookup"><span data-stu-id="8b31b-110">ResourceIdByDeletedVault</span></span>
```
Remove-AzKeyVault [-ResourceId] <String> [-Location] <String> [-InRemovedState] [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8b31b-111">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8b31b-111">DESCRIPTION</span></span>
<span data-ttu-id="8b31b-112">O cmdlet **Remove-AzKeyVault** exclui o cofre de chaves especificado.</span><span class="sxs-lookup"><span data-stu-id="8b31b-112">The **Remove-AzKeyVault** cmdlet deletes the specified key vault.</span></span>
<span data-ttu-id="8b31b-113">Ele também exclui todas as chaves e segredos contidos nessa instância.</span><span class="sxs-lookup"><span data-stu-id="8b31b-113">It also deletes all keys and secrets contained in that instance.</span></span>
<span data-ttu-id="8b31b-114">Observe que, embora a especificação do grupo de recursos seja opcional para esse cmdlet, você deve fazê-lo para melhorar o desempenho.</span><span class="sxs-lookup"><span data-stu-id="8b31b-114">Note that although specifying the resource group is optional for this cmdlet, you should so for better performance.</span></span>

## <span data-ttu-id="8b31b-115">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8b31b-115">EXAMPLES</span></span>

### <span data-ttu-id="8b31b-116">Exemplo 1: remover um cofre de chaves</span><span class="sxs-lookup"><span data-stu-id="8b31b-116">Example 1: Remove a key vault</span></span>
```powershell
PS C:\> Remove-AzKeyVault -VaultName "Contoso03Vault" -PassThru

True
```

<span data-ttu-id="8b31b-117">Esse comando Remove o cofre de chaves denominado Contoso03Vault da sua assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="8b31b-117">This command removes the key vault named Contoso03Vault from your current subscription.</span></span>

### <span data-ttu-id="8b31b-118">Exemplo 2: remover um cofre de chaves de um grupo de recursos especificado</span><span class="sxs-lookup"><span data-stu-id="8b31b-118">Example 2: Remove a key vault from a specified resource group</span></span>
```powershell
PS C:\> Remove-AzKeyVault -Name "Contoso03Vault" -ResourceGroupName "Group14" -PassThru

True
```

<span data-ttu-id="8b31b-119">Esse comando Remove o cofre de chaves chamado Contoso03Vault do grupo de recursos nomeado.</span><span class="sxs-lookup"><span data-stu-id="8b31b-119">This command removes the key vault named Contoso03Vault from the named resource group.</span></span>
<span data-ttu-id="8b31b-120">Se você não especificar o nome do grupo de recursos, o cmdlet pesquisará o cofre de chaves nomeados para excluir na sua assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="8b31b-120">If you do not specify the resource group name, the cmdlet searches for the named key vault to delete in your current subscription.</span></span>

### <span data-ttu-id="8b31b-121">Exemplo 3: remover um HSM gerenciado</span><span class="sxs-lookup"><span data-stu-id="8b31b-121">Example 3: Remove a managed hsm</span></span>
```powershell
PS C:\>  Remove-AzKeyVault -Name "testManagedHsm" -Hsm -PassThru

True
```

<span data-ttu-id="8b31b-122">Esse comando Remove o HSM gerenciado chamado testManagedHsm da sua assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="8b31b-122">This command removes the managed hsm named testManagedHsm from your current subscription.</span></span>

## <span data-ttu-id="8b31b-123">OS</span><span class="sxs-lookup"><span data-stu-id="8b31b-123">PARAMETERS</span></span>

### <span data-ttu-id="8b31b-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8b31b-124">-AsJob</span></span>
<span data-ttu-id="8b31b-125">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="8b31b-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8b31b-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b31b-126">-DefaultProfile</span></span>
<span data-ttu-id="8b31b-127">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="8b31b-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8b31b-128">-Force</span><span class="sxs-lookup"><span data-stu-id="8b31b-128">-Force</span></span>
<span data-ttu-id="8b31b-129">Indica que o cmdlet não solicita confirmação.</span><span class="sxs-lookup"><span data-stu-id="8b31b-129">Indicates that the cmdlet does not prompt you for confirmation.</span></span>
<span data-ttu-id="8b31b-130">Por padrão, esse cmdlet solicita que você confirme que deseja excluir o cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="8b31b-130">By default, this cmdlet prompts you to confirm that you want to delete the key vault.</span></span>

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

### <span data-ttu-id="8b31b-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8b31b-131">-InputObject</span></span>
<span data-ttu-id="8b31b-132">Objeto do cofre de chaves a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="8b31b-132">Key Vault object to be deleted.</span></span>

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

### <span data-ttu-id="8b31b-133">-Inremovestate</span><span class="sxs-lookup"><span data-stu-id="8b31b-133">-InRemovedState</span></span>
<span data-ttu-id="8b31b-134">Remova permanentemente o cofre excluído anteriormente.</span><span class="sxs-lookup"><span data-stu-id="8b31b-134">Remove the previously deleted vault permanently.</span></span>

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

### <span data-ttu-id="8b31b-135">-Local</span><span class="sxs-lookup"><span data-stu-id="8b31b-135">-Location</span></span>
<span data-ttu-id="8b31b-136">O local do cofre excluído.</span><span class="sxs-lookup"><span data-stu-id="8b31b-136">The location of the deleted vault.</span></span>

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

### <span data-ttu-id="8b31b-137">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8b31b-137">-PassThru</span></span>
<span data-ttu-id="8b31b-138">Esse cmdlet não retorna um objeto por padrão.</span><span class="sxs-lookup"><span data-stu-id="8b31b-138">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="8b31b-139">Se essa opção for especificada, retornará true se for bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="8b31b-139">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="8b31b-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b31b-140">-ResourceGroupName</span></span>
<span data-ttu-id="8b31b-141">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="8b31b-141">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="8b31b-142">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8b31b-142">-ResourceId</span></span>
<span data-ttu-id="8b31b-143">ID do recurso do keyvault.</span><span class="sxs-lookup"><span data-stu-id="8b31b-143">KeyVault Resource Id.</span></span>

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

### <span data-ttu-id="8b31b-144">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="8b31b-144">-VaultName</span></span>
<span data-ttu-id="8b31b-145">Especifica o nome do cofre de chaves a ser removido.</span><span class="sxs-lookup"><span data-stu-id="8b31b-145">Specifies the name of the key vault to remove.</span></span>

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

### <span data-ttu-id="8b31b-146">-Confirme</span><span class="sxs-lookup"><span data-stu-id="8b31b-146">-Confirm</span></span>
<span data-ttu-id="8b31b-147">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8b31b-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8b31b-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8b31b-148">-WhatIf</span></span>
<span data-ttu-id="8b31b-149">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8b31b-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8b31b-150">O cmdlet não é executado. Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8b31b-150">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8b31b-151">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8b31b-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8b31b-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b31b-152">CommonParameters</span></span>
<span data-ttu-id="8b31b-153">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b31b-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b31b-154">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8b31b-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b31b-155">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8b31b-155">INPUTS</span></span>

### <span data-ttu-id="8b31b-156">Microsoft. Azure. Commands. keyvault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="8b31b-156">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="8b31b-157">System. String</span><span class="sxs-lookup"><span data-stu-id="8b31b-157">System.String</span></span>

## <span data-ttu-id="8b31b-158">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8b31b-158">OUTPUTS</span></span>

### <span data-ttu-id="8b31b-159">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8b31b-159">System.Boolean</span></span>

## <span data-ttu-id="8b31b-160">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8b31b-160">NOTES</span></span>

## <span data-ttu-id="8b31b-161">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8b31b-161">RELATED LINKS</span></span>

[<span data-ttu-id="8b31b-162">Get-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="8b31b-162">Get-AzKeyVault</span></span>](./Get-AzKeyVault.md)

[<span data-ttu-id="8b31b-163">New-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="8b31b-163">New-AzKeyVault</span></span>](./New-AzKeyVault.md)

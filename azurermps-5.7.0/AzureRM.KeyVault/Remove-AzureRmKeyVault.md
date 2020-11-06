---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 7A929BA8-02D9-4BBE-AFF3-B8781F8DDAD9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurermkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureRmKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureRmKeyVault.md
ms.openlocfilehash: 0c9e37433d28a16a28ca56daf4a726347b7a9533
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602855"
---
# <span data-ttu-id="2d4e5-101">Remove-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="2d4e5-101">Remove-AzureRmKeyVault</span></span>

## <span data-ttu-id="2d4e5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2d4e5-102">SYNOPSIS</span></span>
<span data-ttu-id="2d4e5-103">Exclui um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="2d4e5-103">Deletes a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2d4e5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2d4e5-104">SYNTAX</span></span>

### <span data-ttu-id="2d4e5-105">ByAvailableVault (padrão)</span><span class="sxs-lookup"><span data-stu-id="2d4e5-105">ByAvailableVault (Default)</span></span>
```
Remove-AzureRmKeyVault [-VaultName] <String> [[-ResourceGroupName] <String>] [[-Location] <String>] [-Force]
 [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2d4e5-106">ByDeletedVault</span><span class="sxs-lookup"><span data-stu-id="2d4e5-106">ByDeletedVault</span></span>
```
Remove-AzureRmKeyVault [-VaultName] <String> [-Location] <String> [-InRemovedState] [-Force] [-AsJob]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2d4e5-107">InputObjectByAvailableVault</span><span class="sxs-lookup"><span data-stu-id="2d4e5-107">InputObjectByAvailableVault</span></span>
```
Remove-AzureRmKeyVault [-InputObject] <PSKeyVault> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2d4e5-108">InputObjectByDeletedVault</span><span class="sxs-lookup"><span data-stu-id="2d4e5-108">InputObjectByDeletedVault</span></span>
```
Remove-AzureRmKeyVault [-InputObject] <PSKeyVault> [-InRemovedState] [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2d4e5-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2d4e5-109">DESCRIPTION</span></span>
<span data-ttu-id="2d4e5-110">O cmdlet **Remove-AzureRmKeyVault** exclui o cofre de chaves especificado.</span><span class="sxs-lookup"><span data-stu-id="2d4e5-110">The **Remove-AzureRmKeyVault** cmdlet deletes the specified key vault.</span></span>
<span data-ttu-id="2d4e5-111">Ele também exclui todas as chaves e segredos contidos nessa instância.</span><span class="sxs-lookup"><span data-stu-id="2d4e5-111">It also deletes all keys and secrets contained in that instance.</span></span>

<span data-ttu-id="2d4e5-112">Observe que, embora a especificação do grupo de recursos seja opcional para esse cmdlet, você deve fazê-lo para melhorar o desempenho.</span><span class="sxs-lookup"><span data-stu-id="2d4e5-112">Note that although specifying the resource group is optional for this cmdlet, you should so for better performance.</span></span>

## <span data-ttu-id="2d4e5-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2d4e5-113">EXAMPLES</span></span>

### <span data-ttu-id="2d4e5-114">Exemplo 1: remover um cofre de chaves</span><span class="sxs-lookup"><span data-stu-id="2d4e5-114">Example 1: Remove a key vault</span></span>
```
PS C:\>Remove-AzureRmKeyVault -VaultName "Contoso03Vault"
```

<span data-ttu-id="2d4e5-115">Esse comando Remove o cofre de chaves denominado Contoso03Vault da sua assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="2d4e5-115">This command removes the key vault named Contoso03Vault from your current subscription.</span></span>

### <span data-ttu-id="2d4e5-116">Exemplo 2: remover um cofre de chaves de um grupo de recursos especificado</span><span class="sxs-lookup"><span data-stu-id="2d4e5-116">Example 2: Remove a key vault from a specified resource group</span></span>
```
PS C:\>Remove-AzureRmKeyVault -VaultName "Contoso03Vault" -ResourceGroupName "Group14"
```

<span data-ttu-id="2d4e5-117">Esse comando Remove o cofre de chaves chamado Contoso03Vault do grupo de recursos nomeado.</span><span class="sxs-lookup"><span data-stu-id="2d4e5-117">This command removes the key vault named Contoso03Vault from the named resource group.</span></span>
<span data-ttu-id="2d4e5-118">Se você não especificar o nome do grupo de recursos, o cmdlet pesquisará o cofre de chaves nomeados para excluir na sua assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="2d4e5-118">If you do not specify the resource group name, the cmdlet searches for the named key vault to delete in your current subscription.</span></span>

## <span data-ttu-id="2d4e5-119">OS</span><span class="sxs-lookup"><span data-stu-id="2d4e5-119">PARAMETERS</span></span>

### <span data-ttu-id="2d4e5-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2d4e5-120">-AsJob</span></span>
<span data-ttu-id="2d4e5-121">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="2d4e5-121">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d4e5-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d4e5-122">-DefaultProfile</span></span>
<span data-ttu-id="2d4e5-123">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="2d4e5-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d4e5-124">-Force</span><span class="sxs-lookup"><span data-stu-id="2d4e5-124">-Force</span></span>
<span data-ttu-id="2d4e5-125">Indica que o cmdlet não solicita confirmação.</span><span class="sxs-lookup"><span data-stu-id="2d4e5-125">Indicates that the cmdlet does not prompt you for confirmation.</span></span>
<span data-ttu-id="2d4e5-126">Por padrão, esse cmdlet solicita que você confirme que deseja excluir o cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="2d4e5-126">By default, this cmdlet prompts you to confirm that you want to delete the key vault.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d4e5-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2d4e5-127">-InputObject</span></span>
<span data-ttu-id="2d4e5-128">Objeto do cofre de chaves a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="2d4e5-128">Key Vault object to be deleted.</span></span>

```yaml
Type: PSKeyVault
Parameter Sets: InputObjectByAvailableVault, InputObjectByDeletedVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2d4e5-129">-Inremovestate</span><span class="sxs-lookup"><span data-stu-id="2d4e5-129">-InRemovedState</span></span>
<span data-ttu-id="2d4e5-130">Remova permanentemente o cofre excluído anteriormente.</span><span class="sxs-lookup"><span data-stu-id="2d4e5-130">Remove the previously deleted vault permanently.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByDeletedVault, InputObjectByDeletedVault
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d4e5-131">-Local</span><span class="sxs-lookup"><span data-stu-id="2d4e5-131">-Location</span></span>
<span data-ttu-id="2d4e5-132">O local do cofre excluído.</span><span class="sxs-lookup"><span data-stu-id="2d4e5-132">The location of the deleted vault.</span></span>

```yaml
Type: String
Parameter Sets: ByAvailableVault
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByDeletedVault
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d4e5-133">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2d4e5-133">-PassThru</span></span>
<span data-ttu-id="2d4e5-134">Esse cmdlet não retorna um objeto por padrão.</span><span class="sxs-lookup"><span data-stu-id="2d4e5-134">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="2d4e5-135">Se essa opção for especificada, retornará true se for bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="2d4e5-135">If this switch is specified, it returns true if successful.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d4e5-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d4e5-136">-ResourceGroupName</span></span>
<span data-ttu-id="2d4e5-137">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="2d4e5-137">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: ByAvailableVault
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d4e5-138">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="2d4e5-138">-VaultName</span></span>
<span data-ttu-id="2d4e5-139">Especifica o nome do cofre de chaves a ser removido.</span><span class="sxs-lookup"><span data-stu-id="2d4e5-139">Specifies the name of the key vault to remove.</span></span>

```yaml
Type: String
Parameter Sets: ByAvailableVault, ByDeletedVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d4e5-140">-Confirme</span><span class="sxs-lookup"><span data-stu-id="2d4e5-140">-Confirm</span></span>
<span data-ttu-id="2d4e5-141">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2d4e5-141">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d4e5-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2d4e5-142">-WhatIf</span></span>
<span data-ttu-id="2d4e5-143">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2d4e5-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2d4e5-144">O cmdlet não é executado. Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2d4e5-144">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2d4e5-145">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2d4e5-145">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d4e5-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d4e5-146">CommonParameters</span></span>
<span data-ttu-id="2d4e5-147">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2d4e5-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d4e5-148">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2d4e5-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d4e5-149">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2d4e5-149">INPUTS</span></span>

### <span data-ttu-id="2d4e5-150">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="2d4e5-150">None</span></span>
<span data-ttu-id="2d4e5-151">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="2d4e5-151">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2d4e5-152">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2d4e5-152">OUTPUTS</span></span>

### <span data-ttu-id="2d4e5-153">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2d4e5-153">System.Boolean</span></span>

## <span data-ttu-id="2d4e5-154">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2d4e5-154">NOTES</span></span>

## <span data-ttu-id="2d4e5-155">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2d4e5-155">RELATED LINKS</span></span>

[<span data-ttu-id="2d4e5-156">Get-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="2d4e5-156">Get-AzureRmKeyVault</span></span>](./Get-AzureRmKeyVault.md)

[<span data-ttu-id="2d4e5-157">New-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="2d4e5-157">New-AzureRmKeyVault</span></span>](./New-AzureRmKeyVault.md)

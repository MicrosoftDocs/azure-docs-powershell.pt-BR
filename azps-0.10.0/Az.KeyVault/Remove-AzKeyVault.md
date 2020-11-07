---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 7A929BA8-02D9-4BBE-AFF3-B8781F8DDAD9
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/remove-Azkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Remove-AzKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Remove-AzKeyVault.md
ms.openlocfilehash: 20187e2d7a844b472217fd30acbac9805e85ad40
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776662"
---
# <span data-ttu-id="8afac-101">Remove-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="8afac-101">Remove-AzKeyVault</span></span>

## <span data-ttu-id="8afac-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8afac-102">SYNOPSIS</span></span>
<span data-ttu-id="8afac-103">Exclui um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="8afac-103">Deletes a key vault.</span></span>

## <span data-ttu-id="8afac-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8afac-104">SYNTAX</span></span>

### <span data-ttu-id="8afac-105">ByAvailableVault</span><span class="sxs-lookup"><span data-stu-id="8afac-105">ByAvailableVault</span></span>
```
Remove-AzKeyVault [-VaultName] <String> [[-ResourceGroupName] <String>] [[-Location] <String>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8afac-106">ByDeletedVault</span><span class="sxs-lookup"><span data-stu-id="8afac-106">ByDeletedVault</span></span>
```
Remove-AzKeyVault [-VaultName] <String> [-Location] <String> [-Force] [-InRemovedState] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8afac-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8afac-107">DESCRIPTION</span></span>
<span data-ttu-id="8afac-108">O cmdlet **Remove-AzKeyVault** exclui o cofre de chaves especificado.</span><span class="sxs-lookup"><span data-stu-id="8afac-108">The **Remove-AzKeyVault** cmdlet deletes the specified key vault.</span></span>
<span data-ttu-id="8afac-109">Ele também exclui todas as chaves e segredos contidos nessa instância.</span><span class="sxs-lookup"><span data-stu-id="8afac-109">It also deletes all keys and secrets contained in that instance.</span></span>

<span data-ttu-id="8afac-110">Observe que, embora a especificação do grupo de recursos seja opcional para esse cmdlet, você deve fazê-lo para melhorar o desempenho.</span><span class="sxs-lookup"><span data-stu-id="8afac-110">Note that although specifying the resource group is optional for this cmdlet, you should so for better performance.</span></span>

## <span data-ttu-id="8afac-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8afac-111">EXAMPLES</span></span>

### <span data-ttu-id="8afac-112">Exemplo 1: remover um cofre de chaves</span><span class="sxs-lookup"><span data-stu-id="8afac-112">Example 1: Remove a key vault</span></span>
```
PS C:\>Remove-AzKeyVault -VaultName "Contoso03Vault"
```

<span data-ttu-id="8afac-113">Esse comando Remove o cofre de chaves denominado Contoso03Vault da sua assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="8afac-113">This command removes the key vault named Contoso03Vault from your current subscription.</span></span>

### <span data-ttu-id="8afac-114">Exemplo 2: remover um cofre de chaves de um grupo de recursos especificado</span><span class="sxs-lookup"><span data-stu-id="8afac-114">Example 2: Remove a key vault from a specified resource group</span></span>
```
PS C:\>Remove-AzKeyVault -VaultName "Contoso03Vault" -ResourceGroupName "Group14"
```

<span data-ttu-id="8afac-115">Esse comando Remove o cofre de chaves chamado Contoso03Vault do grupo de recursos nomeado.</span><span class="sxs-lookup"><span data-stu-id="8afac-115">This command removes the key vault named Contoso03Vault from the named resource group.</span></span>
<span data-ttu-id="8afac-116">Se você não especificar o nome do grupo de recursos, o cmdlet pesquisará o cofre de chaves nomeados para excluir na sua assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="8afac-116">If you do not specify the resource group name, the cmdlet searches for the named key vault to delete in your current subscription.</span></span>

## <span data-ttu-id="8afac-117">OS</span><span class="sxs-lookup"><span data-stu-id="8afac-117">PARAMETERS</span></span>

### <span data-ttu-id="8afac-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8afac-118">-AsJob</span></span>
<span data-ttu-id="8afac-119">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="8afac-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8afac-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8afac-120">-DefaultProfile</span></span>
<span data-ttu-id="8afac-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="8afac-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8afac-122">-Force</span><span class="sxs-lookup"><span data-stu-id="8afac-122">-Force</span></span>
<span data-ttu-id="8afac-123">Indica que o cmdlet não solicita confirmação.</span><span class="sxs-lookup"><span data-stu-id="8afac-123">Indicates that the cmdlet does not prompt you for confirmation.</span></span>
<span data-ttu-id="8afac-124">Por padrão, esse cmdlet solicita que você confirme que deseja excluir o cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="8afac-124">By default, this cmdlet prompts you to confirm that you want to delete the key vault.</span></span>

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

### <span data-ttu-id="8afac-125">-Inremovestate</span><span class="sxs-lookup"><span data-stu-id="8afac-125">-InRemovedState</span></span>
<span data-ttu-id="8afac-126">Remova permanentemente o cofre excluído anteriormente.</span><span class="sxs-lookup"><span data-stu-id="8afac-126">Remove the previously deleted vault permanently.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByDeletedVault
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8afac-127">-Local</span><span class="sxs-lookup"><span data-stu-id="8afac-127">-Location</span></span>
<span data-ttu-id="8afac-128">O local do cofre excluído.</span><span class="sxs-lookup"><span data-stu-id="8afac-128">The location of the deleted vault.</span></span>

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

### <span data-ttu-id="8afac-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8afac-129">-ResourceGroupName</span></span>
<span data-ttu-id="8afac-130">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="8afac-130">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="8afac-131">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="8afac-131">-VaultName</span></span>
<span data-ttu-id="8afac-132">Especifica o nome do cofre de chaves a ser removido.</span><span class="sxs-lookup"><span data-stu-id="8afac-132">Specifies the name of the key vault to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8afac-133">-Confirme</span><span class="sxs-lookup"><span data-stu-id="8afac-133">-Confirm</span></span>
<span data-ttu-id="8afac-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8afac-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8afac-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8afac-135">-WhatIf</span></span>
<span data-ttu-id="8afac-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8afac-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8afac-137">O cmdlet não é executado. Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8afac-137">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8afac-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8afac-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8afac-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8afac-139">CommonParameters</span></span>
<span data-ttu-id="8afac-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8afac-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8afac-141">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8afac-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8afac-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8afac-142">INPUTS</span></span>

### <span data-ttu-id="8afac-143">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="8afac-143">None</span></span>
<span data-ttu-id="8afac-144">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="8afac-144">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8afac-145">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8afac-145">OUTPUTS</span></span>

## <span data-ttu-id="8afac-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8afac-146">NOTES</span></span>

## <span data-ttu-id="8afac-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8afac-147">RELATED LINKS</span></span>

[<span data-ttu-id="8afac-148">Get-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="8afac-148">Get-AzKeyVault</span></span>](./Get-AzKeyVault.md)

[<span data-ttu-id="8afac-149">New-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="8afac-149">New-AzKeyVault</span></span>](./New-AzKeyVault.md)

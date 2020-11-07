---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 7A929BA8-02D9-4BBE-AFF3-B8781F8DDAD9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurermkeyvault
schema: 2.0.0
ms.openlocfilehash: 2365a58093be3193c7ac285d6dd38fbaf769ccd4
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785209"
---
# <span data-ttu-id="a3309-101">Remove-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="a3309-101">Remove-AzureRmKeyVault</span></span>

## <span data-ttu-id="a3309-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a3309-102">SYNOPSIS</span></span>
<span data-ttu-id="a3309-103">Exclui um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="a3309-103">Deletes a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a3309-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a3309-104">SYNTAX</span></span>

### <span data-ttu-id="a3309-105">ByAvailableVault</span><span class="sxs-lookup"><span data-stu-id="a3309-105">ByAvailableVault</span></span>
```
Remove-AzureRmKeyVault [-VaultName] <String> [[-ResourceGroupName] <String>] [[-Location] <String>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a3309-106">ByDeletedVault</span><span class="sxs-lookup"><span data-stu-id="a3309-106">ByDeletedVault</span></span>
```
Remove-AzureRmKeyVault [-VaultName] <String> [-Location] <String> [-Force] [-InRemovedState] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a3309-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a3309-107">DESCRIPTION</span></span>
<span data-ttu-id="a3309-108">O cmdlet **Remove-AzureRmKeyVault** exclui o cofre de chaves especificado.</span><span class="sxs-lookup"><span data-stu-id="a3309-108">The **Remove-AzureRmKeyVault** cmdlet deletes the specified key vault.</span></span>
<span data-ttu-id="a3309-109">Ele também exclui todas as chaves e segredos contidos nessa instância.</span><span class="sxs-lookup"><span data-stu-id="a3309-109">It also deletes all keys and secrets contained in that instance.</span></span>

<span data-ttu-id="a3309-110">Observe que, embora a especificação do grupo de recursos seja opcional para esse cmdlet, você deve fazê-lo para melhorar o desempenho.</span><span class="sxs-lookup"><span data-stu-id="a3309-110">Note that although specifying the resource group is optional for this cmdlet, you should so for better performance.</span></span>

## <span data-ttu-id="a3309-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a3309-111">EXAMPLES</span></span>

### <span data-ttu-id="a3309-112">Exemplo 1: remover um cofre de chaves</span><span class="sxs-lookup"><span data-stu-id="a3309-112">Example 1: Remove a key vault</span></span>
```
PS C:\>Remove-AzureRmKeyVault -VaultName "Contoso03Vault"
```

<span data-ttu-id="a3309-113">Esse comando Remove o cofre de chaves denominado Contoso03Vault da sua assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="a3309-113">This command removes the key vault named Contoso03Vault from your current subscription.</span></span>

### <span data-ttu-id="a3309-114">Exemplo 2: remover um cofre de chaves de um grupo de recursos especificado</span><span class="sxs-lookup"><span data-stu-id="a3309-114">Example 2: Remove a key vault from a specified resource group</span></span>
```
PS C:\>Remove-AzureRmKeyVault -VaultName "Contoso03Vault" -ResourceGroupName "Group14"
```

<span data-ttu-id="a3309-115">Esse comando Remove o cofre de chaves chamado Contoso03Vault do grupo de recursos nomeado.</span><span class="sxs-lookup"><span data-stu-id="a3309-115">This command removes the key vault named Contoso03Vault from the named resource group.</span></span>
<span data-ttu-id="a3309-116">Se você não especificar o nome do grupo de recursos, o cmdlet pesquisará o cofre de chaves nomeados para excluir na sua assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="a3309-116">If you do not specify the resource group name, the cmdlet searches for the named key vault to delete in your current subscription.</span></span>

## <span data-ttu-id="a3309-117">OS</span><span class="sxs-lookup"><span data-stu-id="a3309-117">PARAMETERS</span></span>

### <span data-ttu-id="a3309-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a3309-118">-AsJob</span></span>
<span data-ttu-id="a3309-119">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="a3309-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a3309-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3309-120">-DefaultProfile</span></span>
<span data-ttu-id="a3309-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="a3309-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a3309-122">-Force</span><span class="sxs-lookup"><span data-stu-id="a3309-122">-Force</span></span>
<span data-ttu-id="a3309-123">Indica que o cmdlet não solicita confirmação.</span><span class="sxs-lookup"><span data-stu-id="a3309-123">Indicates that the cmdlet does not prompt you for confirmation.</span></span>
<span data-ttu-id="a3309-124">Por padrão, esse cmdlet solicita que você confirme que deseja excluir o cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="a3309-124">By default, this cmdlet prompts you to confirm that you want to delete the key vault.</span></span>

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

### <span data-ttu-id="a3309-125">-Inremovestate</span><span class="sxs-lookup"><span data-stu-id="a3309-125">-InRemovedState</span></span>
<span data-ttu-id="a3309-126">Remova permanentemente o cofre excluído anteriormente.</span><span class="sxs-lookup"><span data-stu-id="a3309-126">Remove the previously deleted vault permanently.</span></span>

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

### <span data-ttu-id="a3309-127">-Local</span><span class="sxs-lookup"><span data-stu-id="a3309-127">-Location</span></span>
<span data-ttu-id="a3309-128">O local do cofre excluído.</span><span class="sxs-lookup"><span data-stu-id="a3309-128">The location of the deleted vault.</span></span>

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

### <span data-ttu-id="a3309-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3309-129">-ResourceGroupName</span></span>
<span data-ttu-id="a3309-130">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a3309-130">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="a3309-131">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="a3309-131">-VaultName</span></span>
<span data-ttu-id="a3309-132">Especifica o nome do cofre de chaves a ser removido.</span><span class="sxs-lookup"><span data-stu-id="a3309-132">Specifies the name of the key vault to remove.</span></span>

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

### <span data-ttu-id="a3309-133">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a3309-133">-Confirm</span></span>
<span data-ttu-id="a3309-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a3309-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a3309-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a3309-135">-WhatIf</span></span>
<span data-ttu-id="a3309-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a3309-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a3309-137">O cmdlet não é executado. Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a3309-137">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a3309-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a3309-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a3309-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3309-139">CommonParameters</span></span>
<span data-ttu-id="a3309-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3309-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3309-141">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a3309-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3309-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a3309-142">INPUTS</span></span>

## <span data-ttu-id="a3309-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a3309-143">OUTPUTS</span></span>

## <span data-ttu-id="a3309-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a3309-144">NOTES</span></span>

## <span data-ttu-id="a3309-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a3309-145">RELATED LINKS</span></span>

[<span data-ttu-id="a3309-146">Get-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="a3309-146">Get-AzureRmKeyVault</span></span>](./Get-AzureRmKeyVault.md)

[<span data-ttu-id="a3309-147">New-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="a3309-147">New-AzureRmKeyVault</span></span>](./New-AzureRmKeyVault.md)

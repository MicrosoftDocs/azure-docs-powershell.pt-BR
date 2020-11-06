---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 7A929BA8-02D9-4BBE-AFF3-B8781F8DDAD9
online version: https://go.microsoft.com/fwlink/?LinkId=690162
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureRmKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureRmKeyVault.md
ms.openlocfilehash: 2a30a190fbf257142e1c1e4fb4329fd6c4f41e3d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93439930"
---
# <span data-ttu-id="ba678-101">Remove-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="ba678-101">Remove-AzureRmKeyVault</span></span>

## <span data-ttu-id="ba678-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ba678-102">SYNOPSIS</span></span>
<span data-ttu-id="ba678-103">Exclui um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="ba678-103">Deletes a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ba678-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ba678-104">SYNTAX</span></span>

### <span data-ttu-id="ba678-105">ByAvailableVault</span><span class="sxs-lookup"><span data-stu-id="ba678-105">ByAvailableVault</span></span>
```
Remove-AzureRmKeyVault [-VaultName] <String> [[-ResourceGroupName] <String>] [[-Location] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ba678-106">ByDeletedVault</span><span class="sxs-lookup"><span data-stu-id="ba678-106">ByDeletedVault</span></span>
```
Remove-AzureRmKeyVault [-VaultName] <String> [-Location] <String> [-Force] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ba678-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ba678-107">DESCRIPTION</span></span>
<span data-ttu-id="ba678-108">O cmdlet **Remove-AzureRmKeyVault** exclui o cofre de chaves especificado.</span><span class="sxs-lookup"><span data-stu-id="ba678-108">The **Remove-AzureRmKeyVault** cmdlet deletes the specified key vault.</span></span>
<span data-ttu-id="ba678-109">Ele também exclui todas as chaves e segredos contidos nessa instância.</span><span class="sxs-lookup"><span data-stu-id="ba678-109">It also deletes all keys and secrets contained in that instance.</span></span>

<span data-ttu-id="ba678-110">Observe que, embora a especificação do grupo de recursos seja opcional para esse cmdlet, você deve fazê-lo para melhorar o desempenho.</span><span class="sxs-lookup"><span data-stu-id="ba678-110">Note that although specifying the resource group is optional for this cmdlet, you should so for better performance.</span></span>

## <span data-ttu-id="ba678-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ba678-111">EXAMPLES</span></span>

### <span data-ttu-id="ba678-112">Exemplo 1: remover um cofre de chaves</span><span class="sxs-lookup"><span data-stu-id="ba678-112">Example 1: Remove a key vault</span></span>
```
PS C:\>Remove-AzureRmKeyVault -VaultName "Contoso03Vault"
```

<span data-ttu-id="ba678-113">Esse comando Remove o cofre de chaves denominado Contoso03Vault da sua assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="ba678-113">This command removes the key vault named Contoso03Vault from your current subscription.</span></span>

### <span data-ttu-id="ba678-114">Exemplo 2: remover um cofre de chaves de um grupo de recursos especificado</span><span class="sxs-lookup"><span data-stu-id="ba678-114">Example 2: Remove a key vault from a specified resource group</span></span>
```
PS C:\>Remove-AzureRmKeyVault -VaultName "Contoso03Vault" -ResourceGroupName "Group14"
```

<span data-ttu-id="ba678-115">Esse comando Remove o cofre de chaves chamado Contoso03Vault do grupo de recursos nomeado.</span><span class="sxs-lookup"><span data-stu-id="ba678-115">This command removes the key vault named Contoso03Vault from the named resource group.</span></span>
<span data-ttu-id="ba678-116">Se você não especificar o nome do grupo de recursos, o cmdlet pesquisará o cofre de chaves nomeados para excluir na sua assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="ba678-116">If you do not specify the resource group name, the cmdlet searches for the named key vault to delete in your current subscription.</span></span>

## <span data-ttu-id="ba678-117">OS</span><span class="sxs-lookup"><span data-stu-id="ba678-117">PARAMETERS</span></span>

### <span data-ttu-id="ba678-118">-Force</span><span class="sxs-lookup"><span data-stu-id="ba678-118">-Force</span></span>
<span data-ttu-id="ba678-119">Indica que o cmdlet não solicita confirmação.</span><span class="sxs-lookup"><span data-stu-id="ba678-119">Indicates that the cmdlet does not prompt you for confirmation.</span></span>
<span data-ttu-id="ba678-120">Por padrão, esse cmdlet solicita que você confirme que deseja excluir o cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="ba678-120">By default, this cmdlet prompts you to confirm that you want to delete the key vault.</span></span>

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

### <span data-ttu-id="ba678-121">-Inremovestate</span><span class="sxs-lookup"><span data-stu-id="ba678-121">-InRemovedState</span></span>
<span data-ttu-id="ba678-122">Remova permanentemente o cofre excluído anteriormente.</span><span class="sxs-lookup"><span data-stu-id="ba678-122">Remove the previously deleted vault permanently.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByDeletedVault
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba678-123">-Local</span><span class="sxs-lookup"><span data-stu-id="ba678-123">-Location</span></span>
<span data-ttu-id="ba678-124">O local do cofre excluído.</span><span class="sxs-lookup"><span data-stu-id="ba678-124">The location of the deleted vault.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAvailableVault
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByDeletedVault
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba678-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba678-125">-ResourceGroupName</span></span>
<span data-ttu-id="ba678-126">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ba678-126">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAvailableVault
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba678-127">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="ba678-127">-VaultName</span></span>
<span data-ttu-id="ba678-128">Especifica o nome do cofre de chaves a ser removido.</span><span class="sxs-lookup"><span data-stu-id="ba678-128">Specifies the name of the key vault to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba678-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="ba678-129">-Confirm</span></span>
<span data-ttu-id="ba678-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ba678-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ba678-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba678-131">-WhatIf</span></span>
<span data-ttu-id="ba678-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ba678-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ba678-133">O cmdlet não é executado. Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ba678-133">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ba678-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ba678-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ba678-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba678-135">-DefaultProfile</span></span>
<span data-ttu-id="ba678-136">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ba678-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba678-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba678-137">CommonParameters</span></span>
<span data-ttu-id="ba678-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba678-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba678-139">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba678-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba678-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ba678-140">INPUTS</span></span>

## <span data-ttu-id="ba678-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ba678-141">OUTPUTS</span></span>

## <span data-ttu-id="ba678-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ba678-142">NOTES</span></span>

## <span data-ttu-id="ba678-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ba678-143">RELATED LINKS</span></span>

[<span data-ttu-id="ba678-144">Get-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="ba678-144">Get-AzureRmKeyVault</span></span>](./Get-AzureRmKeyVault.md)

[<span data-ttu-id="ba678-145">New-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="ba678-145">New-AzureRmKeyVault</span></span>](./New-AzureRmKeyVault.md)

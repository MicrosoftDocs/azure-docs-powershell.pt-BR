---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/remove-azrmstoragecontainerlegalhold
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageContainerLegalHold.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageContainerLegalHold.md
ms.openlocfilehash: 9788acb95be63d9e76525cbeaf7904cd260baae0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890050"
---
# <span data-ttu-id="a5923-101">Remove-AzRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="a5923-101">Remove-AzRmStorageContainerLegalHold</span></span>

## <span data-ttu-id="a5923-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a5923-102">SYNOPSIS</span></span>
<span data-ttu-id="a5923-103">Remove marcas de remoção legais de um contêiner de blob de armazenamento</span><span class="sxs-lookup"><span data-stu-id="a5923-103">Removes legal hold tags from a Storage blob container</span></span>

## <span data-ttu-id="a5923-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="a5923-104">SYNTAX</span></span>

### <span data-ttu-id="a5923-105">AccountName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="a5923-105">AccountName (Default)</span></span>
```
Remove-AzRmStorageContainerLegalHold [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -Name <String> -Tag <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a5923-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="a5923-106">AccountObject</span></span>
```
Remove-AzRmStorageContainerLegalHold -Name <String> -StorageAccount <PSStorageAccount> -Tag <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5923-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="a5923-107">ContainerObject</span></span>
```
Remove-AzRmStorageContainerLegalHold -Container <PSContainer> -Tag <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a5923-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="a5923-108">DESCRIPTION</span></span>
<span data-ttu-id="a5923-109">O cmdlet **Remove-AzRmStorageContainerLegalHold** remove marcas de bloqueio legal de um contêiner de blob de armazenamento</span><span class="sxs-lookup"><span data-stu-id="a5923-109">The **Remove-AzRmStorageContainerLegalHold** cmdlet removes legal hold tags from a Storage blob container</span></span>

## <span data-ttu-id="a5923-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a5923-110">EXAMPLES</span></span>

### <span data-ttu-id="a5923-111">Exemplo 1: Remover marcas de responsabilidade legal de um contêiner de blob de armazenamento com o nome da conta de armazenamento e o nome do contêiner</span><span class="sxs-lookup"><span data-stu-id="a5923-111">Example 1: Remove legal hold tags from a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Remove-AzRmStorageContainerLegalHold -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -Tag  tag1
```

<span data-ttu-id="a5923-112">Este comando remove as marcas de remoção legais de um contêiner de blob de armazenamento com o nome da conta de armazenamento e o nome do contêiner.</span><span class="sxs-lookup"><span data-stu-id="a5923-112">This command removes legal hold tags from a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="a5923-113">Exemplo 2: Remover marcas de remoção legais de um contêiner de blob de armazenamento com o objeto de conta de armazenamento e o nome do contêiner</span><span class="sxs-lookup"><span data-stu-id="a5923-113">Example 2: Remove legal hold tags from a Storage blob container with Storage account object and container name</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Remove-AzRmStorageContainerLegalHold -StorageAccount $accountObject -ContainerName "myContainer"  -Tag  tag1,tag2
```

<span data-ttu-id="a5923-114">Este comando remove marcas de responsabilidade legal de um contêiner de blob de armazenamento com o objeto de conta de armazenamento e o nome do contêiner.</span><span class="sxs-lookup"><span data-stu-id="a5923-114">This command removes legal hold tags from a Storage blob container with Storage account object and container name.</span></span>

### <span data-ttu-id="a5923-115">Exemplo 3: Remover marcas de responsabilidade legal de todos os contêineres de blob de armazenamento em uma conta de armazenamento com pipeline</span><span class="sxs-lookup"><span data-stu-id="a5923-115">Example 3: Remove legal hold tags from all Storage blob containers in a Storage account with pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" | Remove-AzRmStorageContainerLegalHold -Tag  tag1
```

<span data-ttu-id="a5923-116">Este comando remove as marcas de remoção legais de todos os contêineres de blob de armazenamento em uma conta de armazenamento com pipeline.</span><span class="sxs-lookup"><span data-stu-id="a5923-116">This command removes legal hold tags from all Storage blob containers in a Storage account with pipeline.</span></span>

## <span data-ttu-id="a5923-117">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="a5923-117">PARAMETERS</span></span>

### <span data-ttu-id="a5923-118">-Container</span><span class="sxs-lookup"><span data-stu-id="a5923-118">-Container</span></span>
<span data-ttu-id="a5923-119">Objeto contêiner de armazenamento</span><span class="sxs-lookup"><span data-stu-id="a5923-119">Storage container object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSContainer
Parameter Sets: ContainerObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a5923-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5923-120">-DefaultProfile</span></span>
<span data-ttu-id="a5923-121">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="a5923-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a5923-122">-Name</span><span class="sxs-lookup"><span data-stu-id="a5923-122">-Name</span></span>
<span data-ttu-id="a5923-123">Nome do contêiner</span><span class="sxs-lookup"><span data-stu-id="a5923-123">Container Name</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountObject
Aliases: N, ContainerName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a5923-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5923-124">-ResourceGroupName</span></span>
<span data-ttu-id="a5923-125">Nome do Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="a5923-125">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5923-126">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="a5923-126">-StorageAccount</span></span>
<span data-ttu-id="a5923-127">Objeto de conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="a5923-127">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a5923-128">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="a5923-128">-StorageAccountName</span></span>
<span data-ttu-id="a5923-129">Nome da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="a5923-129">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5923-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="a5923-130">-Tag</span></span>
<span data-ttu-id="a5923-131">Marcas De Contêiner LegalHold</span><span class="sxs-lookup"><span data-stu-id="a5923-131">Container LegalHold Tags</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5923-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a5923-132">-Confirm</span></span>
<span data-ttu-id="a5923-133">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a5923-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5923-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5923-134">-WhatIf</span></span>
<span data-ttu-id="a5923-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a5923-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a5923-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a5923-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5923-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5923-137">CommonParameters</span></span>
<span data-ttu-id="a5923-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5923-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5923-139">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5923-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5923-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a5923-140">INPUTS</span></span>

### <span data-ttu-id="a5923-141">System.String</span><span class="sxs-lookup"><span data-stu-id="a5923-141">System.String</span></span>

### <span data-ttu-id="a5923-142">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a5923-142">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="a5923-143">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span><span class="sxs-lookup"><span data-stu-id="a5923-143">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="a5923-144">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="a5923-144">OUTPUTS</span></span>

### <span data-ttu-id="a5923-145">Microsoft.Azure.Commands.Management.Storage.Models.PSLegalHold</span><span class="sxs-lookup"><span data-stu-id="a5923-145">Microsoft.Azure.Commands.Management.Storage.Models.PSLegalHold</span></span>

## <span data-ttu-id="a5923-146">NOTES</span><span class="sxs-lookup"><span data-stu-id="a5923-146">NOTES</span></span>

## <span data-ttu-id="a5923-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a5923-147">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azrmstoragecontainerlegalhold
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageContainerLegalHold.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageContainerLegalHold.md
ms.openlocfilehash: 494995a97ccb74df9ad9a9fc1f88272505598bb9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114415"
---
# <span data-ttu-id="f1971-101">Remove-AzRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="f1971-101">Remove-AzRmStorageContainerLegalHold</span></span>

## <span data-ttu-id="f1971-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f1971-102">SYNOPSIS</span></span>
<span data-ttu-id="f1971-103">Remove marcas de remoção legal de um contêiner de blob armazenamento</span><span class="sxs-lookup"><span data-stu-id="f1971-103">Removes legal hold tags from a Storage blob container</span></span>

## <span data-ttu-id="f1971-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f1971-104">SYNTAX</span></span>

### <span data-ttu-id="f1971-105">Nomeda Conta (Padrão)</span><span class="sxs-lookup"><span data-stu-id="f1971-105">AccountName (Default)</span></span>
```
Remove-AzRmStorageContainerLegalHold [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -Name <String> -Tag <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f1971-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="f1971-106">AccountObject</span></span>
```
Remove-AzRmStorageContainerLegalHold -Name <String> -StorageAccount <PSStorageAccount> -Tag <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f1971-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="f1971-107">ContainerObject</span></span>
```
Remove-AzRmStorageContainerLegalHold -Container <PSContainer> -Tag <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f1971-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="f1971-108">DESCRIPTION</span></span>
<span data-ttu-id="f1971-109">O cmdlet **Remove-AzRmStorageContainerLegalHold** remove marcas de bloqueio legal de um contêiner de blob armazenamento</span><span class="sxs-lookup"><span data-stu-id="f1971-109">The **Remove-AzRmStorageContainerLegalHold** cmdlet removes legal hold tags from a Storage blob container</span></span>

## <span data-ttu-id="f1971-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f1971-110">EXAMPLES</span></span>

### <span data-ttu-id="f1971-111">Exemplo 1: Remover marcas de remoção legal de um contêiner de blob armazenamento com o nome da conta de armazenamento e o nome do contêiner</span><span class="sxs-lookup"><span data-stu-id="f1971-111">Example 1: Remove legal hold tags from a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Remove-AzRmStorageContainerLegalHold -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -Tag  tag1
```

<span data-ttu-id="f1971-112">Esse comando remove marcas de responsabilidade legal de um contêiner de blob armazenamento com o nome da conta de armazenamento e o nome do contêiner.</span><span class="sxs-lookup"><span data-stu-id="f1971-112">This command removes legal hold tags from a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="f1971-113">Exemplo 2: Remover marcas de remoção legal de um contêiner de blob armazenamento com o objeto de conta de armazenamento e o nome do contêiner</span><span class="sxs-lookup"><span data-stu-id="f1971-113">Example 2: Remove legal hold tags from a Storage blob container with Storage account object and container name</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Remove-AzRmStorageContainerLegalHold -StorageAccount $accountObject -ContainerName "myContainer"  -Tag  tag1,tag2
```

<span data-ttu-id="f1971-114">Esse comando remove marcas de responsabilidade legal de um contêiner de blob armazenamento com o objeto de conta de armazenamento e o nome do contêiner.</span><span class="sxs-lookup"><span data-stu-id="f1971-114">This command removes legal hold tags from a Storage blob container with Storage account object and container name.</span></span>

### <span data-ttu-id="f1971-115">Exemplo 3: Remover marcas de responsabilidade legal de todos os contêineres de blob armazenamento em uma conta de armazenamento com pipeline</span><span class="sxs-lookup"><span data-stu-id="f1971-115">Example 3: Remove legal hold tags from all Storage blob containers in a Storage account with pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" | Remove-AzRmStorageContainerLegalHold -Tag  tag1
```

<span data-ttu-id="f1971-116">Esse comando remove marcas de responsabilidade legal de todos os contêineres de blob de armazenamento em uma conta de armazenamento com pipeline.</span><span class="sxs-lookup"><span data-stu-id="f1971-116">This command removes legal hold tags from all Storage blob containers in a Storage account with pipeline.</span></span>

## <span data-ttu-id="f1971-117">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f1971-117">PARAMETERS</span></span>

### <span data-ttu-id="f1971-118">-Contêiner</span><span class="sxs-lookup"><span data-stu-id="f1971-118">-Container</span></span>
<span data-ttu-id="f1971-119">Objeto de contêiner de armazenamento</span><span class="sxs-lookup"><span data-stu-id="f1971-119">Storage container object</span></span>

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

### <span data-ttu-id="f1971-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1971-120">-DefaultProfile</span></span>
<span data-ttu-id="f1971-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="f1971-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f1971-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="f1971-122">-Name</span></span>
<span data-ttu-id="f1971-123">Nome do Contêiner</span><span class="sxs-lookup"><span data-stu-id="f1971-123">Container Name</span></span>

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

### <span data-ttu-id="f1971-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1971-124">-ResourceGroupName</span></span>
<span data-ttu-id="f1971-125">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f1971-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="f1971-126">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="f1971-126">-StorageAccount</span></span>
<span data-ttu-id="f1971-127">Objeto de conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="f1971-127">Storage account object</span></span>

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

### <span data-ttu-id="f1971-128">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="f1971-128">-StorageAccountName</span></span>
<span data-ttu-id="f1971-129">Nome da Conta de Armazenamento.</span><span class="sxs-lookup"><span data-stu-id="f1971-129">Storage Account Name.</span></span>

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

### <span data-ttu-id="f1971-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="f1971-130">-Tag</span></span>
<span data-ttu-id="f1971-131">Container LegalHold Tags</span><span class="sxs-lookup"><span data-stu-id="f1971-131">Container LegalHold Tags</span></span>

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

### <span data-ttu-id="f1971-132">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="f1971-132">-Confirm</span></span>
<span data-ttu-id="f1971-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f1971-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f1971-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1971-134">-WhatIf</span></span>
<span data-ttu-id="f1971-135">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="f1971-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f1971-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f1971-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f1971-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1971-137">CommonParameters</span></span>
<span data-ttu-id="f1971-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1971-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1971-139">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f1971-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1971-140">Entradas</span><span class="sxs-lookup"><span data-stu-id="f1971-140">INPUTS</span></span>

### <span data-ttu-id="f1971-141">System.String</span><span class="sxs-lookup"><span data-stu-id="f1971-141">System.String</span></span>

### <span data-ttu-id="f1971-142">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f1971-142">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="f1971-143">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span><span class="sxs-lookup"><span data-stu-id="f1971-143">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="f1971-144">Saídas</span><span class="sxs-lookup"><span data-stu-id="f1971-144">OUTPUTS</span></span>

### <span data-ttu-id="f1971-145">Microsoft.Azure.Commands.Management.Storage.Models.PSLegalHold</span><span class="sxs-lookup"><span data-stu-id="f1971-145">Microsoft.Azure.Commands.Management.Storage.Models.PSLegalHold</span></span>

## <span data-ttu-id="f1971-146">Notas</span><span class="sxs-lookup"><span data-stu-id="f1971-146">NOTES</span></span>

## <span data-ttu-id="f1971-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f1971-147">RELATED LINKS</span></span>

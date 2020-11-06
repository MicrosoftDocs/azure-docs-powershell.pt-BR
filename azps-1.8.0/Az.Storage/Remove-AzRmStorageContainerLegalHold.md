---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azrmstoragecontainerlegalhold
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageContainerLegalHold.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageContainerLegalHold.md
ms.openlocfilehash: a7183498bba029a7b744a45bd34047926da4bf54
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93598586"
---
# <span data-ttu-id="51669-101">Remove-AzRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="51669-101">Remove-AzRmStorageContainerLegalHold</span></span>

## <span data-ttu-id="51669-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="51669-102">SYNOPSIS</span></span>
<span data-ttu-id="51669-103">Remove as marcas de retenção legal de um contêiner de blob de armazenamento</span><span class="sxs-lookup"><span data-stu-id="51669-103">Removes legal hold tags from a Storage blob container</span></span>

## <span data-ttu-id="51669-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="51669-104">SYNTAX</span></span>

### <span data-ttu-id="51669-105">AccountName (padrão)</span><span class="sxs-lookup"><span data-stu-id="51669-105">AccountName (Default)</span></span>
```
Remove-AzRmStorageContainerLegalHold [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -Name <String> -Tag <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="51669-106">Accountobject</span><span class="sxs-lookup"><span data-stu-id="51669-106">AccountObject</span></span>
```
Remove-AzRmStorageContainerLegalHold -Name <String> -StorageAccount <PSStorageAccount> -Tag <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="51669-107">Idcontêiner</span><span class="sxs-lookup"><span data-stu-id="51669-107">ContainerObject</span></span>
```
Remove-AzRmStorageContainerLegalHold -Container <PSContainer> -Tag <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="51669-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="51669-108">DESCRIPTION</span></span>
<span data-ttu-id="51669-109">O cmdlet **Remove-AzRmStorageContainerLegalHold** remove marcas de retenção legal de um contêiner de blob de armazenamento</span><span class="sxs-lookup"><span data-stu-id="51669-109">The **Remove-AzRmStorageContainerLegalHold** cmdlet removes legal hold tags from a Storage blob container</span></span>

## <span data-ttu-id="51669-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="51669-110">EXAMPLES</span></span>

### <span data-ttu-id="51669-111">Exemplo 1: remover as marcas de retenção legal de um contêiner de blob de armazenamento com nome da conta de armazenamento e nome do contêiner</span><span class="sxs-lookup"><span data-stu-id="51669-111">Example 1: Remove legal hold tags from a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Remove-AzRmStorageContainerLegalHold -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -Tag  tag1
```

<span data-ttu-id="51669-112">Esse comando remove as marcas de retenção legal de um contêiner de blob de armazenamento com nome da conta de armazenamento e nome do contêiner.</span><span class="sxs-lookup"><span data-stu-id="51669-112">This command removes legal hold tags from a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="51669-113">Exemplo 2: remover as marcas de retenção legal de um contêiner de blob de armazenamento com objeto da conta de armazenamento e nome do contêiner</span><span class="sxs-lookup"><span data-stu-id="51669-113">Example 2: Remove legal hold tags from a Storage blob container with Storage account object and container name</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Remove-AzRmStorageContainerLegalHold -StorageAccount $accountObject -ContainerName "myContainer"  -Tag  tag1,tag2
```

<span data-ttu-id="51669-114">Esse comando remove as marcas de retenção legal de um contêiner de blob de armazenamento com o objeto da conta de armazenamento e o nome do contêiner.</span><span class="sxs-lookup"><span data-stu-id="51669-114">This command removes legal hold tags from a Storage blob container with Storage account object and container name.</span></span>

### <span data-ttu-id="51669-115">Exemplo 3: remover as marcas de retenção legal de todos os contêineres de blob de armazenamento em uma conta de armazenamento com pipeline</span><span class="sxs-lookup"><span data-stu-id="51669-115">Example 3: Remove legal hold tags from all Storage blob containers in a Storage account with pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" | Remove-AzRmStorageContainerLegalHold -Tag  tag1
```

<span data-ttu-id="51669-116">Esse comando remove as marcas de retenção legal de todos os contêineres de blob de armazenamento em uma conta de armazenamento com pipeline.</span><span class="sxs-lookup"><span data-stu-id="51669-116">This command removes legal hold tags from all Storage blob containers in a Storage account with pipeline.</span></span>

## <span data-ttu-id="51669-117">OS</span><span class="sxs-lookup"><span data-stu-id="51669-117">PARAMETERS</span></span>

### <span data-ttu-id="51669-118">-Contêiner</span><span class="sxs-lookup"><span data-stu-id="51669-118">-Container</span></span>
<span data-ttu-id="51669-119">Objeto contêiner de armazenamento</span><span class="sxs-lookup"><span data-stu-id="51669-119">Storage container object</span></span>

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

### <span data-ttu-id="51669-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51669-120">-DefaultProfile</span></span>
<span data-ttu-id="51669-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="51669-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="51669-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="51669-122">-Name</span></span>
<span data-ttu-id="51669-123">Nome do contêiner</span><span class="sxs-lookup"><span data-stu-id="51669-123">Container Name</span></span>

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

### <span data-ttu-id="51669-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51669-124">-ResourceGroupName</span></span>
<span data-ttu-id="51669-125">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="51669-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="51669-126">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="51669-126">-StorageAccount</span></span>
<span data-ttu-id="51669-127">Objeto da conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="51669-127">Storage account object</span></span>

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

### <span data-ttu-id="51669-128">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="51669-128">-StorageAccountName</span></span>
<span data-ttu-id="51669-129">Nome da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="51669-129">Storage Account Name.</span></span>

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

### <span data-ttu-id="51669-130">-Marca</span><span class="sxs-lookup"><span data-stu-id="51669-130">-Tag</span></span>
<span data-ttu-id="51669-131">Marcas LegalHold do contêiner</span><span class="sxs-lookup"><span data-stu-id="51669-131">Container LegalHold Tags</span></span>

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

### <span data-ttu-id="51669-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="51669-132">-Confirm</span></span>
<span data-ttu-id="51669-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="51669-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="51669-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="51669-134">-WhatIf</span></span>
<span data-ttu-id="51669-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="51669-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="51669-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="51669-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="51669-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51669-137">CommonParameters</span></span>
<span data-ttu-id="51669-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51669-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51669-139">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51669-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51669-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="51669-140">INPUTS</span></span>

### <span data-ttu-id="51669-141">System. String</span><span class="sxs-lookup"><span data-stu-id="51669-141">System.String</span></span>

### <span data-ttu-id="51669-142">Microsoft. Azure. Commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="51669-142">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="51669-143">Microsoft. Azure. Commands. Management. Storage. Models. PSContainer</span><span class="sxs-lookup"><span data-stu-id="51669-143">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="51669-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="51669-144">OUTPUTS</span></span>

### <span data-ttu-id="51669-145">Microsoft. Azure. Commands. Management. Storage. Models. PSLegalHold</span><span class="sxs-lookup"><span data-stu-id="51669-145">Microsoft.Azure.Commands.Management.Storage.Models.PSLegalHold</span></span>

## <span data-ttu-id="51669-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="51669-146">NOTES</span></span>

## <span data-ttu-id="51669-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="51669-147">RELATED LINKS</span></span>

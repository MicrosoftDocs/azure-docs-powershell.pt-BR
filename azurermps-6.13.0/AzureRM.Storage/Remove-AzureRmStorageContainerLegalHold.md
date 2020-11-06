---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/remove-azurermstoragecontainerlegalhold
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Remove-AzureRmStorageContainerLegalHold.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Remove-AzureRmStorageContainerLegalHold.md
ms.openlocfilehash: da0793e7eb10f7b83d785aea34866842abe9b887
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431278"
---
# <span data-ttu-id="c1a40-101">Remove-AzureRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="c1a40-101">Remove-AzureRmStorageContainerLegalHold</span></span>

## <span data-ttu-id="c1a40-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c1a40-102">SYNOPSIS</span></span>
<span data-ttu-id="c1a40-103">Remove as marcas de retenção legal de um contêiner de blob de armazenamento</span><span class="sxs-lookup"><span data-stu-id="c1a40-103">Removes legal hold tags from a Storage blob container</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c1a40-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c1a40-104">SYNTAX</span></span>

### <span data-ttu-id="c1a40-105">AccountName (padrão)</span><span class="sxs-lookup"><span data-stu-id="c1a40-105">AccountName (Default)</span></span>
```
Remove-AzureRmStorageContainerLegalHold [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -Name <String> -Tag <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c1a40-106">Accountobject</span><span class="sxs-lookup"><span data-stu-id="c1a40-106">AccountObject</span></span>
```
Remove-AzureRmStorageContainerLegalHold -Name <String> -StorageAccount <PSStorageAccount> -Tag <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c1a40-107">Idcontêiner</span><span class="sxs-lookup"><span data-stu-id="c1a40-107">ContainerObject</span></span>
```
Remove-AzureRmStorageContainerLegalHold -Container <PSContainer> -Tag <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c1a40-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c1a40-108">DESCRIPTION</span></span>
<span data-ttu-id="c1a40-109">O cmdlet **Remove-AzureRmStorageContainerLegalHold** remove marcas de retenção legal de um contêiner de blob de armazenamento</span><span class="sxs-lookup"><span data-stu-id="c1a40-109">The **Remove-AzureRmStorageContainerLegalHold** cmdlet removes legal hold tags from a Storage blob container</span></span>

## <span data-ttu-id="c1a40-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c1a40-110">EXAMPLES</span></span>

### <span data-ttu-id="c1a40-111">Exemplo 1: remover as marcas de retenção legal de um contêiner de blob de armazenamento com nome da conta de armazenamento e nome do contêiner</span><span class="sxs-lookup"><span data-stu-id="c1a40-111">Example 1: Remove legal hold tags from a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Remove-AzureRmStorageContainerLegalHold -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -Tag  tag1
```

<span data-ttu-id="c1a40-112">Esse comando remove as marcas de retenção legal de um contêiner de blob de armazenamento com nome da conta de armazenamento e nome do contêiner.</span><span class="sxs-lookup"><span data-stu-id="c1a40-112">This command removes legal hold tags from a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="c1a40-113">Exemplo 2: remover as marcas de retenção legal de um contêiner de blob de armazenamento com objeto da conta de armazenamento e nome do contêiner</span><span class="sxs-lookup"><span data-stu-id="c1a40-113">Example 2: Remove legal hold tags from a Storage blob container with Storage account object and container name</span></span>
```
PS C:\>$accountObject = Get-AzureRmStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Remove-AzureRmStorageContainerLegalHold -StorageAccount $accountObject -ContainerName "myContainer"  -Tag  tag1,tag2 
```

<span data-ttu-id="c1a40-114">Esse comando remove as marcas de retenção legal de um contêiner de blob de armazenamento com o objeto da conta de armazenamento e o nome do contêiner.</span><span class="sxs-lookup"><span data-stu-id="c1a40-114">This command removes legal hold tags from a Storage blob container with Storage account object and container name.</span></span>

### <span data-ttu-id="c1a40-115">Exemplo 3: remover as marcas de retenção legal de todos os contêineres de blob de armazenamento em uma conta de armazenamento com pipeline</span><span class="sxs-lookup"><span data-stu-id="c1a40-115">Example 3: Remove legal hold tags from all Storage blob containers in a Storage account with pipeline</span></span>
```
PS C:\>Get-AzureRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" | Remove-AzureRmStorageContainerLegalHold -Tag  tag1
```

<span data-ttu-id="c1a40-116">Esse comando remove as marcas de retenção legal de todos os contêineres de blob de armazenamento em uma conta de armazenamento com pipeline.</span><span class="sxs-lookup"><span data-stu-id="c1a40-116">This command removes legal hold tags from all Storage blob containers in a Storage account with pipeline.</span></span>


## <span data-ttu-id="c1a40-117">OS</span><span class="sxs-lookup"><span data-stu-id="c1a40-117">PARAMETERS</span></span>

### <span data-ttu-id="c1a40-118">-Contêiner</span><span class="sxs-lookup"><span data-stu-id="c1a40-118">-Container</span></span>
<span data-ttu-id="c1a40-119">Objeto contêiner de armazenamento</span><span class="sxs-lookup"><span data-stu-id="c1a40-119">Storage container object</span></span>

```yaml
Type: PSContainer
Parameter Sets: ContainerObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c1a40-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1a40-120">-DefaultProfile</span></span>
<span data-ttu-id="c1a40-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c1a40-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c1a40-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="c1a40-122">-Name</span></span>
<span data-ttu-id="c1a40-123">Nome do contêiner</span><span class="sxs-lookup"><span data-stu-id="c1a40-123">Container Name</span></span>

```yaml
Type: String
Parameter Sets: AccountName, AccountObject
Aliases: N, ContainerName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c1a40-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1a40-124">-ResourceGroupName</span></span>
<span data-ttu-id="c1a40-125">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c1a40-125">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: AccountName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1a40-126">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="c1a40-126">-StorageAccount</span></span>
<span data-ttu-id="c1a40-127">Objeto da conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="c1a40-127">Storage account object</span></span>

```yaml
Type: PSStorageAccount
Parameter Sets: AccountObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c1a40-128">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="c1a40-128">-StorageAccountName</span></span>
<span data-ttu-id="c1a40-129">Nome da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="c1a40-129">Storage Account Name.</span></span>

```yaml
Type: String
Parameter Sets: AccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1a40-130">-Marca</span><span class="sxs-lookup"><span data-stu-id="c1a40-130">-Tag</span></span>
<span data-ttu-id="c1a40-131">Marcas LegalHold do contêiner</span><span class="sxs-lookup"><span data-stu-id="c1a40-131">Container LegalHold Tags</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1a40-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c1a40-132">-Confirm</span></span>
<span data-ttu-id="c1a40-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c1a40-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1a40-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c1a40-134">-WhatIf</span></span>
<span data-ttu-id="c1a40-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c1a40-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c1a40-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c1a40-136">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1a40-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1a40-137">CommonParameters</span></span>
<span data-ttu-id="c1a40-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c1a40-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1a40-139">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c1a40-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1a40-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c1a40-140">INPUTS</span></span>

### <span data-ttu-id="c1a40-141">System. String</span><span class="sxs-lookup"><span data-stu-id="c1a40-141">System.String</span></span>

## <span data-ttu-id="c1a40-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c1a40-142">OUTPUTS</span></span>

### <span data-ttu-id="c1a40-143">Microsoft. Azure. Commands. Management. Storage. Models. PSLegalHold</span><span class="sxs-lookup"><span data-stu-id="c1a40-143">Microsoft.Azure.Commands.Management.Storage.Models.PSLegalHold</span></span>

## <span data-ttu-id="c1a40-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c1a40-144">NOTES</span></span>

## <span data-ttu-id="c1a40-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c1a40-145">RELATED LINKS</span></span>


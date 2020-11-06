---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/add-azurermstoragecontainerlegalhold
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Add-AzureRmStorageContainerLegalHold.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Add-AzureRmStorageContainerLegalHold.md
ms.openlocfilehash: 465a40e384e5ea7240e0ced2a010c88529feb2f5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427124"
---
# <span data-ttu-id="42ade-101">Add-AzureRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="42ade-101">Add-AzureRmStorageContainerLegalHold</span></span>

## <span data-ttu-id="42ade-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="42ade-102">SYNOPSIS</span></span>
<span data-ttu-id="42ade-103">Adiciona marcas de retenção legal a um contêiner de blob de armazenamento</span><span class="sxs-lookup"><span data-stu-id="42ade-103">Adds legal hold tags to a Storage blob container</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="42ade-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="42ade-104">SYNTAX</span></span>

### <span data-ttu-id="42ade-105">AccountName (padrão)</span><span class="sxs-lookup"><span data-stu-id="42ade-105">AccountName (Default)</span></span>
```
Add-AzureRmStorageContainerLegalHold [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -Name <String> -Tag <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="42ade-106">Accountobject</span><span class="sxs-lookup"><span data-stu-id="42ade-106">AccountObject</span></span>
```
Add-AzureRmStorageContainerLegalHold -Name <String> -StorageAccount <PSStorageAccount> -Tag <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="42ade-107">Idcontêiner</span><span class="sxs-lookup"><span data-stu-id="42ade-107">ContainerObject</span></span>
```
Add-AzureRmStorageContainerLegalHold -Container <PSContainer> -Tag <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="42ade-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="42ade-108">DESCRIPTION</span></span>
<span data-ttu-id="42ade-109">O cmdlet **Add-AzureRmStorageContainerLegalHold** adiciona marcas de retenção legal a um contêiner de blob de armazenamento</span><span class="sxs-lookup"><span data-stu-id="42ade-109">The **Add-AzureRmStorageContainerLegalHold** cmdlet adds legal hold tags to a Storage blob container</span></span>

## <span data-ttu-id="42ade-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="42ade-110">EXAMPLES</span></span>

### <span data-ttu-id="42ade-111">Exemplo 1: adicionar marcas de retenção legal a um contêiner de blob de armazenamento com nome da conta de armazenamento e nome do contêiner</span><span class="sxs-lookup"><span data-stu-id="42ade-111">Example 1: Add legal hold tags to a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Add-AzureRmStorageContainerLegalHold -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -Tag  tag1,tag2 
```

<span data-ttu-id="42ade-112">Esse comando adiciona marcas de retenção legal a um contêiner de blob de armazenamento com nome da conta de armazenamento e nome do contêiner.</span><span class="sxs-lookup"><span data-stu-id="42ade-112">This command adds legal hold tags to a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="42ade-113">Exemplo 2: adicionar marcas de retenção legal a um contêiner de blob de armazenamento com objeto da conta de armazenamento e nome do contêiner</span><span class="sxs-lookup"><span data-stu-id="42ade-113">Example 2: Add legal hold tags to a Storage blob container with Storage account object and container name</span></span>
```
PS C:\>$accountObject = Get-AzureRmStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Add-AzureRmStorageContainerLegalHold -StorageAccount $accountObject -ContainerName "myContainer"  -Tag  tag1
```

<span data-ttu-id="42ade-114">Esse comando adiciona marcas de retenção legal a um contêiner de blob de armazenamento com objeto da conta de armazenamento e nome do contêiner.</span><span class="sxs-lookup"><span data-stu-id="42ade-114">This command adds legal hold tags to a Storage blob container with Storage account object and container name.</span></span>

### <span data-ttu-id="42ade-115">Exemplo 3: adicionar marcas de retenção legal a todos os contêineres de armazenamento em uma conta de armazenamento com pipeline</span><span class="sxs-lookup"><span data-stu-id="42ade-115">Example 3: Add legal hold tags to all Storage blob containers in a Storage account with pipeline</span></span>
```
PS C:\>Get-AzureRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" | Add-AzureRmStorageContainerLegalHold -Tag  tag1,tag2,tag3
```

<span data-ttu-id="42ade-116">Esse comando adiciona marcas de retenção legal a todos os contêineres de armazenamento de BLOB em uma conta de armazenamento com pipeline.</span><span class="sxs-lookup"><span data-stu-id="42ade-116">This command adds legal hold tags to all Storage blob containers in a Storage account with pipeline.</span></span>

## <span data-ttu-id="42ade-117">OS</span><span class="sxs-lookup"><span data-stu-id="42ade-117">PARAMETERS</span></span>

### <span data-ttu-id="42ade-118">-Contêiner</span><span class="sxs-lookup"><span data-stu-id="42ade-118">-Container</span></span>
<span data-ttu-id="42ade-119">Objeto contêiner de armazenamento</span><span class="sxs-lookup"><span data-stu-id="42ade-119">Storage container object</span></span>

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

### <span data-ttu-id="42ade-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42ade-120">-DefaultProfile</span></span>
<span data-ttu-id="42ade-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="42ade-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="42ade-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="42ade-122">-Name</span></span>
<span data-ttu-id="42ade-123">Nome do contêiner</span><span class="sxs-lookup"><span data-stu-id="42ade-123">Container Name</span></span>

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

### <span data-ttu-id="42ade-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42ade-124">-ResourceGroupName</span></span>
<span data-ttu-id="42ade-125">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="42ade-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="42ade-126">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="42ade-126">-StorageAccount</span></span>
<span data-ttu-id="42ade-127">Objeto da conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="42ade-127">Storage account object</span></span>

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

### <span data-ttu-id="42ade-128">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="42ade-128">-StorageAccountName</span></span>
<span data-ttu-id="42ade-129">Nome da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="42ade-129">Storage Account Name.</span></span>

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

### <span data-ttu-id="42ade-130">-Marca</span><span class="sxs-lookup"><span data-stu-id="42ade-130">-Tag</span></span>
<span data-ttu-id="42ade-131">Marcas LegalHold do contêiner</span><span class="sxs-lookup"><span data-stu-id="42ade-131">Container LegalHold Tags</span></span>

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

### <span data-ttu-id="42ade-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="42ade-132">-Confirm</span></span>
<span data-ttu-id="42ade-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="42ade-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="42ade-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="42ade-134">-WhatIf</span></span>
<span data-ttu-id="42ade-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="42ade-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="42ade-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="42ade-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="42ade-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42ade-137">CommonParameters</span></span>
<span data-ttu-id="42ade-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42ade-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42ade-139">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42ade-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42ade-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="42ade-140">INPUTS</span></span>

### <span data-ttu-id="42ade-141">System. String</span><span class="sxs-lookup"><span data-stu-id="42ade-141">System.String</span></span>

## <span data-ttu-id="42ade-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="42ade-142">OUTPUTS</span></span>

### <span data-ttu-id="42ade-143">Microsoft. Azure. Commands. Management. Storage. Models. PSLegalHold</span><span class="sxs-lookup"><span data-stu-id="42ade-143">Microsoft.Azure.Commands.Management.Storage.Models.PSLegalHold</span></span>

## <span data-ttu-id="42ade-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="42ade-144">NOTES</span></span>

## <span data-ttu-id="42ade-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="42ade-145">RELATED LINKS</span></span>


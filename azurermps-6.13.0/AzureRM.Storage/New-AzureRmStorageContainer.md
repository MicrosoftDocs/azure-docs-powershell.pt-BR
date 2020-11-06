---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/new-azurermstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/New-AzureRmStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/New-AzureRmStorageContainer.md
ms.openlocfilehash: 8e136188a2857b53b566d30c439e222caea16abb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427123"
---
# <span data-ttu-id="fae58-101">New-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="fae58-101">New-AzureRmStorageContainer</span></span>

## <span data-ttu-id="fae58-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fae58-102">SYNOPSIS</span></span>
<span data-ttu-id="fae58-103">Cria um contêiner de blob de armazenamento</span><span class="sxs-lookup"><span data-stu-id="fae58-103">Creates a Storage blob container</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fae58-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fae58-104">SYNTAX</span></span>

### <span data-ttu-id="fae58-105">AccountName (padrão)</span><span class="sxs-lookup"><span data-stu-id="fae58-105">AccountName (Default)</span></span>
```
New-AzureRmStorageContainer [-ResourceGroupName] <String> [-StorageAccountName] <String> [-Name] <String>
 [-PublicAccess <PSPublicAccess>] [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fae58-106">Accountobject</span><span class="sxs-lookup"><span data-stu-id="fae58-106">AccountObject</span></span>
```
New-AzureRmStorageContainer -StorageAccount <PSStorageAccount> [-Name] <String>
 [-PublicAccess <PSPublicAccess>] [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fae58-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fae58-107">DESCRIPTION</span></span>
<span data-ttu-id="fae58-108">O cmdlet **New-AzureRmStorageContainer** cria um contêiner de blob de armazenamento</span><span class="sxs-lookup"><span data-stu-id="fae58-108">The **New-AzureRmStorageContainer** cmdlet creates a Storage blob container</span></span>

## <span data-ttu-id="fae58-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fae58-109">EXAMPLES</span></span>

### <span data-ttu-id="fae58-110">Exemplo 1: criar um contêiner de blob de armazenamento com o nome da conta de armazenamento e o nome do contêiner com metadados</span><span class="sxs-lookup"><span data-stu-id="fae58-110">Example 1: Create a Storage blob container with Storage account name and container name, with metadata</span></span>
```
PS C:\>New-AzureRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -Metadata @{tag0="value0";tag1="value1";tag2="value2"} 
```

<span data-ttu-id="fae58-111">Esse comando cria um contêiner de blob de armazenamento com o nome da conta de armazenamento e o nome do contêiner, com metadados.</span><span class="sxs-lookup"><span data-stu-id="fae58-111">This command creates a Storage blob container with Storage account name and container name, with metadata.</span></span>

### <span data-ttu-id="fae58-112">Exemplo 2: criar um contêiner de blob de armazenamento com o objeto da conta de armazenamento e o nome do contêiner com acesso público como blob</span><span class="sxs-lookup"><span data-stu-id="fae58-112">Example 2: Create a Storage blob container with Storage account object and container name, with public access as Blob</span></span>
```
PS C:\>$accountObject = Get-AzureRmStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>New-AzureRmStorageContainer -StorageAccount $accountObject -ContainerName "myContainer" -PublicAccess Blob
```

<span data-ttu-id="fae58-113">Esse comando cria um contêiner de blob de armazenamento com o objeto da conta de armazenamento e o nome do contêiner com acesso público como BLOB.</span><span class="sxs-lookup"><span data-stu-id="fae58-113">This command creates a Storage blob container with Storage account object and container name, with public access as Blob.</span></span>

## <span data-ttu-id="fae58-114">OS</span><span class="sxs-lookup"><span data-stu-id="fae58-114">PARAMETERS</span></span>

### <span data-ttu-id="fae58-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fae58-115">-DefaultProfile</span></span>
<span data-ttu-id="fae58-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fae58-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fae58-117">-Metadados</span><span class="sxs-lookup"><span data-stu-id="fae58-117">-Metadata</span></span>
<span data-ttu-id="fae58-118">Metadados do contêiner</span><span class="sxs-lookup"><span data-stu-id="fae58-118">Container Metadata</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fae58-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="fae58-119">-Name</span></span>
<span data-ttu-id="fae58-120">Nome do contêiner</span><span class="sxs-lookup"><span data-stu-id="fae58-120">Container Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, ContainerName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fae58-121">-PublicAccess</span><span class="sxs-lookup"><span data-stu-id="fae58-121">-PublicAccess</span></span>
<span data-ttu-id="fae58-122">PublicAccess de contêiner</span><span class="sxs-lookup"><span data-stu-id="fae58-122">Container PublicAccess</span></span>

```yaml
Type: PSPublicAccess
Parameter Sets: (All)
Aliases: 
Accepted values: Container, Blob

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fae58-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fae58-123">-ResourceGroupName</span></span>
<span data-ttu-id="fae58-124">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="fae58-124">Resource Group Name.</span></span>

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

### <span data-ttu-id="fae58-125">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="fae58-125">-StorageAccount</span></span>
<span data-ttu-id="fae58-126">Objeto da conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="fae58-126">Storage account object</span></span>

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

### <span data-ttu-id="fae58-127">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="fae58-127">-StorageAccountName</span></span>
<span data-ttu-id="fae58-128">Nome da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="fae58-128">Storage Account Name.</span></span>

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

### <span data-ttu-id="fae58-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="fae58-129">-Confirm</span></span>
<span data-ttu-id="fae58-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fae58-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fae58-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fae58-131">-WhatIf</span></span>
<span data-ttu-id="fae58-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="fae58-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fae58-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="fae58-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fae58-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fae58-134">CommonParameters</span></span>
<span data-ttu-id="fae58-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fae58-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fae58-136">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fae58-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fae58-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fae58-137">INPUTS</span></span>

### <span data-ttu-id="fae58-138">System. String</span><span class="sxs-lookup"><span data-stu-id="fae58-138">System.String</span></span>

## <span data-ttu-id="fae58-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fae58-139">OUTPUTS</span></span>

### <span data-ttu-id="fae58-140">Microsoft. Azure. Commands. Management. Storage. Models. PSContainer</span><span class="sxs-lookup"><span data-stu-id="fae58-140">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="fae58-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fae58-141">NOTES</span></span>

## <span data-ttu-id="fae58-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fae58-142">RELATED LINKS</span></span>


---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/get-azurermstoragecontainerimmutabilitypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageContainerImmutabilityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageContainerImmutabilityPolicy.md
ms.openlocfilehash: cff5f387b6729f51634ee0466b099e1df8314589
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93439991"
---
# <span data-ttu-id="7f013-101">Get-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="7f013-101">Get-AzureRmStorageContainerImmutabilityPolicy</span></span>

## <span data-ttu-id="7f013-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7f013-102">SYNOPSIS</span></span>
<span data-ttu-id="7f013-103">Obtém ImmutabilityPolicy de um contêiner de blob de armazenamento</span><span class="sxs-lookup"><span data-stu-id="7f013-103">Gets ImmutabilityPolicy of a Storage blob containers</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7f013-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7f013-104">SYNTAX</span></span>

### <span data-ttu-id="7f013-105">AccountName (padrão)</span><span class="sxs-lookup"><span data-stu-id="7f013-105">AccountName (Default)</span></span>
```
Get-AzureRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-ContainerName] <String> [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7f013-106">Accountobject</span><span class="sxs-lookup"><span data-stu-id="7f013-106">AccountObject</span></span>
```
Get-AzureRmStorageContainerImmutabilityPolicy [-ContainerName] <String> -StorageAccount <PSStorageAccount>
 [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7f013-107">Idcontêiner</span><span class="sxs-lookup"><span data-stu-id="7f013-107">ContainerObject</span></span>
```
Get-AzureRmStorageContainerImmutabilityPolicy -Container <PSContainer> [-Etag <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7f013-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7f013-108">DESCRIPTION</span></span>
<span data-ttu-id="7f013-109">O cmdlet **Get-AzureRmStorageContainerImmutabilityPolicy** tem ImmutabilityPolicy de um contêiner de blob de armazenamento</span><span class="sxs-lookup"><span data-stu-id="7f013-109">The **Get-AzureRmStorageContainerImmutabilityPolicy** cmdlet gets ImmutabilityPolicy of a Storage blob containers</span></span>

## <span data-ttu-id="7f013-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7f013-110">EXAMPLES</span></span>

### <span data-ttu-id="7f013-111">Exemplo 1: obter ImmutabilityPolicy de um contêiner de blob de armazenamento com nome da conta de armazenamento e nome do contêiner</span><span class="sxs-lookup"><span data-stu-id="7f013-111">Example 1: Get ImmutabilityPolicy of a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Get-AzureRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer"
```

<span data-ttu-id="7f013-112">Esse comando obtém ImmutabilityPolicy de um contêiner de blob de armazenamento com o nome da conta de armazenamento e o nome do contêiner.</span><span class="sxs-lookup"><span data-stu-id="7f013-112">This command gets ImmutabilityPolicy of a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="7f013-113">Exemplo 2: obter ImmutabilityPolicy de um contêiner de blob de armazenamento com o objeto da conta de armazenamento e o nome do contêiner</span><span class="sxs-lookup"><span data-stu-id="7f013-113">Example 2: Get ImmutabilityPolicy of a Storage blob container with Storage account object and container name</span></span>
```
PS C:\>$accountObject = Get-AzureRmStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Get-AzureRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer"
```

<span data-ttu-id="7f013-114">Esse comando obtém ImmutabilityPolicy de um contêiner de blob de armazenamento com objeto da conta de armazenamento e nome do contêiner.</span><span class="sxs-lookup"><span data-stu-id="7f013-114">This command gets ImmutabilityPolicy of a Storage blob containers with Storage account object and container name.</span></span>

### <span data-ttu-id="7f013-115">Exemplo 3: obter ImmutabilityPolicy de um contêiner de blob de armazenamento com objeto contêiner de armazenamento</span><span class="sxs-lookup"><span data-stu-id="7f013-115">Example 3: Get ImmutabilityPolicy of a Storage blob container with Storage container object</span></span>
```
PS C:\>$containerObject = Get-AzureRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -Name "myContainer"
PS C:\>Get-AzureRmStorageContainerImmutabilityPolicy -Container $containerObject 
```

<span data-ttu-id="7f013-116">Esse comando obtém ImmutabilityPolicy de um contêiner de blob de armazenamento com objeto de contêiner de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="7f013-116">This command gets ImmutabilityPolicy of a Storage blob container with Storage container object.</span></span>

## <span data-ttu-id="7f013-117">OS</span><span class="sxs-lookup"><span data-stu-id="7f013-117">PARAMETERS</span></span>

### <span data-ttu-id="7f013-118">-Contêiner</span><span class="sxs-lookup"><span data-stu-id="7f013-118">-Container</span></span>
<span data-ttu-id="7f013-119">Objeto contêiner de armazenamento</span><span class="sxs-lookup"><span data-stu-id="7f013-119">Storage container object</span></span>

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

### <span data-ttu-id="7f013-120">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="7f013-120">-ContainerName</span></span>
<span data-ttu-id="7f013-121">Nome do contêiner</span><span class="sxs-lookup"><span data-stu-id="7f013-121">Container Name</span></span>

```yaml
Type: String
Parameter Sets: AccountName, AccountObject
Aliases: N

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7f013-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f013-122">-DefaultProfile</span></span>
<span data-ttu-id="7f013-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7f013-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7f013-124">-ETag</span><span class="sxs-lookup"><span data-stu-id="7f013-124">-Etag</span></span>
<span data-ttu-id="7f013-125">ETag da política de imutabilidade.</span><span class="sxs-lookup"><span data-stu-id="7f013-125">Immutability policy etag.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: IfMatch

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f013-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f013-126">-ResourceGroupName</span></span>
<span data-ttu-id="7f013-127">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="7f013-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="7f013-128">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="7f013-128">-StorageAccount</span></span>
<span data-ttu-id="7f013-129">Objeto da conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="7f013-129">Storage account object</span></span>

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

### <span data-ttu-id="7f013-130">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="7f013-130">-StorageAccountName</span></span>
<span data-ttu-id="7f013-131">Nome da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="7f013-131">Storage Account Name.</span></span>

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

### <span data-ttu-id="7f013-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f013-132">CommonParameters</span></span>
<span data-ttu-id="7f013-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f013-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f013-134">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f013-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f013-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7f013-135">INPUTS</span></span>

### <span data-ttu-id="7f013-136">System. String</span><span class="sxs-lookup"><span data-stu-id="7f013-136">System.String</span></span>

## <span data-ttu-id="7f013-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7f013-137">OUTPUTS</span></span>

### <span data-ttu-id="7f013-138">Microsoft. Azure. Commands. Management. Storage. Models. PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="7f013-138">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="7f013-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7f013-139">NOTES</span></span>

## <span data-ttu-id="7f013-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7f013-140">RELATED LINKS</span></span>


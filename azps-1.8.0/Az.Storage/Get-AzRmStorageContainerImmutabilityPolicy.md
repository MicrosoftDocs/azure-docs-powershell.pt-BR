---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azrmstoragecontainerimmutabilitypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzRmStorageContainerImmutabilityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzRmStorageContainerImmutabilityPolicy.md
ms.openlocfilehash: 2b324d1b038a6ab97e4e68303bd98570fe0704ef
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93598687"
---
# <span data-ttu-id="62086-101">Get-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="62086-101">Get-AzRmStorageContainerImmutabilityPolicy</span></span>

## <span data-ttu-id="62086-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="62086-102">SYNOPSIS</span></span>
<span data-ttu-id="62086-103">Obtém ImmutabilityPolicy de um contêiner de blob de armazenamento</span><span class="sxs-lookup"><span data-stu-id="62086-103">Gets ImmutabilityPolicy of a Storage blob containers</span></span>

## <span data-ttu-id="62086-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="62086-104">SYNTAX</span></span>

### <span data-ttu-id="62086-105">AccountName (padrão)</span><span class="sxs-lookup"><span data-stu-id="62086-105">AccountName (Default)</span></span>
```
Get-AzRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -ContainerName <String> [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="62086-106">Accountobject</span><span class="sxs-lookup"><span data-stu-id="62086-106">AccountObject</span></span>
```
Get-AzRmStorageContainerImmutabilityPolicy -ContainerName <String> -StorageAccount <PSStorageAccount>
 [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="62086-107">Idcontêiner</span><span class="sxs-lookup"><span data-stu-id="62086-107">ContainerObject</span></span>
```
Get-AzRmStorageContainerImmutabilityPolicy -Container <PSContainer> [-Etag <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="62086-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="62086-108">DESCRIPTION</span></span>
<span data-ttu-id="62086-109">O cmdlet **Get-AzRmStorageContainerImmutabilityPolicy** tem ImmutabilityPolicy de um contêiner de blob de armazenamento</span><span class="sxs-lookup"><span data-stu-id="62086-109">The **Get-AzRmStorageContainerImmutabilityPolicy** cmdlet gets ImmutabilityPolicy of a Storage blob containers</span></span>

## <span data-ttu-id="62086-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="62086-110">EXAMPLES</span></span>

### <span data-ttu-id="62086-111">Exemplo 1: obter ImmutabilityPolicy de um contêiner de blob de armazenamento com nome da conta de armazenamento e nome do contêiner</span><span class="sxs-lookup"><span data-stu-id="62086-111">Example 1: Get ImmutabilityPolicy of a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Get-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer"
```

<span data-ttu-id="62086-112">Esse comando obtém ImmutabilityPolicy de um contêiner de blob de armazenamento com o nome da conta de armazenamento e o nome do contêiner.</span><span class="sxs-lookup"><span data-stu-id="62086-112">This command gets ImmutabilityPolicy of a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="62086-113">Exemplo 2: obter ImmutabilityPolicy de um contêiner de blob de armazenamento com o objeto da conta de armazenamento e o nome do contêiner</span><span class="sxs-lookup"><span data-stu-id="62086-113">Example 2: Get ImmutabilityPolicy of a Storage blob container with Storage account object and container name</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Get-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer"
```

<span data-ttu-id="62086-114">Esse comando obtém ImmutabilityPolicy de um contêiner de blob de armazenamento com objeto da conta de armazenamento e nome do contêiner.</span><span class="sxs-lookup"><span data-stu-id="62086-114">This command gets ImmutabilityPolicy of a Storage blob containers with Storage account object and container name.</span></span>

### <span data-ttu-id="62086-115">Exemplo 3: obter ImmutabilityPolicy de um contêiner de blob de armazenamento com objeto contêiner de armazenamento</span><span class="sxs-lookup"><span data-stu-id="62086-115">Example 3: Get ImmutabilityPolicy of a Storage blob container with Storage container object</span></span>
```
PS C:\>$containerObject = Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -Name "myContainer"
PS C:\>Get-AzRmStorageContainerImmutabilityPolicy -Container $containerObject
```

<span data-ttu-id="62086-116">Esse comando obtém ImmutabilityPolicy de um contêiner de blob de armazenamento com objeto de contêiner de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="62086-116">This command gets ImmutabilityPolicy of a Storage blob container with Storage container object.</span></span>

## <span data-ttu-id="62086-117">OS</span><span class="sxs-lookup"><span data-stu-id="62086-117">PARAMETERS</span></span>

### <span data-ttu-id="62086-118">-Contêiner</span><span class="sxs-lookup"><span data-stu-id="62086-118">-Container</span></span>
<span data-ttu-id="62086-119">Objeto contêiner de armazenamento</span><span class="sxs-lookup"><span data-stu-id="62086-119">Storage container object</span></span>

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

### <span data-ttu-id="62086-120">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="62086-120">-ContainerName</span></span>
<span data-ttu-id="62086-121">Nome do contêiner</span><span class="sxs-lookup"><span data-stu-id="62086-121">Container Name</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountObject
Aliases: N

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="62086-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62086-122">-DefaultProfile</span></span>
<span data-ttu-id="62086-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="62086-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="62086-124">-ETag</span><span class="sxs-lookup"><span data-stu-id="62086-124">-Etag</span></span>
<span data-ttu-id="62086-125">ETag da política de imutabilidade.</span><span class="sxs-lookup"><span data-stu-id="62086-125">Immutability policy etag.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IfMatch

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62086-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62086-126">-ResourceGroupName</span></span>
<span data-ttu-id="62086-127">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="62086-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="62086-128">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="62086-128">-StorageAccount</span></span>
<span data-ttu-id="62086-129">Objeto da conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="62086-129">Storage account object</span></span>

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

### <span data-ttu-id="62086-130">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="62086-130">-StorageAccountName</span></span>
<span data-ttu-id="62086-131">Nome da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="62086-131">Storage Account Name.</span></span>

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

### <span data-ttu-id="62086-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62086-132">CommonParameters</span></span>
<span data-ttu-id="62086-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62086-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62086-134">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="62086-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62086-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="62086-135">INPUTS</span></span>

### <span data-ttu-id="62086-136">System. String</span><span class="sxs-lookup"><span data-stu-id="62086-136">System.String</span></span>

### <span data-ttu-id="62086-137">Microsoft. Azure. Commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="62086-137">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="62086-138">Microsoft. Azure. Commands. Management. Storage. Models. PSContainer</span><span class="sxs-lookup"><span data-stu-id="62086-138">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="62086-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="62086-139">OUTPUTS</span></span>

### <span data-ttu-id="62086-140">Microsoft. Azure. Commands. Management. Storage. Models. PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="62086-140">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="62086-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="62086-141">NOTES</span></span>

## <span data-ttu-id="62086-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="62086-142">RELATED LINKS</span></span>

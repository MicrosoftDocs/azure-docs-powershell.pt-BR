---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/get-azrmstoragecontainerimmutabilitypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzRmStorageContainerImmutabilityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzRmStorageContainerImmutabilityPolicy.md
ms.openlocfilehash: c1e68d77df44688961f867d473a9dfce1205c2dd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892010"
---
# <span data-ttu-id="8fd1e-101">Get-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="8fd1e-101">Get-AzRmStorageContainerImmutabilityPolicy</span></span>

## <span data-ttu-id="8fd1e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8fd1e-102">SYNOPSIS</span></span>
<span data-ttu-id="8fd1e-103">Obtém ImmutabilityPolicy de um contêiner de blob de armazenamento</span><span class="sxs-lookup"><span data-stu-id="8fd1e-103">Gets ImmutabilityPolicy of a Storage blob containers</span></span>

## <span data-ttu-id="8fd1e-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="8fd1e-104">SYNTAX</span></span>

### <span data-ttu-id="8fd1e-105">AccountName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="8fd1e-105">AccountName (Default)</span></span>
```
Get-AzRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -ContainerName <String> [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8fd1e-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="8fd1e-106">AccountObject</span></span>
```
Get-AzRmStorageContainerImmutabilityPolicy -ContainerName <String> -StorageAccount <PSStorageAccount>
 [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8fd1e-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="8fd1e-107">ContainerObject</span></span>
```
Get-AzRmStorageContainerImmutabilityPolicy -Container <PSContainer> [-Etag <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8fd1e-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="8fd1e-108">DESCRIPTION</span></span>
<span data-ttu-id="8fd1e-109">O cmdlet **Get-AzRmStorageContainerImmutabilityPolicy** obtém ImmutabilityPolicy de um contêiner de blob de armazenamento</span><span class="sxs-lookup"><span data-stu-id="8fd1e-109">The **Get-AzRmStorageContainerImmutabilityPolicy** cmdlet gets ImmutabilityPolicy of a Storage blob containers</span></span>

## <span data-ttu-id="8fd1e-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8fd1e-110">EXAMPLES</span></span>

### <span data-ttu-id="8fd1e-111">Exemplo 1: Get ImmutabilityPolicy of a Storage blob container with Storage account name and container name</span><span class="sxs-lookup"><span data-stu-id="8fd1e-111">Example 1: Get ImmutabilityPolicy of a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Get-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer"
```

<span data-ttu-id="8fd1e-112">Este comando obtém ImmutabilityPolicy de um contêiner de blob de armazenamento com o nome da conta de armazenamento e o nome do contêiner.</span><span class="sxs-lookup"><span data-stu-id="8fd1e-112">This command gets ImmutabilityPolicy of a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="8fd1e-113">Exemplo 2: Get ImmutabilityPolicy of a Storage blob container with Storage account object and container name</span><span class="sxs-lookup"><span data-stu-id="8fd1e-113">Example 2: Get ImmutabilityPolicy of a Storage blob container with Storage account object and container name</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Get-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer"
```

<span data-ttu-id="8fd1e-114">Este comando obtém ImmutabilityPolicy de um armazenamento de contêineres blob com o objeto de conta de armazenamento e o nome do contêiner.</span><span class="sxs-lookup"><span data-stu-id="8fd1e-114">This command gets ImmutabilityPolicy of a Storage blob containers with Storage account object and container name.</span></span>

### <span data-ttu-id="8fd1e-115">Exemplo 3: Get ImmutabilityPolicy of a Storage blob container with Storage container object</span><span class="sxs-lookup"><span data-stu-id="8fd1e-115">Example 3: Get ImmutabilityPolicy of a Storage blob container with Storage container object</span></span>
```
PS C:\>$containerObject = Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -Name "myContainer"
PS C:\>Get-AzRmStorageContainerImmutabilityPolicy -Container $containerObject
```

<span data-ttu-id="8fd1e-116">Este comando obtém ImmutabilityPolicy de um contêiner de blob de armazenamento com objeto de contêiner de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="8fd1e-116">This command gets ImmutabilityPolicy of a Storage blob container with Storage container object.</span></span>

## <span data-ttu-id="8fd1e-117">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="8fd1e-117">PARAMETERS</span></span>

### <span data-ttu-id="8fd1e-118">-Container</span><span class="sxs-lookup"><span data-stu-id="8fd1e-118">-Container</span></span>
<span data-ttu-id="8fd1e-119">Objeto contêiner de armazenamento</span><span class="sxs-lookup"><span data-stu-id="8fd1e-119">Storage container object</span></span>

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

### <span data-ttu-id="8fd1e-120">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="8fd1e-120">-ContainerName</span></span>
<span data-ttu-id="8fd1e-121">Nome do contêiner</span><span class="sxs-lookup"><span data-stu-id="8fd1e-121">Container Name</span></span>

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

### <span data-ttu-id="8fd1e-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8fd1e-122">-DefaultProfile</span></span>
<span data-ttu-id="8fd1e-123">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="8fd1e-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8fd1e-124">-Etag</span><span class="sxs-lookup"><span data-stu-id="8fd1e-124">-Etag</span></span>
<span data-ttu-id="8fd1e-125">Etag de política de imutabilidade.</span><span class="sxs-lookup"><span data-stu-id="8fd1e-125">Immutability policy etag.</span></span>

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

### <span data-ttu-id="8fd1e-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8fd1e-126">-ResourceGroupName</span></span>
<span data-ttu-id="8fd1e-127">Nome do Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="8fd1e-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="8fd1e-128">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="8fd1e-128">-StorageAccount</span></span>
<span data-ttu-id="8fd1e-129">Objeto de conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="8fd1e-129">Storage account object</span></span>

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

### <span data-ttu-id="8fd1e-130">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="8fd1e-130">-StorageAccountName</span></span>
<span data-ttu-id="8fd1e-131">Nome da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="8fd1e-131">Storage Account Name.</span></span>

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

### <span data-ttu-id="8fd1e-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8fd1e-132">CommonParameters</span></span>
<span data-ttu-id="8fd1e-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8fd1e-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8fd1e-134">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8fd1e-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8fd1e-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8fd1e-135">INPUTS</span></span>

### <span data-ttu-id="8fd1e-136">System.String</span><span class="sxs-lookup"><span data-stu-id="8fd1e-136">System.String</span></span>

### <span data-ttu-id="8fd1e-137">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8fd1e-137">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="8fd1e-138">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span><span class="sxs-lookup"><span data-stu-id="8fd1e-138">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="8fd1e-139">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="8fd1e-139">OUTPUTS</span></span>

### <span data-ttu-id="8fd1e-140">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="8fd1e-140">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="8fd1e-141">NOTES</span><span class="sxs-lookup"><span data-stu-id="8fd1e-141">NOTES</span></span>

## <span data-ttu-id="8fd1e-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8fd1e-142">RELATED LINKS</span></span>

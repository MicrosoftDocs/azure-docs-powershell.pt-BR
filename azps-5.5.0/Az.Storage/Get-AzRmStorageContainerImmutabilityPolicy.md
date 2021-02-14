---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azrmstoragecontainerimmutabilitypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzRmStorageContainerImmutabilityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzRmStorageContainerImmutabilityPolicy.md
ms.openlocfilehash: 2a1dee58ba741e5bd1c1122b704c5d62666338f2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111280"
---
# <span data-ttu-id="e0237-101">Get-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="e0237-101">Get-AzRmStorageContainerImmutabilityPolicy</span></span>

## <span data-ttu-id="e0237-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e0237-102">SYNOPSIS</span></span>
<span data-ttu-id="e0237-103">Obtém ImmutabilityPolicy de contêineres de blob de armazenamento</span><span class="sxs-lookup"><span data-stu-id="e0237-103">Gets ImmutabilityPolicy of a Storage blob containers</span></span>

## <span data-ttu-id="e0237-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e0237-104">SYNTAX</span></span>

### <span data-ttu-id="e0237-105">Nomeda Conta (Padrão)</span><span class="sxs-lookup"><span data-stu-id="e0237-105">AccountName (Default)</span></span>
```
Get-AzRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -ContainerName <String> [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e0237-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="e0237-106">AccountObject</span></span>
```
Get-AzRmStorageContainerImmutabilityPolicy -ContainerName <String> -StorageAccount <PSStorageAccount>
 [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e0237-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="e0237-107">ContainerObject</span></span>
```
Get-AzRmStorageContainerImmutabilityPolicy -Container <PSContainer> [-Etag <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e0237-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="e0237-108">DESCRIPTION</span></span>
<span data-ttu-id="e0237-109">O cmdlet **Get-AzRmStorageContainerImmutabilityPolicy** obtém ImmutabilityPolicy de contêineres de blob de armazenamento</span><span class="sxs-lookup"><span data-stu-id="e0237-109">The **Get-AzRmStorageContainerImmutabilityPolicy** cmdlet gets ImmutabilityPolicy of a Storage blob containers</span></span>

## <span data-ttu-id="e0237-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="e0237-110">EXAMPLES</span></span>

### <span data-ttu-id="e0237-111">Exemplo 1: Obter ImmutabilidadePolicy de um contêiner de blob armazenamento com o nome da conta de armazenamento e o nome do contêiner</span><span class="sxs-lookup"><span data-stu-id="e0237-111">Example 1: Get ImmutabilityPolicy of a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Get-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer"
```

<span data-ttu-id="e0237-112">Este comando obtém ImmutabilityPolicy de um contêiner de blob armazenamento com o nome da conta de armazenamento e o nome do contêiner.</span><span class="sxs-lookup"><span data-stu-id="e0237-112">This command gets ImmutabilityPolicy of a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="e0237-113">Exemplo 2: Obter ImmutabilidadePolicy de um contêiner de blob armazenamento com o objeto de conta de armazenamento e o nome do contêiner</span><span class="sxs-lookup"><span data-stu-id="e0237-113">Example 2: Get ImmutabilityPolicy of a Storage blob container with Storage account object and container name</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Get-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer"
```

<span data-ttu-id="e0237-114">Este comando obtém ImmutabilityPolicy de um contêiner de blob armazenamento com o objeto de conta de armazenamento e o nome do contêiner.</span><span class="sxs-lookup"><span data-stu-id="e0237-114">This command gets ImmutabilityPolicy of a Storage blob containers with Storage account object and container name.</span></span>

### <span data-ttu-id="e0237-115">Exemplo 3: Obter ImmutabilidadePolicy de um contêiner de blob armazenamento com objeto de contêiner de armazenamento</span><span class="sxs-lookup"><span data-stu-id="e0237-115">Example 3: Get ImmutabilityPolicy of a Storage blob container with Storage container object</span></span>
```
PS C:\>$containerObject = Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -Name "myContainer"
PS C:\>Get-AzRmStorageContainerImmutabilityPolicy -Container $containerObject
```

<span data-ttu-id="e0237-116">Este comando obtém ImmutabilityPolicy de um contêiner de blob armazenamento com objeto de contêiner de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="e0237-116">This command gets ImmutabilityPolicy of a Storage blob container with Storage container object.</span></span>

## <span data-ttu-id="e0237-117">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e0237-117">PARAMETERS</span></span>

### <span data-ttu-id="e0237-118">-Contêiner</span><span class="sxs-lookup"><span data-stu-id="e0237-118">-Container</span></span>
<span data-ttu-id="e0237-119">Objeto de contêiner de armazenamento</span><span class="sxs-lookup"><span data-stu-id="e0237-119">Storage container object</span></span>

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

### <span data-ttu-id="e0237-120">-Nomedo Contêiner</span><span class="sxs-lookup"><span data-stu-id="e0237-120">-ContainerName</span></span>
<span data-ttu-id="e0237-121">Nome do Contêiner</span><span class="sxs-lookup"><span data-stu-id="e0237-121">Container Name</span></span>

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

### <span data-ttu-id="e0237-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0237-122">-DefaultProfile</span></span>
<span data-ttu-id="e0237-123">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="e0237-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e0237-124">-Etag</span><span class="sxs-lookup"><span data-stu-id="e0237-124">-Etag</span></span>
<span data-ttu-id="e0237-125">Étag de política de imutabilidade.</span><span class="sxs-lookup"><span data-stu-id="e0237-125">Immutability policy etag.</span></span>

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

### <span data-ttu-id="e0237-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0237-126">-ResourceGroupName</span></span>
<span data-ttu-id="e0237-127">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e0237-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="e0237-128">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="e0237-128">-StorageAccount</span></span>
<span data-ttu-id="e0237-129">Objeto de conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="e0237-129">Storage account object</span></span>

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

### <span data-ttu-id="e0237-130">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="e0237-130">-StorageAccountName</span></span>
<span data-ttu-id="e0237-131">Nome da Conta de Armazenamento.</span><span class="sxs-lookup"><span data-stu-id="e0237-131">Storage Account Name.</span></span>

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

### <span data-ttu-id="e0237-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0237-132">CommonParameters</span></span>
<span data-ttu-id="e0237-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0237-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0237-134">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e0237-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0237-135">Entradas</span><span class="sxs-lookup"><span data-stu-id="e0237-135">INPUTS</span></span>

### <span data-ttu-id="e0237-136">System.String</span><span class="sxs-lookup"><span data-stu-id="e0237-136">System.String</span></span>

### <span data-ttu-id="e0237-137">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e0237-137">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="e0237-138">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span><span class="sxs-lookup"><span data-stu-id="e0237-138">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="e0237-139">Saídas</span><span class="sxs-lookup"><span data-stu-id="e0237-139">OUTPUTS</span></span>

### <span data-ttu-id="e0237-140">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="e0237-140">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="e0237-141">Notas</span><span class="sxs-lookup"><span data-stu-id="e0237-141">NOTES</span></span>

## <span data-ttu-id="e0237-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e0237-142">RELATED LINKS</span></span>

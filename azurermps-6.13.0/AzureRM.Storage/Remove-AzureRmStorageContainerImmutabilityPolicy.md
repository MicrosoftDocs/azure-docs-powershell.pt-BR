---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/remove-azurermstoragecontainerimmutabilitypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Remove-AzureRmStorageContainerImmutabilityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Remove-AzureRmStorageContainerImmutabilityPolicy.md
ms.openlocfilehash: 74963ef36a33bed6145d315f5792aa776a36bc7d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431279"
---
# <span data-ttu-id="002f7-101">Remove-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="002f7-101">Remove-AzureRmStorageContainerImmutabilityPolicy</span></span>

## <span data-ttu-id="002f7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="002f7-102">SYNOPSIS</span></span>
<span data-ttu-id="002f7-103">Remove ImmutabilityPolicy de um contêiner de blob de armazenamento</span><span class="sxs-lookup"><span data-stu-id="002f7-103">Removes ImmutabilityPolicy of a Storage blob containers</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="002f7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="002f7-104">SYNTAX</span></span>

### <span data-ttu-id="002f7-105">AccountName (padrão)</span><span class="sxs-lookup"><span data-stu-id="002f7-105">AccountName (Default)</span></span>
```
Remove-AzureRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-ContainerName] <String> [-Etag] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="002f7-106">Accountobject</span><span class="sxs-lookup"><span data-stu-id="002f7-106">AccountObject</span></span>
```
Remove-AzureRmStorageContainerImmutabilityPolicy [-ContainerName] <String> -StorageAccount <PSStorageAccount>
 [-Etag] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="002f7-107">Idcontêiner</span><span class="sxs-lookup"><span data-stu-id="002f7-107">ContainerObject</span></span>
```
Remove-AzureRmStorageContainerImmutabilityPolicy -Container <PSContainer> [-Etag] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="002f7-108">ImmutabilityPolicyObject</span><span class="sxs-lookup"><span data-stu-id="002f7-108">ImmutabilityPolicyObject</span></span>
```
Remove-AzureRmStorageContainerImmutabilityPolicy -InputObject <PSImmutabilityPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="002f7-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="002f7-109">DESCRIPTION</span></span>
<span data-ttu-id="002f7-110">O cmdlet **Remove-AzureRmStorageContainerImmutabilityPolicy** remove ImmutabilityPolicy de contêineres de blob de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="002f7-110">The **Remove-AzureRmStorageContainerImmutabilityPolicy** cmdlet removes ImmutabilityPolicy of a Storage blob containers.</span></span>

## <span data-ttu-id="002f7-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="002f7-111">EXAMPLES</span></span>

### <span data-ttu-id="002f7-112">Exemplo 1: remover ImmutabilityPolicy de um contêiner de blob de armazenamento com nome da conta de armazenamento e nome do contêiner</span><span class="sxs-lookup"><span data-stu-id="002f7-112">Example 1: Remove ImmutabilityPolicy of a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>$policy = Get-AzureRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer"
PS C:\>Remove-AzureRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -Etag $policy.Etag
```

<span data-ttu-id="002f7-113">Esse comando Remove ImmutabilityPolicy de um contêiner de blob de armazenamento com nome da conta de armazenamento e nome do contêiner.</span><span class="sxs-lookup"><span data-stu-id="002f7-113">This command removes ImmutabilityPolicy of a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="002f7-114">Exemplo 2: remover o ImmutabilityPolicy de um contêiner de blob de armazenamento, com objeto da conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="002f7-114">Example 2: Remove ImmutabilityPolicy of a Storage blob container, with Storage account object</span></span>
```
PS C:\>$accountObject = Get-AzureRmStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>$policy = Get-AzureRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer"
PS C:\>Remove-AzureRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer" -Etag $policy.Etag
```

<span data-ttu-id="002f7-115">Esse comando Remove ImmutabilityPolicy de um contêiner de blob de armazenamento, com objeto da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="002f7-115">This command removes ImmutabilityPolicy of a Storage blob container, with Storage account object.</span></span> 

### <span data-ttu-id="002f7-116">Exemplo 3: remover ImmutabilityPolicyof um contêiner de blob de armazenamento, com objeto de contêiner</span><span class="sxs-lookup"><span data-stu-id="002f7-116">Example 3: Remove ImmutabilityPolicyof a Storage blob container, with container object</span></span>
```
PS C:\>$containerObject = Get-AzureRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -Name "myContainer"
PS C:\>$policy = Get-AzureRmStorageContainerImmutabilityPolicy -Container $containerObject
PS C:\>Remove-AzureRmStorageContainerImmutabilityPolicy -Container $containerObject -Etag $policy.Etag
```

<span data-ttu-id="002f7-117">Esse comando Remove ImmutabilityPolicy de um contêiner de blob de armazenamento com objeto de contêiner de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="002f7-117">This command removes ImmutabilityPolicy of a Storage blob container with Storage container object.</span></span>

### <span data-ttu-id="002f7-118">Exemplo 4: remover o ImmutabilityPolicy de um contêiner de blob de armazenamento, com objeto ImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="002f7-118">Example 4: Remove ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object</span></span>
```
PS C:\>Get-AzureRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" | Remove-AzureRmStorageContainerImmutabilityPolicy
```

<span data-ttu-id="002f7-119">Esse comando Remove ImmutabilityPolicy de um contêiner de blob de armazenamento, com objeto ImmutabilityPolicy.</span><span class="sxs-lookup"><span data-stu-id="002f7-119">This command removes ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object.</span></span>

## <span data-ttu-id="002f7-120">OS</span><span class="sxs-lookup"><span data-stu-id="002f7-120">PARAMETERS</span></span>

### <span data-ttu-id="002f7-121">-Contêiner</span><span class="sxs-lookup"><span data-stu-id="002f7-121">-Container</span></span>
<span data-ttu-id="002f7-122">Objeto contêiner de armazenamento</span><span class="sxs-lookup"><span data-stu-id="002f7-122">Storage container object</span></span>

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

### <span data-ttu-id="002f7-123">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="002f7-123">-ContainerName</span></span>
<span data-ttu-id="002f7-124">Nome do contêiner</span><span class="sxs-lookup"><span data-stu-id="002f7-124">Container Name</span></span>

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

### <span data-ttu-id="002f7-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="002f7-125">-DefaultProfile</span></span>
<span data-ttu-id="002f7-126">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="002f7-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="002f7-127">-ETag</span><span class="sxs-lookup"><span data-stu-id="002f7-127">-Etag</span></span>
<span data-ttu-id="002f7-128">ETag da política de imutabilidade.</span><span class="sxs-lookup"><span data-stu-id="002f7-128">Immutability policy etag.</span></span>

```yaml
Type: String
Parameter Sets: AccountName, AccountObject, ContainerObject
Aliases: IfMatch

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="002f7-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="002f7-129">-InputObject</span></span>
<span data-ttu-id="002f7-130">Objeto ImmutabilityPolicy para remover</span><span class="sxs-lookup"><span data-stu-id="002f7-130">ImmutabilityPolicy Object to Remove</span></span>

```yaml
Type: PSImmutabilityPolicy
Parameter Sets: ImmutabilityPolicyObject
Aliases: ImmutabilityPolicy

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="002f7-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="002f7-131">-ResourceGroupName</span></span>
<span data-ttu-id="002f7-132">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="002f7-132">Resource Group Name.</span></span>

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

### <span data-ttu-id="002f7-133">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="002f7-133">-StorageAccount</span></span>
<span data-ttu-id="002f7-134">Objeto da conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="002f7-134">Storage account object</span></span>

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

### <span data-ttu-id="002f7-135">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="002f7-135">-StorageAccountName</span></span>
<span data-ttu-id="002f7-136">Nome da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="002f7-136">Storage Account Name.</span></span>

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

### <span data-ttu-id="002f7-137">-Confirme</span><span class="sxs-lookup"><span data-stu-id="002f7-137">-Confirm</span></span>
<span data-ttu-id="002f7-138">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="002f7-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="002f7-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="002f7-139">-WhatIf</span></span>
<span data-ttu-id="002f7-140">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="002f7-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="002f7-141">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="002f7-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="002f7-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="002f7-142">CommonParameters</span></span>
<span data-ttu-id="002f7-143">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="002f7-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="002f7-144">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="002f7-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="002f7-145">SENSORES</span><span class="sxs-lookup"><span data-stu-id="002f7-145">INPUTS</span></span>

### <span data-ttu-id="002f7-146">System. String</span><span class="sxs-lookup"><span data-stu-id="002f7-146">System.String</span></span>
<span data-ttu-id="002f7-147">Microsoft. Azure. Commands. Management. Storage. Models. PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="002f7-147">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="002f7-148">EXIBE</span><span class="sxs-lookup"><span data-stu-id="002f7-148">OUTPUTS</span></span>

### <span data-ttu-id="002f7-149">Microsoft. Azure. Commands. Management. Storage. Models. PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="002f7-149">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="002f7-150">INFORMA</span><span class="sxs-lookup"><span data-stu-id="002f7-150">NOTES</span></span>

## <span data-ttu-id="002f7-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="002f7-151">RELATED LINKS</span></span>


---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azrmstoragecontainerimmutabilitypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageContainerImmutabilityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageContainerImmutabilityPolicy.md
ms.openlocfilehash: eedeeb3311373c240cd564534d3438b948c7a0f6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98427881"
---
# <span data-ttu-id="7888a-101">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="7888a-101">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

## <span data-ttu-id="7888a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7888a-102">SYNOPSIS</span></span>
<span data-ttu-id="7888a-103">Remove ImmutabilityPolicy de um contêiner de blob de armazenamento com uma política desbloqueada</span><span class="sxs-lookup"><span data-stu-id="7888a-103">Removes ImmutabilityPolicy of a Storage blob container with an unlocked policy</span></span>

## <span data-ttu-id="7888a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7888a-104">SYNTAX</span></span>

### <span data-ttu-id="7888a-105">AccountName (padrão)</span><span class="sxs-lookup"><span data-stu-id="7888a-105">AccountName (Default)</span></span>
```
Remove-AzRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -ContainerName <String> -Etag <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7888a-106">Accountobject</span><span class="sxs-lookup"><span data-stu-id="7888a-106">AccountObject</span></span>
```
Remove-AzRmStorageContainerImmutabilityPolicy -ContainerName <String> -StorageAccount <PSStorageAccount>
 -Etag <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7888a-107">Idcontêiner</span><span class="sxs-lookup"><span data-stu-id="7888a-107">ContainerObject</span></span>
```
Remove-AzRmStorageContainerImmutabilityPolicy -Container <PSContainer> -Etag <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7888a-108">ImmutabilityPolicyObject</span><span class="sxs-lookup"><span data-stu-id="7888a-108">ImmutabilityPolicyObject</span></span>
```
Remove-AzRmStorageContainerImmutabilityPolicy [-InputObject] <PSImmutabilityPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7888a-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7888a-109">DESCRIPTION</span></span>
<span data-ttu-id="7888a-110">O cmdlet **Remove-AzRmStorageContainerImmutabilityPolicy** remove ImmutabilityPolicy de um contêiner de blob de armazenamento com uma política desbloqueada.</span><span class="sxs-lookup"><span data-stu-id="7888a-110">The **Remove-AzRmStorageContainerImmutabilityPolicy** cmdlet removes ImmutabilityPolicy of a Storage blob container with an unlocked policy.</span></span>

## <span data-ttu-id="7888a-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7888a-111">EXAMPLES</span></span>

### <span data-ttu-id="7888a-112">Exemplo 1: remover ImmutabilityPolicy desbloqueado de um contêiner de blob de armazenamento com nome da conta de armazenamento e nome do contêiner</span><span class="sxs-lookup"><span data-stu-id="7888a-112">Example 1: Remove unlocked ImmutabilityPolicy of a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>$policy = Get-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer"
PS C:\>Remove-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -Etag $policy.Etag
```

<span data-ttu-id="7888a-113">Esse comando Remove ImmutabilityPolicy desbloqueado de um contêiner de blob de armazenamento com nome da conta de armazenamento e nome do contêiner.</span><span class="sxs-lookup"><span data-stu-id="7888a-113">This command removes unlocked ImmutabilityPolicy of a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="7888a-114">Exemplo 2: remover o ImmutabilityPolicy desbloqueado de um contêiner de blob de armazenamento, com objeto da conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="7888a-114">Example 2: Remove unlocked ImmutabilityPolicy of a Storage blob container, with Storage account object</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>$policy = Get-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer"
PS C:\>Remove-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer" -Etag $policy.Etag
```

<span data-ttu-id="7888a-115">Esse comando Remove ImmutabilityPolicy desbloqueado de um contêiner de blob de armazenamento, com objeto da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="7888a-115">This command removes unlocked ImmutabilityPolicy of a Storage blob container, with Storage account object.</span></span> 

### <span data-ttu-id="7888a-116">Exemplo 3: remover o ImmutabilityPolicy desbloqueado de um contêiner de blob de armazenamento, com objeto de contêiner</span><span class="sxs-lookup"><span data-stu-id="7888a-116">Example 3: Remove unlocked ImmutabilityPolicy of a Storage blob container, with container object</span></span>
```
PS C:\>$containerObject = Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -Name "myContainer"
PS C:\>$policy = Get-AzRmStorageContainerImmutabilityPolicy -Container $containerObject
PS C:\>Remove-AzRmStorageContainerImmutabilityPolicy -Container $containerObject -Etag $policy.Etag
```

<span data-ttu-id="7888a-117">Esse comando Remove ImmutabilityPolicy desbloqueado de um contêiner de blob de armazenamento com objeto de contêiner de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="7888a-117">This command removes unlocked ImmutabilityPolicy of a Storage blob container with Storage container object.</span></span>

### <span data-ttu-id="7888a-118">Exemplo 4: remover o ImmutabilityPolicy desbloqueado de um contêiner de blob de armazenamento, com objeto ImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="7888a-118">Example 4: Remove unlocked ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object</span></span>
```
PS C:\>Get-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" | Remove-AzRmStorageContainerImmutabilityPolicy
```

<span data-ttu-id="7888a-119">Esse comando Remove ImmutabilityPolicy desbloqueado de um contêiner de blob de armazenamento, com objeto ImmutabilityPolicy.</span><span class="sxs-lookup"><span data-stu-id="7888a-119">This command removes unlocked ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object.</span></span>

## <span data-ttu-id="7888a-120">OS</span><span class="sxs-lookup"><span data-stu-id="7888a-120">PARAMETERS</span></span>

### <span data-ttu-id="7888a-121">-Contêiner</span><span class="sxs-lookup"><span data-stu-id="7888a-121">-Container</span></span>
<span data-ttu-id="7888a-122">Objeto contêiner de armazenamento</span><span class="sxs-lookup"><span data-stu-id="7888a-122">Storage container object</span></span>

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

### <span data-ttu-id="7888a-123">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="7888a-123">-ContainerName</span></span>
<span data-ttu-id="7888a-124">Nome do contêiner</span><span class="sxs-lookup"><span data-stu-id="7888a-124">Container Name</span></span>

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

### <span data-ttu-id="7888a-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7888a-125">-DefaultProfile</span></span>
<span data-ttu-id="7888a-126">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7888a-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7888a-127">-ETag</span><span class="sxs-lookup"><span data-stu-id="7888a-127">-Etag</span></span>
<span data-ttu-id="7888a-128">ETag da política de imutabilidade.</span><span class="sxs-lookup"><span data-stu-id="7888a-128">Immutability policy etag.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountObject, ContainerObject
Aliases: IfMatch

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7888a-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7888a-129">-InputObject</span></span>
<span data-ttu-id="7888a-130">Objeto ImmutabilityPolicy desbloqueado para remover</span><span class="sxs-lookup"><span data-stu-id="7888a-130">Unlocked ImmutabilityPolicy Object to Remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy
Parameter Sets: ImmutabilityPolicyObject
Aliases: ImmutabilityPolicy

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7888a-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7888a-131">-ResourceGroupName</span></span>
<span data-ttu-id="7888a-132">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="7888a-132">Resource Group Name.</span></span>

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

### <span data-ttu-id="7888a-133">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="7888a-133">-StorageAccount</span></span>
<span data-ttu-id="7888a-134">Objeto da conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="7888a-134">Storage account object</span></span>

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

### <span data-ttu-id="7888a-135">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="7888a-135">-StorageAccountName</span></span>
<span data-ttu-id="7888a-136">Nome da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="7888a-136">Storage Account Name.</span></span>

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

### <span data-ttu-id="7888a-137">-Confirme</span><span class="sxs-lookup"><span data-stu-id="7888a-137">-Confirm</span></span>
<span data-ttu-id="7888a-138">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7888a-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7888a-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7888a-139">-WhatIf</span></span>
<span data-ttu-id="7888a-140">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7888a-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7888a-141">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7888a-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7888a-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7888a-142">CommonParameters</span></span>
<span data-ttu-id="7888a-143">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7888a-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7888a-144">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7888a-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7888a-145">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7888a-145">INPUTS</span></span>

### <span data-ttu-id="7888a-146">System. String</span><span class="sxs-lookup"><span data-stu-id="7888a-146">System.String</span></span>

### <span data-ttu-id="7888a-147">Microsoft. Azure. Commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7888a-147">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="7888a-148">Microsoft. Azure. Commands. Management. Storage. Models. PSContainer</span><span class="sxs-lookup"><span data-stu-id="7888a-148">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

### <span data-ttu-id="7888a-149">Microsoft. Azure. Commands. Management. Storage. Models. PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="7888a-149">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="7888a-150">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7888a-150">OUTPUTS</span></span>

### <span data-ttu-id="7888a-151">Microsoft. Azure. Commands. Management. Storage. Models. PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="7888a-151">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="7888a-152">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7888a-152">NOTES</span></span>

## <span data-ttu-id="7888a-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7888a-153">RELATED LINKS</span></span>

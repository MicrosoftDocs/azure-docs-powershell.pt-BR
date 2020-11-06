---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/lock-azurermstoragecontainerimmutabilitypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Lock-AzureRmStorageContainerImmutabilityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Lock-AzureRmStorageContainerImmutabilityPolicy.md
ms.openlocfilehash: 726dc9043c1082f97e32da46305cf81192e1806c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426278"
---
# <span data-ttu-id="1e26d-101">Lock-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="1e26d-101">Lock-AzureRmStorageContainerImmutabilityPolicy</span></span>

## <span data-ttu-id="1e26d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1e26d-102">SYNOPSIS</span></span>
<span data-ttu-id="1e26d-103">Bloqueia ImmutabilityPolicy de um contêiner de blob de armazenamento</span><span class="sxs-lookup"><span data-stu-id="1e26d-103">Locks ImmutabilityPolicy of a Storage blob containers</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1e26d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1e26d-104">SYNTAX</span></span>

### <span data-ttu-id="1e26d-105">AccountName (padrão)</span><span class="sxs-lookup"><span data-stu-id="1e26d-105">AccountName (Default)</span></span>
```
Lock-AzureRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-ContainerName] <String> [-Etag] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e26d-106">Accountobject</span><span class="sxs-lookup"><span data-stu-id="1e26d-106">AccountObject</span></span>
```
Lock-AzureRmStorageContainerImmutabilityPolicy [-ContainerName] <String> -StorageAccount <PSStorageAccount>
 [-Etag] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e26d-107">Idcontêiner</span><span class="sxs-lookup"><span data-stu-id="1e26d-107">ContainerObject</span></span>
```
Lock-AzureRmStorageContainerImmutabilityPolicy -Container <PSContainer> [-Etag] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e26d-108">ImmutabilityPolicyObject</span><span class="sxs-lookup"><span data-stu-id="1e26d-108">ImmutabilityPolicyObject</span></span>
```
Lock-AzureRmStorageContainerImmutabilityPolicy -InputObject <PSImmutabilityPolicy> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1e26d-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1e26d-109">DESCRIPTION</span></span>
<span data-ttu-id="1e26d-110">O cmdlet **Lock-AzureRmStorageContainerImmutabilityPolicy** bloqueia ImmutabilityPolicy de um contêiner de blob de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="1e26d-110">The **Lock-AzureRmStorageContainerImmutabilityPolicy** cmdlet locks ImmutabilityPolicy of a Storage blob containers.</span></span>

## <span data-ttu-id="1e26d-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1e26d-111">EXAMPLES</span></span>

### <span data-ttu-id="1e26d-112">Exemplo 1: bloquear ImmutabilityPolicy de um contêiner de blob de armazenamento com nome da conta de armazenamento e nome do contêiner</span><span class="sxs-lookup"><span data-stu-id="1e26d-112">Example 1: Lock ImmutabilityPolicy of a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>$policy = Get-AzureRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer"
PS C:\>Lock-AzureRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -Etag $policy.Etag
```

<span data-ttu-id="1e26d-113">Esse comando trava o ImmutabilityPolicy de um contêiner de blob de armazenamento com nome da conta de armazenamento e nome do contêiner.</span><span class="sxs-lookup"><span data-stu-id="1e26d-113">This command Locks ImmutabilityPolicy of a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="1e26d-114">Exemplo 2: bloquear o ImmutabilityPolicy de um contêiner de blob de armazenamento, com objeto da conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="1e26d-114">Example 2: Lock ImmutabilityPolicy of a Storage blob container, with Storage account object</span></span>
```
PS C:\>$accountObject = Get-AzureRmStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>$policy = Get-AzureRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer"
PS C:\>Lock-AzureRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer" -Etag $policy.Etag -Force
```

<span data-ttu-id="1e26d-115">Esse comando trava o ImmutabilityPolicy de um contêiner de blob de armazenamento, com objeto da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="1e26d-115">This command locks ImmutabilityPolicy of a Storage blob container, with Storage account object.</span></span> 

### <span data-ttu-id="1e26d-116">Exemplo 3: bloquear ImmutabilityPolicyof um contêiner de blob de armazenamento, com objeto de contêiner</span><span class="sxs-lookup"><span data-stu-id="1e26d-116">Example 3: Lock ImmutabilityPolicyof a Storage blob container, with container object</span></span>
```
PS C:\>$containerObject = Get-AzureRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -Name "myContainer"
PS C:\>$policy = Get-AzureRmStorageContainerImmutabilityPolicy -Container $containerObject
PS C:\>Lock-AzureRmStorageContainerImmutabilityPolicy -Container $containerObject -Etag $policy.Etag -Force
```

<span data-ttu-id="1e26d-117">Esse comando trava o ImmutabilityPolicy de um contêiner de blob de armazenamento com objeto de contêiner de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="1e26d-117">This command locks ImmutabilityPolicy of a Storage blob container with Storage container object.</span></span>

### <span data-ttu-id="1e26d-118">Exemplo 4: bloquear o ImmutabilityPolicy de um contêiner de blob de armazenamento, com objeto ImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="1e26d-118">Example 4: Lock ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object</span></span>
```
PS C:\>Get-AzureRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" | Lock-AzureRmStorageContainerImmutabilityPolicy -Force
```

<span data-ttu-id="1e26d-119">Esse comando trava o ImmutabilityPolicy de um contêiner de blob de armazenamento, com objeto ImmutabilityPolicy.</span><span class="sxs-lookup"><span data-stu-id="1e26d-119">This command locks ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object.</span></span> 

## <span data-ttu-id="1e26d-120">OS</span><span class="sxs-lookup"><span data-stu-id="1e26d-120">PARAMETERS</span></span>

### <span data-ttu-id="1e26d-121">-Contêiner</span><span class="sxs-lookup"><span data-stu-id="1e26d-121">-Container</span></span>
<span data-ttu-id="1e26d-122">Objeto contêiner de armazenamento</span><span class="sxs-lookup"><span data-stu-id="1e26d-122">Storage container object</span></span>

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

### <span data-ttu-id="1e26d-123">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="1e26d-123">-ContainerName</span></span>
<span data-ttu-id="1e26d-124">Nome do contêiner</span><span class="sxs-lookup"><span data-stu-id="1e26d-124">Container Name</span></span>

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

### <span data-ttu-id="1e26d-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e26d-125">-DefaultProfile</span></span>
<span data-ttu-id="1e26d-126">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1e26d-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1e26d-127">-ETag</span><span class="sxs-lookup"><span data-stu-id="1e26d-127">-Etag</span></span>
<span data-ttu-id="1e26d-128">ETag da política de imutabilidade.</span><span class="sxs-lookup"><span data-stu-id="1e26d-128">Immutability policy etag.</span></span>

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

### <span data-ttu-id="1e26d-129">-Force</span><span class="sxs-lookup"><span data-stu-id="1e26d-129">-Force</span></span>
<span data-ttu-id="1e26d-130">Force a remoção da ImmutabilityPolicy.</span><span class="sxs-lookup"><span data-stu-id="1e26d-130">Force to remove the ImmutabilityPolicy.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e26d-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1e26d-131">-InputObject</span></span>
<span data-ttu-id="1e26d-132">Objeto ImmutabilityPolicy para remover</span><span class="sxs-lookup"><span data-stu-id="1e26d-132">ImmutabilityPolicy Object to Remove</span></span>

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

### <span data-ttu-id="1e26d-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e26d-133">-ResourceGroupName</span></span>
<span data-ttu-id="1e26d-134">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="1e26d-134">Resource Group Name.</span></span>

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

### <span data-ttu-id="1e26d-135">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="1e26d-135">-StorageAccount</span></span>
<span data-ttu-id="1e26d-136">Objeto da conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="1e26d-136">Storage account object</span></span>

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

### <span data-ttu-id="1e26d-137">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="1e26d-137">-StorageAccountName</span></span>
<span data-ttu-id="1e26d-138">Nome da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="1e26d-138">Storage Account Name.</span></span>

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

### <span data-ttu-id="1e26d-139">-Confirme</span><span class="sxs-lookup"><span data-stu-id="1e26d-139">-Confirm</span></span>
<span data-ttu-id="1e26d-140">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1e26d-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1e26d-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e26d-141">-WhatIf</span></span>
<span data-ttu-id="1e26d-142">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1e26d-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1e26d-143">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1e26d-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1e26d-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e26d-144">CommonParameters</span></span>
<span data-ttu-id="1e26d-145">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1e26d-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e26d-146">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1e26d-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e26d-147">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1e26d-147">INPUTS</span></span>

### <span data-ttu-id="1e26d-148">System. String</span><span class="sxs-lookup"><span data-stu-id="1e26d-148">System.String</span></span>
<span data-ttu-id="1e26d-149">Microsoft. Azure. Commands. Management. Storage. Models. PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="1e26d-149">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="1e26d-150">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1e26d-150">OUTPUTS</span></span>

### <span data-ttu-id="1e26d-151">Microsoft. Azure. Commands. Management. Storage. Models. PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="1e26d-151">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="1e26d-152">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1e26d-152">NOTES</span></span>

## <span data-ttu-id="1e26d-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1e26d-153">RELATED LINKS</span></span>


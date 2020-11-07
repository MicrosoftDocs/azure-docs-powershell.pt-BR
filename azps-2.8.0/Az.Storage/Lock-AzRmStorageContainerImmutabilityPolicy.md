---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/lock-azrmstoragecontainerimmutabilitypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Lock-AzRmStorageContainerImmutabilityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Lock-AzRmStorageContainerImmutabilityPolicy.md
ms.openlocfilehash: f2c9181ab0abc6bf897a94e803caceadb587b296
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93773936"
---
# <span data-ttu-id="d3aa5-101">Lock-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="d3aa5-101">Lock-AzRmStorageContainerImmutabilityPolicy</span></span>

## <span data-ttu-id="d3aa5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d3aa5-102">SYNOPSIS</span></span>
<span data-ttu-id="d3aa5-103">Bloqueia ImmutabilityPolicy de um contêiner de blob de armazenamento</span><span class="sxs-lookup"><span data-stu-id="d3aa5-103">Locks ImmutabilityPolicy of a Storage blob containers</span></span>

## <span data-ttu-id="d3aa5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d3aa5-104">SYNTAX</span></span>

### <span data-ttu-id="d3aa5-105">AccountName (padrão)</span><span class="sxs-lookup"><span data-stu-id="d3aa5-105">AccountName (Default)</span></span>
```
Lock-AzRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -ContainerName <String> -Etag <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d3aa5-106">Accountobject</span><span class="sxs-lookup"><span data-stu-id="d3aa5-106">AccountObject</span></span>
```
Lock-AzRmStorageContainerImmutabilityPolicy -ContainerName <String> -StorageAccount <PSStorageAccount>
 -Etag <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d3aa5-107">Idcontêiner</span><span class="sxs-lookup"><span data-stu-id="d3aa5-107">ContainerObject</span></span>
```
Lock-AzRmStorageContainerImmutabilityPolicy -Container <PSContainer> -Etag <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d3aa5-108">ImmutabilityPolicyObject</span><span class="sxs-lookup"><span data-stu-id="d3aa5-108">ImmutabilityPolicyObject</span></span>
```
Lock-AzRmStorageContainerImmutabilityPolicy [-InputObject] <PSImmutabilityPolicy> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d3aa5-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d3aa5-109">DESCRIPTION</span></span>
<span data-ttu-id="d3aa5-110">O cmdlet **Lock-AzRmStorageContainerImmutabilityPolicy** bloqueia ImmutabilityPolicy de um contêiner de blob de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="d3aa5-110">The **Lock-AzRmStorageContainerImmutabilityPolicy** cmdlet locks ImmutabilityPolicy of a Storage blob containers.</span></span>

## <span data-ttu-id="d3aa5-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d3aa5-111">EXAMPLES</span></span>

### <span data-ttu-id="d3aa5-112">Exemplo 1: bloquear ImmutabilityPolicy de um contêiner de blob de armazenamento com nome da conta de armazenamento e nome do contêiner</span><span class="sxs-lookup"><span data-stu-id="d3aa5-112">Example 1: Lock ImmutabilityPolicy of a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>$policy = Get-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer"
PS C:\>Lock-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -Etag $policy.Etag
```

<span data-ttu-id="d3aa5-113">Esse comando trava o ImmutabilityPolicy de um contêiner de blob de armazenamento com nome da conta de armazenamento e nome do contêiner.</span><span class="sxs-lookup"><span data-stu-id="d3aa5-113">This command Locks ImmutabilityPolicy of a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="d3aa5-114">Exemplo 2: bloquear o ImmutabilityPolicy de um contêiner de blob de armazenamento, com objeto da conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="d3aa5-114">Example 2: Lock ImmutabilityPolicy of a Storage blob container, with Storage account object</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>$policy = Get-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer"
PS C:\>Lock-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer" -Etag $policy.Etag -Force
```

<span data-ttu-id="d3aa5-115">Esse comando trava o ImmutabilityPolicy de um contêiner de blob de armazenamento, com objeto da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="d3aa5-115">This command locks ImmutabilityPolicy of a Storage blob container, with Storage account object.</span></span> 

### <span data-ttu-id="d3aa5-116">Exemplo 3: bloquear ImmutabilityPolicyof um contêiner de blob de armazenamento, com objeto de contêiner</span><span class="sxs-lookup"><span data-stu-id="d3aa5-116">Example 3: Lock ImmutabilityPolicyof a Storage blob container, with container object</span></span>
```
PS C:\>$containerObject = Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -Name "myContainer"
PS C:\>$policy = Get-AzRmStorageContainerImmutabilityPolicy -Container $containerObject
PS C:\>Lock-AzRmStorageContainerImmutabilityPolicy -Container $containerObject -Etag $policy.Etag -Force
```

<span data-ttu-id="d3aa5-117">Esse comando trava o ImmutabilityPolicy de um contêiner de blob de armazenamento com objeto de contêiner de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="d3aa5-117">This command locks ImmutabilityPolicy of a Storage blob container with Storage container object.</span></span>

### <span data-ttu-id="d3aa5-118">Exemplo 4: bloquear o ImmutabilityPolicy de um contêiner de blob de armazenamento, com objeto ImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="d3aa5-118">Example 4: Lock ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object</span></span>
```
PS C:\>Get-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" | Lock-AzRmStorageContainerImmutabilityPolicy -Force
```

<span data-ttu-id="d3aa5-119">Esse comando trava o ImmutabilityPolicy de um contêiner de blob de armazenamento, com objeto ImmutabilityPolicy.</span><span class="sxs-lookup"><span data-stu-id="d3aa5-119">This command locks ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object.</span></span> 

## <span data-ttu-id="d3aa5-120">OS</span><span class="sxs-lookup"><span data-stu-id="d3aa5-120">PARAMETERS</span></span>

### <span data-ttu-id="d3aa5-121">-Contêiner</span><span class="sxs-lookup"><span data-stu-id="d3aa5-121">-Container</span></span>
<span data-ttu-id="d3aa5-122">Objeto contêiner de armazenamento</span><span class="sxs-lookup"><span data-stu-id="d3aa5-122">Storage container object</span></span>

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

### <span data-ttu-id="d3aa5-123">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="d3aa5-123">-ContainerName</span></span>
<span data-ttu-id="d3aa5-124">Nome do contêiner</span><span class="sxs-lookup"><span data-stu-id="d3aa5-124">Container Name</span></span>

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

### <span data-ttu-id="d3aa5-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3aa5-125">-DefaultProfile</span></span>
<span data-ttu-id="d3aa5-126">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d3aa5-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d3aa5-127">-ETag</span><span class="sxs-lookup"><span data-stu-id="d3aa5-127">-Etag</span></span>
<span data-ttu-id="d3aa5-128">ETag da política de imutabilidade.</span><span class="sxs-lookup"><span data-stu-id="d3aa5-128">Immutability policy etag.</span></span>

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

### <span data-ttu-id="d3aa5-129">-Force</span><span class="sxs-lookup"><span data-stu-id="d3aa5-129">-Force</span></span>
<span data-ttu-id="d3aa5-130">Force a remoção da ImmutabilityPolicy.</span><span class="sxs-lookup"><span data-stu-id="d3aa5-130">Force to remove the ImmutabilityPolicy.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3aa5-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d3aa5-131">-InputObject</span></span>
<span data-ttu-id="d3aa5-132">Objeto ImmutabilityPolicy para remover</span><span class="sxs-lookup"><span data-stu-id="d3aa5-132">ImmutabilityPolicy Object to Remove</span></span>

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

### <span data-ttu-id="d3aa5-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3aa5-133">-ResourceGroupName</span></span>
<span data-ttu-id="d3aa5-134">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d3aa5-134">Resource Group Name.</span></span>

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

### <span data-ttu-id="d3aa5-135">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="d3aa5-135">-StorageAccount</span></span>
<span data-ttu-id="d3aa5-136">Objeto da conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="d3aa5-136">Storage account object</span></span>

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

### <span data-ttu-id="d3aa5-137">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="d3aa5-137">-StorageAccountName</span></span>
<span data-ttu-id="d3aa5-138">Nome da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="d3aa5-138">Storage Account Name.</span></span>

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

### <span data-ttu-id="d3aa5-139">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d3aa5-139">-Confirm</span></span>
<span data-ttu-id="d3aa5-140">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d3aa5-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d3aa5-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d3aa5-141">-WhatIf</span></span>
<span data-ttu-id="d3aa5-142">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d3aa5-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d3aa5-143">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d3aa5-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d3aa5-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3aa5-144">CommonParameters</span></span>
<span data-ttu-id="d3aa5-145">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3aa5-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3aa5-146">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3aa5-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3aa5-147">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d3aa5-147">INPUTS</span></span>

### <span data-ttu-id="d3aa5-148">System. String</span><span class="sxs-lookup"><span data-stu-id="d3aa5-148">System.String</span></span>

### <span data-ttu-id="d3aa5-149">Microsoft. Azure. Commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d3aa5-149">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="d3aa5-150">Microsoft. Azure. Commands. Management. Storage. Models. PSContainer</span><span class="sxs-lookup"><span data-stu-id="d3aa5-150">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

### <span data-ttu-id="d3aa5-151">Microsoft. Azure. Commands. Management. Storage. Models. PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="d3aa5-151">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="d3aa5-152">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d3aa5-152">OUTPUTS</span></span>

### <span data-ttu-id="d3aa5-153">Microsoft. Azure. Commands. Management. Storage. Models. PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="d3aa5-153">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="d3aa5-154">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d3aa5-154">NOTES</span></span>

## <span data-ttu-id="d3aa5-155">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d3aa5-155">RELATED LINKS</span></span>

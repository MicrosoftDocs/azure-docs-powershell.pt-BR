---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/lock-azrmstoragecontainerimmutabilitypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Lock-AzRmStorageContainerImmutabilityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Lock-AzRmStorageContainerImmutabilityPolicy.md
ms.openlocfilehash: 44d0f6b9717e51aec508da76a9ef9b776891d8c1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890917"
---
# <span data-ttu-id="4326f-101">Lock-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="4326f-101">Lock-AzRmStorageContainerImmutabilityPolicy</span></span>

## <span data-ttu-id="4326f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4326f-102">SYNOPSIS</span></span>
<span data-ttu-id="4326f-103">Bloqueia ImmutabilityPolicy de um contêiner de blob de armazenamento</span><span class="sxs-lookup"><span data-stu-id="4326f-103">Locks ImmutabilityPolicy of a Storage blob containers</span></span>

## <span data-ttu-id="4326f-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="4326f-104">SYNTAX</span></span>

### <span data-ttu-id="4326f-105">AccountName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="4326f-105">AccountName (Default)</span></span>
```
Lock-AzRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -ContainerName <String> -Etag <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4326f-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="4326f-106">AccountObject</span></span>
```
Lock-AzRmStorageContainerImmutabilityPolicy -ContainerName <String> -StorageAccount <PSStorageAccount>
 -Etag <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4326f-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="4326f-107">ContainerObject</span></span>
```
Lock-AzRmStorageContainerImmutabilityPolicy -Container <PSContainer> -Etag <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4326f-108">ImmutabilityPolicyObject</span><span class="sxs-lookup"><span data-stu-id="4326f-108">ImmutabilityPolicyObject</span></span>
```
Lock-AzRmStorageContainerImmutabilityPolicy [-InputObject] <PSImmutabilityPolicy> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4326f-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="4326f-109">DESCRIPTION</span></span>
<span data-ttu-id="4326f-110">O cmdlet **Lock-AzRmStorageContainerImmutabilityPolicy** bloqueia ImmutabilityPolicy de um contêiner de blob de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="4326f-110">The **Lock-AzRmStorageContainerImmutabilityPolicy** cmdlet locks ImmutabilityPolicy of a Storage blob containers.</span></span>

## <span data-ttu-id="4326f-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4326f-111">EXAMPLES</span></span>

### <span data-ttu-id="4326f-112">Exemplo 1: Bloquear ImmutabilityPolicy de um contêiner de blob de armazenamento com o nome da conta de armazenamento e o nome do contêiner</span><span class="sxs-lookup"><span data-stu-id="4326f-112">Example 1: Lock ImmutabilityPolicy of a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>$policy = Get-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer"
PS C:\>Lock-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -Etag $policy.Etag
```

<span data-ttu-id="4326f-113">Este comando bloqueia ImmutabilityPolicy de um contêiner de blob de armazenamento com o nome da conta de armazenamento e o nome do contêiner.</span><span class="sxs-lookup"><span data-stu-id="4326f-113">This command Locks ImmutabilityPolicy of a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="4326f-114">Exemplo 2: Bloquear ImmutabilityPolicy de um contêiner de blob de armazenamento, com objeto de conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="4326f-114">Example 2: Lock ImmutabilityPolicy of a Storage blob container, with Storage account object</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>$policy = Get-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer"
PS C:\>Lock-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer" -Etag $policy.Etag -Force
```

<span data-ttu-id="4326f-115">Este comando bloqueia ImmutabilityPolicy de um contêiner de blob de armazenamento, com o objeto de conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="4326f-115">This command locks ImmutabilityPolicy of a Storage blob container, with Storage account object.</span></span> 

### <span data-ttu-id="4326f-116">Exemplo 3: Bloquear ImmutabilityPolicyof a Storage blob container, with container object</span><span class="sxs-lookup"><span data-stu-id="4326f-116">Example 3: Lock ImmutabilityPolicyof a Storage blob container, with container object</span></span>
```
PS C:\>$containerObject = Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -Name "myContainer"
PS C:\>$policy = Get-AzRmStorageContainerImmutabilityPolicy -Container $containerObject
PS C:\>Lock-AzRmStorageContainerImmutabilityPolicy -Container $containerObject -Etag $policy.Etag -Force
```

<span data-ttu-id="4326f-117">Este comando bloqueia ImmutabilityPolicy de um contêiner de blob de armazenamento com objeto de contêiner de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="4326f-117">This command locks ImmutabilityPolicy of a Storage blob container with Storage container object.</span></span>

### <span data-ttu-id="4326f-118">Exemplo 4: Bloquear ImmutabilityPolicy de um contêiner de blob de armazenamento, com objeto ImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="4326f-118">Example 4: Lock ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object</span></span>
```
PS C:\>Get-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" | Lock-AzRmStorageContainerImmutabilityPolicy -Force
```

<span data-ttu-id="4326f-119">Este comando bloqueia ImmutabilityPolicy de um contêiner de blob de armazenamento, com o objeto ImmutabilityPolicy.</span><span class="sxs-lookup"><span data-stu-id="4326f-119">This command locks ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object.</span></span> 

## <span data-ttu-id="4326f-120">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="4326f-120">PARAMETERS</span></span>

### <span data-ttu-id="4326f-121">-Container</span><span class="sxs-lookup"><span data-stu-id="4326f-121">-Container</span></span>
<span data-ttu-id="4326f-122">Objeto contêiner de armazenamento</span><span class="sxs-lookup"><span data-stu-id="4326f-122">Storage container object</span></span>

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

### <span data-ttu-id="4326f-123">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="4326f-123">-ContainerName</span></span>
<span data-ttu-id="4326f-124">Nome do contêiner</span><span class="sxs-lookup"><span data-stu-id="4326f-124">Container Name</span></span>

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

### <span data-ttu-id="4326f-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4326f-125">-DefaultProfile</span></span>
<span data-ttu-id="4326f-126">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="4326f-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4326f-127">-Etag</span><span class="sxs-lookup"><span data-stu-id="4326f-127">-Etag</span></span>
<span data-ttu-id="4326f-128">Etag de política de imutabilidade.</span><span class="sxs-lookup"><span data-stu-id="4326f-128">Immutability policy etag.</span></span>

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

### <span data-ttu-id="4326f-129">-Force</span><span class="sxs-lookup"><span data-stu-id="4326f-129">-Force</span></span>
<span data-ttu-id="4326f-130">Force a remover ImmutabilityPolicy.</span><span class="sxs-lookup"><span data-stu-id="4326f-130">Force to remove the ImmutabilityPolicy.</span></span>

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

### <span data-ttu-id="4326f-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4326f-131">-InputObject</span></span>
<span data-ttu-id="4326f-132">Objeto ImmutabilityPolicy a ser removido</span><span class="sxs-lookup"><span data-stu-id="4326f-132">ImmutabilityPolicy Object to Remove</span></span>

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

### <span data-ttu-id="4326f-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4326f-133">-ResourceGroupName</span></span>
<span data-ttu-id="4326f-134">Nome do Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="4326f-134">Resource Group Name.</span></span>

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

### <span data-ttu-id="4326f-135">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="4326f-135">-StorageAccount</span></span>
<span data-ttu-id="4326f-136">Objeto de conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="4326f-136">Storage account object</span></span>

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

### <span data-ttu-id="4326f-137">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="4326f-137">-StorageAccountName</span></span>
<span data-ttu-id="4326f-138">Nome da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="4326f-138">Storage Account Name.</span></span>

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

### <span data-ttu-id="4326f-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4326f-139">-Confirm</span></span>
<span data-ttu-id="4326f-140">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4326f-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4326f-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4326f-141">-WhatIf</span></span>
<span data-ttu-id="4326f-142">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4326f-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4326f-143">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4326f-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4326f-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4326f-144">CommonParameters</span></span>
<span data-ttu-id="4326f-145">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4326f-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4326f-146">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4326f-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4326f-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4326f-147">INPUTS</span></span>

### <span data-ttu-id="4326f-148">System.String</span><span class="sxs-lookup"><span data-stu-id="4326f-148">System.String</span></span>

### <span data-ttu-id="4326f-149">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4326f-149">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="4326f-150">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span><span class="sxs-lookup"><span data-stu-id="4326f-150">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

### <span data-ttu-id="4326f-151">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="4326f-151">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="4326f-152">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="4326f-152">OUTPUTS</span></span>

### <span data-ttu-id="4326f-153">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="4326f-153">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="4326f-154">NOTES</span><span class="sxs-lookup"><span data-stu-id="4326f-154">NOTES</span></span>

## <span data-ttu-id="4326f-155">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4326f-155">RELATED LINKS</span></span>

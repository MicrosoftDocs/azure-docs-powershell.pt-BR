---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azrmstoragecontainerimmutabilitypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageContainerImmutabilityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageContainerImmutabilityPolicy.md
ms.openlocfilehash: eedeeb3311373c240cd564534d3438b948c7a0f6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114418"
---
# <span data-ttu-id="d917b-101">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="d917b-101">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

## <span data-ttu-id="d917b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d917b-102">SYNOPSIS</span></span>
<span data-ttu-id="d917b-103">Remove ImmutabilityPolicy de um contêiner de blob armazenamento com uma política desbloqueada</span><span class="sxs-lookup"><span data-stu-id="d917b-103">Removes ImmutabilityPolicy of a Storage blob container with an unlocked policy</span></span>

## <span data-ttu-id="d917b-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d917b-104">SYNTAX</span></span>

### <span data-ttu-id="d917b-105">Nomeda Conta (Padrão)</span><span class="sxs-lookup"><span data-stu-id="d917b-105">AccountName (Default)</span></span>
```
Remove-AzRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -ContainerName <String> -Etag <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d917b-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="d917b-106">AccountObject</span></span>
```
Remove-AzRmStorageContainerImmutabilityPolicy -ContainerName <String> -StorageAccount <PSStorageAccount>
 -Etag <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d917b-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="d917b-107">ContainerObject</span></span>
```
Remove-AzRmStorageContainerImmutabilityPolicy -Container <PSContainer> -Etag <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d917b-108">ImmutabilityPolicyObject</span><span class="sxs-lookup"><span data-stu-id="d917b-108">ImmutabilityPolicyObject</span></span>
```
Remove-AzRmStorageContainerImmutabilityPolicy [-InputObject] <PSImmutabilityPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d917b-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="d917b-109">DESCRIPTION</span></span>
<span data-ttu-id="d917b-110">O cmdlet **Remove-AzRmStorageContainerImmutabilityPolicy** remove ImmutabilityPolicy de um contêiner de blob armazenamento com uma política desbloqueada.</span><span class="sxs-lookup"><span data-stu-id="d917b-110">The **Remove-AzRmStorageContainerImmutabilityPolicy** cmdlet removes ImmutabilityPolicy of a Storage blob container with an unlocked policy.</span></span>

## <span data-ttu-id="d917b-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="d917b-111">EXAMPLES</span></span>

### <span data-ttu-id="d917b-112">Exemplo 1: Remover ImmutabilityPolicy desbloqueado de um contêiner de blob armazenamento com o nome da conta de armazenamento e o nome do contêiner</span><span class="sxs-lookup"><span data-stu-id="d917b-112">Example 1: Remove unlocked ImmutabilityPolicy of a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>$policy = Get-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer"
PS C:\>Remove-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -Etag $policy.Etag
```

<span data-ttu-id="d917b-113">Este comando remove ImmutabilityPolicy desbloqueado de um contêiner de blob armazenamento com o nome da conta de armazenamento e o nome do contêiner.</span><span class="sxs-lookup"><span data-stu-id="d917b-113">This command removes unlocked ImmutabilityPolicy of a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="d917b-114">Exemplo 2: Remover ImmutabilityPolicy desbloqueado de um contêiner de blob armazenamento, com objeto de conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="d917b-114">Example 2: Remove unlocked ImmutabilityPolicy of a Storage blob container, with Storage account object</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>$policy = Get-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer"
PS C:\>Remove-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer" -Etag $policy.Etag
```

<span data-ttu-id="d917b-115">Este comando remove ImmutabilityPolicy desbloqueado de um contêiner de blob armazenamento, com objeto de conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="d917b-115">This command removes unlocked ImmutabilityPolicy of a Storage blob container, with Storage account object.</span></span> 

### <span data-ttu-id="d917b-116">Exemplo 3: Remover ImmutabilityPolicy desbloqueado de um contêiner de blob armazenamento, com objeto de contêiner</span><span class="sxs-lookup"><span data-stu-id="d917b-116">Example 3: Remove unlocked ImmutabilityPolicy of a Storage blob container, with container object</span></span>
```
PS C:\>$containerObject = Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -Name "myContainer"
PS C:\>$policy = Get-AzRmStorageContainerImmutabilityPolicy -Container $containerObject
PS C:\>Remove-AzRmStorageContainerImmutabilityPolicy -Container $containerObject -Etag $policy.Etag
```

<span data-ttu-id="d917b-117">Este comando remove ImmutabilityPolicy desbloqueado de um contêiner de blob armazenamento com objeto de contêiner de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="d917b-117">This command removes unlocked ImmutabilityPolicy of a Storage blob container with Storage container object.</span></span>

### <span data-ttu-id="d917b-118">Exemplo 4: Remover ImmutabilityPolicy desbloqueado de um contêiner de blob armazenamento, com objeto ImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="d917b-118">Example 4: Remove unlocked ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object</span></span>
```
PS C:\>Get-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" | Remove-AzRmStorageContainerImmutabilityPolicy
```

<span data-ttu-id="d917b-119">Esse comando remove ImmutabilityPolicy desbloqueado de um contêiner de blob armazenamento, com objeto ImmutabilityPolicy.</span><span class="sxs-lookup"><span data-stu-id="d917b-119">This command removes unlocked ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object.</span></span>

## <span data-ttu-id="d917b-120">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d917b-120">PARAMETERS</span></span>

### <span data-ttu-id="d917b-121">-Contêiner</span><span class="sxs-lookup"><span data-stu-id="d917b-121">-Container</span></span>
<span data-ttu-id="d917b-122">Objeto de contêiner de armazenamento</span><span class="sxs-lookup"><span data-stu-id="d917b-122">Storage container object</span></span>

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

### <span data-ttu-id="d917b-123">-Nomedo Contêiner</span><span class="sxs-lookup"><span data-stu-id="d917b-123">-ContainerName</span></span>
<span data-ttu-id="d917b-124">Nome do Contêiner</span><span class="sxs-lookup"><span data-stu-id="d917b-124">Container Name</span></span>

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

### <span data-ttu-id="d917b-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d917b-125">-DefaultProfile</span></span>
<span data-ttu-id="d917b-126">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="d917b-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d917b-127">-Etag</span><span class="sxs-lookup"><span data-stu-id="d917b-127">-Etag</span></span>
<span data-ttu-id="d917b-128">Etag de política de imutabilidade.</span><span class="sxs-lookup"><span data-stu-id="d917b-128">Immutability policy etag.</span></span>

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

### <span data-ttu-id="d917b-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d917b-129">-InputObject</span></span>
<span data-ttu-id="d917b-130">Objeto ImmutabilityPolicy desbloqueado para remover</span><span class="sxs-lookup"><span data-stu-id="d917b-130">Unlocked ImmutabilityPolicy Object to Remove</span></span>

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

### <span data-ttu-id="d917b-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d917b-131">-ResourceGroupName</span></span>
<span data-ttu-id="d917b-132">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d917b-132">Resource Group Name.</span></span>

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

### <span data-ttu-id="d917b-133">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="d917b-133">-StorageAccount</span></span>
<span data-ttu-id="d917b-134">Objeto de conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="d917b-134">Storage account object</span></span>

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

### <span data-ttu-id="d917b-135">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="d917b-135">-StorageAccountName</span></span>
<span data-ttu-id="d917b-136">Nome da Conta de Armazenamento.</span><span class="sxs-lookup"><span data-stu-id="d917b-136">Storage Account Name.</span></span>

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

### <span data-ttu-id="d917b-137">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="d917b-137">-Confirm</span></span>
<span data-ttu-id="d917b-138">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d917b-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d917b-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d917b-139">-WhatIf</span></span>
<span data-ttu-id="d917b-140">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="d917b-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d917b-141">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d917b-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d917b-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d917b-142">CommonParameters</span></span>
<span data-ttu-id="d917b-143">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d917b-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d917b-144">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d917b-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d917b-145">Entradas</span><span class="sxs-lookup"><span data-stu-id="d917b-145">INPUTS</span></span>

### <span data-ttu-id="d917b-146">System.String</span><span class="sxs-lookup"><span data-stu-id="d917b-146">System.String</span></span>

### <span data-ttu-id="d917b-147">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d917b-147">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="d917b-148">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span><span class="sxs-lookup"><span data-stu-id="d917b-148">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

### <span data-ttu-id="d917b-149">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="d917b-149">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="d917b-150">Saídas</span><span class="sxs-lookup"><span data-stu-id="d917b-150">OUTPUTS</span></span>

### <span data-ttu-id="d917b-151">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="d917b-151">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="d917b-152">Notas</span><span class="sxs-lookup"><span data-stu-id="d917b-152">NOTES</span></span>

## <span data-ttu-id="d917b-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d917b-153">RELATED LINKS</span></span>

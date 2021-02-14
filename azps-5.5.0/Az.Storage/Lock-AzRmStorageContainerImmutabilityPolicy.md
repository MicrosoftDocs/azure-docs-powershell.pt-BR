---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/lock-azrmstoragecontainerimmutabilitypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Lock-AzRmStorageContainerImmutabilityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Lock-AzRmStorageContainerImmutabilityPolicy.md
ms.openlocfilehash: 0cb3a4e65d8e464dda85e18e12dc106620e3eee8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115662"
---
# <span data-ttu-id="0127b-101">Lock-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="0127b-101">Lock-AzRmStorageContainerImmutabilityPolicy</span></span>

## <span data-ttu-id="0127b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0127b-102">SYNOPSIS</span></span>
<span data-ttu-id="0127b-103">Bloqueia immutabilidadePolicy de contêineres de blob de armazenamento</span><span class="sxs-lookup"><span data-stu-id="0127b-103">Locks ImmutabilityPolicy of a Storage blob containers</span></span>

## <span data-ttu-id="0127b-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0127b-104">SYNTAX</span></span>

### <span data-ttu-id="0127b-105">Nomeda Conta (Padrão)</span><span class="sxs-lookup"><span data-stu-id="0127b-105">AccountName (Default)</span></span>
```
Lock-AzRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -ContainerName <String> -Etag <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0127b-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="0127b-106">AccountObject</span></span>
```
Lock-AzRmStorageContainerImmutabilityPolicy -ContainerName <String> -StorageAccount <PSStorageAccount>
 -Etag <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0127b-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="0127b-107">ContainerObject</span></span>
```
Lock-AzRmStorageContainerImmutabilityPolicy -Container <PSContainer> -Etag <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0127b-108">ImmutabilityPolicyObject</span><span class="sxs-lookup"><span data-stu-id="0127b-108">ImmutabilityPolicyObject</span></span>
```
Lock-AzRmStorageContainerImmutabilityPolicy [-InputObject] <PSImmutabilityPolicy> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0127b-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="0127b-109">DESCRIPTION</span></span>
<span data-ttu-id="0127b-110">O cmdlet **Lock-AzRmStorageContainerImmutabilityPolicy** bloqueia ImmutabilityPolicy de um contêiner de blob de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="0127b-110">The **Lock-AzRmStorageContainerImmutabilityPolicy** cmdlet locks ImmutabilityPolicy of a Storage blob containers.</span></span>

## <span data-ttu-id="0127b-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="0127b-111">EXAMPLES</span></span>

### <span data-ttu-id="0127b-112">Exemplo 1: Bloquear ImmutabilidadePolicy de um contêiner de blob armazenamento com o nome da conta de armazenamento e o nome do contêiner</span><span class="sxs-lookup"><span data-stu-id="0127b-112">Example 1: Lock ImmutabilityPolicy of a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>$policy = Get-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer"
PS C:\>Lock-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -Etag $policy.Etag
```

<span data-ttu-id="0127b-113">Este comando bloqueia immutabilidadePolicy de um contêiner de blob armazenamento com o nome da conta de armazenamento e o nome do contêiner.</span><span class="sxs-lookup"><span data-stu-id="0127b-113">This command Locks ImmutabilityPolicy of a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="0127b-114">Exemplo 2: Bloquear ImmutabilidadePolicy de um contêiner de blob armazenamento, com objeto de conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="0127b-114">Example 2: Lock ImmutabilityPolicy of a Storage blob container, with Storage account object</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>$policy = Get-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer"
PS C:\>Lock-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer" -Etag $policy.Etag -Force
```

<span data-ttu-id="0127b-115">Esse comando bloqueia ImmutabilityPolicy de um contêiner de blob armazenamento, com objeto de conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="0127b-115">This command locks ImmutabilityPolicy of a Storage blob container, with Storage account object.</span></span> 

### <span data-ttu-id="0127b-116">Exemplo 3: Bloquear ImmutabilidadePolicy de um contêiner de blob armazenamento, com objeto de contêiner</span><span class="sxs-lookup"><span data-stu-id="0127b-116">Example 3: Lock ImmutabilityPolicyof a Storage blob container, with container object</span></span>
```
PS C:\>$containerObject = Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -Name "myContainer"
PS C:\>$policy = Get-AzRmStorageContainerImmutabilityPolicy -Container $containerObject
PS C:\>Lock-AzRmStorageContainerImmutabilityPolicy -Container $containerObject -Etag $policy.Etag -Force
```

<span data-ttu-id="0127b-117">Este comando bloqueia ImmutabilityPolicy de um contêiner de blob armazenamento com objeto de contêiner de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="0127b-117">This command locks ImmutabilityPolicy of a Storage blob container with Storage container object.</span></span>

### <span data-ttu-id="0127b-118">Exemplo 4: Bloquear ImmutabilidadePolicy de um contêiner de blob armazenamento, com objeto ImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="0127b-118">Example 4: Lock ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object</span></span>
```
PS C:\>Get-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" | Lock-AzRmStorageContainerImmutabilityPolicy -Force
```

<span data-ttu-id="0127b-119">Este comando bloqueia ImmutabilityPolicy de um contêiner de blob armazenamento, com objeto ImmutabilityPolicy.</span><span class="sxs-lookup"><span data-stu-id="0127b-119">This command locks ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object.</span></span> 

## <span data-ttu-id="0127b-120">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0127b-120">PARAMETERS</span></span>

### <span data-ttu-id="0127b-121">-Contêiner</span><span class="sxs-lookup"><span data-stu-id="0127b-121">-Container</span></span>
<span data-ttu-id="0127b-122">Objeto de contêiner de armazenamento</span><span class="sxs-lookup"><span data-stu-id="0127b-122">Storage container object</span></span>

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

### <span data-ttu-id="0127b-123">-Nomedo Contêiner</span><span class="sxs-lookup"><span data-stu-id="0127b-123">-ContainerName</span></span>
<span data-ttu-id="0127b-124">Nome do Contêiner</span><span class="sxs-lookup"><span data-stu-id="0127b-124">Container Name</span></span>

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

### <span data-ttu-id="0127b-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0127b-125">-DefaultProfile</span></span>
<span data-ttu-id="0127b-126">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="0127b-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0127b-127">-Etag</span><span class="sxs-lookup"><span data-stu-id="0127b-127">-Etag</span></span>
<span data-ttu-id="0127b-128">Étag de política de imutabilidade.</span><span class="sxs-lookup"><span data-stu-id="0127b-128">Immutability policy etag.</span></span>

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

### <span data-ttu-id="0127b-129">-Forçar</span><span class="sxs-lookup"><span data-stu-id="0127b-129">-Force</span></span>
<span data-ttu-id="0127b-130">Forçar a remoção da ImmutabilidadePolicy.</span><span class="sxs-lookup"><span data-stu-id="0127b-130">Force to remove the ImmutabilityPolicy.</span></span>

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

### <span data-ttu-id="0127b-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0127b-131">-InputObject</span></span>
<span data-ttu-id="0127b-132">Objeto ImmutabilityPolicy para Remover</span><span class="sxs-lookup"><span data-stu-id="0127b-132">ImmutabilityPolicy Object to Remove</span></span>

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

### <span data-ttu-id="0127b-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0127b-133">-ResourceGroupName</span></span>
<span data-ttu-id="0127b-134">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="0127b-134">Resource Group Name.</span></span>

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

### <span data-ttu-id="0127b-135">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="0127b-135">-StorageAccount</span></span>
<span data-ttu-id="0127b-136">Objeto de conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="0127b-136">Storage account object</span></span>

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

### <span data-ttu-id="0127b-137">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="0127b-137">-StorageAccountName</span></span>
<span data-ttu-id="0127b-138">Nome da Conta de Armazenamento.</span><span class="sxs-lookup"><span data-stu-id="0127b-138">Storage Account Name.</span></span>

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

### <span data-ttu-id="0127b-139">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="0127b-139">-Confirm</span></span>
<span data-ttu-id="0127b-140">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0127b-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0127b-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0127b-141">-WhatIf</span></span>
<span data-ttu-id="0127b-142">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="0127b-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0127b-143">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0127b-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0127b-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0127b-144">CommonParameters</span></span>
<span data-ttu-id="0127b-145">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0127b-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0127b-146">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0127b-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0127b-147">Entradas</span><span class="sxs-lookup"><span data-stu-id="0127b-147">INPUTS</span></span>

### <span data-ttu-id="0127b-148">System.String</span><span class="sxs-lookup"><span data-stu-id="0127b-148">System.String</span></span>

### <span data-ttu-id="0127b-149">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0127b-149">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="0127b-150">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span><span class="sxs-lookup"><span data-stu-id="0127b-150">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

### <span data-ttu-id="0127b-151">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="0127b-151">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="0127b-152">Saídas</span><span class="sxs-lookup"><span data-stu-id="0127b-152">OUTPUTS</span></span>

### <span data-ttu-id="0127b-153">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="0127b-153">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="0127b-154">Notas</span><span class="sxs-lookup"><span data-stu-id="0127b-154">NOTES</span></span>

## <span data-ttu-id="0127b-155">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0127b-155">RELATED LINKS</span></span>

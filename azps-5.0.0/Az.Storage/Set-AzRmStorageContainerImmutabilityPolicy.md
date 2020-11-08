---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azrmstoragecontainerimmutabilitypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzRmStorageContainerImmutabilityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzRmStorageContainerImmutabilityPolicy.md
ms.openlocfilehash: 9631855803b4ad16312c907c1d1c747b3aee6fdf
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94115782"
---
# <span data-ttu-id="f851a-101">Set-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="f851a-101">Set-AzRmStorageContainerImmutabilityPolicy</span></span>

## <span data-ttu-id="f851a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f851a-102">SYNOPSIS</span></span>
<span data-ttu-id="f851a-103">Cria ou atualiza ImmutabilityPolicy de um contêiner de blob de armazenamento</span><span class="sxs-lookup"><span data-stu-id="f851a-103">Creates or updates ImmutabilityPolicy of a Storage blob containers</span></span>

## <span data-ttu-id="f851a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f851a-104">SYNTAX</span></span>

### <span data-ttu-id="f851a-105">AccountName (padrão)</span><span class="sxs-lookup"><span data-stu-id="f851a-105">AccountName (Default)</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -ContainerName <String> [-ImmutabilityPeriod <Int32>] [-AllowProtectedAppendWrite <Boolean>] [-Etag <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f851a-106">ExtendAccountName</span><span class="sxs-lookup"><span data-stu-id="f851a-106">ExtendAccountName</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -ContainerName <String> -ImmutabilityPeriod <Int32> -Etag <String> [-ExtendPolicy]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f851a-107">Accountobject</span><span class="sxs-lookup"><span data-stu-id="f851a-107">AccountObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy -ContainerName <String> -StorageAccount <PSStorageAccount>
 [-ImmutabilityPeriod <Int32>] [-AllowProtectedAppendWrite <Boolean>] [-Etag <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f851a-108">ExtendAccountObject</span><span class="sxs-lookup"><span data-stu-id="f851a-108">ExtendAccountObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy -ContainerName <String> -StorageAccount <PSStorageAccount>
 -ImmutabilityPeriod <Int32> -Etag <String> [-ExtendPolicy] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f851a-109">Idcontêiner</span><span class="sxs-lookup"><span data-stu-id="f851a-109">ContainerObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy -Container <PSContainer> [-ImmutabilityPeriod <Int32>]
 [-AllowProtectedAppendWrite <Boolean>] [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f851a-110">ExtendContainerObject</span><span class="sxs-lookup"><span data-stu-id="f851a-110">ExtendContainerObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy -Container <PSContainer> -ImmutabilityPeriod <Int32> -Etag <String>
 [-ExtendPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f851a-111">ImmutabilityPolicyObject</span><span class="sxs-lookup"><span data-stu-id="f851a-111">ImmutabilityPolicyObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy [-InputObject] <PSImmutabilityPolicy> [-ImmutabilityPeriod <Int32>]
 [-AllowProtectedAppendWrite <Boolean>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f851a-112">ExtendImmutabilityPolicyObject</span><span class="sxs-lookup"><span data-stu-id="f851a-112">ExtendImmutabilityPolicyObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy [-InputObject] <PSImmutabilityPolicy> -ImmutabilityPeriod <Int32>
 [-ExtendPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f851a-113">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f851a-113">DESCRIPTION</span></span>
<span data-ttu-id="f851a-114">O cmdlet **set-AzRmStorageContainerImmutabilityPolicy** cria ou atualiza ImmutabilityPolicy de contêineres de blob de armazenamento</span><span class="sxs-lookup"><span data-stu-id="f851a-114">The **Set-AzRmStorageContainerImmutabilityPolicy** cmdlet creates or updates ImmutabilityPolicy of a Storage blob containers</span></span>

## <span data-ttu-id="f851a-115">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f851a-115">EXAMPLES</span></span>

### <span data-ttu-id="f851a-116">Exemplo 1: criar ou atualizar ImmutabilityPolicy de um contêiner de blob de armazenamento com nome da conta de armazenamento e nome do contêiner</span><span class="sxs-lookup"><span data-stu-id="f851a-116">Example 1: Create or update ImmutabilityPolicy of a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Set-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -ImmutabilityPeriod 10
```

<span data-ttu-id="f851a-117">Este comando cria ou atualiza ImmutabilityPolicy de um contêiner de blob de armazenamento com o nome da conta de armazenamento e o nome do contêiner.</span><span class="sxs-lookup"><span data-stu-id="f851a-117">This command creates or updates ImmutabilityPolicy of a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="f851a-118">Exemplo 2: estender o ImmutabilityPolicy de um contêiner de blob de armazenamento com o objeto da conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="f851a-118">Example 2: Extend ImmutabilityPolicy of a Storage blob container, with Storage account object</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>$policy = Get-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer"
PS C:\>Set-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer" -ImmutabilityPeriod 20 -Etag $policy.Etag -ExtendPolicy
```

<span data-ttu-id="f851a-119">Esse comando estende o ImmutabilityPolicy de um contêiner de blob de armazenamento, com objeto da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="f851a-119">This command extend ImmutabilityPolicy of a Storage blob container, with Storage account object.</span></span> <span data-ttu-id="f851a-120">Extend ImmutabilityPolicy só pode ser executado após o bloqueio de ImmutabilityPolicy.</span><span class="sxs-lookup"><span data-stu-id="f851a-120">Extend ImmutabilityPolicy can only run after ImmutabilityPolicy is locked.</span></span>

### <span data-ttu-id="f851a-121">Exemplo 3: atualizar o ImmutabilityPolicy de um contêiner de blob de armazenamento</span><span class="sxs-lookup"><span data-stu-id="f851a-121">Example 3: Update ImmutabilityPolicy of a Storage blob container</span></span>
```
PS C:\>$containerObject = Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -Name "myContainer"
PS C:\>$policy = Set-AzRmStorageContainerImmutabilityPolicy -Container $containerObject -ImmutabilityPeriod 12
PS C:\>$policy = Set-AzRmStorageContainerImmutabilityPolicy -Container $containerObject -ImmutabilityPeriod 9 -Etag $policy.Etag
PS C:\>$policy = Set-AzRmStorageContainerImmutabilityPolicy -Container $containerObject -AllowProtectedAppendWrite $true
```

<span data-ttu-id="f851a-122">Este comando atualiza o ImmutabilityPolicy de um contêiner de blob de armazenamento com o objeto de contêiner de armazenamento 3 vezes: primeiro para ImmutabilityPeriod 12 dias sem ETag, para ImmutabilityPeriod 9 dias com ETag, por fim habilitou AllowProtectedAppendWrite.</span><span class="sxs-lookup"><span data-stu-id="f851a-122">This command updates ImmutabilityPolicy of a Storage blob container with Storage container object 3 times: First to ImmutabilityPeriod 12 days without etag, then to ImmutabilityPeriod 9 days with etag, finally enabled AllowProtectedAppendWrite.</span></span>

### <span data-ttu-id="f851a-123">Exemplo 4: estender o ImmutabilityPolicy de um contêiner de blob de armazenamento com objeto ImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="f851a-123">Example 4: Extend ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object</span></span>
```
PS C:\>Get-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" | Set-AzRmStorageContainerImmutabilityPolicy -ImmutabilityPeriod 15 -ExtendPolicy
```

<span data-ttu-id="f851a-124">Esse comando estende o ImmutabilityPolicy de um contêiner de blob de armazenamento, com objeto ImmutabilityPolicy.</span><span class="sxs-lookup"><span data-stu-id="f851a-124">This command extend ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object.</span></span> <span data-ttu-id="f851a-125">Extend ImmutabilityPolicy só pode ser executado após o bloqueio de ImmutabilityPolicy.</span><span class="sxs-lookup"><span data-stu-id="f851a-125">Extend ImmutabilityPolicy can only run after ImmutabilityPolicy is locked.</span></span>

## <span data-ttu-id="f851a-126">OS</span><span class="sxs-lookup"><span data-stu-id="f851a-126">PARAMETERS</span></span>

### <span data-ttu-id="f851a-127">-AllowProtectedAppendWrite</span><span class="sxs-lookup"><span data-stu-id="f851a-127">-AllowProtectedAppendWrite</span></span>
<span data-ttu-id="f851a-128">Essa propriedade só pode ser alterada para políticas de retenção com base em tempo desbloqueada.</span><span class="sxs-lookup"><span data-stu-id="f851a-128">This property can only be changed for unlocked time-based retention policies.</span></span> <span data-ttu-id="f851a-129">Com essa propriedade habilitada, novos blocos podem ser gravados em um blob de acréscimo, mantendo a proteção contra imutabilidade e a conformidade.</span><span class="sxs-lookup"><span data-stu-id="f851a-129">With this property enabled, new blocks can be written to an append blob while maintaining immutability protection and compliance.</span></span> <span data-ttu-id="f851a-130">Somente novos blocos podem ser adicionados e os blocos existentes não podem ser modificados ou excluídos.</span><span class="sxs-lookup"><span data-stu-id="f851a-130">Only new blocks can be added and any existing blocks cannot be modified or deleted.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: AccountName, AccountObject, ContainerObject, ImmutabilityPolicyObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f851a-131">-Contêiner</span><span class="sxs-lookup"><span data-stu-id="f851a-131">-Container</span></span>
<span data-ttu-id="f851a-132">Objeto contêiner de armazenamento</span><span class="sxs-lookup"><span data-stu-id="f851a-132">Storage container object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSContainer
Parameter Sets: ContainerObject, ExtendContainerObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f851a-133">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="f851a-133">-ContainerName</span></span>
<span data-ttu-id="f851a-134">Nome do contêiner</span><span class="sxs-lookup"><span data-stu-id="f851a-134">Container Name</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, ExtendAccountName, AccountObject, ExtendAccountObject
Aliases: N

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f851a-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f851a-135">-DefaultProfile</span></span>
<span data-ttu-id="f851a-136">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f851a-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f851a-137">-ETag</span><span class="sxs-lookup"><span data-stu-id="f851a-137">-Etag</span></span>
<span data-ttu-id="f851a-138">ETag da política de imutabilidade.</span><span class="sxs-lookup"><span data-stu-id="f851a-138">Immutability policy etag.</span></span> <span data-ttu-id="f851a-139">Se-ExtendPolicy não for especificado, ETag será opcional; else ETag é necessário.</span><span class="sxs-lookup"><span data-stu-id="f851a-139">If -ExtendPolicy is not specified, Etag is optional; else Etag is required.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountObject, ContainerObject
Aliases: IfMatch

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ExtendAccountName, ExtendAccountObject, ExtendContainerObject
Aliases: IfMatch

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f851a-140">-ExtendPolicy</span><span class="sxs-lookup"><span data-stu-id="f851a-140">-ExtendPolicy</span></span>
<span data-ttu-id="f851a-141">Indique ExtendPolicy para estender um ImmutabilityPolicy existente.</span><span class="sxs-lookup"><span data-stu-id="f851a-141">Indicate ExtendPolicy to Extend an existing ImmutabilityPolicy.</span></span>  <span data-ttu-id="f851a-142">Depois que o ImmutabilityPolicy estiver bloqueado, ele só poderá ser estendido.</span><span class="sxs-lookup"><span data-stu-id="f851a-142">After ImmutabilityPolicy is locked, it can only be extend.</span></span> 

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ExtendAccountName, ExtendAccountObject, ExtendContainerObject, ExtendImmutabilityPolicyObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f851a-143">-ImmutabilityPeriod</span><span class="sxs-lookup"><span data-stu-id="f851a-143">-ImmutabilityPeriod</span></span>
<span data-ttu-id="f851a-144">Período de imutabilidade desde a criação em dias.</span><span class="sxs-lookup"><span data-stu-id="f851a-144">Immutability period since creation in days.</span></span>

```yaml
Type: System.Int32
Parameter Sets: AccountName, AccountObject, ContainerObject, ImmutabilityPolicyObject
Aliases: ImmutabilityPeriodSinceCreationInDays

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Int32
Parameter Sets: ExtendAccountName, ExtendAccountObject, ExtendContainerObject, ExtendImmutabilityPolicyObject
Aliases: ImmutabilityPeriodSinceCreationInDays

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f851a-145">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f851a-145">-InputObject</span></span>
<span data-ttu-id="f851a-146">Nome do contêiner</span><span class="sxs-lookup"><span data-stu-id="f851a-146">Container Name</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy
Parameter Sets: ImmutabilityPolicyObject, ExtendImmutabilityPolicyObject
Aliases: ImmutabilityPolicy

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f851a-147">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f851a-147">-ResourceGroupName</span></span>
<span data-ttu-id="f851a-148">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f851a-148">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, ExtendAccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f851a-149">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="f851a-149">-StorageAccount</span></span>
<span data-ttu-id="f851a-150">Objeto da conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="f851a-150">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject, ExtendAccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f851a-151">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="f851a-151">-StorageAccountName</span></span>
<span data-ttu-id="f851a-152">Nome da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="f851a-152">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, ExtendAccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f851a-153">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f851a-153">-Confirm</span></span>
<span data-ttu-id="f851a-154">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f851a-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f851a-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f851a-155">-WhatIf</span></span>
<span data-ttu-id="f851a-156">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f851a-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f851a-157">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f851a-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f851a-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f851a-158">CommonParameters</span></span>
<span data-ttu-id="f851a-159">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f851a-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f851a-160">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f851a-160">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f851a-161">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f851a-161">INPUTS</span></span>

### <span data-ttu-id="f851a-162">System. String</span><span class="sxs-lookup"><span data-stu-id="f851a-162">System.String</span></span>

### <span data-ttu-id="f851a-163">Microsoft. Azure. Commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f851a-163">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="f851a-164">Microsoft. Azure. Commands. Management. Storage. Models. PSContainer</span><span class="sxs-lookup"><span data-stu-id="f851a-164">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

### <span data-ttu-id="f851a-165">Microsoft. Azure. Commands. Management. Storage. Models. PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="f851a-165">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="f851a-166">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f851a-166">OUTPUTS</span></span>

### <span data-ttu-id="f851a-167">Microsoft. Azure. Commands. Management. Storage. Models. PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="f851a-167">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="f851a-168">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f851a-168">NOTES</span></span>

## <span data-ttu-id="f851a-169">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f851a-169">RELATED LINKS</span></span>

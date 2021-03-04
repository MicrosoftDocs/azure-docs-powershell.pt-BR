---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/set-azrmstoragecontainerimmutabilitypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzRmStorageContainerImmutabilityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzRmStorageContainerImmutabilityPolicy.md
ms.openlocfilehash: 81db149500ce489801a25437fbb7a50443d7426a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888157"
---
# <span data-ttu-id="70ae5-101">Set-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="70ae5-101">Set-AzRmStorageContainerImmutabilityPolicy</span></span>

## <span data-ttu-id="70ae5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="70ae5-102">SYNOPSIS</span></span>
<span data-ttu-id="70ae5-103">Cria ou atualiza ImmutabilityPolicy de um contêiner de blob de armazenamento</span><span class="sxs-lookup"><span data-stu-id="70ae5-103">Creates or updates ImmutabilityPolicy of a Storage blob containers</span></span>

## <span data-ttu-id="70ae5-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="70ae5-104">SYNTAX</span></span>

### <span data-ttu-id="70ae5-105">AccountName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="70ae5-105">AccountName (Default)</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -ContainerName <String> [-ImmutabilityPeriod <Int32>] [-AllowProtectedAppendWrite <Boolean>] [-Etag <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="70ae5-106">ExtendAccountName</span><span class="sxs-lookup"><span data-stu-id="70ae5-106">ExtendAccountName</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -ContainerName <String> -ImmutabilityPeriod <Int32> -Etag <String> [-ExtendPolicy]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="70ae5-107">AccountObject</span><span class="sxs-lookup"><span data-stu-id="70ae5-107">AccountObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy -ContainerName <String> -StorageAccount <PSStorageAccount>
 [-ImmutabilityPeriod <Int32>] [-AllowProtectedAppendWrite <Boolean>] [-Etag <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="70ae5-108">ExtendAccountObject</span><span class="sxs-lookup"><span data-stu-id="70ae5-108">ExtendAccountObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy -ContainerName <String> -StorageAccount <PSStorageAccount>
 -ImmutabilityPeriod <Int32> -Etag <String> [-ExtendPolicy] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="70ae5-109">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="70ae5-109">ContainerObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy -Container <PSContainer> [-ImmutabilityPeriod <Int32>]
 [-AllowProtectedAppendWrite <Boolean>] [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="70ae5-110">ExtendContainerObject</span><span class="sxs-lookup"><span data-stu-id="70ae5-110">ExtendContainerObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy -Container <PSContainer> -ImmutabilityPeriod <Int32> -Etag <String>
 [-ExtendPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="70ae5-111">ImmutabilityPolicyObject</span><span class="sxs-lookup"><span data-stu-id="70ae5-111">ImmutabilityPolicyObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy [-InputObject] <PSImmutabilityPolicy> [-ImmutabilityPeriod <Int32>]
 [-AllowProtectedAppendWrite <Boolean>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="70ae5-112">ExtendImmutabilityPolicyObject</span><span class="sxs-lookup"><span data-stu-id="70ae5-112">ExtendImmutabilityPolicyObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy [-InputObject] <PSImmutabilityPolicy> -ImmutabilityPeriod <Int32>
 [-ExtendPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="70ae5-113">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="70ae5-113">DESCRIPTION</span></span>
<span data-ttu-id="70ae5-114">O cmdlet **Set-AzRmStorageContainerImmutabilityPolicy** cria ou atualiza ImmutabilityPolicy de um contêiner de blob de armazenamento</span><span class="sxs-lookup"><span data-stu-id="70ae5-114">The **Set-AzRmStorageContainerImmutabilityPolicy** cmdlet creates or updates ImmutabilityPolicy of a Storage blob containers</span></span>

## <span data-ttu-id="70ae5-115">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="70ae5-115">EXAMPLES</span></span>

### <span data-ttu-id="70ae5-116">Exemplo 1: Criar ou atualizar ImmutabilityPolicy de um contêiner de blob de armazenamento com o nome da conta de armazenamento e o nome do contêiner</span><span class="sxs-lookup"><span data-stu-id="70ae5-116">Example 1: Create or update ImmutabilityPolicy of a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Set-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -ImmutabilityPeriod 10
```

<span data-ttu-id="70ae5-117">Este comando cria ou atualiza ImmutabilityPolicy de um contêiner de blob de armazenamento com o nome da conta de armazenamento e o nome do contêiner.</span><span class="sxs-lookup"><span data-stu-id="70ae5-117">This command creates or updates ImmutabilityPolicy of a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="70ae5-118">Exemplo 2: Estender ImmutabilityPolicy de um contêiner de blob de armazenamento, com objeto de conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="70ae5-118">Example 2: Extend ImmutabilityPolicy of a Storage blob container, with Storage account object</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>$policy = Get-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer"
PS C:\>Set-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer" -ImmutabilityPeriod 20 -Etag $policy.Etag -ExtendPolicy
```

<span data-ttu-id="70ae5-119">Este comando estende ImmutabilityPolicy de um contêiner de blob de armazenamento, com objeto de conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="70ae5-119">This command extend ImmutabilityPolicy of a Storage blob container, with Storage account object.</span></span> <span data-ttu-id="70ae5-120">Extend ImmutabilityPolicy só pode ser executado depois que ImmutabilityPolicy for bloqueado.</span><span class="sxs-lookup"><span data-stu-id="70ae5-120">Extend ImmutabilityPolicy can only run after ImmutabilityPolicy is locked.</span></span>

### <span data-ttu-id="70ae5-121">Exemplo 3: Atualizar ImmutabilityPolicy de um contêiner de blob de armazenamento</span><span class="sxs-lookup"><span data-stu-id="70ae5-121">Example 3: Update ImmutabilityPolicy of a Storage blob container</span></span>
```
PS C:\>$containerObject = Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -Name "myContainer"
PS C:\>$policy = Set-AzRmStorageContainerImmutabilityPolicy -Container $containerObject -ImmutabilityPeriod 12
PS C:\>$policy = Set-AzRmStorageContainerImmutabilityPolicy -Container $containerObject -ImmutabilityPeriod 9 -Etag $policy.Etag
PS C:\>$policy = Set-AzRmStorageContainerImmutabilityPolicy -Container $containerObject -AllowProtectedAppendWrite $true
```

<span data-ttu-id="70ae5-122">Este comando atualiza ImmutabilityPolicy de um contêiner de blob de armazenamento com objeto de contêiner de armazenamento 3 vezes: primeiro para ImmutabilityPeriod 12 dias sem etag, em seguida, para ImmutabilityPeriod 9 dias com etag, finalmente habilitado AllowProtectedAppendWrite.</span><span class="sxs-lookup"><span data-stu-id="70ae5-122">This command updates ImmutabilityPolicy of a Storage blob container with Storage container object 3 times: First to ImmutabilityPeriod 12 days without etag, then to ImmutabilityPeriod 9 days with etag, finally enabled AllowProtectedAppendWrite.</span></span>

### <span data-ttu-id="70ae5-123">Exemplo 4: Estender ImmutabilityPolicy de um contêiner de blob de armazenamento, com objeto ImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="70ae5-123">Example 4: Extend ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object</span></span>
```
PS C:\>Get-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" | Set-AzRmStorageContainerImmutabilityPolicy -ImmutabilityPeriod 15 -ExtendPolicy
```

<span data-ttu-id="70ae5-124">Este comando estende ImmutabilityPolicy de um contêiner de blob de armazenamento, com objeto ImmutabilityPolicy.</span><span class="sxs-lookup"><span data-stu-id="70ae5-124">This command extend ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object.</span></span> <span data-ttu-id="70ae5-125">Extend ImmutabilityPolicy só pode ser executado depois que ImmutabilityPolicy for bloqueado.</span><span class="sxs-lookup"><span data-stu-id="70ae5-125">Extend ImmutabilityPolicy can only run after ImmutabilityPolicy is locked.</span></span>

## <span data-ttu-id="70ae5-126">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="70ae5-126">PARAMETERS</span></span>

### <span data-ttu-id="70ae5-127">-AllowProtectedAppendWrite</span><span class="sxs-lookup"><span data-stu-id="70ae5-127">-AllowProtectedAppendWrite</span></span>
<span data-ttu-id="70ae5-128">Essa propriedade só pode ser alterada para políticas de retenção baseadas em tempo desbloqueadas.</span><span class="sxs-lookup"><span data-stu-id="70ae5-128">This property can only be changed for unlocked time-based retention policies.</span></span> <span data-ttu-id="70ae5-129">Com essa propriedade habilitada, novos blocos podem ser gravados em um blob de anexação, mantendo a proteção e a conformidade imutabilidade.</span><span class="sxs-lookup"><span data-stu-id="70ae5-129">With this property enabled, new blocks can be written to an append blob while maintaining immutability protection and compliance.</span></span> <span data-ttu-id="70ae5-130">Somente novos blocos podem ser adicionados e quaisquer blocos existentes não podem ser modificados ou excluídos.</span><span class="sxs-lookup"><span data-stu-id="70ae5-130">Only new blocks can be added and any existing blocks cannot be modified or deleted.</span></span>

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

### <span data-ttu-id="70ae5-131">-Container</span><span class="sxs-lookup"><span data-stu-id="70ae5-131">-Container</span></span>
<span data-ttu-id="70ae5-132">Objeto contêiner de armazenamento</span><span class="sxs-lookup"><span data-stu-id="70ae5-132">Storage container object</span></span>

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

### <span data-ttu-id="70ae5-133">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="70ae5-133">-ContainerName</span></span>
<span data-ttu-id="70ae5-134">Nome do contêiner</span><span class="sxs-lookup"><span data-stu-id="70ae5-134">Container Name</span></span>

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

### <span data-ttu-id="70ae5-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70ae5-135">-DefaultProfile</span></span>
<span data-ttu-id="70ae5-136">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="70ae5-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="70ae5-137">-Etag</span><span class="sxs-lookup"><span data-stu-id="70ae5-137">-Etag</span></span>
<span data-ttu-id="70ae5-138">Etag de política de imutabilidade.</span><span class="sxs-lookup"><span data-stu-id="70ae5-138">Immutability policy etag.</span></span> <span data-ttu-id="70ae5-139">Se -ExtendPolicy não for especificado, Etag será opcional; else Etag is required.</span><span class="sxs-lookup"><span data-stu-id="70ae5-139">If -ExtendPolicy is not specified, Etag is optional; else Etag is required.</span></span>

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

### <span data-ttu-id="70ae5-140">-ExtendPolicy</span><span class="sxs-lookup"><span data-stu-id="70ae5-140">-ExtendPolicy</span></span>
<span data-ttu-id="70ae5-141">Indique ExtendPolicy para Estender uma ImmutabilityPolicy existente.</span><span class="sxs-lookup"><span data-stu-id="70ae5-141">Indicate ExtendPolicy to Extend an existing ImmutabilityPolicy.</span></span>  <span data-ttu-id="70ae5-142">Depois que ImmutabilityPolicy for bloqueado, ele só poderá ser ampliado.</span><span class="sxs-lookup"><span data-stu-id="70ae5-142">After ImmutabilityPolicy is locked, it can only be extend.</span></span> 

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

### <span data-ttu-id="70ae5-143">-ImmutabilityPeriod</span><span class="sxs-lookup"><span data-stu-id="70ae5-143">-ImmutabilityPeriod</span></span>
<span data-ttu-id="70ae5-144">Período de imutabilidade desde a criação em dias.</span><span class="sxs-lookup"><span data-stu-id="70ae5-144">Immutability period since creation in days.</span></span>

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

### <span data-ttu-id="70ae5-145">-InputObject</span><span class="sxs-lookup"><span data-stu-id="70ae5-145">-InputObject</span></span>
<span data-ttu-id="70ae5-146">Nome do contêiner</span><span class="sxs-lookup"><span data-stu-id="70ae5-146">Container Name</span></span>

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

### <span data-ttu-id="70ae5-147">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70ae5-147">-ResourceGroupName</span></span>
<span data-ttu-id="70ae5-148">Nome do Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="70ae5-148">Resource Group Name.</span></span>

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

### <span data-ttu-id="70ae5-149">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="70ae5-149">-StorageAccount</span></span>
<span data-ttu-id="70ae5-150">Objeto de conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="70ae5-150">Storage account object</span></span>

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

### <span data-ttu-id="70ae5-151">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="70ae5-151">-StorageAccountName</span></span>
<span data-ttu-id="70ae5-152">Nome da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="70ae5-152">Storage Account Name.</span></span>

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

### <span data-ttu-id="70ae5-153">-Confirm</span><span class="sxs-lookup"><span data-stu-id="70ae5-153">-Confirm</span></span>
<span data-ttu-id="70ae5-154">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="70ae5-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="70ae5-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="70ae5-155">-WhatIf</span></span>
<span data-ttu-id="70ae5-156">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="70ae5-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="70ae5-157">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="70ae5-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="70ae5-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70ae5-158">CommonParameters</span></span>
<span data-ttu-id="70ae5-159">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70ae5-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70ae5-160">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="70ae5-160">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70ae5-161">INPUTS</span><span class="sxs-lookup"><span data-stu-id="70ae5-161">INPUTS</span></span>

### <span data-ttu-id="70ae5-162">System.String</span><span class="sxs-lookup"><span data-stu-id="70ae5-162">System.String</span></span>

### <span data-ttu-id="70ae5-163">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="70ae5-163">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="70ae5-164">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span><span class="sxs-lookup"><span data-stu-id="70ae5-164">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

### <span data-ttu-id="70ae5-165">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="70ae5-165">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="70ae5-166">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="70ae5-166">OUTPUTS</span></span>

### <span data-ttu-id="70ae5-167">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="70ae5-167">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="70ae5-168">NOTES</span><span class="sxs-lookup"><span data-stu-id="70ae5-168">NOTES</span></span>

## <span data-ttu-id="70ae5-169">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="70ae5-169">RELATED LINKS</span></span>

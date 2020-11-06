---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azrmstoragecontainerimmutabilitypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzRmStorageContainerImmutabilityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzRmStorageContainerImmutabilityPolicy.md
ms.openlocfilehash: c216765657cc87c958cc20dd0f2014f0e1c16970
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93598551"
---
# <span data-ttu-id="d01fa-101">Set-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="d01fa-101">Set-AzRmStorageContainerImmutabilityPolicy</span></span>

## <span data-ttu-id="d01fa-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d01fa-102">SYNOPSIS</span></span>
<span data-ttu-id="d01fa-103">Cria ou atualiza ImmutabilityPolicy de um contêiner de blob de armazenamento</span><span class="sxs-lookup"><span data-stu-id="d01fa-103">Creates or updates ImmutabilityPolicy of a Storage blob containers</span></span>

## <span data-ttu-id="d01fa-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d01fa-104">SYNTAX</span></span>

### <span data-ttu-id="d01fa-105">AccountName (padrão)</span><span class="sxs-lookup"><span data-stu-id="d01fa-105">AccountName (Default)</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -ContainerName <String> -ImmutabilityPeriod <Int32> [-Etag <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d01fa-106">ExtendAccountName</span><span class="sxs-lookup"><span data-stu-id="d01fa-106">ExtendAccountName</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -ContainerName <String> -ImmutabilityPeriod <Int32> -Etag <String> [-ExtendPolicy]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d01fa-107">Accountobject</span><span class="sxs-lookup"><span data-stu-id="d01fa-107">AccountObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy -ContainerName <String> -StorageAccount <PSStorageAccount>
 -ImmutabilityPeriod <Int32> [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d01fa-108">ExtendAccountObject</span><span class="sxs-lookup"><span data-stu-id="d01fa-108">ExtendAccountObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy -ContainerName <String> -StorageAccount <PSStorageAccount>
 -ImmutabilityPeriod <Int32> -Etag <String> [-ExtendPolicy] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d01fa-109">Idcontêiner</span><span class="sxs-lookup"><span data-stu-id="d01fa-109">ContainerObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy -Container <PSContainer> -ImmutabilityPeriod <Int32>
 [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d01fa-110">ExtendContainerObject</span><span class="sxs-lookup"><span data-stu-id="d01fa-110">ExtendContainerObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy -Container <PSContainer> -ImmutabilityPeriod <Int32> -Etag <String>
 [-ExtendPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d01fa-111">ImmutabilityPolicyObject</span><span class="sxs-lookup"><span data-stu-id="d01fa-111">ImmutabilityPolicyObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy [-InputObject] <PSImmutabilityPolicy> -ImmutabilityPeriod <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d01fa-112">ExtendImmutabilityPolicyObject</span><span class="sxs-lookup"><span data-stu-id="d01fa-112">ExtendImmutabilityPolicyObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy [-InputObject] <PSImmutabilityPolicy> -ImmutabilityPeriod <Int32>
 [-ExtendPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d01fa-113">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d01fa-113">DESCRIPTION</span></span>
<span data-ttu-id="d01fa-114">O cmdlet **set-AzRmStorageContainerImmutabilityPolicy** cria ou atualiza ImmutabilityPolicy de contêineres de blob de armazenamento</span><span class="sxs-lookup"><span data-stu-id="d01fa-114">The **Set-AzRmStorageContainerImmutabilityPolicy** cmdlet creates or updates ImmutabilityPolicy of a Storage blob containers</span></span>

## <span data-ttu-id="d01fa-115">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d01fa-115">EXAMPLES</span></span>

### <span data-ttu-id="d01fa-116">Exemplo 1: criar ou atualizar ImmutabilityPolicy de um contêiner de blob de armazenamento com nome da conta de armazenamento e nome do contêiner</span><span class="sxs-lookup"><span data-stu-id="d01fa-116">Example 1: Create or update ImmutabilityPolicy of a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Set-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -ImmutabilityPeriod 10
```

<span data-ttu-id="d01fa-117">Este comando cria ou atualiza ImmutabilityPolicy de um contêiner de blob de armazenamento com o nome da conta de armazenamento e o nome do contêiner.</span><span class="sxs-lookup"><span data-stu-id="d01fa-117">This command creates or updates ImmutabilityPolicy of a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="d01fa-118">Exemplo 2: estender o ImmutabilityPolicy de um contêiner de blob de armazenamento com o objeto da conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="d01fa-118">Example 2: Extend ImmutabilityPolicy of a Storage blob container, with Storage account object</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>$policy = Get-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer"
PS C:\>Set-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer" -ImmutabilityPeriod 20 -Etag $policy.Etag -ExtendPolicy
```

<span data-ttu-id="d01fa-119">Esse comando estende o ImmutabilityPolicy de um contêiner de blob de armazenamento, com objeto da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="d01fa-119">This command extend ImmutabilityPolicy of a Storage blob container, with Storage account object.</span></span> <span data-ttu-id="d01fa-120">Extend ImmutabilityPolicy só pode ser executado após o bloqueio de ImmutabilityPolicy.</span><span class="sxs-lookup"><span data-stu-id="d01fa-120">Extend ImmutabilityPolicy can only run after ImmutabilityPolicy is locked.</span></span>

### <span data-ttu-id="d01fa-121">Exemplo 3: atualizar ImmutabilityPolicyof um contêiner de blob de armazenamento</span><span class="sxs-lookup"><span data-stu-id="d01fa-121">Example 3: Update ImmutabilityPolicyof a Storage blob container</span></span>
```
PS C:\>$containerObject = Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -Name "myContainer"
PS C:\>$policy = Set-AzRmStorageContainerImmutabilityPolicy -Container $containerObject -ImmutabilityPeriod 12
PS C:\>$policy = Set-AzRmStorageContainerImmutabilityPolicy -Container $containerObject -ImmutabilityPeriod 9 -Etag $policy.Etag
```

<span data-ttu-id="d01fa-122">Esse comando atualiza o ImmutabilityPolicy de um contêiner de blob de armazenamento com objeto de contêiner de armazenamento 2 vezes, primeiro ao ImmutabilityPeriod 12 dias sem ETag, e para ImmutabilityPeriod 9 dias com ETag.</span><span class="sxs-lookup"><span data-stu-id="d01fa-122">This command updates ImmutabilityPolicy of a Storage blob container with Storage container object 2 times, first to ImmutabilityPeriod 12 days without etag, then to ImmutabilityPeriod 9 days with etag.</span></span>

### <span data-ttu-id="d01fa-123">Exemplo 4: estender o ImmutabilityPolicy de um contêiner de blob de armazenamento com objeto ImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="d01fa-123">Example 4: Extend ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object</span></span>
```
PS C:\>Get-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" | Set-AzRmStorageContainerImmutabilityPolicy -ImmutabilityPeriod 15 -ExtendPolicy
```

<span data-ttu-id="d01fa-124">Esse comando estende o ImmutabilityPolicy de um contêiner de blob de armazenamento, com objeto ImmutabilityPolicy.</span><span class="sxs-lookup"><span data-stu-id="d01fa-124">This command extend ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object.</span></span> <span data-ttu-id="d01fa-125">Extend ImmutabilityPolicy só pode ser executado após o bloqueio de ImmutabilityPolicy.</span><span class="sxs-lookup"><span data-stu-id="d01fa-125">Extend ImmutabilityPolicy can only run after ImmutabilityPolicy is locked.</span></span>

## <span data-ttu-id="d01fa-126">OS</span><span class="sxs-lookup"><span data-stu-id="d01fa-126">PARAMETERS</span></span>

### <span data-ttu-id="d01fa-127">-Contêiner</span><span class="sxs-lookup"><span data-stu-id="d01fa-127">-Container</span></span>
<span data-ttu-id="d01fa-128">Objeto contêiner de armazenamento</span><span class="sxs-lookup"><span data-stu-id="d01fa-128">Storage container object</span></span>

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

### <span data-ttu-id="d01fa-129">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="d01fa-129">-ContainerName</span></span>
<span data-ttu-id="d01fa-130">Nome do contêiner</span><span class="sxs-lookup"><span data-stu-id="d01fa-130">Container Name</span></span>

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

### <span data-ttu-id="d01fa-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d01fa-131">-DefaultProfile</span></span>
<span data-ttu-id="d01fa-132">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d01fa-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d01fa-133">-ETag</span><span class="sxs-lookup"><span data-stu-id="d01fa-133">-Etag</span></span>
<span data-ttu-id="d01fa-134">ETag da política de imutabilidade.</span><span class="sxs-lookup"><span data-stu-id="d01fa-134">Immutability policy etag.</span></span> <span data-ttu-id="d01fa-135">Se-ExtendPolicy não for especificado, ETag será opcional; else ETag é necessário.</span><span class="sxs-lookup"><span data-stu-id="d01fa-135">If -ExtendPolicy is not specified, Etag is optional; else Etag is required.</span></span>

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

### <span data-ttu-id="d01fa-136">-ExtendPolicy</span><span class="sxs-lookup"><span data-stu-id="d01fa-136">-ExtendPolicy</span></span>
<span data-ttu-id="d01fa-137">Indique ExtendPolicy para estender um ImmutabilityPolicy existente.</span><span class="sxs-lookup"><span data-stu-id="d01fa-137">Indicate ExtendPolicy to Extend an existing ImmutabilityPolicy.</span></span>  <span data-ttu-id="d01fa-138">Depois que o ImmutabilityPolicy estiver bloqueado, ele só poderá ser estendido.</span><span class="sxs-lookup"><span data-stu-id="d01fa-138">After ImmutabilityPolicy is locked, it can only be extend.</span></span> 

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

### <span data-ttu-id="d01fa-139">-ImmutabilityPeriod</span><span class="sxs-lookup"><span data-stu-id="d01fa-139">-ImmutabilityPeriod</span></span>
<span data-ttu-id="d01fa-140">Período de imutabilidade desde a criação em dias.</span><span class="sxs-lookup"><span data-stu-id="d01fa-140">Immutability period since creation in days.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: ImmutabilityPeriodSinceCreationInDays

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d01fa-141">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d01fa-141">-InputObject</span></span>
<span data-ttu-id="d01fa-142">Nome do contêiner</span><span class="sxs-lookup"><span data-stu-id="d01fa-142">Container Name</span></span>

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

### <span data-ttu-id="d01fa-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d01fa-143">-ResourceGroupName</span></span>
<span data-ttu-id="d01fa-144">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d01fa-144">Resource Group Name.</span></span>

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

### <span data-ttu-id="d01fa-145">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="d01fa-145">-StorageAccount</span></span>
<span data-ttu-id="d01fa-146">Objeto da conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="d01fa-146">Storage account object</span></span>

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

### <span data-ttu-id="d01fa-147">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="d01fa-147">-StorageAccountName</span></span>
<span data-ttu-id="d01fa-148">Nome da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="d01fa-148">Storage Account Name.</span></span>

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

### <span data-ttu-id="d01fa-149">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d01fa-149">-Confirm</span></span>
<span data-ttu-id="d01fa-150">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d01fa-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d01fa-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d01fa-151">-WhatIf</span></span>
<span data-ttu-id="d01fa-152">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d01fa-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d01fa-153">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d01fa-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d01fa-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d01fa-154">CommonParameters</span></span>
<span data-ttu-id="d01fa-155">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d01fa-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d01fa-156">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d01fa-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d01fa-157">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d01fa-157">INPUTS</span></span>

### <span data-ttu-id="d01fa-158">System. String</span><span class="sxs-lookup"><span data-stu-id="d01fa-158">System.String</span></span>

### <span data-ttu-id="d01fa-159">Microsoft. Azure. Commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d01fa-159">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="d01fa-160">Microsoft. Azure. Commands. Management. Storage. Models. PSContainer</span><span class="sxs-lookup"><span data-stu-id="d01fa-160">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

### <span data-ttu-id="d01fa-161">Microsoft. Azure. Commands. Management. Storage. Models. PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="d01fa-161">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="d01fa-162">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d01fa-162">OUTPUTS</span></span>

### <span data-ttu-id="d01fa-163">Microsoft. Azure. Commands. Management. Storage. Models. PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="d01fa-163">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="d01fa-164">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d01fa-164">NOTES</span></span>

## <span data-ttu-id="d01fa-165">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d01fa-165">RELATED LINKS</span></span>

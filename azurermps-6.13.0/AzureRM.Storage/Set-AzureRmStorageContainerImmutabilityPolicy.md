---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/set-azurermstoragecontainerimmutabilitypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Set-AzureRmStorageContainerImmutabilityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Set-AzureRmStorageContainerImmutabilityPolicy.md
ms.openlocfilehash: 7717aaa76efba736015a1cf762c95af440b28218
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431274"
---
# <span data-ttu-id="1ab83-101">Set-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="1ab83-101">Set-AzureRmStorageContainerImmutabilityPolicy</span></span>

## <span data-ttu-id="1ab83-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1ab83-102">SYNOPSIS</span></span>
<span data-ttu-id="1ab83-103">Cria ou atualiza ImmutabilityPolicy de um contêiner de blob de armazenamento</span><span class="sxs-lookup"><span data-stu-id="1ab83-103">Creates or updates ImmutabilityPolicy of a Storage blob containers</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1ab83-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1ab83-104">SYNTAX</span></span>

### <span data-ttu-id="1ab83-105">AccountName (padrão)</span><span class="sxs-lookup"><span data-stu-id="1ab83-105">AccountName (Default)</span></span>
```
Set-AzureRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-ContainerName] <String> -ImmutabilityPeriod <Int32> [-Etag <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1ab83-106">ExtendAccountName</span><span class="sxs-lookup"><span data-stu-id="1ab83-106">ExtendAccountName</span></span>
```
Set-AzureRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-ContainerName] <String> -ImmutabilityPeriod <Int32> -Etag <String> [-ExtendPolicy]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1ab83-107">Accountobject</span><span class="sxs-lookup"><span data-stu-id="1ab83-107">AccountObject</span></span>
```
Set-AzureRmStorageContainerImmutabilityPolicy [-ContainerName] <String> -StorageAccount <PSStorageAccount>
 -ImmutabilityPeriod <Int32> [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1ab83-108">ExtendAccountObject</span><span class="sxs-lookup"><span data-stu-id="1ab83-108">ExtendAccountObject</span></span>
```
Set-AzureRmStorageContainerImmutabilityPolicy [-ContainerName] <String> -StorageAccount <PSStorageAccount>
 -ImmutabilityPeriod <Int32> -Etag <String> [-ExtendPolicy] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1ab83-109">Idcontêiner</span><span class="sxs-lookup"><span data-stu-id="1ab83-109">ContainerObject</span></span>
```
Set-AzureRmStorageContainerImmutabilityPolicy -Container <PSContainer> -ImmutabilityPeriod <Int32>
 [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1ab83-110">ExtendContainerObject</span><span class="sxs-lookup"><span data-stu-id="1ab83-110">ExtendContainerObject</span></span>
```
Set-AzureRmStorageContainerImmutabilityPolicy -Container <PSContainer> -ImmutabilityPeriod <Int32>
 -Etag <String> [-ExtendPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1ab83-111">ImmutabilityPolicyObject</span><span class="sxs-lookup"><span data-stu-id="1ab83-111">ImmutabilityPolicyObject</span></span>
```
Set-AzureRmStorageContainerImmutabilityPolicy -InputObject <PSImmutabilityPolicy> -ImmutabilityPeriod <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1ab83-112">ExtendImmutabilityPolicyObject</span><span class="sxs-lookup"><span data-stu-id="1ab83-112">ExtendImmutabilityPolicyObject</span></span>
```
Set-AzureRmStorageContainerImmutabilityPolicy -InputObject <PSImmutabilityPolicy> -ImmutabilityPeriod <Int32>
 [-ExtendPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1ab83-113">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1ab83-113">DESCRIPTION</span></span>
<span data-ttu-id="1ab83-114">O cmdlet **set-AzureRmStorageContainerImmutabilityPolicy** cria ou atualiza ImmutabilityPolicy de contêineres de blob de armazenamento</span><span class="sxs-lookup"><span data-stu-id="1ab83-114">The **Set-AzureRmStorageContainerImmutabilityPolicy** cmdlet creates or updates ImmutabilityPolicy of a Storage blob containers</span></span>

## <span data-ttu-id="1ab83-115">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1ab83-115">EXAMPLES</span></span>

### <span data-ttu-id="1ab83-116">Exemplo 1: criar ou atualizar ImmutabilityPolicy de um contêiner de blob de armazenamento com nome da conta de armazenamento e nome do contêiner</span><span class="sxs-lookup"><span data-stu-id="1ab83-116">Example 1: Create or update ImmutabilityPolicy of a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Set-AzureRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -ImmutabilityPeriod 10 
```

<span data-ttu-id="1ab83-117">Este comando cria ou atualiza ImmutabilityPolicy de um contêiner de blob de armazenamento com o nome da conta de armazenamento e o nome do contêiner.</span><span class="sxs-lookup"><span data-stu-id="1ab83-117">This command creates or updates ImmutabilityPolicy of a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="1ab83-118">Exemplo 2: estender o ImmutabilityPolicy de um contêiner de blob de armazenamento com o objeto da conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="1ab83-118">Example 2: Extend ImmutabilityPolicy of a Storage blob container, with Storage account object</span></span>
```
PS C:\>$accountObject = Get-AzureRmStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>$policy = Get-AzureRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer"
PS C:\>Set-AzureRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer" -ImmutabilityPeriod 20 -Etag $policy.Etag -ExtendPolicy
```

<span data-ttu-id="1ab83-119">Esse comando estende o ImmutabilityPolicy de um contêiner de blob de armazenamento, com objeto da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="1ab83-119">This command extend ImmutabilityPolicy of a Storage blob container, with Storage account object.</span></span> <span data-ttu-id="1ab83-120">Extend ImmutabilityPolicy só pode ser executado após o bloqueio de ImmutabilityPolicy.</span><span class="sxs-lookup"><span data-stu-id="1ab83-120">Extend ImmutabilityPolicy can only run after ImmutabilityPolicy is locked.</span></span>

### <span data-ttu-id="1ab83-121">Exemplo 3: atualizar ImmutabilityPolicyof um contêiner de blob de armazenamento</span><span class="sxs-lookup"><span data-stu-id="1ab83-121">Example 3: Update ImmutabilityPolicyof a Storage blob container</span></span> 
```
PS C:\>$containerObject = Get-AzureRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -Name "myContainer"
PS C:\>$policy = Set-AzureRmStorageContainerImmutabilityPolicy -Container $containerObject -ImmutabilityPeriod 12
PS C:\>$policy = Set-AzureRmStorageContainerImmutabilityPolicy -Container $containerObject -ImmutabilityPeriod 9 -Etag $policy.Etag
```

<span data-ttu-id="1ab83-122">Esse comando atualiza o ImmutabilityPolicy de um contêiner de blob de armazenamento com objeto de contêiner de armazenamento 2 vezes, primeiro ao ImmutabilityPeriod 12 dias sem ETag, e para ImmutabilityPeriod 9 dias com ETag.</span><span class="sxs-lookup"><span data-stu-id="1ab83-122">This command updates ImmutabilityPolicy of a Storage blob container with Storage container object 2 times, first to ImmutabilityPeriod 12 days without etag, then to ImmutabilityPeriod 9 days with etag.</span></span>

### <span data-ttu-id="1ab83-123">Exemplo 4: estender o ImmutabilityPolicy de um contêiner de blob de armazenamento com objeto ImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="1ab83-123">Example 4: Extend ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object</span></span>
```
PS C:\>Get-AzureRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" | Set-AzureRmStorageContainerImmutabilityPolicy -ImmutabilityPeriod 15 -ExtendPolicy
```

<span data-ttu-id="1ab83-124">Esse comando estende o ImmutabilityPolicy de um contêiner de blob de armazenamento, com objeto ImmutabilityPolicy.</span><span class="sxs-lookup"><span data-stu-id="1ab83-124">This command extend ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object.</span></span> <span data-ttu-id="1ab83-125">Extend ImmutabilityPolicy só pode ser executado após o bloqueio de ImmutabilityPolicy.</span><span class="sxs-lookup"><span data-stu-id="1ab83-125">Extend ImmutabilityPolicy can only run after ImmutabilityPolicy is locked.</span></span>

## <span data-ttu-id="1ab83-126">OS</span><span class="sxs-lookup"><span data-stu-id="1ab83-126">PARAMETERS</span></span>

### <span data-ttu-id="1ab83-127">-Contêiner</span><span class="sxs-lookup"><span data-stu-id="1ab83-127">-Container</span></span>
<span data-ttu-id="1ab83-128">Objeto contêiner de armazenamento</span><span class="sxs-lookup"><span data-stu-id="1ab83-128">Storage container object</span></span>

```yaml
Type: PSContainer
Parameter Sets: ContainerObject, ExtendContainerObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1ab83-129">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="1ab83-129">-ContainerName</span></span>
<span data-ttu-id="1ab83-130">Nome do contêiner</span><span class="sxs-lookup"><span data-stu-id="1ab83-130">Container Name</span></span>

```yaml
Type: String
Parameter Sets: AccountName, ExtendAccountName, AccountObject, ExtendAccountObject
Aliases: N

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1ab83-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ab83-131">-DefaultProfile</span></span>
<span data-ttu-id="1ab83-132">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1ab83-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1ab83-133">-ETag</span><span class="sxs-lookup"><span data-stu-id="1ab83-133">-Etag</span></span>
<span data-ttu-id="1ab83-134">ETag da política de imutabilidade.</span><span class="sxs-lookup"><span data-stu-id="1ab83-134">Immutability policy etag.</span></span> <span data-ttu-id="1ab83-135">Se-ExtendPolicy não for especificado, ETag será opcional; else ETag é necessário.</span><span class="sxs-lookup"><span data-stu-id="1ab83-135">If -ExtendPolicy is not specified, Etag is optional; else Etag is required.</span></span>

```yaml
Type: String
Parameter Sets: AccountName, AccountObject, ContainerObject
Aliases: IfMatch

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ExtendAccountName, ExtendAccountObject, ExtendContainerObject
Aliases: IfMatch

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ab83-136">-ExtendPolicy</span><span class="sxs-lookup"><span data-stu-id="1ab83-136">-ExtendPolicy</span></span>
<span data-ttu-id="1ab83-137">Indique ExtendPolicy para estender um ImmutabilityPolicy existente.</span><span class="sxs-lookup"><span data-stu-id="1ab83-137">Indicate ExtendPolicy to Extend an existing ImmutabilityPolicy.</span></span>  <span data-ttu-id="1ab83-138">Depois que o ImmutabilityPolicy estiver bloqueado, ele só poderá ser estendido.</span><span class="sxs-lookup"><span data-stu-id="1ab83-138">After ImmutabilityPolicy is locked, it can only be extend.</span></span> 

```yaml
Type: SwitchParameter
Parameter Sets: ExtendAccountName, ExtendAccountObject, ExtendContainerObject, ExtendImmutabilityPolicyObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ab83-139">-ImmutabilityPeriod</span><span class="sxs-lookup"><span data-stu-id="1ab83-139">-ImmutabilityPeriod</span></span>
<span data-ttu-id="1ab83-140">Período de imutabilidade desde a criação em dias.</span><span class="sxs-lookup"><span data-stu-id="1ab83-140">Immutability period since creation in days.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: ImmutabilityPeriodSinceCreationInDays

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ab83-141">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1ab83-141">-InputObject</span></span>
<span data-ttu-id="1ab83-142">Nome do contêiner</span><span class="sxs-lookup"><span data-stu-id="1ab83-142">Container Name</span></span>

```yaml
Type: PSImmutabilityPolicy
Parameter Sets: ImmutabilityPolicyObject, ExtendImmutabilityPolicyObject
Aliases: ImmutabilityPolicy

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1ab83-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ab83-143">-ResourceGroupName</span></span>
<span data-ttu-id="1ab83-144">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="1ab83-144">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: AccountName, ExtendAccountName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ab83-145">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="1ab83-145">-StorageAccount</span></span>
<span data-ttu-id="1ab83-146">Objeto da conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="1ab83-146">Storage account object</span></span>

```yaml
Type: PSStorageAccount
Parameter Sets: AccountObject, ExtendAccountObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1ab83-147">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="1ab83-147">-StorageAccountName</span></span>
<span data-ttu-id="1ab83-148">Nome da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="1ab83-148">Storage Account Name.</span></span>

```yaml
Type: String
Parameter Sets: AccountName, ExtendAccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ab83-149">-Confirme</span><span class="sxs-lookup"><span data-stu-id="1ab83-149">-Confirm</span></span>
<span data-ttu-id="1ab83-150">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1ab83-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1ab83-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1ab83-151">-WhatIf</span></span>
<span data-ttu-id="1ab83-152">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1ab83-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1ab83-153">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1ab83-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1ab83-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ab83-154">CommonParameters</span></span>
<span data-ttu-id="1ab83-155">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ab83-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ab83-156">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ab83-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ab83-157">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1ab83-157">INPUTS</span></span>

### <span data-ttu-id="1ab83-158">System. String</span><span class="sxs-lookup"><span data-stu-id="1ab83-158">System.String</span></span>
<span data-ttu-id="1ab83-159">Microsoft. Azure. Commands. Management. Storage. Models. PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="1ab83-159">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="1ab83-160">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1ab83-160">OUTPUTS</span></span>

### <span data-ttu-id="1ab83-161">Microsoft. Azure. Commands. Management. Storage. Models. PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="1ab83-161">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="1ab83-162">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1ab83-162">NOTES</span></span>

## <span data-ttu-id="1ab83-163">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1ab83-163">RELATED LINKS</span></span>


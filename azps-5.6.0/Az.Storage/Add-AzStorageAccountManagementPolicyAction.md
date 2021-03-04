---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/Az.storage/add-Azstorageaccountmanagementpolicyaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Add-AzStorageAccountManagementPolicyAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Add-AzStorageAccountManagementPolicyAction.md
ms.openlocfilehash: 65bce04c3df14a6b9dc4397d47577d0642746c45
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888409"
---
# <span data-ttu-id="aaf1d-101">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="aaf1d-101">Add-AzStorageAccountManagementPolicyAction</span></span>

## <span data-ttu-id="aaf1d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aaf1d-102">SYNOPSIS</span></span>
<span data-ttu-id="aaf1d-103">Adiciona uma ação ao objeto ManagementPolicy Action Group de entrada ou cria um objeto ManagementPolicy Action Group com a ação.</span><span class="sxs-lookup"><span data-stu-id="aaf1d-103">Adds an action to the input ManagementPolicy Action Group object, or creates a ManagementPolicy Action Group object with the action.</span></span> <span data-ttu-id="aaf1d-104">O objeto pode ser usado em New-AzStorageAccountManagementPolicyRule.</span><span class="sxs-lookup"><span data-stu-id="aaf1d-104">The object can be used in New-AzStorageAccountManagementPolicyRule.</span></span>

## <span data-ttu-id="aaf1d-105">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="aaf1d-105">SYNTAX</span></span>

### <span data-ttu-id="aaf1d-106">BaseBlob (Padrão)</span><span class="sxs-lookup"><span data-stu-id="aaf1d-106">BaseBlob (Default)</span></span>
```
Add-AzStorageAccountManagementPolicyAction -BaseBlobAction <String> -DaysAfterModificationGreaterThan <Int32>
 [-InputObject <PSManagementPolicyActionGroup>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aaf1d-107">Instantâneo</span><span class="sxs-lookup"><span data-stu-id="aaf1d-107">Snapshot</span></span>
```
Add-AzStorageAccountManagementPolicyAction -SnapshotAction <String> -DaysAfterCreationGreaterThan <Int32>
 [-InputObject <PSManagementPolicyActionGroup>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aaf1d-108">BlobVersion</span><span class="sxs-lookup"><span data-stu-id="aaf1d-108">BlobVersion</span></span>
```
Add-AzStorageAccountManagementPolicyAction -BlobVersionAction <String> -DaysAfterCreationGreaterThan <Int32>
 [-InputObject <PSManagementPolicyActionGroup>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aaf1d-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="aaf1d-109">DESCRIPTION</span></span>
<span data-ttu-id="aaf1d-110">O cmdlet **Add-AzStorageAccountManagementPolicyAction** adiciona uma ação ao objeto ManagementPolicy Action Group de entrada ou cria um objeto ManagementPolicy Action Group com a ação.</span><span class="sxs-lookup"><span data-stu-id="aaf1d-110">The **Add-AzStorageAccountManagementPolicyAction** cmdlet adds an action to the input ManagementPolicy Action Group object, or creates a ManagementPolicy Action Group object with the action.</span></span>

## <span data-ttu-id="aaf1d-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="aaf1d-111">EXAMPLES</span></span>

### <span data-ttu-id="aaf1d-112">Exemplo 1: cria um objeto ManagementPolicy Action Group com 4 ações, adicione-o a uma regra de política de gerenciamento e desmarcar uma conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="aaf1d-112">Example 1: Creates a ManagementPolicy Action Group object with 4 actions, then add it to a management policy rule and set to a Storage account</span></span>
```
PS C:\>$action = Add-AzStorageAccountManagementPolicyAction -BaseBlobAction Delete -daysAfterModificationGreaterThan 100
PS C:\>$action = Add-AzStorageAccountManagementPolicyAction -BaseBlobAction TierToArchive -daysAfterModificationGreaterThan 50  -InputObject $action
PS C:\>$action = Add-AzStorageAccountManagementPolicyAction -BaseBlobAction TierToCool -daysAfterModificationGreaterThan 30 -InputObject $action
PS C:\>$action = Add-AzStorageAccountManagementPolicyAction -SnapshotAction Delete -daysAfterCreationGreaterThan 100 -InputObject $action
PS C:\>$action 

BaseBlob.TierToCool.DaysAfterModificationGreaterThan    : 30
BaseBlob.TierToArchive.DaysAfterModificationGreaterThan : 50
BaseBlob.Delete.DaysAfterModificationGreaterThan        : 100
Snapshot.TierToCool.DaysAfterCreationGreaterThan        : 
Snapshot.TierToArchive.DaysAfterCreationGreaterThan     : 
Snapshot.Delete.DaysAfterCreationGreaterThan            : 100
Version.TierToCool.DaysAfterCreationGreaterThan         : 
Version.TierToArchive.DaysAfterCreationGreaterThan      : 
Version.Delete.DaysAfterCreationGreaterThan             : 

PS C:\>$filter = New-AzStorageAccountManagementPolicyFilter
PS C:\>$rule = New-AzStorageAccountManagementPolicyRule -Name Test -Action $action -Filter $filter
PS C:\>$policy = Set-AzStorageAccountManagementPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -Rule $rule
```

<span data-ttu-id="aaf1d-113">O primeiro comando cria um objeto ManagementPolicy Action Group, os três comandos a seguir adicionam 3 ações ao objeto.</span><span class="sxs-lookup"><span data-stu-id="aaf1d-113">The first command create a ManagementPolicy Action Group object, the following 3 commands add 3 actions to the object.</span></span> <span data-ttu-id="aaf1d-114">Em seguida, adicione-a a uma regra de política de gerenciamento e desmarcar uma conta de Armazenamento.</span><span class="sxs-lookup"><span data-stu-id="aaf1d-114">Then add it to a management policy rule and set to a Storage account.</span></span>

### <span data-ttu-id="aaf1d-115">Exemplo 2: cria um objeto ManagementPolicy Action Group com 6 ações na versão de instantâneo e blob, em seguida, adicione-a a uma regra de política de gerenciamento e desmarcar uma conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="aaf1d-115">Example 2: Creates a ManagementPolicy Action Group object with 6 actions on snapshot and blob version, then add it to a management policy rule and set to a Storage account</span></span>
```
PS C:\> $action = Add-AzStorageAccountManagementPolicyAction  -SnapshotAction Delete -daysAfterCreationGreaterThan 40
PS C:\> $action = Add-AzStorageAccountManagementPolicyAction -InputObject $action -SnapshotAction TierToArchive -daysAfterCreationGreaterThan 50
PS C:\> $action = Add-AzStorageAccountManagementPolicyAction -InputObject $action -SnapshotAction TierToCool -daysAfterCreationGreaterThan 60
PS C:\> $action = Add-AzStorageAccountManagementPolicyAction -InputObject $action -BlobVersionAction Delete -daysAfterCreationGreaterThan 70
PS C:\> $action = Add-AzStorageAccountManagementPolicyAction -InputObject $action -BlobVersionAction TierToArchive -daysAfterCreationGreaterThan 80
PS C:\> $action = Add-AzStorageAccountManagementPolicyAction -InputObject $action -BlobVersionAction TierToCool -daysAfterCreationGreaterThan 90
PS C:\> $action

BaseBlob.TierToCool.DaysAfterModificationGreaterThan    : 
BaseBlob.TierToArchive.DaysAfterModificationGreaterThan : 
BaseBlob.Delete.DaysAfterModificationGreaterThan        : 
Snapshot.TierToCool.DaysAfterCreationGreaterThan        : 60
Snapshot.TierToArchive.DaysAfterCreationGreaterThan     : 50
Snapshot.Delete.DaysAfterCreationGreaterThan            : 40
Version.TierToCool.DaysAfterCreationGreaterThan         : 90
Version.TierToArchive.DaysAfterCreationGreaterThan      : 80
Version.Delete.DaysAfterCreationGreaterThan             : 70

PS C:\>$filter = New-AzStorageAccountManagementPolicyFilter
PS C:\>$rule = New-AzStorageAccountManagementPolicyRule -Name Test -Action $action -Filter $filter
PS C:\>$policy = Set-AzStorageAccountManagementPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -Rule $rule
```

<span data-ttu-id="aaf1d-116">O primeiro comando cria um objeto ManagementPolicy Action Group, os 5 comandos a seguir adicionam 5 ações em instantâneo e versão de blob ao objeto.</span><span class="sxs-lookup"><span data-stu-id="aaf1d-116">The first command create a ManagementPolicy Action Group object, the following 5 commands add 5 actions on snapshot and blob version to the object.</span></span> <span data-ttu-id="aaf1d-117">Em seguida, adicione-a a uma regra de política de gerenciamento e desmarcar uma conta de Armazenamento.</span><span class="sxs-lookup"><span data-stu-id="aaf1d-117">Then add it to a management policy rule and set to a Storage account.</span></span>

## <span data-ttu-id="aaf1d-118">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="aaf1d-118">PARAMETERS</span></span>

### <span data-ttu-id="aaf1d-119">-BaseBlobAction</span><span class="sxs-lookup"><span data-stu-id="aaf1d-119">-BaseBlobAction</span></span>
<span data-ttu-id="aaf1d-120">A ação de política de gerenciamento para baseblob.</span><span class="sxs-lookup"><span data-stu-id="aaf1d-120">The management policy action for baseblob.</span></span>

```yaml
Type: System.String
Parameter Sets: BaseBlob
Aliases:
Accepted values: Delete, TierToArchive, TierToCool

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aaf1d-121">-BlobVersionAction</span><span class="sxs-lookup"><span data-stu-id="aaf1d-121">-BlobVersionAction</span></span>
<span data-ttu-id="aaf1d-122">A ação de política de gerenciamento para a versão de blob.</span><span class="sxs-lookup"><span data-stu-id="aaf1d-122">The management policy action for blob version.</span></span>

```yaml
Type: System.String
Parameter Sets: BlobVersion
Aliases:
Accepted values: Delete, TierToArchive, TierToCool

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aaf1d-123">-DaysAfterCreationGreaterThan</span><span class="sxs-lookup"><span data-stu-id="aaf1d-123">-DaysAfterCreationGreaterThan</span></span>
<span data-ttu-id="aaf1d-124">Valor inteiro que indica a idade em dias após a criação.</span><span class="sxs-lookup"><span data-stu-id="aaf1d-124">Integer value indicating the age in days after creation.</span></span>

```yaml
Type: System.Int32
Parameter Sets: Snapshot, BlobVersion
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aaf1d-125">-DaysAfterModificationGreaterThan</span><span class="sxs-lookup"><span data-stu-id="aaf1d-125">-DaysAfterModificationGreaterThan</span></span>
<span data-ttu-id="aaf1d-126">Valor inteiro que indica a idade em dias após a última modificação.</span><span class="sxs-lookup"><span data-stu-id="aaf1d-126">Integer value indicating the age in days after last modification.</span></span>

```yaml
Type: System.Int32
Parameter Sets: BaseBlob
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aaf1d-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aaf1d-127">-DefaultProfile</span></span>
<span data-ttu-id="aaf1d-128">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="aaf1d-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aaf1d-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="aaf1d-129">-InputObject</span></span>
<span data-ttu-id="aaf1d-130">Se o objeto ManagementPolicy Action for de entrada, definirá a ação como o objeto de ação de entrada.</span><span class="sxs-lookup"><span data-stu-id="aaf1d-130">If input the ManagementPolicy Action object, will set the action to the input action object.</span></span>
<span data-ttu-id="aaf1d-131">Se não for a entrada, criará um novo objeto de ação.</span><span class="sxs-lookup"><span data-stu-id="aaf1d-131">If not input, will create a new action object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyActionGroup
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="aaf1d-132">-SnapshotAction</span><span class="sxs-lookup"><span data-stu-id="aaf1d-132">-SnapshotAction</span></span>
<span data-ttu-id="aaf1d-133">A ação de política de gerenciamento para instantâneo.</span><span class="sxs-lookup"><span data-stu-id="aaf1d-133">The management policy action for snapshot.</span></span>

```yaml
Type: System.String
Parameter Sets: Snapshot
Aliases:
Accepted values: Delete, TierToArchive, TierToCool

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aaf1d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aaf1d-134">CommonParameters</span></span>
<span data-ttu-id="aaf1d-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aaf1d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aaf1d-136">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aaf1d-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aaf1d-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="aaf1d-137">INPUTS</span></span>

### <span data-ttu-id="aaf1d-138">Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyActionGroup</span><span class="sxs-lookup"><span data-stu-id="aaf1d-138">Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyActionGroup</span></span>

## <span data-ttu-id="aaf1d-139">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="aaf1d-139">OUTPUTS</span></span>

### <span data-ttu-id="aaf1d-140">Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyActionGroup</span><span class="sxs-lookup"><span data-stu-id="aaf1d-140">Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyActionGroup</span></span>

## <span data-ttu-id="aaf1d-141">NOTES</span><span class="sxs-lookup"><span data-stu-id="aaf1d-141">NOTES</span></span>

## <span data-ttu-id="aaf1d-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="aaf1d-142">RELATED LINKS</span></span>

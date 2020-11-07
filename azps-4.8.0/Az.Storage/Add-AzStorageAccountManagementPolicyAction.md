---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storage/add-Azstorageaccountmanagementpolicyaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Add-AzStorageAccountManagementPolicyAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Add-AzStorageAccountManagementPolicyAction.md
ms.openlocfilehash: ed876765e3b5eb9d306847958772d9205758f5d6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93956153"
---
# <span data-ttu-id="58836-101">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="58836-101">Add-AzStorageAccountManagementPolicyAction</span></span>

## <span data-ttu-id="58836-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="58836-102">SYNOPSIS</span></span>
<span data-ttu-id="58836-103">Adiciona uma ação ao objeto de grupo de ação ManagementPolicy de entrada ou cria um objeto de grupo de ação ManagementPolicy com a ação.</span><span class="sxs-lookup"><span data-stu-id="58836-103">Adds an action to the input ManagementPolicy Action Group object, or creates a ManagementPolicy Action Group object with the action.</span></span> <span data-ttu-id="58836-104">O objeto pode ser usado em New-AzStorageAccountManagementPolicyRule.</span><span class="sxs-lookup"><span data-stu-id="58836-104">The object can be used in New-AzStorageAccountManagementPolicyRule.</span></span>

## <span data-ttu-id="58836-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="58836-105">SYNTAX</span></span>

### <span data-ttu-id="58836-106">BaseBlob (padrão)</span><span class="sxs-lookup"><span data-stu-id="58836-106">BaseBlob (Default)</span></span>
```
Add-AzStorageAccountManagementPolicyAction -BaseBlobAction <String> -DaysAfterModificationGreaterThan <Int32>
 [-InputObject <PSManagementPolicyActionGroup>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="58836-107">Captura</span><span class="sxs-lookup"><span data-stu-id="58836-107">Snapshot</span></span>
```
Add-AzStorageAccountManagementPolicyAction -SnapshotAction <String> -DaysAfterCreationGreaterThan <Int32>
 [-InputObject <PSManagementPolicyActionGroup>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="58836-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="58836-108">DESCRIPTION</span></span>
<span data-ttu-id="58836-109">O cmdlet **Add-AzStorageAccountManagementPolicyAction** adiciona uma ação ao objeto de grupo de ação ManagementPolicy de entrada ou cria um objeto de grupo de ação ManagementPolicy com a ação.</span><span class="sxs-lookup"><span data-stu-id="58836-109">The **Add-AzStorageAccountManagementPolicyAction** cmdlet adds an action to the input ManagementPolicy Action Group object, or creates a ManagementPolicy Action Group object with the action.</span></span>

## <span data-ttu-id="58836-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="58836-110">EXAMPLES</span></span>

### <span data-ttu-id="58836-111">Exemplo 1: cria um objeto de grupo de ação ManagementPolicy com 4 ações e, em seguida, adiciona-o a uma regra de política de gerenciamento e definido como uma conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="58836-111">Example 1: Creates a ManagementPolicy Action Group object with 4 actions, then add it to a management policy rule and set to a Storage account</span></span>
```
PS C:\>$action = Add-AzStorageAccountManagementPolicyAction -BaseBlobAction Delete -daysAfterModificationGreaterThan 100
PS C:\>$action = Add-AzStorageAccountManagementPolicyAction -BaseBlobAction TierToArchive -daysAfterModificationGreaterThan 50  -InputObject $action
PS C:\>$action = Add-AzStorageAccountManagementPolicyAction -BaseBlobAction TierToCool -daysAfterModificationGreaterThan 30 -InputObject $action
PS C:\>$action = Add-AzStorageAccountManagementPolicyAction -SnapshotAction Delete -daysAfterCreationGreaterThan 100 -InputObject $action
PS C:\>$action 

BaseBlob.TierToCool.DaysAfterModificationGreaterThan    : 30
BaseBlob.TierToArchive.DaysAfterModificationGreaterThan : 50
BaseBlob.Delete.DaysAfterModificationGreaterThan        : 100
Snapshot.Delete.DaysAfterCreationGreaterThan            : 100

PS C:\>$filter = New-AzStorageAccountManagementPolicyFilter
PS C:\>$rule = New-AzStorageAccountManagementPolicyRule -Name Test -Action $action -Filter $filter
PS C:\>$policy = Set-AzStorageAccountManagementPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -Rule $rule
```

<span data-ttu-id="58836-112">O primeiro comando cria um objeto de grupo de ação ManagementPolicy, os seguintes comandos 3 adicionam 3 ações ao objeto.</span><span class="sxs-lookup"><span data-stu-id="58836-112">The first command create a ManagementPolicy Action Group object, the following 3 commands add 3 actions to the object.</span></span> <span data-ttu-id="58836-113">Em seguida, adicione-o a uma regra de política de gerenciamento e defina-o como uma conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="58836-113">Then add it to a management policy rule and set to a Storage account.</span></span>

## <span data-ttu-id="58836-114">OS</span><span class="sxs-lookup"><span data-stu-id="58836-114">PARAMETERS</span></span>

### <span data-ttu-id="58836-115">-BaseBlobAction</span><span class="sxs-lookup"><span data-stu-id="58836-115">-BaseBlobAction</span></span>
<span data-ttu-id="58836-116">A ação da política de gerenciamento para baseblob.</span><span class="sxs-lookup"><span data-stu-id="58836-116">The management policy action for baseblob.</span></span>

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

### <span data-ttu-id="58836-117">-DaysAfterCreationGreaterThan</span><span class="sxs-lookup"><span data-stu-id="58836-117">-DaysAfterCreationGreaterThan</span></span>
<span data-ttu-id="58836-118">Valor inteiro que indica a idade em dias após a criação.</span><span class="sxs-lookup"><span data-stu-id="58836-118">Integer value indicating the age in days after creation.</span></span>

```yaml
Type: System.Int32
Parameter Sets: Snapshot
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58836-119">-DaysAfterModificationGreaterThan</span><span class="sxs-lookup"><span data-stu-id="58836-119">-DaysAfterModificationGreaterThan</span></span>
<span data-ttu-id="58836-120">Valor inteiro que indica a idade em dias após a última modificação.</span><span class="sxs-lookup"><span data-stu-id="58836-120">Integer value indicating the age in days after last modification.</span></span>

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

### <span data-ttu-id="58836-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58836-121">-DefaultProfile</span></span>
<span data-ttu-id="58836-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="58836-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="58836-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="58836-123">-InputObject</span></span>
<span data-ttu-id="58836-124">Se inserir o objeto de ação ManagementPolicy, a ação será definida como o objeto de ação de entrada.</span><span class="sxs-lookup"><span data-stu-id="58836-124">If input the ManagementPolicy Action object, will set the action to the input action object.</span></span>
<span data-ttu-id="58836-125">Se não for inserido, criará um novo objeto Action.</span><span class="sxs-lookup"><span data-stu-id="58836-125">If not input, will create a new action object.</span></span>

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

### <span data-ttu-id="58836-126">-Instantâneoaction</span><span class="sxs-lookup"><span data-stu-id="58836-126">-SnapshotAction</span></span>
<span data-ttu-id="58836-127">A ação da política de gerenciamento para instantâneo.</span><span class="sxs-lookup"><span data-stu-id="58836-127">The management policy action for snapshot.</span></span>

```yaml
Type: System.String
Parameter Sets: Snapshot
Aliases:
Accepted values: Delete

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58836-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58836-128">CommonParameters</span></span>
<span data-ttu-id="58836-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58836-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58836-130">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="58836-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58836-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="58836-131">INPUTS</span></span>

### <span data-ttu-id="58836-132">Microsoft. Azure. Commands. Management. Storage. Models. PSManagementPolicyActionGroup</span><span class="sxs-lookup"><span data-stu-id="58836-132">Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyActionGroup</span></span>

## <span data-ttu-id="58836-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="58836-133">OUTPUTS</span></span>

### <span data-ttu-id="58836-134">Microsoft. Azure. Commands. Management. Storage. Models. PSManagementPolicyActionGroup</span><span class="sxs-lookup"><span data-stu-id="58836-134">Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyActionGroup</span></span>

## <span data-ttu-id="58836-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="58836-135">NOTES</span></span>

## <span data-ttu-id="58836-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="58836-136">RELATED LINKS</span></span>

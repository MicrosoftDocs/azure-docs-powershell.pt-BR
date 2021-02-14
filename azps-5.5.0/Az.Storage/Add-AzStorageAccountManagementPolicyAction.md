---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storage/add-Azstorageaccountmanagementpolicyaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Add-AzStorageAccountManagementPolicyAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Add-AzStorageAccountManagementPolicyAction.md
ms.openlocfilehash: ed876765e3b5eb9d306847958772d9205758f5d6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100110882"
---
# <span data-ttu-id="b5754-101">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="b5754-101">Add-AzStorageAccountManagementPolicyAction</span></span>

## <span data-ttu-id="b5754-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b5754-102">SYNOPSIS</span></span>
<span data-ttu-id="b5754-103">Adiciona uma ação ao objeto de entrada Grupo de Ação ManagementPolicy ou cria um objeto grupo de ações ManagementPolicy com a ação.</span><span class="sxs-lookup"><span data-stu-id="b5754-103">Adds an action to the input ManagementPolicy Action Group object, or creates a ManagementPolicy Action Group object with the action.</span></span> <span data-ttu-id="b5754-104">O objeto pode ser usado no New-AzStorageAccountManagementPolicyRule.</span><span class="sxs-lookup"><span data-stu-id="b5754-104">The object can be used in New-AzStorageAccountManagementPolicyRule.</span></span>

## <span data-ttu-id="b5754-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b5754-105">SYNTAX</span></span>

### <span data-ttu-id="b5754-106">BaseB ltd (Padrão)</span><span class="sxs-lookup"><span data-stu-id="b5754-106">BaseBlob (Default)</span></span>
```
Add-AzStorageAccountManagementPolicyAction -BaseBlobAction <String> -DaysAfterModificationGreaterThan <Int32>
 [-InputObject <PSManagementPolicyActionGroup>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b5754-107">Instantâneo</span><span class="sxs-lookup"><span data-stu-id="b5754-107">Snapshot</span></span>
```
Add-AzStorageAccountManagementPolicyAction -SnapshotAction <String> -DaysAfterCreationGreaterThan <Int32>
 [-InputObject <PSManagementPolicyActionGroup>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b5754-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="b5754-108">DESCRIPTION</span></span>
<span data-ttu-id="b5754-109">O cmdlet **Add-AzStorageAccountManagementPolicyAction** adiciona uma ação ao objeto de grupo de ações ManagementPolicy de entrada ou cria um objeto grupo de ações ManagementPolicy com a ação.</span><span class="sxs-lookup"><span data-stu-id="b5754-109">The **Add-AzStorageAccountManagementPolicyAction** cmdlet adds an action to the input ManagementPolicy Action Group object, or creates a ManagementPolicy Action Group object with the action.</span></span>

## <span data-ttu-id="b5754-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="b5754-110">EXAMPLES</span></span>

### <span data-ttu-id="b5754-111">Exemplo 1: cria um objeto grupo de ações ManagementPolicy com 4 ações e, em seguida, adiciona-o a uma regra de política de gerenciamento e definido como uma conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="b5754-111">Example 1: Creates a ManagementPolicy Action Group object with 4 actions, then add it to a management policy rule and set to a Storage account</span></span>
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

<span data-ttu-id="b5754-112">O primeiro comando cria um objeto grupo de ações ManagementPolicy, os 3 comandos a seguir adicionam 3 ações ao objeto.</span><span class="sxs-lookup"><span data-stu-id="b5754-112">The first command create a ManagementPolicy Action Group object, the following 3 commands add 3 actions to the object.</span></span> <span data-ttu-id="b5754-113">Em seguida, adicione-a a uma regra de política de gerenciamento e de definida como uma conta de Armazenamento.</span><span class="sxs-lookup"><span data-stu-id="b5754-113">Then add it to a management policy rule and set to a Storage account.</span></span>

## <span data-ttu-id="b5754-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b5754-114">PARAMETERS</span></span>

### <span data-ttu-id="b5754-115">-BaseB ltdaction</span><span class="sxs-lookup"><span data-stu-id="b5754-115">-BaseBlobAction</span></span>
<span data-ttu-id="b5754-116">A ação de política de gerenciamento para baseblab.</span><span class="sxs-lookup"><span data-stu-id="b5754-116">The management policy action for baseblob.</span></span>

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

### <span data-ttu-id="b5754-117">-DaysAfterCreationGreaterThan</span><span class="sxs-lookup"><span data-stu-id="b5754-117">-DaysAfterCreationGreaterThan</span></span>
<span data-ttu-id="b5754-118">Valor inteiro indicando a idade em dias após a criação.</span><span class="sxs-lookup"><span data-stu-id="b5754-118">Integer value indicating the age in days after creation.</span></span>

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

### <span data-ttu-id="b5754-119">-DaysAfterModificationGreaterThan</span><span class="sxs-lookup"><span data-stu-id="b5754-119">-DaysAfterModificationGreaterThan</span></span>
<span data-ttu-id="b5754-120">Valor inteiro indicando a idade em dias após a última modificação.</span><span class="sxs-lookup"><span data-stu-id="b5754-120">Integer value indicating the age in days after last modification.</span></span>

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

### <span data-ttu-id="b5754-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5754-121">-DefaultProfile</span></span>
<span data-ttu-id="b5754-122">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b5754-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b5754-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b5754-123">-InputObject</span></span>
<span data-ttu-id="b5754-124">Se você inserir o objeto ação ManagementPolicy, definirá a ação como o objeto de ação de entrada.</span><span class="sxs-lookup"><span data-stu-id="b5754-124">If input the ManagementPolicy Action object, will set the action to the input action object.</span></span>
<span data-ttu-id="b5754-125">Se não for de entrada, criará um novo objeto de ação.</span><span class="sxs-lookup"><span data-stu-id="b5754-125">If not input, will create a new action object.</span></span>

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

### <span data-ttu-id="b5754-126">-InstantâneoAction</span><span class="sxs-lookup"><span data-stu-id="b5754-126">-SnapshotAction</span></span>
<span data-ttu-id="b5754-127">A ação de política de gerenciamento para instantâneo.</span><span class="sxs-lookup"><span data-stu-id="b5754-127">The management policy action for snapshot.</span></span>

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

### <span data-ttu-id="b5754-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5754-128">CommonParameters</span></span>
<span data-ttu-id="b5754-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5754-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5754-130">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5754-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5754-131">Entradas</span><span class="sxs-lookup"><span data-stu-id="b5754-131">INPUTS</span></span>

### <span data-ttu-id="b5754-132">Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyActionGroup</span><span class="sxs-lookup"><span data-stu-id="b5754-132">Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyActionGroup</span></span>

## <span data-ttu-id="b5754-133">Saídas</span><span class="sxs-lookup"><span data-stu-id="b5754-133">OUTPUTS</span></span>

### <span data-ttu-id="b5754-134">Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyActionGroup</span><span class="sxs-lookup"><span data-stu-id="b5754-134">Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyActionGroup</span></span>

## <span data-ttu-id="b5754-135">Notas</span><span class="sxs-lookup"><span data-stu-id="b5754-135">NOTES</span></span>

## <span data-ttu-id="b5754-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b5754-136">RELATED LINKS</span></span>

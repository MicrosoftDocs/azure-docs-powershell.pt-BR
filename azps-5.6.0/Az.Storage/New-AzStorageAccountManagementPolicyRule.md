---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/Az.storage/new-Azstorageaccountmanagementpolicyrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountManagementPolicyRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountManagementPolicyRule.md
ms.openlocfilehash: 73606a2af9ff0c5e948d407dd5da1f21df5d14b6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891979"
---
# <span data-ttu-id="fcf6a-101">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="fcf6a-101">New-AzStorageAccountManagementPolicyRule</span></span>

## <span data-ttu-id="fcf6a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fcf6a-102">SYNOPSIS</span></span>
<span data-ttu-id="fcf6a-103">Cria um objeto de regra ManagementPolicy, que pode ser usado em Set-AzStorageAccountManagementPolicy.</span><span class="sxs-lookup"><span data-stu-id="fcf6a-103">Creates a ManagementPolicy rule object, which can be used in Set-AzStorageAccountManagementPolicy.</span></span>

## <span data-ttu-id="fcf6a-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="fcf6a-104">SYNTAX</span></span>

```
New-AzStorageAccountManagementPolicyRule [-Name] <String> [-Disabled] -Action <PSManagementPolicyActionGroup>
 [-Filter <PSManagementPolicyRuleFilter>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fcf6a-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="fcf6a-105">DESCRIPTION</span></span>
<span data-ttu-id="fcf6a-106">O cmdlet **New-AzStorageAccountManagementPolicyRule** cria um objeto de regra ManagementPolicy, que pode ser usado em Set-AzStorageAccountManagementPolicy.</span><span class="sxs-lookup"><span data-stu-id="fcf6a-106">The **New-AzStorageAccountManagementPolicyRule** cmdlet creates a ManagementPolicy rule object, which can be used in Set-AzStorageAccountManagementPolicy.</span></span>

## <span data-ttu-id="fcf6a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fcf6a-107">EXAMPLES</span></span>

### <span data-ttu-id="fcf6a-108">Exemplo 1: cria um objeto de regra ManagementPolicy e, em seguida, definido como uma conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="fcf6a-108">Example 1: Creates a ManagementPolicy rule object, then set to a Storage Account</span></span>
```
PS C:\>$action = Add-AzStorageAccountManagementPolicyAction -BaseBlobAction Delete -daysAfterModificationGreaterThan 100
PS C:\>$action = Add-AzStorageAccountManagementPolicyAction -BaseBlobAction TierToArchive -daysAfterModificationGreaterThan 50  -InputObject $action
PS C:\>$action = Add-AzStorageAccountManagementPolicyAction -BaseBlobAction TierToCool -daysAfterModificationGreaterThan 30 -InputObject $action
PS C:\>$action = Add-AzStorageAccountManagementPolicyAction -SnapshotAction Delete -daysAfterCreationGreaterThan 100 -InputObject $action

PS C:\>$filter = New-AzStorageAccountManagementPolicyFilter -PrefixMatch blobprefix1,blobprefix2

PS C:\>$rule = New-AzStorageAccountManagementPolicyRule -Name rule1 -Action $action -Filter $filter
PS C:\>$rule

Enabled    : True
Name       : rule1
Definition : {
                 "Actions":  {
                                 "BaseBlob":  {
                                                  "TierToCool":  {
                                                                     "DaysAfterModificationGreaterThan":  30
                                                                 },
                                                  "TierToArchive":  {
                                                                        "DaysAfterModificationGreaterThan":  50
                                                                    },
                                                  "Delete":  {
                                                                 "DaysAfterModificationGreaterThan":  100
                                                             }
                                              },
                                 "Snapshot":  {
                                                  "Delete":  {
                                                                 "DaysAfterCreationGreaterThan":  100
                                                             }
                                              }
                             },
                 "Filters":  {
                                 "PrefixMatch":  [
                                                     "blobprefix1",
                                                     "blobprefix2"
                                                 ],
                                 "BlobTypes":  [
                                                   "blockBlob"
                                               ]
                             }
             }

PS C:\>$policy = Set-AzStorageAccountManagementPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -Rule $rule
```

<span data-ttu-id="fcf6a-109">Este comando cria um objeto de regra ManagementPolicy, com um objeto de grupo de ação ManagementPolicy contém 4 ações, um objeto de filtro de regra ManagementPolicy e, em seguida, desarmá-lo como uma Conta de Armazenamento.</span><span class="sxs-lookup"><span data-stu-id="fcf6a-109">This command create a ManagementPolicy rule object, with a ManagementPolicy action group object contains 4 actions, a ManagementPolicy rule filter object, then set the rule to a Storage Account.</span></span>

## <span data-ttu-id="fcf6a-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="fcf6a-110">PARAMETERS</span></span>

### <span data-ttu-id="fcf6a-111">-Action</span><span class="sxs-lookup"><span data-stu-id="fcf6a-111">-Action</span></span>
<span data-ttu-id="fcf6a-112">Um objeto que define o conjunto de ações.</span><span class="sxs-lookup"><span data-stu-id="fcf6a-112">An object that defines the action set.</span></span>
<span data-ttu-id="fcf6a-113">Obter o objeto com cmdlet Add-AzureStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="fcf6a-113">Get the Object with cmdlet Add-AzureStorageAccountManagementPolicyAction</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyActionGroup
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fcf6a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fcf6a-114">-DefaultProfile</span></span>
<span data-ttu-id="fcf6a-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fcf6a-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fcf6a-116">-Disabled</span><span class="sxs-lookup"><span data-stu-id="fcf6a-116">-Disabled</span></span>
<span data-ttu-id="fcf6a-117">A regra será desabilitada se defini-la.</span><span class="sxs-lookup"><span data-stu-id="fcf6a-117">The rule is disabled if set it.</span></span>

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

### <span data-ttu-id="fcf6a-118">-Filter</span><span class="sxs-lookup"><span data-stu-id="fcf6a-118">-Filter</span></span>
<span data-ttu-id="fcf6a-119">Um objeto que define o conjunto de filtros.</span><span class="sxs-lookup"><span data-stu-id="fcf6a-119">An object that defines the filter set.</span></span>
<span data-ttu-id="fcf6a-120">Obter o objeto com cmdlet New-AzureStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="fcf6a-120">Get the Object with cmdlet New-AzureStorageAccountManagementPolicyFilter</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyRuleFilter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fcf6a-121">-Name</span><span class="sxs-lookup"><span data-stu-id="fcf6a-121">-Name</span></span>
<span data-ttu-id="fcf6a-122">Um nome de regra pode conter qualquer combinação de caracteres numéricos alfa.</span><span class="sxs-lookup"><span data-stu-id="fcf6a-122">A rule name can contain any combination of alpha numeric characters.</span></span>
<span data-ttu-id="fcf6a-123">O nome da regra é sensível a minúsculas.</span><span class="sxs-lookup"><span data-stu-id="fcf6a-123">Rule name is case-sensitive.</span></span>
<span data-ttu-id="fcf6a-124">Ele deve ser exclusivo em uma política.</span><span class="sxs-lookup"><span data-stu-id="fcf6a-124">It must be unique within a policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fcf6a-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fcf6a-125">CommonParameters</span></span>
<span data-ttu-id="fcf6a-126">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fcf6a-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fcf6a-127">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fcf6a-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fcf6a-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fcf6a-128">INPUTS</span></span>

### <span data-ttu-id="fcf6a-129">Nenhum</span><span class="sxs-lookup"><span data-stu-id="fcf6a-129">None</span></span>

## <span data-ttu-id="fcf6a-130">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="fcf6a-130">OUTPUTS</span></span>

### <span data-ttu-id="fcf6a-131">Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="fcf6a-131">Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyRule</span></span>

## <span data-ttu-id="fcf6a-132">NOTES</span><span class="sxs-lookup"><span data-stu-id="fcf6a-132">NOTES</span></span>

## <span data-ttu-id="fcf6a-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fcf6a-133">RELATED LINKS</span></span>

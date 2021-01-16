---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storage/new-Azstorageaccountmanagementpolicyrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountManagementPolicyRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountManagementPolicyRule.md
ms.openlocfilehash: c2a20d19676cff15ff26792a81bfc09242c5e4c2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98260958"
---
# <span data-ttu-id="b4ca3-101">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="b4ca3-101">New-AzStorageAccountManagementPolicyRule</span></span>

## <span data-ttu-id="b4ca3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b4ca3-102">SYNOPSIS</span></span>
<span data-ttu-id="b4ca3-103">Cria um objeto de regra ManagementPolicy, que pode ser usado em Set-AzStorageAccountManagementPolicy.</span><span class="sxs-lookup"><span data-stu-id="b4ca3-103">Creates a ManagementPolicy rule object, which can be used in Set-AzStorageAccountManagementPolicy.</span></span>

## <span data-ttu-id="b4ca3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b4ca3-104">SYNTAX</span></span>

```
New-AzStorageAccountManagementPolicyRule [-Name] <String> [-Disabled] -Action <PSManagementPolicyActionGroup>
 [-Filter <PSManagementPolicyRuleFilter>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b4ca3-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b4ca3-105">DESCRIPTION</span></span>
<span data-ttu-id="b4ca3-106">O cmdlet **New-AzStorageAccountManagementPolicyRule** cria um objeto de regra ManagementPolicy, que pode ser usado em Set-AzStorageAccountManagementPolicy.</span><span class="sxs-lookup"><span data-stu-id="b4ca3-106">The **New-AzStorageAccountManagementPolicyRule** cmdlet creates a ManagementPolicy rule object, which can be used in Set-AzStorageAccountManagementPolicy.</span></span>

## <span data-ttu-id="b4ca3-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b4ca3-107">EXAMPLES</span></span>

### <span data-ttu-id="b4ca3-108">Exemplo 1: cria um objeto de regra ManagementPolicy e, em seguida, definido como uma conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="b4ca3-108">Example 1: Creates a ManagementPolicy rule object, then set to a Storage Account</span></span>
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

<span data-ttu-id="b4ca3-109">Esse comando cria um objeto de regra ManagementPolicy, com um objeto de grupo de ação ManagementPolicy contém 4 ações, um objeto de filtro de regra ManagementPolicy e, em seguida, define a regra como uma conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="b4ca3-109">This command create a ManagementPolicy rule object, with a ManagementPolicy action group object contains 4 actions, a ManagementPolicy rule filter object, then set the rule to a Storage Account.</span></span>

## <span data-ttu-id="b4ca3-110">OS</span><span class="sxs-lookup"><span data-stu-id="b4ca3-110">PARAMETERS</span></span>

### <span data-ttu-id="b4ca3-111">-Ação</span><span class="sxs-lookup"><span data-stu-id="b4ca3-111">-Action</span></span>
<span data-ttu-id="b4ca3-112">Um objeto que define a ação definida.</span><span class="sxs-lookup"><span data-stu-id="b4ca3-112">An object that defines the action set.</span></span>
<span data-ttu-id="b4ca3-113">Obter o objeto com o cmdlet Add-AzureStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="b4ca3-113">Get the Object with cmdlet Add-AzureStorageAccountManagementPolicyAction</span></span>

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

### <span data-ttu-id="b4ca3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4ca3-114">-DefaultProfile</span></span>
<span data-ttu-id="b4ca3-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b4ca3-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b4ca3-116">-Desabilitado</span><span class="sxs-lookup"><span data-stu-id="b4ca3-116">-Disabled</span></span>
<span data-ttu-id="b4ca3-117">A regra estará desabilitada se definida.</span><span class="sxs-lookup"><span data-stu-id="b4ca3-117">The rule is disabled if set it.</span></span>

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

### <span data-ttu-id="b4ca3-118">-Filtro</span><span class="sxs-lookup"><span data-stu-id="b4ca3-118">-Filter</span></span>
<span data-ttu-id="b4ca3-119">Um objeto que define o conjunto de filtros.</span><span class="sxs-lookup"><span data-stu-id="b4ca3-119">An object that defines the filter set.</span></span>
<span data-ttu-id="b4ca3-120">Obter o objeto com o cmdlet New-AzureStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="b4ca3-120">Get the Object with cmdlet New-AzureStorageAccountManagementPolicyFilter</span></span>

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

### <span data-ttu-id="b4ca3-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="b4ca3-121">-Name</span></span>
<span data-ttu-id="b4ca3-122">Um nome de regra pode conter qualquer combinação de caracteres numéricos alfanuméricos.</span><span class="sxs-lookup"><span data-stu-id="b4ca3-122">A rule name can contain any combination of alpha numeric characters.</span></span>
<span data-ttu-id="b4ca3-123">O nome da regra diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="b4ca3-123">Rule name is case-sensitive.</span></span>
<span data-ttu-id="b4ca3-124">Ele deve ser exclusivo dentro de uma política.</span><span class="sxs-lookup"><span data-stu-id="b4ca3-124">It must be unique within a policy.</span></span>

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

### <span data-ttu-id="b4ca3-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4ca3-125">CommonParameters</span></span>
<span data-ttu-id="b4ca3-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4ca3-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4ca3-127">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4ca3-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4ca3-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b4ca3-128">INPUTS</span></span>

### <span data-ttu-id="b4ca3-129">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="b4ca3-129">None</span></span>

## <span data-ttu-id="b4ca3-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b4ca3-130">OUTPUTS</span></span>

### <span data-ttu-id="b4ca3-131">Microsoft. Azure. Commands. Management. Storage. Models. PSManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="b4ca3-131">Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyRule</span></span>

## <span data-ttu-id="b4ca3-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b4ca3-132">NOTES</span></span>

## <span data-ttu-id="b4ca3-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b4ca3-133">RELATED LINKS</span></span>

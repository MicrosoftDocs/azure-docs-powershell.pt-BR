---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storage/get-Azstorageaccountmanagementpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccountManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccountManagementPolicy.md
ms.openlocfilehash: b27d6e8bec4dda2ba87a0b38a9b37a8d4739ae00
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98260998"
---
# <span data-ttu-id="2b44b-101">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="2b44b-101">Get-AzStorageAccountManagementPolicy</span></span>

## <span data-ttu-id="2b44b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2b44b-102">SYNOPSIS</span></span>
<span data-ttu-id="2b44b-103">Obtém a política de gerenciamento de uma conta de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="2b44b-103">Gets the management policy of an Azure Storage account.</span></span>

## <span data-ttu-id="2b44b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2b44b-104">SYNTAX</span></span>

### <span data-ttu-id="2b44b-105">AccountName (padrão)</span><span class="sxs-lookup"><span data-stu-id="2b44b-105">AccountName (Default)</span></span>
```
Get-AzStorageAccountManagementPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2b44b-106">AccountResourceId</span><span class="sxs-lookup"><span data-stu-id="2b44b-106">AccountResourceId</span></span>
```
Get-AzStorageAccountManagementPolicy [-StorageAccountResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2b44b-107">Accountobject</span><span class="sxs-lookup"><span data-stu-id="2b44b-107">AccountObject</span></span>
```
Get-AzStorageAccountManagementPolicy -StorageAccount <PSStorageAccount>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2b44b-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2b44b-108">DESCRIPTION</span></span>
<span data-ttu-id="2b44b-109">O cmdlet **Get-AzStorageAccountManagementPolicy** Obtém a política de gerenciamento de uma conta de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="2b44b-109">The **Get-AzStorageAccountManagementPolicy** cmdlet gets the management policy of an Azure Storage account.</span></span>

## <span data-ttu-id="2b44b-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2b44b-110">EXAMPLES</span></span>

### <span data-ttu-id="2b44b-111">Exemplo 1: obter a política de gerenciamento de uma conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="2b44b-111">Example 1: Get the management policy of a Storage account.</span></span>
```
PS C:\>Get-AzStorageAccountManagementPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount"

ResourceGroupName  : myresourcegroup
StorageAccountName : mystorageaccount
Id                 : /subscriptions/{subscription-id}/resourceGroups/myresourcegroup/providers/Microsoft.Storage/storageAccounts/mystorageaccount/managementPolicies/default
Type               : Microsoft.Storage/storageAccounts/managementPolicies
LastModifiedTime   : 3/12/2019 7:04:05 AM
Rules              : [
                         {
                             "Enabled":  true,
                             "Name":  "Test",
                             "Definition":  {
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
                                                                                    "prefix1",
                                                                                    "prefix2"
                                                                                ],
                                                                "BlobTypes":  [
                                                                                  "blockBlob"
                                                                              ]
                                                            }
                                            }
                         },
                         {
                             "Enabled":  true,
                             "Name":  "Test2",
                             "Definition":  {
                                                "Actions":  {
                                                                "BaseBlob":  {
                                                                                 "TierToCool":  null,
                                                                                 "TierToArchive":  null,
                                                                                 "Delete":  {
                                                                                                "DaysAfterModificationGreaterThan":  100
                                                                                            }
                                                                             },
                                                                "Snapshot":  null
                                                            },
                                                "Filters":  {
                                                                "PrefixMatch":  null,
                                                                "BlobTypes":  [
                                                                                  "blockBlob"
                                                                              ]
                                                            }
                                            }
                         }
                     ]
```

<span data-ttu-id="2b44b-112">Esse comando obtém a política de gerenciamento de uma conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="2b44b-112">This command gets the management policy of a Storage account.</span></span>

## <span data-ttu-id="2b44b-113">OS</span><span class="sxs-lookup"><span data-stu-id="2b44b-113">PARAMETERS</span></span>

### <span data-ttu-id="2b44b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b44b-114">-DefaultProfile</span></span>
<span data-ttu-id="2b44b-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2b44b-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2b44b-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b44b-116">-ResourceGroupName</span></span>
<span data-ttu-id="2b44b-117">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="2b44b-117">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b44b-118">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="2b44b-118">-StorageAccount</span></span>
<span data-ttu-id="2b44b-119">Objeto da conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="2b44b-119">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2b44b-120">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="2b44b-120">-StorageAccountName</span></span>
<span data-ttu-id="2b44b-121">Nome da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="2b44b-121">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b44b-122">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="2b44b-122">-StorageAccountResourceId</span></span>
<span data-ttu-id="2b44b-123">ID do recurso da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="2b44b-123">Storage Account Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b44b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b44b-124">CommonParameters</span></span>
<span data-ttu-id="2b44b-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b44b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b44b-126">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b44b-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b44b-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2b44b-127">INPUTS</span></span>

### <span data-ttu-id="2b44b-128">System. String</span><span class="sxs-lookup"><span data-stu-id="2b44b-128">System.String</span></span>

## <span data-ttu-id="2b44b-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2b44b-129">OUTPUTS</span></span>

### <span data-ttu-id="2b44b-130">Microsoft. Azure. Management. Storage. Models. StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="2b44b-130">Microsoft.Azure.Management.Storage.Models.StorageAccountKey</span></span>

## <span data-ttu-id="2b44b-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2b44b-131">NOTES</span></span>

## <span data-ttu-id="2b44b-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2b44b-132">RELATED LINKS</span></span>

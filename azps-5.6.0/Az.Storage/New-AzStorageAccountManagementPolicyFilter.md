---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/Az.storage/new-Azstorageaccountmanagementpolicyfilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountManagementPolicyFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountManagementPolicyFilter.md
ms.openlocfilehash: 40a2420803197b21bb9f0f8d20b771482b4e694b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891981"
---
# <span data-ttu-id="c8819-101">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="c8819-101">New-AzStorageAccountManagementPolicyFilter</span></span>

## <span data-ttu-id="c8819-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c8819-102">SYNOPSIS</span></span>
<span data-ttu-id="c8819-103">Cria um objeto de filtro de regra ManagementPolicy, que pode ser usado em New-AzStorageAccountManagementPolicyRule.</span><span class="sxs-lookup"><span data-stu-id="c8819-103">Creates a ManagementPolicy rule filter object, which can be used in New-AzStorageAccountManagementPolicyRule.</span></span>

## <span data-ttu-id="c8819-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="c8819-104">SYNTAX</span></span>

```
New-AzStorageAccountManagementPolicyFilter [-PrefixMatch <String[]>] [-BlobType <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c8819-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="c8819-105">DESCRIPTION</span></span>
<span data-ttu-id="c8819-106">O cmdlet **New-AzStorageAccountManagementPolicyFilter** cria um objeto de filtro de regra ManagementPolicy, que pode ser usado em New-AzStorageAccountManagementPolicyRule.</span><span class="sxs-lookup"><span data-stu-id="c8819-106">The **New-AzStorageAccountManagementPolicyFilter** cmdlet creates a ManagementPolicy rule filter object, which can be used in New-AzStorageAccountManagementPolicyRule.</span></span>

## <span data-ttu-id="c8819-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c8819-107">EXAMPLES</span></span>

### <span data-ttu-id="c8819-108">Exemplo 1: cria um objeto de filtro de regra ManagementPolicy, depois a adiciona a uma regra de política de gerenciamento e configura uma conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="c8819-108">Example 1: Creates a ManagementPolicy rule filter object, then add it to a management policy rule and set to a Storage account</span></span>
```
PS C:\>$filter = New-AzStorageAccountManagementPolicyFilter -PrefixMatch blobprefix1,blobprefix2 -BlobType appendBlob,blockBlob
PS C:\>$filter 

PrefixMatch                BlobTypes  
-----------                ---------  
{blobprefix1, blobprefix2} {appendBlob, blockBlob}

PS C:\>$action = Add-AzStorageAccountManagementPolicyAction -BaseBlobAction Delete -daysAfterModificationGreaterThan 100
PS C:\>$rule = New-AzStorageAccountManagementPolicyRule -Name Test -Action $action -Filter $filter
PS C:\>$policy = Set-AzStorageAccountManagementPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -Rule $rule
```

<span data-ttu-id="c8819-109">Este comando cria um objeto de filtro de regra ManagementPolicy.</span><span class="sxs-lookup"><span data-stu-id="c8819-109">This command create a ManagementPolicy rule filter object.</span></span> <span data-ttu-id="c8819-110">Em seguida, adicione-a a uma regra de política de gerenciamento e desmarcar uma conta de Armazenamento.</span><span class="sxs-lookup"><span data-stu-id="c8819-110">Then add it to a management policy rule and set to a Storage account.</span></span>

## <span data-ttu-id="c8819-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="c8819-111">PARAMETERS</span></span>

### <span data-ttu-id="c8819-112">-BlobType</span><span class="sxs-lookup"><span data-stu-id="c8819-112">-BlobType</span></span>
<span data-ttu-id="c8819-113">Uma matriz de cadeias de caracteres para blobtypes a serem match.</span><span class="sxs-lookup"><span data-stu-id="c8819-113">An array of strings for blobtypes to be match.</span></span> <span data-ttu-id="c8819-114">Atualmente, blockBlob dá suporte a todas as ações de classificação e exclusão.</span><span class="sxs-lookup"><span data-stu-id="c8819-114">Currently blockBlob supports all tiering and delete actions.</span></span> <span data-ttu-id="c8819-115">Somente ações de exclusão são suportadas para appendBlob.</span><span class="sxs-lookup"><span data-stu-id="c8819-115">Only delete actions are supported for appendBlob.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: blockBlob, appendBlob

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8819-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8819-116">-DefaultProfile</span></span>
<span data-ttu-id="c8819-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c8819-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c8819-118">-PrefixMatch</span><span class="sxs-lookup"><span data-stu-id="c8819-118">-PrefixMatch</span></span>
<span data-ttu-id="c8819-119">Uma matriz de cadeias de caracteres para prefixos a serem corresponder.</span><span class="sxs-lookup"><span data-stu-id="c8819-119">An array of strings for prefixes to be match.</span></span>
<span data-ttu-id="c8819-120">Uma cadeia de caracteres de prefixo deve começar com um nome de contêiner.</span><span class="sxs-lookup"><span data-stu-id="c8819-120">A prefix string must start with a container name.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8819-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8819-121">CommonParameters</span></span>
<span data-ttu-id="c8819-122">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8819-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8819-123">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c8819-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8819-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c8819-124">INPUTS</span></span>

### <span data-ttu-id="c8819-125">Nenhum</span><span class="sxs-lookup"><span data-stu-id="c8819-125">None</span></span>

## <span data-ttu-id="c8819-126">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="c8819-126">OUTPUTS</span></span>

### <span data-ttu-id="c8819-127">Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyRuleFilter</span><span class="sxs-lookup"><span data-stu-id="c8819-127">Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyRuleFilter</span></span>

## <span data-ttu-id="c8819-128">NOTES</span><span class="sxs-lookup"><span data-stu-id="c8819-128">NOTES</span></span>

## <span data-ttu-id="c8819-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c8819-129">RELATED LINKS</span></span>

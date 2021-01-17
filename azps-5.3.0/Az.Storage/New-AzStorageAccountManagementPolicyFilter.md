---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storage/new-Azstorageaccountmanagementpolicyfilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountManagementPolicyFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountManagementPolicyFilter.md
ms.openlocfilehash: 48ae8b87671e52abe4d109025048fe1e4aeca117
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98429101"
---
# <span data-ttu-id="b34f0-101">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="b34f0-101">New-AzStorageAccountManagementPolicyFilter</span></span>

## <span data-ttu-id="b34f0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b34f0-102">SYNOPSIS</span></span>
<span data-ttu-id="b34f0-103">Cria um objeto de filtro de regra ManagementPolicy, que pode ser usado em New-AzStorageAccountManagementPolicyRule.</span><span class="sxs-lookup"><span data-stu-id="b34f0-103">Creates a ManagementPolicy rule filter object, which can be used in New-AzStorageAccountManagementPolicyRule.</span></span>

## <span data-ttu-id="b34f0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b34f0-104">SYNTAX</span></span>

```
New-AzStorageAccountManagementPolicyFilter [-PrefixMatch <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b34f0-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b34f0-105">DESCRIPTION</span></span>
<span data-ttu-id="b34f0-106">O cmdlet **New-AzStorageAccountManagementPolicyFilter** cria um objeto de filtro de regra ManagementPolicy, que pode ser usado em New-AzStorageAccountManagementPolicyRule.</span><span class="sxs-lookup"><span data-stu-id="b34f0-106">The **New-AzStorageAccountManagementPolicyFilter** cmdlet creates a ManagementPolicy rule filter object, which can be used in New-AzStorageAccountManagementPolicyRule.</span></span>

## <span data-ttu-id="b34f0-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b34f0-107">EXAMPLES</span></span>

### <span data-ttu-id="b34f0-108">Exemplo 1: cria um objeto de filtro de regra ManagementPolicy e, em seguida, o adiciona a uma regra de política de gerenciamento e definido como uma conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="b34f0-108">Example 1: Creates a ManagementPolicy rule filter object, then add it to a management policy rule and set to a Storage account</span></span>
```
PS C:\>$filter = New-AzStorageAccountManagementPolicyFilter -PrefixMatch blobprefix1,blobprefix2
PS C:\>$filter 

PrefixMatch                BlobTypes  
-----------                ---------  
{blobprefix1, blobprefix2} {blockBlob}

PS C:\>$action = Add-AzStorageAccountManagementPolicyAction -BaseBlobAction Delete -daysAfterModificationGreaterThan 100
PS C:\>$rule = New-AzStorageAccountManagementPolicyRule -Name Test -Action $action -Filter $filter
PS C:\>$policy = Set-AzStorageAccountManagementPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -Rule $rule
```

<span data-ttu-id="b34f0-109">Esse comando cria um objeto de filtro de regra ManagementPolicy.</span><span class="sxs-lookup"><span data-stu-id="b34f0-109">This command create a ManagementPolicy rule filter object.</span></span> <span data-ttu-id="b34f0-110">Em seguida, adicione-o a uma regra de política de gerenciamento e defina-o como uma conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="b34f0-110">Then add it to a management policy rule and set to a Storage account.</span></span>

## <span data-ttu-id="b34f0-111">OS</span><span class="sxs-lookup"><span data-stu-id="b34f0-111">PARAMETERS</span></span>

### <span data-ttu-id="b34f0-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b34f0-112">-DefaultProfile</span></span>
<span data-ttu-id="b34f0-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b34f0-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b34f0-114">-PrefixMatch</span><span class="sxs-lookup"><span data-stu-id="b34f0-114">-PrefixMatch</span></span>
<span data-ttu-id="b34f0-115">Uma matriz de cadeias de caracteres para os prefixos serem CORRESP.</span><span class="sxs-lookup"><span data-stu-id="b34f0-115">An array of strings for prefixes to be match.</span></span>
<span data-ttu-id="b34f0-116">Uma cadeia de caracteres de prefixo deve começar com um nome de contêiner.</span><span class="sxs-lookup"><span data-stu-id="b34f0-116">A prefix string must start with a container name.</span></span>

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

### <span data-ttu-id="b34f0-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b34f0-117">CommonParameters</span></span>
<span data-ttu-id="b34f0-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b34f0-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b34f0-119">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b34f0-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b34f0-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b34f0-120">INPUTS</span></span>

### <span data-ttu-id="b34f0-121">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="b34f0-121">None</span></span>

## <span data-ttu-id="b34f0-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b34f0-122">OUTPUTS</span></span>

### <span data-ttu-id="b34f0-123">Microsoft. Azure. Commands. Management. Storage. Models. PSManagementPolicyRuleFilter</span><span class="sxs-lookup"><span data-stu-id="b34f0-123">Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyRuleFilter</span></span>

## <span data-ttu-id="b34f0-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b34f0-124">NOTES</span></span>

## <span data-ttu-id="b34f0-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b34f0-125">RELATED LINKS</span></span>

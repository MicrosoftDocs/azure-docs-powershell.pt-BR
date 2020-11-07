---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: F6EA099A-D588-49AE-9D2C-865BC32685BA
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageaccountnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Get-AzStorageAccountNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Get-AzStorageAccountNameAvailability.md
ms.openlocfilehash: 2000b2f50ac4c3c26f1e5dfbc5debe07ea9bd894
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776277"
---
# <span data-ttu-id="cacb4-101">Get-AzStorageAccountNameAvailability</span><span class="sxs-lookup"><span data-stu-id="cacb4-101">Get-AzStorageAccountNameAvailability</span></span>

## <span data-ttu-id="cacb4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cacb4-102">SYNOPSIS</span></span>
<span data-ttu-id="cacb4-103">Verifica a disponibilidade de um nome de conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="cacb4-103">Checks the availability of a Storage account name.</span></span>

## <span data-ttu-id="cacb4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cacb4-104">SYNTAX</span></span>

```
Get-AzStorageAccountNameAvailability [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cacb4-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="cacb4-105">DESCRIPTION</span></span>
<span data-ttu-id="cacb4-106">O cmdlet **Get-AzStorageAccountNameAvailability** verifica se o nome de uma conta de armazenamento do Azure é válido e está disponível para uso.</span><span class="sxs-lookup"><span data-stu-id="cacb4-106">The **Get-AzStorageAccountNameAvailability** cmdlet checks whether the name of an Azure Storage account is valid and available to use.</span></span>

## <span data-ttu-id="cacb4-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cacb4-107">EXAMPLES</span></span>

### <span data-ttu-id="cacb4-108">Exemplo 1: verificar a disponibilidade de um nome de conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="cacb4-108">Example 1: Check availability of a Storage account name</span></span>
```
PS C:\>Get-AzStorageAccountNameAvailability -Name 'contosostorage03'
```

<span data-ttu-id="cacb4-109">Esse comando verifica a disponibilidade do nome ContosoStorage03.</span><span class="sxs-lookup"><span data-stu-id="cacb4-109">This command checks the availability of the name ContosoStorage03.</span></span>

## <span data-ttu-id="cacb4-110">OS</span><span class="sxs-lookup"><span data-stu-id="cacb4-110">PARAMETERS</span></span>

### <span data-ttu-id="cacb4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cacb4-111">-DefaultProfile</span></span>
<span data-ttu-id="cacb4-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="cacb4-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cacb4-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="cacb4-113">-Name</span></span>
<span data-ttu-id="cacb4-114">Especifica o nome da conta de armazenamento que este cmdlet verifica.</span><span class="sxs-lookup"><span data-stu-id="cacb4-114">Specifies the name of the Storage account that this cmdlet checks.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cacb4-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cacb4-115">CommonParameters</span></span>
<span data-ttu-id="cacb4-116">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cacb4-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cacb4-117">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cacb4-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cacb4-118">SENSORES</span><span class="sxs-lookup"><span data-stu-id="cacb4-118">INPUTS</span></span>

### <span data-ttu-id="cacb4-119">System. String</span><span class="sxs-lookup"><span data-stu-id="cacb4-119">System.String</span></span>

## <span data-ttu-id="cacb4-120">EXIBE</span><span class="sxs-lookup"><span data-stu-id="cacb4-120">OUTPUTS</span></span>

### <span data-ttu-id="cacb4-121">Microsoft. Azure. Management. Storage. Models. CheckNameAvailabilityResult</span><span class="sxs-lookup"><span data-stu-id="cacb4-121">Microsoft.Azure.Management.Storage.Models.CheckNameAvailabilityResult</span></span>

## <span data-ttu-id="cacb4-122">INFORMA</span><span class="sxs-lookup"><span data-stu-id="cacb4-122">NOTES</span></span>

## <span data-ttu-id="cacb4-123">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cacb4-123">RELATED LINKS</span></span>

[<span data-ttu-id="cacb4-124">Cmdlets do Azure Storage Manager</span><span class="sxs-lookup"><span data-stu-id="cacb4-124">Azure Storage Manager Cmdlets</span></span>](./Az.Storage.md)


---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
ms.assetid: F6EA099A-D588-49AE-9D2C-865BC32685BA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/get-azurermstorageaccountnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageAccountNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageAccountNameAvailability.md
ms.openlocfilehash: 402e3fdfe108486cd356af8a20ea06793f533937
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93439992"
---
# <span data-ttu-id="a6350-101">Get-AzureRmStorageAccountNameAvailability</span><span class="sxs-lookup"><span data-stu-id="a6350-101">Get-AzureRmStorageAccountNameAvailability</span></span>

## <span data-ttu-id="a6350-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a6350-102">SYNOPSIS</span></span>
<span data-ttu-id="a6350-103">Verifica a disponibilidade de um nome de conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="a6350-103">Checks the availability of a Storage account name.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a6350-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a6350-104">SYNTAX</span></span>

```
Get-AzureRmStorageAccountNameAvailability [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a6350-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a6350-105">DESCRIPTION</span></span>
<span data-ttu-id="a6350-106">O cmdlet **Get-AzureRmStorageAccountNameAvailability** verifica se o nome de uma conta de armazenamento do Azure é válido e está disponível para uso.</span><span class="sxs-lookup"><span data-stu-id="a6350-106">The **Get-AzureRmStorageAccountNameAvailability** cmdlet checks whether the name of an Azure Storage account is valid and available to use.</span></span>

## <span data-ttu-id="a6350-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a6350-107">EXAMPLES</span></span>

### <span data-ttu-id="a6350-108">Exemplo 1: verificar a disponibilidade de um nome de conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="a6350-108">Example 1: Check availability of a Storage account name</span></span>
```
PS C:\>Get-AzureRmStorageAccountNameAvailability -Name 'contosostorage03'
```

<span data-ttu-id="a6350-109">Esse comando verifica a disponibilidade do nome ContosoStorage03.</span><span class="sxs-lookup"><span data-stu-id="a6350-109">This command checks the availability of the name ContosoStorage03.</span></span>

## <span data-ttu-id="a6350-110">OS</span><span class="sxs-lookup"><span data-stu-id="a6350-110">PARAMETERS</span></span>

### <span data-ttu-id="a6350-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6350-111">-DefaultProfile</span></span>
<span data-ttu-id="a6350-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a6350-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a6350-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="a6350-113">-Name</span></span>
<span data-ttu-id="a6350-114">Especifica o nome da conta de armazenamento que este cmdlet verifica.</span><span class="sxs-lookup"><span data-stu-id="a6350-114">Specifies the name of the Storage account that this cmdlet checks.</span></span>

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

### <span data-ttu-id="a6350-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6350-115">CommonParameters</span></span>
<span data-ttu-id="a6350-116">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6350-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6350-117">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a6350-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6350-118">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a6350-118">INPUTS</span></span>

### <span data-ttu-id="a6350-119">System. String</span><span class="sxs-lookup"><span data-stu-id="a6350-119">System.String</span></span>

## <span data-ttu-id="a6350-120">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a6350-120">OUTPUTS</span></span>

### <span data-ttu-id="a6350-121">Microsoft. Azure. Management. Storage. Models. CheckNameAvailabilityResult</span><span class="sxs-lookup"><span data-stu-id="a6350-121">Microsoft.Azure.Management.Storage.Models.CheckNameAvailabilityResult</span></span>

## <span data-ttu-id="a6350-122">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a6350-122">NOTES</span></span>

## <span data-ttu-id="a6350-123">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a6350-123">RELATED LINKS</span></span>

[<span data-ttu-id="a6350-124">Cmdlets do Azure Storage Manager</span><span class="sxs-lookup"><span data-stu-id="a6350-124">Azure Storage Manager Cmdlets</span></span>](./AzureRM.Storage.md)


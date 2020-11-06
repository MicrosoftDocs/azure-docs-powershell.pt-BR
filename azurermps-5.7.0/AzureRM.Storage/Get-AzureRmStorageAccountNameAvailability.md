---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
ms.assetid: F6EA099A-D588-49AE-9D2C-865BC32685BA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageAccountNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageAccountNameAvailability.md
ms.openlocfilehash: 8590c9566cf84648dc8668d3fb49ac19b8d4787d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602137"
---
# <span data-ttu-id="57916-101">Get-AzureRmStorageAccountNameAvailability</span><span class="sxs-lookup"><span data-stu-id="57916-101">Get-AzureRmStorageAccountNameAvailability</span></span>

## <span data-ttu-id="57916-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="57916-102">SYNOPSIS</span></span>
<span data-ttu-id="57916-103">Verifica a disponibilidade de um nome de conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="57916-103">Checks the availability of a storage account name.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="57916-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="57916-104">SYNTAX</span></span>

```
Get-AzureRmStorageAccountNameAvailability [-Name] <String> [<CommonParameters>]
```

## <span data-ttu-id="57916-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="57916-105">DESCRIPTION</span></span>
<span data-ttu-id="57916-106">O cmdlet **Get-AzureRmStorageAccountNameAvailability** verifica se o nome de uma conta de armazenamento do Azure é válido e está disponível para uso.</span><span class="sxs-lookup"><span data-stu-id="57916-106">The **Get-AzureRmStorageAccountNameAvailability** cmdlet checks whether the name of an Azure Storage account is valid and available to use.</span></span>

## <span data-ttu-id="57916-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="57916-107">EXAMPLES</span></span>

### <span data-ttu-id="57916-108">Exemplo 1: verificar a disponibilidade de um nome de conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="57916-108">Example 1: Check availability of a storage account name</span></span>
```
PS C:\>Get-AzureRmStorageAccountNameAvailability -Name 'ContosoStorage03'
```

<span data-ttu-id="57916-109">Esse comando verifica a disponibilidade do nome ContosoStorage03.</span><span class="sxs-lookup"><span data-stu-id="57916-109">This command checks the availability of the name ContosoStorage03.</span></span>

## <span data-ttu-id="57916-110">OS</span><span class="sxs-lookup"><span data-stu-id="57916-110">PARAMETERS</span></span>

### <span data-ttu-id="57916-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="57916-111">-Name</span></span>
<span data-ttu-id="57916-112">Especifica o nome da conta de armazenamento que este cmdlet verifica.</span><span class="sxs-lookup"><span data-stu-id="57916-112">Specifies the name of the Storage account that this cmdlet checks.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57916-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57916-113">CommonParameters</span></span>
<span data-ttu-id="57916-114">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57916-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57916-115">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57916-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57916-116">SENSORES</span><span class="sxs-lookup"><span data-stu-id="57916-116">INPUTS</span></span>

### <span data-ttu-id="57916-117">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="57916-117">None</span></span>
<span data-ttu-id="57916-118">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="57916-118">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="57916-119">EXIBE</span><span class="sxs-lookup"><span data-stu-id="57916-119">OUTPUTS</span></span>

## <span data-ttu-id="57916-120">INFORMA</span><span class="sxs-lookup"><span data-stu-id="57916-120">NOTES</span></span>

## <span data-ttu-id="57916-121">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="57916-121">RELATED LINKS</span></span>

[<span data-ttu-id="57916-122">Cmdlets do Azure Storage Manager</span><span class="sxs-lookup"><span data-stu-id="57916-122">Azure Storage Manager Cmdlets</span></span>](./AzureRM.Storage.md)

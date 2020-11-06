---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 3B4F32F3-51ED-4851-B38F-172658186C96
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageTable.md
ms.openlocfilehash: 53bb5f3a34cddf9e74bfb9d9c9f1bd1d109d8f6d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430557"
---
# <span data-ttu-id="d0a10-101">New-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="d0a10-101">New-AzureStorageTable</span></span>

## <span data-ttu-id="d0a10-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d0a10-102">SYNOPSIS</span></span>
<span data-ttu-id="d0a10-103">Cria uma tabela de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="d0a10-103">Creates a storage table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d0a10-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d0a10-104">SYNTAX</span></span>

```
New-AzureStorageTable [-Name] <String> [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="d0a10-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d0a10-105">DESCRIPTION</span></span>
<span data-ttu-id="d0a10-106">O cmdlet **New-AzureStorageTable** cria uma tabela de armazenamento associada à conta de armazenamento no Azure.</span><span class="sxs-lookup"><span data-stu-id="d0a10-106">The **New-AzureStorageTable** cmdlet creates a storage table associated with the storage account in Azure.</span></span>

## <span data-ttu-id="d0a10-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d0a10-107">EXAMPLES</span></span>

### <span data-ttu-id="d0a10-108">Exemplo 1: criar uma tabela de armazenamento do Azure</span><span class="sxs-lookup"><span data-stu-id="d0a10-108">Example 1: Create an azure storage table</span></span>
```
PS C:\>New-AzureStorageTable -Name "tableabc"
```

<span data-ttu-id="d0a10-109">Esse comando cria uma tabela de armazenamento com um nome de tableabc.</span><span class="sxs-lookup"><span data-stu-id="d0a10-109">This command creates a storage table with a name of tableabc.</span></span>

### <span data-ttu-id="d0a10-110">Exemplo 2: criar várias tabelas de armazenamento do Azure</span><span class="sxs-lookup"><span data-stu-id="d0a10-110">Example 2: Create multiple azure storage tables</span></span>
```
PS C:\>"table1 table2 table3".split() | New-AzureStorageTable
```

<span data-ttu-id="d0a10-111">Esse comando cria várias tabelas.</span><span class="sxs-lookup"><span data-stu-id="d0a10-111">This command creates multiple tables.</span></span>
<span data-ttu-id="d0a10-112">Ele usa o método **Split** da classe **String** .net e, em seguida, passa os nomes no pipeline.</span><span class="sxs-lookup"><span data-stu-id="d0a10-112">It uses the **Split** method of the .NET **String** class and then passes the names on the pipeline.</span></span>

## <span data-ttu-id="d0a10-113">OS</span><span class="sxs-lookup"><span data-stu-id="d0a10-113">PARAMETERS</span></span>

### <span data-ttu-id="d0a10-114">-Contexto</span><span class="sxs-lookup"><span data-stu-id="d0a10-114">-Context</span></span>
<span data-ttu-id="d0a10-115">Especifica o contexto de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="d0a10-115">Specifies the storage context.</span></span>
<span data-ttu-id="d0a10-116">Para criá-la, você pode usar o cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="d0a10-116">To create it, you can use the New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d0a10-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="d0a10-117">-Name</span></span>
<span data-ttu-id="d0a10-118">Especifica um nome para a nova tabela.</span><span class="sxs-lookup"><span data-stu-id="d0a10-118">Specifies a name for the new table.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Table

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d0a10-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0a10-119">CommonParameters</span></span>
<span data-ttu-id="d0a10-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0a10-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0a10-121">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d0a10-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0a10-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d0a10-122">INPUTS</span></span>

### <span data-ttu-id="d0a10-123">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="d0a10-123">IStorageContext</span></span>

<span data-ttu-id="d0a10-124">O parâmetro ' Context ' aceita o valor do tipo ' IStorageContext ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="d0a10-124">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="d0a10-125">String</span><span class="sxs-lookup"><span data-stu-id="d0a10-125">String</span></span>

<span data-ttu-id="d0a10-126">O parâmetro ' name ' aceita o valor do tipo ' String ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="d0a10-126">Parameter 'Name' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="d0a10-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d0a10-127">OUTPUTS</span></span>

### <span data-ttu-id="d0a10-128">Microsoft. WindowsAzure. Commands. Common. Storage. ResourceModel. AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="d0a10-128">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageTable</span></span>

## <span data-ttu-id="d0a10-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d0a10-129">NOTES</span></span>

## <span data-ttu-id="d0a10-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d0a10-130">RELATED LINKS</span></span>

[<span data-ttu-id="d0a10-131">Get-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="d0a10-131">Get-AzureStorageTable</span></span>](./Get-AzureStorageTable.md)

[<span data-ttu-id="d0a10-132">Remove-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="d0a10-132">Remove-AzureStorageTable</span></span>](./Remove-AzureStorageTable.md)



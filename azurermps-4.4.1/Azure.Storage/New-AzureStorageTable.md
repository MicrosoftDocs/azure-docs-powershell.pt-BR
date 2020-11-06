---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 3B4F32F3-51ED-4851-B38F-172658186C96
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageTable.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: 2f051fb0724ac266753d87fc30489398a4aa64a0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428338"
---
# <span data-ttu-id="7ef46-101">New-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="7ef46-101">New-AzureStorageTable</span></span>

## <span data-ttu-id="7ef46-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7ef46-102">SYNOPSIS</span></span>
<span data-ttu-id="7ef46-103">Cria uma tabela de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="7ef46-103">Creates a storage table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7ef46-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7ef46-104">SYNTAX</span></span>

```
New-AzureStorageTable [-Name] <String> [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="7ef46-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7ef46-105">DESCRIPTION</span></span>
<span data-ttu-id="7ef46-106">O cmdlet **New-AzureStorageTable** cria uma tabela de armazenamento associada à conta de armazenamento no Azure.</span><span class="sxs-lookup"><span data-stu-id="7ef46-106">The **New-AzureStorageTable** cmdlet creates a storage table associated with the storage account in Azure.</span></span>

## <span data-ttu-id="7ef46-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7ef46-107">EXAMPLES</span></span>

### <span data-ttu-id="7ef46-108">Exemplo 1: criar uma tabela de armazenamento do Azure</span><span class="sxs-lookup"><span data-stu-id="7ef46-108">Example 1: Create an azure storage table</span></span>
```
PS C:\>New-AzureStorageTable -Name "tableabc"
```

<span data-ttu-id="7ef46-109">Esse comando cria uma tabela de armazenamento com um nome de tableabc.</span><span class="sxs-lookup"><span data-stu-id="7ef46-109">This command creates a storage table with a name of tableabc.</span></span>

### <span data-ttu-id="7ef46-110">Exemplo 2: criar várias tabelas de armazenamento do Azure</span><span class="sxs-lookup"><span data-stu-id="7ef46-110">Example 2: Create multiple azure storage tables</span></span>
```
PS C:\>"table1 table2 table3".split() | New-AzureStorageTable
```

<span data-ttu-id="7ef46-111">Esse comando cria várias tabelas.</span><span class="sxs-lookup"><span data-stu-id="7ef46-111">This command creates multiple tables.</span></span>
<span data-ttu-id="7ef46-112">Ele usa o método **Split** da classe **String** .net e, em seguida, passa os nomes no pipeline.</span><span class="sxs-lookup"><span data-stu-id="7ef46-112">It uses the **Split** method of the .NET **String** class and then passes the names on the pipeline.</span></span>

## <span data-ttu-id="7ef46-113">OS</span><span class="sxs-lookup"><span data-stu-id="7ef46-113">PARAMETERS</span></span>

### <span data-ttu-id="7ef46-114">-Contexto</span><span class="sxs-lookup"><span data-stu-id="7ef46-114">-Context</span></span>
<span data-ttu-id="7ef46-115">Especifica o contexto de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="7ef46-115">Specifies the storage context.</span></span>
<span data-ttu-id="7ef46-116">Para criá-la, você pode usar o cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="7ef46-116">To create it, you can use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="7ef46-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="7ef46-117">-Name</span></span>
<span data-ttu-id="7ef46-118">Especifica um nome para a nova tabela.</span><span class="sxs-lookup"><span data-stu-id="7ef46-118">Specifies a name for the new table.</span></span>

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

### <span data-ttu-id="7ef46-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ef46-119">CommonParameters</span></span>
<span data-ttu-id="7ef46-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ef46-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ef46-121">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7ef46-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ef46-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7ef46-122">INPUTS</span></span>

### <span data-ttu-id="7ef46-123">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="7ef46-123">IStorageContext</span></span>

<span data-ttu-id="7ef46-124">O parâmetro ' Context ' aceita o valor do tipo ' IStorageContext ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="7ef46-124">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="7ef46-125">String</span><span class="sxs-lookup"><span data-stu-id="7ef46-125">String</span></span>

<span data-ttu-id="7ef46-126">O parâmetro ' name ' aceita o valor do tipo ' String ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="7ef46-126">Parameter 'Name' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="7ef46-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7ef46-127">OUTPUTS</span></span>

### <span data-ttu-id="7ef46-128">Microsoft. WindowsAzure. Commands. Common. Storage. ResourceModel. AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="7ef46-128">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageTable</span></span>

## <span data-ttu-id="7ef46-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7ef46-129">NOTES</span></span>

## <span data-ttu-id="7ef46-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7ef46-130">RELATED LINKS</span></span>

[<span data-ttu-id="7ef46-131">Get-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="7ef46-131">Get-AzureStorageTable</span></span>](./Get-AzureStorageTable.md)

[<span data-ttu-id="7ef46-132">Remove-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="7ef46-132">Remove-AzureStorageTable</span></span>](./Remove-AzureStorageTable.md)



---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: E9500392-6BE1-46EC-9AF5-9234281025E6
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragequeue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageQueue.md
ms.openlocfilehash: 6363b8030571d6cf3e89b30229395b16cdb5f44b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430566"
---
# <span data-ttu-id="9ffb0-101">New-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="9ffb0-101">New-AzureStorageQueue</span></span>

## <span data-ttu-id="9ffb0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9ffb0-102">SYNOPSIS</span></span>
<span data-ttu-id="9ffb0-103">Cria uma fila de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="9ffb0-103">Creates a storage queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9ffb0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9ffb0-104">SYNTAX</span></span>

```
New-AzureStorageQueue [-Name] <String> [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="9ffb0-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9ffb0-105">DESCRIPTION</span></span>
<span data-ttu-id="9ffb0-106">O cmdlet **New-AzureStorageQueue** cria uma fila de armazenamento no Azure.</span><span class="sxs-lookup"><span data-stu-id="9ffb0-106">The **New-AzureStorageQueue** cmdlet creates a storage queue in Azure.</span></span>

## <span data-ttu-id="9ffb0-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9ffb0-107">EXAMPLES</span></span>

### <span data-ttu-id="9ffb0-108">Exemplo 1: criar uma fila de armazenamento do Azure</span><span class="sxs-lookup"><span data-stu-id="9ffb0-108">Example 1: Create an Azure storage queue</span></span>
```
PS C:\>New-AzureStorageQueue -Name "queueabc"
```

<span data-ttu-id="9ffb0-109">Este exemplo cria uma fila de armazenamento chamada queueabc.</span><span class="sxs-lookup"><span data-stu-id="9ffb0-109">This example creates a storage queue named queueabc.</span></span>

### <span data-ttu-id="9ffb0-110">Exemplo 2: criar várias filas de armazenamento do Azure</span><span class="sxs-lookup"><span data-stu-id="9ffb0-110">Example 2: Create multiple azure storage queues</span></span>
```
PS C:\>"queue1 queue2 queue3".split() | New-AzureStorageQueue
```

<span data-ttu-id="9ffb0-111">Este exemplo cria várias filas de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="9ffb0-111">This example creates multiple storage queues.</span></span>
<span data-ttu-id="9ffb0-112">Ele usa o método Split da classe String .NET e, em seguida, passa os nomes no pipeline.</span><span class="sxs-lookup"><span data-stu-id="9ffb0-112">It uses the Split method of the .NET String class and then passes the names on the pipeline.</span></span>

## <span data-ttu-id="9ffb0-113">OS</span><span class="sxs-lookup"><span data-stu-id="9ffb0-113">PARAMETERS</span></span>

### <span data-ttu-id="9ffb0-114">-Contexto</span><span class="sxs-lookup"><span data-stu-id="9ffb0-114">-Context</span></span>
<span data-ttu-id="9ffb0-115">Especifica o contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="9ffb0-115">Specifies the Azure storage context.</span></span>
<span data-ttu-id="9ffb0-116">Você pode criá-lo usando o cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="9ffb0-116">You can create it by using the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="9ffb0-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="9ffb0-117">-Name</span></span>
<span data-ttu-id="9ffb0-118">Especifica um nome para a fila.</span><span class="sxs-lookup"><span data-stu-id="9ffb0-118">Specifies a name for the queue.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Queue

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9ffb0-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ffb0-119">CommonParameters</span></span>
<span data-ttu-id="9ffb0-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ffb0-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ffb0-121">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9ffb0-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ffb0-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9ffb0-122">INPUTS</span></span>

### <span data-ttu-id="9ffb0-123">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="9ffb0-123">IStorageContext</span></span>

<span data-ttu-id="9ffb0-124">O parâmetro ' Context ' aceita o valor do tipo ' IStorageContext ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="9ffb0-124">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="9ffb0-125">String</span><span class="sxs-lookup"><span data-stu-id="9ffb0-125">String</span></span>

<span data-ttu-id="9ffb0-126">O parâmetro ' name ' aceita o valor do tipo ' String ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="9ffb0-126">Parameter 'Name' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="9ffb0-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9ffb0-127">OUTPUTS</span></span>

### <span data-ttu-id="9ffb0-128">Microsoft. WindowsAzure. Commands. Common. Storage. ResourceModel. AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="9ffb0-128">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageQueue</span></span>

## <span data-ttu-id="9ffb0-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9ffb0-129">NOTES</span></span>

## <span data-ttu-id="9ffb0-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9ffb0-130">RELATED LINKS</span></span>

[<span data-ttu-id="9ffb0-131">Get-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="9ffb0-131">Get-AzureStorageQueue</span></span>](./Get-AzureStorageQueue.md)

[<span data-ttu-id="9ffb0-132">Remove-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="9ffb0-132">Remove-AzureStorageQueue</span></span>](./Remove-AzureStorageQueue.md)


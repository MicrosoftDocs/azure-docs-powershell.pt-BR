---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: E9500392-6BE1-46EC-9AF5-9234281025E6
online version: ''
schema: 2.0.0
ms.openlocfilehash: 76876cb76e65c913401d62fc7f08b3cb8b5626c0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93425975"
---
# <span data-ttu-id="ad634-101">New-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="ad634-101">New-AzureStorageQueue</span></span>

## <span data-ttu-id="ad634-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ad634-102">SYNOPSIS</span></span>
<span data-ttu-id="ad634-103">Cria uma fila de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="ad634-103">Creates a storage queue.</span></span>

## <span data-ttu-id="ad634-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ad634-104">SYNTAX</span></span>

```
New-AzureStorageQueue [-Name] <String> [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="ad634-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ad634-105">DESCRIPTION</span></span>
<span data-ttu-id="ad634-106">O cmdlet **New-AzureStorageQueue** cria uma fila de armazenamento no Azure.</span><span class="sxs-lookup"><span data-stu-id="ad634-106">The **New-AzureStorageQueue** cmdlet creates a storage queue in Azure.</span></span>

## <span data-ttu-id="ad634-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ad634-107">EXAMPLES</span></span>

### <span data-ttu-id="ad634-108">Exemplo 1: criar uma fila de armazenamento do Azure</span><span class="sxs-lookup"><span data-stu-id="ad634-108">Example 1: Create an Azure storage queue</span></span>
```
PS C:\>New-AzureStorageQueue -Name "queueabc"
```

<span data-ttu-id="ad634-109">Este exemplo cria uma fila de armazenamento chamada queueabc.</span><span class="sxs-lookup"><span data-stu-id="ad634-109">This example creates a storage queue named queueabc.</span></span>

### <span data-ttu-id="ad634-110">Exemplo 2: criar várias filas de armazenamento do Azure</span><span class="sxs-lookup"><span data-stu-id="ad634-110">Example 2: Create multiple azure storage queues</span></span>
```
PS C:\>"queue1 queue2 queue3".split() | New-AzureStorageQueue
```

<span data-ttu-id="ad634-111">Este exemplo cria várias filas de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="ad634-111">This example creates multiple storage queues.</span></span>
<span data-ttu-id="ad634-112">Ele usa o método Split da classe String .NET e, em seguida, passa os nomes no pipeline.</span><span class="sxs-lookup"><span data-stu-id="ad634-112">It uses the Split method of the .NET String class and then passes the names on the pipeline.</span></span>

## <span data-ttu-id="ad634-113">OS</span><span class="sxs-lookup"><span data-stu-id="ad634-113">PARAMETERS</span></span>

### <span data-ttu-id="ad634-114">-Contexto</span><span class="sxs-lookup"><span data-stu-id="ad634-114">-Context</span></span>
<span data-ttu-id="ad634-115">Especifica o contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="ad634-115">Specifies the Azure storage context.</span></span>
<span data-ttu-id="ad634-116">Você pode criá-lo usando o cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="ad634-116">You can create it by using the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="ad634-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="ad634-117">-Name</span></span>
<span data-ttu-id="ad634-118">Especifica um nome para a fila.</span><span class="sxs-lookup"><span data-stu-id="ad634-118">Specifies a name for the queue.</span></span>

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

### <span data-ttu-id="ad634-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad634-119">CommonParameters</span></span>
<span data-ttu-id="ad634-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad634-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad634-121">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad634-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad634-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ad634-122">INPUTS</span></span>

## <span data-ttu-id="ad634-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ad634-123">OUTPUTS</span></span>

## <span data-ttu-id="ad634-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ad634-124">NOTES</span></span>

## <span data-ttu-id="ad634-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ad634-125">RELATED LINKS</span></span>

[<span data-ttu-id="ad634-126">Get-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="ad634-126">Get-AzureStorageQueue</span></span>](./Get-AzureStorageQueue.md)

[<span data-ttu-id="ad634-127">Remove-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="ad634-127">Remove-AzureStorageQueue</span></span>](./Remove-AzureStorageQueue.md)



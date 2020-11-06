---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: E9500392-6BE1-46EC-9AF5-9234281025E6
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragequeue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageQueue.md
ms.openlocfilehash: 62fc501c267e388498cb1563206d2efac083c058
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428665"
---
# <span data-ttu-id="87ca5-101">New-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="87ca5-101">New-AzureStorageQueue</span></span>

## <span data-ttu-id="87ca5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="87ca5-102">SYNOPSIS</span></span>
<span data-ttu-id="87ca5-103">Cria uma fila de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="87ca5-103">Creates a storage queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="87ca5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="87ca5-104">SYNTAX</span></span>

```
New-AzureStorageQueue [-Name] <String> [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="87ca5-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="87ca5-105">DESCRIPTION</span></span>
<span data-ttu-id="87ca5-106">O cmdlet **New-AzureStorageQueue** cria uma fila de armazenamento no Azure.</span><span class="sxs-lookup"><span data-stu-id="87ca5-106">The **New-AzureStorageQueue** cmdlet creates a storage queue in Azure.</span></span>

## <span data-ttu-id="87ca5-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="87ca5-107">EXAMPLES</span></span>

### <span data-ttu-id="87ca5-108">Exemplo 1: criar uma fila de armazenamento do Azure</span><span class="sxs-lookup"><span data-stu-id="87ca5-108">Example 1: Create an Azure storage queue</span></span>
```
PS C:\>New-AzureStorageQueue -Name "queueabc"
```

<span data-ttu-id="87ca5-109">Este exemplo cria uma fila de armazenamento chamada queueabc.</span><span class="sxs-lookup"><span data-stu-id="87ca5-109">This example creates a storage queue named queueabc.</span></span>

### <span data-ttu-id="87ca5-110">Exemplo 2: criar várias filas de armazenamento do Azure</span><span class="sxs-lookup"><span data-stu-id="87ca5-110">Example 2: Create multiple azure storage queues</span></span>
```
PS C:\>"queue1 queue2 queue3".split() | New-AzureStorageQueue
```

<span data-ttu-id="87ca5-111">Este exemplo cria várias filas de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="87ca5-111">This example creates multiple storage queues.</span></span>
<span data-ttu-id="87ca5-112">Ele usa o método Split da classe String .NET e, em seguida, passa os nomes no pipeline.</span><span class="sxs-lookup"><span data-stu-id="87ca5-112">It uses the Split method of the .NET String class and then passes the names on the pipeline.</span></span>

## <span data-ttu-id="87ca5-113">OS</span><span class="sxs-lookup"><span data-stu-id="87ca5-113">PARAMETERS</span></span>

### <span data-ttu-id="87ca5-114">-Contexto</span><span class="sxs-lookup"><span data-stu-id="87ca5-114">-Context</span></span>
<span data-ttu-id="87ca5-115">Especifica o contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="87ca5-115">Specifies the Azure storage context.</span></span>
<span data-ttu-id="87ca5-116">Você pode criá-lo usando o cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="87ca5-116">You can create it by using the New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="87ca5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87ca5-117">-DefaultProfile</span></span>
<span data-ttu-id="87ca5-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="87ca5-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="87ca5-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="87ca5-119">-Name</span></span>
<span data-ttu-id="87ca5-120">Especifica um nome para a fila.</span><span class="sxs-lookup"><span data-stu-id="87ca5-120">Specifies a name for the queue.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Queue

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="87ca5-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87ca5-121">CommonParameters</span></span>
<span data-ttu-id="87ca5-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87ca5-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87ca5-123">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87ca5-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87ca5-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="87ca5-124">INPUTS</span></span>

### <span data-ttu-id="87ca5-125">System. String</span><span class="sxs-lookup"><span data-stu-id="87ca5-125">System.String</span></span>

### <span data-ttu-id="87ca5-126">Microsoft. Azure. Commands. Common. Authentication. Abstractings. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="87ca5-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="87ca5-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="87ca5-127">OUTPUTS</span></span>

### <span data-ttu-id="87ca5-128">Microsoft. WindowsAzure. Commands. Common. Storage. ResourceModel. AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="87ca5-128">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageQueue</span></span>

## <span data-ttu-id="87ca5-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="87ca5-129">NOTES</span></span>

## <span data-ttu-id="87ca5-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="87ca5-130">RELATED LINKS</span></span>

[<span data-ttu-id="87ca5-131">Get-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="87ca5-131">Get-AzureStorageQueue</span></span>](./Get-AzureStorageQueue.md)

[<span data-ttu-id="87ca5-132">Remove-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="87ca5-132">Remove-AzureStorageQueue</span></span>](./Remove-AzureStorageQueue.md)



---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: F1EC601C-3ADD-402A-A5F7-84A95D312187
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageQueueStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageQueueStoredAccessPolicy.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: 78815aaa29c46e455f24ce0daac167b2806b6c20
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93603417"
---
# <span data-ttu-id="ad519-101">Get-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ad519-101">Get-AzureStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="ad519-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ad519-102">SYNOPSIS</span></span>
<span data-ttu-id="ad519-103">Obtém a política de acesso armazenado ou políticas para uma fila de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="ad519-103">Gets the stored access policy or policies for an Azure storage queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ad519-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ad519-104">SYNTAX</span></span>

```
Get-AzureStorageQueueStoredAccessPolicy [-Queue] <String> [[-Policy] <String>] [-Context <IStorageContext>]
 [<CommonParameters>]
```

## <span data-ttu-id="ad519-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ad519-105">DESCRIPTION</span></span>
<span data-ttu-id="ad519-106">O cmdlet **Get-AzureStorageQueueStoredAccessPolicy** lista as políticas ou políticas de acesso armazenadas para uma fila de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="ad519-106">The **Get-AzureStorageQueueStoredAccessPolicy** cmdlet lists the stored access policy or policies for an Azure storage queue.</span></span>

## <span data-ttu-id="ad519-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ad519-107">EXAMPLES</span></span>

### <span data-ttu-id="ad519-108">Exemplo 1: obter uma política de acesso armazenado na fila</span><span class="sxs-lookup"><span data-stu-id="ad519-108">Example 1: Get a stored access policy in the queue</span></span>
```
PS C:\>Get-AzureStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy12"
```

<span data-ttu-id="ad519-109">Esse comando obtém a política de acesso chamada Policy12 na fila de armazenamento chamada MyQueue.</span><span class="sxs-lookup"><span data-stu-id="ad519-109">This command gets the access policy named Policy12 in the storage queue named MyQueue.</span></span>

### <span data-ttu-id="ad519-110">Exemplo 2: obter todas as políticas de acesso armazenadas na fila</span><span class="sxs-lookup"><span data-stu-id="ad519-110">Example 2: Get all stored access policies in the queue</span></span>
```
PS C:\>Get-AzureStorageQueueStoredAccessPolicy -Queue "MyQueue"
```

<span data-ttu-id="ad519-111">Esse comando obtém todas as políticas de acesso armazenadas na fila chamada MyQueue.</span><span class="sxs-lookup"><span data-stu-id="ad519-111">This command gets all stored access policies in the queue named MyQueue.</span></span>

## <span data-ttu-id="ad519-112">OS</span><span class="sxs-lookup"><span data-stu-id="ad519-112">PARAMETERS</span></span>

### <span data-ttu-id="ad519-113">-Contexto</span><span class="sxs-lookup"><span data-stu-id="ad519-113">-Context</span></span>
<span data-ttu-id="ad519-114">Especifica o contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="ad519-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="ad519-115">Para obter um contexto de armazenamento, use o cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="ad519-115">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="ad519-116">-Política</span><span class="sxs-lookup"><span data-stu-id="ad519-116">-Policy</span></span>
<span data-ttu-id="ad519-117">Especifica uma política de acesso armazenado, que inclui as permissões para este token de assinatura de acesso compartilhado (SAS).</span><span class="sxs-lookup"><span data-stu-id="ad519-117">Specifies a stored access policy, which includes the permissions for this Shared Access Signature (SAS) token.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad519-118">-Queue</span><span class="sxs-lookup"><span data-stu-id="ad519-118">-Queue</span></span>
<span data-ttu-id="ad519-119">Especifica o nome da fila de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="ad519-119">Specifies the Azure storage queue name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ad519-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad519-120">CommonParameters</span></span>
<span data-ttu-id="ad519-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad519-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad519-122">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad519-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad519-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ad519-123">INPUTS</span></span>

### <span data-ttu-id="ad519-124">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="ad519-124">IStorageContext</span></span>

<span data-ttu-id="ad519-125">O parâmetro ' Context ' aceita o valor do tipo ' IStorageContext ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="ad519-125">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="ad519-126">String</span><span class="sxs-lookup"><span data-stu-id="ad519-126">String</span></span>

<span data-ttu-id="ad519-127">O parâmetro ' Queue ' aceita o valor do tipo ' String ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="ad519-127">Parameter 'Queue' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="ad519-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ad519-128">OUTPUTS</span></span>

### <span data-ttu-id="ad519-129">Microsoft. WindowsAzure. Storage. Queue. SharedAccessQueuePolicy</span><span class="sxs-lookup"><span data-stu-id="ad519-129">Microsoft.WindowsAzure.Storage.Queue.SharedAccessQueuePolicy</span></span>

## <span data-ttu-id="ad519-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ad519-130">NOTES</span></span>

## <span data-ttu-id="ad519-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ad519-131">RELATED LINKS</span></span>

[<span data-ttu-id="ad519-132">New-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ad519-132">New-AzureStorageQueueStoredAccessPolicy</span></span>](./New-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="ad519-133">Remove-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ad519-133">Remove-AzureStorageQueueStoredAccessPolicy</span></span>](./Remove-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="ad519-134">Set-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ad519-134">Set-AzureStorageQueueStoredAccessPolicy</span></span>](./Set-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="ad519-135">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="ad519-135">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)



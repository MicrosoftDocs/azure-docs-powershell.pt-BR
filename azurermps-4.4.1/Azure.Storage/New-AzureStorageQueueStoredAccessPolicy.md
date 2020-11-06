---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 351145AC-7C1E-4EB7-A17D-B8B7D8ED8DAB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageQueueStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageQueueStoredAccessPolicy.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: ef54976ed06eb47da803470a3d4c163a8b294743
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441436"
---
# <span data-ttu-id="4b9b7-101">New-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="4b9b7-101">New-AzureStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="4b9b7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4b9b7-102">SYNOPSIS</span></span>
<span data-ttu-id="4b9b7-103">Cria uma política de acesso armazenado para uma fila de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="4b9b7-103">Creates a stored access policy for an Azure storage queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4b9b7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4b9b7-104">SYNTAX</span></span>

```
New-AzureStorageQueueStoredAccessPolicy [-Queue] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="4b9b7-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4b9b7-105">DESCRIPTION</span></span>
<span data-ttu-id="4b9b7-106">O cmdlet **New-AzureStorageQueueStoredAccessPolicy** cria uma política de acesso armazenado para uma fila de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="4b9b7-106">The **New-AzureStorageQueueStoredAccessPolicy** cmdlet creates a stored access policy for an Azure storage queue.</span></span>

## <span data-ttu-id="4b9b7-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4b9b7-107">EXAMPLES</span></span>

### <span data-ttu-id="4b9b7-108">Exemplo 1: criar uma política de acesso armazenado em uma fila de armazenamento</span><span class="sxs-lookup"><span data-stu-id="4b9b7-108">Example 1: Create a stored access policy in a storage queue</span></span>
```
PS C:\>New-AzureStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy01"
```

<span data-ttu-id="4b9b7-109">Esse comando cria uma política de acesso chamada Policy01 na fila de armazenamento chamada MyQueue.</span><span class="sxs-lookup"><span data-stu-id="4b9b7-109">This command creates an access policy named Policy01 in the storage queue named MyQueue.</span></span>

## <span data-ttu-id="4b9b7-110">OS</span><span class="sxs-lookup"><span data-stu-id="4b9b7-110">PARAMETERS</span></span>

### <span data-ttu-id="4b9b7-111">-Contexto</span><span class="sxs-lookup"><span data-stu-id="4b9b7-111">-Context</span></span>
<span data-ttu-id="4b9b7-112">Especifica um contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="4b9b7-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="4b9b7-113">Para obter um contexto de armazenamento, use o cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="4b9b7-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="4b9b7-114">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="4b9b7-114">-ExpiryTime</span></span>
<span data-ttu-id="4b9b7-115">Especifica o tempo em que a política de acesso armazenado se torna inválida.</span><span class="sxs-lookup"><span data-stu-id="4b9b7-115">Specifies the time at which the stored access policy becomes invalid.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b9b7-116">-Permissão</span><span class="sxs-lookup"><span data-stu-id="4b9b7-116">-Permission</span></span>
<span data-ttu-id="4b9b7-117">Especifica as permissões na política de acesso armazenado para acessar a fila de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="4b9b7-117">Specifies permissions in the stored access policy to access the storage queue.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b9b7-118">-Política</span><span class="sxs-lookup"><span data-stu-id="4b9b7-118">-Policy</span></span>
<span data-ttu-id="4b9b7-119">Especifica um nome para a política de acesso armazenada.</span><span class="sxs-lookup"><span data-stu-id="4b9b7-119">Specifies a name for the stored access policy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b9b7-120">-Queue</span><span class="sxs-lookup"><span data-stu-id="4b9b7-120">-Queue</span></span>
<span data-ttu-id="4b9b7-121">Especifica o nome da fila de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="4b9b7-121">Specifies the Azure storage queue name.</span></span>

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

### <span data-ttu-id="4b9b7-122">-StartTime</span><span class="sxs-lookup"><span data-stu-id="4b9b7-122">-StartTime</span></span>
<span data-ttu-id="4b9b7-123">Especifica a hora em que a política de acesso armazenado se torna válida.</span><span class="sxs-lookup"><span data-stu-id="4b9b7-123">Specifies the time at which the stored access policy becomes valid.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b9b7-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b9b7-124">CommonParameters</span></span>
<span data-ttu-id="4b9b7-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b9b7-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b9b7-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4b9b7-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b9b7-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4b9b7-127">INPUTS</span></span>

### <span data-ttu-id="4b9b7-128">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="4b9b7-128">IStorageContext</span></span>

<span data-ttu-id="4b9b7-129">O parâmetro ' Context ' aceita o valor do tipo ' IStorageContext ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="4b9b7-129">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="4b9b7-130">String</span><span class="sxs-lookup"><span data-stu-id="4b9b7-130">String</span></span>

<span data-ttu-id="4b9b7-131">O parâmetro ' Queue ' aceita o valor do tipo ' String ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="4b9b7-131">Parameter 'Queue' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="4b9b7-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4b9b7-132">OUTPUTS</span></span>

### <span data-ttu-id="4b9b7-133">System. String</span><span class="sxs-lookup"><span data-stu-id="4b9b7-133">System.String</span></span>

## <span data-ttu-id="4b9b7-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4b9b7-134">NOTES</span></span>

## <span data-ttu-id="4b9b7-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4b9b7-135">RELATED LINKS</span></span>

[<span data-ttu-id="4b9b7-136">Get-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="4b9b7-136">Get-AzureStorageQueueStoredAccessPolicy</span></span>](./Get-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="4b9b7-137">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="4b9b7-137">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="4b9b7-138">Remove-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="4b9b7-138">Remove-AzureStorageQueueStoredAccessPolicy</span></span>](./Remove-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="4b9b7-139">Set-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="4b9b7-139">Set-AzureStorageQueueStoredAccessPolicy</span></span>](./Set-AzureStorageQueueStoredAccessPolicy.md)



---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: CF3B6E3B-3FC1-4871-AFE0-366B17A9E4F8
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragetablestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageTableStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageTableStoredAccessPolicy.md
ms.openlocfilehash: 163c6ba0841b19edc76421259b1cd9cc8411e35e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430556"
---
# <span data-ttu-id="3274f-101">New-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="3274f-101">New-AzureStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="3274f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3274f-102">SYNOPSIS</span></span>
<span data-ttu-id="3274f-103">Cria uma política de acesso armazenado para uma tabela de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="3274f-103">Creates a stored access policy for an Azure storage table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3274f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3274f-104">SYNTAX</span></span>

```
New-AzureStorageTableStoredAccessPolicy [-Table] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="3274f-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3274f-105">DESCRIPTION</span></span>
<span data-ttu-id="3274f-106">O cmdlet **New-AzureStorageTableStoredAccessPolicy** cria uma política de acesso armazenado para uma tabela de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="3274f-106">The **New-AzureStorageTableStoredAccessPolicy** cmdlet creates a stored access policy for an Azure storage table.</span></span>

## <span data-ttu-id="3274f-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3274f-107">EXAMPLES</span></span>

### <span data-ttu-id="3274f-108">Exemplo 1: criar uma política de acesso armazenada em uma tabela</span><span class="sxs-lookup"><span data-stu-id="3274f-108">Example 1: Create a stored access policy in a table</span></span>
```
PS C:\>New-AzureStorageTableStoredAccessPolicy -Table "MyTable" -Policy "Policy02"
```

<span data-ttu-id="3274f-109">Esse comando cria uma política de acesso chamada Policy02 na tabela armazenamento chamada MyTable.</span><span class="sxs-lookup"><span data-stu-id="3274f-109">This command creates an access policy named Policy02 in the storage table named MyTable.</span></span>

## <span data-ttu-id="3274f-110">OS</span><span class="sxs-lookup"><span data-stu-id="3274f-110">PARAMETERS</span></span>

### <span data-ttu-id="3274f-111">-Contexto</span><span class="sxs-lookup"><span data-stu-id="3274f-111">-Context</span></span>
<span data-ttu-id="3274f-112">Especifica um contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="3274f-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="3274f-113">Para obter um contexto de armazenamento, use o cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="3274f-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="3274f-114">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="3274f-114">-ExpiryTime</span></span>
<span data-ttu-id="3274f-115">Especifica o tempo em que a política de acesso armazenado se torna inválida.</span><span class="sxs-lookup"><span data-stu-id="3274f-115">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="3274f-116">-Permissão</span><span class="sxs-lookup"><span data-stu-id="3274f-116">-Permission</span></span>
<span data-ttu-id="3274f-117">Especifica as permissões na política de acesso armazenado para acessar a tabela de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="3274f-117">Specifies permissions in the stored access policy to access the storage table.</span></span>

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

### <span data-ttu-id="3274f-118">-Política</span><span class="sxs-lookup"><span data-stu-id="3274f-118">-Policy</span></span>
<span data-ttu-id="3274f-119">Especifica um nome para a política de acesso armazenada.</span><span class="sxs-lookup"><span data-stu-id="3274f-119">Specifies a name for the stored access policy.</span></span>

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

### <span data-ttu-id="3274f-120">-StartTime</span><span class="sxs-lookup"><span data-stu-id="3274f-120">-StartTime</span></span>
<span data-ttu-id="3274f-121">Especifica a hora em que a política de acesso armazenado se torna válida.</span><span class="sxs-lookup"><span data-stu-id="3274f-121">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="3274f-122">-Tabela</span><span class="sxs-lookup"><span data-stu-id="3274f-122">-Table</span></span>
<span data-ttu-id="3274f-123">Especifica o nome da tabela de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="3274f-123">Specifies the Azure storage table name.</span></span>

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

### <span data-ttu-id="3274f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3274f-124">CommonParameters</span></span>
<span data-ttu-id="3274f-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3274f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3274f-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3274f-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3274f-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3274f-127">INPUTS</span></span>

### <span data-ttu-id="3274f-128">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="3274f-128">IStorageContext</span></span>

<span data-ttu-id="3274f-129">O parâmetro ' Context ' aceita o valor do tipo ' IStorageContext ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="3274f-129">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="3274f-130">String</span><span class="sxs-lookup"><span data-stu-id="3274f-130">String</span></span>

<span data-ttu-id="3274f-131">O parâmetro ' Table ' aceita o valor do tipo ' String ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="3274f-131">Parameter 'Table' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="3274f-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3274f-132">OUTPUTS</span></span>

### <span data-ttu-id="3274f-133">System. String</span><span class="sxs-lookup"><span data-stu-id="3274f-133">System.String</span></span>

## <span data-ttu-id="3274f-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3274f-134">NOTES</span></span>

## <span data-ttu-id="3274f-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3274f-135">RELATED LINKS</span></span>

[<span data-ttu-id="3274f-136">Get-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="3274f-136">Get-AzureStorageTableStoredAccessPolicy</span></span>](./Get-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="3274f-137">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="3274f-137">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="3274f-138">Remove-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="3274f-138">Remove-AzureStorageTableStoredAccessPolicy</span></span>](./Remove-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="3274f-139">Set-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="3274f-139">Set-AzureStorageTableStoredAccessPolicy</span></span>](./Set-AzureStorageTableStoredAccessPolicy.md)



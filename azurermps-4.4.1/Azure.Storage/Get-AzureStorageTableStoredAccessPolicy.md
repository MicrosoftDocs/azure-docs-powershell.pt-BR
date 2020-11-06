---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: BF5526C1-11B9-47A8-A5A6-CB275B470A9E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageTableStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageTableStoredAccessPolicy.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: 85501affef70ce0cf31e62f9083d5ed383425497
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602081"
---
# <span data-ttu-id="a3fef-101">Get-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="a3fef-101">Get-AzureStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="a3fef-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a3fef-102">SYNOPSIS</span></span>
<span data-ttu-id="a3fef-103">Obtém a política de acesso armazenado ou políticas para uma tabela de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="a3fef-103">Gets the stored access policy or policies for an Azure storage table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a3fef-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a3fef-104">SYNTAX</span></span>

```
Get-AzureStorageTableStoredAccessPolicy [-Table] <String> [[-Policy] <String>] [-Context <IStorageContext>]
 [<CommonParameters>]
```

## <span data-ttu-id="a3fef-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a3fef-105">DESCRIPTION</span></span>
<span data-ttu-id="a3fef-106">O cmdlet **Get-AzureStorageTableStoredAccessPolicy** lista as políticas ou políticas de acesso armazenadas para uma tabela de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="a3fef-106">The **Get-AzureStorageTableStoredAccessPolicy** cmdlet lists the stored access policy or policies for an Azure storage table.</span></span>

## <span data-ttu-id="a3fef-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a3fef-107">EXAMPLES</span></span>

### <span data-ttu-id="a3fef-108">Exemplo 1: obter uma política de acesso armazenado em uma tabela de armazenamento</span><span class="sxs-lookup"><span data-stu-id="a3fef-108">Example 1: Get a stored access policy in a storage table</span></span>
```
PS C:\>Get-AzureStorageTableStoredAccessPolicy -Table "Table02" -Policy "Policy50"
```

<span data-ttu-id="a3fef-109">Esse comando obtém a política de acesso chamada Policy50 na tabela armazenamento chamada Table02.</span><span class="sxs-lookup"><span data-stu-id="a3fef-109">This command gets the access policy named Policy50 in the storage table named Table02.</span></span>

### <span data-ttu-id="a3fef-110">Exemplo 2: obter todas as políticas de acesso armazenadas em uma tabela de armazenamento</span><span class="sxs-lookup"><span data-stu-id="a3fef-110">Example 2: Get all stored access policies in a storage table</span></span>
```
PS C:\>Get-AzureStorageTableStoredAccessPolicy -Table "Table02"
```

<span data-ttu-id="a3fef-111">Esse comando obtém todas as políticas de acesso na tabela chamada Table02.</span><span class="sxs-lookup"><span data-stu-id="a3fef-111">This command gets all access policies in the table named Table02.</span></span>

## <span data-ttu-id="a3fef-112">OS</span><span class="sxs-lookup"><span data-stu-id="a3fef-112">PARAMETERS</span></span>

### <span data-ttu-id="a3fef-113">-Contexto</span><span class="sxs-lookup"><span data-stu-id="a3fef-113">-Context</span></span>
<span data-ttu-id="a3fef-114">Especifica o contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="a3fef-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="a3fef-115">Para obter um contexto de armazenamento, use o cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="a3fef-115">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="a3fef-116">-Política</span><span class="sxs-lookup"><span data-stu-id="a3fef-116">-Policy</span></span>
<span data-ttu-id="a3fef-117">Especifica uma política de acesso armazenado, que inclui as permissões para este token de assinatura de acesso compartilhado (SAS).</span><span class="sxs-lookup"><span data-stu-id="a3fef-117">Specifies a stored access policy, which includes the permissions for this Shared Access Signature (SAS) token.</span></span>

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

### <span data-ttu-id="a3fef-118">-Tabela</span><span class="sxs-lookup"><span data-stu-id="a3fef-118">-Table</span></span>
<span data-ttu-id="a3fef-119">Especifica o nome da tabela de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="a3fef-119">Specifies the Azure storage table name.</span></span>

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

### <span data-ttu-id="a3fef-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3fef-120">CommonParameters</span></span>
<span data-ttu-id="a3fef-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3fef-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3fef-122">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a3fef-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3fef-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a3fef-123">INPUTS</span></span>

### <span data-ttu-id="a3fef-124">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="a3fef-124">IStorageContext</span></span>

<span data-ttu-id="a3fef-125">O parâmetro ' Context ' aceita o valor do tipo ' IStorageContext ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="a3fef-125">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="a3fef-126">String</span><span class="sxs-lookup"><span data-stu-id="a3fef-126">String</span></span>

<span data-ttu-id="a3fef-127">O parâmetro ' Table ' aceita o valor do tipo ' String ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="a3fef-127">Parameter 'Table' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="a3fef-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a3fef-128">OUTPUTS</span></span>

### <span data-ttu-id="a3fef-129">Microsoft. WindowsAzure. Storage. Table. SharedAccessTablePolicy</span><span class="sxs-lookup"><span data-stu-id="a3fef-129">Microsoft.WindowsAzure.Storage.Table.SharedAccessTablePolicy</span></span>

## <span data-ttu-id="a3fef-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a3fef-130">NOTES</span></span>

## <span data-ttu-id="a3fef-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a3fef-131">RELATED LINKS</span></span>

[<span data-ttu-id="a3fef-132">New-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="a3fef-132">New-AzureStorageTableStoredAccessPolicy</span></span>](./New-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="a3fef-133">Remove-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="a3fef-133">Remove-AzureStorageTableStoredAccessPolicy</span></span>](./Remove-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="a3fef-134">Set-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="a3fef-134">Set-AzureStorageTableStoredAccessPolicy</span></span>](./Set-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="a3fef-135">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="a3fef-135">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)



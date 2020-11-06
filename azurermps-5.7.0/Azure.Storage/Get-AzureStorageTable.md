---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 4631D36F-926A-4279-AA4D-5F694C18081E
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestoragetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageTable.md
ms.openlocfilehash: ac25103ed8a933af4e118087371511842044b6a5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430572"
---
# <span data-ttu-id="4ecd4-101">Get-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="4ecd4-101">Get-AzureStorageTable</span></span>

## <span data-ttu-id="4ecd4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4ecd4-102">SYNOPSIS</span></span>
<span data-ttu-id="4ecd4-103">Lista as tabelas de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="4ecd4-103">Lists the storage tables.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4ecd4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4ecd4-104">SYNTAX</span></span>

### <span data-ttu-id="4ecd4-105">TableName (padrão)</span><span class="sxs-lookup"><span data-stu-id="4ecd4-105">TableName (Default)</span></span>
```
Get-AzureStorageTable [[-Name] <String>] [-Context <IStorageContext>] [<CommonParameters>]
```

### <span data-ttu-id="4ecd4-106">TablePrefix</span><span class="sxs-lookup"><span data-stu-id="4ecd4-106">TablePrefix</span></span>
```
Get-AzureStorageTable -Prefix <String> [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="4ecd4-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4ecd4-107">DESCRIPTION</span></span>
<span data-ttu-id="4ecd4-108">O cmdlet **Get-AzureStorageTable** lista as tabelas de armazenamento associadas à conta de armazenamento no Azure.</span><span class="sxs-lookup"><span data-stu-id="4ecd4-108">The **Get-AzureStorageTable** cmdlet lists the storage tables associated with the storage account in Azure.</span></span>

## <span data-ttu-id="4ecd4-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4ecd4-109">EXAMPLES</span></span>

### <span data-ttu-id="4ecd4-110">Exemplo 1: listar todas as tabelas de armazenamento do Azure</span><span class="sxs-lookup"><span data-stu-id="4ecd4-110">Example 1: List all Azure Storage tables</span></span>
```
PS C:\>Get-AzureStorageTable
```

<span data-ttu-id="4ecd4-111">Este comando obtém todas as tabelas de armazenamento de uma conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="4ecd4-111">This command gets all storage tables for a Storage account.</span></span>

### <span data-ttu-id="4ecd4-112">Exemplo 2: listar tabelas de armazenamento do Azure usando um caractere curinga</span><span class="sxs-lookup"><span data-stu-id="4ecd4-112">Example 2: List Azure Storage tables using a wildcard character</span></span>
```
PS C:\>Get-AzureStorageTable -Name table*
```

<span data-ttu-id="4ecd4-113">Esse comando usa um caractere curinga para obter tabelas de armazenamento cujo nome começa com Table.</span><span class="sxs-lookup"><span data-stu-id="4ecd4-113">This command uses a wildcard character to get storage tables whose name starts with table.</span></span>

### <span data-ttu-id="4ecd4-114">Exemplo 3: listar tabelas de armazenamento do Azure usando prefixo de nome de tabela</span><span class="sxs-lookup"><span data-stu-id="4ecd4-114">Example 3: List Azure Storage tables using table name prefix</span></span>
```
PS C:\>Get-AzureStorageTable -Prefix "table"
```

<span data-ttu-id="4ecd4-115">Esse comando usa o parâmetro *prefix* para obter tabelas de armazenamento cujo nome começa com Table.</span><span class="sxs-lookup"><span data-stu-id="4ecd4-115">This command uses the *Prefix* parameter to get storage tables whose name starts with table.</span></span>

## <span data-ttu-id="4ecd4-116">OS</span><span class="sxs-lookup"><span data-stu-id="4ecd4-116">PARAMETERS</span></span>

### <span data-ttu-id="4ecd4-117">-Contexto</span><span class="sxs-lookup"><span data-stu-id="4ecd4-117">-Context</span></span>
<span data-ttu-id="4ecd4-118">Especifica o contexto de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="4ecd4-118">Specifies the storage context.</span></span>
<span data-ttu-id="4ecd4-119">Para criá-la, você pode usar o cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="4ecd4-119">To create it, you can use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="4ecd4-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="4ecd4-120">-Name</span></span>
<span data-ttu-id="4ecd4-121">Especifica o nome da tabela.</span><span class="sxs-lookup"><span data-stu-id="4ecd4-121">Specifies the table name.</span></span>
<span data-ttu-id="4ecd4-122">Se o nome da tabela estiver vazio, o cmdlet lista todas as tabelas.</span><span class="sxs-lookup"><span data-stu-id="4ecd4-122">If the table name is empty, the cmdlet lists all the tables.</span></span>
<span data-ttu-id="4ecd4-123">Caso contrário, ele lista todas as tabelas que correspondem ao nome especificado ou o padrão normal Name.</span><span class="sxs-lookup"><span data-stu-id="4ecd4-123">Otherwise, it lists all tables that match the specified name or the regular name pattern.</span></span>

```yaml
Type: String
Parameter Sets: TableName
Aliases: N, Table

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: True
```

### <span data-ttu-id="4ecd4-124">-Prefix</span><span class="sxs-lookup"><span data-stu-id="4ecd4-124">-Prefix</span></span>
<span data-ttu-id="4ecd4-125">Especifica um prefixo usado no nome da tabela ou tabelas que você deseja obter.</span><span class="sxs-lookup"><span data-stu-id="4ecd4-125">Specifies a prefix used in the name of the table or tables you want to get.</span></span>
<span data-ttu-id="4ecd4-126">Você pode usar isso para localizar todas as tabelas que começam com a mesma cadeia de caracteres, como Table.</span><span class="sxs-lookup"><span data-stu-id="4ecd4-126">You can use this to find all tables that start with the same string, such as table.</span></span>

```yaml
Type: String
Parameter Sets: TablePrefix
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ecd4-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ecd4-127">CommonParameters</span></span>
<span data-ttu-id="4ecd4-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ecd4-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ecd4-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ecd4-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ecd4-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4ecd4-130">INPUTS</span></span>

### <span data-ttu-id="4ecd4-131">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="4ecd4-131">IStorageContext</span></span>

<span data-ttu-id="4ecd4-132">O parâmetro ' Context ' aceita o valor do tipo ' IStorageContext ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="4ecd4-132">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="4ecd4-133">String</span><span class="sxs-lookup"><span data-stu-id="4ecd4-133">String</span></span>

<span data-ttu-id="4ecd4-134">O parâmetro ' name ' aceita o valor do tipo ' String ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="4ecd4-134">Parameter 'Name' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="4ecd4-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4ecd4-135">OUTPUTS</span></span>

### <span data-ttu-id="4ecd4-136">Microsoft. WindowsAzure. Commands. Common. Storage. ResourceModel. AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="4ecd4-136">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageTable</span></span>

## <span data-ttu-id="4ecd4-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4ecd4-137">NOTES</span></span>

## <span data-ttu-id="4ecd4-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4ecd4-138">RELATED LINKS</span></span>

[<span data-ttu-id="4ecd4-139">New-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="4ecd4-139">New-AzureStorageTable</span></span>](./New-AzureStorageTable.md)

[<span data-ttu-id="4ecd4-140">Remove-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="4ecd4-140">Remove-AzureStorageTable</span></span>](./Remove-AzureStorageTable.md)


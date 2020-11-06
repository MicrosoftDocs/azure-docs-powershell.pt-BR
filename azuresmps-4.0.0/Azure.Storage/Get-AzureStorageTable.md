---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 4631D36F-926A-4279-AA4D-5F694C18081E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3f2bccab190fc27b5e97ecf3af502d3488f28998
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93426139"
---
# <span data-ttu-id="70b1b-101">Get-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="70b1b-101">Get-AzureStorageTable</span></span>

## <span data-ttu-id="70b1b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="70b1b-102">SYNOPSIS</span></span>
<span data-ttu-id="70b1b-103">Lista as tabelas de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="70b1b-103">Lists the storage tables.</span></span>

## <span data-ttu-id="70b1b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="70b1b-104">SYNTAX</span></span>

### <span data-ttu-id="70b1b-105">TableName (padrão)</span><span class="sxs-lookup"><span data-stu-id="70b1b-105">TableName (Default)</span></span>
```
Get-AzureStorageTable [[-Name] <String>] [-Context <IStorageContext>] [<CommonParameters>]
```

### <span data-ttu-id="70b1b-106">TablePrefix</span><span class="sxs-lookup"><span data-stu-id="70b1b-106">TablePrefix</span></span>
```
Get-AzureStorageTable -Prefix <String> [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="70b1b-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="70b1b-107">DESCRIPTION</span></span>
<span data-ttu-id="70b1b-108">O cmdlet **Get-AzureStorageTable** lista as tabelas de armazenamento associadas à conta de armazenamento no Azure.</span><span class="sxs-lookup"><span data-stu-id="70b1b-108">The **Get-AzureStorageTable** cmdlet lists the storage tables associated with the storage account in Azure.</span></span>

## <span data-ttu-id="70b1b-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="70b1b-109">EXAMPLES</span></span>

### <span data-ttu-id="70b1b-110">Exemplo 1: listar todas as tabelas de armazenamento do Azure</span><span class="sxs-lookup"><span data-stu-id="70b1b-110">Example 1: List all Azure Storage tables</span></span>
```
PS C:\>Get-AzureStorageTable
```

<span data-ttu-id="70b1b-111">Este comando obtém todas as tabelas de armazenamento de uma conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="70b1b-111">This command gets all storage tables for a Storage account.</span></span>

### <span data-ttu-id="70b1b-112">Exemplo 2: listar tabelas de armazenamento do Azure usando um caractere curinga</span><span class="sxs-lookup"><span data-stu-id="70b1b-112">Example 2: List Azure Storage tables using a wildcard character</span></span>
```
PS C:\>Get-AzureStorageTable -Name table*
```

<span data-ttu-id="70b1b-113">Esse comando usa um caractere curinga para obter tabelas de armazenamento cujo nome começa com Table.</span><span class="sxs-lookup"><span data-stu-id="70b1b-113">This command uses a wildcard character to get storage tables whose name starts with table.</span></span>

### <span data-ttu-id="70b1b-114">Exemplo 3: listar tabelas de armazenamento do Azure usando prefixo de nome de tabela</span><span class="sxs-lookup"><span data-stu-id="70b1b-114">Example 3: List Azure Storage tables using table name prefix</span></span>
```
PS C:\>Get-AzureStorageTable -Prefix "table"
```

<span data-ttu-id="70b1b-115">Esse comando usa o parâmetro *prefix* para obter tabelas de armazenamento cujo nome começa com Table.</span><span class="sxs-lookup"><span data-stu-id="70b1b-115">This command uses the *Prefix* parameter to get storage tables whose name starts with table.</span></span>

## <span data-ttu-id="70b1b-116">OS</span><span class="sxs-lookup"><span data-stu-id="70b1b-116">PARAMETERS</span></span>

### <span data-ttu-id="70b1b-117">-Contexto</span><span class="sxs-lookup"><span data-stu-id="70b1b-117">-Context</span></span>
<span data-ttu-id="70b1b-118">Especifica o contexto de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="70b1b-118">Specifies the storage context.</span></span>
<span data-ttu-id="70b1b-119">Para criá-la, você pode usar o cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="70b1b-119">To create it, you can use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="70b1b-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="70b1b-120">-Name</span></span>
<span data-ttu-id="70b1b-121">Especifica o nome da tabela.</span><span class="sxs-lookup"><span data-stu-id="70b1b-121">Specifies the table name.</span></span>
<span data-ttu-id="70b1b-122">Se o nome da tabela estiver vazio, o cmdlet lista todas as tabelas.</span><span class="sxs-lookup"><span data-stu-id="70b1b-122">If the table name is empty, the cmdlet lists all the tables.</span></span>
<span data-ttu-id="70b1b-123">Caso contrário, ele lista todas as tabelas que correspondem ao nome especificado ou o padrão normal Name.</span><span class="sxs-lookup"><span data-stu-id="70b1b-123">Otherwise, it lists all tables that match the specified name or the regular name pattern.</span></span>

```yaml
Type: String
Parameter Sets: TableName
Aliases: N, Table

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="70b1b-124">-Prefix</span><span class="sxs-lookup"><span data-stu-id="70b1b-124">-Prefix</span></span>
<span data-ttu-id="70b1b-125">Especifica um prefixo usado no nome da tabela ou tabelas que você deseja obter.</span><span class="sxs-lookup"><span data-stu-id="70b1b-125">Specifies a prefix used in the name of the table or tables you want to get.</span></span>
<span data-ttu-id="70b1b-126">Você pode usar isso para localizar todas as tabelas que começam com a mesma cadeia de caracteres, como Table.</span><span class="sxs-lookup"><span data-stu-id="70b1b-126">You can use this to find all tables that start with the same string, such as table.</span></span>

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

### <span data-ttu-id="70b1b-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70b1b-127">CommonParameters</span></span>
<span data-ttu-id="70b1b-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70b1b-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70b1b-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="70b1b-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70b1b-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="70b1b-130">INPUTS</span></span>

## <span data-ttu-id="70b1b-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="70b1b-131">OUTPUTS</span></span>

## <span data-ttu-id="70b1b-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="70b1b-132">NOTES</span></span>

## <span data-ttu-id="70b1b-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="70b1b-133">RELATED LINKS</span></span>

[<span data-ttu-id="70b1b-134">New-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="70b1b-134">New-AzureStorageTable</span></span>](./New-AzureStorageTable.md)

[<span data-ttu-id="70b1b-135">Remove-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="70b1b-135">Remove-AzureStorageTable</span></span>](./Remove-AzureStorageTable.md)



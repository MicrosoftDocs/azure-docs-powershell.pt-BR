---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 3B4F32F3-51ED-4851-B38F-172658186C96
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9a58f869d5308b176a68614cbb2fa2fec401fa14
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93426064"
---
# <span data-ttu-id="5f186-101">New-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="5f186-101">New-AzureStorageTable</span></span>

## <span data-ttu-id="5f186-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5f186-102">SYNOPSIS</span></span>
<span data-ttu-id="5f186-103">Cria uma tabela de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="5f186-103">Creates a storage table.</span></span>

## <span data-ttu-id="5f186-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5f186-104">SYNTAX</span></span>

```
New-AzureStorageTable [-Name] <String> [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="5f186-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5f186-105">DESCRIPTION</span></span>
<span data-ttu-id="5f186-106">O cmdlet **New-AzureStorageTable** cria uma tabela de armazenamento associada à conta de armazenamento no Azure.</span><span class="sxs-lookup"><span data-stu-id="5f186-106">The **New-AzureStorageTable** cmdlet creates a storage table associated with the storage account in Azure.</span></span>

## <span data-ttu-id="5f186-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5f186-107">EXAMPLES</span></span>

### <span data-ttu-id="5f186-108">Exemplo 1: criar uma tabela de armazenamento do Azure</span><span class="sxs-lookup"><span data-stu-id="5f186-108">Example 1: Create an azure storage table</span></span>
```
PS C:\>New-AzureStorageTable -Name "tableabc"
```

<span data-ttu-id="5f186-109">Esse comando cria uma tabela de armazenamento com um nome de tableabc.</span><span class="sxs-lookup"><span data-stu-id="5f186-109">This command creates a storage table with a name of tableabc.</span></span>

### <span data-ttu-id="5f186-110">Exemplo 2: criar várias tabelas de armazenamento do Azure</span><span class="sxs-lookup"><span data-stu-id="5f186-110">Example 2: Create multiple azure storage tables</span></span>
```
PS C:\>"table1 table2 table3".split() | New-AzureStorageTable
```

<span data-ttu-id="5f186-111">Esse comando cria várias tabelas.</span><span class="sxs-lookup"><span data-stu-id="5f186-111">This command creates multiple tables.</span></span>
<span data-ttu-id="5f186-112">Ele usa o método **Split** da classe **String** .net e, em seguida, passa os nomes no pipeline.</span><span class="sxs-lookup"><span data-stu-id="5f186-112">It uses the **Split** method of the .NET **String** class and then passes the names on the pipeline.</span></span>

## <span data-ttu-id="5f186-113">OS</span><span class="sxs-lookup"><span data-stu-id="5f186-113">PARAMETERS</span></span>

### <span data-ttu-id="5f186-114">-Contexto</span><span class="sxs-lookup"><span data-stu-id="5f186-114">-Context</span></span>
<span data-ttu-id="5f186-115">Especifica o contexto de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="5f186-115">Specifies the storage context.</span></span>
<span data-ttu-id="5f186-116">Para criá-la, você pode usar o cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="5f186-116">To create it, you can use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="5f186-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="5f186-117">-Name</span></span>
<span data-ttu-id="5f186-118">Especifica um nome para a nova tabela.</span><span class="sxs-lookup"><span data-stu-id="5f186-118">Specifies a name for the new table.</span></span>

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

### <span data-ttu-id="5f186-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f186-119">CommonParameters</span></span>
<span data-ttu-id="5f186-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f186-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f186-121">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5f186-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f186-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5f186-122">INPUTS</span></span>

## <span data-ttu-id="5f186-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5f186-123">OUTPUTS</span></span>

## <span data-ttu-id="5f186-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5f186-124">NOTES</span></span>

## <span data-ttu-id="5f186-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5f186-125">RELATED LINKS</span></span>

[<span data-ttu-id="5f186-126">Get-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="5f186-126">Get-AzureStorageTable</span></span>](./Get-AzureStorageTable.md)

[<span data-ttu-id="5f186-127">Remove-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="5f186-127">Remove-AzureStorageTable</span></span>](./Remove-AzureStorageTable.md)



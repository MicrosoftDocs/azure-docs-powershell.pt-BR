---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 3B4F32F3-51ED-4851-B38F-172658186C96
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageTable.md
ms.openlocfilehash: 14f42ae951fe25f7594eb6e314ac65bb678e29c0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427362"
---
# <span data-ttu-id="15706-101">New-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="15706-101">New-AzureStorageTable</span></span>

## <span data-ttu-id="15706-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="15706-102">SYNOPSIS</span></span>
<span data-ttu-id="15706-103">Cria uma tabela de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="15706-103">Creates a storage table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="15706-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="15706-104">SYNTAX</span></span>

```
New-AzureStorageTable [-Name] <String> [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="15706-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="15706-105">DESCRIPTION</span></span>
<span data-ttu-id="15706-106">O cmdlet **New-AzureStorageTable** cria uma tabela de armazenamento associada à conta de armazenamento no Azure.</span><span class="sxs-lookup"><span data-stu-id="15706-106">The **New-AzureStorageTable** cmdlet creates a storage table associated with the storage account in Azure.</span></span>

## <span data-ttu-id="15706-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="15706-107">EXAMPLES</span></span>

### <span data-ttu-id="15706-108">Exemplo 1: criar uma tabela de armazenamento do Azure</span><span class="sxs-lookup"><span data-stu-id="15706-108">Example 1: Create an azure storage table</span></span>
```
PS C:\>New-AzureStorageTable -Name "tableabc"
```

<span data-ttu-id="15706-109">Esse comando cria uma tabela de armazenamento com um nome de tableabc.</span><span class="sxs-lookup"><span data-stu-id="15706-109">This command creates a storage table with a name of tableabc.</span></span>

### <span data-ttu-id="15706-110">Exemplo 2: criar várias tabelas de armazenamento do Azure</span><span class="sxs-lookup"><span data-stu-id="15706-110">Example 2: Create multiple azure storage tables</span></span>
```
PS C:\>"table1 table2 table3".split() | New-AzureStorageTable
```

<span data-ttu-id="15706-111">Esse comando cria várias tabelas.</span><span class="sxs-lookup"><span data-stu-id="15706-111">This command creates multiple tables.</span></span>
<span data-ttu-id="15706-112">Ele usa o método **Split** da classe **String** .net e, em seguida, passa os nomes no pipeline.</span><span class="sxs-lookup"><span data-stu-id="15706-112">It uses the **Split** method of the .NET **String** class and then passes the names on the pipeline.</span></span>

## <span data-ttu-id="15706-113">OS</span><span class="sxs-lookup"><span data-stu-id="15706-113">PARAMETERS</span></span>

### <span data-ttu-id="15706-114">-Contexto</span><span class="sxs-lookup"><span data-stu-id="15706-114">-Context</span></span>
<span data-ttu-id="15706-115">Especifica o contexto de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="15706-115">Specifies the storage context.</span></span>
<span data-ttu-id="15706-116">Para criá-la, você pode usar o cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="15706-116">To create it, you can use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="15706-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15706-117">-DefaultProfile</span></span>
<span data-ttu-id="15706-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="15706-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="15706-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="15706-119">-Name</span></span>
<span data-ttu-id="15706-120">Especifica um nome para a nova tabela.</span><span class="sxs-lookup"><span data-stu-id="15706-120">Specifies a name for the new table.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Table

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="15706-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15706-121">CommonParameters</span></span>
<span data-ttu-id="15706-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="15706-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15706-123">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="15706-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15706-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="15706-124">INPUTS</span></span>

### <span data-ttu-id="15706-125">System. String</span><span class="sxs-lookup"><span data-stu-id="15706-125">System.String</span></span>

### <span data-ttu-id="15706-126">Microsoft. Azure. Commands. Common. Authentication. Abstractings. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="15706-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="15706-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="15706-127">OUTPUTS</span></span>

### <span data-ttu-id="15706-128">Microsoft. WindowsAzure. Commands. Common. Storage. ResourceModel. AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="15706-128">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageTable</span></span>

## <span data-ttu-id="15706-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="15706-129">NOTES</span></span>

## <span data-ttu-id="15706-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="15706-130">RELATED LINKS</span></span>

[<span data-ttu-id="15706-131">Get-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="15706-131">Get-AzureStorageTable</span></span>](./Get-AzureStorageTable.md)

[<span data-ttu-id="15706-132">Remove-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="15706-132">Remove-AzureStorageTable</span></span>](./Remove-AzureStorageTable.md)



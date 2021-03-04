---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 3B4F32F3-51ED-4851-B38F-172658186C96
online version: https://docs.microsoft.com/powershell/module/az.storage/new-azstoragetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageTable.md
ms.openlocfilehash: 84b5389c4f9b404b4b74783184143af310bf1ba5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891942"
---
# <span data-ttu-id="78672-101">New-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="78672-101">New-AzStorageTable</span></span>

## <span data-ttu-id="78672-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="78672-102">SYNOPSIS</span></span>
<span data-ttu-id="78672-103">Cria uma tabela de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="78672-103">Creates a storage table.</span></span>

## <span data-ttu-id="78672-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="78672-104">SYNTAX</span></span>

```
New-AzStorageTable [-Name] <String> [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="78672-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="78672-105">DESCRIPTION</span></span>
<span data-ttu-id="78672-106">O cmdlet **New-AzStorageTable** cria uma tabela de armazenamento associada à conta de armazenamento no Azure.</span><span class="sxs-lookup"><span data-stu-id="78672-106">The **New-AzStorageTable** cmdlet creates a storage table associated with the storage account in Azure.</span></span>

## <span data-ttu-id="78672-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="78672-107">EXAMPLES</span></span>

### <span data-ttu-id="78672-108">Exemplo 1: Criar uma tabela de armazenamento do azure</span><span class="sxs-lookup"><span data-stu-id="78672-108">Example 1: Create an azure storage table</span></span>
```
PS C:\>New-AzStorageTable -Name "tableabc"
```

<span data-ttu-id="78672-109">Este comando cria uma tabela de armazenamento com um nome de tableabc.</span><span class="sxs-lookup"><span data-stu-id="78672-109">This command creates a storage table with a name of tableabc.</span></span>

### <span data-ttu-id="78672-110">Exemplo 2: Criar várias tabelas de armazenamento do azure</span><span class="sxs-lookup"><span data-stu-id="78672-110">Example 2: Create multiple azure storage tables</span></span>
```
PS C:\>"table1 table2 table3".split() | New-AzStorageTable
```

<span data-ttu-id="78672-111">Este comando cria várias tabelas.</span><span class="sxs-lookup"><span data-stu-id="78672-111">This command creates multiple tables.</span></span>
<span data-ttu-id="78672-112">Ele usa o **método Split** da classe .NET **String** e passa os nomes no pipeline.</span><span class="sxs-lookup"><span data-stu-id="78672-112">It uses the **Split** method of the .NET **String** class and then passes the names on the pipeline.</span></span>

## <span data-ttu-id="78672-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="78672-113">PARAMETERS</span></span>

### <span data-ttu-id="78672-114">-Context</span><span class="sxs-lookup"><span data-stu-id="78672-114">-Context</span></span>
<span data-ttu-id="78672-115">Especifica o contexto de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="78672-115">Specifies the storage context.</span></span>
<span data-ttu-id="78672-116">Para criar, você pode usar o cmdlet New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="78672-116">To create it, you can use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="78672-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78672-117">-DefaultProfile</span></span>
<span data-ttu-id="78672-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="78672-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78672-119">-Name</span><span class="sxs-lookup"><span data-stu-id="78672-119">-Name</span></span>
<span data-ttu-id="78672-120">Especifica um nome para a nova tabela.</span><span class="sxs-lookup"><span data-stu-id="78672-120">Specifies a name for the new table.</span></span>

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

### <span data-ttu-id="78672-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78672-121">CommonParameters</span></span>
<span data-ttu-id="78672-122">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78672-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78672-123">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="78672-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78672-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="78672-124">INPUTS</span></span>

### <span data-ttu-id="78672-125">System.String</span><span class="sxs-lookup"><span data-stu-id="78672-125">System.String</span></span>

### <span data-ttu-id="78672-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="78672-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="78672-127">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="78672-127">OUTPUTS</span></span>

### <span data-ttu-id="78672-128">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="78672-128">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageTable</span></span>

## <span data-ttu-id="78672-129">NOTES</span><span class="sxs-lookup"><span data-stu-id="78672-129">NOTES</span></span>

## <span data-ttu-id="78672-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="78672-130">RELATED LINKS</span></span>

[<span data-ttu-id="78672-131">Get-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="78672-131">Get-AzStorageTable</span></span>](./Get-AzStorageTable.md)

[<span data-ttu-id="78672-132">Remove-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="78672-132">Remove-AzStorageTable</span></span>](./Remove-AzStorageTable.md)



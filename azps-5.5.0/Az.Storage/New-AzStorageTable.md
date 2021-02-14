---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 3B4F32F3-51ED-4851-B38F-172658186C96
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageTable.md
ms.openlocfilehash: 0f46570858368a821d176a5f4e0a907c8a56b49c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115649"
---
# <span data-ttu-id="699ce-101">New-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="699ce-101">New-AzStorageTable</span></span>

## <span data-ttu-id="699ce-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="699ce-102">SYNOPSIS</span></span>
<span data-ttu-id="699ce-103">Cria uma tabela de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="699ce-103">Creates a storage table.</span></span>

## <span data-ttu-id="699ce-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="699ce-104">SYNTAX</span></span>

```
New-AzStorageTable [-Name] <String> [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="699ce-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="699ce-105">DESCRIPTION</span></span>
<span data-ttu-id="699ce-106">O **cmdlet New-AzStorageTable** cria uma tabela de armazenamento associada à conta de armazenamento no Azure.</span><span class="sxs-lookup"><span data-stu-id="699ce-106">The **New-AzStorageTable** cmdlet creates a storage table associated with the storage account in Azure.</span></span>

## <span data-ttu-id="699ce-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="699ce-107">EXAMPLES</span></span>

### <span data-ttu-id="699ce-108">Exemplo 1: Criar uma tabela de armazenamento do azure</span><span class="sxs-lookup"><span data-stu-id="699ce-108">Example 1: Create an azure storage table</span></span>
```
PS C:\>New-AzStorageTable -Name "tableabc"
```

<span data-ttu-id="699ce-109">Esse comando cria uma tabela de armazenamento com um nome de tabelaabc.</span><span class="sxs-lookup"><span data-stu-id="699ce-109">This command creates a storage table with a name of tableabc.</span></span>

### <span data-ttu-id="699ce-110">Exemplo 2: Criar várias tabelas de armazenamento do Azure</span><span class="sxs-lookup"><span data-stu-id="699ce-110">Example 2: Create multiple azure storage tables</span></span>
```
PS C:\>"table1 table2 table3".split() | New-AzStorageTable
```

<span data-ttu-id="699ce-111">Esse comando cria várias tabelas.</span><span class="sxs-lookup"><span data-stu-id="699ce-111">This command creates multiple tables.</span></span>
<span data-ttu-id="699ce-112">Ele usa o **método Dividir** da classe cadeia de caracteres **.NET** e passa os nomes no pipeline.</span><span class="sxs-lookup"><span data-stu-id="699ce-112">It uses the **Split** method of the .NET **String** class and then passes the names on the pipeline.</span></span>

## <span data-ttu-id="699ce-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="699ce-113">PARAMETERS</span></span>

### <span data-ttu-id="699ce-114">-Contexto</span><span class="sxs-lookup"><span data-stu-id="699ce-114">-Context</span></span>
<span data-ttu-id="699ce-115">Especifica o contexto de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="699ce-115">Specifies the storage context.</span></span>
<span data-ttu-id="699ce-116">Para criar, você pode usar o cmdlet New-AzStorageContext dados.</span><span class="sxs-lookup"><span data-stu-id="699ce-116">To create it, you can use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="699ce-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="699ce-117">-DefaultProfile</span></span>
<span data-ttu-id="699ce-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="699ce-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="699ce-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="699ce-119">-Name</span></span>
<span data-ttu-id="699ce-120">Especifica um nome para a nova tabela.</span><span class="sxs-lookup"><span data-stu-id="699ce-120">Specifies a name for the new table.</span></span>

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

### <span data-ttu-id="699ce-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="699ce-121">CommonParameters</span></span>
<span data-ttu-id="699ce-122">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="699ce-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="699ce-123">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="699ce-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="699ce-124">Entradas</span><span class="sxs-lookup"><span data-stu-id="699ce-124">INPUTS</span></span>

### <span data-ttu-id="699ce-125">System.String</span><span class="sxs-lookup"><span data-stu-id="699ce-125">System.String</span></span>

### <span data-ttu-id="699ce-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="699ce-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="699ce-127">Saídas</span><span class="sxs-lookup"><span data-stu-id="699ce-127">OUTPUTS</span></span>

### <span data-ttu-id="699ce-128">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="699ce-128">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageTable</span></span>

## <span data-ttu-id="699ce-129">Notas</span><span class="sxs-lookup"><span data-stu-id="699ce-129">NOTES</span></span>

## <span data-ttu-id="699ce-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="699ce-130">RELATED LINKS</span></span>

[<span data-ttu-id="699ce-131">Get-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="699ce-131">Get-AzStorageTable</span></span>](./Get-AzStorageTable.md)

[<span data-ttu-id="699ce-132">Remove-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="699ce-132">Remove-AzStorageTable</span></span>](./Remove-AzStorageTable.md)



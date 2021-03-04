---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: E9500392-6BE1-46EC-9AF5-9234281025E6
online version: https://docs.microsoft.com/powershell/module/az.storage/new-azstoragequeue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageQueue.md
ms.openlocfilehash: 55cee15e3b5327fa0a10def6e2090a77b68b207e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891954"
---
# <span data-ttu-id="6c712-101">New-AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="6c712-101">New-AzStorageQueue</span></span>

## <span data-ttu-id="6c712-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6c712-102">SYNOPSIS</span></span>
<span data-ttu-id="6c712-103">Cria uma fila de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="6c712-103">Creates a storage queue.</span></span>

## <span data-ttu-id="6c712-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="6c712-104">SYNTAX</span></span>

```
New-AzStorageQueue [-Name] <String> [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6c712-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="6c712-105">DESCRIPTION</span></span>
<span data-ttu-id="6c712-106">O cmdlet **New-AzStorageQueue** cria uma fila de armazenamento no Azure.</span><span class="sxs-lookup"><span data-stu-id="6c712-106">The **New-AzStorageQueue** cmdlet creates a storage queue in Azure.</span></span>

## <span data-ttu-id="6c712-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6c712-107">EXAMPLES</span></span>

### <span data-ttu-id="6c712-108">Exemplo 1: Criar uma fila de armazenamento do Azure</span><span class="sxs-lookup"><span data-stu-id="6c712-108">Example 1: Create an Azure storage queue</span></span>
```
PS C:\>New-AzStorageQueue -Name "queueabc"
```

<span data-ttu-id="6c712-109">Este exemplo cria uma fila de armazenamento chamada queueabc.</span><span class="sxs-lookup"><span data-stu-id="6c712-109">This example creates a storage queue named queueabc.</span></span>

### <span data-ttu-id="6c712-110">Exemplo 2: Criar várias filas de armazenamento do azure</span><span class="sxs-lookup"><span data-stu-id="6c712-110">Example 2: Create multiple azure storage queues</span></span>
```
PS C:\>"queue1 queue2 queue3".split() | New-AzStorageQueue
```

<span data-ttu-id="6c712-111">Este exemplo cria várias filas de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="6c712-111">This example creates multiple storage queues.</span></span>
<span data-ttu-id="6c712-112">Ele usa o método Split da classe .NET String e passa os nomes no pipeline.</span><span class="sxs-lookup"><span data-stu-id="6c712-112">It uses the Split method of the .NET String class and then passes the names on the pipeline.</span></span>

## <span data-ttu-id="6c712-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="6c712-113">PARAMETERS</span></span>

### <span data-ttu-id="6c712-114">-Context</span><span class="sxs-lookup"><span data-stu-id="6c712-114">-Context</span></span>
<span data-ttu-id="6c712-115">Especifica o contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="6c712-115">Specifies the Azure storage context.</span></span>
<span data-ttu-id="6c712-116">Você pode criar usando o cmdlet New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="6c712-116">You can create it by using the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="6c712-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c712-117">-DefaultProfile</span></span>
<span data-ttu-id="6c712-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6c712-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6c712-119">-Name</span><span class="sxs-lookup"><span data-stu-id="6c712-119">-Name</span></span>
<span data-ttu-id="6c712-120">Especifica um nome para a fila.</span><span class="sxs-lookup"><span data-stu-id="6c712-120">Specifies a name for the queue.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Queue

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6c712-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c712-121">CommonParameters</span></span>
<span data-ttu-id="6c712-122">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c712-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c712-123">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6c712-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c712-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6c712-124">INPUTS</span></span>

### <span data-ttu-id="6c712-125">System.String</span><span class="sxs-lookup"><span data-stu-id="6c712-125">System.String</span></span>

### <span data-ttu-id="6c712-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="6c712-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="6c712-127">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="6c712-127">OUTPUTS</span></span>

### <span data-ttu-id="6c712-128">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="6c712-128">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageQueue</span></span>

## <span data-ttu-id="6c712-129">NOTES</span><span class="sxs-lookup"><span data-stu-id="6c712-129">NOTES</span></span>

## <span data-ttu-id="6c712-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6c712-130">RELATED LINKS</span></span>

[<span data-ttu-id="6c712-131">Get-AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="6c712-131">Get-AzStorageQueue</span></span>](./Get-AzStorageQueue.md)

[<span data-ttu-id="6c712-132">Remove-AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="6c712-132">Remove-AzStorageQueue</span></span>](./Remove-AzStorageQueue.md)



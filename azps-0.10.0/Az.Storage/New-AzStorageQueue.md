---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: E9500392-6BE1-46EC-9AF5-9234281025E6
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragequeue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/New-AzStorageQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/New-AzStorageQueue.md
ms.openlocfilehash: 1ce3615d7eeef4986f1fefd20ec5be2ea1aaac7b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776218"
---
# <span data-ttu-id="2cb2a-101">New-AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="2cb2a-101">New-AzStorageQueue</span></span>

## <span data-ttu-id="2cb2a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2cb2a-102">SYNOPSIS</span></span>
<span data-ttu-id="2cb2a-103">Cria uma fila de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="2cb2a-103">Creates a storage queue.</span></span>

## <span data-ttu-id="2cb2a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2cb2a-104">SYNTAX</span></span>

```
New-AzStorageQueue [-Name] <String> [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2cb2a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2cb2a-105">DESCRIPTION</span></span>
<span data-ttu-id="2cb2a-106">O cmdlet **New-AzStorageQueue** cria uma fila de armazenamento no Azure.</span><span class="sxs-lookup"><span data-stu-id="2cb2a-106">The **New-AzStorageQueue** cmdlet creates a storage queue in Azure.</span></span>

## <span data-ttu-id="2cb2a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2cb2a-107">EXAMPLES</span></span>

### <span data-ttu-id="2cb2a-108">Exemplo 1: criar uma fila de armazenamento do Azure</span><span class="sxs-lookup"><span data-stu-id="2cb2a-108">Example 1: Create an Azure storage queue</span></span>
```
PS C:\>New-AzStorageQueue -Name "queueabc"
```

<span data-ttu-id="2cb2a-109">Este exemplo cria uma fila de armazenamento chamada queueabc.</span><span class="sxs-lookup"><span data-stu-id="2cb2a-109">This example creates a storage queue named queueabc.</span></span>

### <span data-ttu-id="2cb2a-110">Exemplo 2: criar várias filas de armazenamento do Azure</span><span class="sxs-lookup"><span data-stu-id="2cb2a-110">Example 2: Create multiple azure storage queues</span></span>
```
PS C:\>"queue1 queue2 queue3".split() | New-AzStorageQueue
```

<span data-ttu-id="2cb2a-111">Este exemplo cria várias filas de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="2cb2a-111">This example creates multiple storage queues.</span></span>
<span data-ttu-id="2cb2a-112">Ele usa o método Split da classe String .NET e, em seguida, passa os nomes no pipeline.</span><span class="sxs-lookup"><span data-stu-id="2cb2a-112">It uses the Split method of the .NET String class and then passes the names on the pipeline.</span></span>

## <span data-ttu-id="2cb2a-113">OS</span><span class="sxs-lookup"><span data-stu-id="2cb2a-113">PARAMETERS</span></span>

### <span data-ttu-id="2cb2a-114">-Contexto</span><span class="sxs-lookup"><span data-stu-id="2cb2a-114">-Context</span></span>
<span data-ttu-id="2cb2a-115">Especifica o contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="2cb2a-115">Specifies the Azure storage context.</span></span>
<span data-ttu-id="2cb2a-116">Você pode criá-lo usando o cmdlet New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="2cb2a-116">You can create it by using the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="2cb2a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2cb2a-117">-DefaultProfile</span></span>
<span data-ttu-id="2cb2a-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2cb2a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2cb2a-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="2cb2a-119">-Name</span></span>
<span data-ttu-id="2cb2a-120">Especifica um nome para a fila.</span><span class="sxs-lookup"><span data-stu-id="2cb2a-120">Specifies a name for the queue.</span></span>

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

### <span data-ttu-id="2cb2a-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2cb2a-121">CommonParameters</span></span>
<span data-ttu-id="2cb2a-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2cb2a-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2cb2a-123">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2cb2a-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2cb2a-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2cb2a-124">INPUTS</span></span>

### <span data-ttu-id="2cb2a-125">System. String</span><span class="sxs-lookup"><span data-stu-id="2cb2a-125">System.String</span></span>

### <span data-ttu-id="2cb2a-126">Microsoft. Azure. Commands. Common. Authentication. Abstractings. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="2cb2a-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="2cb2a-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2cb2a-127">OUTPUTS</span></span>

### <span data-ttu-id="2cb2a-128">Microsoft. WindowsAzure. Commands. Common. Storage. ResourceModel. AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="2cb2a-128">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageQueue</span></span>

## <span data-ttu-id="2cb2a-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2cb2a-129">NOTES</span></span>

## <span data-ttu-id="2cb2a-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2cb2a-130">RELATED LINKS</span></span>

[<span data-ttu-id="2cb2a-131">Get-AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="2cb2a-131">Get-AzStorageQueue</span></span>](./Get-AzStorageQueue.md)

[<span data-ttu-id="2cb2a-132">Remove-AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="2cb2a-132">Remove-AzStorageQueue</span></span>](./Remove-AzStorageQueue.md)


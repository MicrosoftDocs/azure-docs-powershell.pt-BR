---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: E9500392-6BE1-46EC-9AF5-9234281025E6
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragequeue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageQueue.md
ms.openlocfilehash: 1c3f258f4aecbeb492e0e60e274c5e702ae1a3f2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116103"
---
# <span data-ttu-id="975e2-101">New-AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="975e2-101">New-AzStorageQueue</span></span>

## <span data-ttu-id="975e2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="975e2-102">SYNOPSIS</span></span>
<span data-ttu-id="975e2-103">Cria uma fila de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="975e2-103">Creates a storage queue.</span></span>

## <span data-ttu-id="975e2-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="975e2-104">SYNTAX</span></span>

```
New-AzStorageQueue [-Name] <String> [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="975e2-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="975e2-105">DESCRIPTION</span></span>
<span data-ttu-id="975e2-106">O **cmdlet New-AzStorageQueue** cria uma fila de armazenamento no Azure.</span><span class="sxs-lookup"><span data-stu-id="975e2-106">The **New-AzStorageQueue** cmdlet creates a storage queue in Azure.</span></span>

## <span data-ttu-id="975e2-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="975e2-107">EXAMPLES</span></span>

### <span data-ttu-id="975e2-108">Exemplo 1: Criar uma fila de armazenamento do Azure</span><span class="sxs-lookup"><span data-stu-id="975e2-108">Example 1: Create an Azure storage queue</span></span>
```
PS C:\>New-AzStorageQueue -Name "queueabc"
```

<span data-ttu-id="975e2-109">Este exemplo cria uma fila de armazenamento chamada queueabc.</span><span class="sxs-lookup"><span data-stu-id="975e2-109">This example creates a storage queue named queueabc.</span></span>

### <span data-ttu-id="975e2-110">Exemplo 2: Criar várias filas de armazenamento do Azure</span><span class="sxs-lookup"><span data-stu-id="975e2-110">Example 2: Create multiple azure storage queues</span></span>
```
PS C:\>"queue1 queue2 queue3".split() | New-AzStorageQueue
```

<span data-ttu-id="975e2-111">Este exemplo cria várias filas de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="975e2-111">This example creates multiple storage queues.</span></span>
<span data-ttu-id="975e2-112">Ele usa o método Dividir da classe cadeia de caracteres .NET e passa os nomes no pipeline.</span><span class="sxs-lookup"><span data-stu-id="975e2-112">It uses the Split method of the .NET String class and then passes the names on the pipeline.</span></span>

## <span data-ttu-id="975e2-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="975e2-113">PARAMETERS</span></span>

### <span data-ttu-id="975e2-114">-Contexto</span><span class="sxs-lookup"><span data-stu-id="975e2-114">-Context</span></span>
<span data-ttu-id="975e2-115">Especifica o contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="975e2-115">Specifies the Azure storage context.</span></span>
<span data-ttu-id="975e2-116">Você pode criar usando o cmdlet New-AzStorageContext dados.</span><span class="sxs-lookup"><span data-stu-id="975e2-116">You can create it by using the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="975e2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="975e2-117">-DefaultProfile</span></span>
<span data-ttu-id="975e2-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="975e2-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="975e2-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="975e2-119">-Name</span></span>
<span data-ttu-id="975e2-120">Especifica um nome para a fila.</span><span class="sxs-lookup"><span data-stu-id="975e2-120">Specifies a name for the queue.</span></span>

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

### <span data-ttu-id="975e2-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="975e2-121">CommonParameters</span></span>
<span data-ttu-id="975e2-122">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="975e2-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="975e2-123">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="975e2-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="975e2-124">Entradas</span><span class="sxs-lookup"><span data-stu-id="975e2-124">INPUTS</span></span>

### <span data-ttu-id="975e2-125">System.String</span><span class="sxs-lookup"><span data-stu-id="975e2-125">System.String</span></span>

### <span data-ttu-id="975e2-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="975e2-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="975e2-127">Saídas</span><span class="sxs-lookup"><span data-stu-id="975e2-127">OUTPUTS</span></span>

### <span data-ttu-id="975e2-128">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="975e2-128">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageQueue</span></span>

## <span data-ttu-id="975e2-129">Notas</span><span class="sxs-lookup"><span data-stu-id="975e2-129">NOTES</span></span>

## <span data-ttu-id="975e2-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="975e2-130">RELATED LINKS</span></span>

[<span data-ttu-id="975e2-131">Get-AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="975e2-131">Get-AzStorageQueue</span></span>](./Get-AzStorageQueue.md)

[<span data-ttu-id="975e2-132">Remove-AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="975e2-132">Remove-AzStorageQueue</span></span>](./Remove-AzStorageQueue.md)



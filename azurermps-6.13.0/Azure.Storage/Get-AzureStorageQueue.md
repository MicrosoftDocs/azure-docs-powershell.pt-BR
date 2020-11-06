---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: C2EBCCF0-56CE-4D49-A138-74E52FC3A9AC
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestoragequeue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageQueue.md
ms.openlocfilehash: 077d8139817c3998e27300d8c86c809b4da9e630
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429631"
---
# <span data-ttu-id="b464f-101">Get-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="b464f-101">Get-AzureStorageQueue</span></span>

## <span data-ttu-id="b464f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b464f-102">SYNOPSIS</span></span>
<span data-ttu-id="b464f-103">Lista as filas de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="b464f-103">Lists storage queues.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b464f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b464f-104">SYNTAX</span></span>

### <span data-ttu-id="b464f-105">QueueName (padrão)</span><span class="sxs-lookup"><span data-stu-id="b464f-105">QueueName (Default)</span></span>
```
Get-AzureStorageQueue [[-Name] <String>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b464f-106">QueuePrefix</span><span class="sxs-lookup"><span data-stu-id="b464f-106">QueuePrefix</span></span>
```
Get-AzureStorageQueue -Prefix <String> [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b464f-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b464f-107">DESCRIPTION</span></span>
<span data-ttu-id="b464f-108">O cmdlet **Get-AzureStorageQueue** lista as filas de armazenamento associadas a uma conta de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="b464f-108">The **Get-AzureStorageQueue** cmdlet lists storage queues associated with an Azure Storage account.</span></span>

## <span data-ttu-id="b464f-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b464f-109">EXAMPLES</span></span>

### <span data-ttu-id="b464f-110">Exemplo 1: listar todas as filas de armazenamento do Azure</span><span class="sxs-lookup"><span data-stu-id="b464f-110">Example 1: List all Azure Storage queues</span></span>
```
PS C:\>Get-AzureStorageQueue
```

<span data-ttu-id="b464f-111">Este comando obtém uma lista de todas as filas de armazenamento da conta de armazenamento atual.</span><span class="sxs-lookup"><span data-stu-id="b464f-111">This command gets a list of all storage queues for the current Storage account.</span></span>

### <span data-ttu-id="b464f-112">Exemplo 2: listar filas de armazenamento do Azure usando um caractere curinga</span><span class="sxs-lookup"><span data-stu-id="b464f-112">Example 2: List Azure Storage queues using a wildcard character</span></span>
```
PS C:\>Get-AzureStorageQueue -Name queue*
```

<span data-ttu-id="b464f-113">Esse comando usa um caractere curinga para obter uma lista de filas de armazenamento cujo nome começa com a fila.</span><span class="sxs-lookup"><span data-stu-id="b464f-113">This command uses a wildcard character to get a list of storage queues whose name starts with queue.</span></span>

### <span data-ttu-id="b464f-114">Exemplo 3: listar filas de armazenamento do Azure usando prefixo do nome da fila</span><span class="sxs-lookup"><span data-stu-id="b464f-114">Example 3: List Azure Storage queues using queue name prefix</span></span>
```
PS C:\>Get-AzureStorageQueue -Prefix "queue"
```

<span data-ttu-id="b464f-115">Este exemplo usa o parâmetro *prefix* para obter uma lista de filas de armazenamento cujo nome começa com a fila.</span><span class="sxs-lookup"><span data-stu-id="b464f-115">This example uses the *Prefix* parameter to get a list of storage queues whose name starts with queue.</span></span>

## <span data-ttu-id="b464f-116">OS</span><span class="sxs-lookup"><span data-stu-id="b464f-116">PARAMETERS</span></span>

### <span data-ttu-id="b464f-117">-Contexto</span><span class="sxs-lookup"><span data-stu-id="b464f-117">-Context</span></span>
<span data-ttu-id="b464f-118">Especifica o contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="b464f-118">Specifies the Azure storage context.</span></span>
<span data-ttu-id="b464f-119">Você pode criá-lo usando o cmdlet **New-AzureStorageContext** .</span><span class="sxs-lookup"><span data-stu-id="b464f-119">You can create it by using the **New-AzureStorageContext** cmdlet.</span></span>

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

### <span data-ttu-id="b464f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b464f-120">-DefaultProfile</span></span>
<span data-ttu-id="b464f-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b464f-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b464f-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="b464f-122">-Name</span></span>
<span data-ttu-id="b464f-123">Especifica um nome.</span><span class="sxs-lookup"><span data-stu-id="b464f-123">Specifies a name.</span></span>
<span data-ttu-id="b464f-124">Se não for especificado um nome, o cmdlet obterá uma lista de todas as filas.</span><span class="sxs-lookup"><span data-stu-id="b464f-124">If no name is specified, the cmdlet gets a list of all the queues.</span></span>
<span data-ttu-id="b464f-125">Se um nome completo ou parcial for especificado, o cmdlet obterá todas as filas correspondentes ao padrão de nome.</span><span class="sxs-lookup"><span data-stu-id="b464f-125">If a full or partial name is specified, the cmdlet gets all queues that match the name pattern.</span></span>

```yaml
Type: System.String
Parameter Sets: QueueName
Aliases: N, Queue

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b464f-126">-Prefix</span><span class="sxs-lookup"><span data-stu-id="b464f-126">-Prefix</span></span>
<span data-ttu-id="b464f-127">Especifica um prefixo usado no nome das filas que você deseja obter.</span><span class="sxs-lookup"><span data-stu-id="b464f-127">Specifies a prefix used in the name of the queues you want to get.</span></span>

```yaml
Type: System.String
Parameter Sets: QueuePrefix
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b464f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b464f-128">CommonParameters</span></span>
<span data-ttu-id="b464f-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b464f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b464f-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b464f-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b464f-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b464f-131">INPUTS</span></span>

### <span data-ttu-id="b464f-132">System. String</span><span class="sxs-lookup"><span data-stu-id="b464f-132">System.String</span></span>

### <span data-ttu-id="b464f-133">Microsoft. Azure. Commands. Common. Authentication. Abstractings. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="b464f-133">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="b464f-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b464f-134">OUTPUTS</span></span>

### <span data-ttu-id="b464f-135">Microsoft. WindowsAzure. Commands. Common. Storage. ResourceModel. AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="b464f-135">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageQueue</span></span>

## <span data-ttu-id="b464f-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b464f-136">NOTES</span></span>

## <span data-ttu-id="b464f-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b464f-137">RELATED LINKS</span></span>

[<span data-ttu-id="b464f-138">New-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="b464f-138">New-AzureStorageQueue</span></span>](./New-AzureStorageQueue.md)

[<span data-ttu-id="b464f-139">Remove-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="b464f-139">Remove-AzureStorageQueue</span></span>](./Remove-AzureStorageQueue.md)



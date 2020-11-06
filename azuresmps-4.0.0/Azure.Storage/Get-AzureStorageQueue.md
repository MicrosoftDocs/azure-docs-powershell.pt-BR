---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: C2EBCCF0-56CE-4D49-A138-74E52FC3A9AC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 11a8ffe26a65bf2ecabab7807d8e54bc23b629fc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93426153"
---
# <span data-ttu-id="5a53a-101">Get-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="5a53a-101">Get-AzureStorageQueue</span></span>

## <span data-ttu-id="5a53a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5a53a-102">SYNOPSIS</span></span>
<span data-ttu-id="5a53a-103">Lista as filas de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="5a53a-103">Lists storage queues.</span></span>

## <span data-ttu-id="5a53a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5a53a-104">SYNTAX</span></span>

### <span data-ttu-id="5a53a-105">QueueName (padrão)</span><span class="sxs-lookup"><span data-stu-id="5a53a-105">QueueName (Default)</span></span>
```
Get-AzureStorageQueue [[-Name] <String>] [-Context <IStorageContext>] [<CommonParameters>]
```

### <span data-ttu-id="5a53a-106">QueuePrefix</span><span class="sxs-lookup"><span data-stu-id="5a53a-106">QueuePrefix</span></span>
```
Get-AzureStorageQueue -Prefix <String> [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="5a53a-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5a53a-107">DESCRIPTION</span></span>
<span data-ttu-id="5a53a-108">O cmdlet **Get-AzureStorageQueue** lista as filas de armazenamento associadas a uma conta de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="5a53a-108">The **Get-AzureStorageQueue** cmdlet lists storage queues associated with an Azure Storage account.</span></span>

## <span data-ttu-id="5a53a-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5a53a-109">EXAMPLES</span></span>

### <span data-ttu-id="5a53a-110">Exemplo 1: listar todas as filas de armazenamento do Azure</span><span class="sxs-lookup"><span data-stu-id="5a53a-110">Example 1: List all Azure Storage queues</span></span>
```
PS C:\>Get-AzureStorageQueue
```

<span data-ttu-id="5a53a-111">Este comando obtém uma lista de todas as filas de armazenamento da conta de armazenamento atual.</span><span class="sxs-lookup"><span data-stu-id="5a53a-111">This command gets a list of all storage queues for the current Storage account.</span></span>

### <span data-ttu-id="5a53a-112">Exemplo 2: listar filas de armazenamento do Azure usando um caractere curinga</span><span class="sxs-lookup"><span data-stu-id="5a53a-112">Example 2: List Azure Storage queues using a wildcard character</span></span>
```
PS C:\>Get-AzureStorageQueue -Name queue*
```

<span data-ttu-id="5a53a-113">Esse comando usa um caractere curinga para obter uma lista de filas de armazenamento cujo nome começa com a fila.</span><span class="sxs-lookup"><span data-stu-id="5a53a-113">This command uses a wildcard character to get a list of storage queues whose name starts with queue.</span></span>

### <span data-ttu-id="5a53a-114">Exemplo 3: listar filas de armazenamento do Azure usando prefixo do nome da fila</span><span class="sxs-lookup"><span data-stu-id="5a53a-114">Example 3: List Azure Storage queues using queue name prefix</span></span>
```
PS C:\>Get-AzureStorageQueue -Prefix "queue"
```

<span data-ttu-id="5a53a-115">Este exemplo usa o parâmetro *prefix* para obter uma lista de filas de armazenamento cujo nome começa com a fila.</span><span class="sxs-lookup"><span data-stu-id="5a53a-115">This example uses the *Prefix* parameter to get a list of storage queues whose name starts with queue.</span></span>

## <span data-ttu-id="5a53a-116">OS</span><span class="sxs-lookup"><span data-stu-id="5a53a-116">PARAMETERS</span></span>

### <span data-ttu-id="5a53a-117">-Contexto</span><span class="sxs-lookup"><span data-stu-id="5a53a-117">-Context</span></span>
<span data-ttu-id="5a53a-118">Especifica o contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="5a53a-118">Specifies the Azure storage context.</span></span>
<span data-ttu-id="5a53a-119">Você pode criá-lo usando o cmdlet **New-AzureStorageContext** .</span><span class="sxs-lookup"><span data-stu-id="5a53a-119">You can create it by using the **New-AzureStorageContext** cmdlet.</span></span>

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

### <span data-ttu-id="5a53a-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="5a53a-120">-Name</span></span>
<span data-ttu-id="5a53a-121">Especifica um nome.</span><span class="sxs-lookup"><span data-stu-id="5a53a-121">Specifies a name.</span></span>
<span data-ttu-id="5a53a-122">Se não for especificado um nome, o cmdlet obterá uma lista de todas as filas.</span><span class="sxs-lookup"><span data-stu-id="5a53a-122">If no name is specified, the cmdlet gets a list of all the queues.</span></span>
<span data-ttu-id="5a53a-123">Se um nome completo ou parcial for especificado, o cmdlet obterá todas as filas correspondentes ao padrão de nome.</span><span class="sxs-lookup"><span data-stu-id="5a53a-123">If a full or partial name is specified, the cmdlet gets all queues that match the name pattern.</span></span>

```yaml
Type: String
Parameter Sets: QueueName
Aliases: N, Queue

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5a53a-124">-Prefix</span><span class="sxs-lookup"><span data-stu-id="5a53a-124">-Prefix</span></span>
<span data-ttu-id="5a53a-125">Especifica um prefixo usado no nome das filas que você deseja obter.</span><span class="sxs-lookup"><span data-stu-id="5a53a-125">Specifies a prefix used in the name of the queues you want to get.</span></span>

```yaml
Type: String
Parameter Sets: QueuePrefix
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a53a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a53a-126">CommonParameters</span></span>
<span data-ttu-id="5a53a-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a53a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a53a-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a53a-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a53a-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5a53a-129">INPUTS</span></span>

## <span data-ttu-id="5a53a-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5a53a-130">OUTPUTS</span></span>

## <span data-ttu-id="5a53a-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5a53a-131">NOTES</span></span>

## <span data-ttu-id="5a53a-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5a53a-132">RELATED LINKS</span></span>

[<span data-ttu-id="5a53a-133">New-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="5a53a-133">New-AzureStorageQueue</span></span>](./New-AzureStorageQueue.md)

[<span data-ttu-id="5a53a-134">Remove-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="5a53a-134">Remove-AzureStorageQueue</span></span>](./Remove-AzureStorageQueue.md)



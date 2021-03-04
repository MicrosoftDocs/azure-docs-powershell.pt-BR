---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: C2EBCCF0-56CE-4D49-A138-74E52FC3A9AC
online version: https://docs.microsoft.com/powershell/module/az.storage/get-azstoragequeue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageQueue.md
ms.openlocfilehash: 2361196f2e8b904f2403aaf06118122931e83afd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891248"
---
# <span data-ttu-id="d0eee-101">Get-AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="d0eee-101">Get-AzStorageQueue</span></span>

## <span data-ttu-id="d0eee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d0eee-102">SYNOPSIS</span></span>
<span data-ttu-id="d0eee-103">Lista filas de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="d0eee-103">Lists storage queues.</span></span>

## <span data-ttu-id="d0eee-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="d0eee-104">SYNTAX</span></span>

### <span data-ttu-id="d0eee-105">QueueName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="d0eee-105">QueueName (Default)</span></span>
```
Get-AzStorageQueue [[-Name] <String>] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d0eee-106">QueuePrefix</span><span class="sxs-lookup"><span data-stu-id="d0eee-106">QueuePrefix</span></span>
```
Get-AzStorageQueue -Prefix <String> [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d0eee-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="d0eee-107">DESCRIPTION</span></span>
<span data-ttu-id="d0eee-108">O cmdlet **Get-AzStorageQueue** lista filas de armazenamento associadas a uma conta de Armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="d0eee-108">The **Get-AzStorageQueue** cmdlet lists storage queues associated with an Azure Storage account.</span></span>

## <span data-ttu-id="d0eee-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d0eee-109">EXAMPLES</span></span>

### <span data-ttu-id="d0eee-110">Exemplo 1: listar todas as filas de armazenamento do Azure</span><span class="sxs-lookup"><span data-stu-id="d0eee-110">Example 1: List all Azure Storage queues</span></span>
```
PS C:\>Get-AzStorageQueue
```

<span data-ttu-id="d0eee-111">Este comando obtém uma lista de todas as filas de armazenamento para a conta de Armazenamento atual.</span><span class="sxs-lookup"><span data-stu-id="d0eee-111">This command gets a list of all storage queues for the current Storage account.</span></span>

### <span data-ttu-id="d0eee-112">Exemplo 2: Listar filas de armazenamento do Azure usando um caractere curinga</span><span class="sxs-lookup"><span data-stu-id="d0eee-112">Example 2: List Azure Storage queues using a wildcard character</span></span>
```
PS C:\>Get-AzStorageQueue -Name queue*
```

<span data-ttu-id="d0eee-113">Este comando usa um caractere curinga para obter uma lista de filas de armazenamento cujo nome começa com fila.</span><span class="sxs-lookup"><span data-stu-id="d0eee-113">This command uses a wildcard character to get a list of storage queues whose name starts with queue.</span></span>

### <span data-ttu-id="d0eee-114">Exemplo 3: Listar filas de armazenamento do Azure usando prefixo de nome da fila</span><span class="sxs-lookup"><span data-stu-id="d0eee-114">Example 3: List Azure Storage queues using queue name prefix</span></span>
```
PS C:\>Get-AzStorageQueue -Prefix "queue"
```

<span data-ttu-id="d0eee-115">Este exemplo usa o *parâmetro Prefix* para obter uma lista de filas de armazenamento cujo nome começa com fila.</span><span class="sxs-lookup"><span data-stu-id="d0eee-115">This example uses the *Prefix* parameter to get a list of storage queues whose name starts with queue.</span></span>

## <span data-ttu-id="d0eee-116">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="d0eee-116">PARAMETERS</span></span>

### <span data-ttu-id="d0eee-117">-Context</span><span class="sxs-lookup"><span data-stu-id="d0eee-117">-Context</span></span>
<span data-ttu-id="d0eee-118">Especifica o contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="d0eee-118">Specifies the Azure storage context.</span></span>
<span data-ttu-id="d0eee-119">Você pode criar usando o cmdlet **New-AzStorageContext.**</span><span class="sxs-lookup"><span data-stu-id="d0eee-119">You can create it by using the **New-AzStorageContext** cmdlet.</span></span>

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

### <span data-ttu-id="d0eee-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0eee-120">-DefaultProfile</span></span>
<span data-ttu-id="d0eee-121">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d0eee-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d0eee-122">-Name</span><span class="sxs-lookup"><span data-stu-id="d0eee-122">-Name</span></span>
<span data-ttu-id="d0eee-123">Especifica um nome.</span><span class="sxs-lookup"><span data-stu-id="d0eee-123">Specifies a name.</span></span>
<span data-ttu-id="d0eee-124">Se nenhum nome for especificado, o cmdlet obtém uma lista de todas as filas.</span><span class="sxs-lookup"><span data-stu-id="d0eee-124">If no name is specified, the cmdlet gets a list of all the queues.</span></span>
<span data-ttu-id="d0eee-125">Se um nome completo ou parcial for especificado, o cmdlet obtém todas as filas que corresponderem ao padrão de nome.</span><span class="sxs-lookup"><span data-stu-id="d0eee-125">If a full or partial name is specified, the cmdlet gets all queues that match the name pattern.</span></span>

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

### <span data-ttu-id="d0eee-126">-Prefix</span><span class="sxs-lookup"><span data-stu-id="d0eee-126">-Prefix</span></span>
<span data-ttu-id="d0eee-127">Especifica um prefixo usado no nome das filas que você deseja obter.</span><span class="sxs-lookup"><span data-stu-id="d0eee-127">Specifies a prefix used in the name of the queues you want to get.</span></span>

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

### <span data-ttu-id="d0eee-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0eee-128">CommonParameters</span></span>
<span data-ttu-id="d0eee-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0eee-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0eee-130">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d0eee-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0eee-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d0eee-131">INPUTS</span></span>

### <span data-ttu-id="d0eee-132">System.String</span><span class="sxs-lookup"><span data-stu-id="d0eee-132">System.String</span></span>

### <span data-ttu-id="d0eee-133">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="d0eee-133">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="d0eee-134">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="d0eee-134">OUTPUTS</span></span>

### <span data-ttu-id="d0eee-135">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="d0eee-135">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageQueue</span></span>

## <span data-ttu-id="d0eee-136">NOTES</span><span class="sxs-lookup"><span data-stu-id="d0eee-136">NOTES</span></span>

## <span data-ttu-id="d0eee-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d0eee-137">RELATED LINKS</span></span>

[<span data-ttu-id="d0eee-138">New-AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="d0eee-138">New-AzStorageQueue</span></span>](./New-AzStorageQueue.md)

[<span data-ttu-id="d0eee-139">Remove-AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="d0eee-139">Remove-AzStorageQueue</span></span>](./Remove-AzStorageQueue.md)



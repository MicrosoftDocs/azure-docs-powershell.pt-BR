---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 351145AC-7C1E-4EB7-A17D-B8B7D8ED8DAB
online version: ''
schema: 2.0.0
ms.openlocfilehash: 578eef176903576778325eb8610870040a515751
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93601766"
---
# <span data-ttu-id="4354a-101">New-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="4354a-101">New-AzureStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="4354a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4354a-102">SYNOPSIS</span></span>
<span data-ttu-id="4354a-103">Cria uma política de acesso armazenado para uma fila de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="4354a-103">Creates a stored access policy for an Azure storage queue.</span></span>

## <span data-ttu-id="4354a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4354a-104">SYNTAX</span></span>

```
New-AzureStorageQueueStoredAccessPolicy [-Queue] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="4354a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4354a-105">DESCRIPTION</span></span>
<span data-ttu-id="4354a-106">O cmdlet **New-AzureStorageQueueStoredAccessPolicy** cria uma política de acesso armazenado para uma fila de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="4354a-106">The **New-AzureStorageQueueStoredAccessPolicy** cmdlet creates a stored access policy for an Azure storage queue.</span></span>

## <span data-ttu-id="4354a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4354a-107">EXAMPLES</span></span>

### <span data-ttu-id="4354a-108">Exemplo 1: criar uma política de acesso armazenado em uma fila de armazenamento</span><span class="sxs-lookup"><span data-stu-id="4354a-108">Example 1: Create a stored access policy in a storage queue</span></span>
```
PS C:\>New-AzureStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy01"
```

<span data-ttu-id="4354a-109">Esse comando cria uma política de acesso chamada Policy01 na fila de armazenamento chamada MyQueue.</span><span class="sxs-lookup"><span data-stu-id="4354a-109">This command creates an access policy named Policy01 in the storage queue named MyQueue.</span></span>

## <span data-ttu-id="4354a-110">OS</span><span class="sxs-lookup"><span data-stu-id="4354a-110">PARAMETERS</span></span>

### <span data-ttu-id="4354a-111">-Contexto</span><span class="sxs-lookup"><span data-stu-id="4354a-111">-Context</span></span>
<span data-ttu-id="4354a-112">Especifica um contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="4354a-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="4354a-113">Para obter um contexto de armazenamento, use o cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="4354a-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="4354a-114">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="4354a-114">-ExpiryTime</span></span>
<span data-ttu-id="4354a-115">Especifica o tempo em que a política de acesso armazenado se torna inválida.</span><span class="sxs-lookup"><span data-stu-id="4354a-115">Specifies the time at which the stored access policy becomes invalid.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4354a-116">-Permissão</span><span class="sxs-lookup"><span data-stu-id="4354a-116">-Permission</span></span>
<span data-ttu-id="4354a-117">Especifica o nível de acesso público a essa fila de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="4354a-117">Specifies the level of public access to this storage queue.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4354a-118">-Política</span><span class="sxs-lookup"><span data-stu-id="4354a-118">-Policy</span></span>
<span data-ttu-id="4354a-119">Especifica uma política de acesso armazenado, que inclui as permissões para esse token SAS.</span><span class="sxs-lookup"><span data-stu-id="4354a-119">Specifies a stored access policy, which includes the permissions for this SAS token.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4354a-120">-Queue</span><span class="sxs-lookup"><span data-stu-id="4354a-120">-Queue</span></span>
<span data-ttu-id="4354a-121">Especifica o nome da fila de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="4354a-121">Specifies the Azure storage queue name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4354a-122">-StartTime</span><span class="sxs-lookup"><span data-stu-id="4354a-122">-StartTime</span></span>
<span data-ttu-id="4354a-123">Especifica a hora em que a política de acesso armazenado se torna válida.</span><span class="sxs-lookup"><span data-stu-id="4354a-123">Specifies the time at which the stored access policy becomes valid.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4354a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4354a-124">CommonParameters</span></span>
<span data-ttu-id="4354a-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4354a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4354a-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4354a-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4354a-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4354a-127">INPUTS</span></span>

## <span data-ttu-id="4354a-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4354a-128">OUTPUTS</span></span>

## <span data-ttu-id="4354a-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4354a-129">NOTES</span></span>

## <span data-ttu-id="4354a-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4354a-130">RELATED LINKS</span></span>

[<span data-ttu-id="4354a-131">Get-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="4354a-131">Get-AzureStorageQueueStoredAccessPolicy</span></span>](./Get-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="4354a-132">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="4354a-132">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="4354a-133">Remove-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="4354a-133">Remove-AzureStorageQueueStoredAccessPolicy</span></span>](./Remove-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="4354a-134">Set-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="4354a-134">Set-AzureStorageQueueStoredAccessPolicy</span></span>](./Set-AzureStorageQueueStoredAccessPolicy.md)



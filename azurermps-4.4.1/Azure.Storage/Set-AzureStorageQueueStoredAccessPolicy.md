---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 4FB7E017-7D37-4EDB-BEC1-36629058B87C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageQueueStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageQueueStoredAccessPolicy.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: 69ec2307dfdf8525f892720281079c58c1e1bd55
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440252"
---
# <span data-ttu-id="3657d-101">Set-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="3657d-101">Set-AzureStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="3657d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3657d-102">SYNOPSIS</span></span>
<span data-ttu-id="3657d-103">Define uma política de acesso armazenado para uma fila de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="3657d-103">Sets a stored access policy for an Azure storage queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3657d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3657d-104">SYNTAX</span></span>

```
Set-AzureStorageQueueStoredAccessPolicy [-Queue] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-NoStartTime] [-NoExpiryTime] [-Context <IStorageContext>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3657d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3657d-105">DESCRIPTION</span></span>
<span data-ttu-id="3657d-106">O cmdlet **set-AzureStorageQueueStoredAccessPolicy** define uma política de acesso armazenado para uma fila de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="3657d-106">The **Set-AzureStorageQueueStoredAccessPolicy** cmdlet sets a stored access policy for an Azure storage queue.</span></span>

## <span data-ttu-id="3657d-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3657d-107">EXAMPLES</span></span>

### <span data-ttu-id="3657d-108">Exemplo 1: definir uma política de acesso armazenado na fila com permissão completa</span><span class="sxs-lookup"><span data-stu-id="3657d-108">Example 1: Set a stored access policy in the queue with full permission</span></span>
```
PS C:\> Set-AzureStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy07" -Permission arup
```

<span data-ttu-id="3657d-109">Esse comando define uma política de acesso chamada Policy07 para fila de armazenamento chamada MyQueue.</span><span class="sxs-lookup"><span data-stu-id="3657d-109">This command sets an access policy named Policy07 for storage queue named MyQueue.</span></span>

## <span data-ttu-id="3657d-110">OS</span><span class="sxs-lookup"><span data-stu-id="3657d-110">PARAMETERS</span></span>

### <span data-ttu-id="3657d-111">-Contexto</span><span class="sxs-lookup"><span data-stu-id="3657d-111">-Context</span></span>
<span data-ttu-id="3657d-112">Especifica um contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="3657d-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="3657d-113">Para obter um contexto de armazenamento, use o cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="3657d-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="3657d-114">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="3657d-114">-ExpiryTime</span></span>
<span data-ttu-id="3657d-115">Especifica o tempo em que a política de acesso armazenado se torna inválida.</span><span class="sxs-lookup"><span data-stu-id="3657d-115">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="3657d-116">-NoExpiryTime</span><span class="sxs-lookup"><span data-stu-id="3657d-116">-NoExpiryTime</span></span>
<span data-ttu-id="3657d-117">Indica que a política de acesso não tem data de expiração.</span><span class="sxs-lookup"><span data-stu-id="3657d-117">Indicates that the access policy has no expiration date.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3657d-118">-Nostarttime</span><span class="sxs-lookup"><span data-stu-id="3657d-118">-NoStartTime</span></span>
<span data-ttu-id="3657d-119">Indica que esse cmdlet define a hora de início como $Null.</span><span class="sxs-lookup"><span data-stu-id="3657d-119">Indicates that this cmdlet sets the start time to be $Null.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3657d-120">-Permissão</span><span class="sxs-lookup"><span data-stu-id="3657d-120">-Permission</span></span>
<span data-ttu-id="3657d-121">Especifica as permissões na política de acesso armazenado para acessar a fila de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="3657d-121">Specifies permissions in the stored access policy to access the storage queue.</span></span>

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

### <span data-ttu-id="3657d-122">-Política</span><span class="sxs-lookup"><span data-stu-id="3657d-122">-Policy</span></span>
<span data-ttu-id="3657d-123">Especifica o nome da política de acesso armazenado.</span><span class="sxs-lookup"><span data-stu-id="3657d-123">Specifies the name for the stored access policy.</span></span>

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

### <span data-ttu-id="3657d-124">-Queue</span><span class="sxs-lookup"><span data-stu-id="3657d-124">-Queue</span></span>
<span data-ttu-id="3657d-125">Especifica o nome da fila de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="3657d-125">Specifies the Azure storage queue name.</span></span>

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

### <span data-ttu-id="3657d-126">-StartTime</span><span class="sxs-lookup"><span data-stu-id="3657d-126">-StartTime</span></span>
<span data-ttu-id="3657d-127">Especifica a hora em que a política de acesso armazenado se torna válida.</span><span class="sxs-lookup"><span data-stu-id="3657d-127">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="3657d-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="3657d-128">-Confirm</span></span>
<span data-ttu-id="3657d-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3657d-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3657d-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3657d-130">-WhatIf</span></span>
<span data-ttu-id="3657d-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3657d-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3657d-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3657d-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3657d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3657d-133">CommonParameters</span></span>
<span data-ttu-id="3657d-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3657d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3657d-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3657d-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3657d-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3657d-136">INPUTS</span></span>

### <span data-ttu-id="3657d-137">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="3657d-137">IStorageContext</span></span>

<span data-ttu-id="3657d-138">O parâmetro ' Context ' aceita o valor do tipo ' IStorageContext ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="3657d-138">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="3657d-139">String</span><span class="sxs-lookup"><span data-stu-id="3657d-139">String</span></span>

<span data-ttu-id="3657d-140">O parâmetro ' Queue ' aceita o valor do tipo ' String ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="3657d-140">Parameter 'Queue' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="3657d-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3657d-141">OUTPUTS</span></span>

### <span data-ttu-id="3657d-142">System. String</span><span class="sxs-lookup"><span data-stu-id="3657d-142">System.String</span></span>

## <span data-ttu-id="3657d-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3657d-143">NOTES</span></span>

## <span data-ttu-id="3657d-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3657d-144">RELATED LINKS</span></span>

[<span data-ttu-id="3657d-145">Get-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="3657d-145">Get-AzureStorageQueueStoredAccessPolicy</span></span>](./Get-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="3657d-146">New-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="3657d-146">New-AzureStorageQueueStoredAccessPolicy</span></span>](./New-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="3657d-147">Remove-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="3657d-147">Remove-AzureStorageQueueStoredAccessPolicy</span></span>](./Remove-AzureStorageQueueStoredAccessPolicy.md)

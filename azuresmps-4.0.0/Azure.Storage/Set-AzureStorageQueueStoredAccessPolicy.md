---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 4FB7E017-7D37-4EDB-BEC1-36629058B87C
online version: ''
schema: 2.0.0
ms.openlocfilehash: b273dbec3fda421574c8866a10eda0a8098513ff
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93426207"
---
# <span data-ttu-id="3de61-101">Set-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="3de61-101">Set-AzureStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="3de61-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3de61-102">SYNOPSIS</span></span>
<span data-ttu-id="3de61-103">Define uma política de acesso armazenado para uma fila de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="3de61-103">Sets a stored access policy for an Azure storage queue.</span></span>

## <span data-ttu-id="3de61-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3de61-104">SYNTAX</span></span>

```
Set-AzureStorageQueueStoredAccessPolicy [-Queue] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-NoStartTime] [-NoExpiryTime] [-Context <IStorageContext>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3de61-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3de61-105">DESCRIPTION</span></span>
<span data-ttu-id="3de61-106">O cmdlet **set-AzureStorageQueueStoredAccessPolicy** define uma política de acesso armazenado para uma fila de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="3de61-106">The **Set-AzureStorageQueueStoredAccessPolicy** cmdlet sets a stored access policy for an Azure storage queue.</span></span>

## <span data-ttu-id="3de61-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3de61-107">EXAMPLES</span></span>

### <span data-ttu-id="3de61-108">Exemplo 1: definir uma política de acesso armazenado na fila</span><span class="sxs-lookup"><span data-stu-id="3de61-108">Example 1: Set a stored access policy in the queue</span></span>
```
PS C:\> Set-AzureStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy07"
```

<span data-ttu-id="3de61-109">Esse comando define uma política de acesso chamada Policy07 para fila de armazenamento chamada MyQueue.</span><span class="sxs-lookup"><span data-stu-id="3de61-109">This command sets an access policy named Policy07 for storage queue named MyQueue.</span></span>

## <span data-ttu-id="3de61-110">OS</span><span class="sxs-lookup"><span data-stu-id="3de61-110">PARAMETERS</span></span>

### <span data-ttu-id="3de61-111">-Contexto</span><span class="sxs-lookup"><span data-stu-id="3de61-111">-Context</span></span>
<span data-ttu-id="3de61-112">Especifica um contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="3de61-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="3de61-113">Para obter um contexto de armazenamento, use o cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="3de61-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="3de61-114">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="3de61-114">-ExpiryTime</span></span>
<span data-ttu-id="3de61-115">Especifica o tempo em que a política de acesso armazenado se torna inválida.</span><span class="sxs-lookup"><span data-stu-id="3de61-115">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="3de61-116">-NoExpiryTime</span><span class="sxs-lookup"><span data-stu-id="3de61-116">-NoExpiryTime</span></span>
<span data-ttu-id="3de61-117">Indica que a política de acesso não tem data de expiração.</span><span class="sxs-lookup"><span data-stu-id="3de61-117">Indicates that the access policy has no expiration date.</span></span>

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

### <span data-ttu-id="3de61-118">-Nostarttime</span><span class="sxs-lookup"><span data-stu-id="3de61-118">-NoStartTime</span></span>
<span data-ttu-id="3de61-119">Indica que esse cmdlet define a hora de início como $Null.</span><span class="sxs-lookup"><span data-stu-id="3de61-119">Indicates that this cmdlet sets the start time to be $Null.</span></span>

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

### <span data-ttu-id="3de61-120">-Permissão</span><span class="sxs-lookup"><span data-stu-id="3de61-120">-Permission</span></span>
<span data-ttu-id="3de61-121">Especifica o nível de acesso público a essa fila de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="3de61-121">Specifies the level of public access to this storage queue.</span></span>

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

### <span data-ttu-id="3de61-122">-Política</span><span class="sxs-lookup"><span data-stu-id="3de61-122">-Policy</span></span>
<span data-ttu-id="3de61-123">Especifica uma política de acesso armazenado, que inclui as permissões para esse token SAS.</span><span class="sxs-lookup"><span data-stu-id="3de61-123">Specifies a stored access policy, which includes the permissions for this SAS token.</span></span>

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

### <span data-ttu-id="3de61-124">-Queue</span><span class="sxs-lookup"><span data-stu-id="3de61-124">-Queue</span></span>
<span data-ttu-id="3de61-125">Especifica o nome da fila de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="3de61-125">Specifies the Azure storage queue name.</span></span>

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

### <span data-ttu-id="3de61-126">-StartTime</span><span class="sxs-lookup"><span data-stu-id="3de61-126">-StartTime</span></span>
<span data-ttu-id="3de61-127">Especifica a hora em que a política de acesso armazenado se torna válida.</span><span class="sxs-lookup"><span data-stu-id="3de61-127">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="3de61-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="3de61-128">-Confirm</span></span>
<span data-ttu-id="3de61-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3de61-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3de61-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3de61-130">-WhatIf</span></span>
<span data-ttu-id="3de61-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3de61-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3de61-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3de61-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3de61-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3de61-133">CommonParameters</span></span>
<span data-ttu-id="3de61-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3de61-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3de61-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3de61-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3de61-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3de61-136">INPUTS</span></span>

## <span data-ttu-id="3de61-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3de61-137">OUTPUTS</span></span>

## <span data-ttu-id="3de61-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3de61-138">NOTES</span></span>

## <span data-ttu-id="3de61-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3de61-139">RELATED LINKS</span></span>

[<span data-ttu-id="3de61-140">Get-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="3de61-140">Get-AzureStorageQueueStoredAccessPolicy</span></span>](./Get-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="3de61-141">New-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="3de61-141">New-AzureStorageQueueStoredAccessPolicy</span></span>](./New-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="3de61-142">Remove-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="3de61-142">Remove-AzureStorageQueueStoredAccessPolicy</span></span>](./Remove-AzureStorageQueueStoredAccessPolicy.md)

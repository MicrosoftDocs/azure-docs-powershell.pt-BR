---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 4FB7E017-7D37-4EDB-BEC1-36629058B87C
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/set-azurestoragequeuestoredaccesspolicy
schema: 2.0.0
ms.openlocfilehash: 4e1b58e2ca2586ada574b55a03287d1cc5915b6f
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93786593"
---
# <span data-ttu-id="8f64a-101">Set-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="8f64a-101">Set-AzureStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="8f64a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8f64a-102">SYNOPSIS</span></span>
<span data-ttu-id="8f64a-103">Define uma política de acesso armazenado para uma fila de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="8f64a-103">Sets a stored access policy for an Azure storage queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8f64a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8f64a-104">SYNTAX</span></span>

```
Set-AzureStorageQueueStoredAccessPolicy [-Queue] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-NoStartTime] [-NoExpiryTime] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8f64a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8f64a-105">DESCRIPTION</span></span>
<span data-ttu-id="8f64a-106">O cmdlet **set-AzureStorageQueueStoredAccessPolicy** define uma política de acesso armazenado para uma fila de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="8f64a-106">The **Set-AzureStorageQueueStoredAccessPolicy** cmdlet sets a stored access policy for an Azure storage queue.</span></span>

## <span data-ttu-id="8f64a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8f64a-107">EXAMPLES</span></span>

### <span data-ttu-id="8f64a-108">Exemplo 1: definir uma política de acesso armazenado na fila com permissão completa</span><span class="sxs-lookup"><span data-stu-id="8f64a-108">Example 1: Set a stored access policy in the queue with full permission</span></span>
```
PS C:\> Set-AzureStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy07" -Permission arup
```

<span data-ttu-id="8f64a-109">Esse comando define uma política de acesso chamada Policy07 para fila de armazenamento chamada MyQueue.</span><span class="sxs-lookup"><span data-stu-id="8f64a-109">This command sets an access policy named Policy07 for storage queue named MyQueue.</span></span>

## <span data-ttu-id="8f64a-110">OS</span><span class="sxs-lookup"><span data-stu-id="8f64a-110">PARAMETERS</span></span>

### <span data-ttu-id="8f64a-111">-Contexto</span><span class="sxs-lookup"><span data-stu-id="8f64a-111">-Context</span></span>
<span data-ttu-id="8f64a-112">Especifica um contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="8f64a-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="8f64a-113">Para obter um contexto de armazenamento, use o cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="8f64a-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="8f64a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f64a-114">-DefaultProfile</span></span>
<span data-ttu-id="8f64a-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8f64a-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8f64a-116">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="8f64a-116">-ExpiryTime</span></span>
<span data-ttu-id="8f64a-117">Especifica o tempo em que a política de acesso armazenado se torna inválida.</span><span class="sxs-lookup"><span data-stu-id="8f64a-117">Specifies the time at which the stored access policy becomes invalid.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f64a-118">-NoExpiryTime</span><span class="sxs-lookup"><span data-stu-id="8f64a-118">-NoExpiryTime</span></span>
<span data-ttu-id="8f64a-119">Indica que a política de acesso não tem data de expiração.</span><span class="sxs-lookup"><span data-stu-id="8f64a-119">Indicates that the access policy has no expiration date.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f64a-120">-Nostarttime</span><span class="sxs-lookup"><span data-stu-id="8f64a-120">-NoStartTime</span></span>
<span data-ttu-id="8f64a-121">Indica que esse cmdlet define a hora de início como $Null.</span><span class="sxs-lookup"><span data-stu-id="8f64a-121">Indicates that this cmdlet sets the start time to be $Null.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f64a-122">-Permissão</span><span class="sxs-lookup"><span data-stu-id="8f64a-122">-Permission</span></span>
<span data-ttu-id="8f64a-123">Especifica as permissões na política de acesso armazenado para acessar a fila de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="8f64a-123">Specifies permissions in the stored access policy to access the storage queue.</span></span>
<span data-ttu-id="8f64a-124">É importante observar que essa é uma cadeia de caracteres, como `rwd` (para ler, gravar e excluir).</span><span class="sxs-lookup"><span data-stu-id="8f64a-124">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f64a-125">-Política</span><span class="sxs-lookup"><span data-stu-id="8f64a-125">-Policy</span></span>
<span data-ttu-id="8f64a-126">Especifica o nome da política de acesso armazenado.</span><span class="sxs-lookup"><span data-stu-id="8f64a-126">Specifies the name for the stored access policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f64a-127">-Queue</span><span class="sxs-lookup"><span data-stu-id="8f64a-127">-Queue</span></span>
<span data-ttu-id="8f64a-128">Especifica o nome da fila de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="8f64a-128">Specifies the Azure storage queue name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8f64a-129">-StartTime</span><span class="sxs-lookup"><span data-stu-id="8f64a-129">-StartTime</span></span>
<span data-ttu-id="8f64a-130">Especifica a hora em que a política de acesso armazenado se torna válida.</span><span class="sxs-lookup"><span data-stu-id="8f64a-130">Specifies the time at which the stored access policy becomes valid.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f64a-131">-Confirme</span><span class="sxs-lookup"><span data-stu-id="8f64a-131">-Confirm</span></span>
<span data-ttu-id="8f64a-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8f64a-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f64a-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f64a-133">-WhatIf</span></span>
<span data-ttu-id="8f64a-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8f64a-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8f64a-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8f64a-135">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f64a-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f64a-136">CommonParameters</span></span>
<span data-ttu-id="8f64a-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f64a-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f64a-138">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f64a-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f64a-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8f64a-139">INPUTS</span></span>

### <span data-ttu-id="8f64a-140">System. String</span><span class="sxs-lookup"><span data-stu-id="8f64a-140">System.String</span></span>

### <span data-ttu-id="8f64a-141">Microsoft. Azure. Commands. Common. Authentication. Abstractings. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="8f64a-141">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="8f64a-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8f64a-142">OUTPUTS</span></span>

### <span data-ttu-id="8f64a-143">System. String</span><span class="sxs-lookup"><span data-stu-id="8f64a-143">System.String</span></span>

## <span data-ttu-id="8f64a-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8f64a-144">NOTES</span></span>

## <span data-ttu-id="8f64a-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8f64a-145">RELATED LINKS</span></span>

[<span data-ttu-id="8f64a-146">Get-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="8f64a-146">Get-AzureStorageQueueStoredAccessPolicy</span></span>](./Get-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="8f64a-147">New-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="8f64a-147">New-AzureStorageQueueStoredAccessPolicy</span></span>](./New-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="8f64a-148">Remove-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="8f64a-148">Remove-AzureStorageQueueStoredAccessPolicy</span></span>](./Remove-AzureStorageQueueStoredAccessPolicy.md)

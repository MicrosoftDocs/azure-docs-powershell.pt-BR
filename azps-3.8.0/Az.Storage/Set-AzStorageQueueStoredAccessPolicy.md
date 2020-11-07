---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 4FB7E017-7D37-4EDB-BEC1-36629058B87C
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstoragequeuestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageQueueStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageQueueStoredAccessPolicy.md
ms.openlocfilehash: 0f8d9860f04112c197b91907a7622683069c3589
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93941513"
---
# <span data-ttu-id="6170f-101">Set-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="6170f-101">Set-AzStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="6170f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6170f-102">SYNOPSIS</span></span>
<span data-ttu-id="6170f-103">Define uma política de acesso armazenado para uma fila de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="6170f-103">Sets a stored access policy for an Azure storage queue.</span></span>

## <span data-ttu-id="6170f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6170f-104">SYNTAX</span></span>

```
Set-AzStorageQueueStoredAccessPolicy [-Queue] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-NoStartTime] [-NoExpiryTime] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6170f-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6170f-105">DESCRIPTION</span></span>
<span data-ttu-id="6170f-106">O cmdlet **set-AzStorageQueueStoredAccessPolicy** define uma política de acesso armazenado para uma fila de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="6170f-106">The **Set-AzStorageQueueStoredAccessPolicy** cmdlet sets a stored access policy for an Azure storage queue.</span></span>

## <span data-ttu-id="6170f-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6170f-107">EXAMPLES</span></span>

### <span data-ttu-id="6170f-108">Exemplo 1: definir uma política de acesso armazenado na fila com permissão completa</span><span class="sxs-lookup"><span data-stu-id="6170f-108">Example 1: Set a stored access policy in the queue with full permission</span></span>
```
PS C:\> Set-AzStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy07" -Permission arup
```

<span data-ttu-id="6170f-109">Esse comando define uma política de acesso chamada Policy07 para fila de armazenamento chamada MyQueue.</span><span class="sxs-lookup"><span data-stu-id="6170f-109">This command sets an access policy named Policy07 for storage queue named MyQueue.</span></span>

## <span data-ttu-id="6170f-110">OS</span><span class="sxs-lookup"><span data-stu-id="6170f-110">PARAMETERS</span></span>

### <span data-ttu-id="6170f-111">-Contexto</span><span class="sxs-lookup"><span data-stu-id="6170f-111">-Context</span></span>
<span data-ttu-id="6170f-112">Especifica um contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="6170f-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="6170f-113">Para obter um contexto de armazenamento, use o cmdlet New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="6170f-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="6170f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6170f-114">-DefaultProfile</span></span>
<span data-ttu-id="6170f-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6170f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6170f-116">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="6170f-116">-ExpiryTime</span></span>
<span data-ttu-id="6170f-117">Especifica o tempo em que a política de acesso armazenado se torna inválida.</span><span class="sxs-lookup"><span data-stu-id="6170f-117">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="6170f-118">-NoExpiryTime</span><span class="sxs-lookup"><span data-stu-id="6170f-118">-NoExpiryTime</span></span>
<span data-ttu-id="6170f-119">Indica que a política de acesso não tem data de expiração.</span><span class="sxs-lookup"><span data-stu-id="6170f-119">Indicates that the access policy has no expiration date.</span></span>

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

### <span data-ttu-id="6170f-120">-Nostarttime</span><span class="sxs-lookup"><span data-stu-id="6170f-120">-NoStartTime</span></span>
<span data-ttu-id="6170f-121">Indica que esse cmdlet define a hora de início como $Null.</span><span class="sxs-lookup"><span data-stu-id="6170f-121">Indicates that this cmdlet sets the start time to be $Null.</span></span>

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

### <span data-ttu-id="6170f-122">-Permissão</span><span class="sxs-lookup"><span data-stu-id="6170f-122">-Permission</span></span>
<span data-ttu-id="6170f-123">Especifica as permissões na política de acesso armazenado para acessar a fila de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="6170f-123">Specifies permissions in the stored access policy to access the storage queue.</span></span>
<span data-ttu-id="6170f-124">É importante observar que essa é uma cadeia de caracteres, como `rwd` (para ler, gravar e excluir).</span><span class="sxs-lookup"><span data-stu-id="6170f-124">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="6170f-125">-Política</span><span class="sxs-lookup"><span data-stu-id="6170f-125">-Policy</span></span>
<span data-ttu-id="6170f-126">Especifica o nome da política de acesso armazenado.</span><span class="sxs-lookup"><span data-stu-id="6170f-126">Specifies the name for the stored access policy.</span></span>

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

### <span data-ttu-id="6170f-127">-Queue</span><span class="sxs-lookup"><span data-stu-id="6170f-127">-Queue</span></span>
<span data-ttu-id="6170f-128">Especifica o nome da fila de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="6170f-128">Specifies the Azure storage queue name.</span></span>

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

### <span data-ttu-id="6170f-129">-StartTime</span><span class="sxs-lookup"><span data-stu-id="6170f-129">-StartTime</span></span>
<span data-ttu-id="6170f-130">Especifica a hora em que a política de acesso armazenado se torna válida.</span><span class="sxs-lookup"><span data-stu-id="6170f-130">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="6170f-131">-Confirme</span><span class="sxs-lookup"><span data-stu-id="6170f-131">-Confirm</span></span>
<span data-ttu-id="6170f-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6170f-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6170f-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6170f-133">-WhatIf</span></span>
<span data-ttu-id="6170f-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6170f-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6170f-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6170f-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6170f-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6170f-136">CommonParameters</span></span>
<span data-ttu-id="6170f-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6170f-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6170f-138">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6170f-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6170f-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6170f-139">INPUTS</span></span>

### <span data-ttu-id="6170f-140">System. String</span><span class="sxs-lookup"><span data-stu-id="6170f-140">System.String</span></span>

### <span data-ttu-id="6170f-141">Microsoft. Azure. Commands. Common. Authentication. Abstractings. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="6170f-141">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="6170f-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6170f-142">OUTPUTS</span></span>

### <span data-ttu-id="6170f-143">System. String</span><span class="sxs-lookup"><span data-stu-id="6170f-143">System.String</span></span>

## <span data-ttu-id="6170f-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6170f-144">NOTES</span></span>

## <span data-ttu-id="6170f-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6170f-145">RELATED LINKS</span></span>

[<span data-ttu-id="6170f-146">Get-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="6170f-146">Get-AzStorageQueueStoredAccessPolicy</span></span>](./Get-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="6170f-147">New-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="6170f-147">New-AzStorageQueueStoredAccessPolicy</span></span>](./New-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="6170f-148">Remove-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="6170f-148">Remove-AzStorageQueueStoredAccessPolicy</span></span>](./Remove-AzStorageQueueStoredAccessPolicy.md)

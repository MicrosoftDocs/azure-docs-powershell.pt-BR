---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: F1EC601C-3ADD-402A-A5F7-84A95D312187
online version: https://docs.microsoft.com/powershell/module/az.storage/get-azstoragequeuestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageQueueStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageQueueStoredAccessPolicy.md
ms.openlocfilehash: fbd5adc202886ae987f7739ac24d1dadbc0d41d8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889065"
---
# <span data-ttu-id="9bc9a-101">Get-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="9bc9a-101">Get-AzStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="9bc9a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9bc9a-102">SYNOPSIS</span></span>
<span data-ttu-id="9bc9a-103">Obtém a política ou políticas de acesso armazenado para uma fila de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="9bc9a-103">Gets the stored access policy or policies for an Azure storage queue.</span></span>

## <span data-ttu-id="9bc9a-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="9bc9a-104">SYNTAX</span></span>

```
Get-AzStorageQueueStoredAccessPolicy [-Queue] <String> [[-Policy] <String>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9bc9a-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="9bc9a-105">DESCRIPTION</span></span>
<span data-ttu-id="9bc9a-106">O cmdlet **Get-AzStorageQueueStoredAccessPolicy** lista a política de acesso armazenado ou as políticas de uma fila de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="9bc9a-106">The **Get-AzStorageQueueStoredAccessPolicy** cmdlet lists the stored access policy or policies for an Azure storage queue.</span></span>

## <span data-ttu-id="9bc9a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9bc9a-107">EXAMPLES</span></span>

### <span data-ttu-id="9bc9a-108">Exemplo 1: Obter uma política de acesso armazenado na fila</span><span class="sxs-lookup"><span data-stu-id="9bc9a-108">Example 1: Get a stored access policy in the queue</span></span>
```
PS C:\>Get-AzStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy12"
```

<span data-ttu-id="9bc9a-109">Este comando obtém a política de acesso chamada Policy12 na fila de armazenamento chamada MyQueue.</span><span class="sxs-lookup"><span data-stu-id="9bc9a-109">This command gets the access policy named Policy12 in the storage queue named MyQueue.</span></span>

### <span data-ttu-id="9bc9a-110">Exemplo 2: Obter todas as políticas de acesso armazenadas na fila</span><span class="sxs-lookup"><span data-stu-id="9bc9a-110">Example 2: Get all stored access policies in the queue</span></span>
```
PS C:\>Get-AzStorageQueueStoredAccessPolicy -Queue "MyQueue"
```

<span data-ttu-id="9bc9a-111">Esse comando obtém todas as políticas de acesso armazenadas na fila chamada MyQueue.</span><span class="sxs-lookup"><span data-stu-id="9bc9a-111">This command gets all stored access policies in the queue named MyQueue.</span></span>

## <span data-ttu-id="9bc9a-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="9bc9a-112">PARAMETERS</span></span>

### <span data-ttu-id="9bc9a-113">-Context</span><span class="sxs-lookup"><span data-stu-id="9bc9a-113">-Context</span></span>
<span data-ttu-id="9bc9a-114">Especifica o contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="9bc9a-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="9bc9a-115">Para obter um contexto de armazenamento, use o New-AzStorageContext cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9bc9a-115">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="9bc9a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9bc9a-116">-DefaultProfile</span></span>
<span data-ttu-id="9bc9a-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9bc9a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9bc9a-118">-Policy</span><span class="sxs-lookup"><span data-stu-id="9bc9a-118">-Policy</span></span>
<span data-ttu-id="9bc9a-119">Especifica uma política de acesso armazenada, que inclui as permissões para este token SAS (Assinatura de Acesso Compartilhado).</span><span class="sxs-lookup"><span data-stu-id="9bc9a-119">Specifies a stored access policy, which includes the permissions for this Shared Access Signature (SAS) token.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9bc9a-120">-Queue</span><span class="sxs-lookup"><span data-stu-id="9bc9a-120">-Queue</span></span>
<span data-ttu-id="9bc9a-121">Especifica o nome da fila de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="9bc9a-121">Specifies the Azure storage queue name.</span></span>

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

### <span data-ttu-id="9bc9a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9bc9a-122">CommonParameters</span></span>
<span data-ttu-id="9bc9a-123">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9bc9a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9bc9a-124">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9bc9a-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9bc9a-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9bc9a-125">INPUTS</span></span>

### <span data-ttu-id="9bc9a-126">System.String</span><span class="sxs-lookup"><span data-stu-id="9bc9a-126">System.String</span></span>

### <span data-ttu-id="9bc9a-127">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="9bc9a-127">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="9bc9a-128">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="9bc9a-128">OUTPUTS</span></span>

### <span data-ttu-id="9bc9a-129">Microsoft.Azure.Storage.Queue.SharedAccessQueuePolicy</span><span class="sxs-lookup"><span data-stu-id="9bc9a-129">Microsoft.Azure.Storage.Queue.SharedAccessQueuePolicy</span></span>

## <span data-ttu-id="9bc9a-130">NOTES</span><span class="sxs-lookup"><span data-stu-id="9bc9a-130">NOTES</span></span>

## <span data-ttu-id="9bc9a-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9bc9a-131">RELATED LINKS</span></span>

[<span data-ttu-id="9bc9a-132">New-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="9bc9a-132">New-AzStorageQueueStoredAccessPolicy</span></span>](./New-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="9bc9a-133">Remove-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="9bc9a-133">Remove-AzStorageQueueStoredAccessPolicy</span></span>](./Remove-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="9bc9a-134">Set-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="9bc9a-134">Set-AzStorageQueueStoredAccessPolicy</span></span>](./Set-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="9bc9a-135">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="9bc9a-135">New-AzStorageContext</span></span>](./New-AzStorageContext.md)



---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: F1EC601C-3ADD-402A-A5F7-84A95D312187
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestoragequeuestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageQueueStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageQueueStoredAccessPolicy.md
ms.openlocfilehash: d0daabef3f4fe9ef60a90365054e12e869f0856a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602502"
---
# <span data-ttu-id="1c4f2-101">Get-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="1c4f2-101">Get-AzureStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="1c4f2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1c4f2-102">SYNOPSIS</span></span>
<span data-ttu-id="1c4f2-103">Obtém a política de acesso armazenado ou políticas para uma fila de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="1c4f2-103">Gets the stored access policy or policies for an Azure storage queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1c4f2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1c4f2-104">SYNTAX</span></span>

```
Get-AzureStorageQueueStoredAccessPolicy [-Queue] <String> [[-Policy] <String>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1c4f2-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1c4f2-105">DESCRIPTION</span></span>
<span data-ttu-id="1c4f2-106">O cmdlet **Get-AzureStorageQueueStoredAccessPolicy** lista as políticas ou políticas de acesso armazenadas para uma fila de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="1c4f2-106">The **Get-AzureStorageQueueStoredAccessPolicy** cmdlet lists the stored access policy or policies for an Azure storage queue.</span></span>

## <span data-ttu-id="1c4f2-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1c4f2-107">EXAMPLES</span></span>

### <span data-ttu-id="1c4f2-108">Exemplo 1: obter uma política de acesso armazenado na fila</span><span class="sxs-lookup"><span data-stu-id="1c4f2-108">Example 1: Get a stored access policy in the queue</span></span>
```
PS C:\>Get-AzureStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy12"
```

<span data-ttu-id="1c4f2-109">Esse comando obtém a política de acesso chamada Policy12 na fila de armazenamento chamada MyQueue.</span><span class="sxs-lookup"><span data-stu-id="1c4f2-109">This command gets the access policy named Policy12 in the storage queue named MyQueue.</span></span>

### <span data-ttu-id="1c4f2-110">Exemplo 2: obter todas as políticas de acesso armazenadas na fila</span><span class="sxs-lookup"><span data-stu-id="1c4f2-110">Example 2: Get all stored access policies in the queue</span></span>
```
PS C:\>Get-AzureStorageQueueStoredAccessPolicy -Queue "MyQueue"
```

<span data-ttu-id="1c4f2-111">Esse comando obtém todas as políticas de acesso armazenadas na fila chamada MyQueue.</span><span class="sxs-lookup"><span data-stu-id="1c4f2-111">This command gets all stored access policies in the queue named MyQueue.</span></span>

## <span data-ttu-id="1c4f2-112">OS</span><span class="sxs-lookup"><span data-stu-id="1c4f2-112">PARAMETERS</span></span>

### <span data-ttu-id="1c4f2-113">-Contexto</span><span class="sxs-lookup"><span data-stu-id="1c4f2-113">-Context</span></span>
<span data-ttu-id="1c4f2-114">Especifica o contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="1c4f2-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="1c4f2-115">Para obter um contexto de armazenamento, use o cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="1c4f2-115">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="1c4f2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c4f2-116">-DefaultProfile</span></span>
<span data-ttu-id="1c4f2-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1c4f2-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1c4f2-118">-Política</span><span class="sxs-lookup"><span data-stu-id="1c4f2-118">-Policy</span></span>
<span data-ttu-id="1c4f2-119">Especifica uma política de acesso armazenado, que inclui as permissões para este token de assinatura de acesso compartilhado (SAS).</span><span class="sxs-lookup"><span data-stu-id="1c4f2-119">Specifies a stored access policy, which includes the permissions for this Shared Access Signature (SAS) token.</span></span>

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

### <span data-ttu-id="1c4f2-120">-Queue</span><span class="sxs-lookup"><span data-stu-id="1c4f2-120">-Queue</span></span>
<span data-ttu-id="1c4f2-121">Especifica o nome da fila de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="1c4f2-121">Specifies the Azure storage queue name.</span></span>

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

### <span data-ttu-id="1c4f2-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c4f2-122">CommonParameters</span></span>
<span data-ttu-id="1c4f2-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c4f2-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c4f2-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1c4f2-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c4f2-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1c4f2-125">INPUTS</span></span>

### <span data-ttu-id="1c4f2-126">System. String</span><span class="sxs-lookup"><span data-stu-id="1c4f2-126">System.String</span></span>

### <span data-ttu-id="1c4f2-127">Microsoft. Azure. Commands. Common. Authentication. Abstractings. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="1c4f2-127">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="1c4f2-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1c4f2-128">OUTPUTS</span></span>

### <span data-ttu-id="1c4f2-129">Microsoft. WindowsAzure. Storage. Queue. SharedAccessQueuePolicy</span><span class="sxs-lookup"><span data-stu-id="1c4f2-129">Microsoft.WindowsAzure.Storage.Queue.SharedAccessQueuePolicy</span></span>

## <span data-ttu-id="1c4f2-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1c4f2-130">NOTES</span></span>

## <span data-ttu-id="1c4f2-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1c4f2-131">RELATED LINKS</span></span>

[<span data-ttu-id="1c4f2-132">New-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="1c4f2-132">New-AzureStorageQueueStoredAccessPolicy</span></span>](./New-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="1c4f2-133">Remove-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="1c4f2-133">Remove-AzureStorageQueueStoredAccessPolicy</span></span>](./Remove-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="1c4f2-134">Set-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="1c4f2-134">Set-AzureStorageQueueStoredAccessPolicy</span></span>](./Set-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="1c4f2-135">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="1c4f2-135">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)



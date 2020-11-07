---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: F1EC601C-3ADD-402A-A5F7-84A95D312187
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragequeuestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Get-AzStorageQueueStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Get-AzStorageQueueStoredAccessPolicy.md
ms.openlocfilehash: 9c61542aeb79cdcaa90d4ac32be4be38649e4abd
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776256"
---
# <span data-ttu-id="2b3f6-101">Get-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="2b3f6-101">Get-AzStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="2b3f6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2b3f6-102">SYNOPSIS</span></span>
<span data-ttu-id="2b3f6-103">Obtém a política de acesso armazenado ou políticas para uma fila de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="2b3f6-103">Gets the stored access policy or policies for an Azure storage queue.</span></span>

## <span data-ttu-id="2b3f6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2b3f6-104">SYNTAX</span></span>

```
Get-AzStorageQueueStoredAccessPolicy [-Queue] <String> [[-Policy] <String>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2b3f6-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2b3f6-105">DESCRIPTION</span></span>
<span data-ttu-id="2b3f6-106">O cmdlet **Get-AzStorageQueueStoredAccessPolicy** lista as políticas ou políticas de acesso armazenadas para uma fila de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="2b3f6-106">The **Get-AzStorageQueueStoredAccessPolicy** cmdlet lists the stored access policy or policies for an Azure storage queue.</span></span>

## <span data-ttu-id="2b3f6-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2b3f6-107">EXAMPLES</span></span>

### <span data-ttu-id="2b3f6-108">Exemplo 1: obter uma política de acesso armazenado na fila</span><span class="sxs-lookup"><span data-stu-id="2b3f6-108">Example 1: Get a stored access policy in the queue</span></span>
```
PS C:\>Get-AzStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy12"
```

<span data-ttu-id="2b3f6-109">Esse comando obtém a política de acesso chamada Policy12 na fila de armazenamento chamada MyQueue.</span><span class="sxs-lookup"><span data-stu-id="2b3f6-109">This command gets the access policy named Policy12 in the storage queue named MyQueue.</span></span>

### <span data-ttu-id="2b3f6-110">Exemplo 2: obter todas as políticas de acesso armazenadas na fila</span><span class="sxs-lookup"><span data-stu-id="2b3f6-110">Example 2: Get all stored access policies in the queue</span></span>
```
PS C:\>Get-AzStorageQueueStoredAccessPolicy -Queue "MyQueue"
```

<span data-ttu-id="2b3f6-111">Esse comando obtém todas as políticas de acesso armazenadas na fila chamada MyQueue.</span><span class="sxs-lookup"><span data-stu-id="2b3f6-111">This command gets all stored access policies in the queue named MyQueue.</span></span>

## <span data-ttu-id="2b3f6-112">OS</span><span class="sxs-lookup"><span data-stu-id="2b3f6-112">PARAMETERS</span></span>

### <span data-ttu-id="2b3f6-113">-Contexto</span><span class="sxs-lookup"><span data-stu-id="2b3f6-113">-Context</span></span>
<span data-ttu-id="2b3f6-114">Especifica o contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="2b3f6-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="2b3f6-115">Para obter um contexto de armazenamento, use o cmdlet New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="2b3f6-115">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="2b3f6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b3f6-116">-DefaultProfile</span></span>
<span data-ttu-id="2b3f6-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2b3f6-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2b3f6-118">-Política</span><span class="sxs-lookup"><span data-stu-id="2b3f6-118">-Policy</span></span>
<span data-ttu-id="2b3f6-119">Especifica uma política de acesso armazenado, que inclui as permissões para este token de assinatura de acesso compartilhado (SAS).</span><span class="sxs-lookup"><span data-stu-id="2b3f6-119">Specifies a stored access policy, which includes the permissions for this Shared Access Signature (SAS) token.</span></span>

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

### <span data-ttu-id="2b3f6-120">-Queue</span><span class="sxs-lookup"><span data-stu-id="2b3f6-120">-Queue</span></span>
<span data-ttu-id="2b3f6-121">Especifica o nome da fila de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="2b3f6-121">Specifies the Azure storage queue name.</span></span>

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

### <span data-ttu-id="2b3f6-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b3f6-122">CommonParameters</span></span>
<span data-ttu-id="2b3f6-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b3f6-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b3f6-124">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b3f6-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b3f6-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2b3f6-125">INPUTS</span></span>

### <span data-ttu-id="2b3f6-126">System. String</span><span class="sxs-lookup"><span data-stu-id="2b3f6-126">System.String</span></span>

### <span data-ttu-id="2b3f6-127">Microsoft. Azure. Commands. Common. Authentication. Abstractings. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="2b3f6-127">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="2b3f6-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2b3f6-128">OUTPUTS</span></span>

### <span data-ttu-id="2b3f6-129">Microsoft. WindowsAz. Storage. Queue. SharedAccessQueuePolicy</span><span class="sxs-lookup"><span data-stu-id="2b3f6-129">Microsoft.WindowsAz.Storage.Queue.SharedAccessQueuePolicy</span></span>

## <span data-ttu-id="2b3f6-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2b3f6-130">NOTES</span></span>

## <span data-ttu-id="2b3f6-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2b3f6-131">RELATED LINKS</span></span>

[<span data-ttu-id="2b3f6-132">New-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="2b3f6-132">New-AzStorageQueueStoredAccessPolicy</span></span>](./New-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="2b3f6-133">Remove-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="2b3f6-133">Remove-AzStorageQueueStoredAccessPolicy</span></span>](./Remove-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="2b3f6-134">Set-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="2b3f6-134">Set-AzStorageQueueStoredAccessPolicy</span></span>](./Set-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="2b3f6-135">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="2b3f6-135">New-AzStorageContext</span></span>](./New-AzStorageContext.md)



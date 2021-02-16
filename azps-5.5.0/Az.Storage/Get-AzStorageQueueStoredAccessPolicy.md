---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: F1EC601C-3ADD-402A-A5F7-84A95D312187
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragequeuestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageQueueStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageQueueStoredAccessPolicy.md
ms.openlocfilehash: b1e7f305b571c5b40c12dacadf520f9637e076f3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118585"
---
# <span data-ttu-id="ab674-101">Get-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ab674-101">Get-AzStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="ab674-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ab674-102">SYNOPSIS</span></span>
<span data-ttu-id="ab674-103">Obtém a política de acesso ou as políticas de acesso armazenadas para uma fila de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="ab674-103">Gets the stored access policy or policies for an Azure storage queue.</span></span>

## <span data-ttu-id="ab674-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ab674-104">SYNTAX</span></span>

```
Get-AzStorageQueueStoredAccessPolicy [-Queue] <String> [[-Policy] <String>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ab674-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="ab674-105">DESCRIPTION</span></span>
<span data-ttu-id="ab674-106">O cmdlet **Get-AzStorageQueueStoredAccessPolicy** lista a política de acesso armazenada ou as políticas de uma fila de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="ab674-106">The **Get-AzStorageQueueStoredAccessPolicy** cmdlet lists the stored access policy or policies for an Azure storage queue.</span></span>

## <span data-ttu-id="ab674-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="ab674-107">EXAMPLES</span></span>

### <span data-ttu-id="ab674-108">Exemplo 1: Obter uma política de acesso armazenada na fila</span><span class="sxs-lookup"><span data-stu-id="ab674-108">Example 1: Get a stored access policy in the queue</span></span>
```
PS C:\>Get-AzStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy12"
```

<span data-ttu-id="ab674-109">Esse comando obtém a política de acesso chamada Política12 na fila de armazenamento chamada MyQueue.</span><span class="sxs-lookup"><span data-stu-id="ab674-109">This command gets the access policy named Policy12 in the storage queue named MyQueue.</span></span>

### <span data-ttu-id="ab674-110">Exemplo 2: Obter todas as políticas de acesso armazenadas na fila</span><span class="sxs-lookup"><span data-stu-id="ab674-110">Example 2: Get all stored access policies in the queue</span></span>
```
PS C:\>Get-AzStorageQueueStoredAccessPolicy -Queue "MyQueue"
```

<span data-ttu-id="ab674-111">Esse comando obtém todas as políticas de acesso armazenadas na fila chamada MyQueue.</span><span class="sxs-lookup"><span data-stu-id="ab674-111">This command gets all stored access policies in the queue named MyQueue.</span></span>

## <span data-ttu-id="ab674-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ab674-112">PARAMETERS</span></span>

### <span data-ttu-id="ab674-113">-Contexto</span><span class="sxs-lookup"><span data-stu-id="ab674-113">-Context</span></span>
<span data-ttu-id="ab674-114">Especifica o contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="ab674-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="ab674-115">Para obter um contexto de armazenamento, use o New-AzStorageContext cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ab674-115">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="ab674-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab674-116">-DefaultProfile</span></span>
<span data-ttu-id="ab674-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ab674-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ab674-118">-Política</span><span class="sxs-lookup"><span data-stu-id="ab674-118">-Policy</span></span>
<span data-ttu-id="ab674-119">Especifica uma política de acesso armazenada, que inclui as permissões para este token de Assinatura de Acesso Compartilhado (SAS).</span><span class="sxs-lookup"><span data-stu-id="ab674-119">Specifies a stored access policy, which includes the permissions for this Shared Access Signature (SAS) token.</span></span>

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

### <span data-ttu-id="ab674-120">-Fila</span><span class="sxs-lookup"><span data-stu-id="ab674-120">-Queue</span></span>
<span data-ttu-id="ab674-121">Especifica o nome da fila de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="ab674-121">Specifies the Azure storage queue name.</span></span>

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

### <span data-ttu-id="ab674-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab674-122">CommonParameters</span></span>
<span data-ttu-id="ab674-123">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab674-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab674-124">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab674-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab674-125">Entradas</span><span class="sxs-lookup"><span data-stu-id="ab674-125">INPUTS</span></span>

### <span data-ttu-id="ab674-126">System.String</span><span class="sxs-lookup"><span data-stu-id="ab674-126">System.String</span></span>

### <span data-ttu-id="ab674-127">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="ab674-127">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="ab674-128">Saídas</span><span class="sxs-lookup"><span data-stu-id="ab674-128">OUTPUTS</span></span>

### <span data-ttu-id="ab674-129">Microsoft.Azure.Storage.Queue.SharedAccessQueuePolicy</span><span class="sxs-lookup"><span data-stu-id="ab674-129">Microsoft.Azure.Storage.Queue.SharedAccessQueuePolicy</span></span>

## <span data-ttu-id="ab674-130">Notas</span><span class="sxs-lookup"><span data-stu-id="ab674-130">NOTES</span></span>

## <span data-ttu-id="ab674-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ab674-131">RELATED LINKS</span></span>

[<span data-ttu-id="ab674-132">New-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ab674-132">New-AzStorageQueueStoredAccessPolicy</span></span>](./New-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="ab674-133">Remove-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ab674-133">Remove-AzStorageQueueStoredAccessPolicy</span></span>](./Remove-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="ab674-134">Set-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ab674-134">Set-AzStorageQueueStoredAccessPolicy</span></span>](./Set-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="ab674-135">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="ab674-135">New-AzStorageContext</span></span>](./New-AzStorageContext.md)



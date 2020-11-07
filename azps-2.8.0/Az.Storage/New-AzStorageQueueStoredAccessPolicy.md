---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 351145AC-7C1E-4EB7-A17D-B8B7D8ED8DAB
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragequeuestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageQueueStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageQueueStoredAccessPolicy.md
ms.openlocfilehash: 39e83844898771d25c5e2f8a62e4814b36b5e85f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93772781"
---
# <span data-ttu-id="3353d-101">New-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="3353d-101">New-AzStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="3353d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3353d-102">SYNOPSIS</span></span>
<span data-ttu-id="3353d-103">Cria uma política de acesso armazenado para uma fila de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="3353d-103">Creates a stored access policy for an Azure storage queue.</span></span>

## <span data-ttu-id="3353d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3353d-104">SYNTAX</span></span>

```
New-AzStorageQueueStoredAccessPolicy [-Queue] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3353d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3353d-105">DESCRIPTION</span></span>
<span data-ttu-id="3353d-106">O cmdlet **New-AzStorageQueueStoredAccessPolicy** cria uma política de acesso armazenado para uma fila de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="3353d-106">The **New-AzStorageQueueStoredAccessPolicy** cmdlet creates a stored access policy for an Azure storage queue.</span></span>

## <span data-ttu-id="3353d-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3353d-107">EXAMPLES</span></span>

### <span data-ttu-id="3353d-108">Exemplo 1: criar uma política de acesso armazenado em uma fila de armazenamento</span><span class="sxs-lookup"><span data-stu-id="3353d-108">Example 1: Create a stored access policy in a storage queue</span></span>
```
PS C:\>New-AzStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy01"
```

<span data-ttu-id="3353d-109">Esse comando cria uma política de acesso chamada Policy01 na fila de armazenamento chamada MyQueue.</span><span class="sxs-lookup"><span data-stu-id="3353d-109">This command creates an access policy named Policy01 in the storage queue named MyQueue.</span></span>

## <span data-ttu-id="3353d-110">OS</span><span class="sxs-lookup"><span data-stu-id="3353d-110">PARAMETERS</span></span>

### <span data-ttu-id="3353d-111">-Contexto</span><span class="sxs-lookup"><span data-stu-id="3353d-111">-Context</span></span>
<span data-ttu-id="3353d-112">Especifica um contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="3353d-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="3353d-113">Para obter um contexto de armazenamento, use o cmdlet New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="3353d-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="3353d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3353d-114">-DefaultProfile</span></span>
<span data-ttu-id="3353d-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3353d-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3353d-116">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="3353d-116">-ExpiryTime</span></span>
<span data-ttu-id="3353d-117">Especifica o tempo em que a política de acesso armazenado se torna inválida.</span><span class="sxs-lookup"><span data-stu-id="3353d-117">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="3353d-118">-Permissão</span><span class="sxs-lookup"><span data-stu-id="3353d-118">-Permission</span></span>
<span data-ttu-id="3353d-119">Especifica as permissões na política de acesso armazenado para acessar a fila de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="3353d-119">Specifies permissions in the stored access policy to access the storage queue.</span></span>
<span data-ttu-id="3353d-120">É importante observar que essa é uma cadeia de caracteres, como `rwd` (para ler, gravar e excluir).</span><span class="sxs-lookup"><span data-stu-id="3353d-120">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="3353d-121">-Política</span><span class="sxs-lookup"><span data-stu-id="3353d-121">-Policy</span></span>
<span data-ttu-id="3353d-122">Especifica um nome para a política de acesso armazenada.</span><span class="sxs-lookup"><span data-stu-id="3353d-122">Specifies a name for the stored access policy.</span></span>

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

### <span data-ttu-id="3353d-123">-Queue</span><span class="sxs-lookup"><span data-stu-id="3353d-123">-Queue</span></span>
<span data-ttu-id="3353d-124">Especifica o nome da fila de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="3353d-124">Specifies the Azure storage queue name.</span></span>

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

### <span data-ttu-id="3353d-125">-StartTime</span><span class="sxs-lookup"><span data-stu-id="3353d-125">-StartTime</span></span>
<span data-ttu-id="3353d-126">Especifica a hora em que a política de acesso armazenado se torna válida.</span><span class="sxs-lookup"><span data-stu-id="3353d-126">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="3353d-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3353d-127">CommonParameters</span></span>
<span data-ttu-id="3353d-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3353d-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3353d-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3353d-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3353d-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3353d-130">INPUTS</span></span>

### <span data-ttu-id="3353d-131">System. String</span><span class="sxs-lookup"><span data-stu-id="3353d-131">System.String</span></span>

### <span data-ttu-id="3353d-132">Microsoft. Azure. Commands. Common. Authentication. Abstractings. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="3353d-132">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="3353d-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3353d-133">OUTPUTS</span></span>

### <span data-ttu-id="3353d-134">System. String</span><span class="sxs-lookup"><span data-stu-id="3353d-134">System.String</span></span>

## <span data-ttu-id="3353d-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3353d-135">NOTES</span></span>

## <span data-ttu-id="3353d-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3353d-136">RELATED LINKS</span></span>

[<span data-ttu-id="3353d-137">Get-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="3353d-137">Get-AzStorageQueueStoredAccessPolicy</span></span>](./Get-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="3353d-138">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="3353d-138">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="3353d-139">Remove-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="3353d-139">Remove-AzStorageQueueStoredAccessPolicy</span></span>](./Remove-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="3353d-140">Set-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="3353d-140">Set-AzStorageQueueStoredAccessPolicy</span></span>](./Set-AzStorageQueueStoredAccessPolicy.md)



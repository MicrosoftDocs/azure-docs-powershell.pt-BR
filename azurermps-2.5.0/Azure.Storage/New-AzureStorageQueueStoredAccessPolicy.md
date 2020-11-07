---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 351145AC-7C1E-4EB7-A17D-B8B7D8ED8DAB
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragequeuestoredaccesspolicy
schema: 2.0.0
ms.openlocfilehash: 054a5d979a13f5592f062f729e4c8c393a35134a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93786010"
---
# <span data-ttu-id="c45f4-101">New-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="c45f4-101">New-AzureStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="c45f4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c45f4-102">SYNOPSIS</span></span>
<span data-ttu-id="c45f4-103">Cria uma política de acesso armazenado para uma fila de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="c45f4-103">Creates a stored access policy for an Azure storage queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c45f4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c45f4-104">SYNTAX</span></span>

```
New-AzureStorageQueueStoredAccessPolicy [-Queue] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c45f4-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c45f4-105">DESCRIPTION</span></span>
<span data-ttu-id="c45f4-106">O cmdlet **New-AzureStorageQueueStoredAccessPolicy** cria uma política de acesso armazenado para uma fila de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="c45f4-106">The **New-AzureStorageQueueStoredAccessPolicy** cmdlet creates a stored access policy for an Azure storage queue.</span></span>

## <span data-ttu-id="c45f4-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c45f4-107">EXAMPLES</span></span>

### <span data-ttu-id="c45f4-108">Exemplo 1: criar uma política de acesso armazenado em uma fila de armazenamento</span><span class="sxs-lookup"><span data-stu-id="c45f4-108">Example 1: Create a stored access policy in a storage queue</span></span>
```
PS C:\>New-AzureStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy01"
```

<span data-ttu-id="c45f4-109">Esse comando cria uma política de acesso chamada Policy01 na fila de armazenamento chamada MyQueue.</span><span class="sxs-lookup"><span data-stu-id="c45f4-109">This command creates an access policy named Policy01 in the storage queue named MyQueue.</span></span>

## <span data-ttu-id="c45f4-110">OS</span><span class="sxs-lookup"><span data-stu-id="c45f4-110">PARAMETERS</span></span>

### <span data-ttu-id="c45f4-111">-Contexto</span><span class="sxs-lookup"><span data-stu-id="c45f4-111">-Context</span></span>
<span data-ttu-id="c45f4-112">Especifica um contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="c45f4-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="c45f4-113">Para obter um contexto de armazenamento, use o cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="c45f4-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="c45f4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c45f4-114">-DefaultProfile</span></span>
<span data-ttu-id="c45f4-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c45f4-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c45f4-116">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="c45f4-116">-ExpiryTime</span></span>
<span data-ttu-id="c45f4-117">Especifica o tempo em que a política de acesso armazenado se torna inválida.</span><span class="sxs-lookup"><span data-stu-id="c45f4-117">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="c45f4-118">-Permissão</span><span class="sxs-lookup"><span data-stu-id="c45f4-118">-Permission</span></span>
<span data-ttu-id="c45f4-119">Especifica as permissões na política de acesso armazenado para acessar a fila de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="c45f4-119">Specifies permissions in the stored access policy to access the storage queue.</span></span>
<span data-ttu-id="c45f4-120">É importante observar que essa é uma cadeia de caracteres, como `rwd` (para ler, gravar e excluir).</span><span class="sxs-lookup"><span data-stu-id="c45f4-120">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="c45f4-121">-Política</span><span class="sxs-lookup"><span data-stu-id="c45f4-121">-Policy</span></span>
<span data-ttu-id="c45f4-122">Especifica um nome para a política de acesso armazenada.</span><span class="sxs-lookup"><span data-stu-id="c45f4-122">Specifies a name for the stored access policy.</span></span>

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

### <span data-ttu-id="c45f4-123">-Queue</span><span class="sxs-lookup"><span data-stu-id="c45f4-123">-Queue</span></span>
<span data-ttu-id="c45f4-124">Especifica o nome da fila de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="c45f4-124">Specifies the Azure storage queue name.</span></span>

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

### <span data-ttu-id="c45f4-125">-StartTime</span><span class="sxs-lookup"><span data-stu-id="c45f4-125">-StartTime</span></span>
<span data-ttu-id="c45f4-126">Especifica a hora em que a política de acesso armazenado se torna válida.</span><span class="sxs-lookup"><span data-stu-id="c45f4-126">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="c45f4-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c45f4-127">CommonParameters</span></span>
<span data-ttu-id="c45f4-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c45f4-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c45f4-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c45f4-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c45f4-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c45f4-130">INPUTS</span></span>

### <span data-ttu-id="c45f4-131">System. String</span><span class="sxs-lookup"><span data-stu-id="c45f4-131">System.String</span></span>

### <span data-ttu-id="c45f4-132">Microsoft. Azure. Commands. Common. Authentication. Abstractings. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="c45f4-132">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="c45f4-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c45f4-133">OUTPUTS</span></span>

### <span data-ttu-id="c45f4-134">System. String</span><span class="sxs-lookup"><span data-stu-id="c45f4-134">System.String</span></span>

## <span data-ttu-id="c45f4-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c45f4-135">NOTES</span></span>

## <span data-ttu-id="c45f4-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c45f4-136">RELATED LINKS</span></span>

[<span data-ttu-id="c45f4-137">Get-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="c45f4-137">Get-AzureStorageQueueStoredAccessPolicy</span></span>](./Get-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="c45f4-138">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="c45f4-138">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="c45f4-139">Remove-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="c45f4-139">Remove-AzureStorageQueueStoredAccessPolicy</span></span>](./Remove-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="c45f4-140">Set-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="c45f4-140">Set-AzureStorageQueueStoredAccessPolicy</span></span>](./Set-AzureStorageQueueStoredAccessPolicy.md)



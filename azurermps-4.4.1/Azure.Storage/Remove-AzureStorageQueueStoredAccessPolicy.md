---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 80DE5D60-93F8-4509-AA9C-F54E4AB70013
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageQueueStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageQueueStoredAccessPolicy.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: 94c5bc28ae381227366b5461b51a2da7fd6feccd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431259"
---
# <span data-ttu-id="96853-101">Remove-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="96853-101">Remove-AzureStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="96853-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="96853-102">SYNOPSIS</span></span>
<span data-ttu-id="96853-103">Remove uma política de acesso armazenado de uma fila de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="96853-103">Removes a stored access policy from an Azure storage queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="96853-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="96853-104">SYNTAX</span></span>

```
Remove-AzureStorageQueueStoredAccessPolicy [-Queue] <String> [-Policy] <String> [-PassThru]
 [-Context <IStorageContext>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="96853-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="96853-105">DESCRIPTION</span></span>
<span data-ttu-id="96853-106">O cmdlet **Remove-AzureStorageQueueStoredAccessPolicy** remove uma política de acesso armazenado de uma fila de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="96853-106">The **Remove-AzureStorageQueueStoredAccessPolicy** cmdlet removes a stored access policy from an Azure storage queue.</span></span>

## <span data-ttu-id="96853-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="96853-107">EXAMPLES</span></span>

### <span data-ttu-id="96853-108">Exemplo 1: remover uma política de acesso armazenado de uma fila de armazenamento</span><span class="sxs-lookup"><span data-stu-id="96853-108">Example 1: Remove a stored access policy from a storage queue</span></span>
```
PS C:\>Remove-AzureStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy04"
```

<span data-ttu-id="96853-109">Esse comando Remove uma política de acesso chamada Policy04 da fila de armazenamento chamada MyQueue.</span><span class="sxs-lookup"><span data-stu-id="96853-109">This command removes an access policy named Policy04 from the storage queue named MyQueue.</span></span>

## <span data-ttu-id="96853-110">OS</span><span class="sxs-lookup"><span data-stu-id="96853-110">PARAMETERS</span></span>

### <span data-ttu-id="96853-111">-Contexto</span><span class="sxs-lookup"><span data-stu-id="96853-111">-Context</span></span>
<span data-ttu-id="96853-112">Especifica um contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="96853-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="96853-113">Para obter um contexto de armazenamento, use o cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="96853-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="96853-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="96853-114">-PassThru</span></span>
<span data-ttu-id="96853-115">Indica que esse cmdlet retorna um **booliano** que reflete o sucesso da operação.</span><span class="sxs-lookup"><span data-stu-id="96853-115">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="96853-116">Por padrão, esse cmdlet não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="96853-116">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="96853-117">-Política</span><span class="sxs-lookup"><span data-stu-id="96853-117">-Policy</span></span>
<span data-ttu-id="96853-118">Especifica o nome da política de acesso armazenado que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="96853-118">Specifies the name of the stored access policy that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96853-119">-Queue</span><span class="sxs-lookup"><span data-stu-id="96853-119">-Queue</span></span>
<span data-ttu-id="96853-120">Especifica o nome da fila de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="96853-120">Specifies the Azure storage queue name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96853-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="96853-121">-Confirm</span></span>
<span data-ttu-id="96853-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="96853-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96853-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="96853-123">-WhatIf</span></span>
<span data-ttu-id="96853-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="96853-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="96853-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="96853-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96853-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96853-126">CommonParameters</span></span>
<span data-ttu-id="96853-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96853-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96853-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="96853-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96853-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="96853-129">INPUTS</span></span>

### <span data-ttu-id="96853-130">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="96853-130">IStorageContext</span></span>

<span data-ttu-id="96853-131">O parâmetro ' Context ' aceita o valor do tipo ' IStorageContext ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="96853-131">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="96853-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="96853-132">OUTPUTS</span></span>

### <span data-ttu-id="96853-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="96853-133">System.Boolean</span></span>

## <span data-ttu-id="96853-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="96853-134">NOTES</span></span>

## <span data-ttu-id="96853-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="96853-135">RELATED LINKS</span></span>

[<span data-ttu-id="96853-136">Get-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="96853-136">Get-AzureStorageQueueStoredAccessPolicy</span></span>](./Get-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="96853-137">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="96853-137">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="96853-138">New-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="96853-138">New-AzureStorageQueueStoredAccessPolicy</span></span>](./New-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="96853-139">Set-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="96853-139">Set-AzureStorageQueueStoredAccessPolicy</span></span>](./Set-AzureStorageQueueStoredAccessPolicy.md)

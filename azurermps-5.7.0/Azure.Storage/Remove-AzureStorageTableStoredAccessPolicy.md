---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 30CC0D80-505A-4988-B4EC-3B7BC5B76F5D
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/remove-azurestoragetablestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageTableStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageTableStoredAccessPolicy.md
ms.openlocfilehash: a9e1290c5933d54481c57b051e170568653eee5a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432150"
---
# <span data-ttu-id="f7954-101">Remove-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="f7954-101">Remove-AzureStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="f7954-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f7954-102">SYNOPSIS</span></span>
<span data-ttu-id="f7954-103">Remove uma política de acesso armazenado de uma tabela de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="f7954-103">Removes a stored access policy from an Azure storage table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f7954-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f7954-104">SYNTAX</span></span>

```
Remove-AzureStorageTableStoredAccessPolicy [-Table] <String> [-Policy] <String> [-PassThru]
 [-Context <IStorageContext>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f7954-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f7954-105">DESCRIPTION</span></span>
<span data-ttu-id="f7954-106">O cmdlet **Remove-AzureStorageTableStoredAccessPolicy** remove uma política de acesso armazenado de uma tabela de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="f7954-106">The **Remove-AzureStorageTableStoredAccessPolicy** cmdlet removes a stored access policy from an Azure storage table.</span></span>

## <span data-ttu-id="f7954-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f7954-107">EXAMPLES</span></span>

### <span data-ttu-id="f7954-108">Exemplo 1: remover uma política de acesso armazenado de uma tabela de armazenamento</span><span class="sxs-lookup"><span data-stu-id="f7954-108">Example 1: Remove a stored access policy from a storage table</span></span>
```
PS C:\>Remove-AzureStorageTableStoredAccessPolicy -Table "MyTable" -Policy "Policy05"
```

<span data-ttu-id="f7954-109">Esse comando Remove a política denominada Policy05 da tabela de armazenamento chamada MyTable.</span><span class="sxs-lookup"><span data-stu-id="f7954-109">This command removes policy named Policy05 from storage table named MyTable.</span></span>

## <span data-ttu-id="f7954-110">OS</span><span class="sxs-lookup"><span data-stu-id="f7954-110">PARAMETERS</span></span>

### <span data-ttu-id="f7954-111">-Contexto</span><span class="sxs-lookup"><span data-stu-id="f7954-111">-Context</span></span>
<span data-ttu-id="f7954-112">Especifica um contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="f7954-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="f7954-113">Para obter um contexto de armazenamento, use o cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="f7954-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="f7954-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f7954-114">-PassThru</span></span>
<span data-ttu-id="f7954-115">Indica que esse cmdlet retorna um **booliano** que reflete o sucesso da operação.</span><span class="sxs-lookup"><span data-stu-id="f7954-115">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="f7954-116">Por padrão, esse cmdlet não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="f7954-116">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="f7954-117">-Política</span><span class="sxs-lookup"><span data-stu-id="f7954-117">-Policy</span></span>
<span data-ttu-id="f7954-118">Especifica o nome da política de acesso armazenado que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="f7954-118">Specifies the name of the stored access policy that this cmdlet removes.</span></span>

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

### <span data-ttu-id="f7954-119">-Tabela</span><span class="sxs-lookup"><span data-stu-id="f7954-119">-Table</span></span>
<span data-ttu-id="f7954-120">Especifica o nome da tabela do Azure.</span><span class="sxs-lookup"><span data-stu-id="f7954-120">Specifies the Azure table name.</span></span>

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

### <span data-ttu-id="f7954-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f7954-121">-Confirm</span></span>
<span data-ttu-id="f7954-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f7954-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f7954-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7954-123">-WhatIf</span></span>
<span data-ttu-id="f7954-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f7954-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f7954-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f7954-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f7954-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7954-126">CommonParameters</span></span>
<span data-ttu-id="f7954-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7954-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7954-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f7954-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7954-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f7954-129">INPUTS</span></span>

### <span data-ttu-id="f7954-130">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="f7954-130">IStorageContext</span></span>

<span data-ttu-id="f7954-131">O parâmetro ' Context ' aceita o valor do tipo ' IStorageContext ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="f7954-131">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="f7954-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f7954-132">OUTPUTS</span></span>

### <span data-ttu-id="f7954-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f7954-133">System.Boolean</span></span>

## <span data-ttu-id="f7954-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f7954-134">NOTES</span></span>

## <span data-ttu-id="f7954-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f7954-135">RELATED LINKS</span></span>

[<span data-ttu-id="f7954-136">Get-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="f7954-136">Get-AzureStorageTableStoredAccessPolicy</span></span>](./Get-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="f7954-137">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="f7954-137">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="f7954-138">New-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="f7954-138">New-AzureStorageTableStoredAccessPolicy</span></span>](./New-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="f7954-139">Set-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="f7954-139">Set-AzureStorageTableStoredAccessPolicy</span></span>](./Set-AzureStorageTableStoredAccessPolicy.md)

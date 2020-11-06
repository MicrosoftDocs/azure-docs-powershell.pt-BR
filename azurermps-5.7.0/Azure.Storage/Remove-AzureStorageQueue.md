---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 22975A89-CAFF-4F18-8DCE-B695413FBAC7
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/remove-azurestoragequeue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageQueue.md
ms.openlocfilehash: b98b0ef6e8c4d47c32cab4ee891041e0820ea3ca
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93603300"
---
# <span data-ttu-id="248a1-101">Remove-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="248a1-101">Remove-AzureStorageQueue</span></span>

## <span data-ttu-id="248a1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="248a1-102">SYNOPSIS</span></span>
<span data-ttu-id="248a1-103">Remove uma fila de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="248a1-103">Removes a storage queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="248a1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="248a1-104">SYNTAX</span></span>

```
Remove-AzureStorageQueue [-Name] <String> [-Force] [-PassThru] [-Context <IStorageContext>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="248a1-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="248a1-105">DESCRIPTION</span></span>
<span data-ttu-id="248a1-106">O cmdlet **Remove-AzureStorageQueue** remove uma fila de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="248a1-106">The **Remove-AzureStorageQueue** cmdlet removes a storage queue.</span></span>

## <span data-ttu-id="248a1-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="248a1-107">EXAMPLES</span></span>

### <span data-ttu-id="248a1-108">Exemplo 1: remover uma fila de armazenamento por nome</span><span class="sxs-lookup"><span data-stu-id="248a1-108">Example 1: Remove a storage queue by name</span></span>
```
PS C:\>Remove-AzureStorageQueue "ContosoQueue01"
```

<span data-ttu-id="248a1-109">Esse comando Remove uma fila chamada ContosoQueue01.</span><span class="sxs-lookup"><span data-stu-id="248a1-109">This command removes a queue named ContosoQueue01.</span></span>

### <span data-ttu-id="248a1-110">Exemplo 2: remover várias filas de armazenamento</span><span class="sxs-lookup"><span data-stu-id="248a1-110">Example 2: Remove multiple storage queues</span></span>
```
PS C:\>Get-AzureStorageQueue "Contoso*" | Remove-AzureStorageQueue
```

<span data-ttu-id="248a1-111">Esse comando Remove todas as filas com nomes que começam com contoso.</span><span class="sxs-lookup"><span data-stu-id="248a1-111">This command removes all queues with names that start with Contoso.</span></span>

## <span data-ttu-id="248a1-112">OS</span><span class="sxs-lookup"><span data-stu-id="248a1-112">PARAMETERS</span></span>

### <span data-ttu-id="248a1-113">-Contexto</span><span class="sxs-lookup"><span data-stu-id="248a1-113">-Context</span></span>
<span data-ttu-id="248a1-114">Especifica o contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="248a1-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="248a1-115">Para obter o contexto de armazenamento, o cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="248a1-115">To obtain the storage context, the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="248a1-116">-Force</span><span class="sxs-lookup"><span data-stu-id="248a1-116">-Force</span></span>
<span data-ttu-id="248a1-117">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="248a1-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="248a1-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="248a1-118">-Name</span></span>
<span data-ttu-id="248a1-119">Especifica o nome da fila a ser removida.</span><span class="sxs-lookup"><span data-stu-id="248a1-119">Specifies the name of the queue to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Queue

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="248a1-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="248a1-120">-PassThru</span></span>
<span data-ttu-id="248a1-121">Indica que esse cmdlet retorna um **booliano** que reflete o sucesso da operação.</span><span class="sxs-lookup"><span data-stu-id="248a1-121">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="248a1-122">Por padrão, esse cmdlet não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="248a1-122">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="248a1-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="248a1-123">-Confirm</span></span>
<span data-ttu-id="248a1-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="248a1-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="248a1-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="248a1-125">-WhatIf</span></span>
<span data-ttu-id="248a1-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="248a1-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="248a1-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="248a1-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="248a1-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="248a1-128">CommonParameters</span></span>
<span data-ttu-id="248a1-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="248a1-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="248a1-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="248a1-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="248a1-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="248a1-131">INPUTS</span></span>

### <span data-ttu-id="248a1-132">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="248a1-132">IStorageContext</span></span>

<span data-ttu-id="248a1-133">O parâmetro ' Context ' aceita o valor do tipo ' IStorageContext ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="248a1-133">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="248a1-134">String</span><span class="sxs-lookup"><span data-stu-id="248a1-134">String</span></span>

<span data-ttu-id="248a1-135">O parâmetro ' name ' aceita o valor do tipo ' String ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="248a1-135">Parameter 'Name' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="248a1-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="248a1-136">OUTPUTS</span></span>

### <span data-ttu-id="248a1-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="248a1-137">System.Boolean</span></span>

## <span data-ttu-id="248a1-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="248a1-138">NOTES</span></span>

## <span data-ttu-id="248a1-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="248a1-139">RELATED LINKS</span></span>

[<span data-ttu-id="248a1-140">Get-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="248a1-140">Get-AzureStorageQueue</span></span>](./Get-AzureStorageQueue.md)

[<span data-ttu-id="248a1-141">New-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="248a1-141">New-AzureStorageQueue</span></span>](./New-AzureStorageQueue.md)

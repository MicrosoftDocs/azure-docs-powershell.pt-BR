---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 1B29AB8C-95DD-4C4F-86E2-2F81E8020CEA
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/remove-azurestoragetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageTable.md
ms.openlocfilehash: 7423cbb6995430523beb137ef10eb6f1a53c959c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93603069"
---
# <span data-ttu-id="e6644-101">Remove-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="e6644-101">Remove-AzureStorageTable</span></span>

## <span data-ttu-id="e6644-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e6644-102">SYNOPSIS</span></span>
<span data-ttu-id="e6644-103">Remove uma tabela de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="e6644-103">Removes a storage table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e6644-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e6644-104">SYNTAX</span></span>

```
Remove-AzureStorageTable [-Name] <String> [-Force] [-PassThru] [-Context <IStorageContext>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e6644-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e6644-105">DESCRIPTION</span></span>
<span data-ttu-id="e6644-106">O cmdlet **Remove-AzureStorageTable** remove uma ou mais tabelas de armazenamento de uma conta de armazenamento no Azure.</span><span class="sxs-lookup"><span data-stu-id="e6644-106">The **Remove-AzureStorageTable** cmdlet removes one or more storage tables from a storage account in Azure.</span></span>

## <span data-ttu-id="e6644-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e6644-107">EXAMPLES</span></span>

### <span data-ttu-id="e6644-108">Exemplo 1: remover uma tabela</span><span class="sxs-lookup"><span data-stu-id="e6644-108">Example 1: Remove a table</span></span>
```
PS C:\>Remove-AzureStorageTable -Name "TableABC"
```

<span data-ttu-id="e6644-109">Esse comando Remove uma tabela.</span><span class="sxs-lookup"><span data-stu-id="e6644-109">This command removes a table.</span></span>

### <span data-ttu-id="e6644-110">Exemplo 2: remover várias tabelas</span><span class="sxs-lookup"><span data-stu-id="e6644-110">Example 2: Remove several tables</span></span>
```
PS C:\>Get-AzureStorageTable table* | Remove-AzureStorageTable
```

<span data-ttu-id="e6644-111">Este exemplo usa um caractere curinga com o parâmetro *Name* para obter todas as tabelas correspondentes à tabela padrão e, em seguida, passa o resultado no pipeline para remover as tabelas.</span><span class="sxs-lookup"><span data-stu-id="e6644-111">This example uses a wildcard character with the *Name* parameter to get all tables that match the pattern table and then passes the result on the pipeline to remove the tables.</span></span>

## <span data-ttu-id="e6644-112">OS</span><span class="sxs-lookup"><span data-stu-id="e6644-112">PARAMETERS</span></span>

### <span data-ttu-id="e6644-113">-Contexto</span><span class="sxs-lookup"><span data-stu-id="e6644-113">-Context</span></span>
<span data-ttu-id="e6644-114">Especifica o contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="e6644-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="e6644-115">Você pode criá-lo usando o cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="e6644-115">You can create it by using the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="e6644-116">-Force</span><span class="sxs-lookup"><span data-stu-id="e6644-116">-Force</span></span>
<span data-ttu-id="e6644-117">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="e6644-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e6644-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="e6644-118">-Name</span></span>
<span data-ttu-id="e6644-119">Especifica o nome da tabela a ser removida.</span><span class="sxs-lookup"><span data-stu-id="e6644-119">Specifies the name of the table to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Table

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e6644-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e6644-120">-PassThru</span></span>
<span data-ttu-id="e6644-121">Indica que esse cmdlet retorna um **booliano** que reflete o sucesso da operação.</span><span class="sxs-lookup"><span data-stu-id="e6644-121">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="e6644-122">Por padrão, esse cmdlet não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="e6644-122">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="e6644-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e6644-123">-Confirm</span></span>
<span data-ttu-id="e6644-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e6644-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e6644-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e6644-125">-WhatIf</span></span>
<span data-ttu-id="e6644-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e6644-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e6644-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e6644-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e6644-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6644-128">CommonParameters</span></span>
<span data-ttu-id="e6644-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6644-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6644-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e6644-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6644-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e6644-131">INPUTS</span></span>

### <span data-ttu-id="e6644-132">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="e6644-132">IStorageContext</span></span>

<span data-ttu-id="e6644-133">O parâmetro ' Context ' aceita o valor do tipo ' IStorageContext ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="e6644-133">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="e6644-134">String</span><span class="sxs-lookup"><span data-stu-id="e6644-134">String</span></span>

<span data-ttu-id="e6644-135">O parâmetro ' name ' aceita o valor do tipo ' String ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="e6644-135">Parameter 'Name' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="e6644-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e6644-136">OUTPUTS</span></span>

### <span data-ttu-id="e6644-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e6644-137">System.Boolean</span></span>

## <span data-ttu-id="e6644-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e6644-138">NOTES</span></span>

## <span data-ttu-id="e6644-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e6644-139">RELATED LINKS</span></span>

[<span data-ttu-id="e6644-140">Get-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="e6644-140">Get-AzureStorageTable</span></span>](./Get-AzureStorageTable.md)

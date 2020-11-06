---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 1B29AB8C-95DD-4C4F-86E2-2F81E8020CEA
online version: ''
schema: 2.0.0
ms.openlocfilehash: fcb08eb9e63917d072630f81a2026d961a70dd27
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93601712"
---
# <span data-ttu-id="bb862-101">Remove-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="bb862-101">Remove-AzureStorageTable</span></span>

## <span data-ttu-id="bb862-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bb862-102">SYNOPSIS</span></span>
<span data-ttu-id="bb862-103">Remove uma tabela de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="bb862-103">Removes a storage table.</span></span>

## <span data-ttu-id="bb862-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bb862-104">SYNTAX</span></span>

```
Remove-AzureStorageTable [-Name] <String> [-Force] [-PassThru] [-Context <IStorageContext>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bb862-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="bb862-105">DESCRIPTION</span></span>
<span data-ttu-id="bb862-106">O cmdlet **Remove-AzureStorageTable** remove uma ou mais tabelas de armazenamento de uma conta de armazenamento no Azure.</span><span class="sxs-lookup"><span data-stu-id="bb862-106">The **Remove-AzureStorageTable** cmdlet removes one or more storage tables from a storage account in Azure.</span></span>

## <span data-ttu-id="bb862-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bb862-107">EXAMPLES</span></span>

### <span data-ttu-id="bb862-108">Exemplo 1: remover uma tabela</span><span class="sxs-lookup"><span data-stu-id="bb862-108">Example 1: Remove a table</span></span>
```
PS C:\>Remove-AzureStorageTable -Name "TableABC"
```

<span data-ttu-id="bb862-109">Esse comando Remove uma tabela.</span><span class="sxs-lookup"><span data-stu-id="bb862-109">This command removes a table.</span></span>

### <span data-ttu-id="bb862-110">Exemplo 2: remover várias tabelas</span><span class="sxs-lookup"><span data-stu-id="bb862-110">Example 2: Remove several tables</span></span>
```
PS C:\>Get-AzureStorageTable table* | Remove-AzureStorageTable
```

<span data-ttu-id="bb862-111">Este exemplo usa um caractere curinga com o parâmetro *Name* para obter todas as tabelas correspondentes à tabela padrão e, em seguida, passa o resultado no pipeline para remover as tabelas.</span><span class="sxs-lookup"><span data-stu-id="bb862-111">This example uses a wildcard character with the *Name* parameter to get all tables that match the pattern table and then passes the result on the pipeline to remove the tables.</span></span>

## <span data-ttu-id="bb862-112">OS</span><span class="sxs-lookup"><span data-stu-id="bb862-112">PARAMETERS</span></span>

### <span data-ttu-id="bb862-113">-Contexto</span><span class="sxs-lookup"><span data-stu-id="bb862-113">-Context</span></span>
<span data-ttu-id="bb862-114">Especifica o contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="bb862-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="bb862-115">Você pode criá-lo usando o cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="bb862-115">You can create it by using the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="bb862-116">-Force</span><span class="sxs-lookup"><span data-stu-id="bb862-116">-Force</span></span>
<span data-ttu-id="bb862-117">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="bb862-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="bb862-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="bb862-118">-Name</span></span>
<span data-ttu-id="bb862-119">Especifica o nome da tabela a ser removida.</span><span class="sxs-lookup"><span data-stu-id="bb862-119">Specifies the name of the table to remove.</span></span>

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

### <span data-ttu-id="bb862-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bb862-120">-PassThru</span></span>
<span data-ttu-id="bb862-121">Indica que esse cmdlet retorna um **booliano** que reflete o sucesso da operação.</span><span class="sxs-lookup"><span data-stu-id="bb862-121">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="bb862-122">Por padrão, esse cmdlet não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="bb862-122">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="bb862-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="bb862-123">-Confirm</span></span>
<span data-ttu-id="bb862-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bb862-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bb862-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bb862-125">-WhatIf</span></span>
<span data-ttu-id="bb862-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="bb862-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bb862-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="bb862-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bb862-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb862-128">CommonParameters</span></span>
<span data-ttu-id="bb862-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb862-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb862-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb862-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb862-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="bb862-131">INPUTS</span></span>

## <span data-ttu-id="bb862-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="bb862-132">OUTPUTS</span></span>

## <span data-ttu-id="bb862-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="bb862-133">NOTES</span></span>

## <span data-ttu-id="bb862-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bb862-134">RELATED LINKS</span></span>

[<span data-ttu-id="bb862-135">Get-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="bb862-135">Get-AzureStorageTable</span></span>](./Get-AzureStorageTable.md)

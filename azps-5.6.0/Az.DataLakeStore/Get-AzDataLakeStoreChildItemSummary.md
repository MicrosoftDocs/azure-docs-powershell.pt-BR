---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/get-azdatalakestorechilditemsummary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreChildItemSummary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreChildItemSummary.md
ms.openlocfilehash: d83e07e207c2b0e3a03c745abc874814378e5ee4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886047"
---
# <span data-ttu-id="7d0a6-101">Get-AzDataLakeStoreChildItemSummary</span><span class="sxs-lookup"><span data-stu-id="7d0a6-101">Get-AzDataLakeStoreChildItemSummary</span></span>

## <span data-ttu-id="7d0a6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7d0a6-102">SYNOPSIS</span></span>
<span data-ttu-id="7d0a6-103">Obtém o resumo do tamanho total, arquivos e diretórios contidos no caminho especificado</span><span class="sxs-lookup"><span data-stu-id="7d0a6-103">Gets the summary of total size, files and directories contained in the path specified</span></span>

## <span data-ttu-id="7d0a6-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="7d0a6-104">SYNTAX</span></span>

```
Get-AzDataLakeStoreChildItemSummary [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Concurrency <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7d0a6-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="7d0a6-105">DESCRIPTION</span></span>
<span data-ttu-id="7d0a6-106">**Get-AzDataLakeStoreChildItemSummary** recupera o resumo de conteúdo de um determinado caminho.</span><span class="sxs-lookup"><span data-stu-id="7d0a6-106">The **Get-AzDataLakeStoreChildItemSummary** retrieves the content summary for a given path.</span></span> <span data-ttu-id="7d0a6-107">Ele calcula recursivamente o número total de arquivos, diretórios e tamanho total de todos os arquivos sob o caminho determinado.</span><span class="sxs-lookup"><span data-stu-id="7d0a6-107">It recursively computes total number of files, directories and total size of all the files under the given path.</span></span>

## <span data-ttu-id="7d0a6-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7d0a6-108">EXAMPLES</span></span>

### <span data-ttu-id="7d0a6-109">Exemplo 1: Obter o resumo de conteúdo de uma pasta</span><span class="sxs-lookup"><span data-stu-id="7d0a6-109">Example 1: Get the content summary of a folder</span></span>
```
PS C:\> Get-AzDataLakeStoreChildItemSummary -Account ContosoADL -Path /a -Concurrency 128
```

<span data-ttu-id="7d0a6-110">Ele lista o número total de diretórios, arquivos e seu tamanho contidos em /a.</span><span class="sxs-lookup"><span data-stu-id="7d0a6-110">It lists number of total directories, files and their size contained under /a.</span></span>

## <span data-ttu-id="7d0a6-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="7d0a6-111">PARAMETERS</span></span>

### <span data-ttu-id="7d0a6-112">-Account</span><span class="sxs-lookup"><span data-stu-id="7d0a6-112">-Account</span></span>
<span data-ttu-id="7d0a6-113">A conta do Data Lake Store para executar a operação do sistema de arquivos em</span><span class="sxs-lookup"><span data-stu-id="7d0a6-113">The Data Lake Store account to execute the filesystem operation in</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d0a6-114">-Concurrency</span><span class="sxs-lookup"><span data-stu-id="7d0a6-114">-Concurrency</span></span>
<span data-ttu-id="7d0a6-115">Indica o número de arquivos/diretórios processados em paralelo.</span><span class="sxs-lookup"><span data-stu-id="7d0a6-115">Indicates the number of files/directories processed in parallel.</span></span>
<span data-ttu-id="7d0a6-116">O padrão será calculado como um melhor esforço com base na especificação do sistema.</span><span class="sxs-lookup"><span data-stu-id="7d0a6-116">Default will be computed as a best effort based on system specification.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d0a6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d0a6-117">-DefaultProfile</span></span>
<span data-ttu-id="7d0a6-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7d0a6-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d0a6-119">-Path</span><span class="sxs-lookup"><span data-stu-id="7d0a6-119">-Path</span></span>
<span data-ttu-id="7d0a6-120">O caminho na conta do Data Lake especificada que deve ser recuperado.</span><span class="sxs-lookup"><span data-stu-id="7d0a6-120">The path in the specified Data Lake account that should be retrieve.</span></span>
<span data-ttu-id="7d0a6-121">Pode ser um arquivo ou pasta No formato '/folder/file.txt', onde o primeiro '/' após o DNS indica a raiz do sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="7d0a6-121">Can be a file or folder In the format '/folder/file.txt', where the first '/' after the DNS indicates the root of the file system.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d0a6-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7d0a6-122">-Confirm</span></span>
<span data-ttu-id="7d0a6-123">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7d0a6-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d0a6-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7d0a6-124">-WhatIf</span></span>
<span data-ttu-id="7d0a6-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7d0a6-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7d0a6-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7d0a6-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d0a6-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d0a6-127">CommonParameters</span></span>
<span data-ttu-id="7d0a6-128">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d0a6-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d0a6-129">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d0a6-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d0a6-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7d0a6-130">INPUTS</span></span>

### <span data-ttu-id="7d0a6-131">System.String</span><span class="sxs-lookup"><span data-stu-id="7d0a6-131">System.String</span></span>

### <span data-ttu-id="7d0a6-132">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="7d0a6-132">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="7d0a6-133">System.Int32</span><span class="sxs-lookup"><span data-stu-id="7d0a6-133">System.Int32</span></span>

## <span data-ttu-id="7d0a6-134">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="7d0a6-134">OUTPUTS</span></span>

### <span data-ttu-id="7d0a6-135">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreChildItemSummary</span><span class="sxs-lookup"><span data-stu-id="7d0a6-135">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreChildItemSummary</span></span>

## <span data-ttu-id="7d0a6-136">NOTES</span><span class="sxs-lookup"><span data-stu-id="7d0a6-136">NOTES</span></span>

## <span data-ttu-id="7d0a6-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7d0a6-137">RELATED LINKS</span></span>

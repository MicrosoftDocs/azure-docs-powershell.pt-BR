---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/get-azureatalakestorechilditemsummary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreChildItemSummary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreChildItemSummary.md
ms.openlocfilehash: 83fb8b3ea5fdf9ad63983d2a3a3d23d402fbb5a0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440062"
---
# <span data-ttu-id="d0903-101">Get-AzureRmDataLakeStoreChildItemSummary</span><span class="sxs-lookup"><span data-stu-id="d0903-101">Get-AzureRmDataLakeStoreChildItemSummary</span></span>

## <span data-ttu-id="d0903-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d0903-102">SYNOPSIS</span></span>
<span data-ttu-id="d0903-103">Obtém o resumo do tamanho total, dos arquivos e das pastas contidos no caminho especificado</span><span class="sxs-lookup"><span data-stu-id="d0903-103">Gets the summary of total size, files and directories contained in the path specified</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d0903-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d0903-104">SYNTAX</span></span>

```
Get-AzureRmDataLakeStoreChildItemSummary [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Concurrency <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d0903-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d0903-105">DESCRIPTION</span></span>
<span data-ttu-id="d0903-106">**Get-AzureRmDataLakeStoreChildItemSummary** recupera o resumo de conteúdo para um determinado caminho.</span><span class="sxs-lookup"><span data-stu-id="d0903-106">The **Get-AzureRmDataLakeStoreChildItemSummary** retrieves the content summary for a given path.</span></span> <span data-ttu-id="d0903-107">Calcula recursivamente o número total de arquivos, diretórios e tamanho total de todos os arquivos sob o caminho fornecido.</span><span class="sxs-lookup"><span data-stu-id="d0903-107">It recursively computes total number of files, directories and total size of all the files under the given path.</span></span>

## <span data-ttu-id="d0903-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d0903-108">EXAMPLES</span></span>

### <span data-ttu-id="d0903-109">Exemplo 1: obter o resumo de conteúdo de uma pasta</span><span class="sxs-lookup"><span data-stu-id="d0903-109">Example 1: Get the content summary of a folder</span></span>
```
PS C:\> Get-AzureRmDataLakeStoreChildItemSummary -Account ContosoADL -Path /a -Concurrency 128
```

<span data-ttu-id="d0903-110">Ele lista o número de diretórios, arquivos e o tamanho total contidos em/a.</span><span class="sxs-lookup"><span data-stu-id="d0903-110">It lists number of total directories, files and their size contained under /a.</span></span>

## <span data-ttu-id="d0903-111">OS</span><span class="sxs-lookup"><span data-stu-id="d0903-111">PARAMETERS</span></span>

### <span data-ttu-id="d0903-112">-Conta</span><span class="sxs-lookup"><span data-stu-id="d0903-112">-Account</span></span>
<span data-ttu-id="d0903-113">A conta do data Lake Store para executar a operação do sistema de arquivos no</span><span class="sxs-lookup"><span data-stu-id="d0903-113">The Data Lake Store account to execute the filesystem operation in</span></span>

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

### <span data-ttu-id="d0903-114">-Simultaneidade</span><span class="sxs-lookup"><span data-stu-id="d0903-114">-Concurrency</span></span>
<span data-ttu-id="d0903-115">Indica o número de arquivos/pastas processados em paralelo.</span><span class="sxs-lookup"><span data-stu-id="d0903-115">Indicates the number of files/directories processed in parallel.</span></span>
<span data-ttu-id="d0903-116">O padrão será calculado como um melhor esforço com base na especificação do sistema.</span><span class="sxs-lookup"><span data-stu-id="d0903-116">Default will be computed as a best effort based on system specification.</span></span>

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

### <span data-ttu-id="d0903-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0903-117">-DefaultProfile</span></span>
<span data-ttu-id="d0903-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d0903-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d0903-119">-Caminho</span><span class="sxs-lookup"><span data-stu-id="d0903-119">-Path</span></span>
<span data-ttu-id="d0903-120">O caminho na conta data Lake especificada que deve ser recuperada.</span><span class="sxs-lookup"><span data-stu-id="d0903-120">The path in the specified Data Lake account that should be retrieve.</span></span>
<span data-ttu-id="d0903-121">Pode ser um arquivo ou uma pasta no formato '/Folder/file.txt ', em que o primeiro '/' após o DNS indica a raiz do sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="d0903-121">Can be a file or folder In the format '/folder/file.txt', where the first '/' after the DNS indicates the root of the file system.</span></span>

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

### <span data-ttu-id="d0903-122">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d0903-122">-Confirm</span></span>
<span data-ttu-id="d0903-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d0903-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d0903-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d0903-124">-WhatIf</span></span>
<span data-ttu-id="d0903-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d0903-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d0903-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d0903-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d0903-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0903-127">CommonParameters</span></span>
<span data-ttu-id="d0903-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0903-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0903-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d0903-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0903-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d0903-130">INPUTS</span></span>

### <span data-ttu-id="d0903-131">System. String</span><span class="sxs-lookup"><span data-stu-id="d0903-131">System.String</span></span>

### <span data-ttu-id="d0903-132">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="d0903-132">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="d0903-133">System. Int32</span><span class="sxs-lookup"><span data-stu-id="d0903-133">System.Int32</span></span>

## <span data-ttu-id="d0903-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d0903-134">OUTPUTS</span></span>

### <span data-ttu-id="d0903-135">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreChildItemSummary</span><span class="sxs-lookup"><span data-stu-id="d0903-135">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreChildItemSummary</span></span>

## <span data-ttu-id="d0903-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d0903-136">NOTES</span></span>

## <span data-ttu-id="d0903-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d0903-137">RELATED LINKS</span></span>
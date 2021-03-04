---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: ECA70C6C-E0B0-445D-BCAD-041625FAC632
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/get-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItem.md
ms.openlocfilehash: 3a39e2f341404ac3f6dbb75c27408dd9d9ee2d47
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892796"
---
# <span data-ttu-id="ae040-101">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="ae040-101">Get-AzDataLakeStoreItem</span></span>

## <span data-ttu-id="ae040-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ae040-102">SYNOPSIS</span></span>
<span data-ttu-id="ae040-103">Obtém os detalhes de um arquivo ou pasta no Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="ae040-103">Gets the details of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="ae040-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="ae040-104">SYNTAX</span></span>

```
Get-AzDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ae040-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="ae040-105">DESCRIPTION</span></span>
<span data-ttu-id="ae040-106">O cmdlet **Get-AzDataLakeStoreItem** obtém os detalhes de um arquivo ou pasta no Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="ae040-106">The **Get-AzDataLakeStoreItem** cmdlet gets the details of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="ae040-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ae040-107">EXAMPLES</span></span>

### <span data-ttu-id="ae040-108">Exemplo 1: Obter detalhes de um arquivo do Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="ae040-108">Example 1: Get details of a file from the Data Lake Store</span></span>
```
PS C:\>Get-AzDataLakeStoreItem -AccountName "ContosoADL" -Path "/MyFiles/Test.csv"
```

<span data-ttu-id="ae040-109">Este comando obtém os detalhes do arquivo Test.csv do Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="ae040-109">This command gets the details of the file Test.csv from the Data Lake Store.</span></span>

## <span data-ttu-id="ae040-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="ae040-110">PARAMETERS</span></span>

### <span data-ttu-id="ae040-111">-Account</span><span class="sxs-lookup"><span data-stu-id="ae040-111">-Account</span></span>
<span data-ttu-id="ae040-112">Especifica o nome da conta do Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="ae040-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="ae040-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae040-113">-DefaultProfile</span></span>
<span data-ttu-id="ae040-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="ae040-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ae040-115">-Path</span><span class="sxs-lookup"><span data-stu-id="ae040-115">-Path</span></span>
<span data-ttu-id="ae040-116">Especifica o caminho do Data Lake Store a partir do qual obter detalhes de um item, começando com o diretório raiz (/).</span><span class="sxs-lookup"><span data-stu-id="ae040-116">Specifies the Data Lake Store path from which to get details of an item, starting with the root directory (/).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae040-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae040-117">CommonParameters</span></span>
<span data-ttu-id="ae040-118">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae040-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae040-119">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae040-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae040-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ae040-120">INPUTS</span></span>

### <span data-ttu-id="ae040-121">System.String</span><span class="sxs-lookup"><span data-stu-id="ae040-121">System.String</span></span>

### <span data-ttu-id="ae040-122">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="ae040-122">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

## <span data-ttu-id="ae040-123">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="ae040-123">OUTPUTS</span></span>

### <span data-ttu-id="ae040-124">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="ae040-124">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItem</span></span>

## <span data-ttu-id="ae040-125">NOTES</span><span class="sxs-lookup"><span data-stu-id="ae040-125">NOTES</span></span>

## <span data-ttu-id="ae040-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ae040-126">RELATED LINKS</span></span>

[<span data-ttu-id="ae040-127">Export-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="ae040-127">Export-AzDataLakeStoreItem</span></span>](./Export-AzDataLakeStoreItem.md)

[<span data-ttu-id="ae040-128">Get-AzDataLakeStoreChildItem</span><span class="sxs-lookup"><span data-stu-id="ae040-128">Get-AzDataLakeStoreChildItem</span></span>](./Get-AzDataLakeStoreChildItem.md)

[<span data-ttu-id="ae040-129">Import-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="ae040-129">Import-AzDataLakeStoreItem</span></span>](./Import-AzDataLakeStoreItem.md)

[<span data-ttu-id="ae040-130">Join-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="ae040-130">Join-AzDataLakeStoreItem</span></span>](./Join-AzDataLakeStoreItem.md)

[<span data-ttu-id="ae040-131">Move-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="ae040-131">Move-AzDataLakeStoreItem</span></span>](./Move-AzDataLakeStoreItem.md)

[<span data-ttu-id="ae040-132">New-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="ae040-132">New-AzDataLakeStoreItem</span></span>](./New-AzDataLakeStoreItem.md)

[<span data-ttu-id="ae040-133">Remove-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="ae040-133">Remove-AzDataLakeStoreItem</span></span>](./Remove-AzDataLakeStoreItem.md)

[<span data-ttu-id="ae040-134">Test-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="ae040-134">Test-AzDataLakeStoreItem</span></span>](./Test-AzDataLakeStoreItem.md)



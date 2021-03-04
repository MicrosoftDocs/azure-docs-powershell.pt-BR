---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: CC0E73BD-2063-4CA2-BBBA-1FB6AE04DADE
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/get-azdatalakestorechilditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreChildItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreChildItem.md
ms.openlocfilehash: e27fde6a25fc512b898ded7d4f087ab7b344d293
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886048"
---
# <span data-ttu-id="92294-101">Get-AzDataLakeStoreChildItem</span><span class="sxs-lookup"><span data-stu-id="92294-101">Get-AzDataLakeStoreChildItem</span></span>

## <span data-ttu-id="92294-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="92294-102">SYNOPSIS</span></span>
<span data-ttu-id="92294-103">Obtém a lista de itens em uma pasta no Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="92294-103">Gets the list of items in a folder in Data Lake Store.</span></span>

## <span data-ttu-id="92294-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="92294-104">SYNTAX</span></span>

```
Get-AzDataLakeStoreChildItem [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="92294-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="92294-105">DESCRIPTION</span></span>
<span data-ttu-id="92294-106">O cmdlet **Get-AzDataLakeStoreChildItem** obtém a lista de itens em uma pasta no Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="92294-106">The **Get-AzDataLakeStoreChildItem** cmdlet gets the list of items in a folder in Data Lake Store.</span></span>

## <span data-ttu-id="92294-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="92294-107">EXAMPLES</span></span>

### <span data-ttu-id="92294-108">Exemplo 1: Obter os itens filho de uma pasta</span><span class="sxs-lookup"><span data-stu-id="92294-108">Example 1: Get the child items for a folder</span></span>
```
PS C:\>Get-AzDataLakeStoreChildItem -AccountName "ContosoADL" -Path "/MyFiles/"
```

<span data-ttu-id="92294-109">Este comando obtém os itens filho da pasta MyFiles.</span><span class="sxs-lookup"><span data-stu-id="92294-109">This command gets the child items for the MyFiles folder.</span></span>

## <span data-ttu-id="92294-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="92294-110">PARAMETERS</span></span>

### <span data-ttu-id="92294-111">-Account</span><span class="sxs-lookup"><span data-stu-id="92294-111">-Account</span></span>
<span data-ttu-id="92294-112">Especifica o nome da conta do Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="92294-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="92294-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92294-113">-DefaultProfile</span></span>
<span data-ttu-id="92294-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="92294-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="92294-115">-Path</span><span class="sxs-lookup"><span data-stu-id="92294-115">-Path</span></span>
<span data-ttu-id="92294-116">Especifica o caminho do Data Lake Store da pasta, começando com o diretório raiz (/).</span><span class="sxs-lookup"><span data-stu-id="92294-116">Specifies the Data Lake Store path of the folder, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="92294-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92294-117">CommonParameters</span></span>
<span data-ttu-id="92294-118">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92294-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92294-119">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="92294-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92294-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="92294-120">INPUTS</span></span>

### <span data-ttu-id="92294-121">System.String</span><span class="sxs-lookup"><span data-stu-id="92294-121">System.String</span></span>

### <span data-ttu-id="92294-122">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="92294-122">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

## <span data-ttu-id="92294-123">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="92294-123">OUTPUTS</span></span>

### <span data-ttu-id="92294-124">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="92294-124">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItem</span></span>

## <span data-ttu-id="92294-125">NOTES</span><span class="sxs-lookup"><span data-stu-id="92294-125">NOTES</span></span>

## <span data-ttu-id="92294-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="92294-126">RELATED LINKS</span></span>

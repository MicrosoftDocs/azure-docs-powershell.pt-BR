---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: ECA70C6C-E0B0-445D-BCAD-041625FAC632
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItem.md
ms.openlocfilehash: ad741d955399b355534074737741b153d8d48690
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93947852"
---
# <span data-ttu-id="fd68a-101">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="fd68a-101">Get-AzDataLakeStoreItem</span></span>

## <span data-ttu-id="fd68a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fd68a-102">SYNOPSIS</span></span>
<span data-ttu-id="fd68a-103">Obtém os detalhes de um arquivo ou pasta no data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="fd68a-103">Gets the details of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="fd68a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fd68a-104">SYNTAX</span></span>

```
Get-AzDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fd68a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fd68a-105">DESCRIPTION</span></span>
<span data-ttu-id="fd68a-106">O cmdlet **Get-AzDataLakeStoreItem** Obtém os detalhes de um arquivo ou pasta no repositório data Lake.</span><span class="sxs-lookup"><span data-stu-id="fd68a-106">The **Get-AzDataLakeStoreItem** cmdlet gets the details of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="fd68a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fd68a-107">EXAMPLES</span></span>

### <span data-ttu-id="fd68a-108">Exemplo 1: obter detalhes de um arquivo do repositório data Lake</span><span class="sxs-lookup"><span data-stu-id="fd68a-108">Example 1: Get details of a file from the Data Lake Store</span></span>
```
PS C:\>Get-AzDataLakeStoreItem -AccountName "ContosoADL" -Path "/MyFiles/Test.csv"
```

<span data-ttu-id="fd68a-109">Este comando obtém os detalhes do arquivo Test.csv do repositório data Lake.</span><span class="sxs-lookup"><span data-stu-id="fd68a-109">This command gets the details of the file Test.csv from the Data Lake Store.</span></span>

## <span data-ttu-id="fd68a-110">OS</span><span class="sxs-lookup"><span data-stu-id="fd68a-110">PARAMETERS</span></span>

### <span data-ttu-id="fd68a-111">-Conta</span><span class="sxs-lookup"><span data-stu-id="fd68a-111">-Account</span></span>
<span data-ttu-id="fd68a-112">Especifica o nome da conta do data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="fd68a-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="fd68a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd68a-113">-DefaultProfile</span></span>
<span data-ttu-id="fd68a-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fd68a-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fd68a-115">-Caminho</span><span class="sxs-lookup"><span data-stu-id="fd68a-115">-Path</span></span>
<span data-ttu-id="fd68a-116">Especifica o caminho do repositório data Lake do qual obter detalhes de um item, começando com o diretório raiz (/).</span><span class="sxs-lookup"><span data-stu-id="fd68a-116">Specifies the Data Lake Store path from which to get details of an item, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="fd68a-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd68a-117">CommonParameters</span></span>
<span data-ttu-id="fd68a-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd68a-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd68a-119">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd68a-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd68a-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fd68a-120">INPUTS</span></span>

### <span data-ttu-id="fd68a-121">System. String</span><span class="sxs-lookup"><span data-stu-id="fd68a-121">System.String</span></span>

### <span data-ttu-id="fd68a-122">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="fd68a-122">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

## <span data-ttu-id="fd68a-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fd68a-123">OUTPUTS</span></span>

### <span data-ttu-id="fd68a-124">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="fd68a-124">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItem</span></span>

## <span data-ttu-id="fd68a-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fd68a-125">NOTES</span></span>

## <span data-ttu-id="fd68a-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fd68a-126">RELATED LINKS</span></span>

[<span data-ttu-id="fd68a-127">Export-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="fd68a-127">Export-AzDataLakeStoreItem</span></span>](./Export-AzDataLakeStoreItem.md)

[<span data-ttu-id="fd68a-128">Get-AzDataLakeStoreChildItem</span><span class="sxs-lookup"><span data-stu-id="fd68a-128">Get-AzDataLakeStoreChildItem</span></span>](./Get-AzDataLakeStoreChildItem.md)

[<span data-ttu-id="fd68a-129">Import-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="fd68a-129">Import-AzDataLakeStoreItem</span></span>](./Import-AzDataLakeStoreItem.md)

[<span data-ttu-id="fd68a-130">Ingressar em AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="fd68a-130">Join-AzDataLakeStoreItem</span></span>](./Join-AzDataLakeStoreItem.md)

[<span data-ttu-id="fd68a-131">Mover-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="fd68a-131">Move-AzDataLakeStoreItem</span></span>](./Move-AzDataLakeStoreItem.md)

[<span data-ttu-id="fd68a-132">New-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="fd68a-132">New-AzDataLakeStoreItem</span></span>](./New-AzDataLakeStoreItem.md)

[<span data-ttu-id="fd68a-133">Remove-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="fd68a-133">Remove-AzDataLakeStoreItem</span></span>](./Remove-AzDataLakeStoreItem.md)

[<span data-ttu-id="fd68a-134">Test-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="fd68a-134">Test-AzDataLakeStoreItem</span></span>](./Test-AzDataLakeStoreItem.md)



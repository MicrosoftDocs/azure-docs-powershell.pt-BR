---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: ECA70C6C-E0B0-445D-BCAD-041625FAC632
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItem.md
ms.openlocfilehash: ad741d955399b355534074737741b153d8d48690
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98426642"
---
# <span data-ttu-id="8501a-101">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="8501a-101">Get-AzDataLakeStoreItem</span></span>

## <span data-ttu-id="8501a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8501a-102">SYNOPSIS</span></span>
<span data-ttu-id="8501a-103">Obtém os detalhes de um arquivo ou pasta no data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="8501a-103">Gets the details of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="8501a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8501a-104">SYNTAX</span></span>

```
Get-AzDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8501a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8501a-105">DESCRIPTION</span></span>
<span data-ttu-id="8501a-106">O cmdlet **Get-AzDataLakeStoreItem** Obtém os detalhes de um arquivo ou pasta no repositório data Lake.</span><span class="sxs-lookup"><span data-stu-id="8501a-106">The **Get-AzDataLakeStoreItem** cmdlet gets the details of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="8501a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8501a-107">EXAMPLES</span></span>

### <span data-ttu-id="8501a-108">Exemplo 1: obter detalhes de um arquivo do repositório data Lake</span><span class="sxs-lookup"><span data-stu-id="8501a-108">Example 1: Get details of a file from the Data Lake Store</span></span>
```
PS C:\>Get-AzDataLakeStoreItem -AccountName "ContosoADL" -Path "/MyFiles/Test.csv"
```

<span data-ttu-id="8501a-109">Este comando obtém os detalhes do arquivo Test.csv do repositório data Lake.</span><span class="sxs-lookup"><span data-stu-id="8501a-109">This command gets the details of the file Test.csv from the Data Lake Store.</span></span>

## <span data-ttu-id="8501a-110">OS</span><span class="sxs-lookup"><span data-stu-id="8501a-110">PARAMETERS</span></span>

### <span data-ttu-id="8501a-111">-Conta</span><span class="sxs-lookup"><span data-stu-id="8501a-111">-Account</span></span>
<span data-ttu-id="8501a-112">Especifica o nome da conta do data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="8501a-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="8501a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8501a-113">-DefaultProfile</span></span>
<span data-ttu-id="8501a-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8501a-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8501a-115">-Caminho</span><span class="sxs-lookup"><span data-stu-id="8501a-115">-Path</span></span>
<span data-ttu-id="8501a-116">Especifica o caminho do repositório data Lake do qual obter detalhes de um item, começando com o diretório raiz (/).</span><span class="sxs-lookup"><span data-stu-id="8501a-116">Specifies the Data Lake Store path from which to get details of an item, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="8501a-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8501a-117">CommonParameters</span></span>
<span data-ttu-id="8501a-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8501a-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8501a-119">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8501a-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8501a-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8501a-120">INPUTS</span></span>

### <span data-ttu-id="8501a-121">System. String</span><span class="sxs-lookup"><span data-stu-id="8501a-121">System.String</span></span>

### <span data-ttu-id="8501a-122">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="8501a-122">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

## <span data-ttu-id="8501a-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8501a-123">OUTPUTS</span></span>

### <span data-ttu-id="8501a-124">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="8501a-124">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItem</span></span>

## <span data-ttu-id="8501a-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8501a-125">NOTES</span></span>

## <span data-ttu-id="8501a-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8501a-126">RELATED LINKS</span></span>

[<span data-ttu-id="8501a-127">Export-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="8501a-127">Export-AzDataLakeStoreItem</span></span>](./Export-AzDataLakeStoreItem.md)

[<span data-ttu-id="8501a-128">Get-AzDataLakeStoreChildItem</span><span class="sxs-lookup"><span data-stu-id="8501a-128">Get-AzDataLakeStoreChildItem</span></span>](./Get-AzDataLakeStoreChildItem.md)

[<span data-ttu-id="8501a-129">Import-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="8501a-129">Import-AzDataLakeStoreItem</span></span>](./Import-AzDataLakeStoreItem.md)

[<span data-ttu-id="8501a-130">Ingressar em AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="8501a-130">Join-AzDataLakeStoreItem</span></span>](./Join-AzDataLakeStoreItem.md)

[<span data-ttu-id="8501a-131">Mover-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="8501a-131">Move-AzDataLakeStoreItem</span></span>](./Move-AzDataLakeStoreItem.md)

[<span data-ttu-id="8501a-132">New-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="8501a-132">New-AzDataLakeStoreItem</span></span>](./New-AzDataLakeStoreItem.md)

[<span data-ttu-id="8501a-133">Remove-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="8501a-133">Remove-AzDataLakeStoreItem</span></span>](./Remove-AzDataLakeStoreItem.md)

[<span data-ttu-id="8501a-134">Test-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="8501a-134">Test-AzDataLakeStoreItem</span></span>](./Test-AzDataLakeStoreItem.md)



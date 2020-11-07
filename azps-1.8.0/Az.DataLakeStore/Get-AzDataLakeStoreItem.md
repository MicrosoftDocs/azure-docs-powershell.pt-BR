---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: ECA70C6C-E0B0-445D-BCAD-041625FAC632
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItem.md
ms.openlocfilehash: b3118c11fa794fef71836a580e272ec481c72147
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93770935"
---
# <span data-ttu-id="d96f6-101">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="d96f6-101">Get-AzDataLakeStoreItem</span></span>

## <span data-ttu-id="d96f6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d96f6-102">SYNOPSIS</span></span>
<span data-ttu-id="d96f6-103">Obtém os detalhes de um arquivo ou pasta no data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="d96f6-103">Gets the details of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="d96f6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d96f6-104">SYNTAX</span></span>

```
Get-AzDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d96f6-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d96f6-105">DESCRIPTION</span></span>
<span data-ttu-id="d96f6-106">O cmdlet **Get-AzDataLakeStoreItem** Obtém os detalhes de um arquivo ou pasta no repositório data Lake.</span><span class="sxs-lookup"><span data-stu-id="d96f6-106">The **Get-AzDataLakeStoreItem** cmdlet gets the details of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="d96f6-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d96f6-107">EXAMPLES</span></span>

### <span data-ttu-id="d96f6-108">Exemplo 1: obter detalhes de um arquivo do repositório data Lake</span><span class="sxs-lookup"><span data-stu-id="d96f6-108">Example 1: Get details of a file from the Data Lake Store</span></span>
```
PS C:\>Get-AzDataLakeStoreItem -AccountName "ContosoADL" -Path "/MyFiles/Test.csv"
```

<span data-ttu-id="d96f6-109">Este comando obtém os detalhes do arquivo Test.csv do repositório data Lake.</span><span class="sxs-lookup"><span data-stu-id="d96f6-109">This command gets the details of the file Test.csv from the Data Lake Store.</span></span>

## <span data-ttu-id="d96f6-110">OS</span><span class="sxs-lookup"><span data-stu-id="d96f6-110">PARAMETERS</span></span>

### <span data-ttu-id="d96f6-111">-Conta</span><span class="sxs-lookup"><span data-stu-id="d96f6-111">-Account</span></span>
<span data-ttu-id="d96f6-112">Especifica o nome da conta do data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="d96f6-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="d96f6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d96f6-113">-DefaultProfile</span></span>
<span data-ttu-id="d96f6-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d96f6-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d96f6-115">-Caminho</span><span class="sxs-lookup"><span data-stu-id="d96f6-115">-Path</span></span>
<span data-ttu-id="d96f6-116">Especifica o caminho do repositório data Lake do qual obter detalhes de um item, começando com o diretório raiz (/).</span><span class="sxs-lookup"><span data-stu-id="d96f6-116">Specifies the Data Lake Store path from which to get details of an item, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="d96f6-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d96f6-117">CommonParameters</span></span>
<span data-ttu-id="d96f6-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d96f6-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d96f6-119">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d96f6-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d96f6-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d96f6-120">INPUTS</span></span>

### <span data-ttu-id="d96f6-121">System. String</span><span class="sxs-lookup"><span data-stu-id="d96f6-121">System.String</span></span>

### <span data-ttu-id="d96f6-122">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="d96f6-122">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

## <span data-ttu-id="d96f6-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d96f6-123">OUTPUTS</span></span>

### <span data-ttu-id="d96f6-124">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="d96f6-124">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItem</span></span>

## <span data-ttu-id="d96f6-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d96f6-125">NOTES</span></span>

## <span data-ttu-id="d96f6-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d96f6-126">RELATED LINKS</span></span>

[<span data-ttu-id="d96f6-127">Export-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="d96f6-127">Export-AzDataLakeStoreItem</span></span>](./Export-AzDataLakeStoreItem.md)

[<span data-ttu-id="d96f6-128">Get-AzDataLakeStoreChildItem</span><span class="sxs-lookup"><span data-stu-id="d96f6-128">Get-AzDataLakeStoreChildItem</span></span>](./Get-AzDataLakeStoreChildItem.md)

[<span data-ttu-id="d96f6-129">Import-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="d96f6-129">Import-AzDataLakeStoreItem</span></span>](./Import-AzDataLakeStoreItem.md)

[<span data-ttu-id="d96f6-130">Ingressar em AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="d96f6-130">Join-AzDataLakeStoreItem</span></span>](./Join-AzDataLakeStoreItem.md)

[<span data-ttu-id="d96f6-131">Mover-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="d96f6-131">Move-AzDataLakeStoreItem</span></span>](./Move-AzDataLakeStoreItem.md)

[<span data-ttu-id="d96f6-132">New-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="d96f6-132">New-AzDataLakeStoreItem</span></span>](./New-AzDataLakeStoreItem.md)

[<span data-ttu-id="d96f6-133">Remove-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="d96f6-133">Remove-AzDataLakeStoreItem</span></span>](./Remove-AzDataLakeStoreItem.md)

[<span data-ttu-id="d96f6-134">Test-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="d96f6-134">Test-AzDataLakeStoreItem</span></span>](./Test-AzDataLakeStoreItem.md)



---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: ECA70C6C-E0B0-445D-BCAD-041625FAC632
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItem.md
ms.openlocfilehash: a7b47425aad152d8851ff90717698b4c25ef026d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93609697"
---
# <span data-ttu-id="6da95-101">Get-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="6da95-101">Get-AzureRmDataLakeStoreItem</span></span>

## <span data-ttu-id="6da95-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6da95-102">SYNOPSIS</span></span>
<span data-ttu-id="6da95-103">Obtém os detalhes de um arquivo ou pasta no data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="6da95-103">Gets the details of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6da95-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6da95-104">SYNTAX</span></span>

```
Get-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6da95-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6da95-105">DESCRIPTION</span></span>
<span data-ttu-id="6da95-106">O cmdlet **Get-AzureRmDataLakeStoreItem** Obtém os detalhes de um arquivo ou pasta no repositório data Lake.</span><span class="sxs-lookup"><span data-stu-id="6da95-106">The **Get-AzureRmDataLakeStoreItem** cmdlet gets the details of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="6da95-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6da95-107">EXAMPLES</span></span>

### <span data-ttu-id="6da95-108">Exemplo 1: obter detalhes de um arquivo do repositório data Lake</span><span class="sxs-lookup"><span data-stu-id="6da95-108">Example 1: Get details of a file from the Data Lake Store</span></span>
```
PS C:\>Get-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Path "/MyFiles/Test.csv"
```

<span data-ttu-id="6da95-109">Este comando obtém os detalhes do arquivo Test.csv do repositório data Lake.</span><span class="sxs-lookup"><span data-stu-id="6da95-109">This command gets the details of the file Test.csv from the Data Lake Store.</span></span>

## <span data-ttu-id="6da95-110">OS</span><span class="sxs-lookup"><span data-stu-id="6da95-110">PARAMETERS</span></span>

### <span data-ttu-id="6da95-111">-Conta</span><span class="sxs-lookup"><span data-stu-id="6da95-111">-Account</span></span>
<span data-ttu-id="6da95-112">Especifica o nome da conta do data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="6da95-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="6da95-113">-Caminho</span><span class="sxs-lookup"><span data-stu-id="6da95-113">-Path</span></span>
<span data-ttu-id="6da95-114">Especifica o caminho do repositório data Lake do qual obter detalhes de um item, começando com o diretório raiz (/).</span><span class="sxs-lookup"><span data-stu-id="6da95-114">Specifies the Data Lake Store path from which to get details of an item, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="6da95-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6da95-115">-DefaultProfile</span></span>
<span data-ttu-id="6da95-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6da95-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6da95-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6da95-117">CommonParameters</span></span>
<span data-ttu-id="6da95-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6da95-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6da95-119">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6da95-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6da95-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6da95-120">INPUTS</span></span>

## <span data-ttu-id="6da95-121">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6da95-121">OUTPUTS</span></span>

### <span data-ttu-id="6da95-122">DataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="6da95-122">DataLakeStoreItem</span></span>
<span data-ttu-id="6da95-123">O arquivo ou pasta no caminho especificado.</span><span class="sxs-lookup"><span data-stu-id="6da95-123">The file or folder at the path specified.</span></span>

## <span data-ttu-id="6da95-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6da95-124">NOTES</span></span>

## <span data-ttu-id="6da95-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6da95-125">RELATED LINKS</span></span>

[<span data-ttu-id="6da95-126">Export-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="6da95-126">Export-AzureRmDataLakeStoreItem</span></span>](./Export-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="6da95-127">Get-AzureRmDataLakeStoreChildItem</span><span class="sxs-lookup"><span data-stu-id="6da95-127">Get-AzureRmDataLakeStoreChildItem</span></span>](./Get-AzureRmDataLakeStoreChildItem.md)

[<span data-ttu-id="6da95-128">Import-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="6da95-128">Import-AzureRmDataLakeStoreItem</span></span>](./Import-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="6da95-129">Ingressar em AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="6da95-129">Join-AzureRmDataLakeStoreItem</span></span>](./Join-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="6da95-130">Mover-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="6da95-130">Move-AzureRmDataLakeStoreItem</span></span>](./Move-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="6da95-131">New-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="6da95-131">New-AzureRmDataLakeStoreItem</span></span>](./New-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="6da95-132">Remove-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="6da95-132">Remove-AzureRmDataLakeStoreItem</span></span>](./Remove-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="6da95-133">Test-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="6da95-133">Test-AzureRmDataLakeStoreItem</span></span>](./Test-AzureRmDataLakeStoreItem.md)



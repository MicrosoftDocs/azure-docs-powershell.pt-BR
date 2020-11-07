---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: A38D8BF6-D302-4586-B7AF-4C80B546E96F
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/add-azdatalakeanalyticsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Add-AzDataLakeAnalyticsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Add-AzDataLakeAnalyticsDataSource.md
ms.openlocfilehash: ddb291a72d3c35c79321ddefa0832d46c489998f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93942803"
---
# <span data-ttu-id="7454d-101">Add-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="7454d-101">Add-AzDataLakeAnalyticsDataSource</span></span>

## <span data-ttu-id="7454d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7454d-102">SYNOPSIS</span></span>
<span data-ttu-id="7454d-103">Adiciona uma fonte de dados a uma conta do data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="7454d-103">Adds a data source to a Data Lake Analytics account.</span></span>

## <span data-ttu-id="7454d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7454d-104">SYNTAX</span></span>

### <span data-ttu-id="7454d-105">AddDataLakeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7454d-105">AddDataLakeStorageAccount</span></span>
```
Add-AzDataLakeAnalyticsDataSource [-Account] <String> [-DataLakeStore] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7454d-106">AddBlobStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7454d-106">AddBlobStorageAccount</span></span>
```
Add-AzDataLakeAnalyticsDataSource [-Account] <String> [-Blob] <String> [-AccessKey] <String>
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7454d-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7454d-107">DESCRIPTION</span></span>
<span data-ttu-id="7454d-108">O cmdlet **Add-AzDataLakeAnalyticsDataSource** adiciona uma fonte de dados a uma conta do Azure data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="7454d-108">The **Add-AzDataLakeAnalyticsDataSource** cmdlet adds a data source to an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="7454d-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7454d-109">EXAMPLES</span></span>

### <span data-ttu-id="7454d-110">Exemplo 1: adicionar uma fonte de dados a uma conta</span><span class="sxs-lookup"><span data-stu-id="7454d-110">Example 1: Add a data source to an account</span></span>
```
PS C:\>Add-AzDataLakeAnalyticsDataSource -Account "ContosoAdlA" -DataLakeStore "ContosoAdlS"
```

<span data-ttu-id="7454d-111">Esse comando adiciona uma fonte de dados do data Lake Store a uma conta do data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="7454d-111">This command adds a Data Lake Store data source to a Data Lake Analytics account.</span></span>

## <span data-ttu-id="7454d-112">OS</span><span class="sxs-lookup"><span data-stu-id="7454d-112">PARAMETERS</span></span>

### <span data-ttu-id="7454d-113">-AccessKey</span><span class="sxs-lookup"><span data-stu-id="7454d-113">-AccessKey</span></span>
<span data-ttu-id="7454d-114">Especifica a tecla de acesso da conta de armazenamento do blob do Azure a ser adicionada.</span><span class="sxs-lookup"><span data-stu-id="7454d-114">Specifies the access key of the Azure Blob storage account to add.</span></span>

```yaml
Type: System.String
Parameter Sets: AddBlobStorageAccount
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7454d-115">-Conta</span><span class="sxs-lookup"><span data-stu-id="7454d-115">-Account</span></span>
<span data-ttu-id="7454d-116">Especifica o nome da conta do data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="7454d-116">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="7454d-117">-Blob</span><span class="sxs-lookup"><span data-stu-id="7454d-117">-Blob</span></span>
<span data-ttu-id="7454d-118">Especifica o nome da conta de armazenamento do blob do Azure a ser adicionada.</span><span class="sxs-lookup"><span data-stu-id="7454d-118">Specifies the name of the Azure Blob Storage account to add.</span></span>

```yaml
Type: System.String
Parameter Sets: AddBlobStorageAccount
Aliases: AzureBlob

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7454d-119">-DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7454d-119">-DataLakeStore</span></span>
<span data-ttu-id="7454d-120">Especifica o nome da conta do Azure data Lake Store a ser adicionada.</span><span class="sxs-lookup"><span data-stu-id="7454d-120">Specifies the name of the Azure Data Lake Store account to add.</span></span>

```yaml
Type: System.String
Parameter Sets: AddDataLakeStorageAccount
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7454d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7454d-121">-DefaultProfile</span></span>
<span data-ttu-id="7454d-122">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="7454d-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7454d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7454d-123">-ResourceGroupName</span></span>
<span data-ttu-id="7454d-124">Especifica o nome do grupo de recursos da conta do data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="7454d-124">Specifies the resource group name of the Data Lake Analytics account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7454d-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7454d-125">CommonParameters</span></span>
<span data-ttu-id="7454d-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7454d-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7454d-127">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7454d-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7454d-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7454d-128">INPUTS</span></span>

### <span data-ttu-id="7454d-129">System. String</span><span class="sxs-lookup"><span data-stu-id="7454d-129">System.String</span></span>

## <span data-ttu-id="7454d-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7454d-130">OUTPUTS</span></span>

### <span data-ttu-id="7454d-131">System. Object</span><span class="sxs-lookup"><span data-stu-id="7454d-131">System.Object</span></span>
## <span data-ttu-id="7454d-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7454d-132">NOTES</span></span>

## <span data-ttu-id="7454d-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7454d-133">RELATED LINKS</span></span>

[<span data-ttu-id="7454d-134">Remove-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="7454d-134">Remove-AzDataLakeAnalyticsDataSource</span></span>](./Remove-AzDataLakeAnalyticsDataSource.md)

[<span data-ttu-id="7454d-135">Set-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="7454d-135">Set-AzDataLakeAnalyticsDataSource</span></span>](./Set-AzDataLakeAnalyticsDataSource.md)



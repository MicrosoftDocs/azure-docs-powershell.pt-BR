---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: A38D8BF6-D302-4586-B7AF-4C80B546E96F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/add-azurermdatalakeanalyticsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Add-AzureRmDataLakeAnalyticsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Add-AzureRmDataLakeAnalyticsDataSource.md
ms.openlocfilehash: 1f2fe13567bd17170fd73854ce5554a693210c7d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428957"
---
# <span data-ttu-id="da431-101">Add-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="da431-101">Add-AzureRmDataLakeAnalyticsDataSource</span></span>

## <span data-ttu-id="da431-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="da431-102">SYNOPSIS</span></span>
<span data-ttu-id="da431-103">Adiciona uma fonte de dados a uma conta do data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="da431-103">Adds a data source to a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="da431-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="da431-104">SYNTAX</span></span>

### <span data-ttu-id="da431-105">AddDataLakeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="da431-105">AddDataLakeStorageAccount</span></span>
```
Add-AzureRmDataLakeAnalyticsDataSource [-Account] <String> [-DataLakeStore] <String>
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="da431-106">AddBlobStorageAccount</span><span class="sxs-lookup"><span data-stu-id="da431-106">AddBlobStorageAccount</span></span>
```
Add-AzureRmDataLakeAnalyticsDataSource [-Account] <String> [-Blob] <String> [-AccessKey] <String>
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="da431-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="da431-107">DESCRIPTION</span></span>
<span data-ttu-id="da431-108">O cmdlet **Add-AzureRmDataLakeAnalyticsDataSource** adiciona uma fonte de dados a uma conta do Azure data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="da431-108">The **Add-AzureRmDataLakeAnalyticsDataSource** cmdlet adds a data source to an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="da431-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="da431-109">EXAMPLES</span></span>

### <span data-ttu-id="da431-110">Exemplo 1: adicionar uma fonte de dados a uma conta</span><span class="sxs-lookup"><span data-stu-id="da431-110">Example 1: Add a data source to an account</span></span>
```
PS C:\>Add-AzureRmDataLakeAnalyticsDataSource -Account "ContosoAdlA" -DataLakeStore "ContosoAdlS"
```

<span data-ttu-id="da431-111">Esse comando adiciona uma fonte de dados do data Lake Store a uma conta do data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="da431-111">This command adds a Data Lake Store data source to a Data Lake Analytics account.</span></span>

## <span data-ttu-id="da431-112">OS</span><span class="sxs-lookup"><span data-stu-id="da431-112">PARAMETERS</span></span>

### <span data-ttu-id="da431-113">-AccessKey</span><span class="sxs-lookup"><span data-stu-id="da431-113">-AccessKey</span></span>
<span data-ttu-id="da431-114">Especifica a tecla de acesso da conta de armazenamento do blob do Azure a ser adicionada.</span><span class="sxs-lookup"><span data-stu-id="da431-114">Specifies the access key of the Azure Blob storage account to add.</span></span>

```yaml
Type: String
Parameter Sets: AddBlobStorageAccount
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da431-115">-Conta</span><span class="sxs-lookup"><span data-stu-id="da431-115">-Account</span></span>
<span data-ttu-id="da431-116">Especifica o nome da conta do data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="da431-116">Specifies the Data Lake Analytics account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da431-117">-Blob</span><span class="sxs-lookup"><span data-stu-id="da431-117">-Blob</span></span>
<span data-ttu-id="da431-118">Especifica o nome da conta de armazenamento do blob do Azure a ser adicionada.</span><span class="sxs-lookup"><span data-stu-id="da431-118">Specifies the name of the Azure Blob Storage account to add.</span></span>

```yaml
Type: String
Parameter Sets: AddBlobStorageAccount
Aliases: AzureBlob

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da431-119">-DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="da431-119">-DataLakeStore</span></span>
<span data-ttu-id="da431-120">Especifica o nome da conta do Azure data Lake Store a ser adicionada.</span><span class="sxs-lookup"><span data-stu-id="da431-120">Specifies the name of the Azure Data Lake Store account to add.</span></span>

```yaml
Type: String
Parameter Sets: AddDataLakeStorageAccount
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da431-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da431-121">-DefaultProfile</span></span>
<span data-ttu-id="da431-122">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="da431-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da431-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da431-123">-ResourceGroupName</span></span>
<span data-ttu-id="da431-124">Especifica o nome do grupo de recursos da conta do data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="da431-124">Specifies the resource group name of the Data Lake Analytics account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da431-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da431-125">CommonParameters</span></span>
<span data-ttu-id="da431-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da431-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da431-127">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da431-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da431-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="da431-128">INPUTS</span></span>

### <span data-ttu-id="da431-129">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="da431-129">None</span></span>
<span data-ttu-id="da431-130">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="da431-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="da431-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="da431-131">OUTPUTS</span></span>

### <span data-ttu-id="da431-132">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="da431-132">None</span></span>

## <span data-ttu-id="da431-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="da431-133">NOTES</span></span>

## <span data-ttu-id="da431-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="da431-134">RELATED LINKS</span></span>

[<span data-ttu-id="da431-135">Remove-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="da431-135">Remove-AzureRmDataLakeAnalyticsDataSource</span></span>](./Remove-AzureRmDataLakeAnalyticsDataSource.md)

[<span data-ttu-id="da431-136">Set-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="da431-136">Set-AzureRmDataLakeAnalyticsDataSource</span></span>](./Set-AzureRmDataLakeAnalyticsDataSource.md)



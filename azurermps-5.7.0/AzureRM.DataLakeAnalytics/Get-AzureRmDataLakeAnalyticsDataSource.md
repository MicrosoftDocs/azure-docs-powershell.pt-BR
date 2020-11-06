---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 0377C4E9-C1DC-49BA-BBC4-5598C83234F8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/get-azurermdatalakeanalyticsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsDataSource.md
ms.openlocfilehash: 93e64c4a64eecbe66fc3f9b2923ade65405a05a4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426718"
---
# <span data-ttu-id="cc97c-101">Get-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="cc97c-101">Get-AzureRmDataLakeAnalyticsDataSource</span></span>

## <span data-ttu-id="cc97c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cc97c-102">SYNOPSIS</span></span>
<span data-ttu-id="cc97c-103">Obtém uma fonte de dados do data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="cc97c-103">Gets a Data Lake Analytics data source.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cc97c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cc97c-104">SYNTAX</span></span>

### <span data-ttu-id="cc97c-105">GetAllDataSources (padrão)</span><span class="sxs-lookup"><span data-stu-id="cc97c-105">GetAllDataSources (Default)</span></span>
```
Get-AzureRmDataLakeAnalyticsDataSource [-Account] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cc97c-106">GetDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="cc97c-106">GetDataLakeStoreAccount</span></span>
```
Get-AzureRmDataLakeAnalyticsDataSource [-Account] <String> [-DataLakeStore] <String>
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cc97c-107">GetBlobStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cc97c-107">GetBlobStorageAccount</span></span>
```
Get-AzureRmDataLakeAnalyticsDataSource [-Account] <String> [-Blob] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cc97c-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="cc97c-108">DESCRIPTION</span></span>
<span data-ttu-id="cc97c-109">O cmdlet **Get-AzureRmDataLakeAnalyticsDataSource** Obtém uma fonte de dados do Azure data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="cc97c-109">The **Get-AzureRmDataLakeAnalyticsDataSource** cmdlet gets an Azure Data Lake Analytics data source.</span></span>

## <span data-ttu-id="cc97c-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cc97c-110">EXAMPLES</span></span>

### <span data-ttu-id="cc97c-111">Exemplo 1: obter uma fonte de dados de uma conta</span><span class="sxs-lookup"><span data-stu-id="cc97c-111">Example 1: Get a data source from an account</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsDataSource -AccountName "ContosoAdlA" -DataLakeStore "ContosoAdls"
```

<span data-ttu-id="cc97c-112">Este comando obtém uma fonte de dados do data Lake Store chamada ContosoAdls de uma conta do data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="cc97c-112">This command gets a Data Lake Store data source named ContosoAdls from a Data Lake Analytics account.</span></span>

### <span data-ttu-id="cc97c-113">Exemplo 2: obter a lista de contas do data Lake Store em uma conta do data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="cc97c-113">Example 2: Get the list of Data Lake Store accounts in a Data Lake Analytics account</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsDataSource -AccountName "ContosoAdlA" -DataSource "DataLakeStore"
```

<span data-ttu-id="cc97c-114">Esse comando obtém todas as contas do data Lake Store de uma conta do data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="cc97c-114">This command gets all Data Lake Store accounts from a Data Lake Analytics account.</span></span>

## <span data-ttu-id="cc97c-115">OS</span><span class="sxs-lookup"><span data-stu-id="cc97c-115">PARAMETERS</span></span>

### <span data-ttu-id="cc97c-116">-Conta</span><span class="sxs-lookup"><span data-stu-id="cc97c-116">-Account</span></span>
<span data-ttu-id="cc97c-117">Especifica a conta do data Lake Analytics que este cmdlet obtém fontes de dados.</span><span class="sxs-lookup"><span data-stu-id="cc97c-117">Specifies the Data Lake Analytics account that this cmdlet gets data sources.</span></span>

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

### <span data-ttu-id="cc97c-118">-Blob</span><span class="sxs-lookup"><span data-stu-id="cc97c-118">-Blob</span></span>
<span data-ttu-id="cc97c-119">Especifica o nome da fonte de dados de armazenamento do blob do Azure.</span><span class="sxs-lookup"><span data-stu-id="cc97c-119">Specifies the name of the Azure Blob Storage data source.</span></span>

```yaml
Type: String
Parameter Sets: GetBlobStorageAccount
Aliases: AzureBlob

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc97c-120">-DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="cc97c-120">-DataLakeStore</span></span>
<span data-ttu-id="cc97c-121">Especifica o nome da conta do data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="cc97c-121">Specifies the name of the Data Lake Store account.</span></span>

```yaml
Type: String
Parameter Sets: GetDataLakeStoreAccount
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc97c-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc97c-122">-DefaultProfile</span></span>
<span data-ttu-id="cc97c-123">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="cc97c-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cc97c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc97c-124">-ResourceGroupName</span></span>
<span data-ttu-id="cc97c-125">Especifica o nome do grupo de recursos que contém a fonte de dados.</span><span class="sxs-lookup"><span data-stu-id="cc97c-125">Specifies the resource group name that contains the data source.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc97c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc97c-126">CommonParameters</span></span>
<span data-ttu-id="cc97c-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc97c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc97c-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cc97c-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc97c-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="cc97c-129">INPUTS</span></span>

### <span data-ttu-id="cc97c-130">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="cc97c-130">None</span></span>
<span data-ttu-id="cc97c-131">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="cc97c-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="cc97c-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="cc97c-132">OUTPUTS</span></span>

### <span data-ttu-id="cc97c-133">PSStorageAccountInfo</span><span class="sxs-lookup"><span data-stu-id="cc97c-133">PSStorageAccountInfo</span></span>
<span data-ttu-id="cc97c-134">Os detalhes da conta de armazenamento do Azure especificada.</span><span class="sxs-lookup"><span data-stu-id="cc97c-134">The specified Azure Storage account details.</span></span>

### <span data-ttu-id="cc97c-135">PSDataLakeStoreAccountInfo</span><span class="sxs-lookup"><span data-stu-id="cc97c-135">PSDataLakeStoreAccountInfo</span></span>
<span data-ttu-id="cc97c-136">Os detalhes da conta do repositório data Lake especificado</span><span class="sxs-lookup"><span data-stu-id="cc97c-136">The specified Data Lake Store account details</span></span>

### <span data-ttu-id="cc97c-137">Programação<AdlDataSource></span><span class="sxs-lookup"><span data-stu-id="cc97c-137">List<AdlDataSource></span></span>
<span data-ttu-id="cc97c-138">A lista das contas de armazenamento do Azure e do data Lake Store na conta do data Lake Analytics especificada.</span><span class="sxs-lookup"><span data-stu-id="cc97c-138">The list of both Azure Storage accounts and Data Lake Store accounts in the specified Data Lake Analytics account.</span></span>

## <span data-ttu-id="cc97c-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="cc97c-139">NOTES</span></span>

## <span data-ttu-id="cc97c-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cc97c-140">RELATED LINKS</span></span>

[<span data-ttu-id="cc97c-141">Add-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="cc97c-141">Add-AzureRmDataLakeAnalyticsDataSource</span></span>](./Add-AzureRmDataLakeAnalyticsDataSource.md)

[<span data-ttu-id="cc97c-142">Remove-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="cc97c-142">Remove-AzureRmDataLakeAnalyticsDataSource</span></span>](./Remove-AzureRmDataLakeAnalyticsDataSource.md)

[<span data-ttu-id="cc97c-143">Set-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="cc97c-143">Set-AzureRmDataLakeAnalyticsDataSource</span></span>](./Set-AzureRmDataLakeAnalyticsDataSource.md)



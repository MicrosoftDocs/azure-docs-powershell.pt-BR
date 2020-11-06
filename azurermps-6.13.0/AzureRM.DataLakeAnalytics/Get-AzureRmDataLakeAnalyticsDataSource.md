---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 0377C4E9-C1DC-49BA-BBC4-5598C83234F8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/get-azurermdatalakeanalyticsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsDataSource.md
ms.openlocfilehash: 2f6dfae3d13a6de57a7dc04367ec2886be78f5f5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93433273"
---
# <span data-ttu-id="a3626-101">Get-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="a3626-101">Get-AzureRmDataLakeAnalyticsDataSource</span></span>

## <span data-ttu-id="a3626-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a3626-102">SYNOPSIS</span></span>
<span data-ttu-id="a3626-103">Obtém uma fonte de dados do data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="a3626-103">Gets a Data Lake Analytics data source.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a3626-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a3626-104">SYNTAX</span></span>

### <span data-ttu-id="a3626-105">GetAllDataSources (padrão)</span><span class="sxs-lookup"><span data-stu-id="a3626-105">GetAllDataSources (Default)</span></span>
```
Get-AzureRmDataLakeAnalyticsDataSource [-Account] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a3626-106">GetDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="a3626-106">GetDataLakeStoreAccount</span></span>
```
Get-AzureRmDataLakeAnalyticsDataSource [-Account] <String> [-DataLakeStore] <String>
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a3626-107">GetBlobStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a3626-107">GetBlobStorageAccount</span></span>
```
Get-AzureRmDataLakeAnalyticsDataSource [-Account] <String> [-Blob] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a3626-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a3626-108">DESCRIPTION</span></span>
<span data-ttu-id="a3626-109">O cmdlet **Get-AzureRmDataLakeAnalyticsDataSource** Obtém uma fonte de dados do Azure data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="a3626-109">The **Get-AzureRmDataLakeAnalyticsDataSource** cmdlet gets an Azure Data Lake Analytics data source.</span></span>

## <span data-ttu-id="a3626-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a3626-110">EXAMPLES</span></span>

### <span data-ttu-id="a3626-111">Exemplo 1: obter uma fonte de dados de uma conta</span><span class="sxs-lookup"><span data-stu-id="a3626-111">Example 1: Get a data source from an account</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsDataSource -AccountName "ContosoAdlA" -DataLakeStore "ContosoAdls"
```

<span data-ttu-id="a3626-112">Este comando obtém uma fonte de dados do data Lake Store chamada ContosoAdls de uma conta do data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="a3626-112">This command gets a Data Lake Store data source named ContosoAdls from a Data Lake Analytics account.</span></span>

### <span data-ttu-id="a3626-113">Exemplo 2: obter a lista de contas do data Lake Store em uma conta do data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="a3626-113">Example 2: Get the list of Data Lake Store accounts in a Data Lake Analytics account</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsDataSource -AccountName "ContosoAdlA" -DataSource "DataLakeStore"
```

<span data-ttu-id="a3626-114">Esse comando obtém todas as contas do data Lake Store de uma conta do data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="a3626-114">This command gets all Data Lake Store accounts from a Data Lake Analytics account.</span></span>

## <span data-ttu-id="a3626-115">OS</span><span class="sxs-lookup"><span data-stu-id="a3626-115">PARAMETERS</span></span>

### <span data-ttu-id="a3626-116">-Conta</span><span class="sxs-lookup"><span data-stu-id="a3626-116">-Account</span></span>
<span data-ttu-id="a3626-117">Especifica a conta do data Lake Analytics que este cmdlet obtém fontes de dados.</span><span class="sxs-lookup"><span data-stu-id="a3626-117">Specifies the Data Lake Analytics account that this cmdlet gets data sources.</span></span>

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

### <span data-ttu-id="a3626-118">-Blob</span><span class="sxs-lookup"><span data-stu-id="a3626-118">-Blob</span></span>
<span data-ttu-id="a3626-119">Especifica o nome da fonte de dados de armazenamento do blob do Azure.</span><span class="sxs-lookup"><span data-stu-id="a3626-119">Specifies the name of the Azure Blob Storage data source.</span></span>

```yaml
Type: System.String
Parameter Sets: GetBlobStorageAccount
Aliases: AzureBlob

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3626-120">-DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a3626-120">-DataLakeStore</span></span>
<span data-ttu-id="a3626-121">Especifica o nome da conta do data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="a3626-121">Specifies the name of the Data Lake Store account.</span></span>

```yaml
Type: System.String
Parameter Sets: GetDataLakeStoreAccount
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3626-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3626-122">-DefaultProfile</span></span>
<span data-ttu-id="a3626-123">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="a3626-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a3626-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3626-124">-ResourceGroupName</span></span>
<span data-ttu-id="a3626-125">Especifica o nome do grupo de recursos que contém a fonte de dados.</span><span class="sxs-lookup"><span data-stu-id="a3626-125">Specifies the resource group name that contains the data source.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3626-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3626-126">CommonParameters</span></span>
<span data-ttu-id="a3626-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3626-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3626-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a3626-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3626-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a3626-129">INPUTS</span></span>

### <span data-ttu-id="a3626-130">System. String</span><span class="sxs-lookup"><span data-stu-id="a3626-130">System.String</span></span>

## <span data-ttu-id="a3626-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a3626-131">OUTPUTS</span></span>

### <span data-ttu-id="a3626-132">Microsoft. Azure. Commands. DataLakeAnalytics. Models. PSStorageAccountInfo</span><span class="sxs-lookup"><span data-stu-id="a3626-132">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSStorageAccountInfo</span></span>

### <span data-ttu-id="a3626-133">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeStoreAccountInfo</span><span class="sxs-lookup"><span data-stu-id="a3626-133">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeStoreAccountInfo</span></span>

### <span data-ttu-id="a3626-134">Microsoft. Azure. Commands. DataLakeAnalytics. Models. AdlDataSource</span><span class="sxs-lookup"><span data-stu-id="a3626-134">Microsoft.Azure.Commands.DataLakeAnalytics.Models.AdlDataSource</span></span>

## <span data-ttu-id="a3626-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a3626-135">NOTES</span></span>

## <span data-ttu-id="a3626-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a3626-136">RELATED LINKS</span></span>

[<span data-ttu-id="a3626-137">Add-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="a3626-137">Add-AzureRmDataLakeAnalyticsDataSource</span></span>](./Add-AzureRmDataLakeAnalyticsDataSource.md)

[<span data-ttu-id="a3626-138">Remove-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="a3626-138">Remove-AzureRmDataLakeAnalyticsDataSource</span></span>](./Remove-AzureRmDataLakeAnalyticsDataSource.md)

[<span data-ttu-id="a3626-139">Set-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="a3626-139">Set-AzureRmDataLakeAnalyticsDataSource</span></span>](./Set-AzureRmDataLakeAnalyticsDataSource.md)



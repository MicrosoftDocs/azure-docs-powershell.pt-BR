---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: 0377C4E9-C1DC-49BA-BBC4-5598C83234F8
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsDataSource.md
ms.openlocfilehash: e14e4c1b58b24cb8065681ae806789cd1252a0db
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93940848"
---
# <span data-ttu-id="ef9b2-101">Get-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="ef9b2-101">Get-AzDataLakeAnalyticsDataSource</span></span>

## <span data-ttu-id="ef9b2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ef9b2-102">SYNOPSIS</span></span>
<span data-ttu-id="ef9b2-103">Obtém uma fonte de dados do data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="ef9b2-103">Gets a Data Lake Analytics data source.</span></span>

## <span data-ttu-id="ef9b2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ef9b2-104">SYNTAX</span></span>

### <span data-ttu-id="ef9b2-105">GetAllDataSources (padrão)</span><span class="sxs-lookup"><span data-stu-id="ef9b2-105">GetAllDataSources (Default)</span></span>
```
Get-AzDataLakeAnalyticsDataSource [-Account] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ef9b2-106">GetDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="ef9b2-106">GetDataLakeStoreAccount</span></span>
```
Get-AzDataLakeAnalyticsDataSource [-Account] <String> [-DataLakeStore] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ef9b2-107">GetBlobStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ef9b2-107">GetBlobStorageAccount</span></span>
```
Get-AzDataLakeAnalyticsDataSource [-Account] <String> [-Blob] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ef9b2-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ef9b2-108">DESCRIPTION</span></span>
<span data-ttu-id="ef9b2-109">O cmdlet **Get-AzDataLakeAnalyticsDataSource** Obtém uma fonte de dados do Azure data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="ef9b2-109">The **Get-AzDataLakeAnalyticsDataSource** cmdlet gets an Azure Data Lake Analytics data source.</span></span>

## <span data-ttu-id="ef9b2-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ef9b2-110">EXAMPLES</span></span>

### <span data-ttu-id="ef9b2-111">Exemplo 1: obter uma fonte de dados de uma conta</span><span class="sxs-lookup"><span data-stu-id="ef9b2-111">Example 1: Get a data source from an account</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsDataSource -AccountName "ContosoAdlA" -DataLakeStore "ContosoAdls"
```

<span data-ttu-id="ef9b2-112">Este comando obtém uma fonte de dados do data Lake Store chamada ContosoAdls de uma conta do data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="ef9b2-112">This command gets a Data Lake Store data source named ContosoAdls from a Data Lake Analytics account.</span></span>

### <span data-ttu-id="ef9b2-113">Exemplo 2: obter a lista de contas do data Lake Store em uma conta do data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="ef9b2-113">Example 2: Get the list of Data Lake Store accounts in a Data Lake Analytics account</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsDataSource -AccountName "ContosoAdlA" -DataSource "DataLakeStore"
```

<span data-ttu-id="ef9b2-114">Esse comando obtém todas as contas do data Lake Store de uma conta do data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="ef9b2-114">This command gets all Data Lake Store accounts from a Data Lake Analytics account.</span></span>

## <span data-ttu-id="ef9b2-115">OS</span><span class="sxs-lookup"><span data-stu-id="ef9b2-115">PARAMETERS</span></span>

### <span data-ttu-id="ef9b2-116">-Conta</span><span class="sxs-lookup"><span data-stu-id="ef9b2-116">-Account</span></span>
<span data-ttu-id="ef9b2-117">Especifica a conta do data Lake Analytics que este cmdlet obtém fontes de dados.</span><span class="sxs-lookup"><span data-stu-id="ef9b2-117">Specifies the Data Lake Analytics account that this cmdlet gets data sources.</span></span>

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

### <span data-ttu-id="ef9b2-118">-Blob</span><span class="sxs-lookup"><span data-stu-id="ef9b2-118">-Blob</span></span>
<span data-ttu-id="ef9b2-119">Especifica o nome da fonte de dados de armazenamento do blob do Azure.</span><span class="sxs-lookup"><span data-stu-id="ef9b2-119">Specifies the name of the Azure Blob Storage data source.</span></span>

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

### <span data-ttu-id="ef9b2-120">-DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ef9b2-120">-DataLakeStore</span></span>
<span data-ttu-id="ef9b2-121">Especifica o nome da conta do data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="ef9b2-121">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="ef9b2-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef9b2-122">-DefaultProfile</span></span>
<span data-ttu-id="ef9b2-123">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="ef9b2-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ef9b2-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef9b2-124">-ResourceGroupName</span></span>
<span data-ttu-id="ef9b2-125">Especifica o nome do grupo de recursos que contém a fonte de dados.</span><span class="sxs-lookup"><span data-stu-id="ef9b2-125">Specifies the resource group name that contains the data source.</span></span>

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

### <span data-ttu-id="ef9b2-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef9b2-126">CommonParameters</span></span>
<span data-ttu-id="ef9b2-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef9b2-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef9b2-128">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef9b2-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef9b2-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ef9b2-129">INPUTS</span></span>

### <span data-ttu-id="ef9b2-130">System. String</span><span class="sxs-lookup"><span data-stu-id="ef9b2-130">System.String</span></span>

## <span data-ttu-id="ef9b2-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ef9b2-131">OUTPUTS</span></span>

### <span data-ttu-id="ef9b2-132">Microsoft. Azure. Commands. DataLakeAnalytics. Models. PSStorageAccountInfo</span><span class="sxs-lookup"><span data-stu-id="ef9b2-132">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSStorageAccountInfo</span></span>

### <span data-ttu-id="ef9b2-133">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeStoreAccountInfo</span><span class="sxs-lookup"><span data-stu-id="ef9b2-133">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeStoreAccountInfo</span></span>

### <span data-ttu-id="ef9b2-134">Microsoft. Azure. Commands. DataLakeAnalytics. Models. AdlDataSource</span><span class="sxs-lookup"><span data-stu-id="ef9b2-134">Microsoft.Azure.Commands.DataLakeAnalytics.Models.AdlDataSource</span></span>

## <span data-ttu-id="ef9b2-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ef9b2-135">NOTES</span></span>

## <span data-ttu-id="ef9b2-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ef9b2-136">RELATED LINKS</span></span>

[<span data-ttu-id="ef9b2-137">Add-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="ef9b2-137">Add-AzDataLakeAnalyticsDataSource</span></span>](./Add-AzDataLakeAnalyticsDataSource.md)

[<span data-ttu-id="ef9b2-138">Remove-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="ef9b2-138">Remove-AzDataLakeAnalyticsDataSource</span></span>](./Remove-AzDataLakeAnalyticsDataSource.md)

[<span data-ttu-id="ef9b2-139">Set-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="ef9b2-139">Set-AzDataLakeAnalyticsDataSource</span></span>](./Set-AzDataLakeAnalyticsDataSource.md)



---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: 0377C4E9-C1DC-49BA-BBC4-5598C83234F8
online version: https://docs.microsoft.com/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsDataSource.md
ms.openlocfilehash: 016c2520ee97f03c19a68eefebdc0319bacdb6e1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892507"
---
# <span data-ttu-id="75a77-101">Get-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="75a77-101">Get-AzDataLakeAnalyticsDataSource</span></span>

## <span data-ttu-id="75a77-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="75a77-102">SYNOPSIS</span></span>
<span data-ttu-id="75a77-103">Obtém uma fonte de dados do Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="75a77-103">Gets a Data Lake Analytics data source.</span></span>

## <span data-ttu-id="75a77-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="75a77-104">SYNTAX</span></span>

### <span data-ttu-id="75a77-105">GetAllDataSources (Padrão)</span><span class="sxs-lookup"><span data-stu-id="75a77-105">GetAllDataSources (Default)</span></span>
```
Get-AzDataLakeAnalyticsDataSource [-Account] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="75a77-106">GetDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="75a77-106">GetDataLakeStoreAccount</span></span>
```
Get-AzDataLakeAnalyticsDataSource [-Account] <String> [-DataLakeStore] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="75a77-107">GetBlobStorageAccount</span><span class="sxs-lookup"><span data-stu-id="75a77-107">GetBlobStorageAccount</span></span>
```
Get-AzDataLakeAnalyticsDataSource [-Account] <String> [-Blob] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="75a77-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="75a77-108">DESCRIPTION</span></span>
<span data-ttu-id="75a77-109">O cmdlet **Get-AzDataLakeAnalyticsDataSource** obtém uma fonte de dados do Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="75a77-109">The **Get-AzDataLakeAnalyticsDataSource** cmdlet gets an Azure Data Lake Analytics data source.</span></span>

## <span data-ttu-id="75a77-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="75a77-110">EXAMPLES</span></span>

### <span data-ttu-id="75a77-111">Exemplo 1: Obter uma fonte de dados de uma conta</span><span class="sxs-lookup"><span data-stu-id="75a77-111">Example 1: Get a data source from an account</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsDataSource -AccountName "ContosoAdlA" -DataLakeStore "ContosoAdls"
```

<span data-ttu-id="75a77-112">Este comando obtém uma fonte de dados do Data Lake Store chamada ContosoAdls de uma conta do Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="75a77-112">This command gets a Data Lake Store data source named ContosoAdls from a Data Lake Analytics account.</span></span>

### <span data-ttu-id="75a77-113">Exemplo 2: Obter a lista de contas do Data Lake Store em uma conta do Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="75a77-113">Example 2: Get the list of Data Lake Store accounts in a Data Lake Analytics account</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsDataSource -AccountName "ContosoAdlA" -DataSource "DataLakeStore"
```

<span data-ttu-id="75a77-114">Este comando obtém todas as contas do Data Lake Store de uma conta do Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="75a77-114">This command gets all Data Lake Store accounts from a Data Lake Analytics account.</span></span>

## <span data-ttu-id="75a77-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="75a77-115">PARAMETERS</span></span>

### <span data-ttu-id="75a77-116">-Account</span><span class="sxs-lookup"><span data-stu-id="75a77-116">-Account</span></span>
<span data-ttu-id="75a77-117">Especifica a conta do Data Lake Analytics que este cmdlet obtém fontes de dados.</span><span class="sxs-lookup"><span data-stu-id="75a77-117">Specifies the Data Lake Analytics account that this cmdlet gets data sources.</span></span>

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

### <span data-ttu-id="75a77-118">-Blob</span><span class="sxs-lookup"><span data-stu-id="75a77-118">-Blob</span></span>
<span data-ttu-id="75a77-119">Especifica o nome da fonte de dados armazenamento de blob do Azure.</span><span class="sxs-lookup"><span data-stu-id="75a77-119">Specifies the name of the Azure Blob Storage data source.</span></span>

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

### <span data-ttu-id="75a77-120">-DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="75a77-120">-DataLakeStore</span></span>
<span data-ttu-id="75a77-121">Especifica o nome da conta do Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="75a77-121">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="75a77-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75a77-122">-DefaultProfile</span></span>
<span data-ttu-id="75a77-123">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="75a77-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="75a77-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75a77-124">-ResourceGroupName</span></span>
<span data-ttu-id="75a77-125">Especifica o nome do grupo de recursos que contém a fonte de dados.</span><span class="sxs-lookup"><span data-stu-id="75a77-125">Specifies the resource group name that contains the data source.</span></span>

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

### <span data-ttu-id="75a77-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75a77-126">CommonParameters</span></span>
<span data-ttu-id="75a77-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75a77-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75a77-128">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75a77-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75a77-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="75a77-129">INPUTS</span></span>

### <span data-ttu-id="75a77-130">System.String</span><span class="sxs-lookup"><span data-stu-id="75a77-130">System.String</span></span>

## <span data-ttu-id="75a77-131">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="75a77-131">OUTPUTS</span></span>

### <span data-ttu-id="75a77-132">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSStorageAccountInfo</span><span class="sxs-lookup"><span data-stu-id="75a77-132">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSStorageAccountInfo</span></span>

### <span data-ttu-id="75a77-133">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeStoreAccountInfo</span><span class="sxs-lookup"><span data-stu-id="75a77-133">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeStoreAccountInfo</span></span>

### <span data-ttu-id="75a77-134">Microsoft.Azure.Commands.DataLakeAnalytics.Models.AdlDataSource</span><span class="sxs-lookup"><span data-stu-id="75a77-134">Microsoft.Azure.Commands.DataLakeAnalytics.Models.AdlDataSource</span></span>

## <span data-ttu-id="75a77-135">NOTES</span><span class="sxs-lookup"><span data-stu-id="75a77-135">NOTES</span></span>

## <span data-ttu-id="75a77-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="75a77-136">RELATED LINKS</span></span>

[<span data-ttu-id="75a77-137">Add-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="75a77-137">Add-AzDataLakeAnalyticsDataSource</span></span>](./Add-AzDataLakeAnalyticsDataSource.md)

[<span data-ttu-id="75a77-138">Remove-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="75a77-138">Remove-AzDataLakeAnalyticsDataSource</span></span>](./Remove-AzDataLakeAnalyticsDataSource.md)

[<span data-ttu-id="75a77-139">Set-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="75a77-139">Set-AzDataLakeAnalyticsDataSource</span></span>](./Set-AzDataLakeAnalyticsDataSource.md)



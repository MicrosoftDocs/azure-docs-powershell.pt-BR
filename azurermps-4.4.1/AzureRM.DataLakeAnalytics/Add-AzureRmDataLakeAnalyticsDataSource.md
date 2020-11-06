---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: A38D8BF6-D302-4586-B7AF-4C80B546E96F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Add-AzureRmDataLakeAnalyticsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Add-AzureRmDataLakeAnalyticsDataSource.md
ms.openlocfilehash: a3eff47b688f2f426c4f255d400ce1ef73c3c027
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427965"
---
# <span data-ttu-id="989b0-101">Add-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="989b0-101">Add-AzureRmDataLakeAnalyticsDataSource</span></span>

## <span data-ttu-id="989b0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="989b0-102">SYNOPSIS</span></span>
<span data-ttu-id="989b0-103">Adiciona uma fonte de dados a uma conta do data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="989b0-103">Adds a data source to a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="989b0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="989b0-104">SYNTAX</span></span>

### <span data-ttu-id="989b0-105">Adicionar uma conta de armazenamento do data Lake</span><span class="sxs-lookup"><span data-stu-id="989b0-105">Add a Data Lake storage account</span></span>
```
Add-AzureRmDataLakeAnalyticsDataSource [-Account] <String> [-DataLakeStore] <String>
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="989b0-106">Adicionar uma conta de armazenamento de BLOB</span><span class="sxs-lookup"><span data-stu-id="989b0-106">Add a Blob storage account</span></span>
```
Add-AzureRmDataLakeAnalyticsDataSource [-Account] <String> [-Blob] <String> [-AccessKey] <String>
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="989b0-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="989b0-107">DESCRIPTION</span></span>
<span data-ttu-id="989b0-108">O cmdlet **Add-AzureRmDataLakeAnalyticsDataSource** adiciona uma fonte de dados a uma conta do Azure data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="989b0-108">The **Add-AzureRmDataLakeAnalyticsDataSource** cmdlet adds a data source to an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="989b0-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="989b0-109">EXAMPLES</span></span>

### <span data-ttu-id="989b0-110">Exemplo 1: adicionar uma fonte de dados a uma conta</span><span class="sxs-lookup"><span data-stu-id="989b0-110">Example 1: Add a data source to an account</span></span>
```
PS C:\>Add-AzureRmDataLakeAnalyticsDataSource -Account "ContosoAdlA" -DataLakeStore "ContosoAdlS"
```

<span data-ttu-id="989b0-111">Esse comando adiciona uma fonte de dados do data Lake Store a uma conta do data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="989b0-111">This command adds a Data Lake Store data source to a Data Lake Analytics account.</span></span>

## <span data-ttu-id="989b0-112">OS</span><span class="sxs-lookup"><span data-stu-id="989b0-112">PARAMETERS</span></span>

### <span data-ttu-id="989b0-113">-AccessKey</span><span class="sxs-lookup"><span data-stu-id="989b0-113">-AccessKey</span></span>
<span data-ttu-id="989b0-114">Especifica a tecla de acesso da conta de armazenamento do blob do Azure a ser adicionada.</span><span class="sxs-lookup"><span data-stu-id="989b0-114">Specifies the access key of the Azure Blob storage account to add.</span></span>

```yaml
Type: System.String
Parameter Sets: Add a Blob storage account
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="989b0-115">-Conta</span><span class="sxs-lookup"><span data-stu-id="989b0-115">-Account</span></span>
<span data-ttu-id="989b0-116">Especifica o nome da conta do data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="989b0-116">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="989b0-117">-Blob</span><span class="sxs-lookup"><span data-stu-id="989b0-117">-Blob</span></span>
<span data-ttu-id="989b0-118">Especifica o nome da conta de armazenamento do blob do Azure a ser adicionada.</span><span class="sxs-lookup"><span data-stu-id="989b0-118">Specifies the name of the Azure Blob Storage account to add.</span></span>

```yaml
Type: System.String
Parameter Sets: Add a Blob storage account
Aliases: AzureBlob

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="989b0-119">-DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="989b0-119">-DataLakeStore</span></span>
<span data-ttu-id="989b0-120">Especifica o nome da conta do Azure data Lake Store a ser adicionada.</span><span class="sxs-lookup"><span data-stu-id="989b0-120">Specifies the name of the Azure Data Lake Store account to add.</span></span>

```yaml
Type: System.String
Parameter Sets: Add a Data Lake storage account
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="989b0-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="989b0-121">-ResourceGroupName</span></span>
<span data-ttu-id="989b0-122">Especifica o nome do grupo de recursos da conta do data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="989b0-122">Specifies the resource group name of the Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="989b0-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="989b0-123">-DefaultProfile</span></span>
<span data-ttu-id="989b0-124">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="989b0-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="989b0-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="989b0-125">CommonParameters</span></span>
<span data-ttu-id="989b0-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="989b0-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="989b0-127">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="989b0-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="989b0-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="989b0-128">INPUTS</span></span>

## <span data-ttu-id="989b0-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="989b0-129">OUTPUTS</span></span>

### <span data-ttu-id="989b0-130">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="989b0-130">None</span></span>

## <span data-ttu-id="989b0-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="989b0-131">NOTES</span></span>

## <span data-ttu-id="989b0-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="989b0-132">RELATED LINKS</span></span>

[<span data-ttu-id="989b0-133">Remove-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="989b0-133">Remove-AzureRmDataLakeAnalyticsDataSource</span></span>](./Remove-AzureRmDataLakeAnalyticsDataSource.md)

[<span data-ttu-id="989b0-134">Set-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="989b0-134">Set-AzureRmDataLakeAnalyticsDataSource</span></span>](./Set-AzureRmDataLakeAnalyticsDataSource.md)



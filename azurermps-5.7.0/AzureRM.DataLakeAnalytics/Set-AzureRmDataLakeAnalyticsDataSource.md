---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 2F28118E-6A34-4261-85BD-8CFDDC8A2707
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/set-azurermdatalakeanalyticsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Set-AzureRmDataLakeAnalyticsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Set-AzureRmDataLakeAnalyticsDataSource.md
ms.openlocfilehash: e873a7f4a825ed84172d098dfa0f8cb631cc3f7f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429814"
---
# <span data-ttu-id="bb3ba-101">Set-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="bb3ba-101">Set-AzureRmDataLakeAnalyticsDataSource</span></span>

## <span data-ttu-id="bb3ba-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bb3ba-102">SYNOPSIS</span></span>
<span data-ttu-id="bb3ba-103">Modifica os detalhes de uma fonte de dados de uma conta do data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="bb3ba-103">Modifies the details of a data source of a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bb3ba-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bb3ba-104">SYNTAX</span></span>

```
Set-AzureRmDataLakeAnalyticsDataSource [-Account] <String> [-Blob] <String> [-AccessKey] <String>
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bb3ba-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="bb3ba-105">DESCRIPTION</span></span>
<span data-ttu-id="bb3ba-106">O cmdlet **set-AzureRmDataLakeAnalyticsDataSource** modifica os detalhes de uma fonte de dados de uma conta do Azure data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="bb3ba-106">The **Set-AzureRmDataLakeAnalyticsDataSource** cmdlet modifies the details of a data source of an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="bb3ba-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bb3ba-107">EXAMPLES</span></span>

### <span data-ttu-id="bb3ba-108">Exemplo 1: alterar a tecla de acesso de uma fonte de dados</span><span class="sxs-lookup"><span data-stu-id="bb3ba-108">Example 1: Change the access key for a data source</span></span>
```
PS C:\>Set-AzureRmDataLakeAnalyticsDataSource -Account "ContosoAdlAccount" -Blob "contosowasb" -AccessKey "...newaccesskey..."
```

<span data-ttu-id="bb3ba-109">Esse comando altera a chave de acesso armazenada para uma fonte de dados de armazenamento do blob do Azure.</span><span class="sxs-lookup"><span data-stu-id="bb3ba-109">This command changes the access key stored for an Azure Blob Storage data source.</span></span>

## <span data-ttu-id="bb3ba-110">OS</span><span class="sxs-lookup"><span data-stu-id="bb3ba-110">PARAMETERS</span></span>

### <span data-ttu-id="bb3ba-111">-AccessKey</span><span class="sxs-lookup"><span data-stu-id="bb3ba-111">-AccessKey</span></span>
<span data-ttu-id="bb3ba-112">Especifica a nova tecla de acesso da fonte de dados de armazenamento do blob do Azure.</span><span class="sxs-lookup"><span data-stu-id="bb3ba-112">Specifies the new access key of the Azure Blob Storage data source.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb3ba-113">-Conta</span><span class="sxs-lookup"><span data-stu-id="bb3ba-113">-Account</span></span>
<span data-ttu-id="bb3ba-114">Especifica o nome da conta do data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="bb3ba-114">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="bb3ba-115">-Blob</span><span class="sxs-lookup"><span data-stu-id="bb3ba-115">-Blob</span></span>
<span data-ttu-id="bb3ba-116">Especifica o nome da fonte de dados de armazenamento do blob do Azure.</span><span class="sxs-lookup"><span data-stu-id="bb3ba-116">Specifies the name of the Azure Blob Storage data source.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AzureBlob

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb3ba-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb3ba-117">-DefaultProfile</span></span>
<span data-ttu-id="bb3ba-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="bb3ba-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bb3ba-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb3ba-119">-ResourceGroupName</span></span>
<span data-ttu-id="bb3ba-120">Especifica o nome do grupo de recursos da conta do data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="bb3ba-120">Specifies the resource group name of the Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="bb3ba-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb3ba-121">CommonParameters</span></span>
<span data-ttu-id="bb3ba-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb3ba-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb3ba-123">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb3ba-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb3ba-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="bb3ba-124">INPUTS</span></span>

### <span data-ttu-id="bb3ba-125">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="bb3ba-125">None</span></span>
<span data-ttu-id="bb3ba-126">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="bb3ba-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="bb3ba-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="bb3ba-127">OUTPUTS</span></span>

### <span data-ttu-id="bb3ba-128">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="bb3ba-128">None</span></span>

## <span data-ttu-id="bb3ba-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="bb3ba-129">NOTES</span></span>

## <span data-ttu-id="bb3ba-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bb3ba-130">RELATED LINKS</span></span>

[<span data-ttu-id="bb3ba-131">Add-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="bb3ba-131">Add-AzureRmDataLakeAnalyticsDataSource</span></span>](./Add-AzureRmDataLakeAnalyticsDataSource.md)

[<span data-ttu-id="bb3ba-132">Remove-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="bb3ba-132">Remove-AzureRmDataLakeAnalyticsDataSource</span></span>](./Remove-AzureRmDataLakeAnalyticsDataSource.md)



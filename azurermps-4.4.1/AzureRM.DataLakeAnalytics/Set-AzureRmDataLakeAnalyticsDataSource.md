---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 2F28118E-6A34-4261-85BD-8CFDDC8A2707
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Set-AzureRmDataLakeAnalyticsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Set-AzureRmDataLakeAnalyticsDataSource.md
ms.openlocfilehash: 258db8a7dc1d771b73ea4c4fa373b1861847b820
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93609710"
---
# <span data-ttu-id="e54bb-101">Set-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="e54bb-101">Set-AzureRmDataLakeAnalyticsDataSource</span></span>

## <span data-ttu-id="e54bb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e54bb-102">SYNOPSIS</span></span>
<span data-ttu-id="e54bb-103">Modifica os detalhes de uma fonte de dados de uma conta do data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="e54bb-103">Modifies the details of a data source of a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e54bb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e54bb-104">SYNTAX</span></span>

```
Set-AzureRmDataLakeAnalyticsDataSource [-Account] <String> [-Blob] <String> [-AccessKey] <String>
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e54bb-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e54bb-105">DESCRIPTION</span></span>
<span data-ttu-id="e54bb-106">O cmdlet **set-AzureRmDataLakeAnalyticsDataSource** modifica os detalhes de uma fonte de dados de uma conta do Azure data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="e54bb-106">The **Set-AzureRmDataLakeAnalyticsDataSource** cmdlet modifies the details of a data source of an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="e54bb-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e54bb-107">EXAMPLES</span></span>

### <span data-ttu-id="e54bb-108">Exemplo 1: alterar a tecla de acesso de uma fonte de dados</span><span class="sxs-lookup"><span data-stu-id="e54bb-108">Example 1: Change the access key for a data source</span></span>
```
PS C:\>Set-AzureRmDataLakeAnalyticsDataSource -Account "ContosoAdlAccount" -Blob "contosowasb" -AccessKey "...newaccesskey..."
```

<span data-ttu-id="e54bb-109">Esse comando altera a chave de acesso armazenada para uma fonte de dados de armazenamento do blob do Azure.</span><span class="sxs-lookup"><span data-stu-id="e54bb-109">This command changes the access key stored for an Azure Blob Storage data source.</span></span>

## <span data-ttu-id="e54bb-110">OS</span><span class="sxs-lookup"><span data-stu-id="e54bb-110">PARAMETERS</span></span>

### <span data-ttu-id="e54bb-111">-AccessKey</span><span class="sxs-lookup"><span data-stu-id="e54bb-111">-AccessKey</span></span>
<span data-ttu-id="e54bb-112">Especifica a nova tecla de acesso da fonte de dados de armazenamento do blob do Azure.</span><span class="sxs-lookup"><span data-stu-id="e54bb-112">Specifies the new access key of the Azure Blob Storage data source.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e54bb-113">-Conta</span><span class="sxs-lookup"><span data-stu-id="e54bb-113">-Account</span></span>
<span data-ttu-id="e54bb-114">Especifica o nome da conta do data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="e54bb-114">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="e54bb-115">-Blob</span><span class="sxs-lookup"><span data-stu-id="e54bb-115">-Blob</span></span>
<span data-ttu-id="e54bb-116">Especifica o nome da fonte de dados de armazenamento do blob do Azure.</span><span class="sxs-lookup"><span data-stu-id="e54bb-116">Specifies the name of the Azure Blob Storage data source.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AzureBlob

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e54bb-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e54bb-117">-ResourceGroupName</span></span>
<span data-ttu-id="e54bb-118">Especifica o nome do grupo de recursos da conta do data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="e54bb-118">Specifies the resource group name of the Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="e54bb-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e54bb-119">-DefaultProfile</span></span>
<span data-ttu-id="e54bb-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e54bb-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e54bb-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e54bb-121">CommonParameters</span></span>
<span data-ttu-id="e54bb-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e54bb-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e54bb-123">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e54bb-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e54bb-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e54bb-124">INPUTS</span></span>

## <span data-ttu-id="e54bb-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e54bb-125">OUTPUTS</span></span>

### <span data-ttu-id="e54bb-126">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="e54bb-126">None</span></span>

## <span data-ttu-id="e54bb-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e54bb-127">NOTES</span></span>

## <span data-ttu-id="e54bb-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e54bb-128">RELATED LINKS</span></span>

[<span data-ttu-id="e54bb-129">Add-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="e54bb-129">Add-AzureRmDataLakeAnalyticsDataSource</span></span>](./Add-AzureRmDataLakeAnalyticsDataSource.md)

[<span data-ttu-id="e54bb-130">Remove-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="e54bb-130">Remove-AzureRmDataLakeAnalyticsDataSource</span></span>](./Remove-AzureRmDataLakeAnalyticsDataSource.md)



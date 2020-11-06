---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: 2F28118E-6A34-4261-85BD-8CFDDC8A2707
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/set-azdatalakeanalyticsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Set-AzDataLakeAnalyticsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Set-AzDataLakeAnalyticsDataSource.md
ms.openlocfilehash: 8fece6d480ee2210ff66256e02baaf6a11f9c1f9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93596887"
---
# <span data-ttu-id="49ff6-101">Set-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="49ff6-101">Set-AzDataLakeAnalyticsDataSource</span></span>

## <span data-ttu-id="49ff6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="49ff6-102">SYNOPSIS</span></span>
<span data-ttu-id="49ff6-103">Modifica os detalhes de uma fonte de dados de uma conta do data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="49ff6-103">Modifies the details of a data source of a Data Lake Analytics account.</span></span>

## <span data-ttu-id="49ff6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="49ff6-104">SYNTAX</span></span>

```
Set-AzDataLakeAnalyticsDataSource [-Account] <String> [-Blob] <String> [-AccessKey] <String>
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="49ff6-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="49ff6-105">DESCRIPTION</span></span>
<span data-ttu-id="49ff6-106">O cmdlet **set-AzDataLakeAnalyticsDataSource** modifica os detalhes de uma fonte de dados de uma conta do Azure data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="49ff6-106">The **Set-AzDataLakeAnalyticsDataSource** cmdlet modifies the details of a data source of an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="49ff6-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="49ff6-107">EXAMPLES</span></span>

### <span data-ttu-id="49ff6-108">Exemplo 1: alterar a tecla de acesso de uma fonte de dados</span><span class="sxs-lookup"><span data-stu-id="49ff6-108">Example 1: Change the access key for a data source</span></span>
```
PS C:\>Set-AzDataLakeAnalyticsDataSource -Account "ContosoAdlAccount" -Blob "contosowasb" -AccessKey "...newaccesskey..."
```

<span data-ttu-id="49ff6-109">Esse comando altera a chave de acesso armazenada para uma fonte de dados de armazenamento do blob do Azure.</span><span class="sxs-lookup"><span data-stu-id="49ff6-109">This command changes the access key stored for an Azure Blob Storage data source.</span></span>

## <span data-ttu-id="49ff6-110">OS</span><span class="sxs-lookup"><span data-stu-id="49ff6-110">PARAMETERS</span></span>

### <span data-ttu-id="49ff6-111">-AccessKey</span><span class="sxs-lookup"><span data-stu-id="49ff6-111">-AccessKey</span></span>
<span data-ttu-id="49ff6-112">Especifica a nova tecla de acesso da fonte de dados de armazenamento do blob do Azure.</span><span class="sxs-lookup"><span data-stu-id="49ff6-112">Specifies the new access key of the Azure Blob Storage data source.</span></span>

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

### <span data-ttu-id="49ff6-113">-Conta</span><span class="sxs-lookup"><span data-stu-id="49ff6-113">-Account</span></span>
<span data-ttu-id="49ff6-114">Especifica o nome da conta do data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="49ff6-114">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="49ff6-115">-Blob</span><span class="sxs-lookup"><span data-stu-id="49ff6-115">-Blob</span></span>
<span data-ttu-id="49ff6-116">Especifica o nome da fonte de dados de armazenamento do blob do Azure.</span><span class="sxs-lookup"><span data-stu-id="49ff6-116">Specifies the name of the Azure Blob Storage data source.</span></span>

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

### <span data-ttu-id="49ff6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49ff6-117">-DefaultProfile</span></span>
<span data-ttu-id="49ff6-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="49ff6-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="49ff6-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49ff6-119">-ResourceGroupName</span></span>
<span data-ttu-id="49ff6-120">Especifica o nome do grupo de recursos da conta do data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="49ff6-120">Specifies the resource group name of the Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="49ff6-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49ff6-121">CommonParameters</span></span>
<span data-ttu-id="49ff6-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49ff6-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49ff6-123">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49ff6-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49ff6-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="49ff6-124">INPUTS</span></span>

### <span data-ttu-id="49ff6-125">System. String</span><span class="sxs-lookup"><span data-stu-id="49ff6-125">System.String</span></span>

## <span data-ttu-id="49ff6-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="49ff6-126">OUTPUTS</span></span>

### <span data-ttu-id="49ff6-127">System. void</span><span class="sxs-lookup"><span data-stu-id="49ff6-127">System.Void</span></span>

## <span data-ttu-id="49ff6-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="49ff6-128">NOTES</span></span>

## <span data-ttu-id="49ff6-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="49ff6-129">RELATED LINKS</span></span>

[<span data-ttu-id="49ff6-130">Add-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="49ff6-130">Add-AzDataLakeAnalyticsDataSource</span></span>](./Add-AzDataLakeAnalyticsDataSource.md)

[<span data-ttu-id="49ff6-131">Remove-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="49ff6-131">Remove-AzDataLakeAnalyticsDataSource</span></span>](./Remove-AzDataLakeAnalyticsDataSource.md)



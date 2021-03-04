---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: 2F28118E-6A34-4261-85BD-8CFDDC8A2707
online version: https://docs.microsoft.com/powershell/module/az.datalakeanalytics/set-azdatalakeanalyticsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Set-AzDataLakeAnalyticsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Set-AzDataLakeAnalyticsDataSource.md
ms.openlocfilehash: cb51b1c703d527a2888bd0e80d8cc7a50d044e36
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886682"
---
# <span data-ttu-id="259a1-101">Set-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="259a1-101">Set-AzDataLakeAnalyticsDataSource</span></span>

## <span data-ttu-id="259a1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="259a1-102">SYNOPSIS</span></span>
<span data-ttu-id="259a1-103">Modifica os detalhes de uma fonte de dados de uma conta do Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="259a1-103">Modifies the details of a data source of a Data Lake Analytics account.</span></span>

## <span data-ttu-id="259a1-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="259a1-104">SYNTAX</span></span>

```
Set-AzDataLakeAnalyticsDataSource [-Account] <String> [-Blob] <String> [-AccessKey] <String>
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="259a1-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="259a1-105">DESCRIPTION</span></span>
<span data-ttu-id="259a1-106">O cmdlet **Set-AzDataLakeAnalyticsDataSource** modifica os detalhes de uma fonte de dados de uma conta do Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="259a1-106">The **Set-AzDataLakeAnalyticsDataSource** cmdlet modifies the details of a data source of an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="259a1-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="259a1-107">EXAMPLES</span></span>

### <span data-ttu-id="259a1-108">Exemplo 1: Alterar a chave de acesso para uma fonte de dados</span><span class="sxs-lookup"><span data-stu-id="259a1-108">Example 1: Change the access key for a data source</span></span>
```
PS C:\>Set-AzDataLakeAnalyticsDataSource -Account "ContosoAdlAccount" -Blob "contosowasb" -AccessKey "...newaccesskey..."
```

<span data-ttu-id="259a1-109">Este comando altera a chave de acesso armazenada para uma fonte de dados de Armazenamento de Blob do Azure.</span><span class="sxs-lookup"><span data-stu-id="259a1-109">This command changes the access key stored for an Azure Blob Storage data source.</span></span>

## <span data-ttu-id="259a1-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="259a1-110">PARAMETERS</span></span>

### <span data-ttu-id="259a1-111">-AccessKey</span><span class="sxs-lookup"><span data-stu-id="259a1-111">-AccessKey</span></span>
<span data-ttu-id="259a1-112">Especifica a nova chave de acesso da fonte de dados de Armazenamento de Blob do Azure.</span><span class="sxs-lookup"><span data-stu-id="259a1-112">Specifies the new access key of the Azure Blob Storage data source.</span></span>

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

### <span data-ttu-id="259a1-113">-Account</span><span class="sxs-lookup"><span data-stu-id="259a1-113">-Account</span></span>
<span data-ttu-id="259a1-114">Especifica o nome da conta do Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="259a1-114">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="259a1-115">-Blob</span><span class="sxs-lookup"><span data-stu-id="259a1-115">-Blob</span></span>
<span data-ttu-id="259a1-116">Especifica o nome da fonte de dados armazenamento de blob do Azure.</span><span class="sxs-lookup"><span data-stu-id="259a1-116">Specifies the name of the Azure Blob Storage data source.</span></span>

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

### <span data-ttu-id="259a1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="259a1-117">-DefaultProfile</span></span>
<span data-ttu-id="259a1-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="259a1-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="259a1-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="259a1-119">-ResourceGroupName</span></span>
<span data-ttu-id="259a1-120">Especifica o nome do grupo de recursos da conta do Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="259a1-120">Specifies the resource group name of the Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="259a1-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="259a1-121">CommonParameters</span></span>
<span data-ttu-id="259a1-122">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="259a1-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="259a1-123">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="259a1-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="259a1-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="259a1-124">INPUTS</span></span>

### <span data-ttu-id="259a1-125">System.String</span><span class="sxs-lookup"><span data-stu-id="259a1-125">System.String</span></span>

## <span data-ttu-id="259a1-126">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="259a1-126">OUTPUTS</span></span>

### <span data-ttu-id="259a1-127">System.Void</span><span class="sxs-lookup"><span data-stu-id="259a1-127">System.Void</span></span>

## <span data-ttu-id="259a1-128">NOTES</span><span class="sxs-lookup"><span data-stu-id="259a1-128">NOTES</span></span>

## <span data-ttu-id="259a1-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="259a1-129">RELATED LINKS</span></span>

[<span data-ttu-id="259a1-130">Add-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="259a1-130">Add-AzDataLakeAnalyticsDataSource</span></span>](./Add-AzDataLakeAnalyticsDataSource.md)

[<span data-ttu-id="259a1-131">Remove-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="259a1-131">Remove-AzDataLakeAnalyticsDataSource</span></span>](./Remove-AzDataLakeAnalyticsDataSource.md)



---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: 2F28118E-6A34-4261-85BD-8CFDDC8A2707
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/set-azdatalakeanalyticsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Set-AzDataLakeAnalyticsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Set-AzDataLakeAnalyticsDataSource.md
ms.openlocfilehash: 0dd0dfb25959ed3a5753ae6bd19b0500d4742634
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115404"
---
# <span data-ttu-id="203da-101">Set-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="203da-101">Set-AzDataLakeAnalyticsDataSource</span></span>

## <span data-ttu-id="203da-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="203da-102">SYNOPSIS</span></span>
<span data-ttu-id="203da-103">Modifica os detalhes de uma fonte de dados de uma conta do Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="203da-103">Modifies the details of a data source of a Data Lake Analytics account.</span></span>

## <span data-ttu-id="203da-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="203da-104">SYNTAX</span></span>

```
Set-AzDataLakeAnalyticsDataSource [-Account] <String> [-Blob] <String> [-AccessKey] <String>
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="203da-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="203da-105">DESCRIPTION</span></span>
<span data-ttu-id="203da-106">O cmdlet **Set-AzDataLakeAnalyticsDataSource** modifica os detalhes de uma fonte de dados de uma conta do Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="203da-106">The **Set-AzDataLakeAnalyticsDataSource** cmdlet modifies the details of a data source of an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="203da-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="203da-107">EXAMPLES</span></span>

### <span data-ttu-id="203da-108">Exemplo 1: Alterar a chave de acesso de uma fonte de dados</span><span class="sxs-lookup"><span data-stu-id="203da-108">Example 1: Change the access key for a data source</span></span>
```
PS C:\>Set-AzDataLakeAnalyticsDataSource -Account "ContosoAdlAccount" -Blob "contosowasb" -AccessKey "...newaccesskey..."
```

<span data-ttu-id="203da-109">Esse comando altera a chave de acesso armazenada para uma fonte de dados de Armazenamento de Blob do Azure.</span><span class="sxs-lookup"><span data-stu-id="203da-109">This command changes the access key stored for an Azure Blob Storage data source.</span></span>

## <span data-ttu-id="203da-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="203da-110">PARAMETERS</span></span>

### <span data-ttu-id="203da-111">-AccessKey</span><span class="sxs-lookup"><span data-stu-id="203da-111">-AccessKey</span></span>
<span data-ttu-id="203da-112">Especifica a nova chave de acesso da fonte de dados Armazenamento de Blob do Azure.</span><span class="sxs-lookup"><span data-stu-id="203da-112">Specifies the new access key of the Azure Blob Storage data source.</span></span>

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

### <span data-ttu-id="203da-113">-Conta</span><span class="sxs-lookup"><span data-stu-id="203da-113">-Account</span></span>
<span data-ttu-id="203da-114">Especifica o nome da conta do Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="203da-114">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="203da-115">-Blob</span><span class="sxs-lookup"><span data-stu-id="203da-115">-Blob</span></span>
<span data-ttu-id="203da-116">Especifica o nome da fonte de dados Armazenamento de Blob do Azure.</span><span class="sxs-lookup"><span data-stu-id="203da-116">Specifies the name of the Azure Blob Storage data source.</span></span>

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

### <span data-ttu-id="203da-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="203da-117">-DefaultProfile</span></span>
<span data-ttu-id="203da-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="203da-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="203da-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="203da-119">-ResourceGroupName</span></span>
<span data-ttu-id="203da-120">Especifica o nome do grupo de recursos da conta do Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="203da-120">Specifies the resource group name of the Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="203da-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="203da-121">CommonParameters</span></span>
<span data-ttu-id="203da-122">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="203da-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="203da-123">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="203da-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="203da-124">Entradas</span><span class="sxs-lookup"><span data-stu-id="203da-124">INPUTS</span></span>

### <span data-ttu-id="203da-125">System.String</span><span class="sxs-lookup"><span data-stu-id="203da-125">System.String</span></span>

## <span data-ttu-id="203da-126">Saídas</span><span class="sxs-lookup"><span data-stu-id="203da-126">OUTPUTS</span></span>

### <span data-ttu-id="203da-127">System.Void</span><span class="sxs-lookup"><span data-stu-id="203da-127">System.Void</span></span>

## <span data-ttu-id="203da-128">Notas</span><span class="sxs-lookup"><span data-stu-id="203da-128">NOTES</span></span>

## <span data-ttu-id="203da-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="203da-129">RELATED LINKS</span></span>

[<span data-ttu-id="203da-130">Add-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="203da-130">Add-AzDataLakeAnalyticsDataSource</span></span>](./Add-AzDataLakeAnalyticsDataSource.md)

[<span data-ttu-id="203da-131">Remove-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="203da-131">Remove-AzDataLakeAnalyticsDataSource</span></span>](./Remove-AzDataLakeAnalyticsDataSource.md)



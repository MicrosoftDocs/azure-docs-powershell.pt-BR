---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticsjobpipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsJobPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsJobPipeline.md
ms.openlocfilehash: 1d13d1b6e55831c972457c5a6a5aadc427ecb3a6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111949"
---
# <span data-ttu-id="44dc0-101">Get-AzDataLakeAnalyticsJobPipeline</span><span class="sxs-lookup"><span data-stu-id="44dc0-101">Get-AzDataLakeAnalyticsJobPipeline</span></span>

## <span data-ttu-id="44dc0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="44dc0-102">SYNOPSIS</span></span>
<span data-ttu-id="44dc0-103">Obtém pipelines ou pipelines de trabalho do Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="44dc0-103">Gets a Data Lake Analytics Job pipeline or pipelines.</span></span>

## <span data-ttu-id="44dc0-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="44dc0-104">SYNTAX</span></span>

### <span data-ttu-id="44dc0-105">GetAllInAccount (Padrão)</span><span class="sxs-lookup"><span data-stu-id="44dc0-105">GetAllInAccount (Default)</span></span>
```
Get-AzDataLakeAnalyticsJobPipeline [-Account] <String> [-SubmittedAfter <DateTimeOffset>]
 [-SubmittedBefore <DateTimeOffset>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="44dc0-106">GetBySpecificJobJobline</span><span class="sxs-lookup"><span data-stu-id="44dc0-106">GetBySpecificJobPipeline</span></span>
```
Get-AzDataLakeAnalyticsJobPipeline [-Account] <String> [-PipelineId] <Guid> [-SubmittedAfter <DateTimeOffset>]
 [-SubmittedBefore <DateTimeOffset>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="44dc0-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="44dc0-107">DESCRIPTION</span></span>
<span data-ttu-id="44dc0-108">O **Get-AzDataLakeAnalytics Job Pipeline do** Azure Data Lake Analytics obtém um pipeline especificado do Azure Data Lake Analytics ou uma lista de pipelines.</span><span class="sxs-lookup"><span data-stu-id="44dc0-108">The **Get-AzDataLakeAnalyticsJobPipeline** gets a specified Azure Data Lake Analytics Job pipeline or a list of pipelines.</span></span>

## <span data-ttu-id="44dc0-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="44dc0-109">EXAMPLES</span></span>

### <span data-ttu-id="44dc0-110">Exemplo 1: Obter um pipeline especificado</span><span class="sxs-lookup"><span data-stu-id="44dc0-110">Example 1: Get a specified pipeline</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsJobPipeline -Account "contosoadla" -PipelineId 83cb7ad2-3523-4b82-b909-d478b0d8aea3
```

<span data-ttu-id="44dc0-111">Este comando obtém o pipeline especificado com a id '83cb7ad2-3523-4b82-b909-d478b0d8aea3' na conta "contosoadla".</span><span class="sxs-lookup"><span data-stu-id="44dc0-111">This command gets the specified pipeline with id '83cb7ad2-3523-4b82-b909-d478b0d8aea3' in account 'contosoadla'.</span></span>

### <span data-ttu-id="44dc0-112">Exemplo 2: Obter uma lista de todos os pipelines na conta</span><span class="sxs-lookup"><span data-stu-id="44dc0-112">Example 2: Get a list of all pipelines in the account</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsJobPipeline -AccountName "contosoadla"
```

<span data-ttu-id="44dc0-113">Este comando obtém uma lista de todos os pipelines na conta "contosoadla"</span><span class="sxs-lookup"><span data-stu-id="44dc0-113">This command gets a list of all pipelines in the account "contosoadla"</span></span>

## <span data-ttu-id="44dc0-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="44dc0-114">PARAMETERS</span></span>

### <span data-ttu-id="44dc0-115">-Conta</span><span class="sxs-lookup"><span data-stu-id="44dc0-115">-Account</span></span>
<span data-ttu-id="44dc0-116">Nome do nome da conta do Data Lake Analytics sob o qual deseja recuperar o pipeline de trabalho.</span><span class="sxs-lookup"><span data-stu-id="44dc0-116">Name of the Data Lake Analytics account name under which want to retrieve the job pipeline.</span></span>

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

### <span data-ttu-id="44dc0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44dc0-117">-DefaultProfile</span></span>
<span data-ttu-id="44dc0-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="44dc0-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="44dc0-119">-PipelineId</span><span class="sxs-lookup"><span data-stu-id="44dc0-119">-PipelineId</span></span>
<span data-ttu-id="44dc0-120">ID do pipeline de trabalho específico para o que retornar informações.</span><span class="sxs-lookup"><span data-stu-id="44dc0-120">ID of the specific job pipeline to return information for.</span></span>

```yaml
Type: System.Guid
Parameter Sets: GetBySpecificJobPipeline
Aliases: Id

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="44dc0-121">-SubmittedAfter</span><span class="sxs-lookup"><span data-stu-id="44dc0-121">-SubmittedAfter</span></span>
<span data-ttu-id="44dc0-122">Um filtro opcional que retorna pipelines de trabalho enviados somente após o tempo especificado.</span><span class="sxs-lookup"><span data-stu-id="44dc0-122">An optional filter which returns job pipeline(s) only submitted after the specified time.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44dc0-123">-SubmittedBefore</span><span class="sxs-lookup"><span data-stu-id="44dc0-123">-SubmittedBefore</span></span>
<span data-ttu-id="44dc0-124">Um filtro opcional que retorna pipelines de trabalho enviados somente antes do tempo especificado.</span><span class="sxs-lookup"><span data-stu-id="44dc0-124">An optional filter which returns job pipeline(s) only submitted before the specified time.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44dc0-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44dc0-125">CommonParameters</span></span>
<span data-ttu-id="44dc0-126">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44dc0-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44dc0-127">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="44dc0-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44dc0-128">Entradas</span><span class="sxs-lookup"><span data-stu-id="44dc0-128">INPUTS</span></span>

### <span data-ttu-id="44dc0-129">System.String</span><span class="sxs-lookup"><span data-stu-id="44dc0-129">System.String</span></span>

### <span data-ttu-id="44dc0-130">System.Guid</span><span class="sxs-lookup"><span data-stu-id="44dc0-130">System.Guid</span></span>

### <span data-ttu-id="44dc0-131">System.Nullable'1[[System.DateTimeOffset, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="44dc0-131">System.Nullable\`1[[System.DateTimeOffset, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="44dc0-132">Saídas</span><span class="sxs-lookup"><span data-stu-id="44dc0-132">OUTPUTS</span></span>

### <span data-ttu-id="44dc0-133">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSJobJoblineInformation</span><span class="sxs-lookup"><span data-stu-id="44dc0-133">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSJobPipelineInformation</span></span>

## <span data-ttu-id="44dc0-134">Notas</span><span class="sxs-lookup"><span data-stu-id="44dc0-134">NOTES</span></span>

## <span data-ttu-id="44dc0-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="44dc0-135">RELATED LINKS</span></span>

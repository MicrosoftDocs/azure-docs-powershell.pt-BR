---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: CE7B54BC-C493-49CE-93BD-346ED0B966A1
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/wait-azdatalakeanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Wait-AzDataLakeAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Wait-AzDataLakeAnalyticsJob.md
ms.openlocfilehash: 047d0c7c9b141f10ee3f1be2ba1e739960f2e5bc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115395"
---
# <span data-ttu-id="f3c58-101">Wait-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="f3c58-101">Wait-AzDataLakeAnalyticsJob</span></span>

## <span data-ttu-id="f3c58-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f3c58-102">SYNOPSIS</span></span>
<span data-ttu-id="f3c58-103">Aguarda a conclusão de um trabalho.</span><span class="sxs-lookup"><span data-stu-id="f3c58-103">Waits for a job to complete.</span></span>

## <span data-ttu-id="f3c58-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f3c58-104">SYNTAX</span></span>

```
Wait-AzDataLakeAnalyticsJob [-Account] <String> [-JobId] <Guid> [[-WaitIntervalInSeconds] <Int32>]
 [[-TimeoutInSeconds] <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f3c58-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="f3c58-105">DESCRIPTION</span></span>
<span data-ttu-id="f3c58-106">O cmdlet **Wait-AzDataLakeAnalytics Job** aguarda a conclusão de um trabalho do Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="f3c58-106">The **Wait-AzDataLakeAnalyticsJob** cmdlet waits for an Azure Data Lake Analytics job to complete.</span></span>

## <span data-ttu-id="f3c58-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f3c58-107">EXAMPLES</span></span>

### <span data-ttu-id="f3c58-108">Exemplo 1: Aguarde a conclusão de um trabalho</span><span class="sxs-lookup"><span data-stu-id="f3c58-108">Example 1: Wait for a job to complete</span></span>
```
PS C:\>Wait-AzDataLakeAnalyticsJob -Account "ContosoAdlAccount" -JobId "a0a78d72-3fa8-4564-9b18-6becb3fda48a"
```

<span data-ttu-id="f3c58-109">O comando a seguir aguarda a conclusão do trabalho com a ID especificada.</span><span class="sxs-lookup"><span data-stu-id="f3c58-109">The following command waits for the job with the specified ID to complete.</span></span>

## <span data-ttu-id="f3c58-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f3c58-110">PARAMETERS</span></span>

### <span data-ttu-id="f3c58-111">-Conta</span><span class="sxs-lookup"><span data-stu-id="f3c58-111">-Account</span></span>
<span data-ttu-id="f3c58-112">Especifica o nome da conta do Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="f3c58-112">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="f3c58-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3c58-113">-DefaultProfile</span></span>
<span data-ttu-id="f3c58-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="f3c58-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f3c58-115">-JobId</span><span class="sxs-lookup"><span data-stu-id="f3c58-115">-JobId</span></span>
<span data-ttu-id="f3c58-116">Especifica a ID do trabalho para o qual aguardar.</span><span class="sxs-lookup"><span data-stu-id="f3c58-116">Specifies the ID of the job for which to wait.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f3c58-117">-TimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="f3c58-117">-TimeoutInSeconds</span></span>
<span data-ttu-id="f3c58-118">Especifica o número de segundos a esperar antes de sair da operação de espera.</span><span class="sxs-lookup"><span data-stu-id="f3c58-118">Specifies the number of seconds to wait before exiting the wait operation.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3c58-119">-WaitIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="f3c58-119">-WaitIntervalInSeconds</span></span>
<span data-ttu-id="f3c58-120">Especifique o número de segundos que se verifica entre cada verificação do estado do trabalho.</span><span class="sxs-lookup"><span data-stu-id="f3c58-120">Specify the number of seconds that elapse between each check of the job state.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3c58-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3c58-121">CommonParameters</span></span>
<span data-ttu-id="f3c58-122">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3c58-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3c58-123">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3c58-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3c58-124">Entradas</span><span class="sxs-lookup"><span data-stu-id="f3c58-124">INPUTS</span></span>

### <span data-ttu-id="f3c58-125">System.String</span><span class="sxs-lookup"><span data-stu-id="f3c58-125">System.String</span></span>

### <span data-ttu-id="f3c58-126">System.Guid</span><span class="sxs-lookup"><span data-stu-id="f3c58-126">System.Guid</span></span>

### <span data-ttu-id="f3c58-127">System.Int32</span><span class="sxs-lookup"><span data-stu-id="f3c58-127">System.Int32</span></span>

## <span data-ttu-id="f3c58-128">Saídas</span><span class="sxs-lookup"><span data-stu-id="f3c58-128">OUTPUTS</span></span>

### <span data-ttu-id="f3c58-129">Microsoft.Azure.Management.DataLake.Analytics.Models.JobInformation</span><span class="sxs-lookup"><span data-stu-id="f3c58-129">Microsoft.Azure.Management.DataLake.Analytics.Models.JobInformation</span></span>

## <span data-ttu-id="f3c58-130">Notas</span><span class="sxs-lookup"><span data-stu-id="f3c58-130">NOTES</span></span>

## <span data-ttu-id="f3c58-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f3c58-131">RELATED LINKS</span></span>

[<span data-ttu-id="f3c58-132">Get-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="f3c58-132">Get-AzDataLakeAnalyticsJob</span></span>](./Get-AzDataLakeAnalyticsJob.md)

[<span data-ttu-id="f3c58-133">Stop-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="f3c58-133">Stop-AzDataLakeAnalyticsJob</span></span>](./Stop-AzDataLakeAnalyticsJob.md)

[<span data-ttu-id="f3c58-134">Submit-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="f3c58-134">Submit-AzDataLakeAnalyticsJob</span></span>](./Submit-AzDataLakeAnalyticsJob.md)



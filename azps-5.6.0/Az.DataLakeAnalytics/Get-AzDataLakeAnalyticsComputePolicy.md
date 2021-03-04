---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticscomputepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsComputePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsComputePolicy.md
ms.openlocfilehash: 6867e57e5465ddab8fc7f0adbfdb3197d8ac1245
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891435"
---
# <span data-ttu-id="74b00-101">Get-AzDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="74b00-101">Get-AzDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="74b00-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="74b00-102">SYNOPSIS</span></span>
<span data-ttu-id="74b00-103">Obtém uma política de computação do Data Lake Analytics ou uma lista de políticas de computação.</span><span class="sxs-lookup"><span data-stu-id="74b00-103">Gets a Data Lake Analytics compute policy or list of compute policies.</span></span>

## <span data-ttu-id="74b00-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="74b00-104">SYNTAX</span></span>

```
Get-AzDataLakeAnalyticsComputePolicy [-ResourceGroupName <String>] [-Account] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="74b00-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="74b00-105">DESCRIPTION</span></span>
<span data-ttu-id="74b00-106">**Get-AzDataLakeAnalyticsComputePolicy** obtém uma política de computação do Azure Data Lake Analytics especificada ou uma lista de políticas.</span><span class="sxs-lookup"><span data-stu-id="74b00-106">The **Get-AzDataLakeAnalyticsComputePolicy** gets a specified Azure Data Lake Analytics compute policy or a list of policies.</span></span>

## <span data-ttu-id="74b00-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="74b00-107">EXAMPLES</span></span>

### <span data-ttu-id="74b00-108">Exemplo 1: Obter uma política de computação especificada</span><span class="sxs-lookup"><span data-stu-id="74b00-108">Example 1: Get a specified compute policy</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name myPolicy
```

<span data-ttu-id="74b00-109">Este comando obtém a política de computação especificada com o nome 'myPolicy' na conta 'contosoadla'.</span><span class="sxs-lookup"><span data-stu-id="74b00-109">This command gets the specified compute policy with name 'myPolicy' in account 'contosoadla'.</span></span>

### <span data-ttu-id="74b00-110">Exemplo 2: Obter uma lista de todas as políticas de computação na conta</span><span class="sxs-lookup"><span data-stu-id="74b00-110">Example 2: Get a list of all compute policies in the account</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsComputePolicy -AccountName "contosoadla"
```

<span data-ttu-id="74b00-111">Este comando obtém uma lista de todas as políticas de computação na conta "contosoadla"</span><span class="sxs-lookup"><span data-stu-id="74b00-111">This command gets a list of all compute policies in the account "contosoadla"</span></span>

## <span data-ttu-id="74b00-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="74b00-112">PARAMETERS</span></span>

### <span data-ttu-id="74b00-113">-Account</span><span class="sxs-lookup"><span data-stu-id="74b00-113">-Account</span></span>
<span data-ttu-id="74b00-114">Nome da conta para obter a política de computação ou políticas.</span><span class="sxs-lookup"><span data-stu-id="74b00-114">Name of the account to get the compute policy or policies from.</span></span>

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

### <span data-ttu-id="74b00-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74b00-115">-DefaultProfile</span></span>
<span data-ttu-id="74b00-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="74b00-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="74b00-117">-Name</span><span class="sxs-lookup"><span data-stu-id="74b00-117">-Name</span></span>
<span data-ttu-id="74b00-118">Nome da política de computação a ser obter.</span><span class="sxs-lookup"><span data-stu-id="74b00-118">Name of the compute policy to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ComputePolicyName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74b00-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74b00-119">-ResourceGroupName</span></span>
<span data-ttu-id="74b00-120">Nome do grupo de recursos no qual você a conta existe.</span><span class="sxs-lookup"><span data-stu-id="74b00-120">Name of resource group under which you the account exists.</span></span>
<span data-ttu-id="74b00-121">Opcional e tentará descobrir se não for fornecido.</span><span class="sxs-lookup"><span data-stu-id="74b00-121">Optional and will attempt to discover if not provided.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74b00-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74b00-122">CommonParameters</span></span>
<span data-ttu-id="74b00-123">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74b00-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74b00-124">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="74b00-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74b00-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="74b00-125">INPUTS</span></span>

### <span data-ttu-id="74b00-126">System.String</span><span class="sxs-lookup"><span data-stu-id="74b00-126">System.String</span></span>

## <span data-ttu-id="74b00-127">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="74b00-127">OUTPUTS</span></span>

### <span data-ttu-id="74b00-128">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="74b00-128">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="74b00-129">NOTES</span><span class="sxs-lookup"><span data-stu-id="74b00-129">NOTES</span></span>

## <span data-ttu-id="74b00-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="74b00-130">RELATED LINKS</span></span>

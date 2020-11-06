---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticscomputepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsComputePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsComputePolicy.md
ms.openlocfilehash: 776249a7a474e3918ed29003f631c984111ca25c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93596923"
---
# <span data-ttu-id="db6f1-101">Get-AzDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="db6f1-101">Get-AzDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="db6f1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="db6f1-102">SYNOPSIS</span></span>
<span data-ttu-id="db6f1-103">Obtém uma política de computação de análise de data Lake ou uma lista de políticas de computação.</span><span class="sxs-lookup"><span data-stu-id="db6f1-103">Gets a Data Lake Analytics compute policy or list of compute policies.</span></span>

## <span data-ttu-id="db6f1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="db6f1-104">SYNTAX</span></span>

```
Get-AzDataLakeAnalyticsComputePolicy [-ResourceGroupName <String>] [-Account] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="db6f1-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="db6f1-105">DESCRIPTION</span></span>
<span data-ttu-id="db6f1-106">**Get-AzDataLakeAnalyticsComputePolicy** Obtém uma política de computação do Azure data Lake Analytics especificada ou uma lista de políticas.</span><span class="sxs-lookup"><span data-stu-id="db6f1-106">The **Get-AzDataLakeAnalyticsComputePolicy** gets a specified Azure Data Lake Analytics compute policy or a list of policies.</span></span>

## <span data-ttu-id="db6f1-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="db6f1-107">EXAMPLES</span></span>

### <span data-ttu-id="db6f1-108">Exemplo 1: obter uma política de computação especificada</span><span class="sxs-lookup"><span data-stu-id="db6f1-108">Example 1: Get a specified compute policy</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name myPolicy
```

<span data-ttu-id="db6f1-109">Este comando obtém a política de computação especificada com o nome ' MyPolicy ' na conta ' contosoadla '.</span><span class="sxs-lookup"><span data-stu-id="db6f1-109">This command gets the specified compute policy with name 'myPolicy' in account 'contosoadla'.</span></span>

### <span data-ttu-id="db6f1-110">Exemplo 2: obter uma lista de todas as políticas de computação na conta</span><span class="sxs-lookup"><span data-stu-id="db6f1-110">Example 2: Get a list of all compute policies in the account</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsComputePolicy -AccountName "contosoadla"
```

<span data-ttu-id="db6f1-111">Este comando obtém uma lista de todas as políticas de computação na conta "contosoadla"</span><span class="sxs-lookup"><span data-stu-id="db6f1-111">This command gets a list of all compute policies in the account "contosoadla"</span></span>

## <span data-ttu-id="db6f1-112">OS</span><span class="sxs-lookup"><span data-stu-id="db6f1-112">PARAMETERS</span></span>

### <span data-ttu-id="db6f1-113">-Conta</span><span class="sxs-lookup"><span data-stu-id="db6f1-113">-Account</span></span>
<span data-ttu-id="db6f1-114">Nome da conta da qual você deseja obter a política ou políticas de computação.</span><span class="sxs-lookup"><span data-stu-id="db6f1-114">Name of the account to get the compute policy or policies from.</span></span>

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

### <span data-ttu-id="db6f1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db6f1-115">-DefaultProfile</span></span>
<span data-ttu-id="db6f1-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="db6f1-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="db6f1-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="db6f1-117">-Name</span></span>
<span data-ttu-id="db6f1-118">Nome da política de computação a ser obtida.</span><span class="sxs-lookup"><span data-stu-id="db6f1-118">Name of the compute policy to get.</span></span>

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

### <span data-ttu-id="db6f1-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db6f1-119">-ResourceGroupName</span></span>
<span data-ttu-id="db6f1-120">Nome do grupo de recursos sob o qual a conta existe.</span><span class="sxs-lookup"><span data-stu-id="db6f1-120">Name of resource group under which you the account exists.</span></span>
<span data-ttu-id="db6f1-121">Opcional e tentará descobrir, se não for fornecido.</span><span class="sxs-lookup"><span data-stu-id="db6f1-121">Optional and will attempt to discover if not provided.</span></span>

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

### <span data-ttu-id="db6f1-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db6f1-122">CommonParameters</span></span>
<span data-ttu-id="db6f1-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db6f1-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db6f1-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db6f1-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db6f1-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="db6f1-125">INPUTS</span></span>

### <span data-ttu-id="db6f1-126">System. String</span><span class="sxs-lookup"><span data-stu-id="db6f1-126">System.String</span></span>

## <span data-ttu-id="db6f1-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="db6f1-127">OUTPUTS</span></span>

### <span data-ttu-id="db6f1-128">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="db6f1-128">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="db6f1-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="db6f1-129">NOTES</span></span>

## <span data-ttu-id="db6f1-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="db6f1-130">RELATED LINKS</span></span>

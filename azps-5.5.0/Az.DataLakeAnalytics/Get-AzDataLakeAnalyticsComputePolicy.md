---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticscomputepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsComputePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsComputePolicy.md
ms.openlocfilehash: 56b1a9378914a7fa2220e948b64c357b06f6f4dc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118800"
---
# <span data-ttu-id="91d3f-101">Get-AzDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="91d3f-101">Get-AzDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="91d3f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="91d3f-102">SYNOPSIS</span></span>
<span data-ttu-id="91d3f-103">Obtém uma política de computação do Data Lake Analytics ou uma lista de políticas de computação.</span><span class="sxs-lookup"><span data-stu-id="91d3f-103">Gets a Data Lake Analytics compute policy or list of compute policies.</span></span>

## <span data-ttu-id="91d3f-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="91d3f-104">SYNTAX</span></span>

```
Get-AzDataLakeAnalyticsComputePolicy [-ResourceGroupName <String>] [-Account] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="91d3f-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="91d3f-105">DESCRIPTION</span></span>
<span data-ttu-id="91d3f-106">O **Get-AzDataLakeAnalyticsComputePolicy** obtém uma política de computação especificada do Azure Data Lake Analytics ou uma lista de políticas.</span><span class="sxs-lookup"><span data-stu-id="91d3f-106">The **Get-AzDataLakeAnalyticsComputePolicy** gets a specified Azure Data Lake Analytics compute policy or a list of policies.</span></span>

## <span data-ttu-id="91d3f-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="91d3f-107">EXAMPLES</span></span>

### <span data-ttu-id="91d3f-108">Exemplo 1: Obter uma política de computação especificada</span><span class="sxs-lookup"><span data-stu-id="91d3f-108">Example 1: Get a specified compute policy</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name myPolicy
```

<span data-ttu-id="91d3f-109">Esse comando obtém a política de computação especificada com o nome 'myPolicy' na conta 'contosoadla'.</span><span class="sxs-lookup"><span data-stu-id="91d3f-109">This command gets the specified compute policy with name 'myPolicy' in account 'contosoadla'.</span></span>

### <span data-ttu-id="91d3f-110">Exemplo 2: Obter uma lista de todas as políticas de computação na conta</span><span class="sxs-lookup"><span data-stu-id="91d3f-110">Example 2: Get a list of all compute policies in the account</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsComputePolicy -AccountName "contosoadla"
```

<span data-ttu-id="91d3f-111">Esse comando obtém uma lista de todas as políticas de computação na conta "contosoadla"</span><span class="sxs-lookup"><span data-stu-id="91d3f-111">This command gets a list of all compute policies in the account "contosoadla"</span></span>

## <span data-ttu-id="91d3f-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="91d3f-112">PARAMETERS</span></span>

### <span data-ttu-id="91d3f-113">-Conta</span><span class="sxs-lookup"><span data-stu-id="91d3f-113">-Account</span></span>
<span data-ttu-id="91d3f-114">Nome da conta para obter a política de computação ou políticas.</span><span class="sxs-lookup"><span data-stu-id="91d3f-114">Name of the account to get the compute policy or policies from.</span></span>

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

### <span data-ttu-id="91d3f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91d3f-115">-DefaultProfile</span></span>
<span data-ttu-id="91d3f-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="91d3f-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="91d3f-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="91d3f-117">-Name</span></span>
<span data-ttu-id="91d3f-118">Nome da política de computação a ser obter.</span><span class="sxs-lookup"><span data-stu-id="91d3f-118">Name of the compute policy to get.</span></span>

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

### <span data-ttu-id="91d3f-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91d3f-119">-ResourceGroupName</span></span>
<span data-ttu-id="91d3f-120">Nome do grupo de recursos no qual a conta existe.</span><span class="sxs-lookup"><span data-stu-id="91d3f-120">Name of resource group under which you the account exists.</span></span>
<span data-ttu-id="91d3f-121">Opcional e tentará descobrir se não for fornecido.</span><span class="sxs-lookup"><span data-stu-id="91d3f-121">Optional and will attempt to discover if not provided.</span></span>

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

### <span data-ttu-id="91d3f-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91d3f-122">CommonParameters</span></span>
<span data-ttu-id="91d3f-123">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91d3f-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91d3f-124">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="91d3f-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91d3f-125">Entradas</span><span class="sxs-lookup"><span data-stu-id="91d3f-125">INPUTS</span></span>

### <span data-ttu-id="91d3f-126">System.String</span><span class="sxs-lookup"><span data-stu-id="91d3f-126">System.String</span></span>

## <span data-ttu-id="91d3f-127">Saídas</span><span class="sxs-lookup"><span data-stu-id="91d3f-127">OUTPUTS</span></span>

### <span data-ttu-id="91d3f-128">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="91d3f-128">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="91d3f-129">Notas</span><span class="sxs-lookup"><span data-stu-id="91d3f-129">NOTES</span></span>

## <span data-ttu-id="91d3f-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="91d3f-130">RELATED LINKS</span></span>

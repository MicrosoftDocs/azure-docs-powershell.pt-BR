---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/get-azurermdatalakeanalyticscomputepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsComputePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsComputePolicy.md
ms.openlocfilehash: f19c4f9d39837534ea5ddd5b16daa055ee54aef6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429829"
---
# <span data-ttu-id="b486d-101">Get-AzureRmDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="b486d-101">Get-AzureRmDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="b486d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b486d-102">SYNOPSIS</span></span>
<span data-ttu-id="b486d-103">Obtém uma política de computação de análise de data Lake ou uma lista de políticas de computação.</span><span class="sxs-lookup"><span data-stu-id="b486d-103">Gets a Data Lake Analytics compute policy or list of compute policies.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b486d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b486d-104">SYNTAX</span></span>

```
Get-AzureRmDataLakeAnalyticsComputePolicy [-ResourceGroupName <String>] [-Account] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b486d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b486d-105">DESCRIPTION</span></span>
<span data-ttu-id="b486d-106">**Get-AzureRmDataLakeAnalyticsComputePolicy** Obtém uma política de computação do Azure data Lake Analytics especificada ou uma lista de políticas.</span><span class="sxs-lookup"><span data-stu-id="b486d-106">The **Get-AzureRmDataLakeAnalyticsComputePolicy** gets a specified Azure Data Lake Analytics compute policy or a list of policies.</span></span>

## <span data-ttu-id="b486d-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b486d-107">EXAMPLES</span></span>

### <span data-ttu-id="b486d-108">Exemplo 1: obter uma política de computação especificada</span><span class="sxs-lookup"><span data-stu-id="b486d-108">Example 1: Get a specified compute policy</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name myPolicy
```

<span data-ttu-id="b486d-109">Este comando obtém a política de computação especificada com o nome ' MyPolicy ' na conta ' contosoadla '.</span><span class="sxs-lookup"><span data-stu-id="b486d-109">This command gets the specified compute policy with name 'myPolicy' in account 'contosoadla'.</span></span>

### <span data-ttu-id="b486d-110">Exemplo 2: obter uma lista de todas as políticas de computação na conta</span><span class="sxs-lookup"><span data-stu-id="b486d-110">Example 2: Get a list of all compute policies in the account</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsComputePolicy -AccountName "contosoadla"
```

<span data-ttu-id="b486d-111">Este comando obtém uma lista de todas as políticas de computação na conta "contosoadla"</span><span class="sxs-lookup"><span data-stu-id="b486d-111">This command gets a list of all compute policies in the account "contosoadla"</span></span>

## <span data-ttu-id="b486d-112">OS</span><span class="sxs-lookup"><span data-stu-id="b486d-112">PARAMETERS</span></span>

### <span data-ttu-id="b486d-113">-Conta</span><span class="sxs-lookup"><span data-stu-id="b486d-113">-Account</span></span>
<span data-ttu-id="b486d-114">Nome da conta da qual você deseja obter a política ou políticas de computação.</span><span class="sxs-lookup"><span data-stu-id="b486d-114">Name of the account to get the compute policy or policies from.</span></span>

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

### <span data-ttu-id="b486d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b486d-115">-DefaultProfile</span></span>
<span data-ttu-id="b486d-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="b486d-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b486d-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="b486d-117">-Name</span></span>
<span data-ttu-id="b486d-118">Nome da política de computação a ser obtida.</span><span class="sxs-lookup"><span data-stu-id="b486d-118">Name of the compute policy to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ComputePolicyName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b486d-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b486d-119">-ResourceGroupName</span></span>
<span data-ttu-id="b486d-120">Nome do grupo de recursos sob o qual a conta existe.</span><span class="sxs-lookup"><span data-stu-id="b486d-120">Name of resource group under which you the account exists.</span></span>
<span data-ttu-id="b486d-121">Opcional e tentará descobrir, se não for fornecido.</span><span class="sxs-lookup"><span data-stu-id="b486d-121">Optional and will attempt to discover if not provided.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b486d-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b486d-122">CommonParameters</span></span>
<span data-ttu-id="b486d-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b486d-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b486d-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b486d-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b486d-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b486d-125">INPUTS</span></span>

### <span data-ttu-id="b486d-126">System. String</span><span class="sxs-lookup"><span data-stu-id="b486d-126">System.String</span></span>

## <span data-ttu-id="b486d-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b486d-127">OUTPUTS</span></span>

### <span data-ttu-id="b486d-128">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="b486d-128">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span></span>
<span data-ttu-id="b486d-129">System. Collections. Generic. IEnumerable ' 1 [[Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy, Microsoft. Azure. Commands. DataLakeAnalytics, Version = 3.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="b486d-129">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy, Microsoft.Azure.Commands.DataLakeAnalytics, Version=3.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="b486d-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b486d-130">NOTES</span></span>

## <span data-ttu-id="b486d-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b486d-131">RELATED LINKS</span></span>


---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 0A7CD695-6D14-4BC9-B960-0CAFE502B88B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/New-AzureRmDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/New-AzureRmDataLakeAnalyticsAccount.md
ms.openlocfilehash: 7c35821cbaf75a616ab1b9b8bbc2db9fc2a96794
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440673"
---
# <span data-ttu-id="b65fb-101">New-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="b65fb-101">New-AzureRmDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="b65fb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b65fb-102">SYNOPSIS</span></span>
<span data-ttu-id="b65fb-103">Cria uma conta do data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="b65fb-103">Creates a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b65fb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b65fb-104">SYNTAX</span></span>

```
New-AzureRmDataLakeAnalyticsAccount [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-DefaultDataLakeStore] <String> [[-Tags] <Hashtable>] [-MaxDegreeOfParallelism <Int32>]
 [-MaxJobCount <Int32>] [-QueryStoreRetention <Int32>] [-Tier <TierType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b65fb-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b65fb-105">DESCRIPTION</span></span>
<span data-ttu-id="b65fb-106">O cmdlet **New-AzureRmDataLakeAnalyticsAccount** cria uma conta do Azure data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="b65fb-106">The **New-AzureRmDataLakeAnalyticsAccount** cmdlet creates an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="b65fb-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b65fb-107">EXAMPLES</span></span>

### <span data-ttu-id="b65fb-108">Exemplo 1: criar uma conta do data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="b65fb-108">Example 1: Create a Data Lake Analytics account</span></span>
```
PS C:\>New-AzureRmDataLakeAnalyticsAccount -Name "ContosoAdlAccount" -ResourceGroupName "ContosoOrg" -Location "East US 2" -DefaultDataLakeStore "ContosoAdlStore"
```

<span data-ttu-id="b65fb-109">Esse comando cria uma conta do data Lake Analytics chamada ContosoAdlAccount que usa o repositório de dados ContosoAdlStore, no grupo de recursos chamado ContosoOrg.</span><span class="sxs-lookup"><span data-stu-id="b65fb-109">This command creates a Data Lake Analytics account named ContosoAdlAccount that uses the ContosoAdlStore Data Store, in the resource group named ContosoOrg.</span></span>

## <span data-ttu-id="b65fb-110">OS</span><span class="sxs-lookup"><span data-stu-id="b65fb-110">PARAMETERS</span></span>

### <span data-ttu-id="b65fb-111">-DefaultDataLakeStore</span><span class="sxs-lookup"><span data-stu-id="b65fb-111">-DefaultDataLakeStore</span></span>
<span data-ttu-id="b65fb-112">Especifica o nome da conta do data Lake Store para definir como a fonte de dados padrão.</span><span class="sxs-lookup"><span data-stu-id="b65fb-112">Specifies the name of the Data Lake Store account to set as the default data source.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b65fb-113">-Local</span><span class="sxs-lookup"><span data-stu-id="b65fb-113">-Location</span></span>
<span data-ttu-id="b65fb-114">Especifica o local no qual criar a conta do data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="b65fb-114">Specifies the location at which to create the Data Lake Analytics account.</span></span>
<span data-ttu-id="b65fb-115">Somente o leste dos EUA 2 tem suporte no momento.</span><span class="sxs-lookup"><span data-stu-id="b65fb-115">Only East US 2 is supported at this time.</span></span>

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

### <span data-ttu-id="b65fb-116">-MaxDegreeOfParallelism</span><span class="sxs-lookup"><span data-stu-id="b65fb-116">-MaxDegreeOfParallelism</span></span>
<span data-ttu-id="b65fb-117">O grau máximo de suporte opcional de paralelismo para esta conta.</span><span class="sxs-lookup"><span data-stu-id="b65fb-117">The optional maximum supported degree of parallelism for this account.</span></span> <span data-ttu-id="b65fb-118">Se nenhum for especificado, o padrão será 30</span><span class="sxs-lookup"><span data-stu-id="b65fb-118">If none is specified, defaults to 30</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b65fb-119">-MaxJobCount</span><span class="sxs-lookup"><span data-stu-id="b65fb-119">-MaxJobCount</span></span>
<span data-ttu-id="b65fb-120">O máximo de trabalhos opcionais com suporte em execução na conta ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="b65fb-120">The optional maximum supported jobs running under the account at the same time.</span></span> <span data-ttu-id="b65fb-121">Se nenhum for especificado, o padrão será 3</span><span class="sxs-lookup"><span data-stu-id="b65fb-121">If none is specified, defaults to 3</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b65fb-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="b65fb-122">-Name</span></span>
<span data-ttu-id="b65fb-123">Especifica o nome da conta do data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="b65fb-123">Specifies the Data Lake Analytics account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b65fb-124">-QueryStoreRetention</span><span class="sxs-lookup"><span data-stu-id="b65fb-124">-QueryStoreRetention</span></span>
<span data-ttu-id="b65fb-125">O número opcional de dias pelos quais os metadados do trabalho são mantidos.</span><span class="sxs-lookup"><span data-stu-id="b65fb-125">The optional number of days that job metadata is retained.</span></span> <span data-ttu-id="b65fb-126">Se nenhum for especificado, o padrão será 30 dias.</span><span class="sxs-lookup"><span data-stu-id="b65fb-126">If none specified, the default is 30 days.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b65fb-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b65fb-127">-ResourceGroupName</span></span>
<span data-ttu-id="b65fb-128">Especifica o nome do grupo de recursos da conta do data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="b65fb-128">Specifies the resource group name of the Data Lake Analytics account.</span></span>
<span data-ttu-id="b65fb-129">Para criar um grupo de recursos, use o cmdlet New-AzureRmResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="b65fb-129">To create a resource group, use the New-AzureRmResourceGroup cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b65fb-130">-Marcas</span><span class="sxs-lookup"><span data-stu-id="b65fb-130">-Tags</span></span>
<span data-ttu-id="b65fb-131">Especifica os pares de valores chave que podem ser usados para identificar a conta do data Lake Analytics entre outros recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="b65fb-131">Specifies key-value pairs that can be used to identify the Data Lake Analytics account among other Azure resources.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b65fb-132">-Tier</span><span class="sxs-lookup"><span data-stu-id="b65fb-132">-Tier</span></span>
<span data-ttu-id="b65fb-133">A camada de compromisso desejada para esta conta usar.</span><span class="sxs-lookup"><span data-stu-id="b65fb-133">The desired commitment tier for this account to use.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.DataLake.Analytics.Models.TierType]
Parameter Sets: (All)
Aliases: 
Accepted values: Consumption, Commitment100AUHours, Commitment500AUHours, Commitment1000AUHours, Commitment5000AUHours, Commitment10000AUHours, Commitment50000AUHours, Commitment100000AUHours, Commitment500000AUHours

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b65fb-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b65fb-134">-DefaultProfile</span></span>
<span data-ttu-id="b65fb-135">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b65fb-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b65fb-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b65fb-136">CommonParameters</span></span>
<span data-ttu-id="b65fb-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b65fb-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b65fb-138">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b65fb-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b65fb-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b65fb-139">INPUTS</span></span>

## <span data-ttu-id="b65fb-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b65fb-140">OUTPUTS</span></span>

### <span data-ttu-id="b65fb-141">PSDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="b65fb-141">PSDataLakeAnalyticsAccount</span></span>
<span data-ttu-id="b65fb-142">Os detalhes da conta recém-criada.</span><span class="sxs-lookup"><span data-stu-id="b65fb-142">The details of the newly created account.</span></span>

## <span data-ttu-id="b65fb-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b65fb-143">NOTES</span></span>

## <span data-ttu-id="b65fb-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b65fb-144">RELATED LINKS</span></span>

[<span data-ttu-id="b65fb-145">Get-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="b65fb-145">Get-AzureRmDataLakeAnalyticsAccount</span></span>](./Get-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="b65fb-146">Remove-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="b65fb-146">Remove-AzureRmDataLakeAnalyticsAccount</span></span>](./Remove-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="b65fb-147">Set-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="b65fb-147">Set-AzureRmDataLakeAnalyticsAccount</span></span>](./Set-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="b65fb-148">Test-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="b65fb-148">Test-AzureRmDataLakeAnalyticsAccount</span></span>](./Test-AzureRmDataLakeAnalyticsAccount.md)



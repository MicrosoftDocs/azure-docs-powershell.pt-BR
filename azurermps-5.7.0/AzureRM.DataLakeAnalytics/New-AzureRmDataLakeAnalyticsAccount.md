---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 0A7CD695-6D14-4BC9-B960-0CAFE502B88B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/new-azurermdatalakeanalyticsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/New-AzureRmDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/New-AzureRmDataLakeAnalyticsAccount.md
ms.openlocfilehash: 36bf1bbfeb0c44189f5eeeaa0988d0314980e48d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428953"
---
# <span data-ttu-id="abccc-101">New-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="abccc-101">New-AzureRmDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="abccc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="abccc-102">SYNOPSIS</span></span>
<span data-ttu-id="abccc-103">Cria uma conta do data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="abccc-103">Creates a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="abccc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="abccc-104">SYNTAX</span></span>

```
New-AzureRmDataLakeAnalyticsAccount [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-DefaultDataLakeStore] <String> [[-Tag] <Hashtable>] [-MaxAnalyticsUnits <Int32>] [-MaxJobCount <Int32>]
 [-QueryStoreRetention <Int32>] [-Tier <TierType>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="abccc-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="abccc-105">DESCRIPTION</span></span>
<span data-ttu-id="abccc-106">O cmdlet **New-AzureRmDataLakeAnalyticsAccount** cria uma conta do Azure data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="abccc-106">The **New-AzureRmDataLakeAnalyticsAccount** cmdlet creates an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="abccc-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="abccc-107">EXAMPLES</span></span>

### <span data-ttu-id="abccc-108">Exemplo 1: criar uma conta do data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="abccc-108">Example 1: Create a Data Lake Analytics account</span></span>
```
PS C:\>New-AzureRmDataLakeAnalyticsAccount -Name "ContosoAdlAccount" -ResourceGroupName "ContosoOrg" -Location "East US 2" -DefaultDataLakeStore "ContosoAdlStore"
```

<span data-ttu-id="abccc-109">Esse comando cria uma conta do data Lake Analytics chamada ContosoAdlAccount que usa o repositório de dados ContosoAdlStore, no grupo de recursos chamado ContosoOrg.</span><span class="sxs-lookup"><span data-stu-id="abccc-109">This command creates a Data Lake Analytics account named ContosoAdlAccount that uses the ContosoAdlStore Data Store, in the resource group named ContosoOrg.</span></span>

## <span data-ttu-id="abccc-110">OS</span><span class="sxs-lookup"><span data-stu-id="abccc-110">PARAMETERS</span></span>

### <span data-ttu-id="abccc-111">-DefaultDataLakeStore</span><span class="sxs-lookup"><span data-stu-id="abccc-111">-DefaultDataLakeStore</span></span>
<span data-ttu-id="abccc-112">Especifica o nome da conta do data Lake Store para definir como a fonte de dados padrão.</span><span class="sxs-lookup"><span data-stu-id="abccc-112">Specifies the name of the Data Lake Store account to set as the default data source.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="abccc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="abccc-113">-DefaultProfile</span></span>
<span data-ttu-id="abccc-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="abccc-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="abccc-115">-Local</span><span class="sxs-lookup"><span data-stu-id="abccc-115">-Location</span></span>
<span data-ttu-id="abccc-116">Especifica o local no qual criar a conta do data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="abccc-116">Specifies the location at which to create the Data Lake Analytics account.</span></span>
<span data-ttu-id="abccc-117">Somente o leste dos EUA 2 tem suporte no momento.</span><span class="sxs-lookup"><span data-stu-id="abccc-117">Only East US 2 is supported at this time.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="abccc-118">-MaxAnalyticsUnits</span><span class="sxs-lookup"><span data-stu-id="abccc-118">-MaxAnalyticsUnits</span></span>
<span data-ttu-id="abccc-119">As unidades de análise máximas com suporte para esta conta.</span><span class="sxs-lookup"><span data-stu-id="abccc-119">The optional maximum supported analytics units for this account.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: MaxDegreeOfParallelism

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="abccc-120">-MaxJobCount</span><span class="sxs-lookup"><span data-stu-id="abccc-120">-MaxJobCount</span></span>
<span data-ttu-id="abccc-121">O máximo de trabalhos opcionais com suporte em execução na conta ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="abccc-121">The optional maximum supported jobs running under the account at the same time.</span></span> <span data-ttu-id="abccc-122">Se nenhum for especificado, o padrão será 3</span><span class="sxs-lookup"><span data-stu-id="abccc-122">If none is specified, defaults to 3</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="abccc-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="abccc-123">-Name</span></span>
<span data-ttu-id="abccc-124">Especifica o nome da conta do data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="abccc-124">Specifies the Data Lake Analytics account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="abccc-125">-QueryStoreRetention</span><span class="sxs-lookup"><span data-stu-id="abccc-125">-QueryStoreRetention</span></span>
<span data-ttu-id="abccc-126">O número opcional de dias pelos quais os metadados do trabalho são mantidos.</span><span class="sxs-lookup"><span data-stu-id="abccc-126">The optional number of days that job metadata is retained.</span></span> <span data-ttu-id="abccc-127">Se nenhum for especificado, o padrão será 30 dias.</span><span class="sxs-lookup"><span data-stu-id="abccc-127">If none specified, the default is 30 days.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="abccc-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="abccc-128">-ResourceGroupName</span></span>
<span data-ttu-id="abccc-129">Especifica o nome do grupo de recursos da conta do data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="abccc-129">Specifies the resource group name of the Data Lake Analytics account.</span></span>
<span data-ttu-id="abccc-130">Para criar um grupo de recursos, use o cmdlet New-AzureRmResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="abccc-130">To create a resource group, use the New-AzureRmResourceGroup cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="abccc-131">-Marca</span><span class="sxs-lookup"><span data-stu-id="abccc-131">-Tag</span></span>
<span data-ttu-id="abccc-132">Uma cadeia de caracteres, dicionário de cadeias de caracteres de marcas associadas a essa conta</span><span class="sxs-lookup"><span data-stu-id="abccc-132">A string,string dictionary of tags associated with this account</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="abccc-133">-Tier</span><span class="sxs-lookup"><span data-stu-id="abccc-133">-Tier</span></span>
<span data-ttu-id="abccc-134">A camada de compromisso desejada para esta conta usar.</span><span class="sxs-lookup"><span data-stu-id="abccc-134">The desired commitment tier for this account to use.</span></span>

```yaml
Type: TierType
Parameter Sets: (All)
Aliases:
Accepted values: Consumption, Commitment100AUHours, Commitment500AUHours, Commitment1000AUHours, Commitment5000AUHours, Commitment10000AUHours, Commitment50000AUHours, Commitment100000AUHours, Commitment500000AUHours

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="abccc-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="abccc-135">CommonParameters</span></span>
<span data-ttu-id="abccc-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="abccc-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="abccc-137">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="abccc-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="abccc-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="abccc-138">INPUTS</span></span>

### <span data-ttu-id="abccc-139">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="abccc-139">None</span></span>
<span data-ttu-id="abccc-140">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="abccc-140">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="abccc-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="abccc-141">OUTPUTS</span></span>

### <span data-ttu-id="abccc-142">PSDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="abccc-142">PSDataLakeAnalyticsAccount</span></span>
<span data-ttu-id="abccc-143">Os detalhes da conta recém-criada.</span><span class="sxs-lookup"><span data-stu-id="abccc-143">The details of the newly created account.</span></span>

## <span data-ttu-id="abccc-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="abccc-144">NOTES</span></span>

## <span data-ttu-id="abccc-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="abccc-145">RELATED LINKS</span></span>

[<span data-ttu-id="abccc-146">Get-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="abccc-146">Get-AzureRmDataLakeAnalyticsAccount</span></span>](./Get-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="abccc-147">Remove-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="abccc-147">Remove-AzureRmDataLakeAnalyticsAccount</span></span>](./Remove-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="abccc-148">Set-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="abccc-148">Set-AzureRmDataLakeAnalyticsAccount</span></span>](./Set-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="abccc-149">Test-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="abccc-149">Test-AzureRmDataLakeAnalyticsAccount</span></span>](./Test-AzureRmDataLakeAnalyticsAccount.md)



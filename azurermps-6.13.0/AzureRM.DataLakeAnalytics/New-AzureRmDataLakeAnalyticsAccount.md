---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 0A7CD695-6D14-4BC9-B960-0CAFE502B88B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/new-azurermdatalakeanalyticsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/New-AzureRmDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/New-AzureRmDataLakeAnalyticsAccount.md
ms.openlocfilehash: 2fec19864e9d13e4b0e4ede1d351a08427e95357
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93433266"
---
# <span data-ttu-id="d08c4-101">New-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="d08c4-101">New-AzureRmDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="d08c4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d08c4-102">SYNOPSIS</span></span>
<span data-ttu-id="d08c4-103">Cria uma conta do data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="d08c4-103">Creates a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d08c4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d08c4-104">SYNTAX</span></span>

```
New-AzureRmDataLakeAnalyticsAccount [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-DefaultDataLakeStore] <String> [[-Tag] <Hashtable>] [-MaxAnalyticsUnits <Int32>] [-MaxJobCount <Int32>]
 [-QueryStoreRetention <Int32>] [-Tier <TierType>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d08c4-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d08c4-105">DESCRIPTION</span></span>
<span data-ttu-id="d08c4-106">O cmdlet **New-AzureRmDataLakeAnalyticsAccount** cria uma conta do Azure data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="d08c4-106">The **New-AzureRmDataLakeAnalyticsAccount** cmdlet creates an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="d08c4-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d08c4-107">EXAMPLES</span></span>

### <span data-ttu-id="d08c4-108">Exemplo 1: criar uma conta do data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="d08c4-108">Example 1: Create a Data Lake Analytics account</span></span>
```
PS C:\>New-AzureRmDataLakeAnalyticsAccount -Name "ContosoAdlAccount" -ResourceGroupName "ContosoOrg" -Location "East US 2" -DefaultDataLakeStore "ContosoAdlStore"
```

<span data-ttu-id="d08c4-109">Esse comando cria uma conta do data Lake Analytics chamada ContosoAdlAccount que usa o repositório de dados ContosoAdlStore, no grupo de recursos chamado ContosoOrg.</span><span class="sxs-lookup"><span data-stu-id="d08c4-109">This command creates a Data Lake Analytics account named ContosoAdlAccount that uses the ContosoAdlStore Data Store, in the resource group named ContosoOrg.</span></span>

## <span data-ttu-id="d08c4-110">OS</span><span class="sxs-lookup"><span data-stu-id="d08c4-110">PARAMETERS</span></span>

### <span data-ttu-id="d08c4-111">-DefaultDataLakeStore</span><span class="sxs-lookup"><span data-stu-id="d08c4-111">-DefaultDataLakeStore</span></span>
<span data-ttu-id="d08c4-112">Especifica o nome da conta do data Lake Store para definir como a fonte de dados padrão.</span><span class="sxs-lookup"><span data-stu-id="d08c4-112">Specifies the name of the Data Lake Store account to set as the default data source.</span></span>

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

### <span data-ttu-id="d08c4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d08c4-113">-DefaultProfile</span></span>
<span data-ttu-id="d08c4-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="d08c4-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d08c4-115">-Local</span><span class="sxs-lookup"><span data-stu-id="d08c4-115">-Location</span></span>
<span data-ttu-id="d08c4-116">Especifica o local no qual criar a conta do data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="d08c4-116">Specifies the location at which to create the Data Lake Analytics account.</span></span>
<span data-ttu-id="d08c4-117">Somente o leste dos EUA 2 tem suporte no momento.</span><span class="sxs-lookup"><span data-stu-id="d08c4-117">Only East US 2 is supported at this time.</span></span>

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

### <span data-ttu-id="d08c4-118">-MaxAnalyticsUnits</span><span class="sxs-lookup"><span data-stu-id="d08c4-118">-MaxAnalyticsUnits</span></span>
<span data-ttu-id="d08c4-119">As unidades de análise máximas com suporte para esta conta.</span><span class="sxs-lookup"><span data-stu-id="d08c4-119">The optional maximum supported analytics units for this account.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: MaxDegreeOfParallelism

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d08c4-120">-MaxJobCount</span><span class="sxs-lookup"><span data-stu-id="d08c4-120">-MaxJobCount</span></span>
<span data-ttu-id="d08c4-121">O máximo de trabalhos opcionais com suporte em execução na conta ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="d08c4-121">The optional maximum supported jobs running under the account at the same time.</span></span> <span data-ttu-id="d08c4-122">Se nenhum for especificado, o padrão será 3</span><span class="sxs-lookup"><span data-stu-id="d08c4-122">If none is specified, defaults to 3</span></span>

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

### <span data-ttu-id="d08c4-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="d08c4-123">-Name</span></span>
<span data-ttu-id="d08c4-124">Especifica o nome da conta do data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="d08c4-124">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="d08c4-125">-QueryStoreRetention</span><span class="sxs-lookup"><span data-stu-id="d08c4-125">-QueryStoreRetention</span></span>
<span data-ttu-id="d08c4-126">O número opcional de dias pelos quais os metadados do trabalho são mantidos.</span><span class="sxs-lookup"><span data-stu-id="d08c4-126">The optional number of days that job metadata is retained.</span></span> <span data-ttu-id="d08c4-127">Se nenhum for especificado, o padrão será 30 dias.</span><span class="sxs-lookup"><span data-stu-id="d08c4-127">If none specified, the default is 30 days.</span></span>

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

### <span data-ttu-id="d08c4-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d08c4-128">-ResourceGroupName</span></span>
<span data-ttu-id="d08c4-129">Especifica o nome do grupo de recursos da conta do data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="d08c4-129">Specifies the resource group name of the Data Lake Analytics account.</span></span>
<span data-ttu-id="d08c4-130">Para criar um grupo de recursos, use o cmdlet New-AzureRmResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="d08c4-130">To create a resource group, use the New-AzureRmResourceGroup cmdlet.</span></span>

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

### <span data-ttu-id="d08c4-131">-Marca</span><span class="sxs-lookup"><span data-stu-id="d08c4-131">-Tag</span></span>
<span data-ttu-id="d08c4-132">Uma cadeia de caracteres, dicionário de cadeias de caracteres de marcas associadas a essa conta</span><span class="sxs-lookup"><span data-stu-id="d08c4-132">A string,string dictionary of tags associated with this account</span></span>

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

### <span data-ttu-id="d08c4-133">-Tier</span><span class="sxs-lookup"><span data-stu-id="d08c4-133">-Tier</span></span>
<span data-ttu-id="d08c4-134">A camada de compromisso desejada para esta conta usar.</span><span class="sxs-lookup"><span data-stu-id="d08c4-134">The desired commitment tier for this account to use.</span></span>

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

### <span data-ttu-id="d08c4-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d08c4-135">CommonParameters</span></span>
<span data-ttu-id="d08c4-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d08c4-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d08c4-137">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d08c4-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d08c4-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d08c4-138">INPUTS</span></span>

### <span data-ttu-id="d08c4-139">System. String</span><span class="sxs-lookup"><span data-stu-id="d08c4-139">System.String</span></span>

### <span data-ttu-id="d08c4-140">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="d08c4-140">System.Collections.Hashtable</span></span>

### <span data-ttu-id="d08c4-141">System. Nullable ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="d08c4-141">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="d08c4-142">System. Nullable ' 1 [[Microsoft. Azure. Management. datalake. remanagement. Models. Tiertype, Microsoft. Azure. Management. datalake. Analytics, Version = 3.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="d08c4-142">System.Nullable\`1[[Microsoft.Azure.Management.DataLake.Analytics.Models.TierType, Microsoft.Azure.Management.DataLake.Analytics, Version=3.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="d08c4-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d08c4-143">OUTPUTS</span></span>

### <span data-ttu-id="d08c4-144">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="d08c4-144">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="d08c4-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d08c4-145">NOTES</span></span>

## <span data-ttu-id="d08c4-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d08c4-146">RELATED LINKS</span></span>

[<span data-ttu-id="d08c4-147">Get-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="d08c4-147">Get-AzureRmDataLakeAnalyticsAccount</span></span>](./Get-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="d08c4-148">Remove-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="d08c4-148">Remove-AzureRmDataLakeAnalyticsAccount</span></span>](./Remove-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="d08c4-149">Set-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="d08c4-149">Set-AzureRmDataLakeAnalyticsAccount</span></span>](./Set-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="d08c4-150">Test-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="d08c4-150">Test-AzureRmDataLakeAnalyticsAccount</span></span>](./Test-AzureRmDataLakeAnalyticsAccount.md)



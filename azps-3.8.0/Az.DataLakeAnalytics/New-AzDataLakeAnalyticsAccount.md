---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: 0A7CD695-6D14-4BC9-B960-0CAFE502B88B
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/new-azdatalakeanalyticsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/New-AzDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/New-AzDataLakeAnalyticsAccount.md
ms.openlocfilehash: c79665a6ed21309a7a702d9fd5bc5e876aa2ff21
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93940842"
---
# <span data-ttu-id="59a48-101">New-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="59a48-101">New-AzDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="59a48-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="59a48-102">SYNOPSIS</span></span>
<span data-ttu-id="59a48-103">Cria uma conta do data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="59a48-103">Creates a Data Lake Analytics account.</span></span>

## <span data-ttu-id="59a48-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="59a48-104">SYNTAX</span></span>

```
New-AzDataLakeAnalyticsAccount [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-DefaultDataLakeStore] <String> [[-Tag] <Hashtable>] [-MaxAnalyticsUnits <Int32>] [-MaxJobCount <Int32>]
 [-QueryStoreRetention <Int32>] [-Tier <TierType>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="59a48-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="59a48-105">DESCRIPTION</span></span>
<span data-ttu-id="59a48-106">O cmdlet **New-AzDataLakeAnalyticsAccount** cria uma conta do Azure data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="59a48-106">The **New-AzDataLakeAnalyticsAccount** cmdlet creates an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="59a48-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="59a48-107">EXAMPLES</span></span>

### <span data-ttu-id="59a48-108">Exemplo 1: criar uma conta do data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="59a48-108">Example 1: Create a Data Lake Analytics account</span></span>
```
PS C:\>New-AzDataLakeAnalyticsAccount -Name "ContosoAdlAccount" -ResourceGroupName "ContosoOrg" -Location "East US 2" -DefaultDataLakeStore "ContosoAdlStore"
```

<span data-ttu-id="59a48-109">Esse comando cria uma conta do data Lake Analytics chamada ContosoAdlAccount que usa o repositório de dados ContosoAdlStore, no grupo de recursos chamado ContosoOrg.</span><span class="sxs-lookup"><span data-stu-id="59a48-109">This command creates a Data Lake Analytics account named ContosoAdlAccount that uses the ContosoAdlStore Data Store, in the resource group named ContosoOrg.</span></span>

## <span data-ttu-id="59a48-110">OS</span><span class="sxs-lookup"><span data-stu-id="59a48-110">PARAMETERS</span></span>

### <span data-ttu-id="59a48-111">-DefaultDataLakeStore</span><span class="sxs-lookup"><span data-stu-id="59a48-111">-DefaultDataLakeStore</span></span>
<span data-ttu-id="59a48-112">Especifica o nome da conta do data Lake Store para definir como a fonte de dados padrão.</span><span class="sxs-lookup"><span data-stu-id="59a48-112">Specifies the name of the Data Lake Store account to set as the default data source.</span></span>

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

### <span data-ttu-id="59a48-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59a48-113">-DefaultProfile</span></span>
<span data-ttu-id="59a48-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="59a48-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="59a48-115">-Local</span><span class="sxs-lookup"><span data-stu-id="59a48-115">-Location</span></span>
<span data-ttu-id="59a48-116">Especifica o local no qual criar a conta do data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="59a48-116">Specifies the location at which to create the Data Lake Analytics account.</span></span>
<span data-ttu-id="59a48-117">Somente o leste dos EUA 2 tem suporte no momento.</span><span class="sxs-lookup"><span data-stu-id="59a48-117">Only East US 2 is supported at this time.</span></span>

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

### <span data-ttu-id="59a48-118">-MaxAnalyticsUnits</span><span class="sxs-lookup"><span data-stu-id="59a48-118">-MaxAnalyticsUnits</span></span>
<span data-ttu-id="59a48-119">As unidades de análise máximas com suporte para esta conta.</span><span class="sxs-lookup"><span data-stu-id="59a48-119">The optional maximum supported analytics units for this account.</span></span>

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

### <span data-ttu-id="59a48-120">-MaxJobCount</span><span class="sxs-lookup"><span data-stu-id="59a48-120">-MaxJobCount</span></span>
<span data-ttu-id="59a48-121">O máximo de trabalhos opcionais com suporte em execução na conta ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="59a48-121">The optional maximum supported jobs running under the account at the same time.</span></span> <span data-ttu-id="59a48-122">Se nenhum for especificado, o padrão será 3</span><span class="sxs-lookup"><span data-stu-id="59a48-122">If none is specified, defaults to 3</span></span>

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

### <span data-ttu-id="59a48-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="59a48-123">-Name</span></span>
<span data-ttu-id="59a48-124">Especifica o nome da conta do data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="59a48-124">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="59a48-125">-QueryStoreRetention</span><span class="sxs-lookup"><span data-stu-id="59a48-125">-QueryStoreRetention</span></span>
<span data-ttu-id="59a48-126">O número opcional de dias pelos quais os metadados do trabalho são mantidos.</span><span class="sxs-lookup"><span data-stu-id="59a48-126">The optional number of days that job metadata is retained.</span></span> <span data-ttu-id="59a48-127">Se nenhum for especificado, o padrão será 30 dias.</span><span class="sxs-lookup"><span data-stu-id="59a48-127">If none specified, the default is 30 days.</span></span>

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

### <span data-ttu-id="59a48-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59a48-128">-ResourceGroupName</span></span>
<span data-ttu-id="59a48-129">Especifica o nome do grupo de recursos da conta do data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="59a48-129">Specifies the resource group name of the Data Lake Analytics account.</span></span>
<span data-ttu-id="59a48-130">Para criar um grupo de recursos, use o cmdlet New-AzResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="59a48-130">To create a resource group, use the New-AzResourceGroup cmdlet.</span></span>

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

### <span data-ttu-id="59a48-131">-Marca</span><span class="sxs-lookup"><span data-stu-id="59a48-131">-Tag</span></span>
<span data-ttu-id="59a48-132">Uma cadeia de caracteres, dicionário de cadeias de caracteres de marcas associadas a essa conta</span><span class="sxs-lookup"><span data-stu-id="59a48-132">A string,string dictionary of tags associated with this account</span></span>

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

### <span data-ttu-id="59a48-133">-Tier</span><span class="sxs-lookup"><span data-stu-id="59a48-133">-Tier</span></span>
<span data-ttu-id="59a48-134">A camada de compromisso desejada para esta conta usar.</span><span class="sxs-lookup"><span data-stu-id="59a48-134">The desired commitment tier for this account to use.</span></span>

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

### <span data-ttu-id="59a48-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59a48-135">CommonParameters</span></span>
<span data-ttu-id="59a48-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59a48-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59a48-137">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59a48-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59a48-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="59a48-138">INPUTS</span></span>

### <span data-ttu-id="59a48-139">System. String</span><span class="sxs-lookup"><span data-stu-id="59a48-139">System.String</span></span>

### <span data-ttu-id="59a48-140">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="59a48-140">System.Collections.Hashtable</span></span>

### <span data-ttu-id="59a48-141">System. Nullable ' 1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="59a48-141">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="59a48-142">System. Nullable ' 1 [[Microsoft. Azure. Management. datalake. remanagement. Models. Tiertype, Microsoft. Azure. Management. datalake. Analytics, Version = 3.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="59a48-142">System.Nullable\`1[[Microsoft.Azure.Management.DataLake.Analytics.Models.TierType, Microsoft.Azure.Management.DataLake.Analytics, Version=3.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="59a48-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="59a48-143">OUTPUTS</span></span>

### <span data-ttu-id="59a48-144">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="59a48-144">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="59a48-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="59a48-145">NOTES</span></span>

## <span data-ttu-id="59a48-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="59a48-146">RELATED LINKS</span></span>

[<span data-ttu-id="59a48-147">Get-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="59a48-147">Get-AzDataLakeAnalyticsAccount</span></span>](./Get-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="59a48-148">Remove-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="59a48-148">Remove-AzDataLakeAnalyticsAccount</span></span>](./Remove-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="59a48-149">Set-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="59a48-149">Set-AzDataLakeAnalyticsAccount</span></span>](./Set-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="59a48-150">Test-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="59a48-150">Test-AzDataLakeAnalyticsAccount</span></span>](./Test-AzDataLakeAnalyticsAccount.md)



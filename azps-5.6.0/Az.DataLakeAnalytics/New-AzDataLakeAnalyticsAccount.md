---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: 0A7CD695-6D14-4BC9-B960-0CAFE502B88B
online version: https://docs.microsoft.com/powershell/module/az.datalakeanalytics/new-azdatalakeanalyticsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/New-AzDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/New-AzDataLakeAnalyticsAccount.md
ms.openlocfilehash: 621500a20aac57b43e86f354112ad1f8a633ec32
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889280"
---
# <span data-ttu-id="bbe29-101">New-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="bbe29-101">New-AzDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="bbe29-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bbe29-102">SYNOPSIS</span></span>
<span data-ttu-id="bbe29-103">Cria uma conta do Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="bbe29-103">Creates a Data Lake Analytics account.</span></span>

## <span data-ttu-id="bbe29-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="bbe29-104">SYNTAX</span></span>

```
New-AzDataLakeAnalyticsAccount [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-DefaultDataLakeStore] <String> [[-Tag] <Hashtable>] [-MaxAnalyticsUnits <Int32>] [-MaxJobCount <Int32>]
 [-QueryStoreRetention <Int32>] [-Tier <TierType>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bbe29-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="bbe29-105">DESCRIPTION</span></span>
<span data-ttu-id="bbe29-106">O cmdlet **New-AzDataLakeAnalyticsAccount** cria uma conta do Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="bbe29-106">The **New-AzDataLakeAnalyticsAccount** cmdlet creates an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="bbe29-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bbe29-107">EXAMPLES</span></span>

### <span data-ttu-id="bbe29-108">Exemplo 1: Criar uma conta do Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="bbe29-108">Example 1: Create a Data Lake Analytics account</span></span>
```
PS C:\>New-AzDataLakeAnalyticsAccount -Name "ContosoAdlAccount" -ResourceGroupName "ContosoOrg" -Location "East US 2" -DefaultDataLakeStore "ContosoAdlStore"
```

<span data-ttu-id="bbe29-109">Este comando cria uma conta do Data Lake Analytics chamada ContosoAdlAccount que usa o Repositório de Dados ContosoAdlStore, no grupo de recursos chamado ContosoOrg.</span><span class="sxs-lookup"><span data-stu-id="bbe29-109">This command creates a Data Lake Analytics account named ContosoAdlAccount that uses the ContosoAdlStore Data Store, in the resource group named ContosoOrg.</span></span>

## <span data-ttu-id="bbe29-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="bbe29-110">PARAMETERS</span></span>

### <span data-ttu-id="bbe29-111">-DefaultDataLakeStore</span><span class="sxs-lookup"><span data-stu-id="bbe29-111">-DefaultDataLakeStore</span></span>
<span data-ttu-id="bbe29-112">Especifica o nome da conta do Data Lake Store para definir como a fonte de dados padrão.</span><span class="sxs-lookup"><span data-stu-id="bbe29-112">Specifies the name of the Data Lake Store account to set as the default data source.</span></span>

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

### <span data-ttu-id="bbe29-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bbe29-113">-DefaultProfile</span></span>
<span data-ttu-id="bbe29-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="bbe29-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bbe29-115">-Location</span><span class="sxs-lookup"><span data-stu-id="bbe29-115">-Location</span></span>
<span data-ttu-id="bbe29-116">Especifica o local em que criar a conta do Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="bbe29-116">Specifies the location at which to create the Data Lake Analytics account.</span></span>
<span data-ttu-id="bbe29-117">Somente o East US 2 tem suporte neste momento.</span><span class="sxs-lookup"><span data-stu-id="bbe29-117">Only East US 2 is supported at this time.</span></span>

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

### <span data-ttu-id="bbe29-118">-MaxAnalyticsUnits</span><span class="sxs-lookup"><span data-stu-id="bbe29-118">-MaxAnalyticsUnits</span></span>
<span data-ttu-id="bbe29-119">As unidades de análise máximas com suporte máximo opcional para essa conta.</span><span class="sxs-lookup"><span data-stu-id="bbe29-119">The optional maximum supported analytics units for this account.</span></span>

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

### <span data-ttu-id="bbe29-120">-MaxJobCount</span><span class="sxs-lookup"><span data-stu-id="bbe29-120">-MaxJobCount</span></span>
<span data-ttu-id="bbe29-121">Os trabalhos opcionais com suporte máximo em execução na conta ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="bbe29-121">The optional maximum supported jobs running under the account at the same time.</span></span> <span data-ttu-id="bbe29-122">Se nenhum for especificado, o padrão será 3</span><span class="sxs-lookup"><span data-stu-id="bbe29-122">If none is specified, defaults to 3</span></span>

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

### <span data-ttu-id="bbe29-123">-Name</span><span class="sxs-lookup"><span data-stu-id="bbe29-123">-Name</span></span>
<span data-ttu-id="bbe29-124">Especifica o nome da conta do Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="bbe29-124">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="bbe29-125">-QueryStoreRetention</span><span class="sxs-lookup"><span data-stu-id="bbe29-125">-QueryStoreRetention</span></span>
<span data-ttu-id="bbe29-126">O número opcional de dias em que os metadados de trabalho são mantidos.</span><span class="sxs-lookup"><span data-stu-id="bbe29-126">The optional number of days that job metadata is retained.</span></span> <span data-ttu-id="bbe29-127">Se nenhum especificado, o padrão é 30 dias.</span><span class="sxs-lookup"><span data-stu-id="bbe29-127">If none specified, the default is 30 days.</span></span>

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

### <span data-ttu-id="bbe29-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bbe29-128">-ResourceGroupName</span></span>
<span data-ttu-id="bbe29-129">Especifica o nome do grupo de recursos da conta do Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="bbe29-129">Specifies the resource group name of the Data Lake Analytics account.</span></span>
<span data-ttu-id="bbe29-130">Para criar um grupo de recursos, use o New-AzResourceGroup cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bbe29-130">To create a resource group, use the New-AzResourceGroup cmdlet.</span></span>

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

### <span data-ttu-id="bbe29-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="bbe29-131">-Tag</span></span>
<span data-ttu-id="bbe29-132">Uma cadeia de caracteres,dicionário de cadeias de caracteres de marcas associadas a essa conta</span><span class="sxs-lookup"><span data-stu-id="bbe29-132">A string,string dictionary of tags associated with this account</span></span>

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

### <span data-ttu-id="bbe29-133">-Tier</span><span class="sxs-lookup"><span data-stu-id="bbe29-133">-Tier</span></span>
<span data-ttu-id="bbe29-134">A camada de compromisso desejada para essa conta ser usada.</span><span class="sxs-lookup"><span data-stu-id="bbe29-134">The desired commitment tier for this account to use.</span></span>

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

### <span data-ttu-id="bbe29-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bbe29-135">CommonParameters</span></span>
<span data-ttu-id="bbe29-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bbe29-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bbe29-137">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bbe29-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bbe29-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bbe29-138">INPUTS</span></span>

### <span data-ttu-id="bbe29-139">System.String</span><span class="sxs-lookup"><span data-stu-id="bbe29-139">System.String</span></span>

### <span data-ttu-id="bbe29-140">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="bbe29-140">System.Collections.Hashtable</span></span>

### <span data-ttu-id="bbe29-141">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="bbe29-141">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="bbe29-142">System.Nullable'1[[Microsoft.Azure.Management.DataLake.Analytics.Models.TierType, Microsoft.Azure.Management.DataLake.Analytics, Version=3.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="bbe29-142">System.Nullable\`1[[Microsoft.Azure.Management.DataLake.Analytics.Models.TierType, Microsoft.Azure.Management.DataLake.Analytics, Version=3.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="bbe29-143">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="bbe29-143">OUTPUTS</span></span>

### <span data-ttu-id="bbe29-144">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="bbe29-144">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="bbe29-145">NOTES</span><span class="sxs-lookup"><span data-stu-id="bbe29-145">NOTES</span></span>

## <span data-ttu-id="bbe29-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bbe29-146">RELATED LINKS</span></span>

[<span data-ttu-id="bbe29-147">Get-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="bbe29-147">Get-AzDataLakeAnalyticsAccount</span></span>](./Get-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="bbe29-148">Remove-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="bbe29-148">Remove-AzDataLakeAnalyticsAccount</span></span>](./Remove-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="bbe29-149">Set-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="bbe29-149">Set-AzDataLakeAnalyticsAccount</span></span>](./Set-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="bbe29-150">Test-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="bbe29-150">Test-AzDataLakeAnalyticsAccount</span></span>](./Test-AzDataLakeAnalyticsAccount.md)



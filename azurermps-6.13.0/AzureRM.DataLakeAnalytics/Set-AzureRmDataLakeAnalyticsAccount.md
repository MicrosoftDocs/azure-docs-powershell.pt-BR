---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 8B10E476-F283-4BDC-BFAD-A33F8EC38341
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/set-azurermdatalakeanalyticsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Set-AzureRmDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Set-AzureRmDataLakeAnalyticsAccount.md
ms.openlocfilehash: 4bfbb25fa8b1e372175f741fd298384caa8050ef
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432006"
---
# <span data-ttu-id="d91a1-101">Set-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="d91a1-101">Set-AzureRmDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="d91a1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d91a1-102">SYNOPSIS</span></span>
<span data-ttu-id="d91a1-103">Modifica uma conta do data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="d91a1-103">Modifies a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d91a1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d91a1-104">SYNTAX</span></span>

```
Set-AzureRmDataLakeAnalyticsAccount [-Name] <String> [[-Tag] <Hashtable>] [[-ResourceGroupName] <String>]
 [-MaxAnalyticsUnits <Int32>] [-MaxJobCount <Int32>] [-QueryStoreRetention <Int32>] [-Tier <TierType>]
 [-FirewallState <FirewallState>] [-AllowAzureIpState <FirewallAllowAzureIpsState>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d91a1-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d91a1-105">DESCRIPTION</span></span>
<span data-ttu-id="d91a1-106">O cmdlet **set-AzureRmDataLakeAnalyticsAccount** modifica uma conta do Azure data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="d91a1-106">The **Set-AzureRmDataLakeAnalyticsAccount** cmdlet modifies an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="d91a1-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d91a1-107">EXAMPLES</span></span>

### <span data-ttu-id="d91a1-108">Exemplo 1: modificar a fonte de dados de uma conta</span><span class="sxs-lookup"><span data-stu-id="d91a1-108">Example 1: Modify the data source of an account</span></span>
```
PS C:\>Set-AzureRmDataLakeAnalyticsAccount -Name "ContosoAdlAcct" -DefaultDataLakeStore "ContosoAdlStore01" -Tags @{"stage"="production"}
```

<span data-ttu-id="d91a1-109">Esse comando altera a fonte de dados padrão e a propriedade Tags da conta.</span><span class="sxs-lookup"><span data-stu-id="d91a1-109">This command changes the default data source and the Tags property of the account.</span></span>

## <span data-ttu-id="d91a1-110">OS</span><span class="sxs-lookup"><span data-stu-id="d91a1-110">PARAMETERS</span></span>

### <span data-ttu-id="d91a1-111">-AllowAzureIpState</span><span class="sxs-lookup"><span data-stu-id="d91a1-111">-AllowAzureIpState</span></span>
<span data-ttu-id="d91a1-112">Opcionalmente, permitir/bloquear IPs de origem do Azure por meio do firewall.</span><span class="sxs-lookup"><span data-stu-id="d91a1-112">Optionally allow/block Azure originating IPs through the firewall.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.DataLake.Analytics.Models.FirewallAllowAzureIpsState]
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d91a1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d91a1-113">-DefaultProfile</span></span>
<span data-ttu-id="d91a1-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="d91a1-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d91a1-115">-Firewallstate</span><span class="sxs-lookup"><span data-stu-id="d91a1-115">-FirewallState</span></span>
<span data-ttu-id="d91a1-116">Opcionalmente, habilite/desabilite regras de firewall existentes.</span><span class="sxs-lookup"><span data-stu-id="d91a1-116">Optionally enable/disable existing firewall rules.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.DataLake.Analytics.Models.FirewallState]
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d91a1-117">-MaxAnalyticsUnits</span><span class="sxs-lookup"><span data-stu-id="d91a1-117">-MaxAnalyticsUnits</span></span>
<span data-ttu-id="d91a1-118">As unidades de análise máxima suportadas para atualizar a conta.</span><span class="sxs-lookup"><span data-stu-id="d91a1-118">The optional maximum supported analytics units to update the account with.</span></span>

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

### <span data-ttu-id="d91a1-119">-MaxJobCount</span><span class="sxs-lookup"><span data-stu-id="d91a1-119">-MaxJobCount</span></span>
<span data-ttu-id="d91a1-120">O máximo de trabalhos opcionais com suporte em execução na conta ao mesmo tempo para definir.</span><span class="sxs-lookup"><span data-stu-id="d91a1-120">The optional maximum supported jobs running under the account at the same time to set.</span></span>

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

### <span data-ttu-id="d91a1-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="d91a1-121">-Name</span></span>
<span data-ttu-id="d91a1-122">Especifica o nome da conta do data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="d91a1-122">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="d91a1-123">-QueryStoreRetention</span><span class="sxs-lookup"><span data-stu-id="d91a1-123">-QueryStoreRetention</span></span>
<span data-ttu-id="d91a1-124">O número opcional de dias pelos quais os metadados do trabalho são mantidos para serem definidos na conta.</span><span class="sxs-lookup"><span data-stu-id="d91a1-124">The optional number of days that job metadata is retained to set in the account.</span></span>

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

### <span data-ttu-id="d91a1-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d91a1-125">-ResourceGroupName</span></span>
<span data-ttu-id="d91a1-126">Especifica o nome do grupo de recursos da conta do data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="d91a1-126">Specifies the resource group name of the Data Lake Analytics account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d91a1-127">-Marca</span><span class="sxs-lookup"><span data-stu-id="d91a1-127">-Tag</span></span>
<span data-ttu-id="d91a1-128">Uma cadeia de caracteres, dicionário de cadeias de caracteres de marcas associadas a essa conta que deve substituir o conjunto atual de marcas</span><span class="sxs-lookup"><span data-stu-id="d91a1-128">A string,string dictionary of tags associated with this account that should replace the current set of tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d91a1-129">-Tier</span><span class="sxs-lookup"><span data-stu-id="d91a1-129">-Tier</span></span>
<span data-ttu-id="d91a1-130">A camada de compromisso desejada para esta conta usar.</span><span class="sxs-lookup"><span data-stu-id="d91a1-130">The desired commitment tier for this account to use.</span></span>

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

### <span data-ttu-id="d91a1-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d91a1-131">CommonParameters</span></span>
<span data-ttu-id="d91a1-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d91a1-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d91a1-133">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d91a1-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d91a1-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d91a1-134">INPUTS</span></span>

### <span data-ttu-id="d91a1-135">System. String</span><span class="sxs-lookup"><span data-stu-id="d91a1-135">System.String</span></span>

### <span data-ttu-id="d91a1-136">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="d91a1-136">System.Collections.Hashtable</span></span>

### <span data-ttu-id="d91a1-137">System. Nullable ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="d91a1-137">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="d91a1-138">System. Nullable ' 1 [[Microsoft. Azure. Management. datalake. remanagement. Models. Tiertype, Microsoft. Azure. Management. datalake. Analytics, Version = 3.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="d91a1-138">System.Nullable\`1[[Microsoft.Azure.Management.DataLake.Analytics.Models.TierType, Microsoft.Azure.Management.DataLake.Analytics, Version=3.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="d91a1-139">System. Nullable ' 1 [[Microsoft. Azure. Management. datalake. Analytics. Models. Firewallstate, Microsoft. Azure. Management. datalake. Analytics, Version = 3.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="d91a1-139">System.Nullable\`1[[Microsoft.Azure.Management.DataLake.Analytics.Models.FirewallState, Microsoft.Azure.Management.DataLake.Analytics, Version=3.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="d91a1-140">System. Nullable ' 1 [[Microsoft. Azure. Management. datalake. Analytics. Models. FirewallAllowAzureIpsState, Microsoft. Azure. Management. datalake. Analytics, Version = 3.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="d91a1-140">System.Nullable\`1[[Microsoft.Azure.Management.DataLake.Analytics.Models.FirewallAllowAzureIpsState, Microsoft.Azure.Management.DataLake.Analytics, Version=3.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="d91a1-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d91a1-141">OUTPUTS</span></span>

### <span data-ttu-id="d91a1-142">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="d91a1-142">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="d91a1-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d91a1-143">NOTES</span></span>

## <span data-ttu-id="d91a1-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d91a1-144">RELATED LINKS</span></span>

[<span data-ttu-id="d91a1-145">Get-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="d91a1-145">Get-AzureRmDataLakeAnalyticsAccount</span></span>](./Get-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="d91a1-146">New-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="d91a1-146">New-AzureRmDataLakeAnalyticsAccount</span></span>](./New-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="d91a1-147">Remove-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="d91a1-147">Remove-AzureRmDataLakeAnalyticsAccount</span></span>](./Remove-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="d91a1-148">Test-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="d91a1-148">Test-AzureRmDataLakeAnalyticsAccount</span></span>](./Test-AzureRmDataLakeAnalyticsAccount.md)



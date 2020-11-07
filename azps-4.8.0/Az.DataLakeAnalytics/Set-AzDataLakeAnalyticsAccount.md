---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: 8B10E476-F283-4BDC-BFAD-A33F8EC38341
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/set-azdatalakeanalyticsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Set-AzDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Set-AzDataLakeAnalyticsAccount.md
ms.openlocfilehash: 2a762bb115132f97dd31cf14f9f13d7c6cf5ef70
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93955636"
---
# <span data-ttu-id="62718-101">Set-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="62718-101">Set-AzDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="62718-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="62718-102">SYNOPSIS</span></span>
<span data-ttu-id="62718-103">Modifica uma conta do data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="62718-103">Modifies a Data Lake Analytics account.</span></span>

## <span data-ttu-id="62718-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="62718-104">SYNTAX</span></span>

```
Set-AzDataLakeAnalyticsAccount [-Name] <String> [[-Tag] <Hashtable>] [[-ResourceGroupName] <String>]
 [-MaxAnalyticsUnits <Int32>] [-MaxJobCount <Int32>] [-QueryStoreRetention <Int32>] [-Tier <TierType>]
 [-FirewallState <FirewallState>] [-AllowAzureIpState <FirewallAllowAzureIpsState>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="62718-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="62718-105">DESCRIPTION</span></span>
<span data-ttu-id="62718-106">O cmdlet **set-AzDataLakeAnalyticsAccount** modifica uma conta do Azure data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="62718-106">The **Set-AzDataLakeAnalyticsAccount** cmdlet modifies an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="62718-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="62718-107">EXAMPLES</span></span>

### <span data-ttu-id="62718-108">Exemplo 1: modificar a fonte de dados de uma conta</span><span class="sxs-lookup"><span data-stu-id="62718-108">Example 1: Modify the data source of an account</span></span>
```
PS C:\>Set-AzDataLakeAnalyticsAccount -Name "ContosoAdlAcct" -DefaultDataLakeStore "ContosoAdlStore01" -Tags @{"stage"="production"}
```

<span data-ttu-id="62718-109">Esse comando altera a fonte de dados padrão e a propriedade Tags da conta.</span><span class="sxs-lookup"><span data-stu-id="62718-109">This command changes the default data source and the Tags property of the account.</span></span>

## <span data-ttu-id="62718-110">OS</span><span class="sxs-lookup"><span data-stu-id="62718-110">PARAMETERS</span></span>

### <span data-ttu-id="62718-111">-AllowAzureIpState</span><span class="sxs-lookup"><span data-stu-id="62718-111">-AllowAzureIpState</span></span>
<span data-ttu-id="62718-112">Opcionalmente, permitir/bloquear IPs de origem do Azure por meio do firewall.</span><span class="sxs-lookup"><span data-stu-id="62718-112">Optionally allow/block Azure originating IPs through the firewall.</span></span>

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

### <span data-ttu-id="62718-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62718-113">-DefaultProfile</span></span>
<span data-ttu-id="62718-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="62718-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="62718-115">-Firewallstate</span><span class="sxs-lookup"><span data-stu-id="62718-115">-FirewallState</span></span>
<span data-ttu-id="62718-116">Opcionalmente, habilite/desabilite regras de firewall existentes.</span><span class="sxs-lookup"><span data-stu-id="62718-116">Optionally enable/disable existing firewall rules.</span></span>

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

### <span data-ttu-id="62718-117">-MaxAnalyticsUnits</span><span class="sxs-lookup"><span data-stu-id="62718-117">-MaxAnalyticsUnits</span></span>
<span data-ttu-id="62718-118">As unidades de análise máxima suportadas para atualizar a conta.</span><span class="sxs-lookup"><span data-stu-id="62718-118">The optional maximum supported analytics units to update the account with.</span></span>

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

### <span data-ttu-id="62718-119">-MaxJobCount</span><span class="sxs-lookup"><span data-stu-id="62718-119">-MaxJobCount</span></span>
<span data-ttu-id="62718-120">O máximo de trabalhos opcionais com suporte em execução na conta ao mesmo tempo para definir.</span><span class="sxs-lookup"><span data-stu-id="62718-120">The optional maximum supported jobs running under the account at the same time to set.</span></span>

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

### <span data-ttu-id="62718-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="62718-121">-Name</span></span>
<span data-ttu-id="62718-122">Especifica o nome da conta do data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="62718-122">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="62718-123">-QueryStoreRetention</span><span class="sxs-lookup"><span data-stu-id="62718-123">-QueryStoreRetention</span></span>
<span data-ttu-id="62718-124">O número opcional de dias pelos quais os metadados do trabalho são mantidos para serem definidos na conta.</span><span class="sxs-lookup"><span data-stu-id="62718-124">The optional number of days that job metadata is retained to set in the account.</span></span>

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

### <span data-ttu-id="62718-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62718-125">-ResourceGroupName</span></span>
<span data-ttu-id="62718-126">Especifica o nome do grupo de recursos da conta do data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="62718-126">Specifies the resource group name of the Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="62718-127">-Marca</span><span class="sxs-lookup"><span data-stu-id="62718-127">-Tag</span></span>
<span data-ttu-id="62718-128">Uma cadeia de caracteres, dicionário de cadeias de caracteres de marcas associadas a essa conta que deve substituir o conjunto atual de marcas</span><span class="sxs-lookup"><span data-stu-id="62718-128">A string,string dictionary of tags associated with this account that should replace the current set of tags</span></span>

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

### <span data-ttu-id="62718-129">-Tier</span><span class="sxs-lookup"><span data-stu-id="62718-129">-Tier</span></span>
<span data-ttu-id="62718-130">A camada de compromisso desejada para esta conta usar.</span><span class="sxs-lookup"><span data-stu-id="62718-130">The desired commitment tier for this account to use.</span></span>

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

### <span data-ttu-id="62718-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62718-131">CommonParameters</span></span>
<span data-ttu-id="62718-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62718-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62718-133">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="62718-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62718-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="62718-134">INPUTS</span></span>

### <span data-ttu-id="62718-135">System. String</span><span class="sxs-lookup"><span data-stu-id="62718-135">System.String</span></span>

### <span data-ttu-id="62718-136">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="62718-136">System.Collections.Hashtable</span></span>

### <span data-ttu-id="62718-137">System. Nullable ' 1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="62718-137">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="62718-138">System. Nullable ' 1 [[Microsoft. Azure. Management. datalake. remanagement. Models. Tiertype, Microsoft. Azure. Management. datalake. Analytics, Version = 3.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="62718-138">System.Nullable\`1[[Microsoft.Azure.Management.DataLake.Analytics.Models.TierType, Microsoft.Azure.Management.DataLake.Analytics, Version=3.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="62718-139">System. Nullable ' 1 [[Microsoft. Azure. Management. datalake. Analytics. Models. Firewallstate, Microsoft. Azure. Management. datalake. Analytics, Version = 3.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="62718-139">System.Nullable\`1[[Microsoft.Azure.Management.DataLake.Analytics.Models.FirewallState, Microsoft.Azure.Management.DataLake.Analytics, Version=3.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="62718-140">System. Nullable ' 1 [[Microsoft. Azure. Management. datalake. Analytics. Models. FirewallAllowAzureIpsState, Microsoft. Azure. Management. datalake. Analytics, Version = 3.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="62718-140">System.Nullable\`1[[Microsoft.Azure.Management.DataLake.Analytics.Models.FirewallAllowAzureIpsState, Microsoft.Azure.Management.DataLake.Analytics, Version=3.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="62718-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="62718-141">OUTPUTS</span></span>

### <span data-ttu-id="62718-142">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="62718-142">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="62718-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="62718-143">NOTES</span></span>

## <span data-ttu-id="62718-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="62718-144">RELATED LINKS</span></span>

[<span data-ttu-id="62718-145">Get-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="62718-145">Get-AzDataLakeAnalyticsAccount</span></span>](./Get-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="62718-146">New-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="62718-146">New-AzDataLakeAnalyticsAccount</span></span>](./New-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="62718-147">Remove-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="62718-147">Remove-AzDataLakeAnalyticsAccount</span></span>](./Remove-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="62718-148">Test-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="62718-148">Test-AzDataLakeAnalyticsAccount</span></span>](./Test-AzDataLakeAnalyticsAccount.md)



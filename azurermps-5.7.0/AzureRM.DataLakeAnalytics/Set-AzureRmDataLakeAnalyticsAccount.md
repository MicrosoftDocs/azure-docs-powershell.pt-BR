---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 8B10E476-F283-4BDC-BFAD-A33F8EC38341
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/set-azurermdatalakeanalyticsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Set-AzureRmDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Set-AzureRmDataLakeAnalyticsAccount.md
ms.openlocfilehash: 8ca5efc7e5cee80fdf7ce34a13ce23ac733c0154
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429824"
---
# <span data-ttu-id="6ca3f-101">Set-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="6ca3f-101">Set-AzureRmDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="6ca3f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6ca3f-102">SYNOPSIS</span></span>
<span data-ttu-id="6ca3f-103">Modifica uma conta do data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="6ca3f-103">Modifies a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6ca3f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6ca3f-104">SYNTAX</span></span>

```
Set-AzureRmDataLakeAnalyticsAccount [-Name] <String> [[-Tag] <Hashtable>] [[-ResourceGroupName] <String>]
 [-MaxAnalyticsUnits <Int32>] [-MaxJobCount <Int32>] [-QueryStoreRetention <Int32>] [-Tier <TierType>]
 [-FirewallState <FirewallState>] [-AllowAzureIpState <FirewallAllowAzureIpsState>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6ca3f-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6ca3f-105">DESCRIPTION</span></span>
<span data-ttu-id="6ca3f-106">O cmdlet **set-AzureRmDataLakeAnalyticsAccount** modifica uma conta do Azure data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="6ca3f-106">The **Set-AzureRmDataLakeAnalyticsAccount** cmdlet modifies an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="6ca3f-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6ca3f-107">EXAMPLES</span></span>

### <span data-ttu-id="6ca3f-108">Exemplo 1: modificar a fonte de dados de uma conta</span><span class="sxs-lookup"><span data-stu-id="6ca3f-108">Example 1: Modify the data source of an account</span></span>
```
PS C:\>Set-AzureRmDataLakeAnalyticsAccount -Name "ContosoAdlAcct" -DefaultDataLakeStore "ContosoAdlStore01" -Tags @{"stage"="production"}
```

<span data-ttu-id="6ca3f-109">Esse comando altera a fonte de dados padrão e a propriedade Tags da conta.</span><span class="sxs-lookup"><span data-stu-id="6ca3f-109">This command changes the default data source and the Tags property of the account.</span></span>

## <span data-ttu-id="6ca3f-110">OS</span><span class="sxs-lookup"><span data-stu-id="6ca3f-110">PARAMETERS</span></span>

### <span data-ttu-id="6ca3f-111">-AllowAzureIpState</span><span class="sxs-lookup"><span data-stu-id="6ca3f-111">-AllowAzureIpState</span></span>
<span data-ttu-id="6ca3f-112">Opcionalmente, permitir/bloquear IPs de origem do Azure por meio do firewall.</span><span class="sxs-lookup"><span data-stu-id="6ca3f-112">Optionally allow/block Azure originating IPs through the firewall.</span></span>

```yaml
Type: FirewallAllowAzureIpsState
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ca3f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ca3f-113">-DefaultProfile</span></span>
<span data-ttu-id="6ca3f-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="6ca3f-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6ca3f-115">-Firewallstate</span><span class="sxs-lookup"><span data-stu-id="6ca3f-115">-FirewallState</span></span>
<span data-ttu-id="6ca3f-116">Opcionalmente, habilite/desabilite regras de firewall existentes.</span><span class="sxs-lookup"><span data-stu-id="6ca3f-116">Optionally enable/disable existing firewall rules.</span></span>

```yaml
Type: FirewallState
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ca3f-117">-MaxAnalyticsUnits</span><span class="sxs-lookup"><span data-stu-id="6ca3f-117">-MaxAnalyticsUnits</span></span>
<span data-ttu-id="6ca3f-118">As unidades de análise máxima suportadas para atualizar a conta.</span><span class="sxs-lookup"><span data-stu-id="6ca3f-118">The optional maximum supported analytics units to update the account with.</span></span>

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

### <span data-ttu-id="6ca3f-119">-MaxJobCount</span><span class="sxs-lookup"><span data-stu-id="6ca3f-119">-MaxJobCount</span></span>
<span data-ttu-id="6ca3f-120">O máximo de trabalhos opcionais com suporte em execução na conta ao mesmo tempo para definir.</span><span class="sxs-lookup"><span data-stu-id="6ca3f-120">The optional maximum supported jobs running under the account at the same time to set.</span></span>

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

### <span data-ttu-id="6ca3f-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="6ca3f-121">-Name</span></span>
<span data-ttu-id="6ca3f-122">Especifica o nome da conta do data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="6ca3f-122">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="6ca3f-123">-QueryStoreRetention</span><span class="sxs-lookup"><span data-stu-id="6ca3f-123">-QueryStoreRetention</span></span>
<span data-ttu-id="6ca3f-124">O número opcional de dias pelos quais os metadados do trabalho são mantidos para serem definidos na conta.</span><span class="sxs-lookup"><span data-stu-id="6ca3f-124">The optional number of days that job metadata is retained to set in the account.</span></span>

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

### <span data-ttu-id="6ca3f-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ca3f-125">-ResourceGroupName</span></span>
<span data-ttu-id="6ca3f-126">Especifica o nome do grupo de recursos da conta do data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="6ca3f-126">Specifies the resource group name of the Data Lake Analytics account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ca3f-127">-Marca</span><span class="sxs-lookup"><span data-stu-id="6ca3f-127">-Tag</span></span>
<span data-ttu-id="6ca3f-128">Uma cadeia de caracteres, dicionário de cadeias de caracteres de marcas associadas a essa conta que deve substituir o conjunto atual de marcas</span><span class="sxs-lookup"><span data-stu-id="6ca3f-128">A string,string dictionary of tags associated with this account that should replace the current set of tags</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ca3f-129">-Tier</span><span class="sxs-lookup"><span data-stu-id="6ca3f-129">-Tier</span></span>
<span data-ttu-id="6ca3f-130">A camada de compromisso desejada para esta conta usar.</span><span class="sxs-lookup"><span data-stu-id="6ca3f-130">The desired commitment tier for this account to use.</span></span>

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

### <span data-ttu-id="6ca3f-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ca3f-131">CommonParameters</span></span>
<span data-ttu-id="6ca3f-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ca3f-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ca3f-133">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ca3f-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ca3f-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6ca3f-134">INPUTS</span></span>

### <span data-ttu-id="6ca3f-135">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="6ca3f-135">None</span></span>
<span data-ttu-id="6ca3f-136">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="6ca3f-136">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6ca3f-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6ca3f-137">OUTPUTS</span></span>

### <span data-ttu-id="6ca3f-138">PSDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="6ca3f-138">PSDataLakeAnalyticsAccount</span></span>
<span data-ttu-id="6ca3f-139">Os detalhes da conta atualizados.</span><span class="sxs-lookup"><span data-stu-id="6ca3f-139">The updated account details.</span></span>

## <span data-ttu-id="6ca3f-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6ca3f-140">NOTES</span></span>

## <span data-ttu-id="6ca3f-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6ca3f-141">RELATED LINKS</span></span>

[<span data-ttu-id="6ca3f-142">Get-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="6ca3f-142">Get-AzureRmDataLakeAnalyticsAccount</span></span>](./Get-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="6ca3f-143">New-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="6ca3f-143">New-AzureRmDataLakeAnalyticsAccount</span></span>](./New-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="6ca3f-144">Remove-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="6ca3f-144">Remove-AzureRmDataLakeAnalyticsAccount</span></span>](./Remove-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="6ca3f-145">Test-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="6ca3f-145">Test-AzureRmDataLakeAnalyticsAccount</span></span>](./Test-AzureRmDataLakeAnalyticsAccount.md)



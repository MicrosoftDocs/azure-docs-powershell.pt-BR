---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 8B10E476-F283-4BDC-BFAD-A33F8EC38341
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Set-AzureRmDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Set-AzureRmDataLakeAnalyticsAccount.md
ms.openlocfilehash: 8de6b2a0d86c9eb83a067f4982a5ef62d3a9adbf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427963"
---
# <span data-ttu-id="99d6a-101">Set-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="99d6a-101">Set-AzureRmDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="99d6a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="99d6a-102">SYNOPSIS</span></span>
<span data-ttu-id="99d6a-103">Modifica uma conta do data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="99d6a-103">Modifies a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="99d6a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="99d6a-104">SYNTAX</span></span>

```
Set-AzureRmDataLakeAnalyticsAccount [-Name] <String> [[-Tags] <Hashtable>] [[-ResourceGroupName] <String>]
 [-MaxDegreeOfParallelism <Int32>] [-MaxJobCount <Int32>] [-QueryStoreRetention <Int32>] [-Tier <TierType>]
 [-FirewallState <FirewallState>] [-AllowAzureIpState <FirewallAllowAzureIpsState>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="99d6a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="99d6a-105">DESCRIPTION</span></span>
<span data-ttu-id="99d6a-106">O cmdlet **set-AzureRmDataLakeAnalyticsAccount** modifica uma conta do Azure data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="99d6a-106">The **Set-AzureRmDataLakeAnalyticsAccount** cmdlet modifies an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="99d6a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="99d6a-107">EXAMPLES</span></span>

### <span data-ttu-id="99d6a-108">Exemplo 1: modificar a fonte de dados de uma conta</span><span class="sxs-lookup"><span data-stu-id="99d6a-108">Example 1: Modify the data source of an account</span></span>
```
PS C:\>Set-AzureRmDataLakeAnalyticsAccount -Name "ContosoAdlAcct" -DefaultDataLakeStore "ContosoAdlStore01" -Tags @{"stage"="production"}
```

<span data-ttu-id="99d6a-109">Esse comando altera a fonte de dados padrão e a propriedade Tags da conta.</span><span class="sxs-lookup"><span data-stu-id="99d6a-109">This command changes the default data source and the Tags property of the account.</span></span>

## <span data-ttu-id="99d6a-110">OS</span><span class="sxs-lookup"><span data-stu-id="99d6a-110">PARAMETERS</span></span>

### <span data-ttu-id="99d6a-111">-AllowAzureIpState</span><span class="sxs-lookup"><span data-stu-id="99d6a-111">-AllowAzureIpState</span></span>
<span data-ttu-id="99d6a-112">Opcionalmente, permitir/bloquear IPs de origem do Azure por meio do firewall.</span><span class="sxs-lookup"><span data-stu-id="99d6a-112">Optionally allow/block Azure originating IPs through the firewall.</span></span>

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

### <span data-ttu-id="99d6a-113">-Firewallstate</span><span class="sxs-lookup"><span data-stu-id="99d6a-113">-FirewallState</span></span>
<span data-ttu-id="99d6a-114">Opcionalmente, habilite/desabilite regras de firewall existentes.</span><span class="sxs-lookup"><span data-stu-id="99d6a-114">Optionally enable/disable existing firewall rules.</span></span>

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

### <span data-ttu-id="99d6a-115">-MaxDegreeOfParallelism</span><span class="sxs-lookup"><span data-stu-id="99d6a-115">-MaxDegreeOfParallelism</span></span>
<span data-ttu-id="99d6a-116">O grau máximo de suporte opcional de paralelismo para atualizar a conta com.</span><span class="sxs-lookup"><span data-stu-id="99d6a-116">The optional maximum supported degree of parallelism to update the account with.</span></span>

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

### <span data-ttu-id="99d6a-117">-MaxJobCount</span><span class="sxs-lookup"><span data-stu-id="99d6a-117">-MaxJobCount</span></span>
<span data-ttu-id="99d6a-118">O máximo de trabalhos opcionais com suporte em execução na conta ao mesmo tempo para definir.</span><span class="sxs-lookup"><span data-stu-id="99d6a-118">The optional maximum supported jobs running under the account at the same time to set.</span></span>

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

### <span data-ttu-id="99d6a-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="99d6a-119">-Name</span></span>
<span data-ttu-id="99d6a-120">Especifica o nome da conta do data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="99d6a-120">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="99d6a-121">-QueryStoreRetention</span><span class="sxs-lookup"><span data-stu-id="99d6a-121">-QueryStoreRetention</span></span>
<span data-ttu-id="99d6a-122">O número opcional de dias pelos quais os metadados do trabalho são mantidos para serem definidos na conta.</span><span class="sxs-lookup"><span data-stu-id="99d6a-122">The optional number of days that job metadata is retained to set in the account.</span></span>

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

### <span data-ttu-id="99d6a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99d6a-123">-ResourceGroupName</span></span>
<span data-ttu-id="99d6a-124">Especifica o nome do grupo de recursos da conta do data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="99d6a-124">Specifies the resource group name of the Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="99d6a-125">-Marcas</span><span class="sxs-lookup"><span data-stu-id="99d6a-125">-Tags</span></span>
<span data-ttu-id="99d6a-126">Especifica os pares de valores chave que podem ser usados para identificar a conta do data Lake Analytics entre outros recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="99d6a-126">Specifies key-value pairs that can be used to identify the Data Lake Analytics account among other Azure resources.</span></span>

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

### <span data-ttu-id="99d6a-127">-Tier</span><span class="sxs-lookup"><span data-stu-id="99d6a-127">-Tier</span></span>
<span data-ttu-id="99d6a-128">A camada de compromisso desejada para esta conta usar.</span><span class="sxs-lookup"><span data-stu-id="99d6a-128">The desired commitment tier for this account to use.</span></span>

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

### <span data-ttu-id="99d6a-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99d6a-129">-DefaultProfile</span></span>
<span data-ttu-id="99d6a-130">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="99d6a-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="99d6a-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99d6a-131">CommonParameters</span></span>
<span data-ttu-id="99d6a-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99d6a-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99d6a-133">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="99d6a-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99d6a-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="99d6a-134">INPUTS</span></span>

## <span data-ttu-id="99d6a-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="99d6a-135">OUTPUTS</span></span>

### <span data-ttu-id="99d6a-136">PSDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="99d6a-136">PSDataLakeAnalyticsAccount</span></span>
<span data-ttu-id="99d6a-137">Os detalhes da conta atualizados.</span><span class="sxs-lookup"><span data-stu-id="99d6a-137">The updated account details.</span></span>

## <span data-ttu-id="99d6a-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="99d6a-138">NOTES</span></span>

## <span data-ttu-id="99d6a-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="99d6a-139">RELATED LINKS</span></span>

[<span data-ttu-id="99d6a-140">Get-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="99d6a-140">Get-AzureRmDataLakeAnalyticsAccount</span></span>](./Get-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="99d6a-141">New-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="99d6a-141">New-AzureRmDataLakeAnalyticsAccount</span></span>](./New-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="99d6a-142">Remove-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="99d6a-142">Remove-AzureRmDataLakeAnalyticsAccount</span></span>](./Remove-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="99d6a-143">Test-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="99d6a-143">Test-AzureRmDataLakeAnalyticsAccount</span></span>](./Test-AzureRmDataLakeAnalyticsAccount.md)



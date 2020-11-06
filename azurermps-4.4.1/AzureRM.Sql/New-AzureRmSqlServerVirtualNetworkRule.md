---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServerVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServerVirtualNetworkRule.md
ms.openlocfilehash: 08d14217cff370557009167e09cd7e5396df4e2c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427744"
---
# <span data-ttu-id="849e6-101">New-AzureRmSqlServerVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="849e6-101">New-AzureRmSqlServerVirtualNetworkRule</span></span>

## <span data-ttu-id="849e6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="849e6-102">SYNOPSIS</span></span>
<span data-ttu-id="849e6-103">Cria uma regra de rede virtual do SQL Server do Azure.</span><span class="sxs-lookup"><span data-stu-id="849e6-103">Creates an Azure SQL Server Virtual Network Rule.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="849e6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="849e6-104">SYNTAX</span></span>

```
New-AzureRmSqlServerVirtualNetworkRule -VirtualNetworkRuleName <String> -VirtualNetworkSubnetId <String>
 -ServerName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="849e6-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="849e6-105">DESCRIPTION</span></span>
<span data-ttu-id="849e6-106">Cria uma regra de rede virtual do SQL Server do Azure.</span><span class="sxs-lookup"><span data-stu-id="849e6-106">Creates an Azure SQL Server Virtual Network Rule.</span></span> <span data-ttu-id="849e6-107">As regras de rede virtual são usadas para conectar o SQL Server do Azure a uma rede virtual específica a fim de restringir o acesso no SQL Server do Azure apenas para estar disponível na rede virtual.</span><span class="sxs-lookup"><span data-stu-id="849e6-107">Virtual Network Rules are used to connect the Azure SQL Server to a specific Virtual Network in order to restrict the access on the Azure SQL Server to only be available within the Virtual Network.</span></span> 

## <span data-ttu-id="849e6-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="849e6-108">EXAMPLES</span></span>

### <span data-ttu-id="849e6-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="849e6-109">Example 1</span></span>
```
PS C:\> $virtualNetworkRule = New-AzureRmSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRuleName -VirtualNetworkSubnetId virtualNetworkSubnetId
```

<span data-ttu-id="849e6-110">Cria uma regra de rede virtual do SQL Server do Azure</span><span class="sxs-lookup"><span data-stu-id="849e6-110">Creates an Azure SQL Server virtual network rule</span></span>

## <span data-ttu-id="849e6-111">OS</span><span class="sxs-lookup"><span data-stu-id="849e6-111">PARAMETERS</span></span>

### <span data-ttu-id="849e6-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="849e6-112">-ResourceGroupName</span></span>
<span data-ttu-id="849e6-113">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="849e6-113">The name of the resource group.</span></span>

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

### <span data-ttu-id="849e6-114">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="849e6-114">-ServerName</span></span>
<span data-ttu-id="849e6-115">O nome do SQL Server do Azure.</span><span class="sxs-lookup"><span data-stu-id="849e6-115">The Azure Sql Server name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="849e6-116">-VirtualNetworkRuleName</span><span class="sxs-lookup"><span data-stu-id="849e6-116">-VirtualNetworkRuleName</span></span>
<span data-ttu-id="849e6-117">Nome da regra de rede virtual do SQL Server do Azure.</span><span class="sxs-lookup"><span data-stu-id="849e6-117">Azure Sql Server Virtual Network Rule Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="849e6-118">-VirtualNetworkSubnetId</span><span class="sxs-lookup"><span data-stu-id="849e6-118">-VirtualNetworkSubnetId</span></span>
<span data-ttu-id="849e6-119">A ID de sub-rede da rede virtual que especifica os detalhes da Microsoft. Network</span><span class="sxs-lookup"><span data-stu-id="849e6-119">The Virtual Network Subnet Id that specifies the Microsoft.Network details</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="849e6-120">-Confirme</span><span class="sxs-lookup"><span data-stu-id="849e6-120">-Confirm</span></span>
<span data-ttu-id="849e6-121">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="849e6-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="849e6-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="849e6-122">-WhatIf</span></span>
<span data-ttu-id="849e6-123">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="849e6-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="849e6-124">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="849e6-124">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="849e6-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="849e6-125">-DefaultProfile</span></span>
<span data-ttu-id="849e6-126">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="849e6-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="849e6-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="849e6-127">CommonParameters</span></span>
<span data-ttu-id="849e6-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="849e6-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="849e6-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="849e6-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="849e6-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="849e6-130">INPUTS</span></span>

### <span data-ttu-id="849e6-131">System. String</span><span class="sxs-lookup"><span data-stu-id="849e6-131">System.String</span></span>

## <span data-ttu-id="849e6-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="849e6-132">OUTPUTS</span></span>

### <span data-ttu-id="849e6-133">Microsoft. Azure. Commands. Sql. VirtualNetworkRule. Model. AzureSqlServerVirtualNetworkRuleModel</span><span class="sxs-lookup"><span data-stu-id="849e6-133">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span></span>

## <span data-ttu-id="849e6-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="849e6-134">NOTES</span></span>

## <span data-ttu-id="849e6-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="849e6-135">RELATED LINKS</span></span>


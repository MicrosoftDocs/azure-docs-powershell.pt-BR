---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerVirtualNetworkRule.md
ms.openlocfilehash: 355b8fdffd5d1e9e16fe9bfaf504d627a8b9b167
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610970"
---
# <span data-ttu-id="a73c6-101">Set-AzureRmSqlServerVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="a73c6-101">Set-AzureRmSqlServerVirtualNetworkRule</span></span>

## <span data-ttu-id="a73c6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a73c6-102">SYNOPSIS</span></span>
<span data-ttu-id="a73c6-103">Modifica a configuração de uma regra de rede virtual do Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="a73c6-103">Modifies the configuration of an Azure SQL Server Virtual Network Rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a73c6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a73c6-104">SYNTAX</span></span>

```
Set-AzureRmSqlServerVirtualNetworkRule -VirtualNetworkRuleName <String> -VirtualNetworkSubnetId <String>
 -ServerName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a73c6-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a73c6-105">DESCRIPTION</span></span>
<span data-ttu-id="a73c6-106">Esse comando modifica a configuração de uma regra de rede virtual do Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="a73c6-106">This command modifies the configuration of an Azure SQL Server Virtual Network Rule.</span></span>


<span data-ttu-id="a73c6-107">Para controlar o conjunto de regras de rede virtual no servidor, use "Add-AzureRmSqlServerVirtualNetworkRule" e "Remove-AzureRmSqlServerVirtualNetworkRule" em vez disso.</span><span class="sxs-lookup"><span data-stu-id="a73c6-107">To control the set of virtual network rules in the server, use 'Add-AzureRmSqlServerVirtualNetworkRule' and 'Remove-AzureRmSqlServerVirtualNetworkRule' instead.</span></span>

## <span data-ttu-id="a73c6-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a73c6-108">EXAMPLES</span></span>

### <span data-ttu-id="a73c6-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a73c6-109">Example 1</span></span>
```
PS C:\> $virtualNetworkRule = Set-AzureRmSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRuleName -VirtualNetworkSubnetId virtualNetworkSubnetId
```

<span data-ttu-id="a73c6-110">Modifica uma regra de rede virtual existente com a nova ID de sub-rede de rede virtual que contém informações sobre a nova rede virtual</span><span class="sxs-lookup"><span data-stu-id="a73c6-110">Modifies an existing virtual network rule with the new virtual network subnet id which contains information about the new virtual network</span></span>

## <span data-ttu-id="a73c6-111">OS</span><span class="sxs-lookup"><span data-stu-id="a73c6-111">PARAMETERS</span></span>

### <span data-ttu-id="a73c6-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a73c6-112">-ResourceGroupName</span></span>
<span data-ttu-id="a73c6-113">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a73c6-113">The name of the resource group.</span></span>

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

### <span data-ttu-id="a73c6-114">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="a73c6-114">-ServerName</span></span>
<span data-ttu-id="a73c6-115">O nome do SQL Server do Azure.</span><span class="sxs-lookup"><span data-stu-id="a73c6-115">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="a73c6-116">-VirtualNetworkRuleName</span><span class="sxs-lookup"><span data-stu-id="a73c6-116">-VirtualNetworkRuleName</span></span>
<span data-ttu-id="a73c6-117">O nome da regra de rede virtual do Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="a73c6-117">The name of the Azure Sql Server Virtual Network Rule.</span></span>

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

### <span data-ttu-id="a73c6-118">-VirtualNetworkSubnetId</span><span class="sxs-lookup"><span data-stu-id="a73c6-118">-VirtualNetworkSubnetId</span></span>
<span data-ttu-id="a73c6-119">A ID de sub-rede da rede virtual para a regra.</span><span class="sxs-lookup"><span data-stu-id="a73c6-119">The Virtual Network Subnet Id for the rule.</span></span>

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

### <span data-ttu-id="a73c6-120">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a73c6-120">-Confirm</span></span>
<span data-ttu-id="a73c6-121">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a73c6-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a73c6-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a73c6-122">-WhatIf</span></span>
<span data-ttu-id="a73c6-123">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a73c6-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a73c6-124">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a73c6-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a73c6-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a73c6-125">-DefaultProfile</span></span>
<span data-ttu-id="a73c6-126">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a73c6-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a73c6-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a73c6-127">CommonParameters</span></span>
<span data-ttu-id="a73c6-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a73c6-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a73c6-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a73c6-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a73c6-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a73c6-130">INPUTS</span></span>

### <span data-ttu-id="a73c6-131">System. String</span><span class="sxs-lookup"><span data-stu-id="a73c6-131">System.String</span></span>

## <span data-ttu-id="a73c6-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a73c6-132">OUTPUTS</span></span>

### <span data-ttu-id="a73c6-133">Microsoft. Azure. Commands. Sql. VirtualNetworkRule. Model. AzureSqlServerVirtualNetworkRuleModel</span><span class="sxs-lookup"><span data-stu-id="a73c6-133">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span></span>

## <span data-ttu-id="a73c6-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a73c6-134">NOTES</span></span>

## <span data-ttu-id="a73c6-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a73c6-135">RELATED LINKS</span></span>


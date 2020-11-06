---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerVirtualNetworkRule.md
ms.openlocfilehash: 8c680cf87deedf5fc4bd8671a60db4329a1f68ca
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610984"
---
# <span data-ttu-id="19590-101">Remove-AzureRmSqlServerVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="19590-101">Remove-AzureRmSqlServerVirtualNetworkRule</span></span>

## <span data-ttu-id="19590-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="19590-102">SYNOPSIS</span></span>
<span data-ttu-id="19590-103">Exclui uma regra de rede virtual do Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="19590-103">Deletes an Azure SQL Server Virtual Network Rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="19590-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="19590-104">SYNTAX</span></span>

```
Remove-AzureRmSqlServerVirtualNetworkRule -VirtualNetworkRuleName <String> -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="19590-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="19590-105">DESCRIPTION</span></span>
<span data-ttu-id="19590-106">Esse comando exclui uma regra de rede virtual do SQL Server do Azure.</span><span class="sxs-lookup"><span data-stu-id="19590-106">This command deletes an Azure SQL Server Virtual Network Rule.</span></span>

## <span data-ttu-id="19590-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="19590-107">EXAMPLES</span></span>

### <span data-ttu-id="19590-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="19590-108">Example 1</span></span>
```
PS C:\> $virtualNetworkRule = Remove-AzureRmSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRuleName
```

<span data-ttu-id="19590-109">Exclui uma regra de rede virtual do Azure SQL Server existente</span><span class="sxs-lookup"><span data-stu-id="19590-109">Deletes an existing Azure SQL Server virtual network rule</span></span>

## <span data-ttu-id="19590-110">OS</span><span class="sxs-lookup"><span data-stu-id="19590-110">PARAMETERS</span></span>

### <span data-ttu-id="19590-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19590-111">-ResourceGroupName</span></span>
<span data-ttu-id="19590-112">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="19590-112">The name of the resource group.</span></span>

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

### <span data-ttu-id="19590-113">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="19590-113">-ServerName</span></span>
<span data-ttu-id="19590-114">O nome do SQL Server do Azure.</span><span class="sxs-lookup"><span data-stu-id="19590-114">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="19590-115">-VirtualNetworkRuleName</span><span class="sxs-lookup"><span data-stu-id="19590-115">-VirtualNetworkRuleName</span></span>
<span data-ttu-id="19590-116">Nome da regra de rede virtual do SQL Server do Azure</span><span class="sxs-lookup"><span data-stu-id="19590-116">Azure Sql Server Virtual Network Rule name</span></span>

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

### <span data-ttu-id="19590-117">-Confirme</span><span class="sxs-lookup"><span data-stu-id="19590-117">-Confirm</span></span>
<span data-ttu-id="19590-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="19590-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="19590-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="19590-119">-WhatIf</span></span>
<span data-ttu-id="19590-120">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="19590-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="19590-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="19590-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="19590-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19590-122">-DefaultProfile</span></span>
<span data-ttu-id="19590-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="19590-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="19590-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19590-124">CommonParameters</span></span>
<span data-ttu-id="19590-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19590-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19590-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19590-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19590-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="19590-127">INPUTS</span></span>

### <span data-ttu-id="19590-128">System. String</span><span class="sxs-lookup"><span data-stu-id="19590-128">System.String</span></span>

## <span data-ttu-id="19590-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="19590-129">OUTPUTS</span></span>

### <span data-ttu-id="19590-130">Microsoft. Azure. Commands. Sql. VirtualNetworkRule. Model. AzureSqlServerVirtualNetworkRuleModel</span><span class="sxs-lookup"><span data-stu-id="19590-130">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span></span>

## <span data-ttu-id="19590-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="19590-131">NOTES</span></span>

## <span data-ttu-id="19590-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="19590-132">RELATED LINKS</span></span>


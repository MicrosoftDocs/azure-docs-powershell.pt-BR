---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerVirtualNetworkRule.md
ms.openlocfilehash: e73409edf07402dd44cb5f29a6e878d29d7bfede
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427763"
---
# <span data-ttu-id="fdb58-101">Get-AzureRmSqlServerVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="fdb58-101">Get-AzureRmSqlServerVirtualNetworkRule</span></span>

## <span data-ttu-id="fdb58-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fdb58-102">SYNOPSIS</span></span>
<span data-ttu-id="fdb58-103">Obtém ou lista a regra de rede virtual do Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="fdb58-103">Gets or lists Azure SQL Server Virtual Network Rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fdb58-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fdb58-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerVirtualNetworkRule [-VirtualNetworkRuleName <String>] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fdb58-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fdb58-105">DESCRIPTION</span></span>
<span data-ttu-id="fdb58-106">Esse comando obtém uma regra específica de rede virtual do SQL Server do Azure ou uma lista de regras de rede virtual do Azure SQL Server em um servidor.</span><span class="sxs-lookup"><span data-stu-id="fdb58-106">This command gets a specific Azure SQL Server Virtual Network Rule or a list of Azure SQL Server Virtual Network Rules under a server.</span></span>

## <span data-ttu-id="fdb58-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fdb58-107">EXAMPLES</span></span>

### <span data-ttu-id="fdb58-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="fdb58-108">Example 1</span></span>
```
PS C:\> $virtualNetworkRule = Get-AzureRmSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRuleName
```

<span data-ttu-id="fdb58-109">Obtém uma única regra de rede virtual do Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="fdb58-109">Gets an single Azure SQL Server virtual network rule</span></span>

### <span data-ttu-id="fdb58-110">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="fdb58-110">Example 2</span></span>
```
PS C:\> $virtualNetworkRules = Get-AzureRmSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName
```

<span data-ttu-id="fdb58-111">Obtém a lista de regras de rede virtual do Azure SQL Server no servidor especificado</span><span class="sxs-lookup"><span data-stu-id="fdb58-111">Gets the list of Azure SQL Server virtual network rules under the specified server</span></span>

## <span data-ttu-id="fdb58-112">OS</span><span class="sxs-lookup"><span data-stu-id="fdb58-112">PARAMETERS</span></span>

### <span data-ttu-id="fdb58-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fdb58-113">-ResourceGroupName</span></span>
<span data-ttu-id="fdb58-114">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="fdb58-114">The name of the resource group.</span></span>

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

### <span data-ttu-id="fdb58-115">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="fdb58-115">-ServerName</span></span>
<span data-ttu-id="fdb58-116">O nome do SQL Server do Azure.</span><span class="sxs-lookup"><span data-stu-id="fdb58-116">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="fdb58-117">-VirtualNetworkRuleName</span><span class="sxs-lookup"><span data-stu-id="fdb58-117">-VirtualNetworkRuleName</span></span>
<span data-ttu-id="fdb58-118">O nome da regra de rede virtual do SQL Server do Azure.</span><span class="sxs-lookup"><span data-stu-id="fdb58-118">The Azure Sql Server Virtual Network Rule name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fdb58-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fdb58-119">-DefaultProfile</span></span>
<span data-ttu-id="fdb58-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fdb58-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fdb58-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fdb58-121">CommonParameters</span></span>
<span data-ttu-id="fdb58-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fdb58-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fdb58-123">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fdb58-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fdb58-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fdb58-124">INPUTS</span></span>

### <span data-ttu-id="fdb58-125">System. String</span><span class="sxs-lookup"><span data-stu-id="fdb58-125">System.String</span></span>

## <span data-ttu-id="fdb58-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fdb58-126">OUTPUTS</span></span>

### <span data-ttu-id="fdb58-127">Microsoft. Azure. Commands. Sql. VirtualNetworkRule. Model. AzureSqlServerVirtualNetworkRuleModel</span><span class="sxs-lookup"><span data-stu-id="fdb58-127">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span></span>

## <span data-ttu-id="fdb58-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fdb58-128">NOTES</span></span>

## <span data-ttu-id="fdb58-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fdb58-129">RELATED LINKS</span></span>


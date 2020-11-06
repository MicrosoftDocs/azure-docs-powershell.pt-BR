---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlservervirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerVirtualNetworkRule.md
ms.openlocfilehash: 68fb8bac3a492bec915af6aea7df5d67fc3668dc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427142"
---
# <span data-ttu-id="b7c8b-101">Get-AzureRmSqlServerVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="b7c8b-101">Get-AzureRmSqlServerVirtualNetworkRule</span></span>

## <span data-ttu-id="b7c8b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b7c8b-102">SYNOPSIS</span></span>
<span data-ttu-id="b7c8b-103">Obtém ou lista a regra de rede virtual do Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="b7c8b-103">Gets or lists Azure SQL Server Virtual Network Rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b7c8b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b7c8b-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerVirtualNetworkRule [-VirtualNetworkRuleName <String>] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b7c8b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b7c8b-105">DESCRIPTION</span></span>
<span data-ttu-id="b7c8b-106">Esse comando obtém uma regra específica de rede virtual do SQL Server do Azure ou uma lista de regras de rede virtual do Azure SQL Server em um servidor.</span><span class="sxs-lookup"><span data-stu-id="b7c8b-106">This command gets a specific Azure SQL Server Virtual Network Rule or a list of Azure SQL Server Virtual Network Rules under a server.</span></span>

## <span data-ttu-id="b7c8b-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b7c8b-107">EXAMPLES</span></span>

### <span data-ttu-id="b7c8b-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b7c8b-108">Example 1</span></span>
```
PS C:\> $virtualNetworkRule = Get-AzureRmSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRuleName
```

<span data-ttu-id="b7c8b-109">Obtém uma única regra de rede virtual do Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="b7c8b-109">Gets an single Azure SQL Server virtual network rule</span></span>

### <span data-ttu-id="b7c8b-110">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="b7c8b-110">Example 2</span></span>
```
PS C:\> $virtualNetworkRules = Get-AzureRmSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName
```

<span data-ttu-id="b7c8b-111">Obtém a lista de regras de rede virtual do Azure SQL Server no servidor especificado</span><span class="sxs-lookup"><span data-stu-id="b7c8b-111">Gets the list of Azure SQL Server virtual network rules under the specified server</span></span>

## <span data-ttu-id="b7c8b-112">OS</span><span class="sxs-lookup"><span data-stu-id="b7c8b-112">PARAMETERS</span></span>

### <span data-ttu-id="b7c8b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7c8b-113">-DefaultProfile</span></span>
<span data-ttu-id="b7c8b-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="b7c8b-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b7c8b-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7c8b-115">-ResourceGroupName</span></span>
<span data-ttu-id="b7c8b-116">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b7c8b-116">The name of the resource group.</span></span>

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

### <span data-ttu-id="b7c8b-117">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="b7c8b-117">-ServerName</span></span>
<span data-ttu-id="b7c8b-118">O nome do SQL Server do Azure.</span><span class="sxs-lookup"><span data-stu-id="b7c8b-118">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="b7c8b-119">-VirtualNetworkRuleName</span><span class="sxs-lookup"><span data-stu-id="b7c8b-119">-VirtualNetworkRuleName</span></span>
<span data-ttu-id="b7c8b-120">O nome da regra de rede virtual do SQL Server do Azure.</span><span class="sxs-lookup"><span data-stu-id="b7c8b-120">The Azure Sql Server Virtual Network Rule name.</span></span>

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

### <span data-ttu-id="b7c8b-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7c8b-121">CommonParameters</span></span>
<span data-ttu-id="b7c8b-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7c8b-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7c8b-123">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b7c8b-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7c8b-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b7c8b-124">INPUTS</span></span>

### <span data-ttu-id="b7c8b-125">System. String</span><span class="sxs-lookup"><span data-stu-id="b7c8b-125">System.String</span></span>

## <span data-ttu-id="b7c8b-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b7c8b-126">OUTPUTS</span></span>

### <span data-ttu-id="b7c8b-127">Microsoft. Azure. Commands. Sql. VirtualNetworkRule. Model. AzureSqlServerVirtualNetworkRuleModel</span><span class="sxs-lookup"><span data-stu-id="b7c8b-127">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span></span>

## <span data-ttu-id="b7c8b-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b7c8b-128">NOTES</span></span>

## <span data-ttu-id="b7c8b-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b7c8b-129">RELATED LINKS</span></span>

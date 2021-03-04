---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticsfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsFirewallRule.md
ms.openlocfilehash: e95d29b5a91f8df257649693bdd9d4029ca3d166
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891433"
---
# <span data-ttu-id="e45f2-101">Get-AzDataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="e45f2-101">Get-AzDataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="e45f2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e45f2-102">SYNOPSIS</span></span>
<span data-ttu-id="e45f2-103">Recupera uma regra de firewall ou uma lista de regras de firewall de uma conta do Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="e45f2-103">Retrieves a firewall rule or list of firewall rules from a Data Lake Analytics account.</span></span>

## <span data-ttu-id="e45f2-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="e45f2-104">SYNTAX</span></span>

```
Get-AzDataLakeAnalyticsFirewallRule [-Account] <String> [[-Name] <String>] [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e45f2-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="e45f2-105">DESCRIPTION</span></span>
<span data-ttu-id="e45f2-106">O cmdlet **Get-AzDataLakeAnalyticsFirewallRule** recupera uma regra de firewall ou uma lista de regras de firewall de uma conta do Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="e45f2-106">The **Get-AzDataLakeAnalyticsFirewallRule** cmdlet retrieves a firewall rule or list of firewall rules from an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="e45f2-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e45f2-107">EXAMPLES</span></span>

### <span data-ttu-id="e45f2-108">Exemplo 1: Obter uma regra de firewall</span><span class="sxs-lookup"><span data-stu-id="e45f2-108">Example 1: Get a firewall rule</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsFirewallRule -Account "ContosoAdlAcct" -Name "My firewall rule"
```

<span data-ttu-id="e45f2-109">Este comando obtém a regra de firewall chamada "minha regra de firewall" da conta "ContosoAdlAcct"</span><span class="sxs-lookup"><span data-stu-id="e45f2-109">This command gets the firewall rule named "my firewall rule" from account "ContosoAdlAcct"</span></span>

### <span data-ttu-id="e45f2-110">Exemplo 2: Listar todas as regras de firewall</span><span class="sxs-lookup"><span data-stu-id="e45f2-110">Example 2: List all firewall rules</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsFirewallRule -Account "ContosoAdlAcct"
```

<span data-ttu-id="e45f2-111">Este comando obtém todas as regras de firewall da conta "ContosoAdlAcct"</span><span class="sxs-lookup"><span data-stu-id="e45f2-111">This command gets all firewall rules from account "ContosoAdlAcct"</span></span>

## <span data-ttu-id="e45f2-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="e45f2-112">PARAMETERS</span></span>

### <span data-ttu-id="e45f2-113">-Account</span><span class="sxs-lookup"><span data-stu-id="e45f2-113">-Account</span></span>
<span data-ttu-id="e45f2-114">A conta do Data Lake Analytics para obter a regra de firewall</span><span class="sxs-lookup"><span data-stu-id="e45f2-114">The Data Lake Analytics account to get the firewall rule from</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e45f2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e45f2-115">-DefaultProfile</span></span>
<span data-ttu-id="e45f2-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="e45f2-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e45f2-117">-Name</span><span class="sxs-lookup"><span data-stu-id="e45f2-117">-Name</span></span>
<span data-ttu-id="e45f2-118">O nome da regra de firewall.</span><span class="sxs-lookup"><span data-stu-id="e45f2-118">The name of the firewall rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e45f2-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e45f2-119">-ResourceGroupName</span></span>
<span data-ttu-id="e45f2-120">Nome do grupo de recursos no qual deseja recuperar a conta.</span><span class="sxs-lookup"><span data-stu-id="e45f2-120">Name of resource group under which want to retrieve the account.</span></span>

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

### <span data-ttu-id="e45f2-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e45f2-121">CommonParameters</span></span>
<span data-ttu-id="e45f2-122">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e45f2-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e45f2-123">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e45f2-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e45f2-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e45f2-124">INPUTS</span></span>

### <span data-ttu-id="e45f2-125">System.String</span><span class="sxs-lookup"><span data-stu-id="e45f2-125">System.String</span></span>

## <span data-ttu-id="e45f2-126">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="e45f2-126">OUTPUTS</span></span>

### <span data-ttu-id="e45f2-127">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="e45f2-127">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="e45f2-128">NOTES</span><span class="sxs-lookup"><span data-stu-id="e45f2-128">NOTES</span></span>

## <span data-ttu-id="e45f2-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e45f2-129">RELATED LINKS</span></span>

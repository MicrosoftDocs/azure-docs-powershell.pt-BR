---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticsfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsFirewallRule.md
ms.openlocfilehash: 40c44ff157fca6a276cac8ece508e9d540b526ed
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113262"
---
# <span data-ttu-id="8a55e-101">Get-AzDataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="8a55e-101">Get-AzDataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="8a55e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8a55e-102">SYNOPSIS</span></span>
<span data-ttu-id="8a55e-103">Recupera uma regra de firewall ou lista de regras de firewall de uma conta do Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="8a55e-103">Retrieves a firewall rule or list of firewall rules from a Data Lake Analytics account.</span></span>

## <span data-ttu-id="8a55e-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8a55e-104">SYNTAX</span></span>

```
Get-AzDataLakeAnalyticsFirewallRule [-Account] <String> [[-Name] <String>] [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8a55e-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="8a55e-105">DESCRIPTION</span></span>
<span data-ttu-id="8a55e-106">O cmdlet **Get-AzDataLakeAnalyticsFirewallRule** recupera uma regra de firewall ou lista de regras de firewall de uma conta do Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="8a55e-106">The **Get-AzDataLakeAnalyticsFirewallRule** cmdlet retrieves a firewall rule or list of firewall rules from an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="8a55e-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="8a55e-107">EXAMPLES</span></span>

### <span data-ttu-id="8a55e-108">Exemplo 1: Obter uma regra de firewall</span><span class="sxs-lookup"><span data-stu-id="8a55e-108">Example 1: Get a firewall rule</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsFirewallRule -Account "ContosoAdlAcct" -Name "My firewall rule"
```

<span data-ttu-id="8a55e-109">Este comando obtém a regra de firewall chamada "minha regra de firewall" da conta "ContosoAdlAcct"</span><span class="sxs-lookup"><span data-stu-id="8a55e-109">This command gets the firewall rule named "my firewall rule" from account "ContosoAdlAcct"</span></span>

### <span data-ttu-id="8a55e-110">Exemplo 2: Listar todas as regras de firewall</span><span class="sxs-lookup"><span data-stu-id="8a55e-110">Example 2: List all firewall rules</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsFirewallRule -Account "ContosoAdlAcct"
```

<span data-ttu-id="8a55e-111">Esse comando obtém todas as regras de firewall da conta "ContosoAdlAcct"</span><span class="sxs-lookup"><span data-stu-id="8a55e-111">This command gets all firewall rules from account "ContosoAdlAcct"</span></span>

## <span data-ttu-id="8a55e-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8a55e-112">PARAMETERS</span></span>

### <span data-ttu-id="8a55e-113">-Conta</span><span class="sxs-lookup"><span data-stu-id="8a55e-113">-Account</span></span>
<span data-ttu-id="8a55e-114">A conta do Data Lake Analytics para obter a regra de firewall</span><span class="sxs-lookup"><span data-stu-id="8a55e-114">The Data Lake Analytics account to get the firewall rule from</span></span>

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

### <span data-ttu-id="8a55e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a55e-115">-DefaultProfile</span></span>
<span data-ttu-id="8a55e-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="8a55e-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8a55e-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="8a55e-117">-Name</span></span>
<span data-ttu-id="8a55e-118">O nome da regra de firewall.</span><span class="sxs-lookup"><span data-stu-id="8a55e-118">The name of the firewall rule.</span></span>

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

### <span data-ttu-id="8a55e-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a55e-119">-ResourceGroupName</span></span>
<span data-ttu-id="8a55e-120">Nome do grupo de recursos no qual deseja recuperar a conta.</span><span class="sxs-lookup"><span data-stu-id="8a55e-120">Name of resource group under which want to retrieve the account.</span></span>

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

### <span data-ttu-id="8a55e-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a55e-121">CommonParameters</span></span>
<span data-ttu-id="8a55e-122">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a55e-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a55e-123">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8a55e-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a55e-124">Entradas</span><span class="sxs-lookup"><span data-stu-id="8a55e-124">INPUTS</span></span>

### <span data-ttu-id="8a55e-125">System.String</span><span class="sxs-lookup"><span data-stu-id="8a55e-125">System.String</span></span>

## <span data-ttu-id="8a55e-126">Saídas</span><span class="sxs-lookup"><span data-stu-id="8a55e-126">OUTPUTS</span></span>

### <span data-ttu-id="8a55e-127">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="8a55e-127">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="8a55e-128">Notas</span><span class="sxs-lookup"><span data-stu-id="8a55e-128">NOTES</span></span>

## <span data-ttu-id="8a55e-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8a55e-129">RELATED LINKS</span></span>

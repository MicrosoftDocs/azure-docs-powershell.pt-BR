---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/get-azurermdatalakeanalyticsfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsFirewallRule.md
ms.openlocfilehash: 421bf32bd0a3b5a27728c675396c10414c435d84
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93433274"
---
# <span data-ttu-id="abd41-101">Get-AzureRmDataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="abd41-101">Get-AzureRmDataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="abd41-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="abd41-102">SYNOPSIS</span></span>
<span data-ttu-id="abd41-103">Recupera uma regra de firewall ou uma lista de regras de firewall de uma conta do data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="abd41-103">Retrieves a firewall rule or list of firewall rules from a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="abd41-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="abd41-104">SYNTAX</span></span>

```
Get-AzureRmDataLakeAnalyticsFirewallRule [-Account] <String> [[-Name] <String>] [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="abd41-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="abd41-105">DESCRIPTION</span></span>
<span data-ttu-id="abd41-106">O cmdlet **Get-AzureRmDataLakeAnalyticsFirewallRule** recupera uma regra de firewall ou uma lista de regras de firewall de uma conta do Azure data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="abd41-106">The **Get-AzureRmDataLakeAnalyticsFirewallRule** cmdlet retrieves a firewall rule or list of firewall rules from an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="abd41-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="abd41-107">EXAMPLES</span></span>

### <span data-ttu-id="abd41-108">Exemplo 1: obter uma regra de firewall</span><span class="sxs-lookup"><span data-stu-id="abd41-108">Example 1: Get a firewall rule</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsFirewallRule -Account "ContosoAdlAcct" -Name "My firewall rule"
```

<span data-ttu-id="abd41-109">Este comando obtém a regra de firewall chamada "minha regra de firewall" da conta "ContosoAdlAcct"</span><span class="sxs-lookup"><span data-stu-id="abd41-109">This command gets the firewall rule named "my firewall rule" from account "ContosoAdlAcct"</span></span>

### <span data-ttu-id="abd41-110">Exemplo 2: listar todas as regras de firewall</span><span class="sxs-lookup"><span data-stu-id="abd41-110">Example 2: List all firewall rules</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsFirewallRule -Account "ContosoAdlAcct"
```

<span data-ttu-id="abd41-111">Este comando obtém todas as regras de firewall da conta "ContosoAdlAcct"</span><span class="sxs-lookup"><span data-stu-id="abd41-111">This command gets all firewall rules from account "ContosoAdlAcct"</span></span>

## <span data-ttu-id="abd41-112">OS</span><span class="sxs-lookup"><span data-stu-id="abd41-112">PARAMETERS</span></span>

### <span data-ttu-id="abd41-113">-Conta</span><span class="sxs-lookup"><span data-stu-id="abd41-113">-Account</span></span>
<span data-ttu-id="abd41-114">A conta do data Lake Analytics para a qual obter a regra de firewall</span><span class="sxs-lookup"><span data-stu-id="abd41-114">The Data Lake Analytics account to get the firewall rule from</span></span>

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

### <span data-ttu-id="abd41-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="abd41-115">-DefaultProfile</span></span>
<span data-ttu-id="abd41-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="abd41-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="abd41-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="abd41-117">-Name</span></span>
<span data-ttu-id="abd41-118">O nome da regra de firewall.</span><span class="sxs-lookup"><span data-stu-id="abd41-118">The name of the firewall rule.</span></span>

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

### <span data-ttu-id="abd41-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="abd41-119">-ResourceGroupName</span></span>
<span data-ttu-id="abd41-120">Nome do grupo de recursos sob o qual deseja recuperar a conta.</span><span class="sxs-lookup"><span data-stu-id="abd41-120">Name of resource group under which want to retrieve the account.</span></span>

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

### <span data-ttu-id="abd41-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="abd41-121">CommonParameters</span></span>
<span data-ttu-id="abd41-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="abd41-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="abd41-123">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="abd41-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="abd41-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="abd41-124">INPUTS</span></span>

### <span data-ttu-id="abd41-125">System. String</span><span class="sxs-lookup"><span data-stu-id="abd41-125">System.String</span></span>

## <span data-ttu-id="abd41-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="abd41-126">OUTPUTS</span></span>

### <span data-ttu-id="abd41-127">Microsoft. Azure. Commands. DataLakeAnalytics. Models. DataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="abd41-127">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="abd41-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="abd41-128">NOTES</span></span>

## <span data-ttu-id="abd41-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="abd41-129">RELATED LINKS</span></span>

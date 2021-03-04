---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/powershell/module/az.datalakeanalytics/remove-azdatalakeanalyticsfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsFirewallRule.md
ms.openlocfilehash: 31e4f1be594735d8ea7afbe9abc5f6ccb21ada1a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886056"
---
# <span data-ttu-id="74eb1-101">Remove-AzDataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="74eb1-101">Remove-AzDataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="74eb1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="74eb1-102">SYNOPSIS</span></span>
<span data-ttu-id="74eb1-103">Remove uma regra de firewall de uma conta do Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="74eb1-103">Removes a firewall rule from a Data Lake Analytics account.</span></span>

## <span data-ttu-id="74eb1-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="74eb1-104">SYNTAX</span></span>

```
Remove-AzDataLakeAnalyticsFirewallRule [-Account] <String> [[-Name] <String>] [-PassThru]
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="74eb1-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="74eb1-105">DESCRIPTION</span></span>
<span data-ttu-id="74eb1-106">O cmdlet **Remove-AzDataLakeAnalyticsFirewallRule** remove uma regra de firewall de uma conta do Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="74eb1-106">The **Remove-AzDataLakeAnalyticsFirewallRule** cmdlet removes a firewall rule from an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="74eb1-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="74eb1-107">EXAMPLES</span></span>

### <span data-ttu-id="74eb1-108">Exemplo 1: Remover uma regra de firewall</span><span class="sxs-lookup"><span data-stu-id="74eb1-108">Example 1: Remove a firewall rule</span></span>
```
PS C:\>Remove-AzDataLakeAnalyticsFirewallRule -Account "ContosoAdlAcct" -Name "My firewall rule"
```

<span data-ttu-id="74eb1-109">Este comando remove a regra de firewall chamada "minha regra de firewall" da conta "ContosoAdlAcct"</span><span class="sxs-lookup"><span data-stu-id="74eb1-109">This command removes the firewall rule named "my firewall rule" from account "ContosoAdlAcct"</span></span>

## <span data-ttu-id="74eb1-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="74eb1-110">PARAMETERS</span></span>

### <span data-ttu-id="74eb1-111">-Account</span><span class="sxs-lookup"><span data-stu-id="74eb1-111">-Account</span></span>
<span data-ttu-id="74eb1-112">A conta do Data Lake Analytics para remover a regra de firewall</span><span class="sxs-lookup"><span data-stu-id="74eb1-112">The Data Lake Analytics account to remove the firewall rule from</span></span>

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

### <span data-ttu-id="74eb1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74eb1-113">-DefaultProfile</span></span>
<span data-ttu-id="74eb1-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="74eb1-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="74eb1-115">-Name</span><span class="sxs-lookup"><span data-stu-id="74eb1-115">-Name</span></span>
<span data-ttu-id="74eb1-116">O nome da regra de firewall.</span><span class="sxs-lookup"><span data-stu-id="74eb1-116">The name of the firewall rule.</span></span>

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

### <span data-ttu-id="74eb1-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="74eb1-117">-PassThru</span></span>
<span data-ttu-id="74eb1-118">Indica que uma resposta booleana deve ser retornada indicando o resultado da operação de exclusão.</span><span class="sxs-lookup"><span data-stu-id="74eb1-118">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74eb1-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74eb1-119">-ResourceGroupName</span></span>
<span data-ttu-id="74eb1-120">Nome do grupo de recursos no qual deseja recuperar a conta.</span><span class="sxs-lookup"><span data-stu-id="74eb1-120">Name of resource group under which want to retrieve the account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74eb1-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="74eb1-121">-Confirm</span></span>
<span data-ttu-id="74eb1-122">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="74eb1-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="74eb1-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="74eb1-123">-WhatIf</span></span>
<span data-ttu-id="74eb1-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="74eb1-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="74eb1-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="74eb1-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="74eb1-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74eb1-126">CommonParameters</span></span>
<span data-ttu-id="74eb1-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74eb1-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74eb1-128">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="74eb1-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74eb1-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="74eb1-129">INPUTS</span></span>

### <span data-ttu-id="74eb1-130">System.String</span><span class="sxs-lookup"><span data-stu-id="74eb1-130">System.String</span></span>

### <span data-ttu-id="74eb1-131">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="74eb1-131">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="74eb1-132">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="74eb1-132">OUTPUTS</span></span>

### <span data-ttu-id="74eb1-133">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="74eb1-133">System.Boolean</span></span>

## <span data-ttu-id="74eb1-134">NOTES</span><span class="sxs-lookup"><span data-stu-id="74eb1-134">NOTES</span></span>

## <span data-ttu-id="74eb1-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="74eb1-135">RELATED LINKS</span></span>

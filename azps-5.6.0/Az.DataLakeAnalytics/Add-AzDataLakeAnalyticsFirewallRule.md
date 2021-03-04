---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/powershell/module/az.datalakeanalytics/add-azdatalakeanalyticsfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Add-AzDataLakeAnalyticsFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Add-AzDataLakeAnalyticsFirewallRule.md
ms.openlocfilehash: ed5d4514603ccefeefa4e99d9458434ffeb17cba
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886985"
---
# <span data-ttu-id="9429f-101">Add-AzDataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="9429f-101">Add-AzDataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="9429f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9429f-102">SYNOPSIS</span></span>
<span data-ttu-id="9429f-103">Adiciona uma regra de firewall a uma conta do Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="9429f-103">Adds a firewall rule to a Data Lake Analytics account.</span></span>

## <span data-ttu-id="9429f-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="9429f-104">SYNTAX</span></span>

```
Add-AzDataLakeAnalyticsFirewallRule [-Account] <String> [-Name] <String> [-StartIpAddress] <String>
 [-EndIpAddress] <String> [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9429f-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="9429f-105">DESCRIPTION</span></span>
<span data-ttu-id="9429f-106">O cmdlet **Add-AzDataLakeAnalyticsFirewallRule** adiciona uma regra de firewall a uma conta do Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="9429f-106">The **Add-AzDataLakeAnalyticsFirewallRule** cmdlet adds a firewall rule to an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="9429f-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9429f-107">EXAMPLES</span></span>

### <span data-ttu-id="9429f-108">Exemplo 1: Adicionar uma regra de firewall</span><span class="sxs-lookup"><span data-stu-id="9429f-108">Example 1: Add a firewall rule</span></span>
```
PS C:\>Add-AzDataLakeAnalyticsFirewallRule -Account "ContosoAdlAcct" -Name "My firewall rule" -StartIpAddress 127.0.0.1 -EndIpAddress 127.0.0.10
```

<span data-ttu-id="9429f-109">Este comando adiciona a regra de firewall chamada "minha regra de firewall" da conta "ContosoAdlAcct" com o intervalo de IP: 127.0.0.1 - 127.0.10</span><span class="sxs-lookup"><span data-stu-id="9429f-109">This command adds the firewall rule named "my firewall rule" from account "ContosoAdlAcct" with the IP range: 127.0.0.1 - 127.0.0.10</span></span>

## <span data-ttu-id="9429f-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="9429f-110">PARAMETERS</span></span>

### <span data-ttu-id="9429f-111">-Account</span><span class="sxs-lookup"><span data-stu-id="9429f-111">-Account</span></span>
<span data-ttu-id="9429f-112">A conta do Data Lake Analytics para adicionar a regra de firewall</span><span class="sxs-lookup"><span data-stu-id="9429f-112">The Data Lake Analytics account to add the firewall rule to</span></span>

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

### <span data-ttu-id="9429f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9429f-113">-DefaultProfile</span></span>
<span data-ttu-id="9429f-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="9429f-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9429f-115">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="9429f-115">-EndIpAddress</span></span>
<span data-ttu-id="9429f-116">O final do intervalo ip válido para a regra de firewall</span><span class="sxs-lookup"><span data-stu-id="9429f-116">The end of the valid ip range for the firewall rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9429f-117">-Name</span><span class="sxs-lookup"><span data-stu-id="9429f-117">-Name</span></span>
<span data-ttu-id="9429f-118">O nome da regra de firewall.</span><span class="sxs-lookup"><span data-stu-id="9429f-118">The name of the firewall rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9429f-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9429f-119">-ResourceGroupName</span></span>
<span data-ttu-id="9429f-120">Nome do grupo de recursos no qual deseja recuperar a conta.</span><span class="sxs-lookup"><span data-stu-id="9429f-120">Name of resource group under which want to retrieve the account.</span></span>

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

### <span data-ttu-id="9429f-121">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="9429f-121">-StartIpAddress</span></span>
<span data-ttu-id="9429f-122">O início do intervalo ip válido para a regra de firewall</span><span class="sxs-lookup"><span data-stu-id="9429f-122">The start of the valid ip range for the firewall rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9429f-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9429f-123">-Confirm</span></span>
<span data-ttu-id="9429f-124">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9429f-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9429f-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9429f-125">-WhatIf</span></span>
<span data-ttu-id="9429f-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9429f-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9429f-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9429f-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9429f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9429f-128">CommonParameters</span></span>
<span data-ttu-id="9429f-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9429f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9429f-130">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9429f-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9429f-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9429f-131">INPUTS</span></span>

### <span data-ttu-id="9429f-132">System.String</span><span class="sxs-lookup"><span data-stu-id="9429f-132">System.String</span></span>

## <span data-ttu-id="9429f-133">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="9429f-133">OUTPUTS</span></span>

### <span data-ttu-id="9429f-134">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="9429f-134">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="9429f-135">NOTES</span><span class="sxs-lookup"><span data-stu-id="9429f-135">NOTES</span></span>

## <span data-ttu-id="9429f-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9429f-136">RELATED LINKS</span></span>

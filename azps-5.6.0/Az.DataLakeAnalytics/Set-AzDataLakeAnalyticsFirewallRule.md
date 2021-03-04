---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/powershell/module/az.datalakeanalytics/set-azdatalakeanalyticsfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Set-AzDataLakeAnalyticsFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Set-AzDataLakeAnalyticsFirewallRule.md
ms.openlocfilehash: 9fbb2064a7b7869af450ad267f73c6dc2e2b9a9a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892981"
---
# <span data-ttu-id="da18a-101">Set-AzDataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="da18a-101">Set-AzDataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="da18a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="da18a-102">SYNOPSIS</span></span>
<span data-ttu-id="da18a-103">Atualiza uma regra de firewall em uma conta do Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="da18a-103">Updates a firewall rule in a Data Lake Analytics account.</span></span>

## <span data-ttu-id="da18a-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="da18a-104">SYNTAX</span></span>

```
Set-AzDataLakeAnalyticsFirewallRule [-Account] <String> [-Name] <String> [[-StartIpAddress] <String>]
 [[-EndIpAddress] <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="da18a-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="da18a-105">DESCRIPTION</span></span>
<span data-ttu-id="da18a-106">O cmdlet **Set-AzDataLakeAnalyticsFirewallRule** atualiza uma regra de firewall em uma conta do Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="da18a-106">The **Set-AzDataLakeAnalyticsFirewallRule** cmdlet updates a firewall rule in an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="da18a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="da18a-107">EXAMPLES</span></span>

### <span data-ttu-id="da18a-108">Exemplo 1: atualizar uma regra de firewall</span><span class="sxs-lookup"><span data-stu-id="da18a-108">Example 1: Update a firewall rule</span></span>
```
PS C:\>Set-AzDataLakeAnalyticsFirewallRule -Account "ContosoAdlAcct" -Name "My firewall rule" -StartIpAddress 127.0.0.1 -EndIpAddress 127.0.0.10
```

<span data-ttu-id="da18a-109">Este comando atualiza a regra de firewall chamada "minha regra de firewall" na conta "ContosoAdlAcct" para ter o novo intervalo de IP: 127.0.0.1 - 127.0.0.10</span><span class="sxs-lookup"><span data-stu-id="da18a-109">This command updates the firewall rule named "my firewall rule" in account "ContosoAdlAcct" to have the new IP range: 127.0.0.1 - 127.0.0.10</span></span>

## <span data-ttu-id="da18a-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="da18a-110">PARAMETERS</span></span>

### <span data-ttu-id="da18a-111">-Account</span><span class="sxs-lookup"><span data-stu-id="da18a-111">-Account</span></span>
<span data-ttu-id="da18a-112">A conta do Data Lake Analytics para atualizar a regra de firewall em</span><span class="sxs-lookup"><span data-stu-id="da18a-112">The Data Lake Analytics account to update the firewall rule in</span></span>

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

### <span data-ttu-id="da18a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da18a-113">-DefaultProfile</span></span>
<span data-ttu-id="da18a-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="da18a-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="da18a-115">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="da18a-115">-EndIpAddress</span></span>
<span data-ttu-id="da18a-116">O final do intervalo ip válido para a regra de firewall</span><span class="sxs-lookup"><span data-stu-id="da18a-116">The end of the valid ip range for the firewall rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da18a-117">-Name</span><span class="sxs-lookup"><span data-stu-id="da18a-117">-Name</span></span>
<span data-ttu-id="da18a-118">O nome da regra de firewall.</span><span class="sxs-lookup"><span data-stu-id="da18a-118">The name of the firewall rule.</span></span>

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

### <span data-ttu-id="da18a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da18a-119">-ResourceGroupName</span></span>
<span data-ttu-id="da18a-120">Nome do grupo de recursos no qual deseja recuperar a conta.</span><span class="sxs-lookup"><span data-stu-id="da18a-120">Name of resource group under which want to retrieve the account.</span></span>

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

### <span data-ttu-id="da18a-121">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="da18a-121">-StartIpAddress</span></span>
<span data-ttu-id="da18a-122">O início do intervalo ip válido para a regra de firewall</span><span class="sxs-lookup"><span data-stu-id="da18a-122">The start of the valid ip range for the firewall rule</span></span>

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

### <span data-ttu-id="da18a-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="da18a-123">-Confirm</span></span>
<span data-ttu-id="da18a-124">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="da18a-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="da18a-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da18a-125">-WhatIf</span></span>
<span data-ttu-id="da18a-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="da18a-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="da18a-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="da18a-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="da18a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da18a-128">CommonParameters</span></span>
<span data-ttu-id="da18a-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da18a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da18a-130">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da18a-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da18a-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="da18a-131">INPUTS</span></span>

### <span data-ttu-id="da18a-132">System.String</span><span class="sxs-lookup"><span data-stu-id="da18a-132">System.String</span></span>

## <span data-ttu-id="da18a-133">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="da18a-133">OUTPUTS</span></span>

### <span data-ttu-id="da18a-134">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="da18a-134">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="da18a-135">NOTES</span><span class="sxs-lookup"><span data-stu-id="da18a-135">NOTES</span></span>

## <span data-ttu-id="da18a-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="da18a-136">RELATED LINKS</span></span>

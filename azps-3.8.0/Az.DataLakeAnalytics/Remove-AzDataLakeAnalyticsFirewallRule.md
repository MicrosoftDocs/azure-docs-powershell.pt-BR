---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/remove-azdatalakeanalyticsfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsFirewallRule.md
ms.openlocfilehash: 879897b6d89e5a1e34ee9f61714628aa741a670f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93940541"
---
# <span data-ttu-id="75709-101">Remove-AzDataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="75709-101">Remove-AzDataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="75709-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="75709-102">SYNOPSIS</span></span>
<span data-ttu-id="75709-103">Remove uma regra de firewall de uma conta do data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="75709-103">Removes a firewall rule from a Data Lake Analytics account.</span></span>

## <span data-ttu-id="75709-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="75709-104">SYNTAX</span></span>

```
Remove-AzDataLakeAnalyticsFirewallRule [-Account] <String> [[-Name] <String>] [-PassThru]
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="75709-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="75709-105">DESCRIPTION</span></span>
<span data-ttu-id="75709-106">O cmdlet **Remove-AzDataLakeAnalyticsFirewallRule** remove uma regra de firewall de uma conta do Azure data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="75709-106">The **Remove-AzDataLakeAnalyticsFirewallRule** cmdlet removes a firewall rule from an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="75709-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="75709-107">EXAMPLES</span></span>

### <span data-ttu-id="75709-108">Exemplo 1: remover uma regra de firewall</span><span class="sxs-lookup"><span data-stu-id="75709-108">Example 1: Remove a firewall rule</span></span>
```
PS C:\>Remove-AzDataLakeAnalyticsFirewallRule -Account "ContosoAdlAcct" -Name "My firewall rule"
```

<span data-ttu-id="75709-109">Esse comando Remove a regra de firewall chamada "minha regra de firewall" da conta "ContosoAdlAcct"</span><span class="sxs-lookup"><span data-stu-id="75709-109">This command removes the firewall rule named "my firewall rule" from account "ContosoAdlAcct"</span></span>

## <span data-ttu-id="75709-110">OS</span><span class="sxs-lookup"><span data-stu-id="75709-110">PARAMETERS</span></span>

### <span data-ttu-id="75709-111">-Conta</span><span class="sxs-lookup"><span data-stu-id="75709-111">-Account</span></span>
<span data-ttu-id="75709-112">A conta do data Lake Analytics para a qual remover a regra de firewall</span><span class="sxs-lookup"><span data-stu-id="75709-112">The Data Lake Analytics account to remove the firewall rule from</span></span>

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

### <span data-ttu-id="75709-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75709-113">-DefaultProfile</span></span>
<span data-ttu-id="75709-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="75709-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="75709-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="75709-115">-Name</span></span>
<span data-ttu-id="75709-116">O nome da regra de firewall.</span><span class="sxs-lookup"><span data-stu-id="75709-116">The name of the firewall rule.</span></span>

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

### <span data-ttu-id="75709-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="75709-117">-PassThru</span></span>
<span data-ttu-id="75709-118">Indica que uma resposta booliana deve ser retornada indicando o resultado da operação de exclusão.</span><span class="sxs-lookup"><span data-stu-id="75709-118">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

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

### <span data-ttu-id="75709-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75709-119">-ResourceGroupName</span></span>
<span data-ttu-id="75709-120">Nome do grupo de recursos sob o qual deseja recuperar a conta.</span><span class="sxs-lookup"><span data-stu-id="75709-120">Name of resource group under which want to retrieve the account.</span></span>

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

### <span data-ttu-id="75709-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="75709-121">-Confirm</span></span>
<span data-ttu-id="75709-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="75709-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="75709-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75709-123">-WhatIf</span></span>
<span data-ttu-id="75709-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="75709-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="75709-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="75709-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="75709-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75709-126">CommonParameters</span></span>
<span data-ttu-id="75709-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75709-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75709-128">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75709-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75709-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="75709-129">INPUTS</span></span>

### <span data-ttu-id="75709-130">System. String</span><span class="sxs-lookup"><span data-stu-id="75709-130">System.String</span></span>

### <span data-ttu-id="75709-131">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="75709-131">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="75709-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="75709-132">OUTPUTS</span></span>

### <span data-ttu-id="75709-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="75709-133">System.Boolean</span></span>

## <span data-ttu-id="75709-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="75709-134">NOTES</span></span>

## <span data-ttu-id="75709-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="75709-135">RELATED LINKS</span></span>

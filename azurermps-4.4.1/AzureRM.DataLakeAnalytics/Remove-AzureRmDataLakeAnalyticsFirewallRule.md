---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsFirewallRule.md
ms.openlocfilehash: cca9a398ad216de1bb28aac128fd9642b79d2dd2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427951"
---
# <span data-ttu-id="d07c7-101">Remove-AzureRmDataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="d07c7-101">Remove-AzureRmDataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="d07c7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d07c7-102">SYNOPSIS</span></span>
<span data-ttu-id="d07c7-103">Remove uma regra de firewall de uma conta do data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="d07c7-103">Removes a firewall rule from a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d07c7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d07c7-104">SYNTAX</span></span>

```
Remove-AzureRmDataLakeAnalyticsFirewallRule [-Account] <String> [[-Name] <String>] [-PassThru]
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d07c7-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d07c7-105">DESCRIPTION</span></span>
<span data-ttu-id="d07c7-106">O cmdlet **Remove-AzureRmDataLakeAnalyticsFirewallRule** remove uma regra de firewall de uma conta do Azure data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="d07c7-106">The **Remove-AzureRmDataLakeAnalyticsFirewallRule** cmdlet removes a firewall rule from an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="d07c7-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d07c7-107">EXAMPLES</span></span>

### <span data-ttu-id="d07c7-108">Exemplo 1: remover uma regra de firewall</span><span class="sxs-lookup"><span data-stu-id="d07c7-108">Example 1: Remove a firewall rule</span></span>
```
PS C:\>Remove-AzureRmDataLakeAnalyticsFirewallRule -Account "ContosoAdlAcct" -Name "My firewall rule"
```

<span data-ttu-id="d07c7-109">Esse comando Remove a regra de firewall chamada "minha regra de firewall" da conta "ContosoAdlAcct"</span><span class="sxs-lookup"><span data-stu-id="d07c7-109">This command removes the firewall rule named "my firewall rule" from account "ContosoAdlAcct"</span></span>

## <span data-ttu-id="d07c7-110">OS</span><span class="sxs-lookup"><span data-stu-id="d07c7-110">PARAMETERS</span></span>

### <span data-ttu-id="d07c7-111">-Conta</span><span class="sxs-lookup"><span data-stu-id="d07c7-111">-Account</span></span>
<span data-ttu-id="d07c7-112">A conta do data Lake Analytics para a qual remover a regra de firewall</span><span class="sxs-lookup"><span data-stu-id="d07c7-112">The Data Lake Analytics account to remove the firewall rule from</span></span>

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

### <span data-ttu-id="d07c7-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="d07c7-113">-Name</span></span>
<span data-ttu-id="d07c7-114">O nome da regra de firewall.</span><span class="sxs-lookup"><span data-stu-id="d07c7-114">The name of the firewall rule.</span></span>

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

### <span data-ttu-id="d07c7-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d07c7-115">-PassThru</span></span>
<span data-ttu-id="d07c7-116">Indica que uma resposta booliana deve ser retornada indicando o resultado da operação de exclusão.</span><span class="sxs-lookup"><span data-stu-id="d07c7-116">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

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

### <span data-ttu-id="d07c7-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d07c7-117">-ResourceGroupName</span></span>
<span data-ttu-id="d07c7-118">Nome do grupo de recursos sob o qual deseja recuperar a conta.</span><span class="sxs-lookup"><span data-stu-id="d07c7-118">Name of resource group under which want to retrieve the account.</span></span>

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

### <span data-ttu-id="d07c7-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d07c7-119">-Confirm</span></span>
<span data-ttu-id="d07c7-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d07c7-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d07c7-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d07c7-121">-WhatIf</span></span>
<span data-ttu-id="d07c7-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d07c7-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d07c7-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d07c7-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d07c7-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d07c7-124">-DefaultProfile</span></span>
<span data-ttu-id="d07c7-125">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d07c7-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d07c7-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d07c7-126">CommonParameters</span></span>
<span data-ttu-id="d07c7-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d07c7-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d07c7-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d07c7-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d07c7-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d07c7-129">INPUTS</span></span>

### <span data-ttu-id="d07c7-130">System. String</span><span class="sxs-lookup"><span data-stu-id="d07c7-130">System.String</span></span>
<span data-ttu-id="d07c7-131">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="d07c7-131">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="d07c7-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d07c7-132">OUTPUTS</span></span>

### <span data-ttu-id="d07c7-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d07c7-133">System.Boolean</span></span>

## <span data-ttu-id="d07c7-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d07c7-134">NOTES</span></span>

## <span data-ttu-id="d07c7-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d07c7-135">RELATED LINKS</span></span>


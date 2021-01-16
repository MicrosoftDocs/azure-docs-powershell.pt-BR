---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/set-azdatalakeanalyticsfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Set-AzDataLakeAnalyticsFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Set-AzDataLakeAnalyticsFirewallRule.md
ms.openlocfilehash: 91941fbef7363a56da8a8021294750cc862aab55
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98433782"
---
# <span data-ttu-id="99ef3-101">Set-AzDataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="99ef3-101">Set-AzDataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="99ef3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="99ef3-102">SYNOPSIS</span></span>
<span data-ttu-id="99ef3-103">Atualiza uma regra de firewall em uma conta do data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="99ef3-103">Updates a firewall rule in a Data Lake Analytics account.</span></span>

## <span data-ttu-id="99ef3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="99ef3-104">SYNTAX</span></span>

```
Set-AzDataLakeAnalyticsFirewallRule [-Account] <String> [-Name] <String> [[-StartIpAddress] <String>]
 [[-EndIpAddress] <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="99ef3-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="99ef3-105">DESCRIPTION</span></span>
<span data-ttu-id="99ef3-106">O cmdlet **set-AzDataLakeAnalyticsFirewallRule** atualiza uma regra de firewall em uma conta do Azure data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="99ef3-106">The **Set-AzDataLakeAnalyticsFirewallRule** cmdlet updates a firewall rule in an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="99ef3-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="99ef3-107">EXAMPLES</span></span>

### <span data-ttu-id="99ef3-108">Exemplo 1: atualizar uma regra de firewall</span><span class="sxs-lookup"><span data-stu-id="99ef3-108">Example 1: Update a firewall rule</span></span>
```
PS C:\>Set-AzDataLakeAnalyticsFirewallRule -Account "ContosoAdlAcct" -Name "My firewall rule" -StartIpAddress 127.0.0.1 -EndIpAddress 127.0.0.10
```

<span data-ttu-id="99ef3-109">Esse comando atualiza a regra de firewall chamada "minha regra de firewall" na conta "ContosoAdlAcct" para ter o novo intervalo de IP: 127.0.0.1-127.0.0.10</span><span class="sxs-lookup"><span data-stu-id="99ef3-109">This command updates the firewall rule named "my firewall rule" in account "ContosoAdlAcct" to have the new IP range: 127.0.0.1 - 127.0.0.10</span></span>

## <span data-ttu-id="99ef3-110">OS</span><span class="sxs-lookup"><span data-stu-id="99ef3-110">PARAMETERS</span></span>

### <span data-ttu-id="99ef3-111">-Conta</span><span class="sxs-lookup"><span data-stu-id="99ef3-111">-Account</span></span>
<span data-ttu-id="99ef3-112">A conta do data Lake Analytics para atualizar a regra de firewall em</span><span class="sxs-lookup"><span data-stu-id="99ef3-112">The Data Lake Analytics account to update the firewall rule in</span></span>

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

### <span data-ttu-id="99ef3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99ef3-113">-DefaultProfile</span></span>
<span data-ttu-id="99ef3-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="99ef3-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="99ef3-115">-Endipaddress</span><span class="sxs-lookup"><span data-stu-id="99ef3-115">-EndIpAddress</span></span>
<span data-ttu-id="99ef3-116">O final do intervalo de IP válido para a regra de firewall</span><span class="sxs-lookup"><span data-stu-id="99ef3-116">The end of the valid ip range for the firewall rule</span></span>

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

### <span data-ttu-id="99ef3-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="99ef3-117">-Name</span></span>
<span data-ttu-id="99ef3-118">O nome da regra de firewall.</span><span class="sxs-lookup"><span data-stu-id="99ef3-118">The name of the firewall rule.</span></span>

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

### <span data-ttu-id="99ef3-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99ef3-119">-ResourceGroupName</span></span>
<span data-ttu-id="99ef3-120">Nome do grupo de recursos sob o qual deseja recuperar a conta.</span><span class="sxs-lookup"><span data-stu-id="99ef3-120">Name of resource group under which want to retrieve the account.</span></span>

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

### <span data-ttu-id="99ef3-121">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="99ef3-121">-StartIpAddress</span></span>
<span data-ttu-id="99ef3-122">O início do intervalo de IP válido para a regra de firewall</span><span class="sxs-lookup"><span data-stu-id="99ef3-122">The start of the valid ip range for the firewall rule</span></span>

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

### <span data-ttu-id="99ef3-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="99ef3-123">-Confirm</span></span>
<span data-ttu-id="99ef3-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="99ef3-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="99ef3-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="99ef3-125">-WhatIf</span></span>
<span data-ttu-id="99ef3-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="99ef3-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="99ef3-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="99ef3-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="99ef3-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99ef3-128">CommonParameters</span></span>
<span data-ttu-id="99ef3-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99ef3-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99ef3-130">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="99ef3-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99ef3-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="99ef3-131">INPUTS</span></span>

### <span data-ttu-id="99ef3-132">System. String</span><span class="sxs-lookup"><span data-stu-id="99ef3-132">System.String</span></span>

## <span data-ttu-id="99ef3-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="99ef3-133">OUTPUTS</span></span>

### <span data-ttu-id="99ef3-134">Microsoft. Azure. Commands. DataLakeAnalytics. Models. DataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="99ef3-134">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="99ef3-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="99ef3-135">NOTES</span></span>

## <span data-ttu-id="99ef3-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="99ef3-136">RELATED LINKS</span></span>

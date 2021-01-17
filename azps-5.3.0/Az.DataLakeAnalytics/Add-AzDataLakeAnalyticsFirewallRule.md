---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/add-azdatalakeanalyticsfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Add-AzDataLakeAnalyticsFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Add-AzDataLakeAnalyticsFirewallRule.md
ms.openlocfilehash: d9e6dd2e3fedff0d97919e04ca4f8b61536e2075
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98429844"
---
# <span data-ttu-id="da3f4-101">Add-AzDataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="da3f4-101">Add-AzDataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="da3f4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="da3f4-102">SYNOPSIS</span></span>
<span data-ttu-id="da3f4-103">Adiciona uma regra de firewall a uma conta do data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="da3f4-103">Adds a firewall rule to a Data Lake Analytics account.</span></span>

## <span data-ttu-id="da3f4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="da3f4-104">SYNTAX</span></span>

```
Add-AzDataLakeAnalyticsFirewallRule [-Account] <String> [-Name] <String> [-StartIpAddress] <String>
 [-EndIpAddress] <String> [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="da3f4-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="da3f4-105">DESCRIPTION</span></span>
<span data-ttu-id="da3f4-106">O cmdlet **Add-AzDataLakeAnalyticsFirewallRule** adiciona uma regra de firewall a uma conta do Azure data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="da3f4-106">The **Add-AzDataLakeAnalyticsFirewallRule** cmdlet adds a firewall rule to an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="da3f4-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="da3f4-107">EXAMPLES</span></span>

### <span data-ttu-id="da3f4-108">Exemplo 1: adicionar uma regra de firewall</span><span class="sxs-lookup"><span data-stu-id="da3f4-108">Example 1: Add a firewall rule</span></span>
```
PS C:\>Add-AzDataLakeAnalyticsFirewallRule -Account "ContosoAdlAcct" -Name "My firewall rule" -StartIpAddress 127.0.0.1 -EndIpAddress 127.0.0.10
```

<span data-ttu-id="da3f4-109">Esse comando adiciona a regra de firewall chamada "minha regra de firewall" da conta "ContosoAdlAcct" com o intervalo IP: 127.0.0.1-127.0.0.10</span><span class="sxs-lookup"><span data-stu-id="da3f4-109">This command adds the firewall rule named "my firewall rule" from account "ContosoAdlAcct" with the IP range: 127.0.0.1 - 127.0.0.10</span></span>

## <span data-ttu-id="da3f4-110">OS</span><span class="sxs-lookup"><span data-stu-id="da3f4-110">PARAMETERS</span></span>

### <span data-ttu-id="da3f4-111">-Conta</span><span class="sxs-lookup"><span data-stu-id="da3f4-111">-Account</span></span>
<span data-ttu-id="da3f4-112">A conta do data Lake Analytics à qual adicionar a regra de firewall</span><span class="sxs-lookup"><span data-stu-id="da3f4-112">The Data Lake Analytics account to add the firewall rule to</span></span>

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

### <span data-ttu-id="da3f4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da3f4-113">-DefaultProfile</span></span>
<span data-ttu-id="da3f4-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="da3f4-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="da3f4-115">-Endipaddress</span><span class="sxs-lookup"><span data-stu-id="da3f4-115">-EndIpAddress</span></span>
<span data-ttu-id="da3f4-116">O final do intervalo de IP válido para a regra de firewall</span><span class="sxs-lookup"><span data-stu-id="da3f4-116">The end of the valid ip range for the firewall rule</span></span>

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

### <span data-ttu-id="da3f4-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="da3f4-117">-Name</span></span>
<span data-ttu-id="da3f4-118">O nome da regra de firewall.</span><span class="sxs-lookup"><span data-stu-id="da3f4-118">The name of the firewall rule.</span></span>

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

### <span data-ttu-id="da3f4-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da3f4-119">-ResourceGroupName</span></span>
<span data-ttu-id="da3f4-120">Nome do grupo de recursos sob o qual deseja recuperar a conta.</span><span class="sxs-lookup"><span data-stu-id="da3f4-120">Name of resource group under which want to retrieve the account.</span></span>

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

### <span data-ttu-id="da3f4-121">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="da3f4-121">-StartIpAddress</span></span>
<span data-ttu-id="da3f4-122">O início do intervalo de IP válido para a regra de firewall</span><span class="sxs-lookup"><span data-stu-id="da3f4-122">The start of the valid ip range for the firewall rule</span></span>

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

### <span data-ttu-id="da3f4-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="da3f4-123">-Confirm</span></span>
<span data-ttu-id="da3f4-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="da3f4-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="da3f4-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da3f4-125">-WhatIf</span></span>
<span data-ttu-id="da3f4-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="da3f4-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="da3f4-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="da3f4-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="da3f4-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da3f4-128">CommonParameters</span></span>
<span data-ttu-id="da3f4-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da3f4-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da3f4-130">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da3f4-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da3f4-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="da3f4-131">INPUTS</span></span>

### <span data-ttu-id="da3f4-132">System. String</span><span class="sxs-lookup"><span data-stu-id="da3f4-132">System.String</span></span>

## <span data-ttu-id="da3f4-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="da3f4-133">OUTPUTS</span></span>

### <span data-ttu-id="da3f4-134">Microsoft. Azure. Commands. DataLakeAnalytics. Models. DataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="da3f4-134">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="da3f4-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="da3f4-135">NOTES</span></span>

## <span data-ttu-id="da3f4-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="da3f4-136">RELATED LINKS</span></span>

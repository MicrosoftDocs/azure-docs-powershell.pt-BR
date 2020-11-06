---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/add-azurermdatalakeanalyticsfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Add-AzureRmDataLakeAnalyticsFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Add-AzureRmDataLakeAnalyticsFirewallRule.md
ms.openlocfilehash: bed4ec4fd3afdf0218f68d9e2e4c61c739db48ca
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431691"
---
# <span data-ttu-id="6d391-101">Add-AzureRmDataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="6d391-101">Add-AzureRmDataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="6d391-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6d391-102">SYNOPSIS</span></span>
<span data-ttu-id="6d391-103">Adiciona uma regra de firewall a uma conta do data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="6d391-103">Adds a firewall rule to a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6d391-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6d391-104">SYNTAX</span></span>

```
Add-AzureRmDataLakeAnalyticsFirewallRule [-Account] <String> [-Name] <String> [-StartIpAddress] <String>
 [-EndIpAddress] <String> [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6d391-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6d391-105">DESCRIPTION</span></span>
<span data-ttu-id="6d391-106">O cmdlet **Add-AzureRmDataLakeAnalyticsFirewallRule** adiciona uma regra de firewall a uma conta do Azure data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="6d391-106">The **Add-AzureRmDataLakeAnalyticsFirewallRule** cmdlet adds a firewall rule to an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="6d391-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6d391-107">EXAMPLES</span></span>

### <span data-ttu-id="6d391-108">Exemplo 1: adicionar uma regra de firewall</span><span class="sxs-lookup"><span data-stu-id="6d391-108">Example 1: Add a firewall rule</span></span>
```
PS C:\>Add-AzureRmDataLakeAnalyticsFirewallRule -Account "ContosoAdlAcct" -Name "My firewall rule" -StartIpAddress 127.0.0.1 -EndIpAddress 127.0.0.10
```

<span data-ttu-id="6d391-109">Esse comando adiciona a regra de firewall chamada "minha regra de firewall" da conta "ContosoAdlAcct" com o intervalo IP: 127.0.0.1-127.0.0.10</span><span class="sxs-lookup"><span data-stu-id="6d391-109">This command adds the firewall rule named "my firewall rule" from account "ContosoAdlAcct" with the IP range: 127.0.0.1 - 127.0.0.10</span></span>

## <span data-ttu-id="6d391-110">OS</span><span class="sxs-lookup"><span data-stu-id="6d391-110">PARAMETERS</span></span>

### <span data-ttu-id="6d391-111">-Conta</span><span class="sxs-lookup"><span data-stu-id="6d391-111">-Account</span></span>
<span data-ttu-id="6d391-112">A conta do data Lake Analytics à qual adicionar a regra de firewall</span><span class="sxs-lookup"><span data-stu-id="6d391-112">The Data Lake Analytics account to add the firewall rule to</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d391-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d391-113">-DefaultProfile</span></span>
<span data-ttu-id="6d391-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="6d391-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d391-115">-Endipaddress</span><span class="sxs-lookup"><span data-stu-id="6d391-115">-EndIpAddress</span></span>
<span data-ttu-id="6d391-116">O final do intervalo de IP válido para a regra de firewall</span><span class="sxs-lookup"><span data-stu-id="6d391-116">The end of the valid ip range for the firewall rule</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d391-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="6d391-117">-Name</span></span>
<span data-ttu-id="6d391-118">O nome da regra de firewall.</span><span class="sxs-lookup"><span data-stu-id="6d391-118">The name of the firewall rule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d391-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d391-119">-ResourceGroupName</span></span>
<span data-ttu-id="6d391-120">Nome do grupo de recursos sob o qual deseja recuperar a conta.</span><span class="sxs-lookup"><span data-stu-id="6d391-120">Name of resource group under which want to retrieve the account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d391-121">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="6d391-121">-StartIpAddress</span></span>
<span data-ttu-id="6d391-122">O início do intervalo de IP válido para a regra de firewall</span><span class="sxs-lookup"><span data-stu-id="6d391-122">The start of the valid ip range for the firewall rule</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d391-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="6d391-123">-Confirm</span></span>
<span data-ttu-id="6d391-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6d391-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d391-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6d391-125">-WhatIf</span></span>
<span data-ttu-id="6d391-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6d391-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6d391-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6d391-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d391-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d391-128">CommonParameters</span></span>
<span data-ttu-id="6d391-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d391-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d391-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6d391-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d391-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6d391-131">INPUTS</span></span>

### <span data-ttu-id="6d391-132">System. String</span><span class="sxs-lookup"><span data-stu-id="6d391-132">System.String</span></span>

## <span data-ttu-id="6d391-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6d391-133">OUTPUTS</span></span>

### <span data-ttu-id="6d391-134">Microsoft. Azure. Commands. DataLakeAnalytics. Models. DataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="6d391-134">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="6d391-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6d391-135">NOTES</span></span>

## <span data-ttu-id="6d391-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6d391-136">RELATED LINKS</span></span>


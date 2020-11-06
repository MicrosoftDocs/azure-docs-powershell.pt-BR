---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Add-AzureRmDataLakeAnalyticsFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Add-AzureRmDataLakeAnalyticsFirewallRule.md
ms.openlocfilehash: 585e0cd6a3cd74c8077833f6b5599b076c2a5db6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427964"
---
# <span data-ttu-id="d6c67-101">Add-AzureRmDataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="d6c67-101">Add-AzureRmDataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="d6c67-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d6c67-102">SYNOPSIS</span></span>
<span data-ttu-id="d6c67-103">Adiciona uma regra de firewall a uma conta do data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="d6c67-103">Adds a firewall rule to a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d6c67-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d6c67-104">SYNTAX</span></span>

```
Add-AzureRmDataLakeAnalyticsFirewallRule [-Account] <String> [-Name] <String> [-StartIpAddress] <String>
 [-EndIpAddress] <String> [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d6c67-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d6c67-105">DESCRIPTION</span></span>
<span data-ttu-id="d6c67-106">O cmdlet **Add-AzureRmDataLakeAnalyticsFirewallRule** adiciona uma regra de firewall a uma conta do Azure data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="d6c67-106">The **Add-AzureRmDataLakeAnalyticsFirewallRule** cmdlet adds a firewall rule to an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="d6c67-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d6c67-107">EXAMPLES</span></span>

### <span data-ttu-id="d6c67-108">Exemplo 1: adicionar uma regra de firewall</span><span class="sxs-lookup"><span data-stu-id="d6c67-108">Example 1: Add a firewall rule</span></span>
```
PS C:\>Add-AzureRmDataLakeAnalyticsFirewallRule -Account "ContosoAdlAcct" -Name "My firewall rule" -StartIpAddress 127.0.0.1 -EndIpAddress 127.0.0.10
```

<span data-ttu-id="d6c67-109">Esse comando adiciona a regra de firewall chamada "minha regra de firewall" da conta "ContosoAdlAcct" com o intervalo IP: 127.0.0.1-127.0.0.10</span><span class="sxs-lookup"><span data-stu-id="d6c67-109">This command adds the firewall rule named "my firewall rule" from account "ContosoAdlAcct" with the IP range: 127.0.0.1 - 127.0.0.10</span></span>

## <span data-ttu-id="d6c67-110">OS</span><span class="sxs-lookup"><span data-stu-id="d6c67-110">PARAMETERS</span></span>

### <span data-ttu-id="d6c67-111">-Conta</span><span class="sxs-lookup"><span data-stu-id="d6c67-111">-Account</span></span>
<span data-ttu-id="d6c67-112">A conta do data Lake Analytics à qual adicionar a regra de firewall</span><span class="sxs-lookup"><span data-stu-id="d6c67-112">The Data Lake Analytics account to add the firewall rule to</span></span>

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

### <span data-ttu-id="d6c67-113">-Endipaddress</span><span class="sxs-lookup"><span data-stu-id="d6c67-113">-EndIpAddress</span></span>
<span data-ttu-id="d6c67-114">O final do intervalo de IP válido para a regra de firewall</span><span class="sxs-lookup"><span data-stu-id="d6c67-114">The end of the valid ip range for the firewall rule</span></span>

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

### <span data-ttu-id="d6c67-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="d6c67-115">-Name</span></span>
<span data-ttu-id="d6c67-116">O nome da regra de firewall.</span><span class="sxs-lookup"><span data-stu-id="d6c67-116">The name of the firewall rule.</span></span>

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

### <span data-ttu-id="d6c67-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6c67-117">-ResourceGroupName</span></span>
<span data-ttu-id="d6c67-118">Nome do grupo de recursos sob o qual deseja recuperar a conta.</span><span class="sxs-lookup"><span data-stu-id="d6c67-118">Name of resource group under which want to retrieve the account.</span></span>

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

### <span data-ttu-id="d6c67-119">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="d6c67-119">-StartIpAddress</span></span>
<span data-ttu-id="d6c67-120">O início do intervalo de IP válido para a regra de firewall</span><span class="sxs-lookup"><span data-stu-id="d6c67-120">The start of the valid ip range for the firewall rule</span></span>

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

### <span data-ttu-id="d6c67-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d6c67-121">-Confirm</span></span>
<span data-ttu-id="d6c67-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d6c67-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d6c67-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d6c67-123">-WhatIf</span></span>
<span data-ttu-id="d6c67-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d6c67-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d6c67-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d6c67-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d6c67-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6c67-126">-DefaultProfile</span></span>
<span data-ttu-id="d6c67-127">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d6c67-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d6c67-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6c67-128">CommonParameters</span></span>
<span data-ttu-id="d6c67-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6c67-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6c67-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d6c67-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6c67-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d6c67-131">INPUTS</span></span>

### <span data-ttu-id="d6c67-132">System. String</span><span class="sxs-lookup"><span data-stu-id="d6c67-132">System.String</span></span>

## <span data-ttu-id="d6c67-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d6c67-133">OUTPUTS</span></span>

### <span data-ttu-id="d6c67-134">Microsoft. Azure. Commands. DataLakeAnalytics. Models. DataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="d6c67-134">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="d6c67-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d6c67-135">NOTES</span></span>

## <span data-ttu-id="d6c67-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d6c67-136">RELATED LINKS</span></span>
